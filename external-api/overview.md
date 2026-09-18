---
title: "Yourang for developers"
description: "What the external API offers, who it is for, general principles."
section: "External APIs and developers"
slug: "external-api/overview"
---

# Yourang for developers

What the external API offers, who it is for, general principles.

_For management systems, portals, custom applications, or advanced automations, Yourang exposes a REST API and a webhook system that let you read and write data and receive real-time notifications._

## Who it's for <a id="a-chi-rivolta"></a>

- **Internal developers** — IT teams who want to integrate Yourang with a PMS, a management system, a mobile app.
- **Integration partners** — Software houses building solutions for hospitality or services who want to offer a Yourang connection to their customers.
- **Power users with technical skills** — Those who use no-code tools (Zapier, Make, n8n) can leverage APIs and webhooks without writing traditional code.

## Technical principles <a id="principi"></a>

- **REST + JSON** — Standard conventions: GET, POST, PUT, DELETE on readable URLs. All exchanges are in JSON UTF-8.
- **URL versioning** — The API has a version prefix (e.g. /api/external/v1/). Breaking changes go into new versions; old ones remain supported with announced deprecation periods.
- **Separate schema** — External API payloads do not share internal product fields: you have a stable surface, independent of internal evolutions.
- **HTTPS required** — All calls happen over TLS. No plaintext endpoints.

> [!TIP]
> **Complete technical documentation**
> This section explains the main concepts and use cases. For the technical details of each endpoint (parameters, responses, error codes), there is a separate OpenAPI documentation, accessible from the developer panel.
