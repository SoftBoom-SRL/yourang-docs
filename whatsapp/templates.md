---
title: "Approved templates"
description: "How to create and use templates needed to write outside the 24-hour window."
section: "WhatsApp"
slug: "whatsapp/templates"
---

# Approved templates

How to create and use templates needed to write outside the 24-hour window.

_WhatsApp Business enforces strict rules: beyond the 24-hour window from the customer's last message, you can only write using templates approved by Meta. It's an anti-spam protection, but it's also a powerful tool for proactive communications._

## When templates are needed <a id="quando-servono"></a>

- Reminders for appointments or scheduled bookings
- Order or shipping confirmations
- Marketing campaigns to a contact list
- Alerts about hour or service changes
- Invitations to reviews or surveys

## Template categories <a id="categorie"></a>

- **Utility** — Confirmations, reminders, transaction updates. Fast approval, low cost.
- **Marketing** — Promotions, campaigns, news. Requires explicit customer consent. Higher cost.
- **Authentication** — OTPs and verification codes. More technical use case, less common for hospitality businesses.

## Creating a template <a id="creare-template"></a>

1. **What it's for** — Pick the language and the category: each category says what it is for with an example. The name is only for you: leave it empty and it is taken from the first words of the message. To start faster, pick “Appointment reminder”, “Promotion” or “Order update” under “Start from an example”: the form fills in and you can change everything.
2. **Write the message** — Write the text, with personalised fields in braces for what changes for each customer: 'Hi {{customer name}}, your booking on {{date}} is confirmed.' Only you see the names; Meta receives {{1}}, {{2}}, in the order they appear. “Add personalised field” adds the next number with its digits selected: type a name over them, then press Enter or → to keep writing. Add a header (a title, image or video), a footer and buttons if you need them. A link button can have a dynamic last part: choose "Dynamic", write the first part of the address and an example value for Meta, and the last part is filled in for each recipient in campaigns and workflows.
3. **Review and send to Meta** — The phone on the right shows the message as the customer will see it, at every step. The examples Meta needs for the personalised fields are filled in for you where the field's name says what it is (Meta's reviewers read them, customers never do): check them and submit: Meta usually approves it within minutes, at most 24 hours.
4. **Use the template** — Once approved, the template is available in chat, automations, and campaigns. There too a phone shows the message with the values filled in.

> [!NOTE]
> **Writing rules**
> Meta rejects templates with aggressive sales language, grammatical errors, links to suspicious domains, or improperly used variables. Keep a tone that is helpful, clear, and honest.

> [!NOTE]
> **Editing a template**
> Click a template in the list to see how it is configured. Approved, rejected and paused templates can be edited and resubmitted to Meta for review; an approved template can be changed once every 24 hours and keeps its category. Templates under review can only be viewed.

> [!NOTE]
> **Naming the variables**
> Write the name straight in the text, in braces: “Hi {{first name}}” instead of “Hi {{1}}”. The name is only for you: the customer never sees it and Meta still receives {{1}}, {{2}}, numbered in the order the variables appear. If you rename a variable in braces and change nothing else, only the names are saved and the template does not go back to review; moving named variables around renumbers them, so check the campaigns and workflows that use the template. The names show up where you fill in the values, in campaigns and workflows. The variable in a button's link, and those of a template that cannot be edited (for example one under review), are named in the “Names of the variables” section.

> [!NOTE]
> **An image on top (banner)**
> In the «Header» field choose «Image» and upload a JPG or PNG up to 5 MB: the preview shows it above the text. The image goes to Meta with the template for review, then appears at the top of every message sent with that template, from campaigns, workflows and the API. To change it, edit the template: the new image goes through Meta's review again.

> [!NOTE]
> **A video on top**
> In the «Header» field choose «Video» and upload an MP4 or 3GPP file (H.264 video, AAC audio) up to 16 MB; a larger file is refused before it is uploaded. The preview plays it above the text, and every message sent with the template carries it, from campaigns, workflows and the API, after Meta's review.
