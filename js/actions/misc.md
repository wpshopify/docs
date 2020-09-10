# JavaScript Actions: Misc

Please first read our [Getting started with JavaScript Hooks](guides/javascript-hooks.md) guide.

## `before.payload.update`

Runs before the payload is fetched for products / colletions

| Arguments  | Description                                                      |
| :--------- | :--------------------------------------------------------------- |
| itemsState | A JavaScript object representing the products / collections data |

**Example Usage**

```js
wp.hooks.addAction('before.payload.update', 'wpshopify', function (itemsState) {
  console.log('WP Shopify Event 💥 before.payload.update', itemsState);
});
```

## `after.payload.update`

Runs after the payload is fetched for products / colletions. Also runs after clicking the load more buttons.

| Arguments  | Description                                                      |
| :--------- | :--------------------------------------------------------------- |
| itemsState | A JavaScript object representing the products / collections data |

**Example Usage**

```js
wp.hooks.addAction('after.payload.update', 'wpshopify', function (itemsState) {
  console.log('WP Shopify Event 💥 after.payload.update', itemsState);
});
```

## `wpshopify.render`

Allows for rendering the products manually. Useful if you need to load products dynamically after initial page load.

**Example Usage**

```js
// You can run this after initial page load inside a callback of some sort
wp.hooks.doAction('wpshopify.render');
```
