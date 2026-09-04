# The Aircon Man

Landing page for The Aircon Man, a marketplace where aircon contractors sell the jobs they've quoted but can't fit in, and licensed installers buy them.

The design is GTA VI / Vice City inspired. The hero is composed like an open-world game screenshot: a full-bleed scene with a live HUD layered over it (installer level bar, notification stack, map pin callout, key prompts, minimap, locked regions and an in-game phone), plus a skewed gradient display logo, a sold-jobs ticker, "mission" style job cards with wanted-star urgency, and a "Mission Passed" call to action.

## Hero image

The hero shows `assets/hero.jpg` (with `assets/hero-1280.jpg` for smaller screens) behind the HUD, colour graded with CSS. The photo is "Gold Coast skyline at night" by marty.vdh, CC BY-SA 2.0, via Wikimedia Commons, and is credited in the footer. If the files are missing the page falls back to a canvas-drawn sunset, skyline, road and palms. See `assets/README.md` for how to swap the image.

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
- The job map is a canvas-drawn, stylised Gold Coast (coast, Broadwater, Nerang River, canals, M1, Gold Coast Highway, suburbs) with pan, zoom, hover, click-to-waypoint, a route from the player marker, type filters and a job brief rail. Job data lives in the `JOBS` array in the second script block.
- The ticker loop and hero canvas are the only other scripted behaviour

## Content notes

Job listings, map positions, totals and the ticker are example data for the Gold Coast. The map geography is stylised, not to scale. Prices, models and fees are illustrative and should be replaced by live marketplace data.
