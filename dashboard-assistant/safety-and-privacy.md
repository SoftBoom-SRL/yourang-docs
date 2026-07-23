---
title: "Safety and privacy"
description: "How the assistant protects your data, why it always asks for confirmation before making changes, and how it behaves based on the role of who is using it."
section: "Dashboard Assistant"
slug: "dashboard-assistant/safety-and-privacy"
status: "beta"
---

# Safety and privacy

How the assistant protects your data, why it always asks for confirmation before making changes, and how it behaves based on the role of who is using it.

_The assistant was designed with safety in mind from day one. It only sees your data, respects the roles you assigned to your team, and always gives you the final say before touching anything._

## It only sees your data <a id="vede-solo-i-tuoi-dati"></a>

Every request you send is executed under your identity. If you ask for calls, you receive exactly your calls, not another company's. When you switch organisation from the top menu, the assistant automatically opens a new conversation: data from different organisations is never mixed.

## Roles and permissions <a id="ruoli-e-permessi"></a>

The assistant respects team roles: anyone can only do, through the assistant, what they could do manually from the dashboard. If you ask for an action your role doesn't allow, the assistant tells you politely.

**Member**
: Can read calls, contacts, KPIs, FAQs, documents and the business profile. Can change personal preferences. Cannot change the company or agent configuration.

**Admin**
: Everything a Member can do, plus: create and update voice agents, add FAQs and contacts, update hours, address, departments and social links, ask the assistant to read web pages.

**Owner**
: All Admin functions. No additional restrictions on the assistant compared to Admin.

## Confirmation before changes <a id="conferma-prima-di-modificare"></a>

For every change to your data the assistant opens a confirmation card with a summary of the action and an impact level: low, medium or high. High impact is reserved for actions that change information visible to your customers or operators (hours, address, company info, deleting a department). Nothing is applied until you click Confirm.

> [!NOTE]
> **Targeted changes**
> When you update a piece of data, the assistant only touches that piece. Everything else (other opening hours, other profile fields) stays intact. There is no risk of overwriting information you didn't mention.

## Activity log <a id="registro-attivita"></a>

All interactions with the assistant are logged: who wrote what, which tools the assistant used, which changes were applied. The log is internal and lets us monitor service quality and you reconstruct any configuration change after the fact.

## Abuse protections <a id="protezioni-contro-abusi"></a>

- **Message rate limit** — To prevent excessive consumption, there is a cap on messages per minute per person. If you ever hit it, the assistant asks you to wait a few seconds.
- **Limited web-page reading** — The assistant can read links you paste, but only public pages, with an hourly cap and a maximum size. It cannot reach private networks or internal systems.
- **Content treated as text** — If a call transcript or web page contains instructions trying to manipulate the assistant, they are treated as text to report, not as commands to execute.

> [!WARNING]
> **When in doubt**
> If the assistant proposes an action you don't recognise or a change you didn't request, don't confirm it: cancel and contact support. Without your confirmation, nothing is ever changed.
