---
title: "Setting up the ChatBot"
description: "Look, sites, the code to paste, publishing and versions."
section: "ChatBot"
slug: "website-chat/setup"
---

# Setting up the ChatBot

Look, sites, the code to paste, publishing and versions.

_Everything the visitor sees is set in the ChatBot's Website tab. On the right, a preview updates as you type, and you can try the ChatBot._

## Instructions, documents and tools <a id="istruzioni"></a>

As with the other assistants, behaviour is set in the Instructions tab, documents in the Knowledge base and actions in the Tools tab. They apply as soon as you save: no need to publish.

When you create the ChatBot you can enter the website it goes on (it is already filled in if it is in your business details). We read it once: we write the first instructions from its content, give the ChatBot the site's colour and icon when the site declares them, and allow the site to show the ChatBot. If the site cannot be read, the instructions start from your answers in the guided setup.

## Look <a id="aspetto"></a>

- **Header** — Title, subtitle, logo and colour. The text colour on top of it is picked automatically so it stays readable.
- **Messages** — The welcome message, up to four suggested questions and the text in the message field.
- **Button on the site** — An image instead of the icon, a bubble next to the button, the position (bottom right or left) and the distance from the edges.
- **Open automatically** — When on, the chat opens by itself after a moment, on every page, until the visitor writes.
- **Language and privacy** — The language of the ChatBot's own texts and the link to your privacy policy.

Changes to the look stay in the draft until you publish: the site keeps showing the published version.

## Options <a id="opzioni"></a>

- **Photos and PDFs from visitors** — Visitors can attach photos or PDFs (up to 10 MB, 10 per chat). The ChatBot reads the text of PDFs; you see the photos in the conversations.
- **Hide the “Powered by” line** — Only the privacy link stays under the chat.

If an option needs the ChatBot package, the tab says so: the setting is saved and applies as soon as you activate the package. Like the appearance, options reach the site when you publish.

## Allowed sites <a id="siti"></a>

The ChatBot only appears on allowed sites, for example example.com (www.example.com included). If your company's website is in your profile, it's already on the list. Write *.example.com for every subdomain. The list applies at once, without publishing: remove a site and the ChatBot stops answering there.

## The code to paste <a id="codice"></a>

Copy the code from the tab and paste it before </body> on every page where you want the ChatBot: under the button you'll find where it goes with WordPress, Wix, Shopify, Squarespace and Google Tag Manager. It never changes: publishing a new version doesn't require touching it. As soon as a page of your site loads the code, the check shows it; if the site isn't allowed, you allow it in one click.

```html
<script src="https://…/widget.js" data-key="…" async></script>
```

## If you do not manage the site yourself <a id="sviluppatore"></a>

Press "Send to whoever manages the site": an e-mail opens with the code and where to paste it. You choose who to send it to; once the code is on the site, the check completes by itself.

## Open the chat from your own button <a id="pulsante-chat"></a>

Any link to #chat opens the ChatBot: a "Contact us" button, a menu item, the link in your e-mail signature. Your site's address followed by /#chat opens the chat as soon as the page loads, handy for a QR code. With data-webchat-message="…" on the link, the question is sent already written.

```html
<a href="#chat">Chat with us</a>
<a href="#chat" data-webchat-message="I would like to book">Book in the chat</a>
```

## Publishing and going back <a id="pubblicare"></a>

- **Publish to your site** — Takes the draft to the site as a new version. You can add a note to remember what changed.
- **Published versions** — Every publication stays in the list. Restoring a version publishes it again as a new version and loads it into the draft.
- **Visible on your site** — Turn it off to hide the ChatBot from the site without removing the code; turn it back on whenever you like.

## Trying the ChatBot <a id="prova"></a>

In the preview you can write to the ChatBot as a visitor would. Tests never show up among the website conversations.

## How it is going <a id="come-va"></a>

On the Website tab, "How it is going" sums up the last 30 days of visitors' chats (your tests do not count):

- **Handled by the ChatBot** — The conversations where no one from the team had to step in.
- **Visitor ratings** — Under each answer the visitor can press 👍 or 👎.
- **To improve** — The questions the ChatBot could not answer and the answers rated not helpful, with the visitor's question and a link to the conversation. Add the right answer to the Knowledge base FAQ or the instructions: it applies at once, no publishing needed.

## WhatsApp <a id="whatsapp"></a>

If you write your WhatsApp number in the look, the chat shows "Write to us on WhatsApp" at the top and when the ChatBot cannot answer. If your site already has a WhatsApp button, the number is taken from it when you create the ChatBot.
