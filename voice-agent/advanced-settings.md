---
title: "Advanced settings"
description: "Fine-tune creativity, speed, and turn detection"
section: "Voice agent"
slug: "voice-agent/advanced-settings"
---

# Advanced settings

Fine-tune creativity, speed, and turn detection

## Responses that fit your business <a id="reasoning-effort"></a>

Reasoning level, or effort, controls how deeply the model examines a request before returning an answer or selecting a tool. In GPT Live, the voice maintains the conversation while a backend model handles delegated checks and operations. Its name appears in advanced settings: effort does not change the model.

Fast: a customer asks your opening hours or simple availability. Balanced: a booking must respect timing, party size and preferences. Thorough: compare alternatives, combine constraints and coordinate checks. Start with Balanced and test representative customer requests.

Under Model and voice, open Advanced settings → Request handling. Choose a profile; changes save automatically after a short pause. Then test the agent. New GPT Live agents start Balanced; existing agents retain Fast until you change it. Restoring a version from before this feature keeps Fast. Resetting to the platform default selects Balanced.

Grok offers Fast and Thorough; the platform default is Fast. There is no equivalent medium setting here. Gemini Live, GPT Realtime, ElevenLabs and Nova have no effort control on this page. Preferences remain saved when switching models, but only apply to a compatible model.

More reasoning can increase wait time and token usage; it guarantees neither correctness nor precise response times. It does not change voice timbre, speaking speed, tone, pauses or listening signals, and cannot fix missing data, slow tools or conflicting instructions. Permissions and action confirmations remain the same at every level. A simulated test does not prove the audio quality of a real phone call.

Open Voice → Advanced settings to reveal a right-hand panel. Conversation style is shared; other controls follow the saved model. Changes save after a short pause. Wait for the save before closing; if it fails, retry or discard the draft.

_Advanced settings let you fine-tune the conversational behavior of the voice assistant. The default values work well in most cases: change them only when you have a specific problem to solve, one parameter at a time._

## Conversation style and listening <a id="stile-conversazione"></a>

The common settings block lets you choose tone, formality, response length, and pace, plus an optional custom note. Use the suggestions beside each field as a starting point: choose a combination that fits your audience. Changes autosave after you stop editing; the status shows when they are saved. If saving fails, your draft stays in place and you can retry. Use the existing Try your agent action in the header after the save completes.

- Choose descriptive presets such as Balanced, Welcoming, Professional, or Direct; expressive pace is chosen with words rather than numeric values.
- For GPT Live, listening signals control brief backchannels while the customer speaks; they are not confirmations of bookings, messages, or other operations.
- Natural pauses leave room for the customer; the patient option gives the assistant more time before responding.

> [!NOTE]
> **GPT Live only**
> Backchannel and pause options are available only for GPT Live. Use the current instructions to keep the previous behaviour; reset the preferences and save to return to that behaviour.

> [!NOTE]
> **Availability by model**
> The options shown depend on the selected provider and model. Common settings remain shared when available; provider-specific options appear in Advanced settings.

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
