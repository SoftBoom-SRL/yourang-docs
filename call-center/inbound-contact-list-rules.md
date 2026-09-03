---
title: "Contact list rules"
description: "Dedicated routing for callers who belong to a contact list."
section: "Call center and dialer"
slug: "call-center/inbound-contact-list-rules"
---

# Contact list rules

Dedicated routing for callers who belong to a contact list.

_Contact list rules override the weekly schedule for people calling from a number already in one of your lists. They exist to treat customers you know differently: support contracts, VIP clients, running campaigns._

## How they are applied <a id="come-funzionano"></a>

When a call comes in, the system looks the number up among the organisation's contacts. If it finds it, it checks which lists the contact belongs to and which rules are active for those lists. A matching rule wins over the weekly schedule; otherwise the schedule applies as usual.

## Priority <a id="priorita"></a>

A contact can belong to several lists, so several rules can match the same call. In that case the lowest priority value wins: 1 beats 10. Give the lowest numbers to the most specific exceptions.

## Validity period <a id="validita"></a>

Each rule can have a start and an end date. Outside that range the rule is ignored and those callers follow the weekly schedule again. Leave both dates empty to keep the rule always active.

> [!WARNING]
> **Rules pointing at a deleted agent**
> As with schedule windows, if you delete an AI agent the rules that used it stay in the list but can no longer run: they are skipped and those callers follow the weekly schedule. The table flags them in red, with a warning at the top of the tab.

> [!TIP]
> **Few rules, well targeted**
> Rules are exceptions. If you find yourself with many of them and have to work out which one wins every time, that logic probably belongs in the weekly schedule instead.
