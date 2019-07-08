# Displaying

Once you're finished syncing, WP Shopify comes with three different methods for displaying your products and collections. You can either use the [default pages](#default-pages), [shortcodes](#shortcodes), or [programmatically](#programmatically).

## Default pages

We provide two default pages that show your products out-of-the box. These pages are:

-  `/products`
-  `/collections`

You can change the slug of these URLs from within the plugin Settings.

![WP Shopify change default page URLs](http://localhost:4000/assets/change-default-pages.png)

If you prefer to disable these pages all together, you can turn them off from within the settings as well.

![WP Shopify disable default pages](http://localhost:4000/assets/displaying-disabled-pages.png)

## Shortcodes

The WP Shopify shortcodes allow you to customize your products and collections in ways that the defaults pages cannot.

For example, each shortcode has a wide array of attributes that you can use to tweak various settings. Everything from filtering products by title or tags, to enabling infinite scrolling and image zooming.

**Below is the full list of provided shortcodes:**

-  [[wps_products]](shortcodes/wps_products)
-  [[wps_products_title]](shortcodes/wps_products_title.md)
-  [[wps_products_description]](shortcodes/wps_products_description.md)
-  [[wps_products_pricing]](shortcodes/wps_products_pricing.md)
-  [[wps_products_buy_button]](shortcodes/wps_products_buy_button.md)
-  [[wps_products_gallery]](shortcodes/wps_products_gallery.md)
-  [[wps_collections]](shortcodes/wps_collections.md)
-  [[wps_cart_icon]](shortcodes/wps_cart_icon.md)
-  [[wps_search]](shortcodes/wps_search.md)
-  [[wps_storefront]](shortcodes/wps_storefront.md)

## Programmatically

WP Shopify comes with a [Render API](render-api/products) that allows you to display products using PHP.