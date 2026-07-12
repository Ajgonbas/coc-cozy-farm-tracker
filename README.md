# Cozy Farm Tracker

A single-file, offline-friendly web tool for tracking friend tatari during the **Cozy Farm** event in **Clash of Critters**. No install, no account, no server — just open the HTML file in any browser on desktop or mobile.

---

## How it works

During the Cozy Farm event, you visit friends' tatari and feed them crops to earn points. Each tatari belongs to a tatari line (e.g. Frugling, Maskfry), and each friend's tatari has its own tier (T1–T4), glitter status, and point value. Each round, up to 5 tatari lines are active — those are the ones you can feed.

This tracker helps you:
- Record each friend's tatari details and point values
- Quickly see which friends give the most points for any given tatari line
- Sort by tatari line to plan your feeding route

---

## Setup (do this once per event round)

### 1. Configure the Tatari Library
Click **📚 Tatari Lib** to manage your tatari lines. Each line has a name (e.g. `Frugling`) and a food type (e.g. `Dragon`). The default lines are pre-loaded:

| Tatari Line | Food     |
|---------------|----------|
| Frugling      | Dragon   |
| Maskfry       | Phantom  |
| Droppit       | Carrot   |
| Pandaroo      | Bamboo   |
| Hootlet       | Clocko   |
| Punchimp      | Banana   |

You can add, rename, or remove lines as the event evolves.

### 2. Activate this round's tatari
On the main screen, click the tatari line chips to mark up to **5 as active** for the current round. These are the tatari that appear for every player. Click a chip again to deactivate it.

### 3. Add your friends
Click **+ Add Player**, enter their name and UID, then fill in the tier (T1–T4), glitter (✦), and point value for each active tatari. Leave blank if a friend doesn't have a particular tatari.

---

## Main screen

### Tatari columns
Each active tatari line appears as a column. Click the column header to sort all players by their points for that line — useful for figuring out who to visit when you have a specific crop to feed. Click the header again to toggle ascending/descending. Click **clear** in the toolbar to go back to best-overall ordering.

### Sorting
- **Default (no column selected):** players sorted by their highest point value across all active tatari.
- **Column selected:** players sorted by their points for that specific tatari line. Players with no data for that line appear at the bottom.

### Search
Type in the search bar to filter players by name or UID. Sorting is always applied on top of the current search.

---

## Per-player data

Each player has:
- **Name** and optional **UID** (used to detect duplicates on import)
- For each active tatari line:
  - **Tier** — T1, T2, T3, or T4
  - **Points** — the point value shown in-game for that tatari
  - **Glitter** ✦ — whether the tatari is glittered (reflected in the gold colour)

Tier and glitter are per-player, per-tatari — two friends can have the same tatari line at different tiers.

---

## Saving and loading

- **Auto-saves** to browser localStorage on every change.
- **Save JSON** — downloads a portable `cozy-farm.json` backup.
- **Import JSON** — loads a previously saved file. If any player UIDs match existing entries, a warning lists the conflicts and lets you confirm before overwriting.
- **Clear all** — wipes all players and resets to defaults. A confirmation dialog appears first. Your saved JSON is not affected.

---

## Mobile

The tracker works on mobile browsers. On small screens:
- The header collapses to a ☰ menu button
- Each player is shown as a stacked card with their tatari in a horizontal scrollable row
- Tatari labels appear on each cell so you know which line you're looking at without column headers

---

## Credits

Built by **Kusanagi**.  
Discord: `kusanagi2k`

Issues or suggestions? Find me on Discord.
