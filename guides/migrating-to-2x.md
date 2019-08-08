# Migrating to WP Shopify 2.x

WP Shopify 2.0 was released in July of 2019. With it came various backwards incompatible changes with version 1.x. This guide aims to help the process of migrating to the new version.

## What changed?

WP Shopify 2.x brings a completely new rendering system. Instead of rendering products on the server via PHP, mostly everything is now rendered in JavaScript. This solves the two main problems with version 1.x which are [syncing reliability](https://wpshop.io/blog/wp-shopify-2-0-has-launched/#limitations-of-v1) and [data accuracy](https://wpshop.io/blog/wp-shopify-2-0-has-launched/#limitations-of-v1). We've come to the conclusion that these two traits _need_ to exist for a store to be of any value.

## What's happening to version 1.x?

Nothing! Version 1.x will continue to work like normal and for all [Pro customers](https://wpshop.io/purchase), we will continue to support 1.x for the forseeable future.

## How to update

1. First, it's highly recommended that you upgrade the plugin to version 2.0 on a staging server _before_ updating your live site. This will allow you to check for breaking changes before your users do!

2. Once you've updated, be sure to check that the following continuing to work:
   -  Any shortcodes you're using
   -  Product single pages

## Breaking changes

We tried our best to avoid breaking changes, but we ultimately decided that it was needed for the long term viability of the plugin. Too many people were having syncing issues and so we decided to take a client-side, JavaScript first approach.

**List of breaking changes:**

-  The PHP namespace `WPS` has changed to `WP_Shopify`
-  Various template overrides no longer work
-  Various PHP hooks no longer work
-  Removed related products on product single pages

> [!NOTE|className:info sm]
> We plan on rolling out server-side PHP rendering similar to version 1.x as an _opt-in_ feature later this year.

## Namespace change

In order to be compatible with the WordPress.org repository, we had to change the namespace of the plugin from `WPS` to `WP_Shopify`. This is so that we don't conflict with other plugins.

For those who were using the template overrides in `1.x`, you need to update your templates to reflect the new namespace.

All instances of `WPS` need to be changed to `WP_Shopify`. For example:

_Old_

```js
$Products = WPS\Factories\DB\Products_Factory::build();
```

_New_

```js
$Products = WP_Shopify\Factories\DB\Products_Factory::build();
```

## Changed shortcode attributes

-  The `[wps_cart]` shortcode has been replaced with `[wps_cart_icon]`
-  `items-per-row` has been replaced with [items_per_row](shortcodes/wps_products?id=items_per_row)
-  `keep-permalinks` has been removed
-  `breadcrumbs` has been removed
-  `add-to-cart` has been removed. The add to cart button is now shown by default. If you wish to hide, use the new [excludes](shortcodes/wps_products?id=excludes) attribute
-  `order` has been replaced with [reverse](shortcodes/wps_products?id=reverse)
-  `orderby` has been replaced with [sort_by](shortcodes/wps_products?id=sort_by)
-  `desc` has been removed
-  `options` has been removed
-  `variants` has been removed
-  `slugs` has been removed
-  `collections` has been removed
-  `titles` has been replaced with [title](shortcodes/wps_products?id=title)
-  `tags` has been replaced with [tag](shortcodes/wps_products?id=tag)
-  `vendors` has been replaced with [vendor](shortcodes/wps_products?id=vendor)
-  `ids` has been replaced with [product_id](shortcodes/wps_products?id=product_id)
