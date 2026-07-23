---
title: "Configure the agent"
description: "Activation, DM reply mode, instructions, comment moderation, tools, and transcripts: every setting explained."
section: "Meta Agent"
slug: "meta-agent/configure"
---

# Configure the agent

Activation, DM reply mode, instructions, comment moderation, tools, and transcripts: every setting explained.

_The Meta agent page brings together everything that determines its behaviour. It is divided into several sub-tabs: «Agent» (the basic settings), «Instructions» (how it should speak), and «Tools» (what it can do). Let's go through them one by one._

## How to open the agent page <a id="dove-sei"></a>

Go to «AI Agents», find your Meta agent in the list and click on it. The page opens with sub-tabs at the top. If you have just created the agent, you are already here.

## Activating the agent <a id="attivazione"></a>

At the top of the page you will find an activation toggle and the agent's status: «Active» (green) or «Inactive». While the agent is inactive, messages and comments receive NO automatic reply.

- **If the toggle is locked** — It means some required fields are missing. A notice at the top of the page lists exactly what to complete (usually the name and instructions). Fill them in and the toggle will unlock.
- **Activate it only when you are ready** — It is best to activate the agent after writing the instructions and choosing the reply mode, so the first reply to a real customer is already the right one.

## DM reply mode (who replies to messages) <a id="modalita-risposta-dm"></a>

This is the most important setting: it decides WHO replies to incoming direct messages. It does not affect replies to comments, which remain managed separately. You will find a dropdown menu with three options.

- **Agent replies automatically (recommended)** — The agent handles every direct message on its own. This is the right choice in most cases: choose this if you want customers to receive an immediate reply.
- **A workflow replies** — The agent's automatic replies are disabled so that a «Meta message received» workflow can manage responses with whatever logic you prefer. Choose this ONLY if you have built (or will build) that workflow in the Workflows section.
- **Do not reply to DMs** — Messages are recorded in the inbox but receive no automatic reply: you only reply manually, by hand, from the inbox. Choose this if for now you just want to collect messages without automation.

> [!WARNING]
> **Watch out for duplicate replies**
> If you create a «Meta message received» workflow but leave the agent on «agent replies automatically», the customer will receive TWO replies. In that case set the mode to «A workflow replies». Yourang warns you with a message when it detects this overlap.

## Instructions (how the agent should speak) <a id="istruzioni"></a>

Open the «Instructions» sub-tab. Here you write, in plain language, how the agent should behave: the tone (formal or friendly), what to do and what to avoid, the key information to communicate (hours, location, services, policies). Write them as you would for a new receptionist on their first day: the clearer and more complete you are, the better the replies.

- State who you are: «You are the assistant of [business name], a hotel in Rimini».
- Set the tone: «Reply in a warm and professional manner, using formal address».
- List what it can say: hours, availability, how to book, included services.
- State the limits: «For complaints, invite them to write to [contact]».

## Comment moderation instructions <a id="moderazione-commenti"></a>

Also in the «Instructions» tab you will find a dedicated field for comment moderation. Here you tell the agent how to behave with public comments on posts: what to reply to publicly, what to redirect to private messages, and what tone to use in public. If you leave the field empty, the agent uses a sensible default behaviour.

## Tools (what the agent can do) <a id="strumenti"></a>

Open the «Tools» sub-tab. Here you enable the agent's capabilities: for example, consulting the knowledge base, which lets it answer frequently asked questions by drawing on the documents you have uploaded (menus, price lists, policies). Tools compatible with messaging appear automatically for Meta agents: enable the ones you need.

## Saving transcripts <a id="trascrizioni"></a>

Among the basic settings you will find the «Save transcripts» toggle. If you disable it, conversations continue to be recorded in the inbox but without the full message text and summary. Disable it only if you prefer to retain less data; in all other cases keep it on — it is useful for reviewing what was said.

> [!TIP]
> **Recommended order**
> Fill in the Instructions first, then choose the DM reply mode, enable the Tools you need, and finally activate the agent. That way the very first real conversation starts already well configured.
