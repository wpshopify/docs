# Checkout JavaScript Filters

You may want to read our [Getting started with JavaScript Hooks](guides/javascript-hooks.md) guide first.

## `before.checkout.lineItems`

Allows you to filter the line items before the checkout redirect occurs

| Parameter | Description                                         |
| :-------- | :-------------------------------------------------- |
| lineItems | Represents the default content after the cart title |
| cartState | Represents the cart state                           |

**Example**

```js
wp.hooks.addFilter('before.checkout.lineItems', 'wpshopify', function (lineItems) {
  return lineItems
})
```

## `checkout.url`

Allows you to filter the checkout URL before the redirect happens

| Parameter | Description              |
| :-------- | :----------------------- |
| url       | The default checkout URL |

**Example**

```js
wp.hooks.addFilter('checkout.url', 'wpshopify', function (url) {
  return url
})
```
