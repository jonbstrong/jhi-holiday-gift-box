# Jackson Heights Insider Holiday Gift Box

Astro static landing page for GitHub Pages with Cloudflare DNS. The published page is deliberately in prelaunch mode: requirements in the brief say the product assortment and refund policy must be finalized before checkout is enabled.

## Run locally

```sh
npm install
npm run dev
```

## Prepare checkout for launch

Set `PUBLIC_STRIPE_PAYMENT_LINK` to the approved Stripe Payment Link at build time. Keep `PRELAUNCH_MODE` true in `src/pages/index.astro` until the guaranteed product description, refund/cancellation policy, pickup process, and checkout configuration have been confirmed. Then change it to false and deploy a production build.

The provided Stripe Payment Link is included in the prelaunch configuration for review, but every purchase CTA is disabled while prelaunch mode is on. Inventory limits, multiple-box quantities, required customer fields, tax treatment, confirmation emails, and purchase tracking must be configured and verified in Stripe before launch.

## GitHub Pages

The `main` branch deploys to GitHub Pages through `.github/workflows/deploy.yml`. `public/CNAME` maps the site to `giftbox.jacksonheightsinsider.com`.

Cloudflare DNS should contain a DNS-only CNAME from `giftbox` to `jonbstrong.github.io`. GitHub Pages provisions HTTPS for the custom domain after DNS validation.
