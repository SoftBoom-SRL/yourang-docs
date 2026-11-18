---
title: "AI hours"
description: "Enable an inbound agent, assign its answering hours, and review caller exceptions."
section: "Voice agent"
slug: "voice-agent/incoming-calls"
---

# AI hours

Enable an inbound agent, assign its answering hours, and review caller exceptions.

_Open an inbound agent and select AI hours, after Instructions. Activation enables the agent but does not assign calls to it. Several inbound agents can be enabled together. The routing summary reports saved configuration, not whether phone connectivity or a particular caller has been verified._

## Assign calls after activation <a id="assign-calls"></a>

1. If the enabled agent has no weekly assignment or current or future caller exception, guided setup opens. You can finish later; the No calls assigned notice remains.
2. With an empty shared schedule, Answer 24/7 and Choose hours prepare an editable draft. Review the destination, days and timezone, then Save to apply it. Choosing a template alone does not change routing.
3. When a schedule already exists, assign calls to this agent in the shared editor. Review the affected days and agents before applying a template or copying a day that replaces existing destinations.

## One shared schedule <a id="shared-routing"></a>

Your agent’s assigned hours appear first. The weekly schedule belongs to the organization: other agents, staff, phone numbers and queues remain visible. Caller exceptions override the weekly schedule for matching callers during their validity period. Expired exceptions no longer apply; future exceptions start on their configured date.

## Answering hours and uncovered time <a id="answering-hours"></a>

Check the schedule timezone. 24:00 means the end of that weekday, including its last second. Unless a caller exception applies, uncovered time plays the default closed message and ends the call. Business opening hours describe when your business is open; they do not assign incoming calls.

## Access, testing and supported connections <a id="routing-access"></a>

Routing permissions are separate from agent permissions, so this section may be editable, read-only or require access. The existing /calls/inbound-rules address remains available as an agent chooser or shared editor, including for members with routing access but no agent access. Shared routing is excluded from agent versions and is hidden during historical preview; restoring a version does not restore routing.

> [!NOTE]
> These schedules and caller exceptions currently apply to Twilio connections. Telnyx bypasses this routing: the section explains that it is unsupported instead of claiming the schedule controls calls. Playground calls also bypass the schedule, so a successful test does not confirm live assignment.
