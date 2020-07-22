# Product Images JavaScript Filters

You may want to read our [Getting started with JavaScript Hooks](guides/javascript-hooks.md) guide first.

## `default.image.zoom.options`

Allows for customizing the image zoom options. The full list of options [can be found here](https://github.com/imgix/drift#options--defaults)

| Parameters     | Description                               |
| :------------- | :---------------------------------------- |
| defaultOptions | Represents the default image zoom options |

**Example**

```js
wp.hooks.addFilter('default.image.zoom.options', 'wpshopify', function (defaultOptions) {
  defaultOptions.onShow = function () {
    console.log('on zoom show')
  }
  return defaultOptions
})
```
