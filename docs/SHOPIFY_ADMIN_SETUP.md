# Shopify Admin Setup Guide

Use this guide if you are installing the component manually through Shopify Admin.

## 1. Open the theme code editor

```txt
Shopify Admin → Online Store → Themes → ... → Edit code
```

## 2. Add the Tailwind snippet

Create:

```txt
snippets/domaine-tailwind-cdn.liquid
```

Paste the code from this repo.

Then open:

```txt
layout/theme.liquid
```

Paste this before `</head>`:

```liquid
{% render 'domaine-tailwind-cdn' %}
```

## 3. Add the custom product card section

Create:

```txt
sections/domaine-product-card.liquid
```

Paste the section code from this repo.

## 4. Add the section in the visual editor

Go to:

```txt
Online Store → Themes → Customize
```

Then:

```txt
Add section → Domaine Product Card
```

Select the product and save.

## 5. Get the prototype link

In the theme customizer, use Preview or publish the duplicate theme if allowed.

Copy the preview/live URL for your submission.
