# JavaScript Actions: Cart

## on.cart.close

Fires after the cart closes

<span class="heading-section">🎯 Example Usage</span>

```js
wp.hooks.addAction('on.cart.close', 'wpshopify', function(lineItem, modVariant) {
   // Do something after add to cart ...
})
```

## on.cart.open

Fires after the cart opens

<span class="heading-section">🎯 Example Usage</span>

```js
wp.hooks.addAction('on.cart.close', 'wpshopify', function(lineItem, modVariant) {
   // Do something after add to cart ...
})
```
