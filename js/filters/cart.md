# Cart JavaScript Filters

You may want to read our [Getting started with JavaScript Hooks](guides/javascript-hooks.md) guide first.

## `default.cart.title`

Allows you to change the default cart title.

| Parameter    | Description                                                 |
| :----------- | :---------------------------------------------------------- |
| defaultTitle | Represents the current cart title. Default: `Shopping cart` |

**Example**

```js
wp.hooks.addFilter('default.cart.title', 'wpshopify', function (defaultTitle) {
  return 'New cart title';
});
```

## `default.cart.checkout.text`

Allows you to change the default checkout button text.

| Parameter           | Description                                                            |
| :------------------ | :--------------------------------------------------------------------- |
| defaultCheckoutText | Represents the default checkout button text. Default: `Begin checkout` |

**Example**

```js
wp.hooks.addFilter('default.cart.checkout.text', 'wpshopify', function (defaultCheckoutText) {
  return 'New checkout button text';
});
```

## `cart.lineItems.link`

Allows you to customize the link for each cart line item

| Parameter   | Description                                 |
| :---------- | :------------------------------------------ |
| defaultLink | Represents the default link. Default: false |
| lineItem    | Represents the line item data               |
| cartState   | Represents the cart state                   |

**Example**

```js
wp.hooks.addFilter('cart.lineItems.link', 'wpshopify', function (defaultLink, lineItem, cartState) {
  return 'https://google.com';
});
```

## `cart.lineItems.disableLink`

Allows you to disable the link for each cart line item

| Parameter   | Description                                 |
| :---------- | :------------------------------------------ |
| defaultLink | Represents the default link. Default: false |
| lineItem    | Represents the line item data               |
| cartState   | Represents the cart state                   |

**Example**

```js
wp.hooks.addFilter('cart.lineItems.disableLink', 'wpshopify', function (
  defaultLink,
  lineItem,
  cartState
) {
  return true;
});
```

## `cart.lineItems.maxQuantity`

Allows you to customize the maximum quantity for each line item

| Parameter   | Description                                     |
| :---------- | :---------------------------------------------- |
| maxQuantity | Represents the maximum quantity. Default: false |
| cartState   | Represents the cart state                       |
| lineItem    | Represents the lineItem data                    |

**Example**

```js
wp.hooks.addAction('after.cart.ready', 'wpshopify', function (cartState) {
  wp.hooks.addFilter('cart.lineItems.maxQuantity', 'wpshopify', function (
    maxQuantity,
    cartState,
    lineItem
  ) {
    return 3;
  });
});
```

## `cart.lineItems.minQuantity`

Allows you to customize the minimum quantity for each line item

| Parameter   | Description                                     |
| :---------- | :---------------------------------------------- |
| minQuantity | Represents the minimum quantity. Default: false |
| cartState   | Represents the cart state                       |
| lineItem    | Represents the lineItem data                    |

**Example**

```js
wp.hooks.addAction('after.cart.ready', 'wpshopify', function (cartState) {
  wp.hooks.addFilter('cart.lineItems.minQuantity', 'wpshopify', function (
    minQuantity,
    cartState,
    lineItem
  ) {
    return 3;
  });
});
```

## `cart.lineItems.quantityStep`

Allows you to customize the quantity step for each line item. This forces the user to only increment by the step. E.g., if the step is "2" the increment would be `2`, `4`, `6`.

| Parameter    | Description                                     |
| :----------- | :---------------------------------------------- |
| quantityStep | Represents the minimum quantity. Default: false |
| cartState    | Represents the cart state                       |
| lineItem     | Represents the lineItem data                    |

**Example**

```js
wp.hooks.addAction('after.cart.ready', 'wpshopify', function (cartState) {
  wp.hooks.addFilter('cart.lineItems.quantityStep', 'wpshopify', function (
    quantityStep,
    cartState,
    lineItem
  ) {
    return 2;
  });
});
```

## `default.cart.notes.label`

Allows you to customize the label above the cart note field

| Parameter    | Description                                                       |
| :----------- | :---------------------------------------------------------------- |
| defaultLabel | Represents the default cart note label. Default: `Checkout notes` |
| cartState    | Represents the cart state                                         |

**Example**

```js
wp.hooks.addFilter('default.cart.notes.label', 'wpshopify', function (defaultLabel, cartState) {
  return 'Custom text';
});
```

## `cart.note.placeholder`

