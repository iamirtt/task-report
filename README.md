# Task Report — Mary Division

A single-page, no-install task/point tracker for a GTA V roleplay server division. Every rider's task counts, weekly totals, and activity history are tracked in one clean, dark-neon table — right in your browser, no backend required.

---

## 1. Getting Started

1. Download both `index.html` and `style.css` and keep them in the **same folder** (the page won't style correctly if they're separated).
2. Double-click `index.html` to open it in your browser (Chrome or Edge recommended).
3. That's it — no installation, no server, no account needed.

**Your data is saved automatically** in your browser's local storage every time you make a change. It stays there between sessions, but only on that browser, on that device.

> ⚠️ **Important:** Clearing your browser's cache/site data will erase everything. Get in the habit of using **📥 Export File** regularly (see below) so you always have a backup.

---

## 2. The Basics

### Adding a rider
Type a name into the **"New Rider's name..."** box and click **Add Rider** (or press Enter).

### Recording a task
Each rider has four task columns. Click **+** to add one completed task, or **−** to remove one (counts never go below 0):

| Task | Points |
|---|---|
| Traffic Stop (T) | 1 |
| Serghat Az Amval Omomi (S) | 2 |
| Car Pursuit (C) | 2 |
| Motorcycle Pursuit (M) | 4 |

The **Total Points** column updates automatically and is simply the sum of each task count × its point value above.

### Renaming a rider
Click the **✎** button next to their row, type the new name, and confirm. Their points carry over — nothing is lost.

### Removing a rider
Click the **✕** button next to their row. This is permanent (unless you still have a backup file — see Export/Import below).

### Searching
Use the **🔍 Search Rider...** box to instantly filter the table by name.

### Sorting
Click **↕ Sort: Score / Name** to toggle between:
- **Score** — highest total points first (default). The top 3 riders get medal icons: 🥇🥈🥉, with matching gold/silver/bronze coloring.
- **Name** — alphabetical order.

---

## 3. Weekly View

Click **📊 Weekly View** to switch to a clean, read-only display meant for sharing (e.g. a screenshot for the rest of the division):

- All editing controls (add/remove/rename, search, +/− buttons) are hidden.
- Only riders with **more than 0 points** are shown.
- The list is always sorted by score with medals visible.
- Nothing scrolls — everyone fits on one screen.

Click **✖ Exit Weekly View** to go back to normal editing.

---

## 4. Starting a New Week

When you're ready to close out the week and reset everyone's counts:

1. Click **🗓️ New Week**.
2. You'll be asked to confirm (or edit) the **date** for the week you're archiving.
3. You'll be asked for an optional **label** — e.g. `Week 5` or `Summer Event`. Leave it blank to just use the date.
4. Confirm the final prompt. This will:
   - Save a snapshot of everyone's current points into **History** (see below).
   - Reset every rider's task counts back to 0, ready for the new week.

This does **not** remove any riders from the list — only their points reset.

---

## 5. History

Click **📜 History** to open the archive panel. Each past week appears as an expandable row (click to open) showing:
- The week's label and/or date.
- Every rider's final total for that week, sorted highest to lowest, with a 🏆 marking the top scorer.

History is stored alongside the rest of your data, so it's included in your exported backup files too.

---

## 6. Activity Log

The panel next to the table (below it on smaller screens) keeps a running log of everything that happens:
- A rider gaining or losing a task point.
- A rider being added, removed, or renamed.

Each entry shows a timestamp. The log keeps the most recent 200 entries.

---

## 7. Backing Up Your Data

Because everything lives in your browser only, **regular backups are strongly recommended**.

- **📥 Export File** — downloads a `.json` file containing every rider, their points, your full history, and the activity log. Save this somewhere safe (cloud drive, USB, etc.).
- **📤 Import File** — loads a previously exported `.json` file, **replacing** whatever is currently on screen. Use this to restore a backup or to move your data to a different computer/browser.

> Tip: export a backup right after every "New Week" archive, so you never lose more than a week's worth of progress.

---

## 8. Exporting an Image

Click **🖼️ Export Image** to generate a PNG snapshot of the current table exactly as it looks on screen (works in both normal and Weekly View mode) — handy for posting a quick screenshot without using your OS's screenshot tool. The file downloads automatically as `daily-report-YYYY-MM-DD.png`.

> This feature needs an internet connection (it loads a small charting library from a CDN the first time you use it); everything else works fully offline.

---

## 9. Themes

Use the colored dots in the toolbar to switch the whole app's color scheme instantly:
- 🟣 **Purple** (default) — neon purple/violet
- ⚪ **Mono** — black, white, and grey

Your choice is remembered per-browser/device.

---

## 10. Moving to a New Computer / Sharing With Someone Else

Since data lives in the browser, not the files themselves:
1. On the old computer, click **📥 Export File**.
2. Copy `index.html`, `style.css`, and the exported `.json` file to the new computer.
3. Open `index.html` there, click **📤 Import File**, and select the `.json` file.

---

## 11. Troubleshooting

| Problem | Likely cause |
|---|---|
| Page looks unstyled / plain | `style.css` isn't in the same folder as `index.html`, or was renamed |
| Data disappeared | Browser cache/site data was cleared — restore from your last exported backup |
| "Export Image" doesn't work | No internet connection (it needs to load a library the first time) |
| Data doesn't show up on another device | Expected — data is per-browser. Use Export/Import to move it manually |

---

## 12. Files in This Project

| File | Purpose |
|---|---|
| `index.html` | The app itself — structure and all logic |
| `style.css` | All visual styling, including the theme presets |
| `README.md` | This guide |
