# Storefront JavaScript Filters

You may want to read our [Getting started with JavaScript Hooks](guides/javascript-hooks.md) guide first.

## `default.storefront.tags.heading`

Allows for changing the heading found within the "Tags" section of the Storefront component.

| Parameters  | Description                                          |
| :---------- | :--------------------------------------------------- |
| tagsHeading | Represents the default tags heading. Default: `Tags` |

**Example**

```js
wp.hooks.addFilter('default.storefront.tags.heading', 'wpshopify', function (tagsHeading) {
  return 'New heading'
})
```

## `default.storefront.vendors.heading`

Allows for changing the heading found within the "Vendors" section of the Storefront component.

| Parameters     | Description                                                |
| :------------- | :--------------------------------------------------------- |
| vendorsHeading | Represents the default vendors heading. Default: `Vendors` |

**Example**

```js
wp.hooks.addFilter('default.storefront.vendors.heading', 'wpshopify', function (vendorsHeading) {
  return 'New heading'
})
```

## `default.storefront.types.heading`

Allows for changing the heading found within the "Types" section of the Storefront component.

| Parameters   | Description                                            |
| :----------- | :----------------------------------------------------- |
| typesHeading | Represents the default types heading. Default: `Types` |

**Example**

```js
wp.hooks.addFilter('default.storefront.types.heading', 'wpshopify', function (defaultHeading) {
  return 'New heading'
})
```

## `storefront.group.loading.text`

Allows for customizing the loading text of each group of filters

| Parameters         | Description                         |
| :----------------- | :---------------------------------- |
| defaultLoadingText | Represents the default loading text |

**Example**

```js
wp.hooks.addFilter('storefront.group.loading.text', 'wpshopify', function (defaultLoadingText) {
  return '<p>Custom loading ...</p>'
})
```

## `storefront.selections.filter.label`

Allows for customizing the label text of the Storefront filter dropdown

| Parameters         | Description                                                        |
| :----------------- | :----------------------------------------------------------------- |
| defaultFilterLabel | Represents the default filter dropdown label. Default: `Filter by` |

**Example**

```js
wp.hooks.addFilter('storefront.selections.filter.label', 'wpshopify', function (
  defaultFilterLabel
) {
  return 'Custom filter text'
})
```

## `storefront.selections.clear.text`

Allows for customizing the "clear selections" text.

| Parameters       | Description                                                        |
| :--------------- | :----------------------------------------------------------------- |
| defaultClearText | Represents the default clear selections text. Default: `Clear all` |

**Example**

```js
wp.hooks.addFilter('storefront.selections.clear.text', 'wpshopify', function (defaultClearText) {
  return 'Custom clear text'
})
```

## `storefront.selections.type.text`

Allows for customizing the label text next to the selections.

| Parameters   | Description                                              |
| :----------- | :------------------------------------------------------- |
| defaultLabel | Represents the default label text next to the selections |

**Example**

```js
wp.hooks.addFilter('storefront.selections.type.text', 'wpshopify', function (defaultText) {
  return 'Custom text'
})
```

## `storefront.selections.available.text`

Allows for customizing the label text for availablity selections

| Parameters   | Description                                                                                 |
| :----------- | :------------------------------------------------------------------------------------------ |
| defaultLabel | Represents the default label text for availablity selections. Default: `Available for sale` |

**Example**

```js
wp.hooks.addFilter('storefront.selections.available.text', 'wpshopify', function (defaultLabel) {
  return 'Custom label'
})
```

## `storefront.sorting.label.text`

Allows for customizing the storefront sorting label text

| Parameters   | Description                                                    |
| :----------- | :------------------------------------------------------------- |
| defaultLabel | Represents the default sorting label text. Default: `Sort by:` |

**Example**

```js
wp.hooks.addFilter('storefront.sorting.label.text', 'wpshopify', function (defaultLabel) {
  return 'Custom label'
})
```

## `storefront.sorting.default.text`

Allows for customizing the default sorting text.

| Parameters  | Description                                                       |
| :---------- | :---------------------------------------------------------------- |
| defaultText | Represents the default sorting text. Default: `Choose an option:` |

**Example**

```js
wp.hooks.addFilter('storefront.sorting.default.text', 'wpshopify', function (defaultText) {
  return 'Custom text'
})
```

## `storefront.sorting.price.text`

Allows for customizing the default sort by price text.

| Parameters  | Description                                                               |
| :---------- | :------------------------------------------------------------------------ |
| defaultText | Represents the default sort by price text. Default: `Price (Low to high)` |

**Example**

```js
wp.hooks.addFilter('storefront.sorting.price.text', 'wpshopify', function (defaultText) {
  return 'Custom text'
})
```

## `storefront.sorting.priceReverse.text`

Allows for customizing the default sort by price reverse text.

| Parameters  | Description                                                                       |
| :---------- | :-------------------------------------------------------------------------------- |
| defaultText | Represents the default sort by price reverse text. Default: `Price (High to low)` |

**Example**

```js
wp.hooks.addFilter('storefront.sorting.priceReverse.text', 'wpshopify', function (defaultText) {
  return 'Custom text'
})
```

## `storefront.sorting.newArrival.text`

Allows for customizing the default sort by new arrival text.

| Parameters  | Description                                                             |
| :---------- | :---------------------------------------------------------------------- |
| defaultText | Represents the default sort by new arrival text. Default: `New Arrival` |

**Example**

```js
wp.hooks.addFilter('storefront.sorting.newArrival.text', 'wpshopify', function (defaultText) {
  return 'Custom text'
})
```

## `storefront.sorting.bestSelling.text`

Allows for customizing the default sort by best selling.

| Parameters  | Description                                                          |
| :---------- | :------------------------------------------------------------------- |
| defaultText | Represents the default sort by best selling. Default: `Best Selling` |

**Example**

```js
wp.hooks.addFilter('storefront.sorting.bestSelling.text', 'wpshopify', function (defaultText) {
  return 'Custom text'
})
```

## `storefront.sorting.title.text`

Allows for customizing the default sort by title text.

| Parameters  | Description                                                       |
| :---------- | :---------------------------------------------------------------- |
| defaultText | Represents the default sort by title text. Default: `Title (A-Z)` |

**Example**

```js
wp.hooks.addFilter('storefront.sorting.bestSelling.text', 'wpshopify', function (defaultText) {
  return 'Custom text'
})
```

## `storefront.sorting.titleReverse.text`

Allows for customizing the default sort by title reverse text.

| Parameters  | Description                                                               |
| :---------- | :------------------------------------------------------------------------ |
| defaultText | Represents the default sort by title reverse text. Default: `Title (Z-A)` |

**Example**

```js
wp.hooks.addFilter('storefront.sorting.titleReverse.text', 'wpshopify', function (defaultText) {
  return 'Custom text'
})
```
