# Mordheim Campaign Map

Interactive campaign tracker for Mordheim. Place warband tokens on a district map, mark explored areas and footholds, and manage multiple campaigns — all in a single HTML file with no build tools or server required.

## Getting Started

1. Clone the repo and open `index.html` in a browser (works from `file://`)
2. Use the sidebar (hamburger menu top-left) to create warbands
3. Click a district on the map to open its menu and place tokens
4. Each warband per district has three states: **None**, **Explored** (●), or **Foothold** (⚜)

## Features

- **Interactive map** — zoom, pan, click districts to manage placements
- **Token stacking** — multiple warbands in the same district stack at center; count badge shown when 2+
- **Drag & drop** — drag tokens between districts to reassign
- **Multi-campaign** — create, rename, switch, and delete campaigns via the Settings tab
- **Data persistence** — all data stored in `localStorage`; export/import all campaigns as JSON
- **District calibration** — nudge/resize hit zones to align with your map image, save as defaults
- **Rules reference** — built-in campaign rules in the sidebar

## Project Structure

```
Mordheim_Map/
├── index.html           # Single-page application (all HTML, CSS, JS inline)
├── data/
│   ├── map_defaults.json       # Calibrated district positions (exported from app)
│   └── mordheim-campaigns.json  # Campaign backup (exported from app)
├── src/
│   ├── modheim-map-EN.jpg     # Campaign map image (4000×2829)
│   └── tokens/                 # 13 token pairs (explored + foothold)
│       ├── apple_explored.jpg
│       ├── apple_foothold.jpg
│       └── ...
└── README.md
```

## Usage Tips

- **First time** — create a warband in the sidebar, then click a district to place its token
- **Multiple warbands** — the district menu shows all warbands with inline None/Explored/Foothold buttons
- **Campaign management** — use Settings to keep different campaign groups separate
- **Calibration** — if zones don't match the map, open **Settings → Calibrate Districts** and use the panel
- **Save defaults** — after calibrating, click "Save as Default" to persist positions for new campaigns
- **Backup** — use "Save to file" in Settings to export all campaigns as a single JSON file

## Browser Notes

The app is designed to run from the `file://` protocol (no HTTP server). It uses `localStorage` for persistence and `addEventListener` for all dynamic interactions — inline `onclick` handlers generated via `innerHTML` are avoided since Chrome blocks them on `file://`.

## Credits

Original Mordheim Campaign Map created by Philip Spence (beyondthetabletop.com), with help from Roland Wenskus, Daniel Särnblom, Giuseppe Chiafele, Maxine Howells, Benoît Dumeaux, Hernan Garcia, Dennis Biegel, Alexander Bai, Kateryna Ruban, Olena Panova and Tuomas Pirinen. Based on the campaign by Chrismish 2010. Map Illustrated by Nuala Kennedy. Mordheim © Games Workshop Limited, All Rights Reserved.
