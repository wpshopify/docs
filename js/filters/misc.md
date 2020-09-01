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
  return 5;
});
```

## `misc.link.target`

Allows you to customize whether links open in a new tab / window

| Parameter     | Description                                               |
| :------------ | :-------------------------------------------------------- |
| defaultTarget | Represents the default target for links. Default: `_self` |

**Example**

```js
wp.hooks.addFilter('misc.link.target', 'wpshopify', function (defaultTarget) {
  return '_blank';
});
```

## `misc.link.href`

Allows you to customize the link for a product or collection

| Parameter     | Description                                             |
| :------------ | :------------------------------------------------------ |
| defaultTarget | Represents the default href for links.                  |
| type          | Represents the type of link `products` or `collections` |

**Example**

```js
wp.hooks.addFilter('misc.link.href', 'wpshopify', function (defaultLink, type) {
  return 'https://mysite.com/newlink';
});
```

## `misc.layout.mobileColumns`

Allows you to customize the number of columns that products are listed within the mobile layout

| Parameter         | Description                                                   |
| :---------------- | :------------------------------------------------------------ |
| defaultMobileCols | Represents the default number of mobile columns. Default: `1` |

**Example**

```js
wp.hooks.addFilter('misc.link.target', 'wpshopify', function (defaultMobileCols) {
  return 2;
});
```

## `misc.pricing.defaultCurrencyCode`

Allows for filtering the default currency code used to format money prices. Useful for changing things like the subtotal format into a different currency. Must return a valid [ISO 4217 Currency Code](https://www.xe.com/iso4217.php).

| Parameters  | Description                                                   |
| :---------- | :------------------------------------------------------------ |
| defaultCode | Represents the default ISO 4217 Currency Code. Default: `USD` |

**Example**

```js
wp.hooks.addFilter('misc.pricing.defaultCurrencyCode', 'wpshopify', function (defaultCode) {
  return 'EUR';
});
```