Allows you to customize the default cart note placeholder value

| Parameter          | Description                                                                      |
| :----------------- | :------------------------------------------------------------------------------- |
| defaultPlaceholder | Represents the default cart note placeholder. Default: `Enter note for checkout` |
| cartState          | Represents the cart state                                                        |

**Example**

```js
wp.hooks.addFilter('cart.note.placeholder', 'wpshopify', function (defaultPlaceholder, cartState) {
  return 'Custom text';
});
```

## `cart.empty.text`

Allows you to customize the default empty cart text

| Parameter   | Description                                                           |
| :---------- | :-------------------------------------------------------------------- |
| defaultText | Represents the default empty cart text. Default: `Your cart is empty` |

**Example**

```js
wp.hooks.addFilter('cart.empty.text', 'wpshopify', function (defaultText, cartState) {
  return 'Custom text ........';
});
```

## `cart.subtotal.text`

Allows you to customize the subtotal label text

| Parameter   | Description                                                      |
| :---------- | :--------------------------------------------------------------- |
| defaultText | Represents the default subtotal label text. Default: `Subtotal:` |

**Example**

```js
wp.hooks.addFilter('cart.subtotal.text', 'wpshopify', function (defaultText) {
  return 'Custom text';
});
```

## `cart.lineItem.remove.text`

Allows you to customize the line item removal text

| Parameter   | Description                                                      |
| :---------- | :--------------------------------------------------------------- |
| defaultText | Represents the default line item removal text. Default: `Remove` |

**Example**

```js
wp.hooks.addFilter('cart.lineItem.remove.text', 'wpshopify', function (defaultText) {
  return 'Custom text';
});
```

## `cart.lineItem.price.sale`

Allows you to customize the line item price sale label

| Parameter   | Description                                                         |
| :---------- | :------------------------------------------------------------------ |
| defaultText | Represents the default line item price sale label. Default: `Sale!` |

**Example**

```js
wp.hooks.addFilter('cart.lineItem.price.sale', 'wpshopify', function (defaultText) {
  return 'Custom text';
});
```

## `cart.lineItem.title.text`

Allows you to customize each line item title

| Parameter     | Description                    |
| :------------ | :----------------------------- |
| lineItemTitle | Represents the line item title |

**Example**

```js
wp.hooks.addFilter('cart.lineItem.title.text', 'wpshopify', function (lineItemTitle) {
  return 'Custom text';
});
```

## `cart.lineItem.variant.title`

Allows you to customize each line item variant title

| Parameter     | Description                       |
| :------------ | :-------------------------------- |
| lineItemTitle | Represents the line variant title |

**Example**

```js
wp.hooks.addFilter('cart.lineItem.variant.title', 'wpshopify', function (lineItemVariantTitle) {
  return 'Custom text';
});
```

## `before.cart.checkout.button`

Allows you to add arbitrary HTML before the cart checkout button

| Parameter  | Description                                                        |
| :--------- | :----------------------------------------------------------------- |
| defaultVal | Represents the default content before the button. Default: `false` |

**Example**

```js
wp.hooks.addFilter('before.cart.checkout.button', 'wpshopify', function (defaultVal) {
  return '<p>Before checkout button</p>';
});
```

## `after.cart.checkout.button`

Allows you to add arbitrary HTML after the cart checkout button

| Parameter  | Description                                                       |
| :--------- | :---------------------------------------------------------------- |
| defaultVal | Represents the default content after the button. Default: `false` |

**Example**

```js
wp.hooks.addFilter('after.cart.checkout.button', 'wpshopify', function (defaultVal) {
  return '<p>After checkout button</p>';
});
```

## `before.cart.title`

Allows you to add arbitrary HTML before the cart title

| Parameter  | Description                                                            |
| :--------- | :--------------------------------------------------------------------- |
| defaultVal | Represents the default content before the cart title. Default: `false` |

**Example**

```js
wp.hooks.addFilter('before.cart.title', 'wpshopify', function (defaultVal) {
  return '<p>Before cart title</p>';
});
```

## `after.cart.title`

Allows you to add arbitrary HTML after the cart title

| Parameter  | Description                                                           |
| :--------- | :-------------------------------------------------------------------- |
| defaultVal | Represents the default content after the cart title. Default: `false` |

**Example**

```js
wp.hooks.addFilter('after.cart.title', 'wpshopify', function (defaultVal) {
  return '<p>Before cart title</p>';
});
```
