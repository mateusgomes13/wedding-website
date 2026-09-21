# Sophie & Mateus — Wedding Website

Single-page wedding site (EN/PT), password-gated, with RSVP via Formspree.

## Publishing

This repo deploys to GitHub Pages automatically via `.github/workflows/deploy-pages.yml`
on every push. Once this branch is pushed, enable Pages once in
**Settings → Pages → Build and deployment → Source: GitHub Actions** (if not
already enabled) and the site will go live at:

```
https://mateusgomes13.github.io/wedding-website/
```

## Still needed

Three illustration images are referenced but not yet in the repo — drop them
in the repo root with these exact filenames and push:

- `img-cottage.png` — used for the Pre-Wedding event card & Day I schedule icon
- `img-venue.png` — used for the Ceremony & Reception event card & Day II schedule icon
- `img-pub.png` — used for the Day After event card & Day III schedule icon

Until they're added, those spots will show broken-image icons.

## Password

The site is gated by a client-side password (`brazilandnorthernireland`,
set in the `<script>` at the bottom of `index.html`). This is a soft gate
only — anyone who views the page source can read it — not real security.
