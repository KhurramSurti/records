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


## Bowling 4s/6s conceded + proper result/target
- The bowling card now has **4s** and **6s conceded** columns (per bowler). These flow into the bowling leaderboard (sortable — filter by month to see who conceded the most sixes), the scorecard, and each bowler's profile (overall and by-format).
- **Target** is shown automatically (first innings total + 1) and the **result margin** is computed by cricket rules: batting-first win → "Won by N runs"; successful chase → "Won/Lost by N wickets"; equal → "Match tied"; plus **Draw** (Test) and **No result**. Which side "won by runs vs wickets" depends on the "We — first innings" choice.


## Wicket types + Playing XI / DNB
- **Bowling wicket types:** the bowling card now has **Bwd / LBW / Ct / St** count boxes per bowler; **Wkts fills automatically** as their sum (run-outs are credited to fielders, not the bowler). Each bowler's profile shows a "How wickets fell: Bowled/Caught/LBW/Stumped" breakdown, so you can see and compare how a bowler takes wickets. Captured in **both** manual Add match and Live scoring.
- **Playing XI + DNB:** Add match now starts with a **Playing XI** picker (drop the 2 resting; only the XI appear in the name boxes; add a substitute if needed). Players in the XI who don't bat are shown on the scorecard as **"Did not bat" (DNB)** — the same as Live, where the chosen XI carries through automatically.


## Bowling dots/runs auto + Match Summary poster
- **Auto dots & runs:** the bowling card now takes the conceded shot breakdown (1s/2s/3s/4s/6s + wides/no-balls + wicket types). Over = 6 legal balls, so **Dots = 6 − scoring balls** and **Runs** compute automatically (extras add to runs but not to balls). Example: an over of 2, 6, 4 → 12 runs, 3 dots. Live scoring already tracks this ball-by-ball, so both entry paths stay consistent.
- **Match Summary poster:** open any scorecard → **📤 Match summary** for a shareable poster (teams, top scorer / most sixes / extras, full batting card with SR + dismissals, Did-Not-Bat, key stats, target, bowling card + per-bowler summary, catches, run-outs, MOTM, and the correct result — "won by runs / by wickets"). **⬇ Download / Share** opens a clean full-page version to Save as PDF and send on WhatsApp (turn on "Background graphics" in the print dialog to keep the dark theme).


## Compare players (head to head)
A new **Compare** tab (under Leaderboards) puts any two players side by side. Pick Player A and Player B, then filter by **format** and/or a single **opponent** — so you can answer "who's the better bowler against Mulla XI" or "how do these two batsmen compare this season." Batting rows: innings, runs, highest, average, strike rate, 50s, 100s, 4s, 6s, ducks. Bowling rows: innings, overs, wickets, economy, average, best (BBI), dots, bowled/caught/lbw/stumped, and 4s/6s conceded. The stronger number in each row is highlighted in gold (lower is better for economy, average, ducks and runs conceded).


## Match numbers
Every match gets an automatic number like **Match #0001**, shown in the Matches list, on the scorecard, on the summary poster, and (tentatively) during live scoring. Numbers run in **play order** — sorted by date, and for two matches on the same Sunday, by the order you entered them — so you can always tell which game came first. The count of matches in any period (e.g. July–Dec 2026) is on the Matches page.


## Refresh data button
A **↻ Refresh data** button (in the sidebar, and as ↻ in the mobile top bar) pulls the latest **published** data.json straight from GitHub, bypassing the browser/CDN cache, and re-renders instantly — no hard refresh needed. It works for view-only visitors too, so everyone always sees the newest data. If you're the editor and have unsaved local changes, it asks first before replacing them with the published version. (Note: a web page can't wipe the whole browser's cache/cookies for security reasons, but this button achieves the same result — always-fresh published data.)


