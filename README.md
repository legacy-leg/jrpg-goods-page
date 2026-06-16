# RELIC FRONT

Relic Front is a static website for a Tokyo-based collector goods sourcing service focused on JRPG, anime, and game goods from Japan.

## Live Site

https://legacy-leg.github.io/jrpg-goods-page/

## Project Overview

Relic Front is a static HTML/CSS marketing site. It does not include a backend, database, customer accounts, cart, or checkout.

Customers submit a goods request through the request form. Availability and pricing are checked manually in Japan, then a price breakdown is sent before payment. Payment happens later by Stripe invoice. Purchase happens only after customer approval and confirmed payment.

## Files

- `index.html` — homepage
- `request.html` — goods request form page
- `styles.css` — shared responsive styling
- `README.md` — project documentation

## Local Preview

```bash
python3 -m http.server 8000
```

Then open:

```text
http://localhost:8000
```

## Deployment

This site is deployed with GitHub Pages from the `main` branch and repository root.

## Form Handling

The request form uses Formspree. It should not be described as a backend, and no private keys or secrets should be committed to this repository.

The Formspree endpoint is public by nature because it is used directly by the browser. Notification settings should be checked in Formspree to confirm requests are delivered to the correct inbox.

## Asset and IP Notes

The site does not use copyrighted anime/game art, screenshots, character images, logos, official product photos, or shop/publisher branding.

If real images are added later, use original photos or properly licensed assets.

## Status

Early public landing page / validation build.
