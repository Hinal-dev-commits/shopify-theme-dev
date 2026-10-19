# Beanie – HTML/CSS design (static)

Pure HTML + CSS version of the Beanie coffee shop homepage. No Liquid, no JavaScript.
It is structured so each part can later be moved into a Shopify theme.

## Folder structure

```
beanie-html/
├── index.html
└── assets/
    ├── css/
    │   ├── base.css                         variables, reset, typography, helpers
    │   ├── components.css                   buttons, product card, list item, article card
    │   ├── section-header.css
    │   ├── section-hero.css
    │   ├── section-quote.css
    │   ├── section-featured-collection.css
    │   ├── section-testimonials.css
    │   ├── section-category-mosaic.css
    │   ├── section-product-lists.css
    │   ├── section-newsletter.css
    │   ├── section-service-features.css
    │   ├── section-featured-blog.css
    │   ├── section-instagram.css
    │   └── section-footer.css
    ├── images/      placeholder SVGs, logo.svg, leaf.svg (replace with real photos)
    ├── icons/       social + feature icons
    └── fonts/       (empty, for self-hosted fonts if you want them later)
```

## How it maps to Shopify later

| HTML block in index.html | Becomes in Shopify |
|---|---|
| `<header>` | `sections/header.liquid` |
| `.hero` | `sections/hero-banner.liquid` |
| `.quote` | `sections/rich-text-quote.liquid` |
| `.featured` | `sections/featured-collection-slider.liquid` |
| `.testimonials` | `sections/testimonials.liquid` |
| `.mosaic` | `sections/collection-grid-mosaic.liquid` |
| `.lists` (x2 blocks) | `sections/collection-list-products.liquid` (reused twice) |
| `.newsletter` | `sections/newsletter.liquid` |
| `.features` | `sections/service-features.liquid` |
| `.blogs` | `sections/featured-blog.liquid` |
| `.instagram` | `sections/instagram-feed.liquid` |
| `<footer>` | `sections/footer.liquid` |
| `.product-card` | `snippets/product-card.liquid` |
| `.list-item` | `snippets/product-list-item.liquid` |
| `.article-card` | `snippets/article-card.liquid` |

## Notes

- Design tokens (colors, fonts, spacing) are CSS variables at the top of `base.css`.
- Sliders are native scroll-snap rows, so the arrow buttons are visual only until JS is added.
- The mobile menu is CSS-only (checkbox toggle).
- Fonts (Marcellus, Jost, Cormorant Garamond) load from Google Fonts in `index.html`.
- Replace the SVG placeholders in `assets/images/` with real photos (keep the same file names or update the `src`).
