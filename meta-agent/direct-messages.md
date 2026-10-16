---
title: "Direct messages"
description: "The “Direct messages” tab: first message, variables, DM instructions and the assisted generator."
section: "Meta Agent"
slug: "meta-agent/direct-messages"
---

# Direct messages

The “Direct messages” tab: first message, variables, DM instructions and the assisted generator.

_The “Direct messages” tab is where you teach the agent how to speak in private Instagram and Facebook conversations. It is only two fields, but they are what separates a generic reply from one that sounds like you wrote it._

## Where to find it <a id="dove-si-trova"></a>

Open the agent from “AI Agents” and click the “Direct messages” tab. Remember to save with the bar that appears at the bottom when you change something: until you press “Save”, your changes are not live.

## First message <a id="primo-messaggio"></a>

This is the message the agent opens the conversation with: the welcome customers read. Introduce yourself and say straight away how you can help. Keep it short — a wall of text puts people off in chat — and avoid greetings that sound robotic.

- Hotel example: “Hi! I'm Hotel Sole's assistant. I can help with availability, prices and services.”
- Restaurant example: “Hi! Go ahead: I can tell you about opening hours, the menu and bookings.”

## Variables <a id="variabili"></a>

Above the field you'll see pills with the names of the available variables: clicking one inserts a placeholder that is replaced when the message is sent (for example your business name). They let you write a message once and keep it correct even when the data changes.

## Instructions for direct messages <a id="istruzioni-dm"></a>

Here you write, in plain language, how the agent should behave: the tone (formal or friendly), what to do and what to avoid, the key information to communicate (hours, location, services, policies). Write them as you would for a new receptionist on their first day: the clearer and more complete you are, the better the replies.

- Say who you are: “You are the assistant of [business name], a hotel in Rimini”.
- Set the tone: “Reply politely and professionally, using the formal form”.
- List what it can say: hours, availability, how to book, included services.
- Set the limits: “For complaints, invite the customer to write to [contact]”.
- Remember this is chat: “Keep replies short, no phone-call phrasing”.

> [!NOTE]
> **These instructions also cover comments**
> If you leave the instructions field in the “Comments” tab empty, the agent reuses these to write public replies. If you want a different tone in public, fill in that field too.

## The instruction generator <a id="generatore"></a>

Next to the field title there's a “Generate” button. It opens a guided flow that asks a few questions about your business and produces a draft set of instructions already tuned for the Meta channel. It is a starting point: always re-read and adapt it before saving. You can regenerate as many times as you like.

> [!WARNING]
> **Mind the length**
> The counter at the top of the agent page measures how long your instructions are. If you exceed the limit, the agent cannot be switched on until you shorten them. A few clear rules beat a whole manual.

## Which language it replies in <a id="lingua"></a>

You don't need to set anything: the agent detects the language of the customer's last message and replies in that language, translating even the information taken from your documents or catalogue if it is written in another one. Feel free to write the instructions in your own language: they guide behaviour, they don't force the reply language.

## A complete example <a id="esempio-istruzioni"></a>

```text title="Instructions for direct messages"
You are the assistant of Hotel Sole, a 3-star hotel on the Rimini seafront.

TONE
- Friendly and direct, informal, short sentences as in a chat.
- Never use phone-call phrasing ("please hold", "thank you for calling").

WHAT YOU CAN DO
- Give information about rooms, services, breakfast, parking and pets.
- State the opening periods and how to reach us.
- Look up the uploaded documents for prices and house rules.

WHAT YOU MUST NOT DO
- Never confirm a booking: collect dates and number of guests and say a
  colleague will confirm shortly.
- Never promise discounts or upgrades.

WHEN YOU DON'T KNOW
- If you can't find the information, say so honestly and invite the customer
  to write to info@example.com or call reception.
```
