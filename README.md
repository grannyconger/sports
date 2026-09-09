# GMC Athletics 2026-27

A one-page schedule of every Greer Middle College game, match and meet for the
2026-27 school year. Pick a season to filter and recolour the page, filter by
sport or home/away, search, and see the next contest with a countdown.

Live: https://www.coachw.club/sports/

## What's here

- **`index.html`** — the whole site. HTML, CSS, JavaScript and the 160 contests
  are all inlined in this one file, so it works opened straight off disk or
  served from anywhere. No build step, no dependencies.
- **`.nojekyll`** — tells GitHub Pages to serve the files as-is.
- **`README.md`** — this file.

## How the schedule reads

- **Season tabs** (All / Fall / Winter / Spring) flip a single CSS custom
  property, `--accent`, so the whole page recolours to match the season.
- **Sports are listed by name only.** There are no `Varsity`, `JV`, or
  `JV & Varsity` labels; each sport appears once. The team level is still part of
  the search text, so typing "JV" in the search box still works.
- **The Sport dropdown reorders by season.** Whatever season tab is active (or,
  on "All seasons", whichever season today falls in) floats its sports to the top.
- **Past events are hidden by default.** The "Show past events" chip brings back
  everything that has already happened.
- **"Last updated"** in the header is read from the data's own build date, so it
  is always correct after a rebuild.

## Styling

Every rule follows the Pit Crew Site Style Guide (`GMCAthleticsStyleGuide.md` in
the source project): the token palette, square edges, Arial only, one accent
colour on screen at a time.

## Editing

Do **not** hand-edit `index.html` — it is generated. In the source project
(`Desktop/Sports/`):

1. Edit `site_template.html` for markup, style or behaviour, **or** edit
   `tools/schedule_data.py` for the contest data.
2. If the data changed, run `python tools/build.py --xlsx` first.
3. Run `python3 build_single.py`. This rewrites `gmc-athletics-site/index.html`
   with the current data inlined.
4. Commit and push from inside `gmc-athletics-site/`.

## Hosting on GitHub Pages

Pages is set to **Deploy from a branch**, `main` / `/ (root)`. After a push the
site refreshes in about a minute. The GitHub account has a repo-wide custom
domain, so the address is `https://www.coachw.club/sports/`; the plain
`github.io` URL redirects there.
