# Gold Hayat Cricket Team — Stats Hub

A self-contained cricket stats website for the Gold Hayat Cricket Team.
Only our own batting, bowling, fielding and captaincy records are tracked.

## Files
- `index.html` — the whole app
- `data.json` — your permanent records (team squad + every match)

## Squad (add / remove players)
Open the **Squad** tab to manage your team roster:
- Add a player (name + Regular/Substitute), or remove one with the Remove button.
- Add a **substitute** any time — or just type a one-off sub's name directly on the scorecard.
- Removing a name only removes it from suggestions; past match stats are never deleted.

Your 13 players are already loaded. Formats available: **T20, OD, Test Match, T10**.

## Publish a free public link (GitHub Pages)
1. Free GitHub account → new **public** repo, e.g. `gold-hayat`.
2. Upload `index.html` and `data.json`.
3. Repo **Settings → Pages → Source: main branch → Save**.
4. Link appears, like `https://yourname.github.io/gold-hayat/`.

## Add matches each Sunday (data stays safe)
1. **Add match** → fill batting / bowling / fielding / captain → **Save** (new matches are appended, never overwritten).
2. **Data & publish → Download data.json** → replace it in your repo and commit.
3. Keep a **Dated backup** after each match day, just in case.

The app also saves a working copy in your browser, and an amber banner reminds you
whenever you have unsaved matches to publish.
