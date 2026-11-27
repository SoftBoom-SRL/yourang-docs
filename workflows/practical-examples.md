---
title: "Practical examples"
description: "Three complete workflows you can adapt to your business."
section: "Workflows"
slug: "workflows/practical-examples"
---

# Practical examples

Three complete workflows you can adapt to your business.

_Theory is useful, but seeing concrete workflows often illuminates more than a thousand explanations. Here are three complete scenarios ready to personalize._

## Workflow 1: multi-channel reservation reminder <a id="promemoria-prenotazione"></a>

1. Trigger: new confirmed reservation
2. Wait: until 24 hours before the scheduled date
3. Action: send SMS with details (date, time, address)
4. Wait: 4 hours
5. Condition: customer confirmed? If yes -> end. If no -> continue
6. Action: send WhatsApp message with "Confirm" / "Cancel" buttons
7. Wait: 2 hours
8. Condition: customer replied? If yes -> record outcome -> end. If no -> continue
9. Action: schedule a phone callback for the next day in the morning
10. End

## Workflow 2: lead qualification from call <a id="qualifica-lead"></a>

1. Trigger: call ended with outcome "potential lead"
2. Action: extract structured data from the transcript (name, phone, request, urgency)
3. Condition: urgency = high? If yes -> continue on fast branch, otherwise standard branch
4. Fast branch: action "send WhatsApp notification to sales team" -> end
5. Standard branch: action "add to new-leads list" -> wait 1 day -> action "send follow-up email" -> end

## Workflow 3: post-stay sequence <a id="post-soggiorno"></a>

1. Trigger: reservation completed (check-out recorded)
2. Wait: 4 hours
3. Action: send a thank-you email with photos of the property
4. Wait: 3 days
5. Action: send email with link to review (Google / TripAdvisor)
6. Wait: 30 days
7. Condition: did the customer leave a review? If yes -> action "tag happy customer". If no -> action "send discount code to return"
8. End

> [!TIP]
> **Version critical workflows**
> Before modifying a workflow that has been active for a while, duplicate it as "v2" and edit the copy. Thorough testing, then activate v2 and deactivate v1. Allows quick rollback if something goes wrong.
