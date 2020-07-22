# Storefront JavaScript Filters

You may want to read our [Getting started with JavaScript Hooks](guides/javascript-hooks.md) guide first.

## `default.storefront.tags.heading`

Allows for changing the heading found within the "Tags" section of the Storefront component.

| Parameters  | Description                         |
| :---------- | :---------------------------------- |
| tagsHeading | Represents the current tags heading |

**Example**

```js
wp.hooks.addFilter('default.storefront.tags.heading', 'wpshopify', function (tagsHeading) {
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
wp.hooks.addFilter('default.storefront.vendors.heading', 'wpshopify', function (vendorsHeading) {
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
wp.hooks.addFilter('default.storefront.types.heading', 'wpshopify', function (defaultHeading) {
  return defaultHeading + ' new!'
})
```

## `storefront.filter.text`

## `storefront.group.loading.text`

## `storefront.selections.filter.label`

## `storefront.selections.clear.text`

## `storefront.selections.type.text`

## `storefront.selections.available.text`

## `storefront.sorting.label.text`

## `storefront.sorting.default.text`

## `storefront.sorting.price.text`

## `storefront.sorting.priceReverse.text`

## `storefront.sorting.newArrival.text`

## `storefront.sorting.bestSelling.text`

## `storefront.sorting.title.text`

## `storefront.sorting.titleReverse.text`

## `default.storefront.tags.heading`

## `default.storefront.types.heading`

## `default.storefront.vendors.heading`
