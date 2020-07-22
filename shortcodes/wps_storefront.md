# [wps_storefront]

Displays the "storefront" component containing filtering, pagination, and sorting. Only available in [WP Shopify Pro](https://wpshop.io/purchase/). Take note that this shortcode contains three required attributes.<br><br>Watch our [quick video tutorial](https://www.youtube.com/watch?v=lYm6G35e8sI) to learn how to use this.

<span class="heading-section">📍 Example Usage</span>

```js
// Render the storefront without tag filters
[wps_storefront show_tags="false"]

// Force two products per row and sort by price
[wps_storefront items_per_row="2" sort_by="price"]

// Show products without the description present
[wps_storefront excludes="description"]

```

<span class="heading-section">🎚 Available Attributes</span>

## `dropzone_payload` <span class="attr-type attr-type-required">(required)</span>

Specifies where the actual filter results should render. Takes any valid CSS selector.

```js
[wps_storefront dropzone_payload="#dropzone-payload"]
```

## `dropzone_options` <span class="attr-type attr-type-required">(required)</span>

Specifies where the selectable filter options should render. Takes any valid CSS selector.

```js
[wps_storefront dropzone_options="#dropzone-options"]
```

## `dropzone_selections` <span class="attr-type attr-type-required">(required)</span>

Specifies where the selected user choices should render. Takes any valid CSS selector. Omitting will hide user selections all together.

```js
[wps_storefront dropzone_selections="#dropzone-selections"]
```

## `sort_by`

Determines the products sort order. Corresponds to the [Shopify API values](https://help.shopify.com/en/api/custom-storefronts/storefront-api/reference/enum/productsortkeys). Will be overwritten if user uses the provided sorting dropdown.

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
[wps_storefront sort_by="price"]
```

## `reverse`

Reverses the order of products. Useful when used in combination with `sort_by`. Will be overwritten if user uses the provided sorting dropdown.

| Possible values |
| :-------------- |
| true            |
| false           |

**Example**

```js
// Smallest to largest (A to Z) (old to new)
[wps_storefront sort_by="title" reverse="true"]
```

## `page_size`

Determines the number of products to show per page. Only applicable when pagination is turned on. Will default to the plugin's global [products per page](getting-started/settings?id=products-per-page) setting. Will be overwritten if user uses the provided page size dropdown.

| Possible values |
| :-------------- |
| Any number      |

**Example**

```js
// Shows 4 products per page
[wps_storefront page_size="4"]
```

## `limit`

Limits the overall number of products that show. Max limit is `250`.

| Possible values |
| :-------------- |
| Any number      |

**Example**

```js
// Show two products per page, up to 10
[wps_storefront page_size="2" limit="10"]

// Only show one product
[wps_storefront limit="1"]
```

## `excludes`

Allows for excluding certain product components like the title, description, etc. Takes a comma separated string of values.

| Possible values |
| :-------------- |
| images          |
| title           |
| pricing         |
| description     |
| buy-button      |

**Example**

```js
// Don't show the title or pricing
[wps_storefront excludes="title, pricing"]
```

## `items_per_row`

Determines how many products will appear in each row.

| Possible values |
| :-------------- |
| Any text string |

**Example**

```js
[wps_storefront items_per_row="5"]
```

## `pagination`

Determines whether to hide or show pagination.

| Possible values |
| :-------------- |
| true            |
| false           |

**Example**

```js
[wps_storefront pagination="false"]
```

## `no_results_text`

Specifies the text to use when no filter results are found. Default: `No results found`.

```js
[wps_storefront no_results_text="Custom no results text with emojis 🚨"]
```

## `infinite_scroll` <span class="attr-type attr-type-pro-only">(Pro only)</span>

When turned on, the next page of items will automatically append to the container. Only works when pagination is used.

| Possible values |
| :-------------- |
| true            |
| false           |

**Example**

```js
[wps_storefront infinite_scroll="true"]
```

## `infinite_scroll_offset` <span class="attr-type attr-type-pro-only">(Pro only)</span>

Determines the offset from the edge of the items container. For example, a value of `-100` will begin loading additional items 100px before the end of the items container. Offset can be a positive or negative value.

| Possible values                 |
| :------------------------------ |
| Any positive or negative number |

**Example**

```js
[wps_storefront infinite_scroll_offset="-100"]
```

## `dropzone_sorting`

Specifies where the sorting component should render. Takes any valid CSS selector. Omitting will hide sorting all together.

```js
[wps_storefront dropzone_sorting="#dropzone-sorting"]
```

## `dropzone_pagination`

Specifies where the pagination should render. Takes any valid CSS selector. Omitting will hide pagination all together.

```js
[wps_storefront dropzone_pagination="#dropzone-pagination"]
```

## `show_tags`

Specifies whether to allow the user to filer by product tags. Setting to false will hide the ability to filter by tags.

```js
[wps_storefront show_tags="false"]
```

## `show_vendors`

Specifies whether to allow the user to filer by product vendors. Setting to false will hide the ability to filter by vendors.

```js
[wps_storefront show_vendors="false"]
```

## `show_types`

Specifies whether to allow the user to filer by product types. Setting to false will hide the ability to filter by types.

```js
[wps_storefront show_types="false"]
```

## `show_options_heading`

Specifies whether to show the default "Filter by" options heading.

```js
[wps_storefront show_options_heading="false"]
```

## `available_for_sale`

Display products based on their availability. Setting to `true` will only show products that are in stock.

| Possible values |
| :-------------- |
| true            |
| any (default)   |

**Example**

```js
[wps_storefront available_for_sale="true"]
```
