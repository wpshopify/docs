# [wps_products_pricing]

Displays the product "pricing" component.

## 🎯 Example Usage

```js
// Defaults to showing pricing for the latest 10 products
[wps_products_pricing]

// Show pricing for products with vendors "Apple"
[wps_products_pricing vendor="Apple"]

// Show pricing for product with title "Product A". Also show compare at prices.
[wps_products_pricing title="Product A" show_compare_at="true"]

```

## ⚡️ Available Attributes

### `title`

Display pricing from product title(s).

Default: `false`

```js
[wps_products_pricing title="Product A, Product B"]
```

### `slug`

Display pricing from product slug(s). Case insensitive.

Default: `false`

```js
[wps_products_pricing slug="product-a, product-b"]
```

### `tag`

Display pricing from product tag(s).

Default: `false`

```js
[wps_products_pricing tag="tag-a, tab-b"]
```

### `vendor`

Display pricing from product vendor(s).

Default: `false`

```js
[wps_products_pricing vendor="Apple, Microsoft"]
```

### `type`

Display pricing from product type(s).

Default: `false`

```js
[wps_products_pricing type="Featured, Popular"]
```

### `description`

Display pricing from product description. Performs a "wildcard" search based on the content you provide. For example, providing the value "Sale" will return products will the following descriptions:

"This product is on Sale until Tuesday!"<br>
"Sale ends tomorrow"

Default: `false`

```js
[wps_products_pricing description="This is from the product description ..."]
```

### `product_id`

Display pricing from product id(s).

Default: `false`

```js
[wps_products_pricing product_id="19213874213, 93283473232"]
```

### `post_id`

Display pricing from post id(s).

Default: `false`

```js
[wps_products_pricing post_id="3124, 9128"]
```

### `orderby`

Determines the order criteria of the output of two or more descriptions. Only one value allowed.

Default: `title`

| Available Values |
| :--------------- |
| title            |
| updated_at       |
| created_at       |

```js
[wps_products_pricing orderby="title"]
```

### `order`

Determines how to order the output of two or more descriptions. Only one value allowed.

Default: `desc`

| Available Values |
| :--------------- |
| asc              |
| desc             |

```js
// Smallest to largest (A to Z) (old to new)
[wps_products_pricing order="asc"]

// Largest to smallest (Z to A) (new to old)
[wps_products_pricing order="desc"]
```

### `limit`

Allows for limiting the number of descriptions. Set to "false" to remove limit altogether.

Default: `10`

| Available Values |
| :--------------- |
| Any number       |
| false            |

```js
[wps_products_pricing limit="25"]

// Removes limit altogether
[wps_products_pricing limit="false"]
```

### `render_from_server`

Determines whether to render the description on the client or server. [Learn more](/getting-started/displaying)

Default: `false`

| Available Values |
| :--------------- |
| true             |
| false            |

```js
[wps_products_pricing render_from_server="true"]
```

### `show_price_range`

Determines whether to show price ranges. The variant order will not be taken into consideration. Instead, prices will be sorted from smallest to largest to create the necessary range.

Default: `false`

| Available Values |
| :--------------- |
| true             |
| false            |

```js
[wps_products_pricing show_price_range="true"]
```

### `show_compare_at`

Determines whether to show the "compare at" prices. Will _not_ show when compare at price is either: A) The same as the normal price or B) Is empty.

Default: `false`

| Available Values |
| :--------------- |
| true             |
| false            |

```js
[wps_products_pricing show_compare_at="true"]
```

### `show_local`

Determines whether to show prices in the users local currency. [Learn more](/getting-started/displaying)

Default: `false`

| Available Values |
| :--------------- |
| true             |
| false            |

```js
[wps_products_pricing show_local="true"]
```