## Extras entry
Extras are now entered right inside the cards: under the **Batting card** you'll see "Batting runs + Extras (wides/no-balls/byes to us) = Total", so entering e.g. 76 runs + 14 extras shows a Total of 90 (and the opponent's target becomes 91). Opponent byes/leg-byes go under the **Bowling card** ("Extras conceded not on a bowler"). Per-bowler wides and no-balls stay in the bowling table as before.


## Premium themes (default: White)
Four full-background themes in the sidebar — **White (default), Cream, Grey, Black**. Clicking a swatch changes the whole background and re-tunes every text colour for strong contrast; the gold accent is tuned per theme. New visitors see White by default; each person's choice is remembered on their device. The mobile top bar (logo, refresh ↻, menu ☰) now follows the theme too, so it stays clearly visible on light themes.


## Tasteful depth & motion (mobile-first, no heavy 3D)
Subtle premium polish that stays fast and legible: soft elevation shadows on cards, a gentle lift on hover / press feedback on tap, smooth fade-in when switching views, button press animation, a light 3D tilt on the logo crest, and a quick count-up on the dashboard's Won / Lost / Win-rate numbers. Everything respects "reduced motion" system settings and adds no heavy 3D or performance cost.


## Design pass — alignment & premium polish
- **Dashboard hero:** the Won / Lost / Win-rate stats are now a properly aligned cluster — each number centred over its label, separated by hairline dividers — so widths never throw the labels off. Added a cricket-native **Recent form** guide (last five results as W/L/T pills) as the signature element.
- **Global rhythm:** refined type scale (display headings, eyebrows, labels), consistent card radius and spacing, and tightened table headers/rows with clear right-aligned numerics and a subtle row hover. These are shared tokens/components, so every screen lifts at once.


## Street-cricket rules & sound
- **LBW removed** everywhere (bowling card, live wicket picker, batting "how out", comparison, profiles). Bowling wickets are now Bowled + Caught + Stumped; run-outs stay credited to the fielder.
- **Sound** is now a crisp mechanical "tick" (like a phone keypad) on taps, with the Sound on/off toggle in the sidebar and mobile top bar.
- Dismissal options: caught, bowled, run out, stumped, hit wicket, retired, not out.


## Live extras with runs + one-page portrait PDFs
- **Wide / No-ball runs picker (live):** tapping Wide or No ball now asks "total runs on this ball?" (1–5). A plain wide is 1; if the batsmen also run, pick the total (e.g. wide + 2 run = 3). It's added to the score and the bowler's extras, and correctly does NOT count as a legal ball.
- **PDF downloads are now portrait and fit on a single page.** Every report (team, batting, bowling, player, captain, venues, records) and each match scorecard scales to one A4 portrait page. The match PDF also includes the per-bowler **bowling summary**. Keep "Background graphics" on in the print dialog for full colour.


## Reports section (new)
A dedicated **Reports** tab (under Overview, available to everyone) for downloads:
- **Match summary:** pick any match from the dropdown and download its full premium one-page summary (or preview it first).
- **Batting top-10 lists:** Most runs, sixes, fours, singles, doubles, threes, fifties, and best strike rate.
- **Bowling top-10 lists:** Most wickets, wides, runs conceded, sixes conceded, fours conceded, dot balls, no-balls, and best economy.
Each opens as a clean one-page PDF to save or share. Existing pages (Batting/Bowling leaderboards, Records, etc.) are unchanged and still sortable.


## Match download — print-optimised premium summary
The match "Download PDF" now produces a clean, print-ready version of the summary: a light layout where every card, table and highlight is defined by borders and gold accents, so it looks premium in the PDF **without needing "Background graphics" turned on**. It uses the full page width (large and readable) and flows across at most two A4 portrait pages, with cards kept whole (never split mid-card). Batting and bowling are clearly separated sections.



