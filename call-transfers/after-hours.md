---
title: "AI after-hours"
description: "How the assistant handles calls when the business is closed."
section: "Call transfers"
slug: "call-transfers/after-hours"
---

# AI after-hours

How the assistant handles calls when the business is closed.

_A large part of Yourang's value lies precisely outside opening hours. When the staff isn't there, the assistant keeps answering, collecting requests, taking notes, and providing basic information, preventing opportunities from being lost and customers from being left without a response._

## What changes compared to opening hours <a id="cosa-cambia-fuori-orario"></a>

- **No direct transfers** — No department is available, so transfers are replaced with other actions: collecting the request, scheduling a callback, sending a summary by email.
- **More informative style** — The assistant clearly communicates that the business is closed, gives the opening hours, and proposes concrete alternatives (callback the following morning, sending a message, online booking if available).
- **Priority on capturing the contact** — The main goal after hours isn't to close the request but to make sure the contact isn't lost: name, number, description of the request, time to be called back.

## Configuring the weekly schedule <a id="configurare-orari-AI"></a>

From the Call Center → Inbound → Weekly Schedule you can define when the 'normal hours' flow applies and when the after-hours flow takes over. You can configure different hours for each day of the week, manage extraordinary periods (holidays, bank-holiday bridges, seasonal closures), and set ad-hoc exceptions.

> [!NOTE]
> **Closure calendars**
> For recurring holidays you can use Yourang's built-in calendar, which automatically applies closure hours to Italian public holidays. For extraordinary closures, add individual exceptions with a date and description.

## Typical after-hours actions <a id="azioni-fuori-orario"></a>

- **Collecting requests** — The assistant records what the customer needs and when they want to be called back. The summary arrives by email for the staff before opening the following day.
- **Automatic confirmations** — For simple requests (hours, address, price list), the assistant replies directly. There's no need to collect the contact if the question has already been answered.
- **Autonomous bookings** — If the booking doesn't require human checks (e.g. standard table, already-defined treatment slot), the assistant can complete the operation directly and send the customer the confirmation.
- **Callback scheduling** — For requests that need to be handled manually, the assistant schedules an outbound callback for the next opening time, handled by the staff or by a second agent.
- **Smart voicemail** — If you prefer, after-hours can simply record a message from the customer, transcribe it automatically, and send it to the contact person. It's the simplest solution, suited to those who just want to avoid missing signals.

## Differences between sectors <a id="differenze-tra-settori"></a>

- **Hotel, always on** — For a hotel there's no true 'after hours': reception is 24/7. There can, however, be night-time slots where only specific requests justify a transfer, while the rest is treated as soft after-hours.
- **Restaurant, full closure** — Outside service hours the assistant collects bookings for the next day, communicates hours, and for special cases (private events) collects the contact.
- **B&B, variable** — Often the owner handles everything: during hours, the assistant transfers; after hours, it collects and emails. A simple configuration covers 95% of cases.
- **Appointment-based services (beauty centres, practices)** — After hours is prime time: many people call in the evening to book. An assistant that closes bookings autonomously in those slots can significantly increase confirmations.
