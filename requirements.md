Build a simple web app to track my sourdough fermentation and bake outcomes.

## Goal
I want to log each bake, then look back to see which fermentation conditions
tend to give good results.

## Data per entry
- Date (defaults to today, editable)
- Temperature: °C, number, one decimal allowed (e.g. 24.5)
- Water: grams, whole number (e.g. 350)
- Fermentation time: hours, number, one decimal allowed (e.g. 8.5)
- Outcome: one of "good", "neutral", "bad" (required, chosen with buttons
  or a dropdown, not free text)
- Notes: optional free text (crumb, flavour, what I'd change)

## Features
1. Entry form to add a new bake. Validate that temperature, water and hours
   are positive numbers and that an outcome is selected.
2. Table of all entries, newest first, with colour-coded outcome badges
   (green = good, grey = neutral, red = bad).
3. Edit and delete existing entries (confirm before deleting).
4. Summary section showing:
   - total bakes and the count of each outcome
   - average temperature (°C), water (g) and fermentation hours for each outcome
   - a chart of fermentation hours vs temperature, with points coloured
     by outcome
5. Filter the table by outcome, and sort by date, temperature, water or hours.
6. Export all entries to CSV.

## Technical requirements
- Single-page app using plain HTML, CSS and JavaScript (no build step),
  so I can open it directly in a browser.
- Persist data in localStorage. No backend or login.
- Responsive and usable on a phone, since I'll log entries in the kitchen.
- Clean, minimal design; large tap targets on the form.
- Include 3 sample entries on first load so I can see how it looks, with a
  button to clear them.

## Deliverable
A single index.html file, plus a short README explaining how to open and use it.
Before you finish, test adding, editing and deleting an entry and check that
data survives a page refresh.