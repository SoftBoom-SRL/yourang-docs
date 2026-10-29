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

## Creating a campaign <a id="creare-campagna"></a>

From Campaigns choose New campaign: a full-screen flow opens, with the assistant always at hand. No call starts until you start the campaign yourself.

- **Prepare with AI** — Recommended. Tell the assistant who you want to call and why: it asks a few questions, one at a time, and fills in the draft for you to review before saving.
- **Duplicate a campaign** — Start from a campaign you already have: the copy keeps the same settings and starts as a draft.
- **Set up step by step** — You choose: goal, who you call (businesses, consumers or both), who calls (assistant, operators or both), contact lists, caller ID, calling hours, outcomes to collect.

The last step is the summary: review each section, fix what you need, then press Create draft. If you leave earlier, you are asked to confirm so you do not lose your changes.

## Checks before you start <a id="controlli-prima-di-partire"></a>

The draft shows a checklist: contacts, caller IDs, assistant or operators, legal information, credit, calling hours and outcomes. Required checks block the start and each missing item links to the section to complete; recommended ones only warn you.

## Results and contacts <a id="risultati-e-contatti"></a>

The campaign page shows how many contacts were reached, the answer rate and the outcomes with percentages, also as a donut chart. Click a slice to open the calls with that outcome.

- **Contacts by status** — Search by name or number, filter by status (for example the ones not reached) and export the list to CSV.
- **Call the unreached again** — Duplicates the campaign into a new draft that calls only the contacts who were not reached, leaving the original untouched.
- **Contacts versus calls** — The chart counts contacts, the Outcomes tab counts calls: a contact called several times can appear more than once.

> [!WARNING]
> **Respect opt-out lists**
> Those who have asked not to be contacted must not appear in campaigns. Yourang maintains a global blacklist that automatically excludes these numbers. Keeping it updated is your responsibility: simple work but crucial.
