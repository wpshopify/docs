# JavaScript Actions: Init

Please first read our [Getting started with JavaScript Hooks](guides/javascript-hooks.md) guide.

## `before.ready`

Fires before the application is ready to use.

| Parameters     | Description                           |
| :------------- | :------------------------------------ |
| pluginSettings | Represents the global plugin settings |

**Example Usage**

```js
wp.hooks.addAction('before.ready', 'wpshopify', function(pluginSettings) {
   // Do something after add to cart ...
})
```

## `after.ready`

Fires after the application is finished initializing and is ready to use.

| Parameters     | Description                           |
| :------------- | :------------------------------------ |
| pluginSettings | Represents the global plugin settings |

**Example Usage**

```js
wp.hooks.addAction('after.ready', 'wpshopify', function(pluginSettings) {
   // Do something after add to cart ...
})
```
