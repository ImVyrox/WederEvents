# WederEvents

**Automated Scheduled Events System with PlaceholderAPI Support**

[![SpigotMC Resource](https://img.shields.io/badge/SpigotMC-137774-orange?style=for-the-badge&logo=spigotmc)](https://www.spigotmc.org/resources/wederevents.137774/)

WederEvents is a lightweight, fully configurable plugin that automates the scheduling and execution of server events like KOTH, tournaments, sumo battles, and drop parties. Trigger any command sequence automatically — on fixed daily intervals, clock-anchored cycles, or fixed daily times — and display live countdowns on scoreboards or holograms using PlaceholderAPI.

**Official Resource Page:** [SpigotMC - WederEvents](https://www.spigotmc.org/resources/wederevents.137774/)

---

## Key Features

* **Three Scheduling Modes:**
  * **Interval:** Simple countdown intervals (e.g., every 2 hours).
  * **Clock-Anchored:** Fixed cycles tied to wall-clock times (e.g., every 6h starting at `00:00`, `06:00`, `12:00`, `18:00`).
  * **Fixed Time:** Daily execution at specific times (e.g., `15:30`, `20:00`).
* **Timezone Support:** Set custom timezones (e.g., `America/La_Paz`) to maintain accurate schedules regardless of host server location.
* **Unlimited Events:** Define as many independent scheduled events as needed, each with unique timing and command sequences.
* **PlaceholderAPI Integration:** Live countdown and metadata placeholders for holograms, scoreboards, and chat broadcasts.
* **Duplicate-Execution Protection:** Built-in cooldown guard ensures event start-commands never double-fire.
* **Manual Controls:** Trigger any event on demand or reload configurations on the fly.
* **100% Configurable:** Customize messages, event names, and command execution chains from `config.yml`.

---

## Commands & Permissions

| Command | Description | Permission |
| :--- | :--- | :--- |
| `/wevent start <event>` | Manually trigger a configured event | `wevent.admin` |
| `/wevent reload` | Reload `config.yml` without restarting the server | `wevent.admin` |

---

## Placeholders (PlaceholderAPI)

| Placeholder | Description |
| :--- | :--- |
| `%wederevents_<event>_time%` | Live countdown (`HH:MM:SS`) to the next event execution |
| `%wederevents_<event>_displayname%` | Configured display name of the event |
| `%wederevents_<event>_schedule_type%` | Schedule mode (`INTERVAL`, `FIXED_INTERVAL`, or `FIXED_TIME`) |
| `%wederevents_<event>_raw_time%` | Raw time value configured in `config.yml` |

---

## Installation

1. Download `WederEvents.jar` from [SpigotMC](https://www.spigotmc.org/resources/wederevents.137774/).
2. Place the `.jar` file into your server's `/plugins` directory.
3. *(Optional)* Install **PlaceholderAPI** to enable live hologram and scoreboard countdowns.
4. Restart your server to generate configuration files.
5. Configure `config.yml` to set your timezone, events, schedule modes, and command actions.

---

## Requirements

* **Server Software:** Paper, Purpur, or any Paper fork (1.20+)
* **Java Version:** Java 21+
* **Dependencies:** *(Optional)* [PlaceholderAPI](https://www.spigotmc.org/resources/placeholderapi.6245/)
