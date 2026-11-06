# Rotate

Log every dose, rotate your injection sites, never miss an injection.

A small offline-first PWA for people who self-inject on a fixed weekly schedule (e.g. 3 times a week, at least 48 hours apart). Thai / English.

## Features

- **Today** — next due dose, 48-hour spacing warning, suggested site, adherence over the last 4 weeks
- **Sites** — front/back body map with 12 injection zones; colour shows ready / resting / recent reaction; configurable rest period (default 7 days)
- **History** — date, time, site, reaction and notes, grouped by week
- **Symptoms** — daily symptom diary (0–3 severity) and doctor-visit prep checklist
- **Report** — 8-week summary for your doctor, print/save as PDF, CSV export
- **Reminders** — one-tap "Add to Google Calendar" recurring event
- All data stays in the browser (`localStorage`); backup/restore as JSON

## Run locally

Any static server works:

```bash
npx serve .
# or
python3 -m http.server 8080
```

Open http://localhost:8080 — the service worker needs `localhost` or HTTPS.

## Deploy to GitHub Pages

1. Push this folder to a repository.
2. Settings › Pages › Source: **Deploy from a branch**, branch `main`, folder `/ (root)`.
3. Open the Pages URL on your phone and use *Add to Home Screen*.

The app is a single `index.html`; `manifest.json`, `sw.js` and `icons/` make it installable and usable offline. Fonts load from Google Fonts and are cached after first use.

## Files

```
index.html     the whole app (HTML + CSS + JS)
manifest.json  PWA manifest
sw.js          service worker (offline cache)
icons/         app icons (SVG source + PNG 180/192/512)
```

## Disclaimer

This app only keeps notes. It is not medical advice. Follow the instructions that came with your medication and your healthcare provider's guidance.

## License

MIT
