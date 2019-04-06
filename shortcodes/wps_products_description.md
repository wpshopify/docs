# [wps_products_description]

Displays the product "description" component.

## 🎯 Example Usage

```js
// Defaults to showing descriptions for the latest 10 products
[wps_products_description]

// Show descriptions for products with vendors "Apple"
[wps_products_description vendor="Apple"]

// Show descriptions for products with tags "tag-a", "tag-b", or "tag-c"
[wps_products_description tag="tag-a, tag-b, tag-c"]

```

## ⚡️ Available Attributes

### `title`

Display description from product title(s).

Default: `false`

```js
[wps_products_description title="Product A, Product B"]
```

### `slug`

Display description from product slug(s). Case insensitive.

Default: `false`

```js
[wps_products_description slug="product-a, product-b"]
```

### `tag`

Display description from product tag(s).

Default: `false`

```js
[wps_products_description tag="tag-a, tab-b"]
```

### `vendor`

Display description from product vendor(s).

Default: `false`

```js
[wps_products_description vendor="Apple, Microsoft"]
```

### `type`

Display description from product type(s).

Default: `false`

```js
[wps_products_description type="Featured, Popular"]
```

### `description`

Display description from product description. Performs a "wildcard" search based on the content you provide. For example, providing the value "Sale" will return products will the following descriptions:

"This product is on Sale until Tuesday!"<br>
"Sale ends tomorrow"

Default: `false`

```js
[wps_products_description description="This is from the product description ..."]
```

### `product_id`

Display description from product id(s).

Default: `false`

```js
[wps_products_description product_id="19213874213, 93283473232"]
```

### `post_id`

Display description from post id(s).

Default: `false`

```js
[wps_products_description post_id="3124, 9128"]
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
[wps_products_description orderby="title"]
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
[wps_products_description order="asc"]

// Largest to smallest (Z to A) (new to old)
[wps_products_description order="desc"]
```

### `limit`

Allows for limiting the number of descriptions. Set to "false" to remove limit altogether.

Default: `10`

| Available Values |
| :--------------- |
| Any number       |
| false            |

```js
[wps_products_description limit="25"]

// Removes limit altogether
[wps_products_description limit="false"]
```

### `render_from_server`

Determines whether to render the description on the client or server. [Learn more](/getting-started/displaying)

Default: `false`

| Available Values |
| :--------------- |
| true             |
| false            |

```js
[wps_products_description render_from_server="true"]
```
