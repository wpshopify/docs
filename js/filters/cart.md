# JavaScript Filters: Cart

## default.cart.title

Changes the default cart title

<span class="heading-section">🎯 Example Usage</span>

```js
wp.hooks.addFilter('default.cart.title', 'wpshopify', content => {
   return 'New cart title'
})
```

## default.cart.checkout.text

Changes the default checkout button text

<span class="heading-section">🎯 Example Usage</span>

```js
wp.hooks.addFilter('default.cart.checkout.text', 'wpshopify', content => {
   return 'New checkout button text'
})
```
