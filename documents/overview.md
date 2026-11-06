---
title: "What the knowledge base is"
description: "How the knowledge base (RAG) works and why it's the most effective way to give the assistant your own information."
section: "Documents and knowledge base"
slug: "documents/overview"
---

# What the knowledge base is

How the knowledge base (RAG) works and why it's the most effective way to give the assistant your own information.

_The knowledge base is the archive of documents, manuals, and procedures that your assistant consults in real time to answer customer questions. It's the simplest way to ensure the answers are consistent, up to date, and based on your own materials._

## Difference between instructions and knowledge base <a id="differenza-istruzioni"></a>

- **Instructions** — Define the general behaviour of the agent: how it speaks, what it can do, what tone it uses. They are read on every call.
- **Knowledge base** — Contains your business's domain knowledge: price lists, regulations, extended FAQs, service descriptions. It's consulted only when needed.

Together they form the assistant's 'personality': the instructions decide how it behaves, the knowledge base provides the concrete answers. Keeping the two separate makes maintenance much easier.

## How retrieval (RAG) works <a id="come-funziona-rag"></a>

1. **Indexing** — When you upload a document, Yourang splits it into small blocks (chunks) and computes a semantic representation of each.
2. **Customer question** — During the call, the customer's request is matched semantically against the indexed chunks to find the most relevant ones.
3. **Response based on the chunks** — The agent formulates the answer using the retrieved chunks as its source, without inventing information missing from the documents.

> [!TIP]
> **Less invented, more reliable**
> The knowledge base drastically reduces 'made-up' answers. If the question doesn't match anything in your documents, the assistant says so rather than improvising.
