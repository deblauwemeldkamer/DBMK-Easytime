# DBMK-Time — Time & Weather Control (ESX Legacy)

> A modern admin utility for FiveM servers to control in-game time and weather in real-time.  
> **Price: €1.00** (support tier) to help fund continued development and updates.

![Banner](https://i.imgur.com/j1mDKln.png)

---

## Why DBMK-Time?

DBMK-Time is built for serious RP servers that need reliable synchronization, secure admin-only controls, and a clean UX without unnecessary complexity.

### Key Highlights
- Real-time global sync for all connected players
- Interactive 24h time control UI
- One-click weather selection (15 weather types)
- Admin-only access with configurable groups
- Rate limiting / anti-spam protection
- Multi-language support (`nl` / `en`)
- ESX Legacy compatible

---

## Price & Support

This project is available for **€1.00**.  
The low price is intentional and mainly acts as a **development support contribution**.

With purchase/support you get:
- Access to the latest build
- Update notifications
- Priority support via Discord
- Future maintenance improvements

---

## 🇬🇧 English

### Features
- Set in-game time via an interactive 24-hour clock UI
- Change weather with one click from 15 weather types
- Instant synchronization to **all players**
- Admin-only controls (group configurable)
- Request cooldown to prevent event overflow/spam
- Localization-ready UI and notifications

### Requirements
- [ESX Legacy](https://github.com/esx-framework/esx_core)

### Installation
1. Download this resource into your `resources` folder
2. Add `ensure DBMK-Time` to `server.cfg`
3. Configure `config.lua`

### Configuration (`config.lua`)
| Option | Default | Description |
|---|---|---|
| `Config.Locale` | `'nl'` | Language: `'nl'` or `'en'` |
| `Config.Command` | `'easytime'` | Command used to open UI |
| `Config.AdminGroups` | `{'admin','superadmin','mod','staff'}` | Allowed admin groups |
| `Config.Cooldown` | `2000` | Milliseconds between changes |

### Usage
- Open menu with `/easytime` or **F7**
- Pick time via clock/sliders
- Pick a weather type
- Click **Apply** to sync globally

---

## 🇳🇱 Nederlands

### Functies
- Stel ingame tijd in via een interactieve 24-uurs klok UI
- Stel het weer in met één klik uit 15 weertypes
- Directe synchronisatie naar **alle spelers**
- Alleen admins met juiste groep hebben toegang
- Cooldown/rate-limit tegen event spam
- Meertalige ondersteuning (`nl` / `en`)

### Vereisten
- [ESX Legacy](https://github.com/esx-framework/esx_core)

### Installatie
1. Plaats deze resource in je `resources` map
2. Voeg `ensure DBMK-Time` toe aan `server.cfg`
3. Stel `config.lua` in naar wens

### Gebruik
- Open menu met `/easytime` of **F7**
- Kies tijd en weertype
- Klik op **Apply/Toepassen** om alles te synchroniseren

---

## Add a New Language
1. Copy `locales/nl.json` to `locales/xx.json`
2. Translate values
3. Set `Config.Locale = 'xx'` in `config.lua`

---

## Permissions
Only users in `Config.AdminGroups` can open/use the menu.

---

## File Structure

```text
DBMK-Time/
├── client/
│   └── main.lua
├── server/
│   └── main.lua
├── html/
│   ├── index.html
│   ├── style.css
│   └── script.js
├── locales/
│   ├── nl.json
│   └── en.json
├── config.lua
├── fxmanifest.lua
└── README.md