## Reports & summary — layout fixes
- **All top-10 reports redesigned:** every leaderboard report (batting: runs/sixes/fours/singles/doubles/threes/fifties/SR; bowling: wickets/wides/runs/sixes/fours conceded/dots/no-balls/economy) now shows a **centred ranked list** with gold/silver/bronze rank badges, the player name and detail, and a large gold value — readable at 100%, no more stretched columns. They all share one layout, so the whole section is consistent.
- **Match summary is now compact and fits ~2 pages:** the logo is removed from the download header and spacing tightened, so bowling lands on page 1 and batting + result on page 2 (was breaking to 3).
- Meta line (Date/Venue/Format/Captain/Toss) uses fixed columns so values never run together; "Most wickets" breaks ties by fewest runs conceded.


## Match summary — clean page split
The downloadable summary now breaks cleanly into two pages by innings: **page 1** holds the complete first-innings section plus the target, and **page 2** holds the complete second-innings section plus the result. If you bowled first: page 1 = full bowling + target, page 2 = full batting + result. If you batted first: page 1 = full batting + target, page 2 = full bowling + result. No section is split across pages.


## Reports now use a content-fit page
Leaderboard/top-10 reports no longer print on a big empty A4 sheet. The PDF page **shrinks to fit the content** — a fixed readable width with the height sized to however many rows there are. Three players makes a short, tidy page; a full top-10 makes a taller one. Everything stays large and clearly presented (rank badges, bold names, big gold values), and it's ideal for sharing on WhatsApp. The match summary still uses its clean two A4 pages.


## Bowling innings fix
Bowling "innings" now counts the number of matches in which a bowler actually bowled — not the number of overs. A bowler's separate overs/spells within one match are combined first, so two matches where they bowled = 2 innings (with the overs summed). If a bowler got no over in one of the matches, that match doesn't count as an innings for them. Best bowling (BBI) and 3-wicket hauls are now measured per match too. Batting is a completely separate section and is unaffected.


## Compare — categories, multiple players, download
The Compare tab now lets you:
- **Pick a category** (Batting / Bowling / Fielding) and the right fields load automatically — batting shows runs/average/SR/50s/6s/etc., bowling shows wickets/economy/BBI/wides/6s conceded/etc., fielding shows catches/run-outs/stumpings/total.
- **Compare 2 to 4 players** at once (Add player / remove), each with its own colour, shown as grouped bars per metric with the leader highlighted.
- **Download** the comparison as a PDF (the page sizes to the content, like the other reports — never a tiny table on a big empty sheet).



## Dashboard — command center (with sparklines & auto highlights)
The dashboard is a professional command center tuned for club data:
- **KPI row** — six gradient cards (Matches, Win rate, Total runs, Total wickets, Highest total, Best bowling), each with a **mini sparkline** of its trend across matches.
- **Team highlights** — an auto-generated insights panel (win/loss streak, batting leader, bowling leader, best economy, highest total) that reads like a briefing.
- **Results donut with a legend table** (Won/Lost/Tied + counts + %).
- **Charts** — runs-per-match trend, win-rate-by-format, top run-scorers and top wicket-takers as bars, plus a recent-matches card.
Everything follows the active theme and stays fast on mobile — full and premium without empty filler.


