# [wps_products_gallery]

Displays the product "gallery "component of one or more products.

## 🎯 Example Usage

```js
// Defaults to showing gallery for the latest 10 products
[wps_products_gallery]

// Show gallery from products with titles "Product A" and Product B"
[wps_products_gallery title="Product A, Product B"]

// Show gallery from products of type "Sale". Don't show image zoom or gallery thumbnails.
[wps_products_gallery type="Sale" show_featured_only="true" show_zoom="false"]

```

## ⚡️ Attributes

### `title`

Display gallery component from product title(s).

Default: `false`

```js
[wps_products_gallery title="Product A, Product B"]
```

### `slug`

Display gallery component from product slug(s). Case insensitive.

Default: `false`

```js
[wps_products_gallery slug="product-a, product-b"]
```

### `tag`

Display gallery component from product tag(s).

Default: `false`

```js
[wps_products_gallery tag="tag-a, tab-b"]
```

### `vendor`

Display gallery component from product vendor(s).

Default: `false`

```js
[wps_products_gallery vendor="Apple, Microsoft"]
```

### `type`

Display gallery component from product type(s).

Default: `false`

```js
[wps_products_gallery type="Featured, Popular"]
```

### `description`

Display gallery component from product description

Default: `false`

```js
[wps_products_gallery description="This is from the product description ..."]
```

### `product_id`

Display gallery component from product id(s).

Default: `false`

```js
[wps_products_gallery product_id="19213874213, 93283473232"]
```

### `post_id`

Display gallery component from post id(s).

Default: `false`

```js
[wps_products_gallery post_id="3124, 9128"]
```

### `orderby`

Determines the order criteria of the output of two or more galleries. Only one value allowed.

Default: `title`

| Available Values |
| :--------------- |
| title            |
| updated          |
| created          |

```js
[wps_products_gallery orderby="title"]
```

### `order`

Determines how to order the output of two or more galleries. Only one value allowed.

Default: `desc`

| Available Values |
| :--------------- |
| asc              |
| desc             |

```js
[wps_products_gallery order="asc"]
```

### `limit`

Allows for limiting the output to a certain number of items.

Default: `10`

```js
[wps_products_gallery limit="25"]
```

### `render_from_server`

Determines whether to render the gallery on the client or server. [Learn more](/getting-started/displaying)

Default: `false`

```js
[wps_products_gallery render_from_server="true"]
```

### `show_featured_only`

Determines whether to show only the feature image. By default, all product images will show as thumbnails below the featured image.

Default: `false`

```js
[wps_products_gallery show_featured_only="true"]
```

### `show_zoom` <span class="pro-only">(Pro only)</span>

Determines whether to enable product image zooming. When enabled, zoom will be triggered on the featured image. Only available in [WP Shopify Pro](/getting-started/wp-shopify-pro.md).

Default: `false`

```js
[wps_products_gallery show_zoom="true"]
```
