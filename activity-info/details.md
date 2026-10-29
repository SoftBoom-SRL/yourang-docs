---
title: "Business details"
description: "Name, public contacts, description and social profiles shown to customers."
section: "Business information"
slug: "activity-info/details"
---

# Business details

Name, public contacts, description and social profiles shown to customers.

_Business details are the starting point of your setup: name, public contacts, description and social profiles. Everything you fill in here is used by the AI assistant when answering calls and by your customers to recognize you._

## Main fields <a id="campi-principali"></a>

- **Business name** — The name the AI assistant introduces itself with on calls and that appears in messages sent to customers.
- **Business type** — A category that describes what you do (restaurant, hotel, beauty salon…). Helps the AI use the right vocabulary.
- **Phone and website** — Public contacts the AI can share with callers on request.
- **SMS sender** — Sender name (max 11 characters) shown on SMS messages sent from the platform.
- **Description** — A short presentation (min. 10 characters) about what you do. It's the first context the AI uses to answer general questions.

> [!TIP]
> **Generate the description with AI**
> If you don't know where to start, click “Generate with AI” next to the description field: answer a few questions and you'll get a ready-to-personalize draft.

## Social profiles <a id="profili-social"></a>

Add your main social profiles (Instagram, Facebook, LinkedIn, TikTok, YouTube, X, Snapchat or a custom site). The assistant can point callers to the right channels when they want to know more about your business.

> [!NOTE]
> For tax data, VAT number or legal company name go to Management → Account: those fields are used for billing and not for the AI context.

## Assigned phone number <a id="numero-telefono"></a>

Request a dedicated phone number that your customers can call to talk to the AI assistant. The request goes through a document review: you'll be asked for the company registry, the legal representative's ID and a recent utility bill as proof of address. Once approved, the number is shown as assigned in the details card.

- Status “Pending”: the request was submitted, wait for the team review.
- Status “Approved”: the number is active and already wired to the assistant.
- Status “Rejected”: read the reason and submit a new request with corrected data.

A phone number can be requested only while your organization has an active paid voice plan: the free plan every organization starts with and pay-as-you-go do not count. Without one, the “Request new number” button is disabled and a hint with a “Choose a plan” link takes you to the plans.

While you are on a voice plan, one number is included: the one assigned to your organization or, failing that, your oldest active number. Nothing is charged to your wallet for it when it is activated or at its monthly renewals. Each additional number is charged monthly from the wallet, starting the moment it is activated.

If the plan ends, the number is not charged but it is not kept forever either: you have a 30-day grace period to choose a plan again, then the number is released automatically (the release at the carrier is final and the number cannot be recovered). Numbers that support has marked as protected are never released automatically. In the history of previously purchased numbers, such a release appears with the reason “No active plan”.

## SIP trunk transfers to internal extensions <a id="sip-transfer"></a>

If your organization uses a Twilio SIP trunk, support configures the SIP destination used to transfer calls back to your PBX. An organization manager can see it under Business information → Phone numbers.

- Send support your PBX address (a sip: or sips: URI with one {extension} placeholder, for example sip:{extension}@pbx.example.com:5060) and, if your PBX requires it, a login for the assistant.
- Support saves it for you; to change the PBX host or the login later, contact support again. The saved password is never displayed.
- Then open AI Agents → Actions → Transfer to phone number and add each internal extension (1–6 digits), such as 226.
- Internal PBX extension legs are not charged as external phone transfers during the current SIP pilot. Normal phone-number destinations keep their displayed transfer rate.

## Verified caller IDs (Twilio only) <a id="numeri-verificati"></a>

For organizations that use Twilio as the voice provider, you can register up to 3 verified phone numbers that the AI can use as caller IDs for outbound calls. Each number requires verification through an automated call.

- Verify only the numbers you actually use to call customers.
- The verification process takes about 2-3 minutes per number.
- During the verification call, enter the code using the phone keypad (don't say it out loud).
- You can delete and add numbers at any time.
