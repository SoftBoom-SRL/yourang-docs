---
title: "Connect HubSpot"
description: "Step-by-step guide to connect HubSpot CRM to Yourang"
section: "Integrations"
slug: "integrations/hubspot-setup"
lastUpdated: "2026-06-16"
---

# Connect HubSpot

Step-by-step guide to connect HubSpot CRM to Yourang

_Connect HubSpot to manage contacts, deals, companies and tickets directly from Yourang workflows. All you need is a Private App token._

## Prerequisites <a id="prerequisiti"></a>

- A HubSpot account with admin permissions
- Access to HubSpot Private Apps settings

## How to connect HubSpot <a id="passaggi"></a>

1. **Sign in to HubSpot** — Log in to your HubSpot account as an administrator.
2. **Open Private Apps** — Go to Settings → Integrations → Private Apps.
3. **Create a Private App** — Create a new Private App, assign the required scopes (contacts, deals, companies, tickets) and copy the generated token (starts with pat-).
4. **Paste the token in Yourang** — Back in Yourang → Integrations → HubSpot, paste the token, name the integration and press Connect.

![HubSpot screen showing the Private App token](/images/docs/integrations/hubspot/private-app-token.png)

_Where to find the Private App token in HubSpot_

> [!TIP]
> **Webhook (only for the trigger)**
> The Webhook Client Secret field is only needed if you use the HubSpot trigger node in automations: without it HubSpot events are rejected. You can leave it empty now and add it later from the trigger node.

> [!WARNING]
> Never share your Private App token: it grants access to your CRM data. If it leaks, revoke it in HubSpot and generate a new one.

## Starting an automation from HubSpot <a id="trigger-hubspot"></a>

To start an automation when something changes in HubSpot, add the HubSpot trigger node and open it: below its settings, the “Connect HubSpot to this trigger” panel shows what to do. HubSpot private apps cannot register webhooks automatically, so you do it once in HubSpot.

1. **Paste the URL in HubSpot** — In HubSpot, open your private app and go to the Webhooks tab. Paste this URL as the target URL.
2. **Create the subscription** — Create a subscription for the event you picked (for “Contact updated”: contact, property change, and the property you want to watch). Activate it.
3. **Save the client secret** — Copy the app's client secret (Auth tab) and save it below, so we can verify HubSpot's signature. Without it every event is rejected.

Only owners and administrators see the client secret field. Saving it replaces any secret already stored for that HubSpot connection.
