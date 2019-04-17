# [wps_products_buy_button]

Displays the product "Buy Button" component. Will output three different elements including the quantity selector, variant drop-downs, and the add to cart button.

## 🎯 Example Usage

```js
// Defaults to showing buy buttons for the latest 10 products
[wps_products_buy_button]

// Show buy buttons for products with vendors "Apple"
[wps_products_buy_button vendor="Apple"]

// Show buy buttons for product with title "Product A". Also hide the quantity element
[wps_products_buy_button title="Product A" hide_quantity="true"]

```

## ⚡️ Available Attributes

### `title` <span class="attr-type attr-type-optional">(optional)</span>

Display buy button from product title(s).

Default: `false`

```js
[wps_products_buy_button title="Product A, Product B"]
```

### `slug` <span class="attr-type attr-type-optional">(optional)</span>

Display buy button from product slug(s). Case insensitive.

Default: `false`

```js
[wps_products_buy_button slug="product-a, product-b"]
```

### `tag` <span class="attr-type attr-type-optional">(optional)</span>

Display buy button from product tag(s).

Default: `false`

```js
[wps_products_buy_button tag="tag-a, tab-b"]
```

### `vendor` <span class="attr-type attr-type-optional">(optional)</span>

Display buy button from product vendor(s).

Default: `false`

```js
[wps_products_buy_button vendor="Apple, Microsoft"]
```

### `type` <span class="attr-type attr-type-optional">(optional)</span>

Display buy button from product type(s).

Default: `false`

```js
[wps_products_buy_button type="Featured, Popular"]
```

### `description` <span class="attr-type attr-type-optional">(optional)</span>

Display buy button from product description. Performs a "wildcard" search based on the content you provide. For example, providing the value "Sale" will return products will the following descriptions:

"This product is on Sale until Tuesday!"<br>
"Sale ends tomorrow"

Default: `false`

```js
[wps_products_buy_button description="This is from the product description ..."]
```

### `product_id` <span class="attr-type attr-type-optional">(optional)</span>

Display buy button from product id(s).

Default: `false`

```js
[wps_products_buy_button product_id="19213874213, 93283473232"]
```

### `post_id` <span class="attr-type attr-type-optional">(optional)</span>

Display buy button from post id(s).

Default: `false`

```js
[wps_products_buy_button post_id="3124, 9128"]
```

### `orderby` <span class="attr-type attr-type-optional">(optional)</span>

Determines the order criteria of the output of two or more buy buttons. Only one value allowed.

Default: `title`

| Available Values |
| :--------------- |
| title            |
| updated_at       |
| created_at       |

```js
[wps_products_buy_button orderby="title"]
```

### `order` <span class="attr-type attr-type-optional">(optional)</span>

Determines how to order the output of two or more buy buttons. Only one value allowed.

Default: `desc`

| Available Values |
| :--------------- |
| asc              |
| desc             |

```js
// Smallest to largest (A to Z) (old to new)
[wps_products_buy_button order="asc"]

// Largest to smallest (Z to A) (new to old)
[wps_products_buy_button order="desc"]
```

### `limit` <span class="attr-type attr-type-optional">(optional)</span>

Allows for limiting the number of buy buttons. Set to "false" to remove limit altogether.

Default: `10`

| Available Values |
| :--------------- |
| Any number       |
| false            |

```js
[wps_products_buy_button limit="25"]

// Removes limit altogether
[wps_products_buy_button limit="false"]
```

### `render_from_server` <span class="attr-type attr-type-optional">(optional)</span>

Determines whether to render the buy button on the client or server. [Learn more](/getting-started/displaying)

Default: `false`

| Available Values |
| :--------------- |
| true             |
| false            |

```js
[wps_products_buy_button render_from_server="true"]
```

### `button_color` <span class="attr-type attr-type-optional">(optional)</span>

Determines the buy button color.

Default: `#14273b`

| Available Values                      |
| :------------------------------------ |
| Any valid CSS background-color value. |

```js
[wps_products_buy_button button_color="#000"]
```

### `variant_color` <span class="attr-type attr-type-optional">(optional)</span>

Determines the variant dropdown color.

Default: `#52a7a6`

| Available Values                      |
| :------------------------------------ |
| Any valid CSS background-color value. |

```js
[wps_products_buy_button button_color="#000"]
```

### `button_text` <span class="attr-type attr-type-optional">(optional)</span>

Determines the buy button text.

Default: `Add to cart`

```js
[wps_products_buy_button button_color="Add in bag"]
```

### `hide_quantity` <span class="attr-type attr-type-optional">(optional)</span>

Determines whether to hide the quantity selection element

Default: `false`

| Available Values |
| :--------------- |
| true             |
| false            |

```js
[wps_products_buy_button hide_quantity="true"]
```

### `min_quantity` <span class="attr-type attr-type-optional">(optional)</span>

Sets a "minimum" number to the quantity field. The user will not be able to add _less than_ this number to the cart at any given time.

Default: `false`

```js
[wps_products_buy_button min_quantity="4"]
```

### `max_quantity` <span class="attr-type attr-type-optional">(optional)</span>

Sets a "maximum" number to the quantity field. The user will not be able to add _more than_ this number to the cart at any given time.

Default: `false`

```js
[wps_products_buy_button max_quantity="20"]
```

### `show_quantity_label` <span class="attr-type attr-type-optional">(optional)</span>

Determines whether to show or hide the "label" to the quantity selection element. Shows the word "Quantity" when turned on.

Default: `true`

| Available Values |
| :--------------- |
| true             |
| false            |

```js
[wps_products_buy_button show_quantity_label="false"]
```
