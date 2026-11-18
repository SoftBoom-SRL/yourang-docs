---
title: "Meta agent tools"
description: "What a Meta agent can look up and do: knowledge base, catalogue, external tools and MCP servers."
section: "Meta Agent"
slug: "meta-agent/tools"
---

# Meta agent tools

What a Meta agent can look up and do: knowledge base, catalogue, external tools and MCP servers.

_“Tools” are the capabilities you give the agent beyond conversation: searching a document, checking the price list, calling one of your systems. A Meta agent has a shorter list than a phone agent, because anything call-related makes no sense in chat._

## Where to find them <a id="dove-si-trovano"></a>

Open the agent and click the “Tools” tab. Below it there are three sub-tabs: “Built-in”, “External” and “MCP”. Each tool is enabled with a switch and, where applicable, configured by opening the side panel.

## Built-in <a id="strumenti-predefiniti"></a>

These are the platform's ready-made tools. For a Meta agent the list is filtered automatically: only the ones that work on a text channel appear.

**Search the knowledge base**
: Lets the agent look up the documents you uploaded (menus, price lists, house rules, FAQs) and answer by quoting their content instead of improvising. It is by far the most useful tool: switch it on almost always.

**Search the catalogue**
: Lets the agent search your business's catalogue for products and services and report their name, description and price. Designed for channels that answer questions without taking orders.

> [!NOTE]
> **Why you don't see the other built-in tools**
> Call transfer, ending the call, creating orders and bookings, saving the contact and scheduling a callback only exist inside a phone call: with no call in progress they would have nothing to act on, so they don't appear for Meta agents.

## External <a id="strumenti-esterni"></a>

These are calls to your own systems: a management system, a CRM, an endpoint on your website. You define the address, method, headers and parameters, and the agent can use it when needed. They work the same way on calls and messages: a Meta agent can use the external tools you have configured.

> [!TIP]
> **Remember you're in chat**
> A tool that answers in 10 seconds goes unnoticed on the phone but is an eternity in chat, where the customer only sees silence. Prefer fast endpoints and compact responses.

## MCP servers <a id="mcp"></a>

An MCP server is a standard way to expose a whole group of tools to the agent (for example those of software you already use) without configuring them one by one. If you connect one, its tools become available to the Meta agent too.

## In short: what it can and cannot do <a id="non-disponibili"></a>

- **It can** — Look up documents and the catalogue, query your systems through external or MCP tools, reply and moderate on Instagram and Facebook.
- **It cannot** — Make calls, transfer a call, end a call, create orders and bookings on its own, send SMS. For those steps, hand the conversation to a person or build a workflow.
