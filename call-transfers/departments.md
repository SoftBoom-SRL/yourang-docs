---
title: "Departments"
description: "Configuring destination departments to route calls to the right team."
section: "Call transfers"
slug: "call-transfers/departments"
---

# Departments

Configuring destination departments to route calls to the right team.

_Departments are the internal recipients the assistant can transfer a call to. Reception, dining room, administration, maintenance: each department is a configurable destination with its own number, hours, and rules._

## Configuring a department <a id="configurare-un-dipartimento"></a>

From the Business Information → Departments page you can create a new department specifying:

- **Name** — How the assistant identifies the department internally. Use clear, unique names (e.g. 'Reception', 'Dining', 'Management'), not abbreviations.
- **Phone number** — The number the assistant transfers the call to. It can be an internal extension, a mobile, or another VoIP number.
- **Operating hours** — When the department is available to receive calls. Outside these hours the assistant follows the after-hours flow.
- **Areas of expertise** — A brief description of the requests this department can handle. The assistant uses it to decide which department is the best fit for a specific call.
- **Priority** — When several departments could handle the same request, priority defines the order of preference. Useful for businesses with overlapping roles.

## How the assistant picks the right department <a id="come-l-assistente-sceglie"></a>

1. **Understands the request** — The AI model analyses what the customer said and identifies the main intent (booking, information, complaint, etc.).
2. **Looks for the best match** — It compares the intent with the description of every configured department and selects the most aligned one.
3. **Checks availability** — It checks the operating hours of the chosen department. If it's outside hours, it automatically escalates to the next department by priority or switches to the after-hours flow.
4. **Informs the customer and transfers** — It tells the customer who they're being passed to and why, then initiates the transfer. If the call drops or no one answers, it follows the configured fallback.

> [!NOTE]
> **How many departments?**
> Tend to keep few and well-distinct ones. Three or four clear departments are better than ten that overlap. The AI needs sharp boundaries to choose well; too many categories generate routing errors.

## Typical configuration scenarios <a id="scenari-tipici"></a>

- **Hotel** — Reception (bookings, information, check-in), Dining (table bookings, allergies), Management (complaints, special requests, events).
- **Restaurant** — Dining room (bookings for the day), Kitchen (serious allergies and intolerances), Administration (private events, invoicing).
- **B&B or small property** — Often a single department (the owner) handles everything. More important in this case is the after-hours flow.
- **Beauty centre** — Treatment room (treatment bookings), Management (packages, subscriptions, complaints), Stockroom (product sales).

## Tracking and analysis <a id="tracciamento-e-analisi"></a>

Every transfer is logged. From the Calls page, filtering by outcome 'transferred', you can see how many transfers each department receives, in which time slots, and at what answer rate. These are valuable data for sizing department staff and for understanding whether routing rules need to be revisited.
