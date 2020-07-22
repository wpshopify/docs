# Cart JavaScript Filters

You may want to read our [Getting started with JavaScript Hooks](guides/javascript-hooks.md) guide first.

## `default.cart.title`

Allows you to change the default cart title.

| Parameter | Description                       |
| :-------- | :-------------------------------- |
| title     | Represents the current cart title |

**Example**

```js
wp.hooks.addFilter('default.cart.title', 'wpshopify', function (title) {
  return 'New cart title'
})
```

## `default.cart.checkout.text`

Allows you to change the default checkout button text.

**Example**

| Parameter  | Description                                 |
| :--------- | :------------------------------------------ |
| buttonText | Represents the current checkout button text |

```js
wp.hooks.addFilter('default.cart.checkout.text', 'wpshopify', function (buttonText) {
  return 'New checkout button text'
})
```

## `cart.lineItems.link`

## `cart.lineItems.disableLink`

## `cart.lineItems.maxQuantity`

## `cart.lineItems.minQuantity`

## `cart.lineItems.quantityStep`

## `cart.note.label`

## `cart.note.placeholder`

## `cart.checkout.text`

## `cart.empty.text`

## `cart.subtotal.text`

## `cart.lineItem.remove.text`

## `cart.lineItem.price.sale`

## `cart.lineItem.title.text`

## `cart.lineItem.variant.title`

## `cart.title.text`

## `before.cart.checkout.button`

## `after.cart.checkout.button`

## `before.cart.title`

## `after.cart.title`

## `default.cart.notes.label`
