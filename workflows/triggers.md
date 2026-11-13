---
title: "Triggers and webhooks"
description: "How to start a workflow at the right moment."
section: "Workflows"
slug: "workflows/triggers"
---

# Triggers and webhooks

How to start a workflow at the right moment.

_A workflow exists only to do something when needed. The trigger defines exactly when. Choosing the right trigger avoids wasted work and ensures automations start at the right moment._

## Event-based triggers <a id="triggers-eventi"></a>

- **New call** — Starts on every received or made call. Lets you process every conversation (e.g. tagging in CRM, evaluating criteria, archiving transcript).
- **New contact** — When a contact is added to the CRM (manually, via import, via integration).
- **New order** — When an order is created from the shop or from an external integration.
- **New reservation** — To highlight calendar-related flows: confirmations, reminders, change handling.
- **Status change** — When an entity changes status (e.g. order from "in preparation" to "ready"). Useful for reactive workflows.

## Time-based triggers <a id="triggers-temporali"></a>

For periodic workflows (e.g. daily report, weekly cleanup, monthly invoice), the time-based trigger defines the execution time. It supports cron syntax for complex patterns (e.g. "every first Monday of the month at 9").

> [!NOTE]
> **Timezone**
> Every schedule trigger has a timezone. The default is UTC: choose Europe/Rome for Italian time.

## Webhook trigger <a id="webhooks"></a>

To integrate external systems, the webhook trigger exposes a unique public URL. When the external system makes a request to that URL, the workflow starts receiving the request data. It's the most flexible way to connect Yourang to any software that supports webhooks.

> [!TIP]
> **Replying to the webhook caller**
> Add the "Reply to the app (webhook)" step where the answer is ready: the webhook waits for that step (up to 25 seconds) and returns its status code and body. This lets a workflow act as a voice-agent tool: create an External Tool pointing at the webhook URL. Voice tools wait 10 seconds at most, so reply before slow steps. If the external system cannot send the X-Webhook-Token header, add ?token=… to the URL. Anyone who sees that URL can call the workflow, so prefer the header when you can.

> [!TIP]
> **Test with a real payload**
> When you configure a webhook trigger, send a test request from the source system. The panel shows the received payload and lets you map fields to workflow variables. Avoid working "blind".
