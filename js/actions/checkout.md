# JavaScript Actions: Checkout

## set.checkout.attributes

Fires after the cart closes

<span class="heading-section">🎯 Example Usage</span>

```js
wp.hooks.addAction('set.checkout.attributes', 'wpshopify', function(lineItem, modVariant) {
   // Do something after add to cart ...
})
```

## update.checkout.attributes

Fires after the cart opens

<span class="heading-section">🎯 Example Usage</span>

```js
wp.hooks.addAction('update.checkout.attributes', 'wpshopify', function(lineItem, modVariant) {
   // Do something after add to cart ...
})
```

## set.checkout.note

Fires after the cart opens

<span class="heading-section">🎯 Example Usage</span>

```js
wp.hooks.addAction('set.checkout.note', 'wpshopify', function(lineItem, modVariant) {
   // Do something after add to cart ...
})
```

# on.checkout

Event fires when the checkout button is clicked

<span class="heading-section">🎯 Example Usage</span>

```js
wp.hooks.addAction('on.checkout', 'wpshopify', function(checkout) {
   // Do something on checkout ...
})
```
