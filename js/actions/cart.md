# JavaScript Actions: Cart

Before getting started, please [read our JavaScript hooks guide](guides/javascript-hooks.md).

## on.cart.open

Fires after the cart opens.

| Parameters  | Description                     |
| :---------- | :------------------------------ |
| cartElement | Represents the cart DOM element |

**Example**

```js
wp.hooks.addAction('on.cart.open', 'wpshopify', function(cartElement) {
   // Do something after the cart opens
})
```

## on.cart.close

Fires after the cart closes.

| Parameters  | Description                     |
| :---------- | :------------------------------ |
| cartElement | Represents the cart DOM element |

**Example**

```js
wp.hooks.addAction('on.cart.close', 'wpshopify', function(cartElement) {
   // Do something after the cart closes
})
```
