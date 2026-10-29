---
title: "Steps and blocks"
description: "The building blocks of a workflow: triggers, actions, conditions, waits, end."
section: "Workflows"
slug: "workflows/nodes-and-blocks"
---

# Steps and blocks

The building blocks of a workflow: triggers, actions, conditions, waits, end.

_A workflow is made up of connected steps. Each step performs a specific task. Knowing the available steps is the starting point for building effective automations._

## Step types <a id="tipi-di-nodi"></a>

- **Trigger (start)** — Defines when the workflow starts. It can be an event (new call, new order), a time (every day at 8), an incoming webhook, or manual (you launch it). A workflow can have several triggers: each one runs only the steps you connect it to.
- **Action** — Performs an operation: send SMS, create contact, update field, call external API, log a note. It's the block that "does things".
- **Condition (If-Criteria)** — Chooses a branch based on a check: "if the customer already has an active order, do X; otherwise do Y". Conditions make the workflow intelligent.
- **Wait** — Pauses execution for a duration (5 minutes, 2 hours, 3 days) or until an event occurs (e.g. customer replies).
- **Sub-workflow** — Invokes another workflow from within the current one. Lets you reuse common logic without duplicating steps.
- **End** — Closes the workflow recording the outcome (completed, failed, cancelled). There can be more than one end step to express different outcomes.

> [!TIP]
> **Steps with more than one output**
> Some steps continue on more than one arrow. The "Send WhatsApp template" step, for example, has "Always, right after sending", one output for each quick-reply button ("On button tap: …") and "If delivery fails": see WhatsApp > Automations, "Branch on buttons and delivery failures".

> [!NOTE]
> **Wait: three modes**
> The Wait step can pause for a duration (up to 31 days), until a date and time (e.g. {{ event.start.dateTime | add_days:"-1" }} for the day before the appointment), or until business hours: outside them it resumes at the next opening, skipping non-working days and Italian public holidays.

## Variables and expressions <a id="variabili"></a>

Steps can read and write variables: data that flows through the workflow. For example, the "New order" trigger step exposes variables like "customer.name", "order.total", "order.items". Subsequent actions can use them to personalize messages or decide branches.

> [!NOTE]
> **Simple expressions, not programming**
> The system supports basic expressions ("equals", "greater than", "contains", elementary arithmetic operators). You don't need to know how to program: the editor shows contextual suggestions at every step.

> [!TIP]
> **Functions in expressions**
> After a value you can add functions with |, chained: | phone (number as +39…), | digits | last:"9" (last 9 digits), | add_days:"1", | add_hours:"2", | date:"DD/MM/YYYY HH:mm", | tz:"Europe/Rome", | upper, | lower, | trim, | default:"…", | number, | round, | length, | first, | last, | slice:"0,3", | split:",", | join, | json, | parse_json, | weekday. List items are read by index: items.0.name. {{ now }} is the current date and time.

## The visual canvas <a id="canvas"></a>

Build the workflow by dragging steps onto the canvas and connecting them with arrows. Each step has a configuration panel that opens when you click it. For long workflows you can create groups and labels to stay oriented.

Connect two steps by dragging from one connection point to the other, or by clicking one connection point and then the other. Scrolling with two fingers pans the canvas; pinching (or Ctrl/Cmd + wheel) zooms. Every step has a name, numbered by kind when you add more than one (“Check a condition”, “Check a condition 1”, “Check a condition 2”): to rename it, open the step's settings and click its title; Enter or clicking away saves, Esc cancels.

## Executions and the run log <a id="esecuzioni"></a>

Each run is saved in the workflow's “Executions” tab. It opens on the latest run, and every run has its own link that you can share with a colleague.

- **The canvas is the run** — Each step shows its icon, its name and a ✓ or ⚠ mark, with a step number that matches the log. Every output is labelled (“True”, “False”, “If delivery fails”). Arrows that ran are green; what did not run stays grey.
- **Click and double-click** — Click a step to select it in the log. Double-click a step, or a log row, to open it read-only: Input (what came from the previous step) on the left, Parameters in the middle, Output (with the branch taken and any error) on the right. Under Parameters, “Values used in this run” shows the values after the placeholders were filled in.
- **The “Execution log” panel** — Under the canvas, collapsed by default: click its bar to open or close it and drag to resize it. At the top you see the total time (for example “Failed in 1.8s”); each row is a step with icon, name, status, duration and the branch taken. The log opens on the failed step, or on the first one. For the selected step you choose Input, Output or both, and switch between Fields and JSON, with “Copy JSON”.

> [!NOTE]
> **Loops**
> A step that runs several times in the same run shows only one record: the single iterations are not shown yet.

> [!TIP]
> **Sending data to other systems**
> In the “Web request (HTTP)” and “Send data (webhook)” steps, placeholders (for example {{ contact.id }}) are filled in the URL, headers, query parameters and body, and the URL's own query string is kept. A JSON body is sent as JSON: {"id": "{{ contact.id }}"} sends the number 7, or null when the variable is missing. A header whose variable is missing is left out.
