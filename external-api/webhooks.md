---
title: "Incoming webhooks"
description: "Receive notifications from Yourang when events occur."
section: "External APIs and developers"
slug: "external-api/webhooks"
---

# Incoming webhooks

Receive notifications from Yourang when events occur.

_Webhooks allow Yourang to notify your external system as soon as something happens, without polling. The model is simple: you register a URL, Yourang sends an HTTP POST request to it on every event of interest._

## Why webhooks instead of polling <a id="perche-webhook"></a>

Without webhooks, your system would have to call the API repeatedly to ask "did anything new happen?". It's inefficient, expensive, and introduces delays. With webhooks you receive the notification within milliseconds of the event, with the payload ready.

## Available events <a id="eventi-disponibili"></a>

- Call ended (with transcript, summary, outcome)
- New reservation
- Reservation modified
- Reservation cancelled
- New order
- Order status updated
- New contact created
- Contact fields updated
- Evaluation criterion outcome
- Workflow completed

## Configuring a webhook <a id="configurare-webhook"></a>

1. **Implement the endpoint in your system** — A public HTTPS URL that receives POST. It must respond 200 OK when the event has been accepted.
2. **Register the URL in Yourang** — Go to Administration -> API -> Webhooks, enter the URL and select the events of interest.
3. **Verify the signature** — Each payload is signed with a shared secret. Your endpoint must validate the signature to ensure the message really comes from Yourang.
4. **Test with real events** — The panel shows the log of recent deliveries with outcome (200 OK, errors). Use this log for debugging.

## Retry and reliability <a id="retry-e-affidabilita"></a>

If your endpoint responds with an error or doesn't respond in time, Yourang automatically retries following an exponential backoff strategy (e.g. 30 seconds, 5 minutes, 1 hour, ...). After several failed attempts, the event goes to a dead letter queue for manual intervention. On the endpoint, it's best to respond 200 OK immediately and process asynchronously to avoid timeouts.

> [!TIP]
> **Idempotency**
> Each payload has a unique ID. If you receive the same event twice (can happen with retries), recognize it by ID and ignore the duplicate. No unintended consequences.
