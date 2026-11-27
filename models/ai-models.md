---
title: "AI models"
description: "The understanding and reasoning models that decide the assistant's replies and actions."
section: "Models offered"
slug: "models/ai-models"
---

# AI models

The understanding and reasoning models that decide the assistant's replies and actions.

_The AI model is the engine that turns what the customer says into a useful answer. It's the model that decides whether the assistant can answer directly, whether it should consult the price list, whether it should query the business system to check availability, or whether to transfer the call._

## AI model tiers <a id="livelli"></a>

- **Standard model** — Balanced between quality and cost. It handles most typical hospitality requests very well: hours, simple bookings, business information, contact-data collection. It's the recommended starting point.
- **Advanced model** — Better at understanding ambiguous requests, linguistic nuances, and long-context conversations. It excels when customers ask articulated questions or when the assistant has to manage several pieces of information in parallel (dates, party size, preferences).
- **Reasoning model** — Built for complex scenarios: articulated packages, intricate availability rules, exception handling. It costs more per minute but drastically reduces cases in which the assistant makes mistakes or unnecessarily transfers the call.

## What the model actually does <a id="cosa-fa-il-modello"></a>

1. Transcribes the customer's voice into text in real time (Speech-to-Text).
2. Interprets the request based on the instructions you've configured.
3. Decides whether to reply with its own information, consult a knowledge base, trigger an integrated tool, or transfer the call.
4. Composes the answer in natural language and hands it to the voice model for pronunciation.

> [!TIP]
> **The model is not all-powerful**
> Even the best model follows the instructions you give it. Investing 30 minutes in writing the agent's instructions well brings more improvement than switching to a more expensive model with vague instructions.

## When it's worth upgrading to a more advanced model <a id="quando-vale-la-pena-salire"></a>

- **Detail-heavy conversations** — If your bookings include variables (number of guests, flexible dates, multiple preferences), the advanced model handles it all without losing information.
- **International customers** — The advanced model better understands non-native accents and code-switching (mixing different languages in the same sentence).
- **Reducing transfers** — If you notice the assistant often transfers calls it could have handled, upgrading to a higher model can raise the rate of calls resolved autonomously.
- **Fine-grained evaluation criteria** — If you use sophisticated criteria to categorise call outcomes, an advanced model classifies with more precision and makes subsequent analysis more reliable.

## Privacy and data handling <a id="privacy-e-dati"></a>

The AI models used by Yourang are hosted in GDPR-compliant data centres. Conversations are processed to deliver the response in real time and then stored encrypted on our systems, accessible only to your organisation. Data is not used to train general models and is not shared with third parties for commercial purposes.
