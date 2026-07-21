# Cozy Farm Tracker

A single-file, offline-friendly web tool for tracking friend tatari during the **Cozy Farm** event in **Clash of Critters**. No install, no account, no server — just open in any browser on desktop or mobile.

🚀 **[➜ Open Cozy Farm Tracker](https://ajgonbas.github.io/coc-cozy-farm-tracker/)**

🔗 **Repository:** https://github.com/Ajgonbas/coc-cozy-farm-tracker

---

## How it works

During the Cozy Farm event, you visit friends' tatari and feed them crops to earn points. Each tatari belongs to a tatari line (e.g. Frugling, Maskfry), and each friend's tatari has its own tier (T1–T4), glitter status, and point value. Each round, up to 5 tatari lines are active — those are the ones you can feed.

This tracker helps you:
- Record each friend's tatari details and point values per tatari line
- Quickly see which friends give the most points for any given tatari line
- Sort by tatari line to plan your feeding route

---

## Setup (do this once per event)

### 1. Configure the Tatari Library
Click **📚 Tatari Lib** to manage your tatari lines. The modal is titled **Tatari + Food Line** and shows all registered tatari. Each entry has a name (e.g. `Frugling`) and a food type (e.g. `Dragon`).

The default lines are pre-loaded:

| Tatari Line | Food     |
|-------------|----------|
| Frugling    | Dragon   |
| Maskfry     | Phantom  |
| Droppit     | Carrot   |
| Pandaroo    | Bamboo   |
| Hootlet     | Clocko   |
| Punchimp    | Banana   |

You can add, rename, remove, or **drag and drop** to reorder lines. The order here is the same order shown in the Add/Edit Player screen and the main table columns.

### 2. Activate this round's tatari
On the main screen, click the tatari line chips to mark up to **5 as active** for the current round. Click a chip again to deactivate. Active chips control which columns are shown and which tatari appear in the sort buttons. Columns appear in the order you activate them.

### 3. Add your friends
Click **+ Add Player**, enter their name and optional UID, then fill in the tier (T1–T4), points, and glitter (✦) for each tatari line in the table. You can fill in data for all registered tatari lines — not just the active ones — so your data is ready when you switch rounds.

---

## Main screen

### Player table
Each active tatari line appears as a column. Click a column header to sort all players by their points for that line. Click again to toggle ascending/descending.

On **mobile**, a row of sort buttons appears below the search bar — one per active tatari line, plus a "Best overall" button.

### Sorting
- **Best overall (default):** players sorted by their highest single point value across all active tatari.
- **Column selected:** players sorted by points for that specific tatari line. Players with no data for that line appear at the bottom.

### Search
Type in the search bar to filter players by name or UID. Sorting is always applied on top of the current search. The search bar is persistent and does not reset on every keystroke.

---

## Per-player data

Each player has:
- **Name** and optional **UID** — used to detect and merge duplicates on import
- A 📋 **copy UID** button next to Edit and Delete on their card — tap to copy to clipboard
- For each tatari line (all registered, not just active):
  - **Tier** — T1, T2, T3, or T4
  - **Points** — the point value shown in-game
  - **Glitter** ✦ — whether the tatari is glittered (shown in gold in the table)

When editing a player, the tatari table follows the order set in the Tatari Library. A **?** tooltip next to the table header reminds you where to edit the list.

---

## Saving and loading

- **Auto-saves** to browser localStorage on every change.
- **Save JSON** — downloads a portable `cozy-farm.json` backup.
- **Import JSON** — merges incoming data with current data:
  - Players with matching UIDs have their tatari data **deep-merged** — incoming tatari lines overwrite per-line, but lines present only in the current data are preserved.
  - New tatari lines from the imported file are added to the library; existing lines keep their current active state.
  - Players without UIDs are always added as new entries.
  - If any UID conflicts are detected, a confirmation dialog lists them before committing.
- **Clear all** — wipes all players and resets to defaults. A confirmation dialog appears first. Your saved JSON is not affected.

---

## Help button

A **Help** button is available in both the desktop header and the mobile ☰ menu. It opens this README page on GitHub in a new tab.

---

## Mobile

The tracker works on mobile browsers. On small screens:
- The header collapses to a ☰ menu button containing all actions
- Each player is shown as a stacked card with their tatari in a horizontal scrollable row
- Tatari labels appear on each cell so you know which line you're looking at without column headers
- A sort button row replaces the column header sorting

---

## Credits

Built by **Kusanagi**.  
Discord: `kusanagi2k`

Issues or suggestions? Find me on Discord.
