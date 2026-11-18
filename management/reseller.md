---
title: "Reseller statistics and MCP access"
description: "Follow the organizations you resell and connect an AI assistant to them"
section: "Management"
slug: "management/reseller"
---

# Reseller statistics and MCP access

Follow the organizations you resell and connect an AI assistant to them

_If you sell Yourang to other businesses, the organizations you resell are linked to your account. Reseller mode shows what they earn and pay, and lets you connect an AI assistant that can work on them with your own role._

## Opening reseller mode <a id="open"></a>

Open the workspace switcher at the top of the sidebar and choose “Reseller Analytics”. The sidebar then shows two tabs: Statistics and MCP access. Choose your organization in the switcher to go back to the usual navigation.

## Statistics <a id="statistics"></a>

Pick the period (3, 6, 12 or 24 months) above the figures. If a period cannot be loaded, the page says so and keeps showing the period you had before.

- **Revenue** — Counted as in the platform analytics: the minutes used within each plan at the plan's price, plus the overage charged to the wallet.
- **Payments received** — Successful payments net of VAT, in the month (UTC) the payment was started: subscriptions, add-ons, wallet top-ups and one-off fees. Payments in other currencies are not included.
- **Your organizations** — One row per organization: plan, current period, calls, talk time, revenue, payments and the date of the last payment. On a phone the table scrolls sideways inside its own box.

> [!NOTE]
> **What the payment figures include**
> Only the payments made since each organization became yours are counted. A plan renewal paid from the wallet is not counted a second time on top of the wallet top-up that funded it. Refunds are not deducted yet.

## MCP access <a id="mcp-access"></a>

An MCP token lets an AI assistant, such as Claude, read and (if you allow it) change the organizations you resell, always with your own role and permissions in each one. It never reaches any other organization.

1. **Create a token** — In the MCP access tab choose “Create token”, give it a name that says where it is used, pick the access (read only, or read and write) and how long it stays valid.
2. **Copy the settings at once** — The token is shown only once. Copy the server URL, the access header and the Authorization header, or the ready-made Claude Desktop configuration.
3. **Connect your assistant** — In Claude Desktop, open claude_desktop_config.json (Settings → Developer → Edit Config), add the “reseller-mcp” entry inside the existing “mcpServers” object and restart the app. It runs the mcp-remote bridge, which needs Node.js. Assistants that accept a server URL with custom headers take the three values directly.

### Revoking a token <a id="revoke"></a>

Revoke a token from the list as soon as you no longer use it: assistants using it lose access immediately. Changing your password or logging out of every device also ends all your tokens. If you stop being a reseller, the MCP access tab stays available while you still own working tokens, so you can revoke them; you can no longer create new ones.

> [!TIP]
> **When no connection settings are shown**
> Some environments, such as test environments, do not expose an MCP server. The token is still created, but the dialog shows a note instead of the connection settings because no assistant could reach it there. Platform administrators and white-label reseller domains cannot create reseller tokens.
