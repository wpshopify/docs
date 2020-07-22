# Misc JavaScript Filters

You may want to read our [Getting started with JavaScript Hooks](guides/javascript-hooks.md) guide first.

## `misc.inventory.leftInStock.total`

Allows you to customize the number threshold before the left in stock notice appears

| Parameter        | Description                                                          |
| :--------------- | :------------------------------------------------------------------- |
| leftInStockTotal | Represents the default left in stock threshold number. Default: `10` |

**Example**

```js
wp.hooks.addFilter('misc.inventory.leftInStock.total', 'wpshopify', function (leftInStockTotal) {
  return 5
})
```

## `misc.link.target`

Allows you to customize whether links open in a new tab / window

| Parameter     | Description                                               |
| :------------ | :-------------------------------------------------------- |
| defaultTarget | Represents the default target for links. Default: `_self` |

**Example**

```js
wp.hooks.addFilter('misc.link.target', 'wpshopify', function (defaultTarget) {
  return '_blank'
})
```

## `misc.layout.mobileColumns`

Allows you to customize the number of columns that products are listed within the mobile layout

| Parameter         | Description                                                   |
| :---------------- | :------------------------------------------------------------ |
| defaultMobileCols | Represents the default number of mobile columns. Default: `1` |

**Example**

```js
wp.hooks.addFilter('misc.link.target', 'wpshopify', function (defaultMobileCols) {
  return 2
})
```
