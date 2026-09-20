# NXT Cloud website

Static site for NXT Cloud (NXTPad, NXT DEX, NXT Finance). Plain HTML, CSS, and JavaScript, so there is no build step.

## Files

- `index.html` — homepage
- `whitepaper.html` — white paper
- `assets/css/style.css` — all styling (colors and fonts are variables at the top)
- `assets/js/main.js` — mobile menu and white paper contents highlighting
- `assets/img/` — your logo (optimized), favicons, and a social preview image
- `_headers` — Cloudflare Pages security and cache headers

## Push to GitHub

```bash
cd nxt-cloud
git init
git add .
git commit -m "Initial NXT Cloud site"
git branch -M main
git remote add origin https://github.com/YOUR-USERNAME/nxt-cloud.git
git push -u origin main
```

Create the empty `nxt-cloud` repository on GitHub first, then run the commands above.

## Deploy on Cloudflare Pages

1. In the Cloudflare dashboard, go to Workers and Pages, then Create, then Pages, then Connect to Git.
2. Pick the `nxt-cloud` repository.
3. Framework preset: None. Build command: leave empty. Build output directory: `/` (the repo root).
4. Save and deploy. Every push to `main` redeploys the site.
5. Add your custom domain under the project's Custom domains tab.

## Before you go live

- Review the white paper copy in `whitepaper.html`. It is a draft written from the product status you gave me and contains no chains, fees, token details, dates, or security claims beyond general principles. Add real details once they are final.
- Add your community links (X, Telegram, Discord) in the footer. There is a commented example in `index.html`.
- Once you have a domain, add an `og:image` tag pointing to `assets/img/og.png` (an absolute URL is needed) so links preview well when shared.
- Add a license file if you want one.
