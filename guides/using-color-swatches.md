# Using Color Swatches

WP Shopify provides two "variant styles": dropdowns and buttons. The color swatches will show only if you're using variant buttons.

By default, the plugin will attempt to transform your variant buttons into color swatches for you automatically. There are two requirements for this to "just work".

1. Your Option name must be called "Color" (case-insensitive) inside Shopify.
2. Your variant value must correspond to a [valid HTML color name](https://htmlcolorcodes.com/color-names).

## Disabling Swatches

If you wish to disable color swatches, add the below code to your theme's JavaScript:

```js
wp.hooks.addFilter('product.variant.styles.colorSwatch.names', 'wpshopify', function (
  defaultNames
) {
  return []
})
```

## Customizing Option Name

If you want to use a custom Option name you can add it to the list of names that WP Shopify will check for. You can do this by using the `product.variant.styles.colorSwatch.names` filter in your theme's JavaScript, like this:

```js
wp.hooks.addFilter('product.variant.styles.colorSwatch.names', 'wpshopify', function (
  defaultNames
) {
  defaultNames.push('material')

  return defaultNames
})
```

Here, we're adding the option name `material` to the list. Now WP Shopify will check if your variants belong to an option called "Material" or "Color" to determine whether to show the color swatches or not.

## Customizing Variant Value

If you're unable to name your variant to match a [valid HTML color name](https://htmlcolorcodes.com/color-names), you can provide a custom color to use instead. You can do this by using the `product.variant.styles.colorSwatch.value` filter in your theme's JavaScript, like this:

```js
wp.hooks.addFilter('product.variant.styles.colorSwatch.value', 'wpshopify', function (
  variantValue
) {
  if (variantValue === 'some variant value') {
    // Here any valid CSS color value will work
    return '#696969'
  }

  return variantValue
})
```

## Overriding All Variant CSS

If you want to customize the entire variant style, you can filter all of the CSS by using the `product.variant.styles` filter in your theme's JavaScript, like this:

```js
wp.hooks.addFilter('product.variant.styles', 'wpshopify', function (
  defaultCustomStyles,
  variant,
  isSelected,
  isAvailableToSelect
) {
  return `
      margin: 0 10px 10px 0;
      padding: 10px;
   `
})
```
