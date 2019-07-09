# [wps_products_pricing]

Displays the product "pricing" component.<br><br>Watch our [quick video tutorial](https://www.youtube.com/watch?v=lYm6G35e8sI) to learn how to use this.

<span class="heading-section">📍 Example Usage</span>

```js
// Defaults to showing pricing for the latest 10 products
[wps_products_pricing]

// Show pricing for products with vendors "Apple"
[wps_products_pricing vendor="Apple"]

// Show pricing for product with title "Product A". Also show compare at prices.
[wps_products_pricing title="Product A" show_compare_at="true"]

```

<span class="heading-section">🎚 Available Attributes</span>

## `title`

Displays products based on one or more product title(s).

| Possible values                 |
| :------------------------------ |
| Any valid Shopify product title |

**Example**

```js
[wps_products_pricing title="Product A, Product B"]
```

## `tag`

Display products based on one or more product tag(s).

| Possible values       |
| :-------------------- |
| Any valid product tag |

**Example**

```js
[wps_products_pricing tag="Tag A, Tag B"]
```

## `vendor`

Display products based on one or more product vendor(s).

| Possible                 |
| :----------------------- |
| Any valid product vendor |

**Example**

```js
[wps_products_pricing vendor="Vendor A, Vendor B"]
```

## `product_type`

Display products based on one or more product type(s).

| Possible values        |
| :--------------------- |
| Any valid product type |

**Example**

```js
[wps_products_pricing product_type="Books"]
```

## `available_for_sale`

Display products based on their availability. Setting to `available` will only show products that are in stock. Setting to `unavailable` will only show products that are _out_ of stock. Setting to `any` will show both.

| Possible values |
| :-------------- |
| available       |
| unavailable     |
| any (default)   |

**Example**

```js
[wps_products_pricing available_for_sale="available"]
```

## `created_at`

Display products based on the date it was created. Must use an [ISO 8601](https://en.wikipedia.org/wiki/ISO_8601) format. Example can be [found based on orders](https://help.shopify.com/en/api/reference/orders/order#created-at-property-2019-07).

| Possible values         |
| :---------------------- |
| Any valid ISO 8601 date |

**Example**

```js
[wps_products_pricing created_at="2019-02-21 03:16:41"]
```

## `updated_at`

Display products based on the date it was updated. Must use an [ISO 8601](https://en.wikipedia.org/wiki/ISO_8601) format. Default: `false`. Example can be [found based on orders](https://help.shopify.com/en/api/reference/orders/order#created-at-property-2019-07).

| Possible values         |
| :---------------------- |
| Any valid ISO 8601 date |

**Example**

```js
[wps_products_pricing updated_at="2019-02-21 03:16:41"]
```

## `product_id`

Display products based on one or more Shopify product id(s).

Note: this id is different from the GraphQL id that looks like this:

`Z2lkOi8vc2hvcGlmeS9Qcm9kdWN0LzIyMTY5Mjg0MTE2OTY=`

You can base64 decode the above value and get a string such as `gid://shopify/Product/2216928411696`. The end of which represents the Shopify product id.

| Possible values              |
| :--------------------------- |
| Any valid Shopify product id |

**Example**

```js
[wps_products_pricing product_id="2216928411696, 93283473232"]
```

## `sort_by`

Determines the products sort order. Corresponds to the [Shopify API values](https://help.shopify.com/en/api/custom-storefronts/storefront-api/reference/enum/productsortkeys).

| Possible values |
| :-------------- |
| title (default) |
| vendor          |
| id              |
| price           |
| best_selling    |
| product_type    |
| created_at      |
| updated_at      |

**Example**

```js
[wps_products_pricing sort_by="price"]
```

## `reverse`

Reverses the order of products. Useful when used in combination with `sort_by`.

| Possible values |
| :-------------- |
| true            |
| false           |

**Example**

```js
// Smallest to largest (A to Z) (old to new)
[wps_products_pricing sort_by="title" reverse="true"]
```

## `page_size`

Determines the number of products to show per page. Only applicable when pagination is turned on. Will default to the plugin's global [products per page](getting-started/settings?id=products-per-page) setting.

| Possible values |
| :-------------- |
| Any number      |

**Example**

```js
// Shows 4 products per page
[wps_products_pricing page_size="4"]
```

## `limit`

Limits the overall number of products that show. Max limit is `250`.

| Possible values |
| :-------------- |
| Any number      |

**Example**

```js
// Show two products per page, up to 10
[wps_products_pricing page_size="2" limit="10"]

// Only show one product
[wps_products_pricing limit="1"]
```

## `connective`

The "connective" attribute determines how the products are found when combining _other_ shortcode attributes. For example when set to `and`, every provided attribute must match the searched products. With `or`, _any_ provided attribute will return the matched products. Default: `or`.

| Possible values |
| :-------------- |
| and             |
| or              |

**Example**

```js
// Products with either title will show
[wps_products_pricing title="Awesome product, Even better product" connective="or"]

// Only products with both Tag1 and Tag2 will show
[wps_products_pricing tag="Tag1, Tag2" connective="and"]
```

## `items_per_row`

Determines how many products will appear in each row.

| Possible values |
| :-------------- |
| Any text string |

**Example**

```js
[wps_products_pricing items_per_row="5"]
```

## `show_price_range`

Determines whether to show price ranges. Only applicable when `pricing` is not set within the [excludes](#excludes) attribute.

| Possible values |
| :-------------- |
| true            |
| false           |

**Example**

```js
[wps_products_pricing show_price_range="true"]
```

## `show_compare_at`

Determines whether to show the compare at price. Only applicable when `pricing` is not set within the [excludes](#excludes) attribute.

| Possible values |
| :-------------- |
| true            |
| false           |

**Example**

```js
[wps_products_pricing show_compare_at="true"]
```

## `pagination`

Determines whether to hide or show pagination.

| Possible values |
| :-------------- |
| true            |
| false           |

**Example**

```js
[wps_products_pricing pagination="false"]
```

## `no_results_text`

The text to show when no products are found.

| Possible values |
| :-------------- |
| Any text string |

**Example**

```js
[wps_products_pricing no_results_text="Nothing found! 🙃"]
```

## `infinite_scroll`

When turned on, the next page of items will automatically append to the container. Only works when pagination is used.

| Possible values |
| :-------------- |
| true            |
| false           |

**Example**

```js
[wps_products_pricing infinite_scroll="true"]
```

## `infinite_scroll_offset`

Determines the offset from the edge of the items container. For example, a value of `-100` will begin loading additional items 100px before the end of the items container. Offset can be a positive or negative value.

| Possible values                 |
| :------------------------------ |
| Any positive or negative number |

**Example**

```js
[wps_products_pricing infinite_scroll_offset="-100"]
```

## `dropzone_load_more`

When `pagination` is set to true, this allows for specifying a custom location in the DOM to place the pagination "load more" control component. Takes any valid CSS selector. When set to false, the load more button will be placed directly below the products output. Default: `false`.

> [!NOTE|className:info sm]
> The HTML element specified will be completely emptied and replaced with the load more component.

**Example**

```js
[wps_products_pricing dropzone_load_more="#my-custom-load-more-container"]
```
