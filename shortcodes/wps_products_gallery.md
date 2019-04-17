# [wps_products_gallery]

Displays the product "gallery" component.

## 🎯 Example Usage

```js
// Defaults to showing galleries for the latest 10 products
[wps_products_gallery]

// Show galleries for products with titles "Product A" and Product B"
[wps_products_gallery title="Product A, Product B"]

// Show galleries for products of type "Sale". Don't show image zoom or gallery thumbs
[wps_products_gallery type="Sale" show_featured_only="true" show_zoom="false"]

```

## ⚡️ Available Attributes

### `title` <span class="attr-type attr-type-optional">(optional)</span>

Display gallery from product title(s).

Default: `false`

```js
[wps_products_gallery title="Product A, Product B"]
```

### `slug` <span class="attr-type attr-type-optional">(optional)</span>

Display gallery from product slug(s). Case insensitive.

Default: `false`

```js
[wps_products_gallery slug="product-a, product-b"]
```

### `tag` <span class="attr-type attr-type-optional">(optional)</span>

Display gallery from product tag(s).

Default: `false`

```js
[wps_products_gallery tag="tag-a, tab-b"]
```

### `vendor` <span class="attr-type attr-type-optional">(optional)</span>

Display gallery from product vendor(s).

Default: `false`

```js
[wps_products_gallery vendor="Apple, Microsoft"]
```

### `type` <span class="attr-type attr-type-optional">(optional)</span>

Display gallery from product type(s).

Default: `false`

```js
[wps_products_gallery type="Featured, Popular"]
```

### `description` <span class="attr-type attr-type-optional">(optional)</span>

Display gallery from product description. Performs a "wildcard" search based on the content you provide. For example, providing the value "Sale" will return products will the following descriptions:

"This product is on Sale until Tuesday!"<br>
"Sale ends tomorrow"

Default: `false`

```js
[wps_products_gallery description="This is from the product description ..."]
```

### `product_id` <span class="attr-type attr-type-optional">(optional)</span>

Display gallery from product id(s).

Default: `false`

```js
[wps_products_gallery product_id="19213874213, 93283473232"]
```

### `post_id` <span class="attr-type attr-type-optional">(optional)</span>

Display gallery from post id(s).

Default: `false`

```js
[wps_products_gallery post_id="3124, 9128"]
```

### `orderby` <span class="attr-type attr-type-optional">(optional)</span>

Determines the order criteria of the output of two or more galleries. Only one value allowed.

Default: `title`

| Available Values |
| :--------------- |
| title            |
| updated_at       |
| created_at       |

```js
[wps_products_gallery orderby="title"]
```

### `order` <span class="attr-type attr-type-optional">(optional)</span>

Determines how to order the output of two or more galleries. Only one value allowed.

Default: `desc`

| Available Values |
| :--------------- |
| asc              |
| desc             |

```js
// Smallest to largest (A to Z) (old to new)
[wps_products_gallery order="asc"]

// Largest to smallest (Z to A) (new to old)
[wps_products_gallery order="desc"]
```

### `limit` <span class="attr-type attr-type-optional">(optional)</span>

Allows for limiting the number of galleries. Set to "false" to remove limit altogether.

Default: `10`

| Available Values |
| :--------------- |
| Any number       |
| false            |

```js
[wps_products_gallery limit="25"]

// Removes limit altogether
[wps_products_gallery limit="false"]
```

### `render_from_server` <span class="attr-type attr-type-optional">(optional)</span>

Determines whether to render the gallery on the client or server. [Learn more](/getting-started/displaying)

Default: `false`

| Available Values |
| :--------------- |
| true             |
| false            |

```js
[wps_products_gallery render_from_server="true"]
```

### `show_featured_only` <span class="attr-type attr-type-optional">(optional)</span>

Determines whether to show only the feature image. By default, all product images will show as thumbnails below the featured image.

Default: `false`

| Available Values |
| :--------------- |
| true             |
| false            |

```js
[wps_products_gallery show_featured_only="true"]
```

### `show_zoom` <span class="attr-type attr-type-pro-only">(Pro only)</span>

Determines whether to enable product image zooming. When enabled, zoom will be triggered on the featured image. Only available in [WP Shopify Pro](/getting-started/wp-shopify-pro.md).

Default: `false`

| Available Values |
| :--------------- |
| true             |
| false            |

```js
[wps_products_gallery show_zoom="true"]
```
