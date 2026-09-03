---
title: "Troubleshooting"
description: "The most frequent cases where the Meta agent doesn't reply or doesn't behave as expected, in order of likelihood."
section: "Meta Agent"
slug: "meta-agent/troubleshooting"
---

# Troubleshooting

The most frequent cases where the Meta agent doesn't reply or doesn't behave as expected, in order of likelihood.

_Almost every Meta agent problem has one of six causes. Go through them in order: they are listed from the most frequent to the rarest, and most of the time the first one is the answer._

## The agent doesn't reply to any message <a id="nessun-messaggio"></a>

1. **The agent is a draft** — Open the “Agent” tab and check the toggle at the top: it must say “Active”. This is by far the most common cause.
2. **The reply mode is set to “Don't reply”** — Still in the “Agent” tab, check the “DM reply mode”: for automatic replies it must be on “The agent replies automatically”.
3. **Interactions have run out** — Look at the counter at the top: if it is red and shows zero, the agent won't reply until the period renews.
4. **The plan doesn't include the Meta agent** — If the counter shows a padlock, you need a Plus or Enterprise plan.
5. **The Meta authorisation has expired** — Go to Integrations and press “Connect” again on the Meta card, re-selecting the same Page and the same Instagram account.
6. **You're waiting less than the configured delay** — If you chose “Medium — 5 minutes” or “Slow — 15 minutes”, the reply arrives that long after the customer's last message. That is the expected behaviour.

## Facebook messages arrive but Instagram ones don't <a id="solo-facebook"></a>

Nine times out of ten the “Allow access to messages” switch inside Instagram is off (Settings → Messages and story replies → Message controls → Connected tools). Turn it on and try again. If “Connected tools” doesn't appear, the profile isn't professional or isn't linked to the Page: revisit Steps 1 and 2 of “Prepare your Meta accounts”.

## Comments get no reply <a id="commenti-non-risposti"></a>

- **The comment is yours** — The agent ignores comments published by the business profile.
- **The comment is old** — Only recent comments are handled: those on posts published before connecting aren't picked up.
- **It was hidden** — If moderation classified it as abusive, it is hidden instead of answered. You can see it in the inbox's “Comments” tab.
- **The agent isn't active** — As with DMs, with no active Meta agent nothing happens: no replies, no moderation.

## The customer receives two replies <a id="doppie-risposte"></a>

You have an active workflow with the “Meta DM received” trigger and, at the same time, the agent on “replies automatically”. Choose who should answer: if it's the workflow, set the mode to “A workflow handles replies”; if it's the agent, deactivate the workflow.

## The agent answers badly or too generically <a id="agente-muto"></a>

- **Instructions are missing** — An agent with no instructions answers vaguely. Fill in the “Direct messages” tab with tone, information and limits.
- **It has no access to your content** — If the replies never mention your prices or rules, enable the “Search the knowledge base” tool and check that you have uploaded the documents.
- **The instructions are too long** — If the counter at the top is in warning state, the agent may not be activatable: cut the fluff and keep the essential rules.
- **The public tone is wrong** — Comment replies follow the “Comments” tab: if it is empty, they reuse the DM instructions. Fill it in to differentiate the public tone.

## It replies in the wrong language <a id="lingua-sbagliata"></a>

The agent follows the language of the customer's last message. If you got a reply in the wrong language, the message was usually too short or ambiguous to identify it (an “ok” or an emoji). You can help by adding a line to the instructions, for example: “If you cannot tell the language, reply in English”.

## If none of this helps <a id="supporto"></a>

Collect three pieces of information before contacting support: the platform involved (Instagram or Facebook), the exact time of a message left unanswered, and the name of the Meta agent. With those, the check is immediate.
