---
title: "External Tools"
description: "Custom webhooks the AI agent can call during a conversation."
section: "Voice agent"
slug: "voice-agent/external-tools"
---

# External Tools

Custom webhooks the AI agent can call during a conversation.

_External Tools are HTTP webhooks you configure: the voice agent invokes them in real time to fetch data or trigger actions in your systems (CRM, business software, custom automations)._

## What they are <a id="external-tools-cosa"></a>

An External Tool is a function that lives on your server. Yourang registers it as an available tool for the AI agent: when the model decides that action is needed (e.g. look up a customer in the CRM, check room availability), it sends an HTTP request to the URL you configured.

## How to configure <a id="external-tools-configurazione"></a>

1. **Open the agent tools panel** — Go to /ai-agents → select the agent → Tools tab → External tools.
2. **Set name and description** — The internal name (tool_name) is a technical identifier (e.g. lookup_customer). The description tells the AI when to use the tool: keep it clear, concrete, focused on user intent.
3. **Set up the webhook** — HTTPS URL that will receive the calls, method (GET/POST/PUT), parameter schema (JSON Schema) that the AI will pass to the payload.
4. **Configure authentication** — None, Bearer token, API key in a header, Basic auth, or multiple custom headers. Credentials are encrypted at rest.
5. **Test with a trial call** — Start the agent in playground and ask something that should trigger the tool. The call log shows request, response and timings.

## Authentication <a id="external-tools-auth"></a>

**None**
: Public endpoint, no headers. Not recommended in production.

**API key**
: Sent in your chosen HTTP header (e.g. X-API-Key).

**Bearer**
: Authorization: Bearer <token> header.

**Basic**
: Authorization: Basic <base64(user:pass)>.

**Custom header**
: One or more arbitrary headers (e.g. X-Tenant, X-Signature).

## When to use them <a id="external-tools-casi"></a>

- **CRM lookup** — The agent searches a customer by phone number and tailors the answer with their data.
- **Business system availability** — The agent asks the PMS whether there are free rooms on a given date.
- **Ticket creation** — The agent logs a complaint as a ticket in your customer-care system.
- **Order update** — The agent changes the status of an order already handled in your e-commerce.

> [!TIP]
> **Keep tools focused**
> One tool per action. Generic tools (e.g. 'do_something' with 20 optional parameters) confuse the AI and produce wrong calls. Three specific tools beat a single Swiss-Army knife.

## Example request <a id="external-tools-esempio"></a>

```json title="POST /tools/lookup-customer"
{
 "phone": "+1 415 555 0142",
 "call_id": "cl_abc123",
 "organization_id": "org_xyz"
}

# Expected response (200 OK):
{
 "found": true,
 "customer": {
 "name": "Jane Doe",
 "tier": "gold",
 "last_order_date": "2026-03-12"
 }
}
```
