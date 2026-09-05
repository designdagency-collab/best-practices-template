# #airconlife

Landing page for #airconlife, a marketplace where aircon contractors sell the jobs they've quoted but can't fit in, and licensed installers buy them.

The design is GTA VI / Vice City inspired. The hero is composed like an open-world game screenshot: a full-bleed scene with a live HUD layered over it (installer level bar, notification stack, map pin callout, key prompts, minimap, locked regions and an in-game phone), plus a skewed gradient display logo, a sold-jobs ticker, "mission" style job cards with wanted-star urgency, and a "Mission Passed" call to action.

## Hero image

The hero shows `assets/hero.jpg` (with `assets/hero-1280.jpg` for smaller screens) behind the HUD: the supplied #airconlife render, lightly graded with CSS. If the files are missing the page falls back to a canvas-drawn sunset, skyline, road and palms. See `assets/README.md` for how to swap the image.

## Run it

It is a single static file with no build step. Open `index.html` in a browser, or serve the folder:

```sh
python3 -m http.server 8000
```

Then visit http://localhost:8000.

## Stack

- Plain HTML, CSS and vanilla JS in `index.html`
- Google Fonts: Anton (display), Barlow (body), Share Tech Mono (HUD numbers)
- Dark neon theme by default; a moon/sun toggle in the nav switches to a light daytime theme (stored per browser). The hero and ticker stay dark in both themes because they are the "game screen".
- Logo: `assets/logo.png` (the supplied wordmark) with `assets/logo.svg` as a vector fallback; `assets/mark.png` is the hash mark used as the favicon
- Palms are drawn on a `<canvas>` at load and on resize
- The job map is a canvas-drawn, stylised Gold Coast (coast, Broadwater, Nerang River, canals, M1, Gold Coast Highway, suburbs) with pan, zoom, hover, click-to-waypoint, a route from the player marker, type filters and a job brief rail. Job data lives in the `JOBS` array in the second script block.
- The ticker loop and hero canvas are the only other scripted behaviour

## Content notes

Job listings, map positions, totals and the ticker are example data for the Gold Coast. The map geography is stylised, not to scale. Prices, models and fees are illustrative and should be replaced by live marketplace data.
