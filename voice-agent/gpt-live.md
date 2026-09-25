---
title: "GPT Live: voices, style and listening"
description: "Explore GPT Live 1, try its voices and configure your agent."
section: "Voice agent"
slug: "voice-agent/gpt-live"
lastUpdated: "2026-09-18"
status: "beta"
---

# GPT Live: voices, style and listening

Explore GPT Live 1, try its voices and configure your agent.

_GPT Live 1 is a voice model distinct from GPT Realtime: it keeps listening while speaking. In Yourang it uses your agent’s instructions, context and tools; the backend handles actions and returns their results to the voice. Changing a voice does not add tools or permissions._

> [!NOTE]
> **Availability**
> GPT Live is available to every organization when the provider is enabled and voices are available. If it does not appear in your catalogue, your plan or organization settings exclude it. Existing agents never switch to Live automatically.

## Personality, tone and listening <a id="style-and-listening"></a>

- Listening signals: Off, Discreet, Natural or Expressive. Natural is a recommendation, never an automatic default. “Mm-hm” signals attention, not a confirmed booking.
- Pauses: Natural or more patience while the customer thinks. These are model instructions, without guaranteed frequencies or durations. Interrupting speech does not automatically cancel an action already started.

In Advanced, choose tone, formality, response length, expressive pace and an optional note up to 500 characters. Balanced, Welcoming, Professional and Direct presets are editable starting points. Use current instructions preserves existing behavior; resetting preferences restores that behavior. Expressive pace is guidance, not numeric audio speed.

## Choose, configure and try <a id="configure-and-test"></a>

1. **Choose a voice** — Open your agent → Voice, select GPT Live 1 and listen to available previews. Live voices are distinct from Realtime voices with the same name; language and characterization do not guarantee an accent.
2. **Adjust the style** — In Advanced, configure style, listening signals and pauses. Changes save after a short pause: wait for the saved state. If saving fails, your draft remains available and you can retry.
3. **Try your agent** — After saving, use Try your agent in the header. Describe a request with pauses, interrupt to correct a detail and check a response while a tool is working.
4. **Keep your preferences** — Switching providers preserves common style; Live listening and pause settings remain saved but inactive on other models. Business rules remain in Instructions.

## Demo and real actions <a id="demo-and-actions"></a>

> [!WARNING]
> **Demo and real actions**
> The launch demo explicitly simulates actions: it creates no bookings, sends no messages and makes no business changes. Your agent’s playground and operational calls follow its configured tools and can perform real actions. The voice must confirm success only after receiving the tool result.

## Responses that fit your business <a id="reasoning-effort"></a>

Reasoning level, or effort, controls how deeply the model examines a request before returning an answer or selecting a tool. In GPT Live, the voice maintains the conversation while a backend model handles delegated checks and operations. Its name appears in advanced settings: effort does not change the model.

Fast: a customer asks your opening hours or simple availability. Balanced: a booking must respect timing, party size and preferences. Thorough: compare alternatives, combine constraints and coordinate checks. Start with Balanced and test representative customer requests.

Under Model and voice, open Advanced settings → Request handling. Choose a profile; changes save automatically after a short pause. Then test the agent. New GPT Live agents start Balanced; existing agents retain Fast until you change it. Restoring a version from before this feature keeps Fast. Resetting to the platform default selects Balanced.

Grok offers Fast and Thorough; the platform default is Fast. There is no equivalent medium setting here. Gemini Live, GPT Realtime, ElevenLabs and Nova have no effort control on this page. Preferences remain saved when switching models, but only apply to a compatible model.

More reasoning can increase wait time and token usage; it guarantees neither correctness nor precise response times. It does not change voice timbre, speaking speed, tone, pauses or listening signals, and cannot fix missing data, slow tools or conflicting instructions. Permissions and action confirmations remain the same at every level. A simulated test does not prove the audio quality of a real phone call.

## Learn more <a id="learn-more"></a>

- [**Voices and languages**](/voice-agent/voices-and-language) — Listen to previews and choose languages.
- [**Advanced settings**](/voice-agent/advanced-settings) — Customize style, listening and pauses.
- [**Instructions and business rules**](/voice-agent/instructions) — Define tasks and required confirmations.
