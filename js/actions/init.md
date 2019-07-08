# JavaScript Actions: Init

## before.ready

Fires before the application is ready to use while loading

<span class="heading-section">🎯 Example Usage</span>

```js
wp.hooks.addAction('before.ready', 'wpshopify', function(lineItem, modVariant) {
   // Do something after add to cart ...
})
```

## after.ready

Fires after the application is finished initializing and ready to use.

<span class="heading-section">🎯 Example Usage</span>

```js
wp.hooks.addAction('after.ready', 'wpshopify', function(lineItem, modVariant) {
   // Do something after add to cart ...
})
```
