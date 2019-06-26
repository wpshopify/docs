# [wps_collections]

Displays a list of collections

## 🎯 Examples

```js
// Display the cheapest 10 products
[wps_collections sort_by="lowest_price" limit="10"]

```

## ⚡️ Attributes

### `sort_by` <span class="attr-type attr-type-optional">(optional)</span>

Determines the collections sort order. Corresponds to the [Shopify Storefront API](https://help.shopify.com/en/api/storefront-api/reference/enum/collectionsortkeys). Default: `title`

| Values     |
| :--------- |
| title      |
| updated_at |

```js
[wps_collections_title sort_by="title"]
```

### `reverse` <span class="attr-type attr-type-optional">(optional)</span>

Reverses the order that the products are displayed in

Default: `false`

```js

// Smallest to largest (A to Z) (old to new)
[wps_collections_title sort_by="title" reverse="true"]

```

### `limit` <span class="attr-type attr-type-optional">(optional)</span>

Limits the number of titles. Max allowed is `250`.

Default: `10`

| Values     |
| :--------- |
| Any number |

```js
// Shows up to 250 at any time
[wps_collections_title limit="25"]

// Only show one
[wps_collections_title limit="1"]
```

### `products_sort_by` <span class="attr-type attr-type-optional">(optional)</span>

Determines the products sort order within a collection. Corresponds to the [Shopify Storefront API](https://help.shopify.com/en/api/storefront-api/reference/enum/productcollectionsortkeys). Default: `title`

| Values             |
| :----------------- |
| title              |
| collection_default |
| created            |
| id                 |
| manual             |
| price              |
| relevance          |
| best_selling       |

```js
[wps_collections_title products_sort_by="price"]
```
