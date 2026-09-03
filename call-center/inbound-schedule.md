---
title: "Weekly schedule for incoming calls"
description: "Decide who answers incoming calls, hour by hour and day by day."
section: "Call center and dialer"
slug: "call-center/inbound-schedule"
---

# Weekly schedule for incoming calls

Decide who answers incoming calls, hour by hour and day by day.

_The weekly schedule decides who answers an incoming call based on the day and time it arrives. It is the foundation of Inbound Call Center: without at least one window, no call is handled._

## Windows and uncovered time <a id="finestre"></a>

A window is a range of hours on a single day, with an action attached to it. Time that no window covers is treated as closed: the caller hears the closing message and the call ends there. That is why it pays to cover all 24 hours of every day, leaving the AI assistant in charge of the hours when nobody is in the office.

## The five available actions <a id="azioni"></a>

- **AI agent** — The voice assistant answers and handles the conversation. You must choose which inbound agent to use.
- **Transfer to the app** — The call is routed to the selected departments, who receive it inside the application.
- **Forward to a number** — The call is forwarded to an external phone number, for example the owner's mobile.
- **Call centre operator** — The caller enters the human operator queue, with configurable language, capacity and maximum wait.
- **Closed** — The caller hears a customisable closing message. Use it for holidays and planned shutdowns, not as a default.

## Starting from a template <a id="template"></a>

The Templates button offers ready-made weeks for the most common scenarios: always-on assistant, office hours with forwarding to your number, split hours with a lunch break, out-of-hours on call, operator queue, departments. Every template covers the whole week and gives the AI assistant the uncovered hours, so the service never stops. Applying a template replaces the windows on the days it touches.

## If you delete an AI agent <a id="agente-eliminato"></a>

> [!WARNING]
> **The windows using it stop working**
> Deleting an agent does not delete the windows that used it: they stay set to AI agent with no agent attached. Calls landing in those ranges are treated as a closure. The schedule flags broken windows in red and shows a warning at the top of the page: open each flagged window and pick another agent.

> [!TIP]
> **A switched-off agent does not answer**
> An agent that still exists but is switched off takes no calls either. In that case the warning is yellow and the fix is quicker: turn the agent back on from the AI Agents section.
