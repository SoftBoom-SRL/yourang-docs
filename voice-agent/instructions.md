---
title: "Instructions"
description: "Write effective instructions for the voice agent"
section: "Voice agent"
slug: "voice-agent/instructions"
---

# Instructions

Write effective instructions for the voice agent

_Instructions guide the agent's behaviour in every situation. Clear, well-structured instructions deliver consistent and appropriate responses._

## Three core principles <a id="tre-principi"></a>

- **Clarity** — Write simple, direct sentences. Avoid ambiguity, technical jargon, and circumlocutions. The agent must understand exactly what to do.
- **Specificity** — Don't say 'be polite': explain how and when. For example, 'if the customer asks about hours, reply with the exact time and add: we want to make sure everything is perfect for you'.
- **Completeness** — Anticipate edge cases and exceptions. Specify what to do if the agent doesn't know the answer or if the customer becomes rude.

## What to include in the instructions <a id="cosa-includere"></a>

**Role and purpose**
: Who you are and what your main mission is (e.g. booking support, service information).

**Available information**
: Data the agent can provide: rates, hours, available services, business rules.

**Actions you can take**
: What you can do: accept bookings, change dates, give information about packages.

**Situations requiring an operator**
: Which requests must be transferred to a human operator (complaints, complex requests).

**Security protocols**
: How to handle sensitive data: never ask for passwords, never share confidential information.

**Behaviour when misunderstanding occurs**
: How to react when you don't understand: ask the customer to repeat, suggest alternatives, offer human support.

## Dynamic variables <a id="variabili-dinamiche"></a>

You can personalize every call by inserting variables wrapped in double curly braces: during the call they are automatically replaced with the contact's real data. They work both in the instructions and in the first message. Use the buttons above the editor to insert them without typing them by hand.

**{{first_name}}**
: The contact's first name.

**{{last_name}}**
: The contact's last name.

**{{full_name}}**
: First and last name together.

**{{phone}}**
: The contact's phone number.

**{{email}}**
: The contact's email.

**{{business_name}}**
: Your business name.

**{{custom.field_name}}**
: A contact custom field (e.g. {{custom.preferred_room}}).

```text
Hello {{first_name}}, this is Anna and I'm calling about...
```

Default value (fallback): if a value might be missing, add a default after a pipe. It is only used when the variable is empty.

```text
Hello {{first_name | "there"}}!
```

> [!TIP]
> **Always plan a fallback**
> If the contact has no value for that field (for example a call from an unknown number, with no name) and you haven't set a fallback, the variable stays empty. As an alternative to the fallback, you can tell the agent what to do, e.g. "if you don't know the name, politely ask who you're speaking with".

> [!WARNING]
> **Inconsistent instructions cause problems**
> If the instructions contradict each other (e.g. 'reply in 10 seconds' but also 'always double-check information'), the agent will give unpredictable answers. Always check internal consistency.
