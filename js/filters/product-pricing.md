# Product Pricing JavaScript Filters

You may want to read our [Getting started with JavaScript Hooks](guides/javascript-hooks.md) guide first.

## `product.pricing.from.text`

Allows for customizing the label shown when displaying price ranges.

| Parameters  | Description                  |
| :---------- | :--------------------------- |
| defaultText | Represents the default text. |

**Example**

```js
wp.hooks.addFilter('product.pricing.from.text', 'wpshopify', function (defaultText) {
  return 'Custom from text';
});
```
