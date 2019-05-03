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

### `title` <span class="attr-type attr-type-optional">(optional)</span>

Display description from product title(s).

Default: `false`

```js
[wps_products_description title="Product A, Product B"]
```

### `slug` <span class="attr-type attr-type-optional">(optional)</span>

Display description from product slug(s). Case insensitive.

Default: `false`

```js
[wps_products_description slug="product-a, product-b"]
```

### `tag` <span class="attr-type attr-type-optional">(optional)</span>

Display description from product tag(s).

Default: `false`

```js
[wps_products_description tag="tag-a, tab-b"]
```

### `vendor` <span class="attr-type attr-type-optional">(optional)</span>

Display description from product vendor(s).

Default: `false`

```js
[wps_products_description vendor="Apple, Microsoft"]
```

### `type` <span class="attr-type attr-type-optional">(optional)</span>

Display description from product type(s).

Default: `false`

```js
[wps_products_description type="Featured, Popular"]
```

### `description` <span class="attr-type attr-type-optional">(optional)</span>

Display description from product description. Performs a "wildcard" search based on the content you provide. For example, providing the value "Sale" will return products will the following descriptions:

"This product is on Sale until Tuesday!"<br>
"Sale ends tomorrow"

Default: `false`

```js
[wps_products_description description="This is from the product description ..."]
```

### `product_id` <span class="attr-type attr-type-optional">(optional)</span>

Display description from product id(s).

Default: `false`

```js
[wps_products_description product_id="19213874213, 93283473232"]
```

### `post_id` <span class="attr-type attr-type-optional">(optional)</span>

Display description from post id(s).

Default: `false`

```js
[wps_products_description post_id="3124, 9128"]
```

### `orderby` <span class="attr-type attr-type-optional">(optional)</span>

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

### `order` <span class="attr-type attr-type-optional">(optional)</span>

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

### `limit` <span class="attr-type attr-type-optional">(optional)</span>

Limits the number of titles. Max allowed is `250`.

Default: `10`

| Available Values |
| :--------------- |
| Any number       |

```js
// Shows up to 250 at any time
[wps_products_title limit="25"]

// Only show one
[wps_products_title limit="1"]
```

### `render_from_server` <span class="attr-type attr-type-optional">(optional)</span>

Determines whether to render the description on the client or server. [Learn more](/getting-started/displaying)

Default: `false`

| Available Values |
| :--------------- |
| true             |
| false            |

```js
[wps_products_description render_from_server="true"]
```
