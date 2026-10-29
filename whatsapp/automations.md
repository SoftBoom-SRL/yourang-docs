---
title: "Automations"
description: "Automatic replies, routing, and after-hours management via WhatsApp."
section: "WhatsApp"
slug: "whatsapp/automations"
---

# Automations

Automatic replies, routing, and after-hours management via WhatsApp.

_Automations reply in place of the team when the message is predictable, when no one is available, or when the conversation needs to be routed to the right department._

## Types of automation <a id="tipi-di-automazione"></a>

- **Welcome message** — Sent the first time a new contact writes. It introduces the business and indicates what they can ask.
- **After-hours reply** — When a message arrives outside operating hours, it informs the customer and collects the context of the request.
- **Keyword replies** — Phrases like 'hours', 'menu', 'directions' trigger pre-configured, immediate replies.
- **Routing** — Based on content, a conversation is assigned to the correct department (e.g. messages about bookings → reception).
- **Follow-up sequences** — Messages scheduled after an event: 24 hours after check-in, one week after the order, etc.

## How to configure an automation <a id="configurare"></a>

1. **Define the trigger** — When it should fire: new contact, keyword, time, external event.
2. **Write the message** — Use variables (customer name, date, etc.) to personalise. Keep the tone consistent with the brand.
3. **Add follow-up actions** — Route to a department? Add to a list? Schedule follow-up? Automations can chain multiple actions.
4. **Test with one account** — Send a real message from a test number before going live.

> [!WARNING]
> **No blind automations**
> When a customer writes 'urgent' or 'complaint', an automation that replies 'thanks for your message' sounds indifferent. Always configure escalation keywords that bypass the automation and bring an operator in immediately.

> [!TIP]
> **Reacting to template buttons**
> In Workflows, start a workflow with the "WhatsApp message received" trigger and set it to "Button taps only" (optionally only for one template). The trigger exposes the tapped button's label, so a Switch node can send a different follow-up for each button. While the workflow handles the message, the AI agent does not answer it as well. This is the “Pause the AI reply” option of the trigger, on by default: the editor shows a warning while it is on. Turn it off if the AI should keep answering.

## Branch on buttons and delivery failures <a id="rami-pulsanti-consegna"></a>

In Workflows, the "Send WhatsApp template" step, which sends an approved template, has more than one output. One workflow can send the message and then continue in a different way depending on what happens to it, without a second workflow.

- **Always, right after sending** — Runs right after every send, without waiting for the message to be delivered or answered. Connect here what must always happen.
- **On button tap: …** — One output for each quick-reply button of the template, with the button's text after the colon. It runs when the customer taps that button on the message sent by this node, inside the same run. The outputs appear once you select the template in the node. In a node that was set up earlier, select the template again: until you do, the editor shows a notice and the button outputs do not appear. An arrow from a button the template no longer has stays visible, marked "(not in this template)", and never runs: delete it.
- **If delivery fails** — Runs when the message cannot reach that recipient: the phone number is missing or not valid, or WhatsApp refuses the message or cannot deliver it, for example because the number is not on WhatsApp. It can run at once, or later when WhatsApp reports the failure. When it runs at once, "Always, right after sending" runs too, with the send marked as not successful (whatsapp_result.success is false), and the run does not fail. Without an arrow on this output, a refused send fails the run, as before.

### How the branches behave <a id="rami-comportamento"></a>

- Draw only the arrows you need. A workflow that uses only "Always, right after sending" works exactly as before: it does not wait, and a failed send fails the run.
- Only the first tap on a button with an arrow counts. That tap is handled by the workflow: the AI agent does not answer it and it does not start "WhatsApp message received" workflows. Every other tap is handled as usual, by those workflows and by the AI agent: a tap on a button with no arrow, any tap after the one already handled, and a tap that arrives after the wait is over.
- If the step has an arrow on a button or on "If delivery fails", after sending it waits for a tap or a delivery failure for up to 168 hours (7 days) by default. To change how long, use the field "Wait for a button tap (hours)" in the step's "Options" section: from 1 to 720 hours (30 days). The wait ends earlier at the first tap on a button with an arrow or when WhatsApp reports the failure; if only "If delivery fails" has an arrow, it also ends as soon as WhatsApp confirms the message was delivered. While it waits, the run shows as "Running" in the executions list. If the time runs out, nothing else runs and the run completes.
- A run started by the "On a schedule" never waits. It sends the message and runs "Always, right after sending" (and "If delivery fails" when the phone number is missing or not valid, or WhatsApp refuses the message at the moment of sending), but it does not follow button taps or delivery reports that come later: those taps are handled as usual, by "WhatsApp message received" workflows and by the AI agent. Runs of the same workflow started by another trigger do wait.
- Problems that concern your whole WhatsApp account or the template rather than one recipient (for example no WhatsApp conversation pack, the plan's conversations used up, WhatsApp Business connection not active, missing messaging permission, a template that is paused or not approved in that language, values that do not match the template's placeholders) do not go to "If delivery fails". When they are known at the send, the run fails, as before; when WhatsApp reports them later, the wait ends and nothing else runs.
- Each arrow is independent. If a step fails on one arrow, the other arrows keep working: a button tapped later still runs its steps. The run gets the status "Failed" only when the last arrow has finished.
- If you select another template, an arrow follows the button with the same text; arrows of buttons that the new template does not have are removed. Undo brings them back.
- If you delete the workflow, its runs that are still waiting end.

### What each output provides <a id="rami-dati"></a>

**whatsapp_result (every output)**
: The outcome of the send: success, phone, template_name, message_id and, when it did not succeed, the reason in error and message.

**whatsapp_reply (button outputs)**
: The customer's tap: button_text, button_index, button_payload, replied_at, from_phone and conversation_id. For example, {{ whatsapp_reply.button_text }} is the text of the tapped button.

**whatsapp_delivery (If delivery fails)**
: Why the message was not delivered: error_code, error_title, error_message, error_scope (recipient or unknown), failed_at and source (send when the problem was known at the send, status_webhook when WhatsApp reported it later).

> [!WARNING]
> **WhatsApp Business (Meta) only**
> Button outputs and "If delivery fails" work only when the number is connected through WhatsApp Business (Meta). With another WhatsApp provider only the first output, "Always, right after sending", runs, and the editor tells you so.

> [!NOTE]
> **Costs**
> A message sent from a button arrow is a new send and is charged like any other; to answer a tap, send another template or use another channel. If you send an SMS from "If delivery fails" as a fallback, the SMS is charged on top.
