# DBMK-Time — Time & Weather Control

> Admin tool for FiveM (ESX Legacy) to control in-game time and weather for all players in real-time.

![Banner](https://i.imgur.com/j1mDKln.png)

---

## 🇬🇧 English

### Features
- Set in-game time via an interactive 24-hour clock UI
- Set weather with one click from 15 weather types
- Changes are synced to **all players** instantly
- Admin-only access (configurable groups)
- Rate limiting to prevent network event overflow
- Multi-language support (`nl` / `en`)

### Requirements
- [ESX Legacy](https://github.com/esx-framework/esx_core)

### Installation
1. Download or clone this repository into your `resources` folder
2. Add `ensure DBMK-Time` to your `server.cfg`
3. Configure `config.lua` to your liking

### Configuration (`config.lua`)
| Option | Default | Description |
|---|---|---|
| `Config.Locale` | `'nl'` | Language: `'nl'` or `'en'` |
| `Config.Command` | `'easytime'` | Command to open the UI |
| `Config.AdminGroups` | `{'admin','superadmin','mod','staff'}` | Groups with access |
| `Config.Cooldown` | `2000` | Milliseconds between changes |

### Usage
- Open the menu with `/easytime` or press **F7**
- Select a time using the clock or sliders
- Select a weather type
- Press **Apply** to sync to all players

### Adding a language
1. Copy `locales/nl.json` to `locales/xx.json`
2. Translate all values
3. Set `Config.Locale = 'xx'` in `config.lua`

### Permissions
Only players in the configured `Config.AdminGroups` can open and use the menu.

---

## 🇳🇱 Nederlands

### Functies
- Stel de ingame tijd in via een interactieve 24-uurs klok UI
- Stel het weer in met één klik uit 15 weertypes
- Wijzigingen worden direct gesynchroniseerd naar **alle spelers**
- Alleen toegankelijk voor admins (configureerbare groepen)
- Rate limiting om network event overflow te voorkomen
- Meertalige ondersteuning (`nl` / `en`)

### Vereisten
- [ESX Legacy](https://github.com/esx-framework/esx_core)

### Installatie
1. Download of clone deze repository naar je `resources` map
2. Voeg `ensure DBMK-Time` toe aan je `server.cfg`
3. Pas `config.lua` aan naar wens

### Configuratie (`config.lua`)
| Optie | Standaard | Beschrijving |
|---|---|---|
| `Config.Locale` | `'nl'` | Taal: `'nl'` of `'en'` |
| `Config.Command` | `'easytime'` | Commando om het menu te openen |
| `Config.AdminGroups` | `{'admin','superadmin','mod','staff'}` | Groepen met toegang |
| `Config.Cooldown` | `2000` | Milliseconden tussen wijzigingen |

### Gebruik
- Open het menu met `/easytime` of druk op **F7**
- Selecteer een tijd via de klok of sliders
- Selecteer een weertype
- Druk op **Toepassen** om te synchroniseren naar alle spelers

### Taal toevoegen
1. Kopieer `locales/nl.json` naar `locales/xx.json`
2. Vertaal alle waarden
3. Stel `Config.Locale = 'xx'` in in `config.lua`

### Rechten
Alleen spelers in de geconfigureerde `Config.AdminGroups` kunnen het menu openen en gebruiken.

---

## File Structure

```
DBMK-Time/
├── client/
│   └── main.lua          # Client-side logic
├── server/
│   └── main.lua          # Server-side logic + permission checks
├── html/
│   ├── index.html        # NUI interface
│   ├── style.css         # Styling
│   └── script.js         # UI logic
├── locales/
│   ├── nl.json           # Dutch translations
│   └── en.json           # English translations
├── config.lua            # Configuration
├── fxmanifest.lua        # Resource manifest
└── README.md
```

## License

MIT — free to use, modify and distribute. Credits appreciated.
