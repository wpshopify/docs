# [wps_products]

Displays a list of products

## 🎯 Example Usage

```js
// Displays the cheapest 10 products
[wps_products sort_by="lowest_price" limit="10"]

// Displays products in rows of 5, sorted by best selling
[wps_products items_per_row="5" sort_by="best_selling"]

// Displays 20 products per page, sorted by title reversed as Z-A
[wps_products page_size="20" sort_by="title" reverse="true"]

```

## ⚡️ Available Attributes

### `title`

Displays products based on one or more product title(s). Default: `false`.

| Possible values:        |
| :---------------------- |
| Any valid product title |

```js
[wps_products title="Product A, Product B"]
```

### `tag`

Display products based on one or more product tag(s). Default: `false`.

| Possible values       |
| :-------------------- |
| Any valid product tag |

```js
[wps_products tag="Tag A, Tag B"]
```

### `vendor`

Display products based on one or more product vendor(s). Default: `false`.

| Possible                 |
| :----------------------- |
| Any valid product vendor |

```js
[wps_products vendor="Vendor A, Vendor B"]
```

### `product_type`

Display products based on one or more product type(s). Default: `false`

| Possible values:       |
| :--------------------- |
| Any valid product type |

```js
[wps_products product_type="Books"]
```

### `variants_price`

Display products based on the price of one or more variant(s). Default: `false`.

| Possible values:        |
| :---------------------- |
| Any valid variant price |

```js
[wps_products variants_price="10.00"]
```

### `available_for_sale`

Display products based on their availability. Setting `true` will only show products that are in stock. Settings `false` will only show products that are out of stock. Default: `false`.

| Possible values |
| :-------------- |
| true            |
| false           |

```js
[wps_products available_for_sale="true"]
```

### `created_at`

