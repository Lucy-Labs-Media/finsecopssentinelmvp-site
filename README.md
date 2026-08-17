# FinSecOps Sentinel — public site

The marketing site served at GitHub Pages. **This repository is public. The
Sentinel codebase is not, and must stay that way** — nothing in this repo should
ever contain source, the calculation specification, the engineering log, or
customer data.

## Deploying

1. Create a **new public repository** (suggested name: `sentinel-site`).
2. Copy `index.html`, `.nojekyll` and this README into it, and push to `main`.
3. In the repo, go to **Settings → Pages**, set **Source** to *Deploy from a
   branch*, branch `main`, folder `/ (root)`, and save.
4. The site publishes at `https://<username>.github.io/sentinel-site/` within a
   minute or two.

## Custom domain (optional)

Add a file named `CNAME` containing your domain (e.g. `sentinel.example.com`),
then point a CNAME DNS record at `<username>.github.io`. Enable
**Enforce HTTPS** in Settings → Pages once the certificate provisions.

## The live environment link

The site links to the Cloudflare-gated application at
`https://finsecops-sentinel.jordan-d77.workers.dev/`. That deployment is
unchanged — this site is only a public wrapper around it.

Access control stays where it is: Cloudflare Access one-time PIN, allow-listed
per email address. The public page explains the gate rather than hiding it, so
an unauthorized visitor understands why they hit an auth wall instead of
assuming the site is broken.

**Keep the allow-list pruned.** When an evaluation ends, remove the address.
The page tells prospects access can be revoked at any time; that should be true.

## Before you publish

- [ ] Replace all three `REPLACE-WITH-YOUR-EMAIL` placeholders in `index.html`
- [ ] Confirm the 15% figure against current market gain-share rates
- [ ] Resolve the product-name question — "Sentinel" collides with Microsoft
      Sentinel, Thales Sentinel, Payloop's Sentinel module, and a registered
      mark in financial software. A public page raises exposure materially
      compared with a private repository.
- [ ] Have counsel review the footer disclaimer alongside the LICENSE and NDA

## Editing

Single self-contained file, no build step and no dependencies. Edit
`index.html`, commit, push — Pages redeploys automatically.
