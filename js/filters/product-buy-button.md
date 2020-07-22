# Product Buy Button JavaScript Filters

You may want to read our [Getting started with JavaScript Hooks](guides/javascript-hooks.md) guide first.

## `products.buyButton.unavailable.html`

This filter allows for customizing the HTML shown when a product is out of stock. This will replace the Buy Button component.

| Parameters   | Description                      |
| :----------- | :------------------------------- |
| productState | State data for the given product |

**Example**

```js
wp.hooks.addFilter('products.buyButton.unavailable.html', 'wpshopify', function (
  defaultVal,
  productState
) {
  return '<p>Custom out of stock HTML</p>'
})
```

## `products.variant.title.text`

Allows for customizing the variant title text.

| Parameters   | Description                         |
| :----------- | :---------------------------------- |
| variantTitle | Represents the actual variant title |

**Example**

```js
wp.hooks.addFilter('products.variant.title.text', 'wpshopify', function (variantTitle) {
  return variantTitle + ' custom text!'
})
```

## `products.quantity.label.text`

Allows for customizing the quantity label text.

| Parameters    | Description                                |
| :------------ | :----------------------------------------- |
| quantityLabel | Represents the default quantity label text |

**Example**

```js
wp.hooks.addFilter('products.quantity.label.text', 'wpshopify', function (quantityLabel) {
  return quantityLabel + ' custom text!'
})
```

## `product.variant.styles.colorSwatch.names`

Allows for adding custom option names for the plugin to check when determining whether to create a color swatch. By default, the plugin will only create a color swatch automatically when a product has an option name of `color`.

Only applicable when using "buttons" variants style.

| Parameters   | Description                                                                                |
| :----------- | :----------------------------------------------------------------------------------------- |
| defaultNames | Array of default names to determine whether to create a color swatch. Default: `['color']` |

**Example**

```js
wp.hooks.addFilter('product.variant.styles.colorSwatch.names', 'wpshopify', function (
  defaultNames
) {
  return defaultNames
})
```

## `product.variant.styles.colorSwatch.value`

Allows for customizing the actual color of each color swatch. By default, the plugin will attempt to match your variant value to a [valid HTML Color Code](https://htmlcolorcodes.com). So if your variant name does not match an HTML color code, you can specify a color using this filter.

You must return a valid CSS color value. For example, `Black`, `#000`, or `rgb(0,0,0)`.

| Parameters   | Description                                                                                |
| :----------- | :----------------------------------------------------------------------------------------- |
| defaultNames | Array of default names to determine whether to create a color swatch. Default: `['color']` |

**Example**

```js
wp.hooks.addFilter('product.variant.styles.colorSwatch.value', 'wpshopify', function (colorValue) {
  if (colorValue === 'Variant name') {
    return '#000'
  }
})
```

## `product.variant.styles`

Allows for customizing the CSS of the variant. Must return the new CSS as a string.

| Parameters    | Description                                    |
| :------------ | :--------------------------------------------- |
| defaultStyles | Represents the default variant CSS as a string |

**Example**

```js
wp.hooks.addFilter('product.variant.styles', 'wpshopify', function (defaultStyles) {
  return defaultStyles
})
```

## `product.addToCart.text`

Allows for customizing the add to cart text

| Parameters         | Description                                               |
| :----------------- | :-------------------------------------------------------- |
| defaultTextElement | Represents the default text element as a React element    |
| defaultText        | Represents the default text value. Default: `Add to cart` |

**Example**

```js
wp.hooks.addFilter('product.addToCart.text', 'wpshopify', function (
  defaultTextElement,
  defaultText
) {
  return 'Custom text'
})
```

## `product.missingSelection.text`

Allows for customizing the missing selections text

| Parameters  | Description                                                                                 |
| :---------- | :------------------------------------------------------------------------------------------ |
| defaultText | Represents the default text of the missing selections. Default: `Please select a variation` |

**Example**

```js
wp.hooks.addFilter('product.missingSelection.text', 'wpshopify', function (defaultText) {
  return 'Custom missing selections text'
})
```

## `before.product.buyButton`

Allows for adding arbitrary HTML before the product's buy button.

| Parameters   | Description                                             |
| :----------- | :------------------------------------------------------ |
| defaultValue | Represents the before buy button HTML. Default: `false` |
| productState | Represents the product state                            |

**Example**

```js
wp.hooks.addFilter('before.product.buyButton', 'wpshopify', function (defaultValue, productState) {
  return '<p>Before HTML</p>'
})
```

## `after.product.buyButton`

Allows for adding arbitrary HTML after the product's buy button.

| Parameters   | Description                                            |
| :----------- | :----------------------------------------------------- |
| defaultValue | Represents the after buy button HTML. Default: `false` |
| productState | Represents the product state                           |

**Example**

```js
wp.hooks.addFilter('after.product.buyButton', 'wpshopify', function (defaultValue, productState) {
  return '<p>After HTML</p>'
})
```

## `buyButton.quantityStep`

Allows for customizing the "step" of the quantity field. For example, returning `2` will only allow the user to increment the quanaity field by steps of 2. E.g., `2`, `4,`, `6`, ...etc.

| Parameters     | Description                                 |
| :------------- | :------------------------------------------ |
| defaultStep    | Represents the after step. Default: `false` |
| buyButtonState | Represents the buy button state             |

**Example**

```js
wp.hooks.addFilter('buyButton.quantityStep', 'wpshopify', function (defaultStep, buyButtonState) {
  return 2
})
```
