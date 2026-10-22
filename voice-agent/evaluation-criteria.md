---
title: "Evaluation criteria"
description: "Define how the agent evaluates customer requests"
section: "Voice agent"
slug: "voice-agent/evaluation-criteria"
---

# Evaluation criteria

Define how the agent evaluates customer requests

_Evaluation criteria let the agent make smart decisions: accept a booking, transfer to an operator, or share information. They are the core of the assistant's logic._

## What evaluation criteria are <a id="cosa-sono-criteri"></a>

Criteria are yes/no rules that guide the agent's behaviour. For example: 'If the customer asks for a booking AND has all the required details AND the room is available, THEN accept the booking.'

## How to write effective criteria <a id="come-scrivere-criteri"></a>

- **Simple structure** — If [conditions] THEN [action]. Keep each criterion short and focused on one thing.
- **Explicit conditions** — Specify exactly what must be true. Not 'if the customer is happy' but 'if the customer said yes three times or confirmed verbally'.
- **Concrete actions** — Describe what to do: 'transfer to operator', 'record the booking', 'ask for the phone number'.
- **Logical order** — Criteria are evaluated top to bottom. Put the more specific cases before the generic ones.

## Practical examples <a id="esempi-pratici"></a>

- If the customer requests a booking AND provides date, party size, and room type AND the room is available, THEN proceed with the booking
- If the customer asks about services AND the answer is in the database, THEN provide the answer
- If the customer is rude OR asks to speak with the manager, THEN transfer immediately to an operator
- If the customer asks for something outside your remit AND it isn't an emergency, THEN suggest they contact the hotel at [number]
- If the customer doesn't provide the necessary information after two requests, THEN ask whether they prefer to speak with an operator
- If the customer cancels a booking AND the cancellation is within the allowed window, THEN proceed and explain the refund policy
- If the customer seems confused OR keeps misunderstanding, THEN offer them a transfer to a human operator

> [!TIP]
> **Test your criteria**
> Run criteria against real scenarios: valid bookings, cancellations, difficult customers. You'll quickly see which criteria have gaps.
