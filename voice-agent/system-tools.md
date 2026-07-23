---
title: "Built-in tools"
description: "Native agent capabilities: transfers, bookings, knowledge search, call end."
section: "Voice agent"
slug: "voice-agent/system-tools"
---

# Built-in tools

Native agent capabilities: transfers, bookings, knowledge search, call end.

_Built-in tools (system tools) are ready-to-use capabilities you enable with one click. They cover the recurring use cases: transfer a call, take a reservation, search the knowledge base, end the conversation politely._

## Catalogue <a id="system-tools-catalogo"></a>

**end_the_call**
: Ends the call professionally when the conversation is complete. Always on and cannot be disabled.

**transfer_to_mobile_operator**
: Hands the call to a human operator via the mobile app. Configurable by hours and departments.

**transfer_to_phone**
: Forwards to a fixed phone number (switchboard, company mobile). Mutually exclusive with transfer_to_mobile_operator.

**transfer_to_campaign_operator**
: Forwards to an operator inside an active dialer campaign. Useful for mixed outbound + human handover scenarios.

**make_reservation**
: Creates a booking in the unified calendar, with SMS confirmation and optional Google/Apple Calendar sync.

**search_knowledge_base**
: Searches the company knowledge base (documents, manuals, price lists uploaded in the Documents section).

## Typical configuration <a id="system-tools-configurazione"></a>

1. **Open the agent's tools section** — /ai-agents → select the agent → Built-in tools tab.
2. **Enable a tool** — Toggle on/off. If a tool conflicts with another already enabled, the system blocks the change and tells you which one to disable first.
3. **Fill in required parameters** — E.g. availability hours for transfers, knowledge base to query, SMS template for bookings.
4. **Save and test** — Run a test from the playground to verify the tool activates when expected.

## Mutual exclusions <a id="system-tools-esclusioni"></a>

Some tools cannot coexist because they cover the same intent with different strategies. Example: transfer_to_mobile_operator and transfer_to_phone are mutually exclusive, you must choose whether transfers go to a human operator on the app or to a fixed number.

> [!TIP]
> **Best practices**
> Enable only the tools that are truly needed. More tools = more decisions for the model = longer response time. Start with 2-3, measure, add more only when an uncovered case emerges.

## When to prefer a built-in tool over an External Tool <a id="system-tools-vs-external"></a>

- **You need the out-of-the-box capability** — Transfer, booking, RAG: prefer the built-in tool. Already optimized and integrated with our systems.
- **You need to talk to your own system** — You need an External Tool, not a built-in one.
- **You want the standard MCP protocol** — See the dedicated page: MCP servers expose many remote tools with a single uniform protocol.
