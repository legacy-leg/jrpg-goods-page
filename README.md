# Relic Front Static Site

Relic Front is a static website for a Tokyo-based collector goods sourcing service focused on JRPG, anime, and game goods from Japan.

## Files

- `index.html` - Homepage with collector-focused sourcing copy, request flow, source types, risk limits, and FAQ.
- `request.html` - Goods request page with a native Formspree-powered form and customer checklist.
- `styles.css` - Shared responsive styling.

## Local Preview

Open `index.html` directly in a browser, or serve the folder with any static server.

```sh
python3 -m http.server 8000
```

Then visit:

```text
http://localhost:8000
```

## Formspree setup

`request.html` intentionally has no backend, database, account system, shopping cart, checkout, or Stripe integration code.

The goods request form posts directly to the Formspree endpoint configured in `request.html`:

```html
<form action="https://formspree.io/f/xaqzlble" method="POST">
```

Before launch, replace `CONTACT_EMAIL_PLACEHOLDER` in `request.html` with the fallback contact email you want customers to use if the form does not work.

Test the form after deployment to confirm Formspree accepts submissions from the live site and sends notifications to the correct inbox.

Keep the request flow price-breakdown-first:

1. Customer submits a goods request.
2. Availability and pricing are checked manually in Japan.
3. A price breakdown is sent to the customer.
4. Payment is collected later through a Stripe invoice.
5. The approved item is purchased after payment is confirmed.
6. Photos are sent before international shipping when practical.
7. The tracking link is sent after dispatch when the selected shipping method supports tracking.

## Asset Notes

The current site uses original CSS-built cards and icons. It does not use copyrighted anime/game art, screenshots, character images, logos, official product photos, or shop/publisher branding.

If you add real images later, use your own photos or properly licensed original assets in `assets/images/`.
