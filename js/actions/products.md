# JavaScript Actions: Products

Please first read our [Getting started with JavaScript Hooks](guides/javascript-hooks.md) guide.

## `before.product.addToCart`

Fires after all available variants are selected but before adding to the cart.

| Parameters     | Description                                                |
| :------------- | :--------------------------------------------------------- |
| buyButtonState | Represents the buy button state and contains product data. |

**Example**

```js
wp.hooks.addAction('before.product.addToCart', 'wpshopify', function(buyButtonState) {
   // Do something
})
```

## `on.product.addToCart`

Fires when a product is added to the cart.

| Parameters     | Description                                           |
| :------------- | :---------------------------------------------------- |
| lineItem       | Represents the data that is added to the cart session |
| productVariant | Represents the product variant data                   |

**Example**

```js
wp.hooks.addAction('on.product.addToCart', 'wpshopify', function(lineItem, productVariant) {
   // Do something
})
```

## `on.product.variant.selection`

Fires each time a product variant is selected.

| Parameters         | Description                          |
| :----------------- | :----------------------------------- |
| selectedVariant    | Represents the selected variant data |
| productOptionState | Represents the product data          |

**Example**

```js
wp.hooks.addAction('on.product.variant.selection', 'wpshopify', function(selectedVariant, productOptionState) {
   // Do something
})
```
