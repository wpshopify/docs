# [wps_collections]

Displays a list of collections

## 🎯 Example Usage

```js
// Display the cheapest 10 products
[wps_collections sort_by="lowest_price" limit="10"]

```

## ⚡️ Available Attributes

### `sort_by` <span class="attr-type attr-type-optional">(optional)</span>

Determines the sort order of the output of two or more titles. Only one value allowed.

Default: `title`

| Available Values |
| :--------------- |
| title            |
| updated_at       |
| created_at       |
| best_selling     |
| highest_price    |
| lowest_price     |
| newest           |
| oldest           |
| manually         |

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

| Available Values |
| :--------------- |
| Any number       |

```js
// Shows up to 250 at any time
[wps_collections_title limit="25"]

// Only show one
[wps_collections_title limit="1"]
```
