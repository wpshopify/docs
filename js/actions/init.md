# JavaScript Actions: Init

Before getting started, please [read our JavaScript hooks guide](guides/javascript-hooks.md).

## before.ready

Fires before the application is ready to use.

| Parameters | Description                             |
| :--------- | :-------------------------------------- |
| shopState  | Represents the global application state |

**Example Usage**

```js
wp.hooks.addAction('before.ready', 'wpshopify', function(shopState) {
   // Do something after add to cart ...
})
```

## after.ready

Fires after the application is finished initializing and is ready to use.

| Parameters | Description                             |
| :--------- | :-------------------------------------- |
| shopState  | Represents the global application state |

**Example Usage**

```js
wp.hooks.addAction('after.ready', 'wpshopify', function(shopState) {
   // Do something after add to cart ...
})
```
