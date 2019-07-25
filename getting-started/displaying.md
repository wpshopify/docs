# Displaying

Once you're finished syncing, WP Shopify comes with three different methods for displaying your products and collections. You can either use [default pages](#default-pages), [shortcodes](#shortcodes), or the [Render API](#programmatically).

<iframe width="860" height="515" src="https://www.youtube.com/embed/8-TbA0HHoBw" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

## Default pages

We provide two default pages that show your products out-of-the box. These pages are:

-  `/products`
-  `/collections`

You can change the slug of these URLs from within the plugin Settings.

![WP Shopify change default page URLs](https://docs.wpshop.io/assets/change-default-pages.png)

If you prefer to disable these pages all together, you can turn them off by setting the [disable default pages](getting-started/settings?id=disable-default-pages) setting.

![WP Shopify disable default pages](https://docs.wpshop.io/assets/displaying-disabled-pages.png)

## Shortcodes

The WP Shopify shortcodes allow you to customize products in ways that defaults pages cannot.

For example, each shortcode has a wide array of attributes which you can use to tweak various settings. Everything from filtering products by tags, to enabling infinite scrolling and image zooming for [Pro users](https://wpshop.io/purchase).

**Below is the full list of provided shortcodes:**

-  [[wps_products]](shortcodes/wps_products)
-  [[wps_products_title]](shortcodes/wps_products_title.md)
-  [[wps_products_description]](shortcodes/wps_products_description.md)
-  [[wps_products_pricing]](shortcodes/wps_products_pricing.md)
-  [[wps_products_buy_button]](shortcodes/wps_products_buy_button.md)
-  [[wps_products_gallery]](shortcodes/wps_products_gallery.md)
-  [[wps_collections]](shortcodes/wps_collections.md)
-  [[wps_cart_icon]](shortcodes/wps_cart_icon.md)
-  [[wps_search]](shortcodes/wps_search.md) (pro only)
-  [[wps_storefront]](shortcodes/wps_storefront.md) (pro only)

## Render API

WP Shopify comes with a [Render API](guides/render-api.md) that allows you to display products using PHP.
