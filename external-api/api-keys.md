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
2. **Create a new key** — Assign a descriptive name (e.g. "PMS production", "Zapier dev") and select the permission level.
3. **Copy the value immediately** — The key is shown only once. Store it securely: a password manager, a vault, an environment variable. Yourang stores only the hash and cannot show it to you again.
4. **Configure the external system** — Paste the key into the system that will call the API. The test call confirms everything works.

## Permission levels <a id="livelli-permesso"></a>

- **Read** — Read-only: contacts, orders, calls, statistics. Ideal for dashboards, reports, pull-based synchronizations.
- **Write** — Read + create/modify data: add contacts, register orders, create reservations. For two-way integrations.
- **Write + outbound calls** — Includes the ability to trigger outbound calls. It's the most powerful permission, to be assigned only to trusted systems.

## Using the key <a id="usare-chiave"></a>

Each request includes the key in the HTTP Authorization header as a Bearer token. Example: Authorization: Bearer yr_live_abc123. The API validates the key, identifies the organization, and applies permissions before processing the request.

## Rotation and revocation <a id="rotazione-revoca"></a>

Best practice: rotate keys at least once a year or whenever the staff managing them changes. Revocation is immediate: by clicking "revoke" the key stops working instantly. Always create a new key before revoking the old one, to avoid service interruption.

> [!WARNING]
> **Never keys in the client**
> API keys must not appear in public JavaScript code, compiled mobile apps, or public git repositories. They live only server-side. If you suspect compromise: revoke immediately and investigate.

- [**Open the developer portal**]({{developersUrl}}) — API console, request logs, browsable OpenAPI.
- [**Go to the API overview**](/external-api/overview) — REST endpoints, authentication, practical examples.
