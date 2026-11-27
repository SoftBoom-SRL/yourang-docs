---
title: "Call history"
description: "Browse the complete list of calls received and handled by your Yourang voice assistant."
section: "Calls"
slug: "calls/history"
---

# Call history

Browse the complete list of calls received and handled by your Yourang voice assistant.

_Call history is the centralised log of every call handled by your voice assistant. From here you can track every interaction with your guests and customers without missing a detail._

## How to access the history <a id="come-accedere-allo-storico"></a>

Go to the "Calls" section in the sidebar of your dashboard. You'll find the list of all calls in reverse chronological order, with the most recent one at the top. You can scroll the list or use the filters to quickly find a specific call.

## Information visible for each call <a id="informazioni-visibili-per-ogni-chiamata"></a>

For each entry in the history the following information is available at a glance:

- **Date and time** — The exact moment the call arrived or was started.
- **Duration** — The total length of the call in minutes and seconds.
- **Caller number** — The contact's phone number, when available.
- **Outcome** — The final result of the call (answered, abandoned, transferred, etc.).
- **Voice agent** — The name of the Yourang assistant that handled the call.
- **Property** — The property or contact point associated with the call, for those managing multiple locations.

## Outcome types <a id="tipi-di-esito"></a>

Each call is classified with an outcome that describes how it ended. Below is the meaning of each type:

**Answered**
: The assistant answered and conducted the conversation to its natural conclusion. The call took place normally.

**Reservation confirmed**
: A reservation was actually made during the call: the assistant booked it, or a custom tool you marked as making reservations ran successfully. A caller who only asks to book, without a reservation being made, is not shown as a confirmed reservation.

**Abandoned**
: The caller hung up before the assistant could answer, or during the conversation without it being completed.

**Transferred**
: The assistant recognised the need to involve a human and transferred the call to an operator or external number.

**Voicemail**
: The outbound call was not answered and the assistant left a message on voicemail, when configured.

**Unanswered**
: The system could not answer the call, for example due to a high number of simultaneous calls or a temporarily disabled configuration.

> [!NOTE]
> **Fallback model**
> If the voice model chosen for the assistant is unavailable, a fallback model handles the call instead of dropping it. In the call history the row shows a small warning triangle: hover it to see which model answered and why, and the same notice appears in the call detail. For now we set the fallback model; in the future you will be able to choose it yourself.

> [!TIP]
> **Open the detail view**
> Click any row in the history to open the detail panel. There you'll find the transcript, summary, and audio recording for the individual call.

## Call reason <a id="motivo-della-chiamata"></a>

After every call handled by the assistant, the call gets a reason: what the caller wanted, for example a booking or information about a service. The reasons come from a list made for your type of business, and you can filter the history by reason.

> [!TIP]
> **Change the list with the assistant**
> There is no settings page for the list. Ask the dashboard assistant, for example "show my call reasons", "add a reason for gift cards" or "remove the delivery reason". A removed reason stays on the calls that already have it.

## Why the caller hung up <a id="perche-ha-riattaccato"></a>

When the caller ends the call, the "Hangup reason" field says why, with one of the values below (in the call detail and as a filter in the history). Other values say who ended the call: the assistant, a timer, a transfer or an error.

**Got what they needed**
: The caller got what they needed, or the call ended with a normal goodbye.

**Not interested**
: The caller declined an offer, a survey or a sales call.

**Left at the greeting**
: The caller hung up during or right after the greeting, before asking for anything.

**Request not possible**
: The assistant did its job, but the business could not give what was asked: closed, no availability, a service not offered.

**Wanted a person**
: The caller wanted to speak to a person and no transfer was offered, or it failed.

**Assistant error**
: The assistant misunderstood, repeated itself, answered off-topic or was too slow.

**Too many questions**
: The caller gave up when asked for personal or repeated details.

**Line dropped**
: The call was cut off mid-conversation, or the caller could not hear the assistant.

**Not a real call**
: Spam, an automated message, a test call or a wrong number.

**Other**
: Any other reason.

> [!NOTE]
> **Use it to improve the assistant**
> "Wanted a person", "Assistant error" and "Too many questions" point to things you can change: transfer settings, the assistant's instructions and the details it asks for.

## Real-time updates <a id="aggiornamento-in-tempo-reale"></a>

The history updates automatically as soon as a call ends. There's no need to reload the page: new calls appear at the top of the list within a few seconds.
