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

## Deploy

Any static host works (GitHub Pages, Netlify, Cloudflare Pages, S3, etc.). Upload the three files at the site root — no build step.
