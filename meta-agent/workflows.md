---
title: "Meta in workflows"
description: "Triggers, agent node and Meta actions for building custom automations instead of the automatic reply."
section: "Meta Agent"
slug: "meta-agent/workflows"
---

# Meta in workflows

Triggers, agent node and Meta actions for building custom automations instead of the automatic reply.

_If the agent's automatic reply isn't enough — you want to filter, decide, notify someone or record a contact before replying — you can handle Meta inside a workflow. The Workflows section provides triggers, an agent node and a send action._

## When a workflow is worth it <a id="quando-usarli"></a>

- You only want to reply to certain messages (for example those containing a keyword) and ignore the rest.
- You want to save the contact, open a ticket or notify the team before or after replying.
- You want the reply to go through a condition or a wait.
- You want to process the leads collected by Meta's ad forms.

> [!NOTE]
> **Most of the time you don't need this**
> If all you need is for the agent to answer messages well, leave the mode on “The agent replies automatically” and ignore this page. Workflows are for specific needs.

## “Private message received” trigger <a id="trigger-dm"></a>

Starts the workflow when a direct message arrives on Instagram or Facebook. You can restrict it to a single platform or leave it on both, and choose which connected Meta account to listen on. The received message and the sender's details are available to the following nodes. It also starts when the customer sends only a photo, voice note or file: the message text is then empty.

## “AI social reply” step <a id="nodo-agente-meta"></a>

Has the reply written by the brain of a Meta agent you already configured: you choose which agent and what text to feed it. The node returns the reply as data without sending it: you decide whether and how to send it, for example with the send node below. This way you reuse the agent's instructions, documents and tools inside your own logic.

## “Send private message” action <a id="azione-invia-dm"></a>

Sends a direct message to a person on Instagram or Facebook. You specify the Meta account, the recipient (usually taken from the trigger) and the text, which can be the one produced by the “AI social reply” step or a fixed text. Remember the 24-hour window: outside it, Meta may refuse the send.

## “New contact from an ad” trigger <a id="lead-ads"></a>

Starts the workflow when someone fills in a contact form linked to your Meta ads. You choose the account, the Page and the form to listen on. The answers reach the workflow already sorted: the variable picker offers the first name, last name, full name, email, phone number (in international format), every answer of the form by its question key (custom questions included) and the contact saved from the lead, so you can use them in the following nodes without any mapping. With the “Save Leads as Contacts” option of the Meta integration on, a lead with a valid phone number is also saved in your address book: a new contact is created, while an existing one only gets its blank fields filled and nothing is overwritten. A lead without a valid phone number is not saved as a contact, but the workflow runs anyway.

## Avoiding double replies <a id="evitare-doppie-risposte"></a>

> [!WARNING]
> **One rule to remember**
> If a workflow replies to DMs, the agent must not: open the “Agent” tab and set the DM reply mode to “A workflow handles replies”. Otherwise the customer will get two answers to the same message.
