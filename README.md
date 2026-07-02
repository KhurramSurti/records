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


## One-click Publish (save straight to GitHub)
So you don't have to download + upload every time, set up one-click publish once:
1. Go to **Data & publish → One-click publish to GitHub**.
2. Enter your GitHub **owner (username)**, **repository**, branch (**main**), path (**data.json**).
3. Create a **fine-grained Personal Access Token** (GitHub → Settings → Developer settings →
   Fine-grained tokens): give it access to only your repo, permission **Contents: Read and write**,
   set an expiry. Paste it in and **Save publish settings**.
4. Now just tap **Publish now** (or the **Publish now** button in the amber banner) — your data.json
   is committed to GitHub automatically and the public site updates within ~1 minute.

Notes: the token is stored only in your browser, never in the code or on the public site. Add a
match → edit if needed → **Publish now**. Download data.json still works as a manual fallback.


## Player profiles (cricinfo-style, by format)
Open any player (Players tab or tap a name anywhere). Each profile now has:
- **Format tabs** — All formats / T20 / OD / Test Match / T10. Pick one and the whole
  profile (stats + charts + match log + vs-team) switches to that format.
- **Separate Batting and Bowling cards** with key numbers (runs, avg, SR, HS, 50s/100s;
  wickets, econ, avg, BBI, dots).
- **Charts**: Runs-by-month and Wickets-by-month bar charts (see how form is trending),
  a "How out" dismissal donut, and runs/wickets per-innings bars.
- **Career by format** tables (batting & bowling) comparing all four formats at a glance.
- **Match-by-match** log and **Against each team** split, filtered to the chosen format.


## Team & Captain views (format-wise + charts)
- **Dashboard (Team):** now has format tabs (All / T20 / OD / Test / T10). Everything —
  results donut, totals chart, this-month leaders, most runs/wickets, recent matches —
  switches to the chosen format. Button: **Team report PDF**.
- **Captains:** the list has format tabs + a Win% comparison chart, and each captain's page
  shows a **Results donut** and **Wins-by-month** chart, record vs each team, top scorer/bowler,
  and matches led — all filterable by format.

## Download PDF on every record (one click, landscape)
A PDF button is on every record: match scorecard, player profile, captain, Team report,
Captains list, Batting/Bowling/Fielding leaderboards, Venues and Records. Each opens a clean
landscape sheet with the logo and team name; choose **Save as PDF** in the print dialog.
Player and Captain PDFs follow the format tab you've selected.


## Player charts: Monthly vs By-Sunday (batting & bowling)
On each player profile, the batting and bowling charts have two views (toggle on the chart):
- **Monthly** — one bar per month (Jul, Aug, Sep …) for a season/year comparison. Batting shows
  runs, bowling shows wickets. Updates automatically as new months are added.
- **By Sunday** — pick a month; one bar per Sunday of that month (e.g. 6 Jul, 13 Jul …).
  The value sits above each bar; bowling shows "N wkts". If a Sunday had two matches
  (double-header), that day's totals are summed into one bar.
Both views respect the selected format tab (T20 / OD / Test / T10).


## Live scoring (ball-by-ball, offline, auto-saved)
At the start you pick today's **Playing XI**: all 13 squad names show as tappable chips (all selected by default) — tap the 2 who are resting to drop them, so only the playing 11 appear in every batsman/bowler/fielder pick for that match. Add a **substitute/guest** by name at this stage or mid-match via the **＋ Sub / ＋ Add player** buttons; their stats record automatically.

Start-match setup asks the **format** (T20 / OD / Test / T10); choosing it auto-fills the usual **overs** (OD = 8 for us, T20 = 20, T10 = 10) which you can change or type. Balls-left and overs are computed from that.

New **Live scoring** tab. Set up the match, then tap each ball: 0/1/2/3/4/6, Wide, No-ball, Wicket, Undo.
- We only score OUR team: our batting (per-batter shots → runs & balls) and our bowling (per-bowler overs, runs, wickets, dots, wides, no-balls). Opponent batters are never needed.
- Strike rotation is automatic (odd runs and end of over). On a wicket you pick how out and the next batsman.
- Bowling wickets can credit our fielder (catch/run-out/stumping) → feeds fielding stats.
- Every tap auto-saves to this browser, so nothing is lost if the phone locks or the page reloads — reopen the Live tab to resume.
- Tap **Finish & review** → it converts the whole innings into a normal scorecard (per-player runs, singles, dots, fours, sixes; bowlers' overs/runs/wickets), opens the Add-match form pre-filled so you can check it, then Save and Publish as usual.

Note: live scoring still needs one person tapping each ball during the match. If no one can score live, the manual Add-match entry after the game works exactly as before.


## Edit protection (view-only for others)
In **Data & publish → Edit protection**, set an **edit password**. After you Publish, anyone who opens the shared link gets a **view-only** app: Dashboard, leaderboards, player/captain/venue/records pages and PDFs all work, but **Add match, Squad, Schedule editing, Data & publish and Live scoring are hidden**, and Edit/Delete buttons disappear. Tap **🔒 View only — unlock** in the sidebar and enter the password to edit; **🔓 tap to lock** puts it back to view-only. Your password is stored only as a one-way hash (never in plain text).

This is a friendly lock for a shared link, not bank-grade security (the app runs in the browser). Your **permanent** record is protected separately: only a browser that has your **GitHub token** can actually save to GitHub — opening the app never writes anything by itself.


## Add match — smarter entry
- **We — first innings:** choose "We batted first" or "We bowled first". The cards reorder so the innings you did first is on top (bowled first → bowling card on top). No data is lost when you switch.
- **Auto-filled match summary:** Our total / wickets / overs and Opponent total / wickets / overs and the Result now compute automatically from the cards as you type — no manual entry. Our total = batsmen runs + an optional **Extras (ours)** field; our wickets = batsmen who got out; our overs = balls faced. Opponent total/wickets/overs come from your bowling card (plus run-outs from fielding). Result is set by comparing the two totals (you can still override it, e.g. No result for rain).
