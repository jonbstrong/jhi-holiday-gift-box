# Jackson Heights Insider Holiday Gift Box

Astro static landing page for GitHub Pages with Cloudflare DNS. Preorders are accepted through the existing Stripe Payment Link.

## Run locally

```sh
npm install
npm run dev
```

## Checkout and fulfillment

The `PUBLIC_STRIPE_PAYMENT_LINK` build variable can override the provided Stripe link. All purchase buttons use the same URL. The assortment is still being curated, and preorder customers will receive the final guaranteed contents and relevant product information before pickup. If the box cannot be put together, customers will receive a full refund.

## GitHub Pages

The `main` branch deploys to GitHub Pages through `.github/workflows/deploy.yml`. `public/CNAME` maps the site to `giftbox.jacksonheightsinsider.com`.

Cloudflare DNS should contain a DNS-only CNAME from `giftbox` to `jonbstrong.github.io`. GitHub Pages provisions HTTPS for the custom domain after DNS validation.
