# Getting started with JavaScript Hooks

> [!NOTE|className:info sm]
> JavaScript Hooks require that WordPress 5.0 or higher be installed.

JavaScript hooks were introduce to WordPress in version 5.0 with the advent of the highly anticipated Gutenberg release. These are very similar to the standard PHP hooks that WordPress developers have been familiar with for years.

Like PHP hooks, these JavaScript-based hooks allow you to "filter" data and listen to unique "actions". This guide won't be a thorough tutorial on how to use WordPress hooks. For that, please take a look at the [official WordPress documentation](https://developer.wordpress.org/block-editor/packages/packages-hooks/) first.

WP Shopify provides many different JavaScript hooks which allow you to hook into various parts of the plugin. This enables you to do things such as detect when the cart opens, or when the user clicks the checkout button. From there, you can run your own code from a callback function to make any customizations you want. Let's see how this works.

## 1. Bootstrapping

Any hook you add needs to be encapsulated within the `after.ready` action. This action runs when WP Shopify is done bootstrapping. So begin your customizations with the following:

```js
wp.hooks.addAction('after.ready', 'wpshopify', function() {
   // Your custom actions and filters go here
})
```

## 2. Adding a hook

Let's say we wanted to detect when a product was added to the cart so we could make some customizations. We can do this by hooking into the [after.product.addToCart](js/actions/products?id=afterproductaddtocart) action like this:

```js
wp.hooks.addAction('after.ready', 'wpshopify', function() {
   wp.hooks.addAction('after.product.addToCart', 'wpshopify', function(lineItem, productVariant) {
      // Do something after adding to cart ...
   })
})
```

The `after.product.addToCart` action is given two parameters `lineItem` and `productVariant` that you can inspect. Each hook will have useful parameters like this to aid you along the way.

We've listed all of the [available JavaScript hooks](js/actions/init) in this documentation.
