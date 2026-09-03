---
title: "Advanced settings"
description: "Fine-tune creativity, speed, and turn detection"
section: "Voice agent"
slug: "voice-agent/advanced-settings"
---

# Advanced settings

Fine-tune creativity, speed, and turn detection

_Advanced settings let you fine-tune the conversational behavior of the voice assistant. The default values work well in most cases: change them only when you have a specific problem to solve, one parameter at a time._

> [!NOTE]
> **Availability by model**
> Not all options are available for every voice model. OpenAI offers the most complete control; the other models expose a subset. The fields not supported by the chosen model appear disabled.

## Temperature <a id="temperatura"></a>

Temperature controls how variable and creative the assistant's responses are. Low values make responses more predictable and consistent; high values make them more natural and varied, but with a greater risk of going off track. The range goes from 0.6 to 1.2, with 0.8 as the default value.

**Low (0.6-0.7)**
: Very consistent and repeatable responses. Ideal when precise factual information is needed, such as hours, prices, and availability.

**Medium (0.8, recommended)**
: A good balance between consistency and naturalness. Suitable for most activities.

**High (1.0-1.2)**
: Warmer, more conversational responses. Useful for hospitality and rapport, less suited to communicating critical data.

> [!TIP]
> **When to raise or lower it**
> If the assistant sounds robotic or repetitive, raise the temperature slightly. If it invents details or strays from the script, lower it.

## Response speed <a id="velocita"></a>

Adjusts how fast the assistant pronounces its responses; the default value is 1.0 and the available range depends on the voice model. An appropriate speed improves comprehension without making the conversation feel unnatural.

- **Slower** — Improves comprehension for elderly customers, non-native speakers, or complex topics such as procedures and addresses.
- **Faster** — Suitable for short, dynamic conversations with customers who already know the service.

## Turn detection <a id="rilevamento-turno"></a>

Turn detection decides when the assistant understands that you have finished speaking and can respond. Good tuning avoids two opposite problems: the assistant that interrupts too soon and the assistant that makes you wait too long before responding.

With OpenAI you can choose between two detection modes:

**Semantic (semantic VAD)**
: The assistant also evaluates the meaning of the sentence to understand whether it is complete. More natural in real conversations; it is adjusted with responsiveness.

**Threshold-based (server VAD)**
: The assistant relies on voice volume and the duration of silence. More predictable in noisy environments; it is adjusted with threshold and silence duration.

- **Responsiveness** — How quickly the assistant steps in (automatic, low, medium, high). High steps in as soon as it perceives a pause; low leaves more room for the customer and is recommended with people who speak slowly.
- **Threshold** — How loud the audio must be to be considered speech (from 0 to 0.99). Raise it in noisy environments to avoid false starts; lower it if the assistant struggles to hear the customer.
- **Silence duration** — The milliseconds of silence before the assistant considers the turn finished (from 100 to 2000 ms). Increase it if the assistant interrupts people who pause; reduce it for more responsive replies.

## Scenarios and use cases <a id="casi-uso"></a>

**Hotel reception with international clientele**
: Slightly reduced speed, medium temperature, higher silence duration, and low responsiveness: non-native speakers take longer pauses and should not be interrupted.

**Restaurant reservations at peak times**
: Medium-high responsiveness and low silence duration for a fast conversation; low temperature to read the date, time, and number of guests accurately.

**Outbound sales calls**
: Medium-high temperature for a warm and persuasive tone, speed just above 1.0, and high responsiveness to keep a lively pace.

**Noisy environment (bar, waiting room)**
: Threshold-based mode with a higher threshold to ignore background noise and prevent the assistant from starting on its own.

**Elderly clientele or complex topics**
: Reduced speed, high silence duration, and low responsiveness to give the maximum room to speak without interruptions.

> [!WARNING]
> **Change one parameter at a time**
> Change one value, try it in the playground with realistic scenarios, and listen to the result before touching the next one. Changing several parameters together makes it hard to understand what worked.