## Mobile responsiveness audit
Fixed the horizontal-overflow issue that made wide tables get cut off on phones and pushed the page sideways (so the menu only appeared after sliding). Root cause: the main content column (a grid item) wasn't allowed to shrink below its content, and the table container clipped instead of scrolling.
- Table containers now scroll horizontally on their own (swipe the scorecard's bowling/batting tables left–right) instead of clipping.
- The main column can shrink to the screen width, so nothing pushes the page sideways.
- Added a viewport-width guard on the app shell as a safety net.
Every data table across the app (scorecard, leaderboards, player/captain profiles, records, add-match cards, schedule, data) is inside a horizontal-scroll container, and filters/controls wrap to fit narrow screens.


## Mobile: narrow tables fit without scrolling
Checked every leaderboard/team table's width on a 360px phone:
- Batting and Bowling genuinely have many columns (14), so they keep a horizontal swipe — the normal pattern for dense stats (tap a player for the full profile).
- Fielding, Captains, Venues and Records had only a few columns but were overflowing because of wide headers and long names. These now fit the phone with no sideways scroll: player/opponent/venue names wrap, spacing tightens on small screens, and fielding uses the standard Ct / RO / St / Tot headers.


## Batting: default not out, and retired counts as not out
- When you add a match, each batter's dismissal now defaults to **not out** — so you consciously change it to how they actually got out, rather than an accidental "caught".
- **Retired** is now treated as **not out** for the record: it counts as an innings but not as a dismissal, so it doesn't hurt the batting average and a retired-for-0 is never a duck — matching the cricket rule that an innings isn't "out" until the batter is properly dismissed.


## Stable match order + retired not a wicket
- The Matches list now sorts by date (newest first) and then by match number (newest first) — so within the same day it reads #0004, #0003, #0002, #0001, and editing a match never jumps it to the top. The order is fixed by date and sequence, not by when you last edited.
- When a match is entered/edited, a **retired** batter no longer adds to "our wickets", so the result margin is correct (e.g. one out + one retired = one wicket down). Note: for any match saved before this fix, open it in Edit and Save once to recalculate its wickets.


## Editing keeps your Playing XI and guests
When you edit a match, the Playing XI now loads exactly as you saved it — the players you rested stay excluded and any guest/substitute players are restored — instead of resetting to all 13 squad members. So you no longer have to re-drop the resting players or re-add guests, and Did Not Bat stays correct.


## Dashboard — Home vs Away & Record by venue
- **Home vs Away** — a stacked won/lost/tied bar for Home and for Away, with the W-L counts.
- **Record by venue** — replaced the earlier "wins by venue" donut (which showed 100% whenever you play at a single ground and could be misread as a 100% win rate). It now shows each ground's actual result split and win rate — e.g. Uni Plaza 2W · 2L · 50% — so it's honest and useful with any number of venues.


## Retired shows as "retired", not "not out"
On the scorecard, a retired batter no longer gets a "not out" tag next to their name — the How-out column already reads "retired". Only genuinely not-out batters show the "not out" tag, so the card can't look like three players are not out. (Retired is still treated as not-out for averages, as before.)


## Fielding innings column
The Fielding leaderboard now has an **Inns** column showing how many innings each fielder was on the field (the matches they were in the Playing XI). This gives context to the catches/run-outs/stumpings, since players don't all play the same number of matches. It's sortable and included in the fielding PDF.


## Bowling: 5W (five-wicket hauls)
The Bowling leaderboard now has a **5W** column alongside 3W, so five-wicket hauls are recognised. 3W counts innings with 3 or more wickets and 5W counts innings with 5 or more, so a five-fer shows up in both. Included in the bowling PDF too.


## Schedule: edit fixtures + View result
- Fixtures now have an **Edit** button (alongside Remove) so you can change the opponent, venue, date, format or note — handy when a match is cancelled and you line up a different team.
- Once a fixture's match has been recorded, its button changes from **Record result** to **View result** (which opens the Matches page), and the fixture shows a "recorded" tag. A fixture counts as recorded when a saved match shares its date and opponent name, so keep the opponent spelling consistent (or use Edit to match it).


## View result filters to that opponent + per-innings wickets fix
- Tapping **View result** on a fixture now opens the Matches page with the opponent filter already set to that team, so you see only that fixture's match(es).
- Fixed the player profile "Wickets per innings" chart (and the match log's bowling figures): they were showing only the first over of a spell, so a 3-wicket innings looked like "1". They now combine all of a bowler's overs in a match, so the per-innings wickets and figures (e.g. 3/18) are correct.


## Chart fix: tallest bar no longer clipped
The per-innings bar charts (Runs per innings and Wickets per innings on the player profile) were drawing the tallest bar and its number right up to the top edge, so the value got cut off. Added top headroom so the biggest bar and its label always fit. Wickets-by-month and the dashboard trend charts already had enough space.


## Schedule: next match pulses
The soonest upcoming fixture now gently pulses and carries a gold "NEXT" tag, so your next match stands out. It always tracks whichever upcoming fixture is nearest by date, so if you edit or remove one, the highlight moves automatically. Honors reduced-motion settings (shows a steady highlight instead of animating).


## #1 leaderboard player pulses
The top-ranked player in each leaderboard (Batting, Bowling, Fielding) now gently pulses with a gold highlight, so the current number one stands out. It follows the active sort, so re-sorting moves the highlight to the new leader. Honors reduced-motion settings.


## Matches column (Mat) + captaincy audit
- **Batting and Bowling leaderboards** now have a **Mat** column before Inns: Mat = how many matches the player was in the Playing XI, while Inns = how many times they actually batted / bowled. So you can see, e.g., a player picked in 4 matches who only batted twice or bowled in three. Included in the leaderboard PDFs.
- **Captaincy audit:** open a captain (Team → Captains → a name) and you'll see **"Player opportunities under [captain]"** — a table of every player with matches in the XI, batting innings, bowling innings, overs, runs scored, runs conceded and wickets, all under that captain, sorted by most selected. It makes it easy to spot who was under-used (in the XI a lot but rarely given a bat or bowl) under a particular captain.


## Captaincy audit table is sortable
The "Player opportunities under [captain]" table can now be sorted by any column — tap a header (Mat, Bat, Bowl, Overs, Runs, Conc, Wkts, or Player) to sort, and tap again to flip between largest-to-smallest and smallest-to-largest. Makes it quick to find, say, the players with the most matches but fewest bat/bowl chances under a captain.


## Auto-refresh, best spell, and batting positions
- **Auto-refresh every 5 minutes:** the app now quietly re-fetches the published data (no-cache, so no stale copies) every five minutes and on load, so viewers always see the latest. It only re-renders when something actually changed, and it never interrupts you while you're editing, scoring live, or have unpublished changes.
- **Best bowling spell (dashboard):** the "Best bowling" KPI now shows the single best innings figures anyone has produced (e.g. 3/8) with that bowler's name — the true best spell, not just the leading wicket-taker's best.
- **Runs by batting position (new "By position" tab):** for each spot in the order (1, 2, 3…), see which batsmen have scored most there, with innings, runs, highest, average and strike rate. Handy for picking the batting line-up.



## Two-team worm graph (scorecard)
Each scorecard shows a scoring-comparison worm of both innings on one chart: the opponent's actual over-by-over line (from our bowling, with red dots where wickets fell) and Gold Hayat's run line. Because we log our own batting per batsman rather than per over, Gold Hayat's line is drawn as an even run-rate line (dashed) while the opponent's is the true over-by-over shape — this is noted on the chart. A genuine ball-by-ball worm for our own innings is possible for live-scored matches in future.


## Opponent bowling is free-text and isolated
The Opponent bowling card's name field is a plain text box (placeholder "e.g. Bowler 1") — there's no opponent squad, no XI picker, and no autocomplete linked to your team. Type "Bowler 1", "Bowler 2", or a real name if you know it. These names live only inside the match's opponent-bowling entry: they never appear in your players list, XI picker, any leaderboard, or any report — this card exists solely to draw the worm graph.


## 5W now actually in the bowling table
An earlier attempt to add the 5W column to the Bowling leaderboard hadn't taken effect (a silent text-match miss), so it wasn't appearing. It's now added for real — the Bowling table shows 3W then 5W then 4s, and the empty-state column counts were corrected. The bowling PDF already includes 5W.



## Bowling by order — fixed to be per over
The "Bowling by order" tab now works by over number, not by who came on first. Each spot is an actual over of our bowling innings — 1st over, 2nd over, and so on — and shows only that over's figures. So a bowler who bowled the 1st over in four matches shows 4 innings and 4 overs at "1st over" (not their whole spell), and if they also bowled, say, the 5th over in some games, that appears separately under "5th over". This lines up because bowling is entered over-by-over in sequence.


## Full audit (all features verified)
Audited the entire file feature-by-feature. Every requested feature is present and working: cricket rules (no LBW anywhere selectable, retired = not out and not a wicket, default dismissal "not out"), bowling innings counted per match, Mat columns, fielding Inns, 3W/5W, captaincy audit (sortable), Batting order & Bowling order (per-over), multi-player Compare with categories and content-fit download, Reports with rank-badge PDFs, two-team worm graph with the isolated Opponent-bowling card, dashboard command center (KPI sparklines, highlights, home/away, venue record, best spell), schedule Edit / View-result / next-match pulse, stable match ordering, edit restoring XI+guests+opponent bowling, 5-minute auto-refresh with fresh-on-load, and the mobile responsiveness fixes. One regression was found and fixed during the audit: the 3W/5W counting had reverted to exclusive (a five-for wasn't counting as a 3W); it now counts in both, verified by test. A full render smoke-test of all 18 views passes.



## Bat first vs Chase — premium redesign
Rebuilt the "Bat 1st vs Chase" tab to be self-explanatory and richer:
- Two donut cards ("When we bat first" / "When we chase") with a colour legend, matches played, and a clear win-rate line — no jargon.
- A multi-line "run-scoring form" chart showing the top batsmen's running totals innings by innings (with a named legend), in the trend-line style you shared.
- Clear grouped tables for Batsmen (Batting first vs Chasing: Inns, Runs, SR), Bowlers (Bowling first vs Defending: Overs, Wkts, Econ) and Captains (Chasing a target vs Defending a total: Played, Won-Lost, Win rate). Every column is labelled in plain words, a short caption explains each block, the stronger side is highlighted in gold, and a subtle vertical divider separates the two situations. Jargon like "Chase P / W-L / %" is gone.


## Splits refinements + sortable everywhere
- Batsmen table now includes batting Average (alongside Inns, Runs, SR) in each situation; Bowlers table now shows Runs conceded (alongside Overs, Wkts, Econ).
- Removed the run-scoring form line chart for now (it needs more matches to read well) — it can come back once there's more data.
- Every column in the Bat-first-vs-Chase tables (Batsmen, Bowlers, Captains) is now tap-to-sort, ascending/descending.
- Audited all leaderboards for sorting: Batting, Bowling, Fielding and Captains were already sortable; added sorting to the Venues "results by venue" table. Players is a card grid (nothing to sort) and the Records/Positions views are situational breakdowns already ordered by their key metric.


## Page-head title alignment
On the three newer views (Bat first vs Chase, Batting order, Bowling order) the heading was drifting to the right because the eyebrow and title weren't wrapped together — the flex page-head (space-between) was pushing them to opposite ends. Wrapped the eyebrow/title/description in a single container like every other page, so the title now sits left-aligned as expected. Verified by DOM that each page-head now has one wrapper child holding the eyebrow and h2.



## Split tables: two-tone groups + worm shows every wicket
- Split tables (Bat first vs Chase, and the bowling one): removed the sticky column and the heavy divider line. Instead the two situations are shown as two soft background bands — the first group light grey, the second cream — so on mobile it's immediately clear which columns belong to which side, without any thick line. Verified by pixel sampling that the name column, grey group and cream group are three visibly distinct shades.
- Worm graph: when more than one wicket falls in the same over, the red dot now carries the count (e.g. a "2"), so the graph reflects every wicket. Previously an over with two wickets only showed one dot, so seven wickets looked like five. Verified that eight overs with wickets 0,2,1,1,0,1,0,2 now render as five dots totalling seven (two of them marked "2").


## Schedule: every past series shows + Load more
The past section wasn't actually capped at two, and recording a match no longer deletes its fixture — but a series with no saved fixture (like the Mulla XI game) simply wasn't appearing. Now the "Past fixtures & results" section lists every recorded series, pulling in any match that has no matching fixture as a read-only "View result" row, so nothing goes missing. It shows the six most recent by default with a "Load more" button to reveal older ones, and there's no limit on how many it can hold.


## Sort by name everywhere
Every leaderboard column header is now tap-to-sort including the name column, and a faint up/down indicator on each header makes it clear the column is sortable (previously the arrow only appeared once a column was active, so name-sorting wasn't discoverable). The Batting order and Bowling order per-position tables, which weren't sortable before, now sort by name and every stat too. Name and venue columns sort A to Z on the first tap (Z to A on the second); number columns still lead with the highest value.


## Visitor counts (GoatCounter)
The app now includes a small GoatCounter tracking script in the head, pointing at https://goldhayat.goatcounter.com/count. It loads asynchronously so it doesn't slow the page, sets no cookies and stores no personal data about visitors. Once the updated index.html is live, sign in at https://goldhayat.goatcounter.com to see daily visitor counts, which pages are viewed and where traffic came from. Nothing about it is visible to visitors, and it has no effect on the cricket data or any of the app's own features.


## Visitors page (in-app)
There's now a "Visitors" tab under Overview, so you can see the numbers inside the Stats Hub itself instead of opening another site. It reads GoatCounter's public counter endpoint (/counter/TOTAL.json) and shows Today, Last 7 days, Last 30 days and All-time visitor counts, a bar chart of the last 14 days, and your busiest day. There's a Refresh button, and results are kept in memory so switching tabs doesn't re-fetch.

**One-time setup:** open https://goldhayat.goatcounter.com/settings and tick "Allow adding visitor counts on your website" — that permission is off by default and is what lets the app read its own totals. Until it's on, the page shows a note explaining this. Note that GoatCounter caches counter responses for up to a few hours, so today's number can lag slightly; the full dashboard (linked from the page) still has pages, referrers and the rest.


## Visitors: timezone fix
The Visitors page was building its day ranges from the UTC date, so in Pakistan (UTC+5) the "Today" figure and the daily bars could query the wrong day in the early hours. They now use the local calendar date.

## Test Match & T10 — proper two-innings scoring (NEW)
Test Match and T10 are now scored as **real two-innings-per-side games** (T10 = a Test
played with each innings capped at ten overs, finished in a day). T20 and OD are unchanged —
they stay single-innings and behave exactly as before.

**How to enter a Test/T10 match**
1. In **Add match**, pick **Test Match** or **T10** as the Format. A gold-bordered
   **Second innings** section appears below the normal cards.
2. Fill the **first-innings** batting, bowling and fielding as usual (these are now labelled
   "· 1st innings").
3. Fill the **Second innings** section the same way — 2nd-innings batting, bowling and fielding.
   Leave it blank if the match was decided inside one innings.
4. **Target** and **Result** are worked out automatically on the **two-innings aggregate**:
   the side batting last chases *(other side's two-innings total − its own first innings + 1)*.
   The result reads like a real Test — "Won by 5 runs", "Won by 6 wickets", or "Match drawn"
   (choose **Draw (Test)** in the Result box for a draw).

**Where the second innings shows up**
- The **scorecard** shows both innings for each side, clearly labelled, with the aggregate
  and the correct target/result.
- **Batting / Bowling / Fielding leaderboards** and the **Records** page count *both* innings,
  so a player's 2nd-innings runs, wickets and catches are all included.
- The **match PDF** prints both innings and the aggregate.

**One small note:** a bowler who bowls in *both* innings of the same match is currently counted
as **one** bowling innings in the leaderboard's "Inns"/economy-per-innings column (his total
runs and wickets are still fully correct). Everything else reflects both innings.
