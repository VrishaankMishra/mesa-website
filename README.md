# MeSA 2.0 — Website & Showcase

The public website and showcase assets for **MeSA 2.0**, the Medication & Safety Assistant
Robot. Product/source code lives in a separate repo:
[VrishaankMishra/mesa-ai-robot](https://github.com/VrishaankMishra/mesa-ai-robot).

A static, dependency-free site (one `index.html` + `styles.css`) — minimal-portfolio style,
black/white, typography-led.

## Contents
| File | What |
|------|------|
| `index.html` / `styles.css` | the landing page |
| `assets/logo.svg`, `assets/favicon.svg` | brand marks |
| `BRAND.md` | brand kit — name, color, type, logo, voice |
| `YOUTUBE.md` | channel setup + full content plan, scripts, storyboards, metadata |
| `VIDEO-PRODUCTION.md` | how to film/record/edit/export the demos |

## Run locally
No build step. Either open `index.html` directly, or:
```bash
python3 -m http.server 8000   # then visit http://localhost:8000
```

## Deploy (GitHub Pages — free)
1. Push this repo to GitHub.
2. Repo **Settings → Pages → Build and deployment → Source: Deploy from a branch**.
3. Branch: `main`, folder: `/ (root)`. Save.
4. Live at `https://vrishaankmishra.github.io/mesa-website/` in ~1 minute.
5. (Optional) add a custom domain under Settings → Pages → Custom domain.

## Before you publish — placeholders to replace
- [ ] `assets/og-image.png` — 1200×630 social preview image
- [ ] Hero media — swap the placeholder for a robot photo / muted loop
- [ ] Demo section — replace the placeholder with the YouTube embed (`<iframe>` snippet is in `index.html`)
- [ ] Results — replace target numbers with measured results (mAP, posture accuracy, FPS)
- [ ] Footer YouTube link (`data-youtube-link`) — point to the channel

> MeSA is an assistive aid, not a medical device.
