---
title: "Prompt tokens"
description: "Understand and manage your assistant's prompt tokens"
section: "Voice agent"
slug: "voice-agent/token-usage"
---

# Prompt tokens

Understand and manage your assistant's prompt tokens

_Every assistant sends the model a fixed prompt on each call: your instructions, the active tools, the business context, and the FAQs. This prompt is measured in tokens and has a limit. Keeping it under control keeps the assistant fast, cost-effective, and reliable._

## What tokens are <a id="cosa-sono"></a>

Tokens are the units the model uses to read text: a common word is worth about one token, while long or rare words take up more. The indicator at the top shows the prompt's static tokens (the ones always present) against the agent's limit.

## The limit and the states <a id="il-limite"></a>

The indicator changes color based on how close you are to the limit:

**Healthy (green)**
: You are well within the limit: the assistant has enough room to reason and respond.

**Warning (yellow)**
: You are getting close to the limit. Start trimming the longest parts before adding anything else.

**Over the limit (red)**
: You have exceeded the limit: the assistant cannot be activated until you reduce the prompt.

## What consumes tokens <a id="cosa-consuma"></a>

The summary in the indicator breaks tokens down by source, so you know where to act:

**Custom instructions**
: The instructions you write for the assistant. Usually the heaviest item: this is where it's worth cutting first.

**Tool schemas**
: The description of each active tool (built-in, external, or MCP). The more active tools, the more tokens.

**Business context**
: Your business data (name, hours, address) included automatically in the prompt.

**FAQs**
: The questions and answers from your knowledge base that get included in the prompt.

## How to reduce tokens <a id="come-ridurre"></a>

- Shorten the instructions: short sentences, only the cases that really matter, no repetition.
- Turn off the tools you don't use: every active tool adds its schema to the prompt.
- Move detailed information into the FAQs instead of putting it all in the instructions.
- Review periodically: as you add features, the prompt grows without you noticing.

> [!WARNING]
> **Over the limit the agent won't activate**
> If the prompt exceeds the limit, the assistant stays disabled until you bring it back below the threshold. Keep a margin: a prompt close to the limit leaves the model little room to reason during the conversation.
