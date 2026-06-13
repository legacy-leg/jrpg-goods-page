# Japan Game Goods Sourcing Static Site

Simple static website for a request-based Japanese game, JRPG, and anime goods sourcing/export service.

## Files

- `index.html` - Main marketing and service information page.
- `request.html` - Basic request form layout with a clearly marked replacement area for Google Forms, Tally, or another provider.
- `styles.css` - Shared responsive styling.

## Local Preview

Open `index.html` directly in a browser, or serve the folder with any static server.

Example:

```sh
python3 -m http.server 8000
```

Then visit:

```text
http://localhost:8000
```

## Request Form Setup

The form in `request.html` is a static placeholder and does not submit anywhere yet. Before launch, replace the form area with one of the following:

- Google Forms embed
- Tally embed
- Formspree, Basin, or another form backend
- A custom server endpoint

Look for the `form-shell` section in `request.html`. The note at the top of that section marks the intended replacement area.

## Business Flow

1. Customer submits a sourcing request.
2. Availability is checked manually in Japan.
3. A quote is sent to the customer.
4. Payment is collected through a Stripe invoice.
5. The approved item is purchased in Japan.
6. The item is packed and shipped internationally.

## Deployment

Deployment instructions:

