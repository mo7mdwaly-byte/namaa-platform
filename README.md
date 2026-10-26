# NAMAA Platform

Static site (single `index.html`) hosted on GitHub Pages.

## Deploy
1. Create a repository (e.g. `namaa-platform`) on GitHub.
2. Upload `index.html`, `404.html`, `.nojekyll`, `README.md`.
3. Settings → Pages → Source: *Deploy from a branch* → `main` / `/ (root)` → Save.
4. Site goes live at `https://<username>.github.io/namaa-platform/`.

## Note
Demo mode: carts, library, reviews and progress are stored in each visitor's browser (localStorage). No real payments. A live store needs a backend.

## Dashboard
Open `admin.html`, enter `owner/repo` and a fine-grained token limited to this one repository (Contents RW, Issues RW, Pages R, Metadata R). Products are saved to `products.json`, which the public site loads. Never commit a token.

## Editable content
`content.json` (all site text EN/AR, plan prices, image paths) and `products.json` (all products) are edited from the dashboard. Upload both once, then manage everything from `admin.html`.

## Payments
In the dashboard Products tab, paste each product's Egypt link (e.g. Paymob) and/or global link (e.g. Stripe Payment Link). The Buy button then opens the right checkout. Products with no links keep the demo cart. Update the footer note in Site content (`note`) when going live. The Royalties tab estimates author payouts from provider CSV exports.
