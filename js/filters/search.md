# Search JavaScript Filters

You may want to read our [Getting started with JavaScript Hooks](guides/javascript-hooks.md) guide first.

## `search.placeholder.text`

Allows for customizing the default search placeholder text.

| Parameters         | Description                                                                 |
| :----------------- | :-------------------------------------------------------------------------- |
| defaultPlaceholder | Represents the default search placeholder text. Default: `Search the store` |

**Example**

```js
wp.hooks.addFilter('search.placeholder.text', 'wpshopify', function (defaultPlaceholder) {
  return defaultPlaceholder
})
```
