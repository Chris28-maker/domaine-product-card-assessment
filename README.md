# Domaine Product Card Technical Assessment

A Shopify product card built from scratch for the Domaine technical assessment.

The component is implemented as a custom Shopify section using:

- Shopify Liquid
- TailwindCSS utility classes
- Vanilla JavaScript
- Shopify product variants and product media

## Assessment Coverage

| Requirement | Status | Implementation |
|---|---:|---|
| Build within a headed Shopify environment | Done | Built for a normal Shopify Online Store theme |
| Product card built from scratch | Done | Custom `sections/domaine-product-card.liquid` section |
| Use TailwindCSS | Done | TailwindCSS utilities via `snippets/domaine-tailwind-cdn.liquid` |
| Sale badge and markdown pricing | Done | Uses `compare_at_price > price` |
| Variant swatches | Done | Color swatches are generated from the product's Color option |
| Alternate color imagery | Done | Clicking a swatch changes the active variant image |
| Secondary image on hover | Done | Uses product media alt text such as `green side` or `green hover` |
| Product title, brand, and price | Done | Shows product vendor, product title, sale price, and compare-at price |
| GitHub repo | Pending user upload | Push this repository to GitHub |
| Working prototype | Pending Shopify setup | Add the section to a Shopify page and copy the preview/live link |

## Folder Structure

```txt
.
├── sections/
│   └── domaine-product-card.liquid
├── snippets/
│   └── domaine-tailwind-cdn.liquid
├── templates/
│   └── page.domaine-product-card.json
├── docs/
│   ├── PRODUCT_MEDIA_SETUP.md
│   ├── SHOPIFY_ADMIN_SETUP.md
│   └── QA_CHECKLIST.md
├── product-media-samples/
├── SUBMISSION.md
├── README.md
└── .gitignore
```

## Shopify Admin Installation

This project is designed to be installed through Shopify Admin without Shopify CLI.

### 1. Duplicate your theme

Go to:

```txt
Shopify Admin → Online Store → Themes → ... → Duplicate
```

Work only on the duplicated theme.

### 2. Add TailwindCSS

Go to:

```txt
Online Store → Themes → Edit code
```

Create this snippet if it does not exist:

```txt
snippets/domaine-tailwind-cdn.liquid
```

Paste the contents from this repo's `snippets/domaine-tailwind-cdn.liquid`.

Then open:

```txt
layout/theme.liquid
```

Paste this before `</head>`:

```liquid
{% render 'domaine-tailwind-cdn' %}
```

Do not add it twice.

### 3. Add the section

Create this file in Shopify:

```txt
sections/domaine-product-card.liquid
```

Paste the contents from this repo's `sections/domaine-product-card.liquid`.

### 4. Add the card to a page

Go to:

```txt
Online Store → Themes → Customize
```

Then:

```txt
Add section → Domaine Product Card → Select product → Save
```

You can also create a page template using:

```txt
templates/page.domaine-product-card.json
```

## Product Setup

Create a product with a Color option.

Example product data:

```txt
Vendor / Brand: Good Brand Company
Product title: Plain T-shirt
Price: $20.00
Compare-at price: $29.50
Color values: Orange, Green, Blue, Yellow, Pink, Navy
```

Assign each color variant its front shirt image.

Then upload the side/secondary image for each color to the product media gallery.

Set the alt text of secondary images like this:

```txt
orange side
green side
blue side
yellow side
pink side
navy side
```

The alt text must include the variant color name and either `side` or `hover`.

## How the Hover Image Works

The component searches the product media gallery for an image whose alt text includes:

```txt
{color name} side
```

or:

```txt
{color name} hover
```

Example:

If the active variant is `Green`, the component will look for product media with alt text:

```txt
green side
```

If found, that image becomes the hover image.

## Notes About TailwindCSS

This repository uses the TailwindCSS CDN approach because the prototype is built through Shopify Admin without Shopify CLI.

For a production implementation, Tailwind should be compiled into a static CSS asset and committed to the theme.

## Submission

Submit:

1. GitHub repository link
2. Shopify prototype link

Use `SUBMISSION.md` as your final checklist.
# domaine-product-card-assessment
