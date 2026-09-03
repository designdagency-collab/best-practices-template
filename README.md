# The Aircon Man

Landing page for The Aircon Man, a marketplace where aircon contractors sell the jobs they've quoted but can't fit in, and licensed installers buy them.

The design is GTA VI / Vice City inspired: a striped sunset sun, canvas-drawn palm silhouettes, a skewed gradient display logo, HUD-style counters, a sold-jobs ticker, "mission" style job cards with wanted-star urgency, and a "Mission Passed" call to action.

## Run it

It is a single static file with no build step. Open `index.html` in a browser, or serve the folder:

```sh
python3 -m http.server 8000
```

Then visit http://localhost:8000.

## Stack

- Plain HTML, CSS and vanilla JS in `index.html`
- Google Fonts: Anton (display), Barlow (body), Share Tech Mono (HUD numbers)
- Palms are drawn on a `<canvas>` at load and on resize
- Job board filters and the ticker loop are the only scripted behaviour

## Content notes

Job listings, totals and the ticker are example data for the Gold Coast. Prices, models and fees are illustrative and should be replaced by live marketplace data.
