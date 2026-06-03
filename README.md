# Mordheim Campaign Map

Interactive campaign map for Mordheim. Manage warbands, mark explored districts and footholds, track campaign progress — all in a single HTML file running from `file://` protocol with no server needed.

## Usage

Open `index.html` in a browser. Create warbands in the sidebar, then click districts on the map to place tokens. Three statuses per warband per district:

- **None** — not present
- **● Explored** — warband has scouted this district
- **⚜ Foothold** — warband controls this district (only one per district)

Tokens stack at the district center with the foothold on top. Drag tokens between districts to reposition.

## Campaigns

Multiple campaigns are stored in your browser's localStorage. Use the **Settings** tab to create, rename, switch, or delete campaigns. Export all campaigns to a JSON file for backup.

## Calibration

If district hit zones don't align with your map image, open the calibration panel from **Settings → Calibrate Districts** to nudge/resize zones. Save calibrated positions as defaults so new campaigns start with them.

## Credits

Original Mordheim Campaign Map created by Philip Spence (beyondthetabletop.com), with help from Roland Wenskus, Daniel Särnblom, Giuseppe Chiafele, Maxine Howells, Benoît Dumeaux, Hernan Garcia, Dennis Biegel, Alexander Bai, Kateryna Ruban, Olena Panova and Tuomas Pirinen. Based on the campaign by Chrismish 2010. Map Illustrated by Nuala Kennedy. Mordheim © Games Workshop Limited, All Rights Reserved.
