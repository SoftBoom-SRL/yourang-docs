---
title: "Operator app (iOS / Android)"
description: "Receive AI-transferred calls directly on the operator’s mobile app."
section: "Call transfers"
slug: "call-transfers/operator-mobile-app"
---

# Operator app (iOS / Android)

Receive AI-transferred calls directly on the operator’s mobile app.

_When the voice agent realizes a human is needed, it can hand the call off to one of your operators on their phone through the Yourang app for iOS and Android. The operator gets a push notification, accepts, and the conversation continues with no perceptible break for the customer._

## How it works <a id="mobile-app-funzionamento"></a>

1. **The AI decides to transfer** — When the conversation needs a human (complex request, explicit escalation, out of scope), the agent invokes the transfer_to_mobile_operator tool.
2. **Routing to the right operator** — Yourang queries the online operator queue for the configured department and picks an available one. If the tool has hours constraints, only on-shift operators are considered.
3. **Push notification to the app** — The selected operator gets a push notification (APNs on iOS, FCM on Android) with a preview of the transfer reason, the call summary and the customer details.
4. **Accept and audio bridge** — The operator accepts from the app. The system creates an audio bridge: customer, operator and (if configured) AI in conference for a few seconds, then the AI steps back, leaving human and customer on the line.
5. **Full tracking** — The transferred call stays visible in the call history with all details: AI-customer transcript, transfer moment, operator-customer duration, outcome.

## Operator setup <a id="mobile-app-setup"></a>

1. **Create the operator profile** — /user-roles → invite the operator with the Operator role. They receive an email with the signup link.
2. **Install the app** — The operator downloads Yourang from the App Store (iOS) or Google Play (Android) and signs in with the received credentials.
3. **Check permissions** — The app asks for push notifications, microphone and (optional) contacts permissions. All are required to receive calls.
4. **Assign to a department** — From the dashboard, assign the operator to one or more departments. Only calls routed to those departments will reach them.
5. **Set availability hours** — On the transfer_to_mobile_operator tool, define the global hours (e.g. Mon-Fri 9-18). Outside that window, the AI does not attempt the transfer and follows the fallback rule (e.g. after-hours AI or transfer to a fixed number).

## Real-time availability <a id="mobile-app-disponibilita"></a>

The app shows operators their online/offline status and any in-progress call. If no operator of a department is online when the AI tries to transfer, Yourang runs the configured fallback (continue with the AI, transfer to a number, log as escalation for callback).

> [!WARNING]
> **Avoid missed notifications**
> iOS and Android can put unused apps to sleep. Make sure your operators are required to keep the app active or to enable priority notifications for Yourang (exact instructions vary by OS: the app's first run shows them).

## Differences vs. transfer to a fixed number <a id="mobile-app-differenze"></a>

**Smart routing**
: The app picks operator + department; a fixed number always rings the same phone.

**Context on the fly**
: The operator sees the AI summary and customer data BEFORE accepting; a fixed number starts blind.

**Dynamic online status**
: The operator can pause themselves; a fixed number rings regardless.

**Multi-device availability**
: An operator can have the app on two devices (e.g. iPhone + iPad); a fixed number is just one.
