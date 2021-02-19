# [wps_products]

Displays the main products component. Useful for showing a general list of products.
<br><br>Watch our [quick video tutorial](https://www.youtube.com/watch?v=lYm6G35e8sI) to learn how to use this.

<iframe width="860" height="515" src="https://www.youtube.com/embed/kvRYOiJAXJ0" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

<span class="heading-section">📍 Example Usage</span>

```js
// Displays the cheapest 10 products
[wps_products sort_by="lowest_price" limit="10"]

// Displays products in rows of 5, sorted by best selling
[wps_products items_per_row="5" sort_by="best_selling"]

// Displays 20 products per page, sorted by title reversed as Z-A
[wps_products page_size="20" sort_by="title" reverse="true"]

```

<span class="heading-section">🎚 Available Attributes</span>

## `title`

Displays products based on one or more product title(s).

| Possible values                 |
| :------------------------------ |
| Any valid Shopify product title |

**Example**

```js
[wps_products title="Product A, Product B"]
```

## `tag`

Display products based on one or more product tag(s).

| Possible values       |
| :-------------------- |
| Any valid product tag |

**Example**

```js
[wps_products tag="Tag A, Tag B"]
```

## `vendor`

Display products based on one or more product vendor(s).

| Possible                 |
| :----------------------- |
| Any valid product vendor |

**Example**

```js
[wps_products vendor="Vendor A, Vendor B"]
```

## `collection`

Display products based on a single collection.

| Possible                         |
| :------------------------------- |
| Any valid collection name vendor |

**Example**

```js
[wps_products collection="Featured Products"]
```

## `product_type`

Display products based on one or more product type(s).

| Possible values        |
| :--------------------- |
| Any valid product type |

**Example**

```js
[wps_products product_type="Books"]
```

## `available_for_sale`

Display products based on their availability. Setting to `true` will only show products that are in stock.

| Possible values |
| :-------------- |
| true            |
| any (default)   |

**Example**

```js
[wps_products_buy_button available_for_sale="true"]
```

## `created_at`

Display products based on the date it was created. Must use an [ISO 8601](https://en.wikipedia.org/wiki/ISO_8601) format. Example can be [found based on orders](https://help.shopify.com/en/api/reference/orders/order#created-at-property-2019-07).

| Possible values         |
| :---------------------- |
| Any valid ISO 8601 date |

**Example**

```js
[wps_products created_at="2019-02-21 03:16:41"]
```

## `updated_at`

Display products based on the date it was updated. Must use an [ISO 8601](https://en.wikipedia.org/wiki/ISO_8601) format. Default: `false`. Example can be [found based on orders](https://help.shopify.com/en/api/reference/orders/order#created-at-property-2019-07).

| Possible values         |
| :---------------------- |
| Any valid ISO 8601 date |

**Example**

```js
[wps_products updated_at="2019-02-21 03:16:41"]
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
[wps_products product_id="2216928411696, 93283473232"]
```

## `post_id`

Display products based on one or more product post id(s).

| Possible values           |
| :------------------------ |
| Any valid product post id |

**Example**

```js
[wps_products post_id="35421, 35418"]
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

## `connective`

The "connective" attribute determines how the products are found when combining _other_ shortcode attributes. For example when set to `and`, every provided attribute must match the searched products. With `or`, _any_ provided attribute will return the matched products. Default: `and`.

| Possible values |
| :-------------- |
| and             |
| or              |

**Example**

```js
// Products with either title will show
[wps_products title="Awesome product, Even better product" connective="or"]

// Only products with both Tag1 and Tag2 will show
[wps_products tag="Tag1, Tag2" connective="and"]
```

## `title_size`

Allows for customizing the font size of the product title.

| Possible values          |
| :----------------------- |
| Any valid CSS size value |

**Example**

```js
[wps_products title_size="20px"]
[wps_products title_size="2em"]
```

## `title_color`

Allows for customizing the font color of the product title.

| Possible values           |
| :------------------------ |
| Any valid CSS color value |

**Example**

```js
[wps_products title_color="red"]
[wps_products title_color="#000000"]
```

## `add_to_cart_button_color`

Determines the buy button color. Default: `#14273b`.

| Possible values     |
| :------------------ |
| Any valid CSS color |

**Example**

```js
[wps_products add_to_cart_button_color="#000"]
```

## `variant_button_color`

Determines the variant dropdown color. Default: `#52a7a6`.

| Possible values     |
| :------------------ |
| Any valid CSS color |

**Example**

```js
[wps_products variant_button_color="#000"]
```

## `variant_style`

Only available in [WP Shopify Pro](getting-started/wp-shopify-pro.md).

Determines the visual style of variant controls. Default: `dropdown`.

| Possible values |
| :-------------- |
| dropdown        |
| buttons         |

**Example**

```js
[wps_products variant_style="buttons"]
```

## `add_to_cart_button_text`

Determines the buy button text. Default: `Add to cart`.

| Possible values |
| :-------------- |
| Any text string |

**Example**

```js
[wps_products add_to_cart_button_text="Add to bag"]
```

## `add_to_cart_button_text_color`

Determines the buy button text color. Default: `#FFFFFF`.

| Possible values     |
| :------------------ |
| Any valid CSS color |

**Example**

```js
[wps_products add_to_cart_button_text_color="#000"]
```

## `hide_quantity`

Determines whether to hide the quantity input.

| Possible values |
| :-------------- |
| true            |
| false           |

**Example**

```js
[wps_products hide_quantity="true"]
```

## `show_quantity_label`

Determines whether to show or hide the "label" to the quantity selection element. Shows the word "Quantity" when turned on.

| Possible values |
| :-------------- |
| true            |
| false           |

**Example**

```js
[wps_products show_quantity_label="false"]
```

## `min_quantity`

Sets a "minimum" number to the quantity field. The user will not be able to add _less than_ this number to the cart at any given time.

**Example**

```js
[wps_products min_quantity="4"]
```

## `max_quantity`

Sets a "maximum" number to the quantity field. The user will not be able to add _more than_ this number to the cart at any given time.

**Example**

```js
[wps_products max_quantity="20"]
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

## `show_price_range`

Determines whether to show price ranges for each product. Only applicable when `pricing` is not set within the [excludes](#excludes) attribute.

| Possible values |
| :-------------- |
| true            |
| false           |

**Example**

```js
[wps_products show_price_range="true"]
```

## `show_compare_at`

Determines whether to show the compare at price for each product. Only applicable when `pricing` is not set within the [excludes](#excludes) attribute.

| Possible values |
| :-------------- |
| true            |
| false           |

**Example**

```js
[wps_products show_compare_at="true"]
```

## `quantity_label_text`

Customizes the label text next to the quantity input field.

| Possible values |
| :-------------- |
| Any text string |

**Example**

```js
[wps_products quantity_label_text="Custom quantity text"]
```

## `show_featured_only`

Determines whether to only show the product feature image. By default, all product images will show as thumbnails below the featured image.

| Possible values |
| :-------------- |
| true            |
| false           |

**Example**

```js
[wps_products show_featured_only="true"]
```

## `show_zoom`

Only available in [WP Shopify Pro](getting-started/wp-shopify-pro.md).

Determines whether to enable product image zooming. When enabled, zoom will be triggered on the featured image.

| Possible values |
| :-------------- |
| true            |
| false           |

**Example**

```js
[wps_products show_zoom="true"]
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

## `description_length`

Determines how long the product description should be in characters. Useful for only showing a specific excerpt.

| Possible values                                  |
| :----------------------------------------------- |
| Number of characters to limit the description by |

**Example**

```js
[wps_products_description description_length="50"]
```

## `infinite_scroll`

Only available in [WP Shopify Pro](getting-started/wp-shopify-pro.md).

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

Only available in [WP Shopify Pro](getting-started/wp-shopify-pro.md).

Determines the offset from the edge of the items container. For example, a value of `-100` will begin loading additional items 100px before the end of the items container. Offset can be a positive or negative value.

| Possible values                 |
| :------------------------------ |
| Any positive or negative number |

**Example**

```js
[wps_products infinite_scroll_offset="-100"]
```

## `dropzone_load_more`

When `pagination` is set to true, this allows for specifying a custom location in the DOM to place the pagination "load more" control component. Takes any valid CSS selector. When set to false, the load more button will be placed directly below the products output. Default: `false`.

> [!NOTE|className:info sm]
> The HTML element specified will be completely emptied and replaced with the load more component.

**Example**

```js
[wps_products dropzone_load_more="#my-custom-load-more-container"]
```

## `full_width`

When set to `true`, will force the product to span the width of its container.

| Possible values |
| :-------------- |
| true            |
| false           |

**Example**

```js
[wps_products full_width="true"]
```

## `images_align`

Allows for determining how the featured image is positioned horizontally. Default: `left`.

| Possible values |
| :-------------- |
| left            |
| center          |
| right           |

**Example**

```js
[wps_products images_align="true"]
```

## `link_to`

Allows for determining where products link, if anywhere. Default: `wordpress`.

| Possible values |
| :-------------- |
| none            |
| wordpress       |
| shopify         |
| modal           |

**Example**

```js
[wps_products link_to="none"]
```

## `link_target`

Allows for determining whether links open in a new tab or not. Default: `_self`.

| Possible values |
| :-------------- |
| \_self          |
| \_blank         |

**Example**

```js
[wps_products link_target="_blank"]
```

## `link_with_buy_button`

Allows for determining whether to show the buy button controls when linking to WordPress or Shopify. Default: `false`.

| Possible values |
| :-------------- |
| true            |
| false           |

**Example**

```js
[wps_products link_with_buy_button="true" link_to="wordpress"]
```

## `carousel`

Allows for showing products in a carousel view. Default: `false`.

| Possible values |
| :-------------- |
| true            |
| false           |

**Example**

```js
[wps_products carousel="true"]
```

## `carousel_dots`

Determines whether to show the carousel dots or not. Default: `true`.

| Possible values |
| :-------------- |
| true            |
| false           |

**Example**

```js
[wps_products carousel="true" carousel_dots="false"]
```

## `carousel_infinite`

Determines whether to continue sliding through products endlessly. Default: `true`.

| Possible values |
| :-------------- |
| true            |
| false           |

**Example**

```js
[wps_products carousel="true" carousel_infinite="false"]
```

## `carousel_speed`

Determines the carousel speed. Default: `500`ms.

| Possible values        |
| :--------------------- |
| Numebr of milliseconds |

**Example**

```js
[wps_products carousel="true" carousel_speed="1000"]
```

## `carousel_slides_to_show`

Determines the number of carousel slides to show at once. Default: `4`.

| Possible values          |
| :----------------------- |
| Numebr of slides to show |

**Example**

```js
[wps_products carousel="true" carousel_slides_to_show="3"]
```

## `carousel_slides_to_scroll`

Determines the number of carousel slides to scroll at once. Default: `4`.

| Possible values            |
| :------------------------- |
| Numebr of slides to scroll |

**Example**

```js
[wps_products carousel="true" carousel_slides_to_scroll="3"]
```

## `carousel_prev_arrow`

Allows to specifying a custom "previous slide" arrow icon. Defaults to a black arrow.

| Possible values                                                       |
| :-------------------------------------------------------------------- |
| A URL to a custom icon, or any valid CSS image url prop like data uri |

**Example**

```js
[wps_products carousel="true" carousel_prev_arrow="https://mysite.com/pre_arrow.png"]
```

## `carousel_next_arrow`

Allows to specifying a custom "next slide" arrow icon. Defaults to a black arrow.

| Possible values                                                       |
| :-------------------------------------------------------------------- |
| A URL to a custom icon, or any valid CSS image url prop like data uri |

**Example**

```js
[wps_products carousel="true" carousel_next_arrow="https://mysite.com/pre_arrow.png"]
```

## `keep_commas`

By default, if you have a product with commas in the title, WP Shopify will treat this as multiple different product titles. Setting `keep_commas` to true will allow you to search products with commas in their title.

| Possible values |
| :-------------- |
| true            |
| false (default) |

**Example**

```js
[wps_products title="This, is my, product" keep_commas="true"]
```

## `direct_checkout`

Allows for linking customers directly to the Shopify checkout process. This will bypass the default WP Shopify cart experience altogether. Default: `false`.

| Possible values |
| :-------------- |
| true            |
| false           |

**Example**

```js
[wps_products direct_checkout="true"]
```
