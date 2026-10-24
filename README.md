# Enoogi.Studio

Watercolour pet portraits — originals, prints and commissions.

## Pages
- `index.html` — Home (scroll-pinned Selected works)
- `gallery.html` — Gallery walkthrough, acquire + commission flow
- `about.html` — About the artist

## Responsive
Mobile <640 · sm 640–767 · tablet 768–1023 · desktop 1024–1279 · xl 1280–1535 · 2xl ≥1536. Breakpoint rules live in each page's `<style>` block (look for `data-r`).

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
- Payments: PayPal checkout (PayPal, Venmo, cards) via the PayPal JS SDK, plus a Zelle QR code. Orders are confirmed manually in the admin tool.
- Commission requests are emailed to enoogi.studio@gmail.com via FormSubmit (formsubmit.co), photos attached. The first submission triggers a one-time activation email.
- The admin tool is intentionally not included.
