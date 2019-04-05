# [wps_products_title]

Displays the product "title "component of one or more products.

## 🎯 Example Usage

```js
// Simple usage to show all products
[wps_products_title]

// Show products from collections "Featured" and "Sale". Limit to 10.
[wps_products_title title="Product A, Product B"]

// Show products belonging to certain tags and ordered by price.
[wps_products_title type="Sale" limit="10"]

// Products that contain the words "Limited offer" in the product description.
[wps_products_title description="Limited offer"]
```

## ⚡️ Attributes

### `title`

Allows for filtering products that contain specific titles. Multiple values must be comma separated.

```js
[wps_products_title title="Product A, Product B"]
```

### `vendor`

Allows for filtering products that belong to certain vendors. Multiple values must be comma separated.

```js
[wps_products_title vendor="Apple, Microsoft"]
```

### `description`

### `type`

### `slug`

### `tag`

### `product_id`

### `post_id`

### `render_from_server`
