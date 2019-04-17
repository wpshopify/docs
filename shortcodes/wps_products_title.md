# [wps_products_title]

Displays the product "title" component.

## 🎯 Example Usage

```js
// Defaults to showing titles for the latest 10 products
[wps_products_title]

// Show titles for products with vendors "Apple"
[wps_products_title vendor="Apple"]

// Show titles for products with tags "tag-a", "tag-b", or "tag-c"
[wps_products_title tag="tag-a, tag-b, tag-c"]

```

## ⚡️ Available Attributes

### `title` <span class="attr-type attr-type-optional">(optional)</span>

Display title from product title(s).

Default: `false`

```js
[wps_products_title title="Product A, Product B"]
```

### `slug` <span class="attr-type attr-type-optional">(optional)</span>

Display title from product slug(s). Case insensitive.

Default: `false`

```js
[wps_products_title slug="product-a, product-b"]
```

### `tag` <span class="attr-type attr-type-optional">(optional)</span>

Display title from product tag(s).

Default: `false`

```js
[wps_products_title tag="tag-a, tab-b"]
```

### `vendor` <span class="attr-type attr-type-optional">(optional)</span>

Display title from product vendor(s).

Default: `false`

```js
[wps_products_title vendor="Apple, Microsoft"]
```

### `type` <span class="attr-type attr-type-optional">(optional)</span>

Display title from product type(s).

Default: `false`

```js
[wps_products_title type="Featured, Popular"]
```

### `description` <span class="attr-type attr-type-optional">(optional)</span>

Display title from product description. Performs a "wildcard" search based on the content you provide. For example, providing the value "Sale" will return products will the following descriptions:

"This product is on Sale until Tuesday!"<br>
"Sale ends tomorrow"

Default: `false`

```js
[wps_products_title description="This is from the product description ..."]
```

### `product_id` <span class="attr-type attr-type-optional">(optional)</span>

Display title from product id(s).

Default: `false`

```js
[wps_products_title product_id="19213874213, 93283473232"]
```

### `post_id` <span class="attr-type attr-type-optional">(optional)</span>

Display title from post id(s).

Default: `false`

```js
[wps_products_title post_id="3124, 9128"]
```

### `orderby` <span class="attr-type attr-type-optional">(optional)</span>

Determines the order criteria of the output of two or more titles. Only one value allowed.

Default: `title`

| Available Values |
| :--------------- |
| title            |
| updated_at       |
| created_at       |

```js
[wps_products_title orderby="title"]
```

### `order` <span class="attr-type attr-type-optional">(optional)</span>

Determines how to order the output of two or more titles. Only one value allowed.

Default: `desc`

| Available Values |
| :--------------- |
| asc              |
| desc             |

```js
// Smallest to largest (A to Z) (old to new)
[wps_products_title order="asc"]

// Largest to smallest (Z to A) (new to old)
[wps_products_title order="desc"]
```

### `limit` <span class="attr-type attr-type-optional">(optional)</span>

Allows for limiting the number of titles. Set to "false" to remove limit altogether.

Default: `10`

| Available Values |
| :--------------- |
| Any number       |
| false            |

```js
[wps_products_title limit="25"]

// Removes limit altogether
[wps_products_title limit="false"]
```

### `render_from_server` <span class="attr-type attr-type-optional">(optional)</span>

Determines whether to render the title on the client or server. [Learn more](/getting-started/displaying)

Default: `false`

| Available Values |
| :--------------- |
| true             |
| false            |

```js
[wps_products_title render_from_server="true"]
```
