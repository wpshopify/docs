# [wps_collections]

Displays the main collections component. Useful for showing a general list of collections.<br><br>Watch our [quick video tutorial](https://www.youtube.com/watch?v=lYm6G35e8sI) to learn how to use this.

<span class="heading-section">📍 Example Usage</span>

```js
// Display the cheapest 10 collections
[wps_collections sort_by="lowest_price" limit="10"]

```

<span class="heading-section">🎚 Available Attributes</span>

## `title`

Displays collections based on one or more collection title(s).

| Possible values                    |
| :--------------------------------- |
| Any valid Shopify collection title |

```js
[wps_collections title="Featured"]
```

## `updated_at`

Display collections based on the date it was updated. Must use an [ISO 8601](https://en.wikipedia.org/wiki/ISO_8601) format. Default: `false`. Example can be [found based on orders](https://help.shopify.com/en/api/reference/orders/order#created-at-property-2019-07).

| Possible values         |
| :---------------------- |
| Any valid ISO 8601 date |

**Example**

```js
[wps_collections updated_at="2019-02-21 03:16:41"]
```

## `connective`

The "connective" attribute determines how the collections are found when combining _other_ shortcode attributes. For example when set to `and`, every provided attribute must match the searched collections. With `or`, _any_ provided attribute will return the matched collections. Default: `or`.

| Possible values |
| :-------------- |
| and             |
| or              |

**Example**

```js
// collections with either title will show
[wps_collections title="Awesome collection, Even better collection" connective="or"]
```

## `sort_by`

Determines the collections sort order. Corresponds to the [Shopify Storefront API](https://help.shopify.com/en/api/storefront-api/reference/enum/collectionsortkeys). Default: `title`

| Values     |
| :--------- |
| title      |
| updated_at |

```js
[wps_collections sort_by="title"]
```

## `reverse`

Reverses the order that the collections are displayed in

Default: `false`

```js
// Smallest to largest (A to Z) (old to new)
[wps_collections sort_by="title" reverse="true"]

```

## `page_size`

Determines the number of collections to show per page. Only applicable when pagination is turned on. Will default to the plugin's global [products per page](getting-started/settings?id=products-per-page) setting.

| Possible values |
| :-------------- |
| Any number      |

**Example**

```js
// Shows 4 collections per page
[wps_collections page_size="4"]
```

## `limit`

Limits the number of collections. Max allowed is `250`.

Default: `10`

| Values     |
| :--------- |
| Any number |

```js
// Shows up to 250 at any time
[wps_collections limit="25"]

// Only show one
[wps_collections limit="1"]
```

## `items_per_row`

Determines how many collections will appear in each row.

| Possible values |
| :-------------- |
| Any text string |

**Example**

```js
[wps_collections items_per_row="5"]
```

## `excludes`

Allows for excluding certain collection components like the title. Takes a comma separated string of values.

| Possible values |
| :-------------- |
| image           |
| title           |
| description     |

**Example**

```js
[wps_collections excludes="title, description"]
```

## `single`

Determines whether to show the collection products or not. Useful for only showing one collection with it's products. Enables the `products_` shortcode attributes.

| Possible values |
| :-------------- |
| true            |
| false           |

**Example**

```js
[wps_collections single="true"]
```

## `pagination`

Determines whether to hide or show pagination.

| Possible values |
| :-------------- |
| true            |
| false           |

**Example**

```js
[wps_collections pagination="false"]
```

## `dropzone_load_more`

When [pagination](#pagination) is set to true, this allows for specifying a custom location in the DOM to place the pagination "load more" control component for collections. Takes any valid CSS selector. When set to false, the load more button will be placed directly below the products output. Default: `false`.

> [!NOTE|className:info sm]
> The HTML element specified will be completely emptied and replaced with the load more component.

**Example**

```js
[wps_collections dropzone_load_more="#my-custom-load-more-container"]
```

## `dropzone_collection_title`

When [single](#single) is set to true, this allows for specifying a custom location in the DOM to place the collection title. Takes any valid CSS selector.

> [!NOTE|className:info sm]
> The HTML element specified will be completely emptied and replaced with the load more component.

**Example**

```js
[wps_collections single="true" dropzone_collection_title="#title-container"]
```

## `dropzone_collection_image`

When [single](#single) is set to true, this allows for specifying a custom location in the DOM to place the collection image. Takes any valid CSS selector.

> [!NOTE|className:info sm]
> The HTML element specified will be completely emptied and replaced with the load more component.

**Example**

```js
[wps_collections single="true" dropzone_collection_image="#image-container"]
```

## `dropzone_collection_description`

When [single](#single) is set to true, this allows for specifying a custom location in the DOM to place the collection description. Takes any valid CSS selector.

> [!NOTE|className:info sm]
> The HTML element specified will be completely emptied and replaced with the load more component.

**Example**

```js
[wps_collections single="true" dropzone_collection_description="#description-container"]
```

## `dropzone_collection_products`

When [single](#single) is set to true, this allows for specifying a custom location in the DOM to place the collection products. Takes any valid CSS selector.

> [!NOTE|className:info sm]
> The HTML element specified will be completely emptied and replaced with the load more component.

**Example**

```js
[wps_collections single="true" dropzone_collection_products="#products-container"]
```

## `infinite_scroll` <span class="attr-type attr-type-pro-only">(Pro only)</span>

When turned on, the next page of collections will automatically append to the container. Only works when pagination is used.

| Possible values |
| :-------------- |
| true            |
| false           |

**Example**

```js
[wps_collections infinite_scroll="true"]
```

## `infinite_scroll_offset` <span class="attr-type attr-type-pro-only">(Pro only)</span>

Determines the offset from the edge of the collections container. For example, a value of `-100` will begin loading additional collections 100px before the end of the collections container. Offset can be a positive or negative value.

| Possible values                 |
| :------------------------------ |
| Any positive or negative number |

**Example**

```js
[wps_collections infinite_scroll_offset="-100"]
```

## `products_sort_by`

Determines the products sort order within a collection. Corresponds to the [Shopify Storefront API](https://help.shopify.com/en/api/storefront-api/reference/enum/productcollectionsortkeys). Default: `title`

| Values             |
| :----------------- |
| title              |
| collection_default |
| created            |
| id                 |
| manual             |
| price              |
| relevance          |
| best_selling       |

```js
[wps_collections products_sort_by="price"]
```

## `products_reverse`

Reverses the order of products. Useful when used in combination with `sort_by`.

| Possible values |
| :-------------- |
| true            |
| false           |

**Example**

```js
// Smallest to largest (A to Z) (old to new)
[wps_collections products_reverse="true"]
```

## `products_page_size`

Determines the number of products to show per page. Only applicable when pagination is turned on. Will default to the plugin's global [products per page](getting-started/settings?id=products-per-page) setting.

| Possible values |
| :-------------- |
| Any number      |

**Example**

```js
// Shows 4 products per page
[wps_collections single="true" products_page_size="4"]
```

## `products_limit`

Limits the overall number of products that show. Max limit is `250`.

| Possible values |
| :-------------- |
| Any number      |

**Example**

```js
// Show two products per page, up to 10
[wps_collections single="true" products_page_size="2" products_limit="10"]

// Only show one product
[wps_collections single="true" products_limit="1"]
```

## `products_add_to_cart_button_color`

Determines the buy button color. Default: `#14273b`.

| Possible values     |
| :------------------ |
| Any valid CSS color |

**Example**

```js
[wps_collections single="true" products_add_to_cart_button_color="#000"]
```

## `products_variant_button_color`

Determines the variant dropdown color. Default: `#52a7a6`.

| Possible values     |
| :------------------ |
| Any valid CSS color |

**Example**

```js
[wps_collections single="true" products_variant_button_color="#000"]
```

## `products_add_to_cart_button_text`

Determines the buy button text. Default: `Add to cart`.

| Possible values |
| :-------------- |
| Any text string |

**Example**

```js
[wps_collections single="true" products_add_to_cart_button_text="Add to bag"]
```

## `products_hide_quantity`

Determines whether to hide the quantity input.

| Possible values |
| :-------------- |
| true            |
| false           |

**Example**

```js
[wps_collections single="true" products_hide_quantity="true"]
```

## `products_show_quantity_label`

Determines whether to show or hide the "label" to the quantity selection element. Shows the word "Quantity" when turned on.

| Possible values |
| :-------------- |
| true            |
| false           |

**Example**

```js
[wps_collections single="true" products_show_quantity_label="false"]
```

## `products_min_quantity`

Sets a "minimum" number to the quantity field. The user will not be able to add _less than_ this number to the cart at any given time.

**Example**

```js
[wps_collections single="true" products_min_quantity="4"]
```

## `products_max_quantity`

Sets a "maximum" number to the quantity field. The user will not be able to add _more than_ this number to the cart at any given time.

**Example**

```js
[wps_collections single="true" products_max_quantity="20"]
```

## `products_excludes`

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
[wps_collections single="true" products_excludes="title, pricing"]
```

## `products_items_per_row`

Determines how many products will appear in each row.

| Possible values |
| :-------------- |
| Any text string |

**Example**

```js
[wps_collections single="true" products_items_per_row="5"]
```

## `products_show_price_range`

Determines whether to show price ranges for each product. Only applicable when `pricing` is not set within the [excludes](#excludes) attribute.

| Possible values |
| :-------------- |
| true            |
| false           |

**Example**

```js
[wps_collections single="true" products_show_price_range="true"]
```

## `products_show_compare_at`

Determines whether to show the compare at price for each product. Only applicable when `pricing` is not set within the [excludes](#excludes) attribute.

| Possible values |
| :-------------- |
| true            |
| false           |

**Example**

```js
[wps_collections single="true" products_show_compare_at="true"]
```

## `products_quantity_label_text`

Customizes the label text next to the quantity input field.

| Possible values |
| :-------------- |
| Any text string |

**Example**

```js
[wps_collections single="true" products_quantity_label_text="Custom quantity text"]
```

## `products_show_featured_only`

Determines whether to only show the product feature image. By default, all product images will show as thumbnails below the featured image.

| Possible values |
| :-------------- |
| true            |
| false           |

**Example**

```js
[wps_collections single="true" products_show_featured_only="true"]
```

## `products_show_zoom` <span class="attr-type attr-type-pro-only">(Pro only)</span>

Determines whether to enable product image zooming. When enabled, zoom will be triggered on the featured image. Only available in [WP Shopify Pro](/getting-started/wp-shopify-pro.md).

| Possible values |
| :-------------- |
| true            |
| false           |

**Example**

```js
[wps_collections single="true" products_show_zoom="true"]
```

## `products_pagination`

Determines whether to hide or show pagination.

| Possible values |
| :-------------- |
| true            |
| false           |

**Example**

```js
[wps_collections single="true" products_pagination="false"]
```

## `products_no_results_text`

The text to show when no products are found.

| Possible values |
| :-------------- |
| Any text string |

**Example**

```js
[wps_collections single="true" products_no_results_text="Nothing found! 🙃"]
```

## `products_infinite_scroll` <span class="attr-type attr-type-pro-only">(Pro only)</span>

When turned on, the next page of items will automatically append to the container. Only works when pagination is used.

| Possible values |
| :-------------- |
| true            |
| false           |

**Example**

```js
[wps_collections single="true" products_infinite_scroll="true"]
```

## `products_infinite_scroll_offset` <span class="attr-type attr-type-pro-only">(Pro only)</span>

Determines the offset from the edge of the items container. For example, a value of `-100` will begin loading additional items 100px before the end of the items container. Offset can be a positive or negative value.

| Possible values                 |
| :------------------------------ |
| Any positive or negative number |

**Example**

```js
[wps_collections single="true" products_infinite_scroll_offset="-100"]
```

## `products_dropzone_load_more`

When `pagination` is set to true, this allows for specifying a custom location in the DOM to place the pagination "load more" control component. Takes any valid CSS selector. When set to false, the load more button will be placed directly below the products output. Default: `false`.

> [!NOTE|className:info sm]
> The HTML element specified will be completely emptied and replaced with the load more component.

**Example**

```js
[wps_collections single="true" products_dropzone_load_more="#my-custom-load-more-container"]
```
