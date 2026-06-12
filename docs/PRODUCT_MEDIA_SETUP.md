# Product Media Setup

The product card depends on Shopify product variants and product media.

## Required Product Fields

Use these values or similar values:

```txt
Vendor: Good Brand Company
Title: Plain T-shirt
Price: 20.00
Compare-at price: 29.50
Option name: Color
```

## Variant Colors

Create one Color option with these values:

```txt
Orange
Green
Blue
Yellow
Pink
Navy
```

## Front Images

Assign each front shirt image directly to its matching Shopify variant.

Example:

| Variant | Variant image |
|---|---|
| Orange | Orange front shirt |
| Green | Green front shirt |
| Blue | Blue front shirt |
| Yellow | Yellow front shirt |
| Pink | Pink front shirt |
| Navy | Navy front shirt |

## Hover / Secondary Images

Upload the side image for each color into the product media gallery.

Set the image alt text exactly like this:

| Variant | Secondary image alt text |
|---|---|
| Orange | `orange side` |
| Green | `green side` |
| Blue | `blue side` |
| Yellow | `yellow side` |
| Pink | `pink side` |
| Navy | `navy side` |

The section also supports `hover` instead of `side`.

Example:

```txt
green hover
```

## Sale Badge

To display the sale badge and markdown price:

```txt
Price: 20.00
Compare-at price: 29.50
```

The badge appears only when compare-at price is higher than the current price.
