# Global JavaScript Filters

You may want to read our [Getting started with JavaScript Hooks](guides/javascript-hooks.md) guide first.

## `global.loading.text`

Allows you to customize the global loading text before the plugin is ready

| Parameter          | Description                                                        |
| :----------------- | :----------------------------------------------------------------- |
| defaultLoadingText | Represents the default global loading text. Default: `Loading ...` |

**Example**

```js
wp.hooks.addFilter('global.loading.text', 'wpshopify', function (defaultLoadingText) {
  return 'Custom text'
})
```
