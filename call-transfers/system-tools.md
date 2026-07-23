---
title: "System tools"
description: "The built-in tools the assistant can trigger during a call."
section: "Call transfers"
slug: "call-transfers/system-tools"
---

# System tools

The built-in tools the assistant can trigger during a call.

_System tools are the 'buttons' available to the assistant. Each tool corresponds to a concrete action that can be carried out during or at the end of a call. These include transfer mechanisms but also other operational tools._

## What system tools are <a id="cosa-sono"></a>

In the configuration, you activate the tools your assistant is authorised to use. When a condition during the call requires an action (e.g. the customer confirms a booking, or the customer asks to speak with reception), the AI model recognises the situation and triggers the corresponding tool.

## Available tools <a id="tool-disponibili"></a>

- **Call transfer** — Forwards the conversation to the most appropriate department. It's the most-used tool: we covered it in detail on the Departments page.
- **Booking** — Records a booking (room, table, treatment, slot) by collecting the necessary data and entering it into the configured system or calendar.
- **Lead capture** — Collects the customer's contact details (name, phone, email, request) and saves them in the CRM. Useful when the assistant can't close the request but wants to enable a qualified callback.
- **Send message** — Sends the customer, during or after the call, an SMS or email with useful information: confirmation link, address, price list, booking confirmation.
- **Check availability** — Queries the calendar or business system in real time to check whether a room, table, or slot is available. Allows replying with verified data rather than estimates.
- **Schedule callback** — Plans an outbound call to the customer at a future time. Useful to follow up on requests requiring checks or to reply the following day.
- **Automatic summary** — Generates a structured text summary at the end of the call and sends it to the configured recipients (e.g. to the contact person of the relevant department).
- **Transfer to a second assistant** — In advanced scenarios, the assistant can hand the call to another specialised voice agent (e.g. from generic reception to a dedicated premium service agent).

> [!TIP]
> **Activate only the tools you need**
> The more tools the assistant has available, the more decisions it has to make, and the greater the risk of suboptimal choices. Start with the tools essential for your flow (e.g. Transfer + Booking + Lead capture) and add the others only when you realise they're needed.

## How to configure a system tool <a id="configurazione"></a>

1. **Open the agent page** — Go to AI Agents → select the agent → System tools. You'll see the list of available tools with an activation toggle for each.
2. **Activate the tool** — Switch the toggle to active. For some tools you'll be asked to complete the configuration (e.g. the transfer number, the email recipient of the summary, the calendar integration).
3. **Describe when to use it** — Each tool has a description that tells the AI when to trigger it. Customise it based on your flow: the clearer the description, the more targeted the activations.
4. **Test in the Playground** — Run trial conversations in the Playground and verify that the AI triggers the tools at the right moments. If you see missed or wrong activations, refine the tool description and the agent's instructions.

## External tools and MCP servers <a id="tool-esterni"></a>

In addition to system tools, Yourang supports external tools (calls to webhooks or external APIs) and MCP servers for more advanced scenarios. They let you extend the assistant with custom logic or connect specific business systems. They're aimed at teams with technical skills: the IT contact finds dedicated instructions in the Integrations section and in Actions.
