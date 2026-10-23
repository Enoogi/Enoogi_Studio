# ENOOGI.STUDIO

An immersive online gallery for original watercolour &amp; ink pet portraits by Inwook Kim — originals and commissions, framed in oak and shipped worldwide.

The site is a single self-contained page: all CSS, JavaScript, the oak picture frame, and the paintings are inlined into `index.html`, so it runs anywhere with no build step and no server.

## Files

| File | Purpose |
|------|---------|
| `index.html` | The entire website (styles, scripts, frame, and artwork are all inlined). |
| `favicon.svg` | Browser-tab icon (framed-portrait mark). |
| `og-image.png` | Social-sharing preview image (used by the Open Graph / Twitter tags). |
| `vercel.json` | Minimal Vercel config (clean URLs). |
| `.gitignore` | Keeps OS/editor junk out of the repo. |

That's everything the live site needs. No `images/` folder is required — the paintings are embedded in the page.

## Publish it (GitHub → Vercel)

1. Create a new repository on GitHub and upload every file in this folder (drag them into **Add file → Upload files**).
2. Go to [vercel.com](https://vercel.com), sign in with GitHub, and click **Add New → Project**.
3. Import this repo. Leave **Framework Preset** as **Other** and set **no build command** — Vercel serves `index.html` automatically.
4. Click **Deploy**. You'll get a live `*.vercel.app` URL in under a minute.
5. Any future change you push to the repo redeploys automatically.

### Custom domain
In the Vercel project: **Settings → Domains → Add** `enoogi.studio`, then set the DNS records Vercel shows you at your registrar. HTTPS is automatic and free.

After the domain is live, update the social-share URL in `index.html` (search for `og:url`) to your real domain so link previews resolve correctly.

## Editing the site

- **Paintings, titles, prices, years, descriptions:** open `index.html` and edit the `works` array near the bottom (inside the `<script>`). Artwork is stored in the `ART` object as data URIs.
- **Text & copy:** all page copy lives directly in the HTML markup.
- **Brand colours & fonts:** see the CSS custom properties in the `:root` block at the top of the `<style>`.

## Note on forms

The **Commission wizard** and **Store Admin** sign-in are front-end only. The commission form validates input and shows a confirmation, but it does not yet email or store submissions, and the admin screen is a demo with no real authentication. To make these functional, connect the commission form to a service like [Formspree](https://formspree.io) (or a small backend) and add real auth for the admin area.
