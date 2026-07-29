# Dietary Ingredient Scanner — User Manual (deploy-ready site)

This folder is the complete website. Upload **the contents of this folder** (not the folder
itself) to any static host. Everything is self-contained — no build step, no server, no database.

```
index.html            the manual (renamed from website-wireframe-fun.html)
assets/               app icon, favicon, apple-touch-icon
screenshots/          32 screenshots, resized to 720px wide and optimised (23.6 MB → 5.9 MB)
media/                infographic, 14 primer slides, 2 audio explainers, the primer PDF
.nojekyll             tells GitHub Pages to serve files as-is
```

Total about 28 MB — comfortably inside every free tier below.

---

## Option A — Cloudflare Pages (no Git needed, unlimited bandwidth)

1. Sign in at <https://dash.cloudflare.com> → **Workers & Pages** → **Create** → **Pages** →
   **Upload assets**.
2. Give the project a name (this becomes `your-name.pages.dev`).
3. Drag this entire folder onto the upload area.
4. **Deploy site.** Live in under a minute.

To update later, upload the folder again as a new deployment.

## Option B — Netlify (simplest drag-and-drop)

1. Sign in at <https://app.netlify.com>.
2. Drag this folder onto the "deploy manually" drop zone on the Sites page.
3. Live immediately at a random `*.netlify.app` name — rename it under **Site settings →
   Change site name**.

Free tier caps bandwidth at 100 GB/month, which is far more than this site will use.

## Option C — GitHub Pages (best if you want version history)

Requires a **public** repository on a free account.

1. Create a new public repo, e.g. `dietary-scanner-manual`.
2. Upload the contents of this folder to the repo root (drag-and-drop works on
   github.com → **Add file → Upload files**).
3. Repo **Settings → Pages** → Source: **Deploy from a branch** → Branch: `main`, folder: `/ (root)`
   → **Save**.
4. Live at `https://<username>.github.io/dietary-scanner-manual/` within a couple of minutes.

Limits: 1 GB site size, 100 GB/month bandwidth, 10 builds/hour.

---

## Custom domain

All three hosts support a custom domain free of charge — you only pay the registrar for the
domain itself. Add it in the host's dashboard, then point your DNS at the value it gives you.
HTTPS is issued automatically.

## Before you publish

The About section still contains placeholder contact details:

- Email `email@email.com`
- Website `www.dietaryingredientscanner.app`
- `@dietaryscanner` on X and Instagram
- `github.com/dietaryscanner`

Edit those in `index.html` (search for "email@email.com") and replace them with real ones.

## Notes

- Fonts (Baloo 2, Quicksand) load from Google Fonts, so the page needs a network connection to
  render exactly as designed. Offline it falls back to system fonts and stays fully readable.
- Screenshots are lazy-loaded, so only the ones on screen are downloaded.
- The source file this was built from is `../User Manual/website-wireframe-fun.html`. Re-run the
  copy step there if you edit the manual.
