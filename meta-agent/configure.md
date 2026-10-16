---
title: "Configure the agent"
description: "The “Agent” tab: activation, name, DM reply mode, reply delay, transcripts and the interaction counter."
section: "Meta Agent"
slug: "meta-agent/configure"
---

# Configure the agent

The “Agent” tab: activation, name, DM reply mode, reply delay, transcripts and the interaction counter.

_The Meta agent page gathers everything that drives its behaviour, split into tabs. This page covers the first one, “Agent”: the basic settings. The other tabs each have their own page in this guide._

## How to open the agent page <a id="dove-sei"></a>

Go to “AI Agents”, find your Meta agent in the list and click it. The page opens with the tabs at the top. If you have just created the agent, you are already here.

## A Meta agent's tabs <a id="le-tab"></a>

**Agent**
: Name, activation, DM reply mode, reply delay and transcript saving. This is the tab described on this page.

**Direct messages**
: The first message and the instructions that drive DM replies. See “Direct messages”.

**Comments**
: The instructions for public replies and the moderation rules. See “Comments and moderation”.

**Tools**
: What the agent can look up or do: built-in, external and MCP. See “Meta agent tools”.

**Versions**
: The history of saved configurations, with preview and restore.

> [!NOTE]
> **Why there is no “Voice & language”, “Criteria” or “Advanced”**
> Those are telephony settings: voice, spoken language, maximum call duration, recording, silence detection, call evaluation. A Meta agent writes, it doesn't speak: those tabs and fields don't appear because they would have no effect on messages. For the same reason a Meta agent has no “Playground”: you test it by actually sending a DM from another account.

## Switching the agent on <a id="attivazione"></a>

At the top of the “Agent” tab, next to the name, you'll find the activation toggle with the status: “Active” (green) or “Draft”. While the agent is not active, messages and comments get NO automatic reply: they are still recorded in the inbox.

- **No required fields to complete** — Unlike voice agents (which require a voice and a language), a Meta agent can be switched on right after creation. That doesn't make it a good idea: with no instructions it will answer generically.
- **If the toggle is locked** — The only possible block is instruction length: if your prompt exceeds the token limit shown by the counter at the top, a warning appears and activation stays disabled until you shorten it.
- **Switch it on only when you're ready** — It's best to activate the agent after writing the DM and comment instructions, so the first reply a real customer gets is already the right one.

## Agent name <a id="nome-agente"></a>

The name you recognise the agent by in the dashboard list. You can also use it in the instructions so the agent introduces itself to customers (“I'm Sofia from…”). Changing it has no effect on conversations already in progress.

## Agent type <a id="tipo-agente"></a>

It shows “Meta — Replies to Instagram and Facebook DMs” and is deliberately locked: the type is chosen at creation and a Meta agent cannot be converted into a phone agent (or vice versa).

## DM reply mode (who answers messages) <a id="modalita-risposta-dm"></a>

This is the most important setting: it decides WHO answers incoming direct messages. It has no effect on comment replies, which are handled separately from the “Comments” tab. You get a dropdown with three options.

- **The agent replies automatically (recommended)** — The agent answers every direct message on its own. This is the right choice in most cases: pick it if you want customers to get an immediate reply.
- **A workflow handles replies** — The agent's automatic reply is disabled, so a workflow started by the “Meta DM received” trigger can handle replies with the logic you prefer. Choose this ONLY if you have built (or will build) that workflow in the Workflows section.
- **Don't reply to DMs automatically** — Messages are recorded in the inbox but never get an automatic reply: you answer manually from the inbox. Choose this if for now you only want to collect messages without automation.

> [!WARNING]
> **Watch out for double replies**
> If you build a workflow with the “Meta DM received” trigger but leave the agent on “replies automatically”, the customer will get TWO answers. In that case set the mode to “A workflow handles replies”.

## DM reply delay <a id="ritardo-risposta-dm"></a>

It only appears when the mode is “The agent replies automatically”. It gives the customer time to finish writing: instead of answering the first message and then again the second and the third, the agent waits a while after the last message received and then answers the whole sequence once. It applies to direct messages only, not comments.

**Instant**
: No wait: the agent replies as soon as the message arrives. Maximum responsiveness, but with people who type in bursts you risk fragmented replies.

**Fast — 30 seconds**
: A good compromise: it groups messages fired off in a row while still feeling immediate.

**Medium — 5 minutes**
: Useful if your customers write in pieces, perhaps attaching photos or extra details in separate messages.

**Slow — 15 minutes**
: For non-urgent conversations, where you prefer one complete answer over many partial ones.

**Custom**
: You set the minutes yourself, from 0 to 30 (0.5 = 30 seconds). The countdown restarts with every new customer message.

> [!TIP]
> **Which one to pick**
> If you don't know where to start, use “Fast — 30 seconds”. It is quick enough to feel instant and patient enough not to split a message that arrived in three parts into three replies.

## Transcript saving <a id="trascrizioni"></a>

With the switch on, the text of every conversation is kept in the history, so you can re-read it and get summaries. If you turn it off, conversations are still recorded but without the text detail. Only turn it off if you prefer to store less data; otherwise keep it on.

## The interaction counter <a id="contatore-interazioni"></a>

At the top of the agent page, next to the badges, there is a pill with a speech-bubble icon and a number: those are the Meta interactions still available in the current billing period. Click it to see how many you have used, how many your plan includes and when the count resets. When the number hits zero the agent stops replying. Full details in “Plans, interactions and limits”.

## The “Versions” tab <a id="versioni"></a>

Every time you save the configuration, a copy is kept. From the “Versions” tab you can browse previous versions, open them in read-only preview (the striped background reminds you that you are looking at history, not the live configuration) and restore one if a change didn't work out.

## Recommended order <a id="ordine-consigliato"></a>

> [!TIP]
> **Recommended order**
> Write the instructions in the “Direct messages” tab first, then those in the “Comments” tab, enable the Tools you need, choose the DM reply mode and delay, and only then switch the agent on. That way the first real conversation starts from a proper configuration.
