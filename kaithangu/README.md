# Kaithangu — Kerala Welfare Entitlement Assistant

A lightweight, responsive, bilingual (English/Malayalam) vanilla HTML/CSS/JS prototype.

## Fixed in this build

- Manual district selection never requests browser location permission.
- Selecting a district immediately updates the checker, map focus, district list, and saved district.
- A pending GPS request can no longer override a district the user selected manually.
- A stale GPS success/error callback cannot move the map or show an old "Access denied" toast after manual selection.
- "Use my location" remains an optional feature and is only triggered by the user.
- If browser location is denied, the app explicitly tells the user that manual district selection still works.
- Previous district selection is restored from localStorage.

## Run

Use a local static server for the most consistent browser behavior:

```bash
python -m http.server 8000
```

Then open:

http://localhost:8000

The map uses Leaflet and OpenStreetMap tiles, so internet access is required for map tiles.

## Files

- `index.html` — page structure
- `style.css` — design, responsive layout and animations
- `app.js` — language, eligibility logic, district data, map and interactions
- `assets/kaithangu-logo.jpg` — Kaithangu logo

## Important prototype note

The welfare guidance is a limited hackathon prototype and does not make a final government eligibility decision. Verify current scheme rules and application requirements against official sources before production use.
