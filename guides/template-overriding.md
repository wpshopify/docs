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
> Do not edit the core plugin template files. If you do, your changes will be overwritten when the plugin updates and any customizations will be lost.

## HTML Templates

Starting in version `3.2.0`, you can now specify a custom template to be used for product html. This can be done by using the `html_template` attribute either with a shortcode or through the Render API.

This is different from the `products-single.php` and `products-all.php` templates in that **it will only apply to the product itself**. If displaying more than one product, this template will be ran for each product in the list.

It's also different because of the [specific rules of when using it](#rules-of-using-html-templates).

### Using the html_template attribute

When using `html_template` you must specify the name of a valid .php file you wish to use, like this:

Shortcode:

```
[wps_products html_template="product.php"]
```

Render API:

```
$Products = WP_Shopify\Factories\Render\Products\Products_Factory::build();

$Products->products([ 'html_template' => 'product.php' ]);
```

### Locating the custom html_template files

Because you can specify any file to be used, you'll need to add your files to a special folder so the plugin can look for them. This special folder is called `custom`, and must be placed directly inside the `wps-templates` folder.

For example, if your template file is called `product.php`, the folder structure must look like this:

```
wp-content/my-theme/wps-templates/custom/product.php
```

> [!NOTE|className:info sm]
> If you're using a page builder you don't need to worry about this. The builder's module will handle the actual template content so you don't have to.

### Rules of using HTML Templates

There are a couple rules when using HTML Templates.

1. Any PHP that you use must output valid HTML. For example, if you have a PHP function called `doStuff()`, this function must return HTML and therefore you must echo it.

2. Any HTML syntax errors can cause render issues so be sure your HTML is valid.

3. In order to output the various product components (Title, Pricing, etc), you must use them like this:

```
<ProductImages />
<ProductTitle />
<ProductPricing />
<ProductDescription />
<ProductBuyButton />
```

For example, to create a two column layout with images on the left and product title on the right, you could do something like this:

```
<div class="row">
   <div class="col-2">
      <ProductImages />
   </div>
   <div class="col-2">
      <ProductTitle />
   </div>
</div>
```

You cannot currently modify the HTML contents of the template components.

### Available HTML Template components

```
<ProductImages />
<ProductTitle />
<ProductPricing />
<ProductDescription />
<ProductBuyButton />
```

## List of available templates

- [products-single](templates/products/single.md)
- [products-all](templates/products/all.md)
- [collections-single](templates/collections/single.md)
- [collections-all](templates/collections/all.md)
- [custom](#html_template)
