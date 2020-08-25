# JavaScript Actions: Cart

Please first read our [Getting started with JavaScript Hooks](guides/javascript-hooks.md) guide.

## `before.cart.ready`

Runs before the cart state has been initialized during initial page load.

| Argument  | Description         |
| :-------- | :------------------ |
| cartState | The full cart state |

**Example**

```js
wp.hooks.addAction('before.cart.ready', 'wpshopify', function (cartState) {
  console.log('cartState :: ', cartState);
});
```

## `after.cart.ready`

Runs after the cart state has been initialized during initial page load.

| Argument  | Description         |
| :-------- | :------------------ |
| cartState | The full cart state |

**Example**

```js
wp.hooks.addAction('after.cart.ready', 'wpshopify', function (cartState) {
  console.log('cartState :: ', cartState);
});
```

## `on.cart.toggle`

Fires when the cart opens / closes

| Parameter | Description                                                  |
| :-------- | :----------------------------------------------------------- |
| openState | Represents whether the cart is open or not. Default: `false` |

**Example**

```js
wp.hooks.addAction('on.cart.toggle', 'wpshopify', function (openState) {
  // Do something when the cart opens or closes
  console.log('openState :: ', openState);
});
```

## `cart.toggle`

Allows for opening or closing the cart

| Argument  | Description                                                                      |
| :-------- | :------------------------------------------------------------------------------- |
| openState | Whether to open or close the cart as a string. Accepts either `open` or `close`. |

**Example**

```js
wp.hooks.addAction('after.cart.ready', 'wpshopify', function (cartState) {
  // Open the cart
  wp.hooks.doAction('cart.toggle', 'open');
});
```

```js
wp.hooks.addAction('after.cart.ready', 'wpshopify', function (cartState) {
  // Close the cart
  wp.hooks.doAction('cart.toggle', 'close');
});
```

## `show.cart.title`

Allows for hiding the title within the cart

| Argument  | Description                                                         |
| :-------- | :------------------------------------------------------------------ |
| hideTitle | Whether to hide the cart title. Accepts boolean: `true` or `false`. |

**Example**

```js
wp.hooks.addAction('after.cart.ready', 'wpshopify', function (cartState) {
  wp.hooks.doAction('show.cart.title', false);
});
```

## `show.cart.close`

Allows for hiding the close icon within the cart

| Argument | Description                                                   |
| :------- | :------------------------------------------------------------ |
| hideIcon | Whether to hide the icon. Accepts boolean: `true` or `false`. |

**Example**

```js
wp.hooks.addAction('after.cart.ready', 'wpshopify', function (cartState) {
  wp.hooks.doAction('show.cart.close', false);
});
```

## `after.cart.lineItem.remove`

Runs after a line item is removed from the cart.

| Argument  | Description                     |
| :-------- | :------------------------------ |
| lineItem  | The line item object            |
| variantId | The variant id that was removed |

**Example**

```js
wp.hooks.addAction('after.cart.lineItem.remove', 'wpshopify', function (lineItem, variantId) {
  // Do something after line item is removed
});
```
