# Pagination JavaScript Filters

You may want to read our [Getting started with JavaScript Hooks](guides/javascript-hooks.md) guide first.

## `pagination.loadMore.text`

Allows for customizing the load more button text

| Parameter   | Description                                                 |
| :---------- | :---------------------------------------------------------- |
| defaultText | Represents the default load more text. Default: `Load more` |

**Example**

```js
wp.hooks.addFilter('pagination.loadMore.text', 'wpshopify', function (defaultText) {
  return 'Custom text'
})
```
