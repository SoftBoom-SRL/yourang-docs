---
title: "Nodes and blocks"
description: "The building blocks of a workflow: triggers, actions, conditions, waits, end."
section: "Workflows"
slug: "workflows/nodes-and-blocks"
---

# Nodes and blocks

The building blocks of a workflow: triggers, actions, conditions, waits, end.

_A workflow is made up of connected nodes. Each node performs a specific task. Knowing the available nodes is the first step to building effective automations._

## Node types <a id="tipi-di-nodi"></a>

- **Trigger (start)** — Defines when the workflow starts. It can be an event (new call, new order), a time (every day at 8), an incoming webhook, or manual (you launch it).
- **Action** — Performs an operation: send SMS, create contact, update field, call external API, log a note. It's the block that "does things".
- **Condition (If-Criteria)** — Chooses a branch based on a check: "if the customer already has an active order, do X; otherwise do Y". Conditions make the workflow intelligent.
- **Wait** — Pauses execution for a duration (5 minutes, 2 hours, 3 days) or until an event occurs (e.g. customer replies).
- **Sub-workflow** — Invokes another workflow from within the current one. Lets you reuse common logic without duplicating nodes.
- **End** — Closes the workflow recording the outcome (completed, failed, cancelled). There can be more than one end node to express different outcomes.

## Variables and expressions <a id="variabili"></a>

Nodes can read and write variables: data that flows through the workflow. For example, the "New order" trigger node exposes variables like "customer.name", "order.total", "order.items". Subsequent actions can use them to personalize messages or decide branches.

> [!NOTE]
> **Simple expressions, not programming**
> The system supports basic expressions ("equals", "greater than", "contains", elementary arithmetic operators). You don't need to know how to program: the editor shows contextual suggestions at every step.

## The visual canvas <a id="canvas"></a>

Build the workflow by dragging nodes onto the canvas and connecting them with arrows. Each node has a configuration panel that opens when you click it. For long workflows you can create groups and labels to stay oriented.
