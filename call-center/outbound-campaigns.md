---
title: "Outbound campaigns"
description: "Configuring a campaign: list, script, hours, retry rules."
section: "Call center and dialer"
slug: "call-center/outbound-campaigns"
---

# Outbound campaigns

Configuring a campaign: list, script, hours, retry rules.

_An outbound campaign is the container for everything needed for a series of calls: who to call, what to say, when, how to handle those who don't answer._

## Basic configuration <a id="configurazione-base"></a>

- **Contact list** — The numbers to call. They can be selected from the CRM with filters (e.g. "hotel customers winter 2024") or uploaded from CSV.
- **AI agent** — Which voice agent runs the calls. You can have an agent dedicated to the campaign, with targeted instructions (e.g. "post-stay survey").
- **Caller ID** — The number that appears to the recipient. Yourang allows rotating multiple caller IDs to avoid spam labeling and respect regional limits.
- **Time window** — When calls go out (e.g. Mon-Fri 10:00-19:00). Never outside these windows, out of respect and by law.
- **Pace** — How many calls in parallel, how many per minute. Balances campaign speed and operator availability (in escalation mode).

## Retry rules <a id="regole-retry"></a>

Not all calls go well on the first attempt. Retry rules define what to do when: no answer, busy, voicemail, number unreachable. Typically: retry 2-3 times at intervals of several hours, spread across different days. When the number is confirmed unreachable, mark it so it isn't retried.

## Structured outcomes <a id="esiti-strutturati"></a>

Each call ends with a categorized outcome: "confirmation received", "polite refusal", "callback requested", "wrong number", etc. The list of possible outcomes is defined by you based on the campaign goal. The AI assigns the outcome based on the conversation; outcomes enable later analysis and segmentation.

> [!WARNING]
> **Respect opt-out lists**
> Those who have asked not to be contacted must not appear in campaigns. Yourang maintains a global blacklist that automatically excludes these numbers. Keeping it updated is your responsibility: simple work but crucial.
