---
title: "API keys and authentication"
description: "Generate, use, and revoke API keys safely."
section: "External APIs and developers"
slug: "external-api/api-keys"
---

# API keys and authentication

Generate, use, and revoke API keys safely.

_Authentication to the external API is done via API keys, distinct from user credentials. A key identifies an organization and has specific permissions._

## Generating a key <a id="generare-chiave"></a>

1. **Open the API panel** — Go to Administration -> API. Only users with Owner or Admin role can manage keys.
2. **Create a new key** — Click “Create API Key”, give it a descriptive name (e.g. "PMS production", "Zapier dev"), choose the permission and the expiry: 30, 60, 90 or 365 days, a number of days of your choice, or never. A new key starts as “Read only”, expiring in 90 days.
3. **Copy the value immediately** — The key is shown only once. Store it securely: a password manager, a vault, an environment variable. Yourang stores only the hash and cannot show it to you again.
4. **Configure the external system** — Paste the key into the system that will call the API. The test call confirms everything works.

## Permission levels <a id="livelli-permesso"></a>

- **Read only** — The program sees the data but cannot change it: ideal for reports, dashboards and read-only syncs.
- **Read and write** — The program can also create and edit: contacts, reservations, orders and the other areas of the API.

## Using the key <a id="usare-chiave"></a>

Each request includes the key in the HTTP Authorization header as a Bearer token. Example: Authorization: Bearer yr_live_abc123. The API validates the key, identifies the organization, and applies permissions before processing the request.

## Rotation and revocation <a id="rotazione-revoca"></a>

Best practice: rotate keys at least once a year or whenever the staff managing them changes. Revocation is immediate: by clicking "revoke" the key stops working instantly. Always create a new key before revoking the old one, to avoid service interruption.

Regenerating a key: "Regenerate" (the ↻ icon in the key's row, or the warning under its name) gives the key a new value and a new expiry, which is the only thing you are asked for. Its name, description, permission and usage stay the same. The new value is shown only once and the old one stops working immediately, so update the integration right after regenerating. If the integration cannot stop even for a moment, create a new key instead, update the integration and only then revoke the old one.

A key that expires within 30 days shows the warning "This key expires on …" under its name; once it has expired, "This key has expired".

Email notices: whoever created the key receives an email 30, 7 and 1 day before it expires, one when it has expired, one when it is revoked and one when it is regenerated (naming who revoked or regenerated it). If the creator is no longer an owner or admin of the organization, the emails go to the owners and to the admins who manage API keys.

> [!WARNING]
> **Never keys in the client**
> API keys must not appear in public JavaScript code, compiled mobile apps, or public git repositories. They live only server-side. If you suspect compromise: revoke immediately and investigate.

- [**Open the developer portal**]({{developersUrl}}) — API console, request logs, browsable OpenAPI.
- [**Go to the API overview**](/external-api/overview) — REST endpoints, authentication, practical examples.
