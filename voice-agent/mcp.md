---
title: "MCP servers"
description: "Expose many remote tools through the standard Model Context Protocol."
section: "Voice agent"
slug: "voice-agent/mcp"
---

# MCP servers

Expose many remote tools through the standard Model Context Protocol.

_An MCP server (Model Context Protocol) is an endpoint that exposes one or more tools the AI can discover and use at runtime. It lets you evolve the tool set without touching the agent configuration: add a tool on your server and the AI sees it on the next discovery._

## What an MCP server is <a id="mcp-cosa"></a>

MCP is an open protocol based on JSON-RPC 2.0 over HTTP (Streamable HTTP). The server exposes primitives like tools/list and tools/call. Yourang queries your server at the start of every call to discover the tools, then exposes them to the AI as callable functions. Every invocation goes through your server, which runs the logic and replies.

## How the AI communicates with the MCP server <a id="mcp-comunicazione"></a>

1. **Initial discovery** — When the call starts, Yourang sends a tools/list request to your MCP server. The server replies with the list of tools (name, description, parameter schema). Discovery carries no customer data: it only builds the tool catalogue.
2. **MCP session** — The first response from the server returns an Mcp-Session-Id header. We reuse it on every subsequent request (tools/list and tools/call) within that voice call, so your server can keep state if needed.
3. **Exposure to the agent** — Discovered tools are passed to the AI model as callable functions, alongside built-in tools and External Tools.
4. **Invocation (tools/call)** — When the model decides to use an MCP tool, Yourang calls tools/call with the tool name + arguments. Along with the arguments we automatically attach a _meta.caller block with the customer metadata we know (see section below).
5. **Reply to the AI** — The text content of the MCP response is extracted from content[].text blocks, concatenated and returned to the model as function output. The conversation continues.

## JSON-RPC payload <a id="mcp-payload"></a>

The two requests your server will receive are simple and standard. Discovery does not pass metadata; invocation does.

#### Discovery (tools/list)

```json title="POST <server-url>"
{
 "jsonrpc": "2.0",
 "method": "tools/list",
 "params": {},
 "id": "<uuid>"
}
```

#### Invocation (tools/call)

```json title="POST <server-url>"
{
 "jsonrpc": "2.0",
 "method": "tools/call",
 "params": {
 "name": "<tool_name>",
 "arguments": { "...": "..." },
 "_meta": {
 "caller": {
 "call_sid": "<uuid della chiamata>",
 "agent_id": "<uuid dell'agente AI>",
 "organization_id": "<uuid dell'organizzazione>",
 "phone": "+39 333 1234567",
 "name": "Mario Rossi",
 "email": "mario@example.com",
 "contact_id": "<uuid contatto se trovato>"
 }
 }
 },
 "id": "<uuid>"
}
```

## Customer metadata sent automatically <a id="mcp-metadati"></a>

When the AI invokes a tool, Yourang enriches the request with a _meta.caller block carrying the current call context. They are standard fields, populated with what we already know about the customer at call time.

**call_sid**
: Unique UUID of the current call. Useful to correlate your MCP-side logs with the call history in Yourang.

**agent_id**
: UUID of the AI agent that invoked the tool. Use it if several agents share the same MCP server and you need to branch logic.

**organization_id**
: Organization (tenant) UUID. Typically the first filter you apply on your server: every call belongs to a single tenant.

**phone**
: Caller phone number in E.164 format (e.g. +1 415 555 0142), when available.

**name**
: Contact name if we already have it in the address book for that number. Absent if the caller is unknown.

**email**
: Contact email, if present in the contact record in Yourang.

**contact_id**
: UUID of the contact in Yourang if the phone matched a record in the address book. Use it to fetch more data without going through a phone-based search.

> [!TIP]
> **Metadata = already in _meta, do not duplicate in arguments**
> Do not ask the AI to pass you phone or organization_id as a tool argument: they arrive automatically in _meta.caller. Keep your parameter schema focused on user intent.

## How to configure one <a id="mcp-configurazione"></a>

1. **Open the agent configuration** — /ai-agents → select the agent → MCP tab.
2. **Enter URL and authentication** — HTTPS URL of the MCP server, authentication method (none, Bearer, API key, custom headers).
3. **Save and check the discovery** — The panel shows the number of tools discovered last time and the timestamp. You can force a new discovery with one click.
4. **Enable or disable individual tools** — Even if the server exposes 30 tools, you can enable only the 5 you need for that agent.

## Authentication and headers <a id="mcp-auth"></a>

Every MCP request always includes the standard Content-Type and Accept, plus the auth header you configured and an Mcp-Session-Id we reuse across all requests of the same voice session.

```http title="HTTP headers"
# Sempre presenti
Content-Type: application/json
Accept: application/json, text/event-stream
Mcp-Session-Id: <restituito dal server alla prima risposta>

# Auth (in base alla configurazione)
Authorization: Bearer <token>
# oppure
X-API-Key: <chiave>
```

**None**
: Public server. Only for testing or tools without sensitive data.

**Bearer**
: Authorization: Bearer <token> header on every request.

**API key**
: HTTP header of your choice (e.g. X-API-Key).

**Custom headers**
: Multiple combinations (e.g. X-Tenant + X-Signature).

## When to prefer MCP vs External Tool <a id="mcp-vs-external"></a>

- **You have many related tools** — An MCP server exposing 10 CRM tools (lookup, create, update, list, ...) is more manageable than 10 separate External Tools.
- **You want to evolve the tool catalogue** — Add tools on your server without touching the Yourang configuration: the next discovery picks them up.
- **You need to talk to a single endpoint** — An External Tool is lighter: less overhead, direct configuration.

> [!NOTE]
> **MCP is a protocol, not a service**
> The MCP server is your own application (Python, Node, Go, anything) that implements the standard. Official SDKs help you implement it quickly, even as a small 50-line script.
