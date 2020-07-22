# Product Pricing JavaScript Filters

You may want to read our [Getting started with JavaScript Hooks](guides/javascript-hooks.md) guide first.

## `misc.pricing.defaultCurrencyCode`

Allows for filtering the default currency code used to format money prices. Useful for changing things like the subtotal format into a different currency. Must return a valid [ISO 4217 Currency Code](https://www.xe.com/iso4217.php).

| Parameters  | Description            | Default |
| :---------- | :--------------------- | :------ |
| defaultCode | ISO 4217 Currency Code | USD     |

**Example**

```js
wp.hooks.addFilter('misc.pricing.defaultCurrencyCode', 'wpshopify', function (defaultCode) {
  return 'EUR'
})
```

## `product.pricing.from.text`
