---
title: "Weekly schedule for incoming calls"
description: "Decide who answers incoming calls, hour by hour and day by day."
section: "Call center and dialer"
slug: "call-center/inbound-schedule"
---

# Weekly schedule for incoming calls

Decide who answers incoming calls, hour by hour and day by day.

_Open an inbound agent’s AI hours section to manage the organization’s shared weekly schedule. On supported Twilio connections, it decides who answers by day and time, unless a matching caller exception takes precedence. Telnyx currently bypasses this schedule._

## Windows and uncovered time <a id="finestre"></a>

A window is a range of hours on one weekday with an action attached. Unless a caller exception applies, uncovered time plays the default closed message and ends the call. Check the timezone and the complete week before saving. Use 24:00 for the end of a weekday; 23:59 retains its existing earlier boundary.

## The five available actions <a id="azioni"></a>

- **AI agent** — The voice assistant answers and handles the conversation. You must choose which inbound agent to use.
- **Transfer to the app** — The call is routed to the selected departments, who receive it inside the application.
- **Forward to a number** — The call is forwarded to an external phone number, for example the owner's mobile.
- **Call centre operator** — The caller enters the human operator queue, with configurable language, capacity and maximum wait.
- **Closed** — The caller hears a customisable closing message. Use it for holidays and planned shutdowns, not as a default.

## Starting from a template <a id="template"></a>

Templates prepare a draft for scenarios such as an always-on assistant, office hours, split hours, forwarding, operator queues and departments. Applying one can replace destinations on the affected days: review those days and agents, then Save. Changes apply only after a successful save.

## Letting your phone ring first <a id="ring-first"></a>

The schedule decides who answers by time of day, not by number of rings. If you want your phone to ring first and the assistant to answer only when you don't, turn on call forwarding on no answer on your phone towards the assistant's number, and keep the assistant as the destination here.

## If you delete an AI agent <a id="agente-eliminato"></a>

> [!WARNING]
> **The time slots using it stop working**
> Deleting an agent does not delete the time slots that used it: they stay set to AI agent with no agent attached. In those slots callers hear the closed message. The schedule flags broken time slots in red and shows a warning at the top of the page: open each flagged time slot and pick another agent.

> [!TIP]
> **A switched-off agent does not answer**
> An agent that still exists but is switched off takes no calls either. In that case the warning is yellow and the fix is quicker: turn the agent back on from the AI Agents section.
