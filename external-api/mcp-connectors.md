---
title: "Connect Claude and ChatGPT (MCP)"
description: "Use Yourang straight from Claude, ChatGPT or Claude Code: interactive cards in the chat, secure OAuth access."
section: "External APIs and developers"
slug: "external-api/mcp-connectors"
lastUpdated: "2026-10-05"
---

# Connect Claude and ChatGPT (MCP)

Use Yourang straight from Claude, ChatGPT or Claude Code: interactive cards in the chat, secure OAuth access.

_With the Yourang MCP server you work on your organization right from Claude or ChatGPT: ask how the day is going, open calls and transcripts, create and approve reservations, update contacts, orders and agents. In Claude and ChatGPT the results appear as interactive cards. No API key is needed: sign in with your account and choose the organizations._

## Where to find the URL <a id="mcp-url"></a>

Go to Administration → API, "MCP connection" card. Copy the URL there (the same for every client) or click "Add to Claude", which opens Claude with the name and URL already filled in.

## Connect the client <a id="mcp-connect"></a>

#### Claude

1. **Open the form** — Click "Add to Claude" in Administration → API. Or, in Claude (web or desktop), go to Customize → Connectors → + Add → Add custom connector and paste the name and URL.
2. **Add the connector** — Keep the recommended OAuth client option, click "Add" and then "Connect".
3. **Authorize** — The Yourang sign-in page opens: sign in, choose the organizations, decide whether to allow changes too and click "Allow".
4. **Use it in a chat** — In a chat, turn the connector on from + → Connectors and ask, for example, "How is today going?".

> [!NOTE]
> **Plans and permissions**
> Available on every Claude plan (Free: one custom connector). On Team and Enterprise an Owner adds it from Organization settings → Connectors; then each member clicks "Connect". The mobile app can use it once it has been added on the web or desktop.

#### ChatGPT

1. **Turn on developer mode** — In ChatGPT open Settings → Security and login and turn on Developer mode.
2. **Create the plugin** — Go to chatgpt.com/plugins, click +, enter a name and paste the MCP server URL as the connection; choose OAuth as the authentication and click "Create".
3. **Authorize** — Sign in to Yourang, choose the organizations and click "Allow".
4. **Use it in a chat** — In a chat, pick it from + → Developer mode (or type @) and ask "How is today going?".

> [!NOTE]
> **Plans and permissions**
> Requires Developer mode: Plus, Pro, Business, Enterprise and Edu plans, on the web. On Business only admins and owners can create the plugin and publish it to the workspace. ChatGPT asks for confirmation before every change.

#### Claude Code

1. **Add the server** — In your terminal run: claude mcp add --transport http <name> <MCP server URL>.
2. **Authorize** — In Claude Code type /mcp, select the server and finish signing in in the browser.

If you use the same account as claude.ai, connectors added there already appear in Claude Code. In Claude Code the results are text: the interactive cards appear in Claude and ChatGPT.

## What you can do in the chat <a id="mcp-use"></a>

When you ask to see something, Claude and ChatGPT show an interactive card: open the details, move between days, approve or confirm in one click. Every action that changes data asks for your confirmation.

- **Overview** — Today's reservations (and how many wait for approval), plan minutes, credit, active agents, latest calls.
- **Calls** — List with outcome and duration; for each call the summary, transcript and recording.
- **Reservations** — Day-by-day agenda: create a reservation, approve or reject confirmed reservations.
- **Contacts and orders** — Find a contact and see their calls; open an order and confirm or complete it.
- **AI agents** — See the configuration and ask to change the instructions, first message, voice, languages or style.
- **Plans** — Compare the plans, pick minutes and monthly or yearly billing, see what you pay today and open the secure payment page; apply the activation discount code. WhatsApp and Meta packs open the dashboard configurator.
- **Everything else in the dashboard** — FAQ and knowledge base, opening hours and company details, departments and call routing, phone numbers, call statistics, call campaigns, WhatsApp replies and integrations: everything the dashboard AI assistant does, with your own permissions.

> [!TIP]
> **Try asking**
> "How is today going?" · "Which reservations do I have tonight? Approve the confirmed ones" · "Create a reservation for 4 people tomorrow at 8:30 pm for Rossi" · "Summarize yesterday's unanswered calls" · "Make my agent friendlier".

## Permissions and revocation <a id="mcp-permissions"></a>

- **Organizations per connection** — On the consent screen you tick the organizations the connection may work in (all by default). The client names the organization before acting. Disconnecting it from one organization's Connected apps leaves the others working.
- **Read-only** — On the consent screen you can turn off "Allow changes": the client can then only read data.
- **Permissions by area** — The consent screen shows one permission per area (contacts, agents, calls, reservations…). If an action is refused, reconnect the client and grant that permission. Connections made before these permissions existed must reconnect.
- **Dashboard only** — Members and roles, invitations, password and email, API keys, ownership transfer and deleting the organization, as well as live-call controls, the wallet's automatic top-up and promo codes, are never available from Claude or ChatGPT.
- **Revoke** — Administration → API → “Connected apps”: disconnect the client and its access ends immediately. Changing or resetting your password, or signing out all other devices, also disconnects every client: reconnect them afterwards.

> [!WARNING]
> **Actions with real effects**
> Agent changes apply from their next calls; call campaigns, WhatsApp replies, phone numbers and workflows cost money or reach your customers. Claude and ChatGPT ask for confirmation before any action that changes something: always read what you are approving. Payments never go through the chat: you get a Stripe link and confirm it yourself.
