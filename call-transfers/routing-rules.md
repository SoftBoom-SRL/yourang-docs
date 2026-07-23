---
title: "Routing rules"
description: "Mapping requests to the right destination in a predictable and transparent way."
section: "Call transfers"
slug: "call-transfers/routing-rules"
---

# Routing rules

Mapping requests to the right destination in a predictable and transparent way.

_When departments, system tools, and after-hours work together, routing rules define who-does-what in every situation. A clear map prevents unpredictable behaviour and makes the assistant reliable over time._

## The three layers of the decision <a id="i-tre-piani"></a>

1. Moment layer: what time slot are we in? Open or after hours?
2. Content layer: what type of request is it? Booking, information, complaint, emergency?
3. Destination layer: which department or tool is the best fit? Is it available? Is there a fallback?

The assistant goes through these three layers in order: first it understands what context it's in, then what the customer needs, then who to pass the ball to. The rules you configure define exactly these three steps.

## Common routing patterns <a id="pattern-comuni"></a>

- **Direct match** — A clear request → a department. E.g. 'I'd like to book a table for tonight' → Dining room.
- **Match with verification** — The assistant checks a condition before choosing. E.g. 'Is the double room available?' → Check availability → if yes, booking; if no, alternative proposed by reception.
- **Destination cascade** — Try the primary department, if it doesn't answer pass to the secondary. E.g. Reception → Management → Smart voicemail.
- **Routing by time** — Same request, different destination based on time. E.g. 'I'd like to speak with the manager' → during day hours transfers to Management, in the evening records a callback request.
- **Routing by customer** — For customers recognised by the CRM (e.g. VIP customers or program members), routing can skip to the dedicated department without going through reception.

> [!WARNING]
> **Avoid conflicts**
> When two departments have descriptions that overlap or ambiguous hours, the AI can make unstable choices (today it routes to one, tomorrow to another). Use priority and precise descriptions to avoid this.

## Test the rules before going to production <a id="testare-le-regole"></a>

The Playground lets you simulate conversations and verify how the assistant routes. Prepare a set of 'test cases' that cover your main scenarios (open/closed, typical/atypical requests, error handling) and verify that routing is consistent. It's a half-hour investment that prevents days of real-world problems.

## Monitoring and correcting over time <a id="monitorare-e-correggere"></a>

- **Routing statistics** — From the Calls page you can filter by department and see how many routings it receives, in which hours, and at what answer rate.
- **Failed transfers** — Calls transferred but unanswered are a signal: the department is understaffed, the hours are wrong, or the fallback isn't well configured.
- **Outcomes by category** — If evaluation criteria show many 'unhandled' or 'customer dissatisfied' outcomes in a certain category, it's worth revisiting the routing rules for that type of request.
- **Staff feedback** — Whoever receives the transfers knows perfectly well whether the assistant routes well or badly. A short monthly review with the operational team often surfaces more than a thousand dashboards.

> [!TIP]
> **Rules grow with you**
> Starting simple is the right move: two or three departments, clear rules, basic after-hours. Add complexity only when volume and feedback justify it. A platform with intricate but well-maintained rules works better than one with unnecessarily sophisticated rules that are never updated.
