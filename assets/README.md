# Hero image

The hero uses `hero.jpg` (1448 px) and `hero-1280.jpg`, both exported from the supplied #airconlife render. To swap it, replace both files (same names, JPEG, roughly 4:3 or wider) and the page picks them up automatically. Without them, the page draws a stylised sunset, skyline, road and palms on canvas instead.

The HUD is designed for a shot like this. Suggested generation prompt:

> Photorealistic wide shot in the style of a modern open-world game screenshot, golden-hour sunset over the Gold Coast, Australia. An aircon installer in a black "#airconlife" t-shirt seen from behind, walking towards a white work van with roof racks and rooftop split-system condensers on a glass showroom behind. Q1 tower and city skyline on the horizon, palm trees, wet asphalt reflecting pink and orange sky, cinematic lighting, 16:9, no text, no logos.

Keep the subject centred-right so the left panel and phone do not cover the focal point.

# Logo

The page loads `assets/logo.png` (the supplied wordmark, trimmed of its transparent margins) and falls back to `assets/logo.svg`, a vector rebuild, if the PNG is missing. `assets/mark.png` is the hash mark cropped from the same file, used as the favicon.
