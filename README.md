# sf-chap Shopify Theme Starter

A Shopify Online Store 2.0 theme starter designed to match the look and feel direction of mattgagedigital.com:

- Warm neutral background + slate/gold brand accents
- Conversion-first hero and feature sections
- Service-forward presentation style
- App-ready sections so you can wire in your distro app stack quickly

## Theme structure

- `layout/theme.liquid` - global page shell
- `assets/theme.css` - brand styling and component CSS
- `sections/*.liquid` - reusable homepage, header/footer, and product/collection sections
- `templates/*.json` - OS 2.0 templates for index/product/collection/page
- `config/settings_schema.json` - customizable theme settings

## App wiring support

This starter includes `@app` blocks in:

- `sections/announcement-bar.liquid`
- `sections/hero.liquid`
- `sections/rich-content.liquid`
- `sections/main-product.liquid`
- `sections/footer.liquid`

That means Shopify apps (reviews, subscriptions, bundles, upsells, loyalty, analytics widgets) can be inserted directly in the theme editor without editing code.

## Next steps

1. Zip this repository and upload as a new theme in Shopify admin.
2. Configure menus (`main-menu`, `footer`) in Navigation.
3. Replace default copy and connect product collections.
4. Install apps and drop their blocks into the app-enabled sections.
