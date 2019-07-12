# JavaScript Filters: Storefront

Please first read our [Getting started with JavaScript Hooks](guides/javascript-hooks.md) guide.

## `default.storefront.tags.heading`

Allows for changing the heading found within the "Tags" section of the Storefront component.

| Parameters  | Description                         |
| :---------- | :---------------------------------- |
| tagsHeading | Represents the current tags heading |

**Example**

```js
wp.hooks.addFilter('default.storefront.tags.heading', 'wpshopify', tagsHeading => {
   return 'New heading'
})
```

## `default.storefront.vendors.heading`

Allows for changing the heading found within the "Vendors" section of the Storefront component.

| Parameters     | Description                            |
| :------------- | :------------------------------------- |
| vendorsHeading | Represents the current vendors heading |

**Example**

```js
wp.hooks.addFilter('default.storefront.vendors.heading', 'wpshopify', vendorsHeading => {
   return 'New heading'
})
```

## `default.storefront.types.heading`

Allows for changing the heading found within the "Types" section of the Storefront component.

| Parameters   | Description                          |
| :----------- | :----------------------------------- |
| typesHeading | Represents the current types heading |

**Example**

```js
wp.hooks.addFilter('default.storefront.types.heading', 'wpshopify', defaultHeading => {
   return defaultHeading + ' new!'
})
```