Display products based on the date it was created. Must use an [ISO 8601](https://en.wikipedia.org/wiki/ISO_8601) format. Default: `false`.

| Possible values:        |
| :---------------------- |
| Any valid ISO 8601 date |

```js
[wps_products created_at="2019-06-01T06:06:08-04"]
```

### `updated_at`

Display products based on the date it was updated. Must use an [ISO 8601](https://en.wikipedia.org/wiki/ISO_8601) format. Default: `false`.

| Possible values:        |
| :---------------------- |
| Any valid ISO 8601 date |

```js
[wps_products updated_at="2019-06-01T06:06:08-04"]
```

### `product_id`

Display products based on one or more product id(s). Default: `false`.

| Possible values:             |
| :--------------------------- |
| Any valid Shopify product id |

```js
[wps_products product_id="19213874213, 93283473232"]
```

### `post_id`

Display products based on one or more post id(s). Default: `false`.

| Possible values:            |
| :-------------------------- |
| Any valid WordPress post id |

```js
[wps_products post_id="3124, 9128"]
```

### `sort_by`

Determines the products sort order. Corresponds to the [Shopify API values](https://help.shopify.com/en/api/custom-storefronts/storefront-api/reference/enum/productsortkeys). Default: `title`.

| Possible values |
| :-------------- |
| title           |
| vendor          |
| id              |
| price           |
| best_selling    |
| product_type    |
| relevance       |
| created_at      |
| updated_at      |

```js
[wps_products sort_by="title"]
```

### `reverse`

Reverses the products order. Useful when used in combination with `sort_by`. Default: `false`.

| Possible values |
| :-------------- |
| true            |
| false           |

```js
// Smallest to largest (A to Z) (old to new)
[wps_products sort_by="title" reverse="true"]
```

### `page_size`

Determines the number of products to show per page. Only applicable when pagination is turned on. Default: `10`

| Possible values |
| :-------------- |
| Any number      |

```js
// Shows 4 products per page
[wps_products page_size="4"]
```

### `limit`

Limits the number of products that show. Max limit is `250`. Default: `10`.

| Possible values |
| :-------------- |
| Any number      |

```js
// Shows up to 25 products
[wps_products limit="25"]

// Only show one product
[wps_products limit="1"]
```

### `connective`

The "connective" attribute determines how the products are found when combining shortcode attributes. The two possible values are `AND` / `OR`. When set to `AND`, all shortcode attributes must match the products. With `OR`, any matched shortcode criteria will return the given products. Default: `AND`.

| Possible values |
| :-------------- |
| AND             |
| OR              |

```js
// Products with either title will show
[wps_products title="Awesome product, Even better product" connective="OR"]

// Only products with both Tag1 and Tag2 will show
[wps_products tag="Tag1, Tag2" connective="AND"]
```

### `button_color`

Determines the buy button color. Default: `#14273b`.

| Possible values     |
| :------------------ |
| Any valid CSS color |

```js
[wps_products button_color="#000"]
```

### `variant_color`

Determines the variant dropdown color. Default: `#52a7a6`.

| Possible values     |
| :------------------ |
| Any valid CSS color |

```js
[wps_products variant_color="#000"]
```

### `button_text`

Determines the buy button text. Default: `Add to cart`.

| Possible values |
| :-------------- |
| Any text string |

```js
[wps_products button_text="Add in bag"]
```

### `hide_quantity`

Determines whether to hide the quantity selection element Default: `false`.

| Possible values |
| :-------------- |
| true            |
| false           |

```js
[wps_products hide_quantity="true"]
```

### `min_quantity`

Sets a "minimum" number to the quantity field. The user will not be able to add _less than_ this number to the cart at any given time. Default: `false`.

```js
[wps_products min_quantity="4"]
```

### `max_quantity`

Sets a "maximum" number to the quantity field. The user will not be able to add _more than_ this number to the cart at any given time. Default: `false`.

```js
[wps_products max_quantity="20"]
```

### `show_quantity_label`

Determines whether to show or hide the "label" to the quantity selection element. Shows the word "Quantity" when turned on. Default: `true`.

| Possible values |
| :-------------- |
| true            |
| false           |

```js
[wps_products show_quantity_label="false"]
```

### `excludes`

Allows for excluding certain product components like the title, description, etc. Takes a comma separated string of values. Default: `false`.

| Possible values |
| :-------------- |
| images          |
| title           |
| pricing         |
| description     |
| buy-button      |

```js
[wps_products excludes="title, pricing"]
```

### `items_per_row`

Determines how many products will appear in each row. Default: `3`.

| Possible values |
| :-------------- |
| Any text string |

```js
[wps_products items_per_row="5"]
```

### `show_price_range`

Determines whether to show price ranges for each product. Only applicable when `pricing` is not set within the `excludes` attribute. Default: `false`.

| Possible values |
| :-------------- |
| true            |
| false           |

```js
[wps_products show_price_range="true"]
```

### `show_compare_at`

Determines whether to show the compare at price for each product. Only applicable when `pricing` is not set within the `excludes` attribute. Default: `false`.

| Possible values |
| :-------------- |
| true            |
| false           |

```js
[wps_products show_compare_at="true"]
```

### `quantity_label_text`

Allows for customizing the label text next to the quantity field. Default: `Quantity`.

| Possible values |
| :-------------- |
| Any text string |

```js
[wps_products quantity_label_text="Custom quantity text"]
```

### `show_featured_only`

Determines whether to show only the feature image. By default, all product images will show as thumbnails below the featured image. Default: `false`.

| Possible values |
| :-------------- |
| true            |
| false           |

```js
[wps_products show_featured_only="true"]
```

### `show_zoom` <span class="attr-type attr-type-pro-only">(Pro only)</span>

Determines whether to enable product image zooming. When enabled, zoom will be triggered on the featured image. Only available in [WP Shopify Pro](/getting-started/wp-shopify-pro.md). Default: `false`.

| Possible values |
| :-------------- |
| true            |
| false           |

```js
[wps_products show_zoom="true"]
```

### `pagination`

Determines whether to hide or show pagination. Default: `true`.

| Possible values |
| :-------------- |
| true            |
| false           |

```js
[wps_products pagination="false"]
```

### `dropzone_pagination`

When `pagination` is set to true, this allows for specifying a custom location in the DOM to place the overall pagination component. Takes any valid CSS selector. When set to false, the pagination component will be placed directly below the products output. Default: `false`.

> [!NOTE|className:info sm]
> The HTML element specified will be completely emptied and replaced with the pagination.

```js
[wps_products dropzone_pagination="#my-custom-pagination-container"]
```

### `dropzone_page_size`

When `pagination` is set to true, this allows for specifying a custom location in the DOM to place the pagination "page size" controls component. Takes any valid CSS selector. When set to false, the page size controls will be placed directly below the products output. Default: `false`.

> [!NOTE|className:info sm]
> The HTML element specified will be completely emptied and replaced with the page size component.

```js
[wps_products dropzone_page_size="#my-custom-page-size-container"]
```

### `dropzone_load_more`

When `pagination` is set to true, this allows for specifying a custom location in the DOM to place the pagination "load more" control component. Takes any valid CSS selector. When set to false, the load more button will be placed directly below the products output. Default: `false`.

> [!NOTE|className:info sm]
> The HTML element specified will be completely emptied and replaced with the load more component.

```js
[wps_products dropzone_load_more="#my-custom-load-more-container"]
```

### `render_from_server`

Determines whether to render the title on the client or server. Must have lite sync disabled. [Learn more](/getting-started/displaying). Default: `false`

| Possible values |
| :-------------- |
| true            |
| false           |

```js
[wps_products render_from_server="true"]
```
