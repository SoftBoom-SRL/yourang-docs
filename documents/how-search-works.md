---
title: "How search works during a call"
description: "What happens behind the scenes when the assistant consults the knowledge base."
section: "Documents and knowledge base"
slug: "documents/how-search-works"
---

# How search works during a call

What happens behind the scenes when the assistant consults the knowledge base.

_Understanding (at least at a surface level) how semantic search works helps you write documents the assistant can use well._

## Semantic search, not textual <a id="ricerca-semantica"></a>

The search isn't for exact words but for meanings. A question about 'rates for families with children' can find a paragraph about a 'family unit discount', even if the words don't match. This makes the base resilient to how customers phrase their questions.

## Why small blocks work better <a id="chunk-piccoli-meglio"></a>

Documents are split into small blocks of a few hundred words. Each block is retrieved independently. Because of this, short self-contained paragraphs produce better results than walls of continuous text: a block with a single clear idea is easier to match to a question.

## Writing documents the AI uses well <a id="scrivere-bene"></a>

- **Explicit headings** — Phrases like 'Cancellation policy' or 'Indoor pool hours' make every section easy to identify.
- **Self-contained sentences** — Avoid references like 'as seen above'. Each paragraph must be able to be read on its own and make sense.
- **Explicit numbers and details** — Write 'free cancellation is possible up to 48 hours before arrival' instead of 'it's possible to cancel before the stay'. Specific data is more useful than generalities.
- **No acronyms without explanation** — If your business uses internal terms, define them at least once in the document: it helps both the AI and whoever reads the file tomorrow.
