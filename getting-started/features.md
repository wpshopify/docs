# WP Shopify Features

WP Shopify comes with many unique features. Below is a list of the most popular with a description of how they work. If you have questions please [email us](mailto:hello@wpshop.io)!

## Automatic syncing

The automatic syncing feature keeps your WordPress site "in sync" automatically with your Shopify store. For example, in Shopify if you change the title or price of a product, this change will automatically reflect itself on WordPress.

Starting in version `2.1`, caching was introduced to help speed up the plugin's page-load time. If you're not seeing your Shopify changes reflected on WordPress automatically, try clearing the plugin cache, reducing the cache time, or disabling the cache altogether.

This feature is in both plugin versions.

## Shortcodes

WP Shopify comes with various shortcodes. These shortcodes allow you to control how your products look, which products show, and many other properties. This gives you flexibility to customize products in ways that the plugin default pages do not.

For example, each shortcode has a wide variety of attributes which you can use to tweak different settings. Everything from filtering products by tags, custom sorting, hiding buttons or product descriptions, and even [infinite scrolling for Pro users](https://wpshop.io/purchase?utm_medium=docs&utm_source=features&utm_campaign=upgrade).

**Below is the full list of provided shortcodes:**

- [[wps_products]](shortcodes/wps_products)
- [[wps_products_title]](shortcodes/wps_products_title.md)
- [[wps_products_description]](shortcodes/wps_products_description.md)
- [[wps_products_pricing]](shortcodes/wps_products_pricing.md)
- [[wps_products_buy_button]](shortcodes/wps_products_buy_button.md)
- [[wps_products_gallery]](shortcodes/wps_products_gallery.md)
- [[wps_collections]](shortcodes/wps_collections.md)
- [[wps_cart_icon]](shortcodes/wps_cart_icon.md)
- [[wps_search]](shortcodes/wps_search.md) (pro only)
- [[wps_storefront]](shortcodes/wps_storefront.md) (pro only)

Shortcodes are in both plugin versions. The exceptions are [[wps_search]](shortcodes/wps_search.md) and [[wps_storefront]](shortcodes/wps_storefront.md) which are pro-only shortcodes.

## Built-in cart experience

WP Shopify comes with a built-in cart experience. The cart has a slide-out effect which you can see on [our demo page](http://demo.wpshop.io?utm_medium=docs&utm_source=features&utm_campaign=info). The cart does not have a dedicated page.

When the user is ready to pay and click "Checkout", they're taken to the default Shopify checkout page like normal.

Any Shopify third-party app which customizes the checkout page will work with WP Shopify.

This feature is in both plugin versions.

## No iframes

WP Shopify does not use iframes to display products and collections. Because we use raw HTML, you can use custom CSS to adjust the visual layout to your liking.

This feature is in both plugin versions.

## Product detail pages

WP Shopify will create product and collection detail pages for you. By default, these pages are disabled by the plugin. However you can turn them on by enabling "Sync posts" within the plugin settings followed by a manual resync of your Shopify store from the Tools tab.

You can see a live example on [our demo page](https://demo.wpshop.io/shop/products/test?utm_medium=docs&utm_source=features&utm_campaign=info).

This feature is in both plugin versions.

## Fixed cart icon

Like all eCommerce sites, WP Shopify allows you to place a "cart icon" anywhere on your site. You can also enable a "fixed" icon that locks to the side of the page. This fixed cart icon follows the user as they scroll.

You can see a live example on [our demo page](https://demo.wpshop.io?utm_medium=docs&utm_source=features&utm_campaign=info).

This feature is in both plugin versions.

## Image crop and sizing

WP Shopify comes with the ability to adjust the size and crop of both product and collection images. Within the plugin settings, you can set the image dimensions of the product featured images and thumbnails seperately.

In addition to dimensions, you can set the [crop](getting-started/settings?id=crop-position) location. For example, if you set crop to "center", the plugin will attempt to resize the image while keeping the image centered.

If you set the [scale](getting-started/settings?id=scale) property, you can choose to load a higher-resolution version of your image. Setting scale to `2` will load an image twice as large, setting to `3` will load an image three times as large. For example, a 200x200 image becomes 400x400 and 600x600 respectfully.

This feature is in both plugin versions.

## Link to Shopify

WP Shopify allows you to link your products and collections to the default Shopify detail pages. This is useful if you want to leverage both platforms instead of using the WP Shopify product single pages.

Also useful if you want to embed a couple products and link them back to Shopify.

This feature is in both plugin versions.

## Custom button colors

WP Shopify allows you to customize the colors of the add to cart button, variant dropdowns, and cart icons. You can set these colors individually within the plugin settings.

This feature is in both plugin versions.

## Plugin updates

WP Shopify releases plugin updates on a bi-weekly cadence.

This feature is in both plugin versions.

## Search shortcode <span class="attr-type attr-type-pro-only">(Pro only)</span>

WP Shopify Pro provides a [search shortcode](https://docs.wpshop.io/#/shortcodes/wps_search) that allows you to display a dedicated search form on any WordPress page.

You can configure the search form to search by Title, Tag, Vendor, Product Type, and Variants Title.

By default, the search will be "fuzzy", meaning partial words will still match a full word. You can configure the search to be "exact" instead.

You can see a live example on [our demo page](https://demo.wpshop.io/search-example?utm_medium=docs&utm_source=features&utm_campaign=info).

This is a [Pro-only feature](https://wpshop.io/purchase?utm_medium=docs&utm_source=features&utm_campaign=upgrade).

## Storefront shortcode <span class="attr-type attr-type-pro-only">(Pro only)</span>

WP Shopify Pro provides a [storefront shortcode](https://docs.wpshop.io/#/shortcodes/wps_storefront) that allows you to display a fully-featured "storefront" with filtering and sorting options.

You can configure the storefront to filter by Tags, Vendors, an Product Types. By default, the shortcode has three required attributes: `dropzone_payload`, `dropzone_options`, `dropzone_selections`.

You can see a live example on [our demo page](https://demo.wpshop.io/search-example?utm_medium=docs&utm_source=features&utm_campaign=info).

This is a [Pro-only feature](https://wpshop.io/purchase?utm_medium=docs&utm_source=features&utm_campaign=upgrade).

## Image zoom <span class="attr-type attr-type-pro-only">(Pro only)</span>

WP Shopify Pro allows you to turn on "image zooming" for product feature images. When enabled, this will zoom the image on hover and when the user taps on mobile.

We use the Drift library from Imgix. You can see a [live demo here](https://imgix.github.io/drift).

This is a [Pro-only feature](https://wpshop.io/purchase?utm_medium=docs&utm_source=features&utm_campaign=upgrade).

## Infinite scrolling <span class="attr-type attr-type-pro-only">(Pro only)</span>

WP Shopify Pro provides infinite scrolling as an alternative form of pagination. When turned on, the plugin will automatically load the "next page" of products and append them to the bottom.

Any existing pagination settings that you have configured will be taken into consideration. For example, customizing the default page size from 10 to 20 will load 20 instead of 10.

This is a [Pro-only feature](https://wpshop.io/purchase?utm_medium=docs&utm_source=features&utm_campaign=upgrade).

## Selective syncing <span class="attr-type attr-type-pro-only">(Pro only)</span>

The selective syncing feature allows you to choose what "type" of data gets synced as native WordPress posts.

This is a [Pro-only feature](https://wpshop.io/purchase?utm_medium=docs&utm_source=features&utm_campaign=upgrade).

## Sync by collection <span class="attr-type attr-type-pro-only">(Pro only)</span>

Instead of syncing _all products_, WP Shopify Pro allows you to sync by one or more collections instead. This is useful if you have many products and only want to pull over a certain segment.

This is a [Pro-only feature](https://wpshop.io/purchase?utm_medium=docs&utm_source=features&utm_campaign=upgrade).

## Cart notes <span class="attr-type attr-type-pro-only">(Pro only)</span>

WP Shopify Pro allows you to add a "notes" section to the slide-out cart. The customer can add their own order notes before they checkout.

You can see a [live demo here](https://demo.wpshop.io?utm_medium=docs&utm_source=features&utm_campaign=info).

This is a [Pro-only feature](https://wpshop.io/purchase?utm_medium=docs&utm_source=features&utm_campaign=upgrade).

## Cart terms <span class="attr-type attr-type-pro-only">(Pro only)</span>

WP Shopify Pro allows you to add a "terms and conditions" checkbox to the cart. This will prevent the user from checking out until they agree to the terms. You can add custom HTML to the label text which allows you to provide a custon link to your own unique terms and conditions page.

You can see a [live demo here](https://demo.wpshop.io?utm_medium=docs&utm_source=features&utm_campaign=info).

This is a [Pro-only feature](https://wpshop.io/purchase?utm_medium=docs&utm_source=features&utm_campaign=upgrade).

## Cart attributes <span class="attr-type attr-type-pro-only">(Pro only)</span>

WP Shopify Pro enables you to provide "custom data" to orders. We use the native Shopify "cart attributes" to achieve this [which you can learn more about here](https://help.shopify.com/en/themes/customization/cart/get-more-information-with-cart-attributes).

At the moment, adding the custom data requires writing custom JavaScript to your WordPress theme. For more information on this, read through our [JavaScript hooks guide](/guides/javascript-hooks).

This is a [Pro-only feature](https://wpshop.io/purchase?utm_medium=docs&utm_source=features&utm_campaign=upgrade).

## PHP templates <span class="attr-type attr-type-pro-only">(Pro only)</span>

WP Shopify Pro allows you to customize four PHP templates that the plugin uses. The four templates correspond to the "product all", "product single", "collection all", and "collection single" pages.

Customizing these templates works similar to many other plugins. First, you need to create a folder in your theme called `wps-templates`. Then, you can copy the template files from the plugin foldder into the `wps-templates` folder.

You can find the plugin template files at this location: `plugins/wp-shopify-pro/public/templates`. Currently only `products-all.php`, `products-single.php`, `collections-all.php`, and `collections-single.php` work.

Any customizations you make to the files in `wps-templates` will not revert during plugin or theme updates and is the recommended way of customizing the plugin.

This is a [Pro-only feature](https://wpshop.io/purchase?utm_medium=docs&utm_source=features&utm_campaign=upgrade).

## Dedicated support <span class="attr-type attr-type-pro-only">(Pro only)</span>

When you purchase WP Shopify Pro you gain access to dedicated live support via our private Slack channel. In addition to chatting in real-time, your questions will take priority over thousands of other users on the free version.

We can also help with minor coding and theme customizations.

This is a [Pro-only feature](https://wpshop.io/purchase?utm_medium=docs&utm_source=features&utm_campaign=upgrade).

## Cross-domain tracking <span class="attr-type attr-type-pro-only">(Pro only)</span>

WP Shopify Pro provides cross-domain tracking via Google Analytics. WP Shopify integrates with the GA Linker plugin and takes care of storing the tracking cookie during checkout redirect.

You will still need to add the corrosponding google analytics code to both Shopify and WordPress.

This is a [Pro-only feature](https://wpshop.io/purchase?utm_medium=docs&utm_source=features&utm_campaign=upgrade).

## Direct checkout <span class="attr-type attr-type-pro-only">(Pro only)</span>

Direct Checkout allows you to replace the "add to cart" buttons with a link that takes the user directly to the checkout page. This is great if you don't need a cart experience and simply want to send users to pay immediately.

The main limitation with this feature at the moment is that it only works with single products. Meaning, you can’t use this to checkout with more than one product at a time. If you have two products side-by-side, both using direct checkout, they won’t share the “same” line items. Each button will take the user to a unique checkout page.

Direct Checkout can be enabled globally within the plugin settings under the "Checkout" subnav, or by using the new shortcode attribute `direct_checkout="true"`

This is a [Pro-only feature](https://wpshop.io/purchase?utm_medium=docs&utm_source=features&utm_campaign=upgrade).

## Sync featured images <span class="attr-type attr-type-pro-only">(Pro only)</span>

Sync featured images will allow you to sync your Shopify images as native WordPress featured images. The image itself will be uploaded into the WordPress media library, allowing you to use standard functions like `the_post_thumbnail` and `get_the_post_thumbnail_url`.

This is turned off by default and only the featured images inside Shopify will be uploaded.

This is a [Pro-only feature](https://wpshop.io/purchase?utm_medium=docs&utm_source=features&utm_campaign=upgrade).
