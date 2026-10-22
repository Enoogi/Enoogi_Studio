# Enoogi.Studio

Watercolour pet portraits — originals, prints and commissions.

## Pages
- `index.html` — Home (scroll-pinned Selected works)
- `gallery.html` — Gallery walkthrough, acquire + commission flow
- `about.html` — About the artist

## Run locally
Serve the folder with any static server (pages won't load from `file://`):

```
npx serve .
# or
python3 -m http.server
```

## Deploy to GitHub Pages
1. Push this folder's contents to the repo root.
2. Settings → Pages → Deploy from branch → `main` / root.

## Notes
- `support.js` is the page runtime; it loads React from unpkg.com.
- Artwork lives in `art/` (web-sized PNGs).
- Checkout and commission submissions are front-end only — connect a payment/form service before going live.
- The admin tool is intentionally not included.
