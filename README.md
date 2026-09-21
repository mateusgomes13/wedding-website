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

## Custom domain

The site is configured (via the `CNAME` file) to serve at
**sophandmateus.website**, registered on GoDaddy. DNS records needed at
GoDaddy (DNS Management for the domain):

| Type  | Name | Value                     |
|-------|------|---------------------------|
| A     | @    | 185.199.108.153           |
| A     | @    | 185.199.109.153           |
| A     | @    | 185.199.110.153           |
| A     | @    | 185.199.111.153           |
| CNAME | www  | mateusgomes13.github.io   |

Remove GoDaddy's default parked `@` A record/forwarding first, or it will
conflict. After DNS propagates, check **Settings → Pages** on the repo —
GitHub will show a "DNS check successful" message and let you enable
**Enforce HTTPS**.

## Password

The site is gated by a client-side password (`brazilandnorthernireland`,
set in the `<script>` at the bottom of `index.html`). This is a soft gate
only — anyone who views the page source can read it — not real security.
