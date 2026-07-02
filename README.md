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


## Finding a specific match (e.g. "the 28 June game vs Mulla XI")
Open **Matches** → use the **Opponent**, **Month**, or **Exact date** filter. Pick the date
and that day's match appears; tap it for the full scorecard — who scored what, and which
bowler conceded how much. Each match row also shows the weekday (Sun, Sat…).

## Schedule (upcoming fixtures)
**Schedule** tab: add upcoming matches with date, opponent, **venue**, Home/Away, format and a note.
When the match is played, tap **Record result** — the Add-match form opens pre-filled with that
fixture's date, opponent and venue. Recording a result removes it from the schedule automatically.

## Venues
Add-match now has a **Venue** field plus a **Match at**selector (Home / Away / Neutral).
The **Venues** tab shows results by ground, and a head-to-head "by venue" table —
i.e. how many times we've beaten each team at each venue.


## Editing or deleting a match later (safe)
Open any match's scorecard → **✎ Edit match** opens the form pre-filled with that match's
exact data; change anything and press **Update match** — it overwrites ONLY that one match,
every other match stays untouched. **🗑 Delete** removes just that single match (with a
confirmation). Adding a new match always *appends*; it never wipes older data.

Golden rule for total safety: after any add/edit/delete, go to **Data & publish → Download data.json**
and commit it to GitHub (and keep a Dated backup). The copy on GitHub is your permanent record.
