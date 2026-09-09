# GMC Athletics 2026-27

A one-page schedule of every Greer Middle College game, match and meet for the
2026-27 school year. Filter by season, sport, team, or home/away, and see the
next contest with a countdown.

## What's here

- **`index.html`** — the whole site. HTML, CSS, JavaScript and the schedule data
  are all in this one file, so it works opened straight off disk or served from
  anywhere. No build step, no dependencies.
- **`.nojekyll`** — tells GitHub Pages to serve the files as-is.

## Hosting on GitHub Pages

1. Create a new repository and push these two files to it.
2. In the repo, open **Settings -> Pages**.
3. Under **Build and deployment**, set **Source** to *Deploy from a branch*,
   pick the `main` branch and the `/ (root)` folder, and save.
4. Wait about a minute. The site appears at
   `https://<your-username>.github.io/<repo-name>/`.

## Styling

Every rule follows the Pit Crew Site Style Guide: the token palette, square
edges, Arial only, one accent colour at a time. Each season tab flips a single
CSS custom property (`--accent`) and the whole page recolours.

## Changing the schedule

The contest data is the `window.GMC_ATHLETICS` block near the bottom of
`index.html`. It is generated from `tools/schedule_data.py` in the source
project; edit it there and rebuild rather than hand-editing the copy in this
file.
