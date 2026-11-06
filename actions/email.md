---
title: "Email campaigns"
description: "Transactional emails, newsletters, sequences: best practices and configuration."
section: "Actions and campaigns"
slug: "actions/email"
---

# Email campaigns

Transactional emails, newsletters, sequences: best practices and configuration.

_Email remains the most versatile channel for communications that need space: structured confirmations, newsletters, institutional announcements. It costs very little, but to be effective it requires care._

## Transactional vs marketing emails <a id="tipi-email"></a>

- **Transactional** — Sent in response to a customer action: booking confirmation, receipt, password reset. High delivery, no promo filters.
- **Marketing** — Sent on your initiative: newsletters, promotions, events. Require explicit opt-in and an unsubscribe link.

## Configuring the sender <a id="configurare-mittente"></a>

Before sending emails, it's essential to configure the sending domain with SPF, DKIM, and DMARC records. Yourang guides the configuration: without it, your emails often end up in spam or are rejected by servers. The setup is one-off and takes 10 minutes of work by the IT contact.

## Writing emails that work <a id="scrivere-email"></a>

- **Clear subject line** — No clickbait, no shouted caps. 'Booking confirmation 12 March - Hotel Mare' works better than 'IMPORTANT!!!'.
- **Useful preview** — The first words appear as a preview in the inbox. Put concrete information there, not 'dear customer'.
- **Responsive layout** — Over 60% of emails are read on mobile. Yourang provides responsive templates by default.
- **Visible unsubscribe link** — For marketing it's mandatory. Hiding it in tiny text breaks the law and ruins reputation.

## Automated sequences <a id="sequenze"></a>

A sequence is a series of emails scheduled after an event. Example: a 'post-stay sequence' that sends a thank-you email the day after check-out, an invitation to leave a review 3 days later, and a discount offer for the next stay 30 days later. Sequences are configured once and work on their own.
