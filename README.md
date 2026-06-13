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
| `assets/og-image.svg` → `.png` | 1200×630 social preview (SVG source + rendered PNG) |
| `assets/youtube-banner.svg` → `.png` | 2560×1440 channel banner (SVG source + rendered PNG) |
| `BRAND.md` | brand kit — name, color, type, logo, voice |
| `YOUTUBE.md` | channel setup + full content plan, scripts, storyboards, metadata |
| `VIDEO-PRODUCTION.md` | how to film/record/edit/export the demos |

## Re-rendering the brand images
The `.svg` files are the editable source; the `.png` files are generated from them. After
editing an SVG, re-render its PNG with headless Chrome (exact size, no extra tooling):
```bash
CHROME="/Applications/Google Chrome.app/Contents/MacOS/Google Chrome"
"$CHROME" --headless=new --hide-scrollbars --force-device-scale-factor=1 \
  --window-size=1200,630 --screenshot="assets/og-image.png" "file://$PWD/assets/og-image.svg"
"$CHROME" --headless=new --hide-scrollbars --force-device-scale-factor=1 \
  --window-size=2560,1440 --screenshot="assets/youtube-banner.png" "file://$PWD/assets/youtube-banner.svg"
```

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
- [x] `assets/og-image.png` — 1200×630 social preview image (done; edit `og-image.svg` then re-render to change)
- [x] `assets/youtube-banner.png` — 2560×1440 channel banner (done; for YouTube upload, not the site)
- [ ] Hero media — swap the placeholder for a robot photo / muted loop
- [ ] Demo section — replace the placeholder with the YouTube embed (`<iframe>` snippet is in `index.html`)
- [ ] Results — replace target numbers with measured results (mAP, posture accuracy, FPS)
- [ ] Footer YouTube link (`data-youtube-link`) — point to the channel

> MeSA is an assistive aid, not a medical device.
