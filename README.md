# Dendrite Studio — promotional site

Clean, self-contained static landing page for **Dendrite Studio**.

## Run locally

Open `index.html` in a browser, or serve the folder:

```bash
# Python
python -m http.server 8080

# Node
npx serve .
```

Then visit `http://localhost:8080`.

## Contents

| File | Purpose |
|------|---------|
| `index.html` | Single-page promo: hero + download, features, install guide |
| `styles.css` | Layout and theme |
| `script.js` | Mobile nav + light polish |

## Download button

The **Download for Windows** CTA currently scrolls to the install section. When a real `Setup.exe` URL is available, set `DOWNLOAD_URL` in `script.js` (and optionally point the hero button `href` straight at that file).

## Live site

- **Repo:** https://github.com/mfillalan/dendrite-studio-site
- **GitHub Pages:** https://mfillalan.github.io/dendrite-studio-site/

Publishing source is the `main` branch root (with `.nojekyll` so Pages serves plain HTML).

## Deploy

Any static host works (GitHub Pages, Netlify, Cloudflare Pages, S3, etc.). No build step.

### Installer distribution (Setup.exe)

Do **not** commit the binary into this repo. Use **GitHub Releases** on this repo (or on the app repo):

```bash
# after you have a built Setup.exe
gh release create v0.1.0 ./path/to/DendriteStudio-Setup.exe \
  --title "Dendrite Studio 0.1.0" \
  --notes "Early Windows build. SmartScreen may warn (unsigned)."
```

Then set `DOWNLOAD_URL` in `script.js` to the release asset URL, e.g.:

`https://github.com/mfillalan/dendrite-studio-site/releases/download/v0.1.0/DendriteStudio-Setup.exe`

Limits (GitHub docs): each release asset &lt; 2 GiB; no stated bandwidth cap on release downloads.
