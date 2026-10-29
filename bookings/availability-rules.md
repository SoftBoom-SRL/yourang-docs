---
title: "Availability rules"
description: "Configure opening hours, time slots, and capacity for your business"
section: "Reservations"
slug: "bookings/availability-rules"
---

# Availability rules

Configure opening hours, time slots, and capacity for your business

_Availability rules define when and how your business accepts reservations. Yourang uses these rules to give the voice assistant the information it needs to handle customer requests accurately._

## Configuring opening hours <a id="configurazione-orari"></a>

Opening hours define the time windows in which your business accepts reservations. You can set different hours for each day of the week and manage exceptions for holidays and special days.

### Time-slot management <a id="gestione-slot-temporali"></a>

- Define the duration of each slot (e.g. 30, 60, 90 minutes)
- Set the intervals between consecutive reservations
- Configure different slots for different categories (breakfast, lunch, dinner, room service)
- Enable back-to-back reservations or enforce gaps between turns

### Capacity and limits per slot <a id="capacita-e-limiti"></a>

1. **Restaurants** — Maximum number of covers per slot. Yourang accounts for the number of people in each reservation and automatically rejects requests that exceed capacity.
2. **Hotels and B&Bs** — Number of rooms available per category. The assistant checks availability for the customer's specific needs (double, twin, suite).
3. **Function rooms and events** — Maximum capacity per event type. You can set different limits for private dinners, business meetings, or celebrations.

### Closure days and holiday exceptions <a id="giorni-chiusura-eccezioni"></a>

Yourang lets you mark specific days as unavailable (planned closures, public holidays, private events). The voice assistant will automatically tell the customer when the business is closed and suggest alternative available dates.

> [!WARNING]
> **Watch out for overbooking**
> If you don't configure capacity limits correctly, the assistant could accept more reservations than your business can host. Always verify that capacity data is accurate and up to date.

### Configuration examples <a id="esempi-configurazione"></a>

- Restaurant: 2 services of 90 minutes each (12:00-13:30 and 19:00-20:30), with a maximum capacity of 50 covers per service
- Hotel: 25 double rooms, 15 twin rooms, 5 suites, minimum 1-night bookings
- B&B: 4 rooms, bookings accepted from Friday to Sunday, minimum 2 nights on weekends
