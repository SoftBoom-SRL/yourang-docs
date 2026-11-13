---
title: "Website conversations"
description: "Reading visitors' chats and replying when they ask for a person."
section: "ChatBot"
slug: "website-chat/conversations"
---

# Website conversations

Reading visitors' chats and replying when they ask for a person.

_In the menu, under ChatBot → Conversations, you'll find every chat between visitors and the ChatBot. The number next to the entry tells you how many chats have unread messages._

## The list <a id="elenco"></a>

- **Open** — Every ongoing chat. Chats where someone waits for a person come first, longest wait first.
- **To handle** — Only chats where the visitor asked to talk to someone on your team. The waiting time turns yellow after 15 minutes and red after an hour.
- **Closed** — Chats you closed. If the visitor writes again, the chat reopens by itself.

You can search by the visitor's name, email or phone and, with more than one ChatBot, filter by ChatBot.

## When the visitor asks for a person <a id="persona"></a>

The ChatBot tells the visitor that someone on the team will reply, asks for a name and a contact, and notes the reason. At the top of the chat you see the request, the reason and how long they've waited; next to the visitor, the contact details they left and the page they're writing from.

## Replying <a id="rispondere"></a>

1. **Write your reply** — The visitor sees it in the ChatBot, marked as a reply from the team.
2. **The ChatBot pauses** — Replying takes the chat over: the ChatBot stops replying in that chat. You can also take it over without writing.
3. **Hand the chat back** — When you're done, Hand back to the assistant puts it back to work.
4. **Close the chat** — Close the chat once it's sorted. If the visitor writes again, it reopens.

## Contacts, source and files <a id="contatti-file"></a>

When a visitor leaves a name and phone number, they become a contact in the Contacts module (source “Website chat”) and you get a notice. If they are already one of your contacts, the chat is linked to it without changing it. Next to the visitor you see where they came from (the site that sent them and the campaign, for example google / cpc) and a link to the contact. Photos and PDFs they send appear under their message: one click downloads them.

## Exporting chats <a id="esportare"></a>

“Export chats” downloads a CSV file with the last 30 days of chats, one row per message, with the visitor's details and source; it opens in Excel or Google Sheets. The icon at the top of a chat exports only that one.

## Connecting a CRM or an automation <a id="webhook"></a>

With a webhook in Administration → API → Webhooks you get an event when a visitor first writes (webchat.conversation.started) and when they leave their details (webchat.lead.captured). It works with Make, n8n or your CRM.

> [!NOTE]
> **Who can reply**
> Reading conversations needs permission to view Messages; replying, taking over and closing need permission to manage them. Set this in Team.
