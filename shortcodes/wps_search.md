# [wps_search]

Displays the search component.<br><br>Watch our [quick video tutorial](https://www.youtube.com/watch?v=lYm6G35e8sI) to learn how to use this.

<span class="heading-section">📍 Example Usage</span>

```js
// Drops the search results into a container with the id of #search-container
[wps_search dropzone="#search-container"]

```

<span class="heading-section">🎚 Available Attributes</span>

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
[wps_products sort_by="price"]
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
[wps_products sort_by="title" reverse="true"]
```

## `page_size`

Determines the number of products to show per page. Only applicable when pagination is turned on. Will default to the plugin's global [products per page](getting-started/settings?id=products-per-page) setting.

| Possible values |
| :-------------- |
| Any number      |

**Example**

```js
// Shows 4 products per page
[wps_products page_size="4"]
```

## `limit`

Limits the overall number of products that show. Max limit is `250`.

| Possible values |
| :-------------- |
| Any number      |

**Example**

```js
// Show two products per page, up to 10
[wps_products page_size="2" limit="10"]

// Only show one product
[wps_products limit="1"]
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
[wps_products excludes="title, pricing"]
```

## `items_per_row`

Determines how many products will appear in each row.

| Possible values |
| :-------------- |
| Any text string |

**Example**

```js
[wps_products items_per_row="5"]
```

## `pagination`

Determines whether to hide or show pagination.

| Possible values |
| :-------------- |
| true            |
| false           |

**Example**

```js
[wps_products pagination="false"]
```

## `no_results_text`

The text to show when no products are found.

| Possible values |
| :-------------- |
| Any text string |

**Example**

```js
[wps_products no_results_text="Nothing found! 🙃"]
```

## `infinite_scroll`

When turned on, the next page of items will automatically append to the container. Only works when pagination is used.

| Possible values |
| :-------------- |
| true            |
| false           |

**Example**

```js
[wps_products infinite_scroll="true"]
```

## `infinite_scroll_offset`

Determines the offset from the edge of the items container. For example, a value of `-100` will begin loading additional items 100px before the end of the items container. Offset can be a positive or negative value.

| Possible values                 |
| :------------------------------ |
| Any positive or negative number |

**Example**

```js
[wps_products infinite_scroll_offset="-100"]
```

## `no_results_text` <span class="attr-type attr-type-optional">(optional)</span>

Specifies the text to use when no results are found.

Default: `No results found`

```js
[wps_search no_results_text="Custom no results text with emojis 🚨"]
```

## `dropzone_form`

Specifies where the search form should render. Takes any valid CSS selector.

```js
[wps_search dropzone_form="#search-form"]
```

## `dropzone_load_more`

When `pagination` is set to true, this allows for specifying a custom location in the DOM to place the pagination "load more" control component. Takes any valid CSS selector. When set to false, the load more button will be placed directly below the products output. Default: `false`.

> [!NOTE|className:info sm]
> The HTML element specified will be completely emptied and replaced with the load more component.

**Example**

```js
[wps_products dropzone_load_more="#my-custom-load-more-container"]
```

## `dropzone_payload`

Specifies where the products being searched should render. Takes any valid CSS selector.

```js
[wps_search dropzone_payload="#search-form"]
```

## `dropzone_loader`

Specifies where the search loading indicator should render. Takes any valid CSS selector.

```js
[wps_search dropzone_loader="#search-form"]
```
