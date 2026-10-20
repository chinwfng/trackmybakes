# Sourdough Tracker

A single-page app for logging sourdough bakes and spotting which fermentation
conditions give the best results.

## How to open it

Just double-click `index.html` (or open it from your browser with
`File > Open`). No install, no server, no build step. It needs an internet
connection on first load to fetch the charting library (Chart.js) from a CDN;
after that, the page itself works offline — only the chart would be missing
without a connection.

## How to use it

1. **Add a bake** — fill in the form at the top (date, temperature, water,
   fermentation hours, outcome, optional notes) and tap **Add bake**.
   Temperature, water and hours must be positive numbers; an outcome must be
   selected.
2. **Browse entries** — the table below the summary lists every bake, newest
   first, with a colour-coded outcome badge (green = good, grey = neutral,
   red = bad).
3. **Edit** — tap **Edit** on a row to load it back into the form, make
   changes, and tap **Save changes**. Tap **Cancel** to back out without
   saving.
4. **Delete** — tap **Delete** on a row; you'll be asked to confirm before
   it's removed.
5. **Filter & sort** — use the dropdowns above the table to filter by
   outcome, or sort by date, temperature, water or hours (ascending or
   descending). You can also tap a column header to sort by it.
6. **Summary & chart** — the Summary card shows total bakes, counts per
   outcome, average temperature/water/hours per outcome, and a scatter chart
   of fermentation hours vs temperature, coloured by outcome.
7. **Export** — tap **Export CSV** to download all entries as a `.csv` file
   you can open in a spreadsheet.
8. **Sample data** — on first load, 3 sample entries are included so you can
   see how everything looks. Tap **Clear sample entries** to remove them
   once you're ready to start logging your own bakes (the button disappears
   after you use it).

## Data storage

All entries are saved to your browser's `localStorage`, scoped to this file.
There's no backend, account or login — your data stays on your device and
survives page refreshes and browser restarts, but won't sync across devices
or browsers. Clearing your browser's site data for this page will erase it.

## Notes

- Everything lives in one file, `index.html` (HTML, CSS and JavaScript
  together), so it's easy to copy or back up.
- The layout is responsive with large tap targets, designed to be usable on
  a phone in the kitchen.
