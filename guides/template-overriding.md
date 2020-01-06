# Template Overriding

[WP Shopify Pro](https://wpshop.io/purchase/) comes with PHP templates that you can use to override various parts of the plugin's layout. Our templates are very similar to how the WooCommerce templates work.

## Setting up your theme

First, create a folder inside your theme (or child theme) called `wps-templates`.

## How to override

Once you've created the `wps-templates` folder, you need to figure which template to override. Have a look at our full [list of available templates](#list-of-available-templates).

The plugin templates can be found within the `plugins/wp-shopify-pro/public/templates/` directory. Once you find the template you want, copy the file from the plugin into your `wps-templates` folder.

It's important that you keep the same folder structure that the plugin uses. The plugin's "templates" folder acts as the root, similar to the "wps-templates" folder that you create. For example, if your intention is to customize the product single pages you’ll need to ...

> Copy from: `wp-shopify-pro/public/templates/products-single.php`<br>
> Copy to: `<your theme>/wps-templates/products-single.php`

Notice how the `products-single.php` file sits at the same directory level in both cases.

The copied file will now override the WP Shopify default template file. When you update the plugin none of the changes in your theme’s `wps-templates` will be lost.

However, if you want to override a template that lives in a nested sub-folder, you'll need to also add those sub-folders. For example ...

> Copy from: `wp-shopify-pro/public/templates/webhooks/products/product-update.php`<br>
> Copy to: `<your theme>/wps-templates/webhooks/products/product-update.php`

Notice how you need also create the `webhooks` and `products` sub-folders in the above example?

> [!NOTE|className:warning sm]
> Do not edit the core plugin template files as they are overwritten during the upgrade process and any customizations will be lost.

## List of available templates

- [products-single](templates/products/single.md)
- [products-all](templates/products/all.md)
- [collections-single](templates/collections/single.md)
- [collections-all](templates/collections/all.md)
