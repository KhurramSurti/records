# Gold Hayat Cricket Team — Stats Hub

A self-contained cricket stats website for the Gold Hayat Cricket Team.
Only our own batting, bowling, fielding and captaincy records are tracked.
The team logo is built into the app, so nothing extra is needed for it to show.

## Files
- `index.html` — the whole app (logo is embedded inside it)
- `data.json` — your permanent records (team squad + every match)
- `Gold_Hayat_logo.jpg` — the logo image (optional spare copy; not required by the app)

## What's inside
- **Logo + branding** on every screen and on all PDF exports.
- **Theme switcher** (bottom-left): Midnight Gold, Daylight (light), Emerald, Royal Blue, Maroon.
  Backgrounds and text colours change together so data always stays readable. Your choice is remembered.
- **Squad** tab: add / remove players, mark substitutes (a one-off sub can also just be typed on the scorecard).
- **Filters**: opponent + month/season on Batting, Bowling, Fielding leaderboards.
- **Captains**: win-ratio comparison, record vs each team, per-captain detail.
- **PDF exports (landscape):**
  - Any match → open its scorecard → **Download scorecard PDF**.
  - **Batting → Top 10 PDF** and **Bowling → Top 10 PDF** (respects the active opponent/month filter).
  - To save: in the print dialog choose **Save as PDF**. Allow pop-ups the first time.

## Publish a free public link (GitHub Pages)
1. Free GitHub account → new **public** repo, e.g. `gold-hayat`.
2. Upload `index.html` and `data.json` (the logo is already embedded).
3. Repo **Settings → Pages → Source: main branch → Save**.
4. Link appears, like `https://yourname.github.io/gold-hayat/`.

## Add matches each Sunday (data stays safe)
1. **Add match** → fill batting / bowling / fielding / captain → **Save** (new matches are appended, never overwritten).
2. **Data & publish → Download data.json** → replace it in your repo and commit.
3. Keep a **Dated backup** after each match day. Formats available: T20, OD, Test Match, T10.

The app also keeps a working copy in your browser, and an amber banner reminds you
whenever you have unsaved matches to publish.
