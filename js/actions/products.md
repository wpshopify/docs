# JavaScript Actions: Products

## before.product.addToCart

Fires before the add to cart event

<span class="heading-section">🎯 Example Usage</span>

```js
wp.hooks.addAction('before.product.addToCart', 'wpshopify', function(lineItem, modVariant) {
   // Do something after add to cart ...
})
```

## after.product.addToCart

Fires after the add to cart event

<span class="heading-section">🎯 Example Usage</span>

```js
wp.hooks.addAction('after.product.addToCart', 'wpshopify', function(lineItem, modVariant) {
   // Do something after add to cart ...
})
```

## on.product.variant.selection

Fires after a product variant has been selected

<span class="heading-section">🎯 Example Usage</span>

```js
wp.hooks.addAction('on.product.variant.selection', 'wpshopify', function(lineItem, modVariant) {
   // Do something after add to cart ...
})
```
