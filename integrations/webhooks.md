---
title: "Outbound webhooks"
description: "Technical notifications to your systems"
section: "Integrations"
slug: "integrations/webhooks"
---

# Outbound webhooks

Technical notifications to your systems

_Webhooks allow Yourang to "notify" your systems when something happens: a reservation, a call ended, a message sent. If you have your own software, you can make it react to these events._

## What webhooks are <a id="cosa-sono-webhook"></a>

A webhook is an automatic notification. When an event happens in Yourang, it sends a message (a "notification") to your system. Your system receives it and can take consequential actions.

Example: when a reservation is created, Yourang notifies your accounting system, which automatically creates an invoice.

## Which events trigger webhooks <a id="quali-eventi"></a>

- Reservation created
- Reservation cancelled
- Reservation modified
- Call ended
- WhatsApp message sent
- Feedback received

## How to configure webhooks <a id="come-configurare"></a>

1. **Go to Integrations > Webhooks** — Open the webhooks configuration panel
2. **Paste your system's URL** — Yourang will send messages to that address (your software must have a receiver)
3. **Choose the events** — Select which events you want to receive (reservations, calls, messages...)

> [!NOTE]
> **For those with their own system**
> Webhooks are intended for users with custom software. If you use standard tools (Google Calendar, email, SMS), you don't need webhooks. If instead you have your own app or database, webhooks let you connect it to Yourang.

The technical configuration of webhooks requires programming skills. If you don't know what a URL endpoint is or how to receive HTTP requests, contact your developer.
