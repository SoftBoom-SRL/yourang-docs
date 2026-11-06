---
title: "Calendar view"
description: "View and manage all reservations in a single intuitive interface"
section: "Reservations"
slug: "bookings/calendar-view"
---

# Calendar view

View and manage all reservations in a single intuitive interface

_The Yourang calendar view lets you see every reservation in real time, navigate by day, week, or month, and quickly access the details of each booking._

## Calendar view overview <a id="panoramica-calendario"></a>

The calendar shows the reservations of all your calendars in one grid, in the style of Google Calendar. Use the menu at the top right to switch between month, week and day, move with “Today” and the arrows, and narrow what you see with the panel on the right.

### Display modes <a id="modalita-visualizzazione"></a>

1. **Month view** — One line per reservation: dot, time and title. When a day has no room for all of them, “+N more” appears and a click opens that day's list. Clicking the day number opens the day view. The mouse wheel, or scrolling on a trackpad, moves to the next or previous month.
2. **Week view** — A 7-day overview with an hourly layout. Perfect for staff planning and spotting peaks.
3. **Day view** — Shows all reservations of a single day with exact times. Ideal for pre-service checks.

### Colours and reservation status <a id="codici-colore-stato"></a>

The colour is the calendar's: each calendar has its own (the same as in Google Calendar, if connected) and you find it again in the checkbox of the “Calendars” panel. The status is read from the dot next to the title, so it never depends on colour alone. All-day and multi-day reservations are solid bars in the calendar's colour.

**Filled dot - Confirmed or approved**
: The reservation is valid.

**Empty circle - Pending**
: Waiting for the customer's confirmation or for more information.

**Dashed circle - Cancellation requested**
: The customer asked to cancel and is waiting for your confirmation.

**Empty circle and struck-through title - Rejected**
: The reservation was rejected. The slot is available again.

### The panel on the right <a id="pannello-calendari"></a>

The panel starts closed: open it with the button at the top right (on small screens it opens as a drawer). It holds a mini calendar, the list of calendars, the status filter and the next reservation.

- **Mini calendar** — A click on a day moves the grid to that date without changing the view; a double click opens the day view of that date, with all its appointments. Changing the month in the mini calendar does not move the grid.
- **Calendars** — The list holds the Yourang calendar, the calendars chosen in the Google setup and any calendar an agent already books on. Untick a calendar to hide it: the choice is remembered in this browser. The “⋯” menu lets you show only that calendar or, if you have the permissions, open its settings.
- **Status** — Statuses work like the calendars: untick one to hide the reservations in that status, and press “Show all” to see them all again. The dot next to each status is the one the calendar draws; rejected reservations also have their title struck through.
- **Callbacks** — If you can see campaigns, the calendar also shows the scheduled callbacks: when the AI agent or an operator will call a customer back, because the customer asked during a call or an operator scheduled it. They appear as dashed-outline blocks with a phone icon, next to the bookings but without their colour, and they cannot be edited from here. A click opens the details: contact, number, campaign, who will call, who asked for it, notes, and a link to the campaign's contacts or to the original call. A callback leaves the calendar once it has been placed. Callbacks created outside campaigns (inbound calls and operators' manual calls) are visible only to owners and admins; campaign callbacks are visible to anyone who can see campaigns. Callbacks of a paused campaign are marked: they are placed only once the campaign resumes. In the «Callbacks» section of the panel you can hide them, and tick «Include automatic retries» to also see the retries campaigns plan on their own (usually many).
- **Sidebar notice** — When something is new, a blue dot appears in the sidebar on the section that holds «Reservations»; open it and «Reservations» shows a number: the bookings that arrived since you last opened the calendar plus the callbacks scheduled in the next 24 hours. The number updates every minute; bookings go back to zero when you open the calendar, callbacks disappear once they have been placed. Callbacks are counted only if you can see campaigns.
- **Agents' settings** — The «Agent settings» button at the top right of the panel opens the voice agents' booking settings: the same ones as on the agent's page (SMS, overlaps, number of people, calendar event title and description), with the list of agents on top. Tick the agents they apply to: on save each one gets exactly these settings and its bookings turn on, while unticked agents stay as they are. The form starts from the first ticked agent's settings, and a note names the agents that currently have different settings or bookings off. The event title is required and starts as «Prenotazione per {nome_cliente}»; the description starts as «Prenotazione di {nome_cliente} dal {data_inizio} al {data_fine}» and may be left empty. Only owners and admins see it.

### Creating a reservation from the calendar <a id="creazione-rapida"></a>

In month view, click an empty part of a day: a quick window opens with title, start and end time and the destination calendar. “Save” creates the reservation, “More options” opens the full form. The “New event” button also opens the full form; when creating you choose the calendar, when editing the calendar is only shown. Only people who can manage reservations see these actions.

> [!NOTE]
> **Quick interaction**
> Click any reservation in the calendar to view the full details: customer name, party size, time, special notes, and communication history.

Every reservation in the calendar is clickable and gives you immediate access to all relevant information, including customer contact details, recorded preferences, and the history of interactions with the voice assistant.
