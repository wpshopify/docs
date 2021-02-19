# JavaScript Actions: Products

Please first read our [Getting started with JavaScript Hooks](guides/javascript-hooks.md) guide.

## `before.product.addToCart`

Fires after all available variants are selected but before adding to the cart.

| Parameters     | Description                                                |
| :------------- | :--------------------------------------------------------- |
| buyButtonState | Represents the buy button state and contains product data. |

**Example**

```js
wp.hooks.addAction('after.cart.ready', 'wpshopify', function (cartState) {
  wp.hooks.addAction('before.product.addToCart', 'wpshopify', function (buyButtonState) {
    // Do something
    console.log('WP Shopify Event 💥 before.product.addToCart', buyButtonState);
  });
});
```

## `after.product.addToCart`

Fires after a product variant is added to the cart.

| Parameters     | Description                                           |
| :------------- | :---------------------------------------------------- |
| lineItem       | Represents the data that is added to the cart session |
| productVariant | Represents the product variant data                   |

**Example**

```js
wp.hooks.addAction('after.cart.ready', 'wpshopify', function (cartState) {
  wp.hooks.addAction('after.product.addToCart', 'wpshopify', function (lineItems, variant) {
    console.log('WP Shopify Event 💥 after.product.addToCart', buyButtonState);
  });
});
```

## `before.product.variantDropdown.toggle`

Fires before the variant dropdown opens

| Parameters         | Description                              |
| :----------------- | :--------------------------------------- |
| productOptionState | Represents the product option state data |

**Example**

```js
wp.hooks.addAction('after.cart.ready', 'wpshopify', function (cartState) {
  wp.hooks.addAction(
    'before.product.variantDropdown.toggle',
    'wpshopify',
    function (productOptionState) {
      console.log('WP Shopify Event 💥 before.product.variantDropdown.toggle', productOptionState);
    }
  );
});
```

## `after.product.variant.selection`

Fires after each product variant selection

| Parameters         | Description                         |
| :----------------- | :---------------------------------- |
| selectedVariant    | Represents the product variant data |
| productOptionState | Represents the product option state |

**Example**

```js
wp.hooks.addAction('after.cart.ready', 'wpshopify', function (cartState) {
  wp.hooks.addAction(
    'after.product.variant.selection',
    'wpshopify',
    function (selectedVariant, productOptionState) {
      console.log(
        'WP Shopify Event 💥 after.product.variant.selection',
        selectedVariant,
        productOptionState
      );
    }
  );
});
```

## `after.variants.selection`

Fires only after all product variants are selected

| Parameters | Description                          |
| :--------- | :----------------------------------- |
| variant    | Represents the selected variant data |

**Example**

```js
wp.hooks.addAction('after.variants.selection', 'wpshopify', function (variant) {
  console.log('variant', variant);
});
```
