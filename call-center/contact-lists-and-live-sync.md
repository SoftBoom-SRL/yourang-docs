---
title: "Contact lists and live sync"
description: "How campaign contact lists work, what live sync does, and when to use snapshot mode instead."
section: "Call center and dialer"
slug: "call-center/contact-lists-and-live-sync"
---

# Contact lists and live sync

How campaign contact lists work, what live sync does, and when to use snapshot mode instead.

_When you set up an outbound campaign, you pick one or more contact lists. Each list behaves independently inside the campaign — including how new additions are handled while the campaign is running._

## How lists are attached to a campaign <a id="come-si-collegano-le-liste"></a>

At launch, every contact in every selected list is enqueued for dialing. From that point on, two per-list settings control what happens next: the custom fields the operator sees during the call, and the live-sync flag that decides whether mid-campaign additions are also dialed.

> [!NOTE]
> **Per list, not per campaign**
> Both settings are configured independently for each list you attach. You can mix snapshot lists and live-sync lists in the same campaign — for example, a frozen "Cold leads (Jan 2026)" list plus a live "New web sign-ups" list.

## Live sync vs. snapshot mode <a id="sync-live-vs-snapshot"></a>

Each attached list has a Live sync toggle. It controls one thing: what happens when a contact is added to that list after the campaign has already started.

- **Live sync ON** — New contacts added to the list are appended to the dialer queue automatically, as long as the campaign is in DRAFT, SCHEDULED, RUNNING, or PAUSED status. Once the campaign is COMPLETED, STOPPED, or FAILED, no further additions are picked up.
- **Live sync OFF (snapshot mode)** — The list is frozen at launch. Contacts added afterward are ignored for this specific campaign — they will only be dialed in the next campaign you launch using this list.

## When to use live sync <a id="quando-usare-sync-live"></a>

Live sync fits any list that represents a continuously growing pool: web sign-ups during a promo, leads coming in from a form, new bookings of the day. The campaign keeps working as long as new contacts arrive.

- **Hot leads dialer** — A campaign that runs all week, with sales adding qualified leads to the list as they come in. Live sync = ON.
- **Promo sign-ups** — A 48-hour campaign that calls everyone who registers during the promotion. Live sync = ON.
- **Post-purchase survey, batch of 500** — A one-shot list with no expected additions. Live sync = OFF (snapshot).

## When NOT to use live sync <a id="quando-non-usare"></a>

- **Static lists** — Lists imported once from CSV with no expected growth. Snapshot avoids accidental late additions polluting the campaign metrics.
- **A/B test cohorts** — When the campaign is measuring a specific cohort, you want the cohort frozen so the comparison stays clean.
- **Compliance-sensitive campaigns** — If the list was built inside a specific consent window, freezing the list prevents contacts whose consent hasn't been re-verified from being dialed.

## Things to know <a id="cose-da-sapere"></a>

- **Removals are never propagated** — Removing a contact from a list does not remove them from a running campaign's queue. Already-enqueued contacts will be dialed unless you stop the campaign.
- **Retry rules still apply** — Contacts that enter via live sync follow the same retry rules as the original contacts — no special treatment.
- **You can toggle live sync while the campaign runs** — The change takes effect on the next sync tick (typically within a minute). Switching OFF freezes future additions; switching ON catches up with any contacts added since the campaign launched.
- **Stopped campaigns ignore live sync** — Once a campaign reaches a terminal status (COMPLETED, STOPPED, or FAILED), no further contacts are appended regardless of the live-sync state.

> [!TIP]
> **Default is snapshot**
> Live sync is OFF by default for safety. Opt in deliberately for lists where mid-campaign growth is part of the strategy.
