# JavaScript Actions: Cart

Please first read our [Getting started with JavaScript Hooks](guides/javascript-hooks.md) guide.

## `on.cart.open`

Fires after the cart opens.

| Parameter   | Description                     |
| :---------- | :------------------------------ |
| cartElement | Represents the cart DOM element |

**Example**

```js
wp.hooks.addAction('on.cart.open', 'wpshopify', function(cartElement) {
   // Do something after the cart opens
})
```

## `on.cart.close`

Fires after the cart closes.

| Parameter   | Description                     |
| :---------- | :------------------------------ |
| cartElement | Represents the cart DOM element |

**Example**

```js
wp.hooks.addAction('on.cart.close', 'wpshopify', function(cartElement) {
   // Do something after the cart closes
})
```
