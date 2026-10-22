---
title: "What workflows are"
description: "The visual way to orchestrate multiple actions and decisions in a single automation."
section: "Workflows"
slug: "workflows/overview"
---

# What workflows are

The visual way to orchestrate multiple actions and decisions in a single automation.

_Workflows are visual diagrams that describe step by step what should happen when an event occurs. Think of them as an assembly line: at each station there's an action, a decision, or a wait._

## Why single actions aren't enough <a id="perche-non-bastano-le-azioni"></a>

A single action (send an SMS, update a contact) solves a simple case. But many real processes are more complex: "if the customer doesn't reply within 2 hours, send an email; if that doesn't work either, schedule a phone callback". Workflows let you express these conditional sequences without writing code.

## Typical examples <a id="esempi-tipici"></a>

- **Multi-channel reminders** — Send SMS 24 hours before the appointment. If unread, send WhatsApp 12 hours before. If still silent, call 1 hour before.
- **New customer onboarding** — When a new contact registers, send a welcome email, wait 3 days, send the services guide, wait a week, ask for feedback.
- **Lead handling** — When a new lead arrives, qualify it via AI based on the request; if interesting, create a task for the sales team, otherwise reply automatically with information.
- **No-show recovery** — If a reservation results in a no-show, send WhatsApp after 1 hour asking if rescheduling is needed; if positive, open available slots; if negative, archive.

> [!TIP]
> **Start from a real case, not from theory**
> The best way to learn workflows is to take a process you currently do manually and rebuild it in the system. You'll immediately see where decisions, waits, and branches are needed.
