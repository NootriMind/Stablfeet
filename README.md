# Stablfeet Landing Page

This repository contains a simple, responsive landing page for **Stablfeet®** high‑arch orthotics insoles.  It’s written in plain HTML and CSS so that it can be easily hosted on any static‑site platform such as Netlify.

The design mimics the layout from the provided reference screenshots, including sections for product benefits, size chart, foot‑pain relief information, and a call‑to‑action that links to your payment flow.

## File structure

```
stablfeet-landing/
├── index.html      # Main page markup
├── style.css       # Page styling
├── images/         # Place your uploaded images here (see below)
└── README.md       # This file
```

## Customising the content

1. **Logo and product photos** – Place your logo and any product images into the `images/` folder.  Then edit the `<img>` tags in `index.html` to point to the correct file names.  For example:

   ```html
   <img src="images/logo.png" alt="Stablfeet logo">
   <img src="images/product-hero.jpg" alt="Stablfeet insoles and packaging">
   ```

2. **Payment link** – The “Proceed to Checkout” button currently links to `#` (a placeholder).  To enable checkout with Stripe:

   - Create a [Stripe Payment Link](https://stripe.com/docs/payment-links) for your insoles product.  Payment Links handle checkout, including HSA/FSA eligibility, without requiring any backend code.
   - Replace the `href` attribute on the checkout button in `index.html` with your payment link, for example:

     ```html
     <a id="checkout-link" href="https://buy.stripe.com/YOUR_PAYMENT_LINK" class="btn primary-btn">Proceed to Checkout</a>
     ```

3. **Text and pricing** – Feel free to adjust headings, bullet points, and other copy in `index.html` to better match your branding and marketing message.

## Uploading images to GitHub

To add your logo and product photos:

1. From the repository page on GitHub, click **Add file → Upload files**.
2. Drag your image files into the upload area (for example `logo.png` or `product-hero.jpg`).
3. Once uploaded, ensure they live inside the `images/` directory (create this folder if it doesn’t exist).
4. Commit the changes using a descriptive message like “Add logo and product photos.”

After uploading, update the `<img>` tags in `index.html` so they reference the correct file names.

## Deploying on Netlify

1. **Delete any existing site** – In Netlify’s dashboard, locate the old Stablfeet site and remove it.  This ensures you’re starting fresh.
2. **Connect the new repository** – Click **Add new site → Import from Git** and choose this repository.  Grant Netlify access if prompted.
3. **Configure build settings** – Because this is a static site, you don’t need a build command.  Set the publish directory to the root of the repository (or leave it blank).
4. **Deploy** – Netlify will deploy your site automatically.  You can configure a custom domain in the Netlify settings afterward.

Once deployed, your payment link will take visitors to Stripe’s secure checkout where they can pay with credit cards—including HSA/FSA cards—without any additional code.

## License

This project is provided as‑is without warranty.  Feel free to adapt it to your needs.
