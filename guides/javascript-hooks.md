# Getting started with JavaScript Hooks

> [!NOTE|className:info sm]
> JavaScript Hooks require WordPress 5.0 or higher

JavaScript hooks were introduce to WordPress in version 5.0 with the advent of the highly anticipated Gutenberg release. These are very similar to the standard PHP hooks that WordPress developers have been familiar with for years.

Like PHP hooks, these JavaScript-based hooks allow you to "filter" data and listen to unique "actions". This guide won't be a thorough tutorial on how to use WordPress hooks. For that, please take a look at the [official WordPress documentation](https://developer.wordpress.org/block-editor/packages/packages-hooks/) first.

WP Shopify provides many different JavaScript hooks which allow you to hook into various parts of the plugin. This enables you to do things such as detect when the cart opens, or when the user clicks the checkout button. From there, you can run your own code from a callback function to make any customizations you want. Let's see how this works.

## 1. Bootstrapping

The process is a bit different depending on whether you're using an action or filter.

Any _action_ hook needs to be encapsulated within the `after.ready` action. This action runs when WP Shopify is done bootstrapping. So if you're using an action, begin your customizations with the following.

```js
wp.hooks.addAction('after.ready', 'wpshopify', function() {
   // Your custom actions go here
})
```

Any _filter_ hook can be used without the `after.ready` action.

## 2. Adding an action hook

Let's say we want to detect when a product is added to the cart. We can do this by hooking into the [after.product.addToCart](js/actions/products?id=afterproductaddtocart) action like this:

```js
wp.hooks.addAction('after.ready', 'wpshopify', function() {
   wp.hooks.addAction('after.product.addToCart', 'wpshopify', function(lineItem, productVariant) {
      // Do something after adding to cart ...
   })
})
```

The `after.product.addToCart` action is given two parameters `lineItem` and `productVariant` that you can inspect. Each hook will have useful parameters like this to aid you along the way.

We've listed all of the [available JavaScript hooks](js/actions/init) in this documentation.

## 2. Adding a filter hook

Let's say we want to customize the checkout button text. We can do this by hooking into the [default.cart.checkout.text](js/filters/cart?id=defaultcartcheckouttext) filter like this:

```js
wp.hooks.addFilter('default.cart.checkout.text', 'wpshopify', buttonText => {
   return 'New checkout button text'
})
```

## 3. Getting the order right

WP Shopify injects it's JavaScript in the footer to improve performance. However it's possible that your theme's JavaScript may run _before_ WP Shopify. If this occurs none of the JavaScript hooks will work.

To get around this, be sure to set `wpshopify-scripts-frontend` as a dependency in your theme's wp_enqueue_script call like this:

```php
wp_enqueue_script( 'your-js', '<your path>/stuff.js', ['wpshopify-scripts-frontend'], true);
```