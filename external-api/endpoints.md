---
title: "Main endpoints"
description: "Overview of API areas and the most common use cases."
section: "External APIs and developers"
slug: "external-api/endpoints"
---

# Main endpoints

Overview of API areas and the most common use cases.

_The API is organized by resources, each with its own endpoints. Here's a map of the main areas._

## Quick start <a id="quick-start-code"></a>

Three ready-to-use snippets to call the external API. Replace `yr_live_xxx` with your personal key (see the “API keys and authentication” page).

#### cURL

```bash title="list-contacts.sh"
curl -X GET "https://api.Yourang.io/external/v1/contacts?limit=20" \
  -H "Authorization: Bearer yr_live_xxx" \
  -H "Accept: application/json"
```

#### Node.js

```javascript title="list-contacts.mjs"
import fetch from "node-fetch";

const res = await fetch(
  "https://api.Yourang.io/external/v1/contacts?limit=20",
  {
    headers: {
      Authorization: "Bearer yr_live_xxx",
      Accept: "application/json",
    },
  }
);
const { data } = await res.json();
console.log(`Got ${data.length} contacts`);
```

#### Python

```python title="list_contacts.py"
import requests

resp = requests.get(
    "https://api.Yourang.io/external/v1/contacts",
    params={"limit": 20},
    headers={
        "Authorization": "Bearer yr_live_xxx",
        "Accept": "application/json",
    },
    timeout=10,
)
resp.raise_for_status()
print(f"Got {len(resp.json()['data'])} contacts")
```

## API areas <a id="aree-api"></a>

- **Contacts** — Read, create, update CRM contacts. Two-way synchronizations with management systems, periodic imports from external sources.
- **Calls** — Retrieve call history with metadata, transcripts, summaries. Trigger outbound calls programmatically.
- **Reservations** — Create, read, modify reservations. Sync the Yourang calendar with the PMS or management system.
- **Orders** — For the Shop module: create orders from external systems, read status, receive payment confirmations.
- **Documents** — Upload and manage the knowledge base via API. Useful for those who keep the catalog/price list in a source system and want to replicate it in Yourang.
- **Webhooks** — Configure the URLs to which Yourang notifies events (see dedicated page).

## Typical use cases <a id="casi-uso-tipici"></a>

- **Sync management system -> Yourang** — Every night the PMS publishes new contacts and the day's reservations to Yourang. The voice assistant works with always-aligned data.
- **Yourang -> management system** — When the assistant records a new reservation, it reports it to the main management system via API. The assistant becomes an input channel to the central system.
- **Custom dashboard** — A BI or Excel sheet connected to the API shows custom aggregated data, beyond the standard panel.
- **Automations with n8n / Make** — No-code workflows that react to Yourang events to orchestrate actions in other systems: Slack, Notion, Airtable.

## Pagination and filters <a id="paginazione-filtri"></a>

All list endpoints support pagination (limit + offset) and filters on the main fields. For bulk exports it's better to paginate with reasonable sizes (50-100 per page) rather than asking for everything at once: avoids timeouts and load on systems.

> [!NOTE]
> **Rate limits**
> The API has rate limits to protect the system from abuse. Standard limits are generous for normal use; for integrations with high volumes, contact the sales team for dedicated plans.
