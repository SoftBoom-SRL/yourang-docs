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
> **Webhook (optional)**
> Fill in the Webhook Client Secret field only if you use the HubSpot Trigger node in workflows.

> [!WARNING]
> Never share your Private App token: it grants access to your CRM data. If it leaks, revoke it in HubSpot and generate a new one.
