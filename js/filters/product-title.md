# Product Title JavaScript Filters

You may want to read our [Getting started with JavaScript Hooks](guides/javascript-hooks.md) guide first.

## `product.title.class`

Allows for filtering the class of the product's title HTML element.

| Parameters     | Description                                  |
| :------------- | :------------------------------------------- |
| defaultClasses | Represents the default product title classes |

**Example**

```js
wp.hooks.addFilter('product.title.class', 'wpshopify', function (defaultClasses) {
  return defaultClasses + ' my-awesome-class'
})
```

## `product.title.text`

Allows for filtering the product title.

| Parameters   | Description                  |
| :----------- | :--------------------------- |
| productTitle | Represents the product title |

**Example**

```js
wp.hooks.addFilter('product.title.text', 'wpshopify', function (productTitle) {
  return productTitle
})
```

## `before.product.title`

Allows for adding arbitrary HTML before the product title

| Parameters  | Description                                       |
| :---------- | :------------------------------------------------ |
| defaultVal  | false                                             |
| productData | Data for the product like title, description, etc |

**Example**

```js
wp.hooks.addFilter('before.product.title', 'wpshopify', function (defaultVal, productData) {
  return '<p>Custom HTML</p>'
})
```

## `after.product.title`

Allows for adding arbitrary HTML after the product title

| Parameters  | Description                                       |
| :---------- | :------------------------------------------------ |
| defaultVal  | false                                             |
| productData | Data for the product like title, description, etc |

**Example**

```js
wp.hooks.addFilter('after.product.title', 'wpshopify', function (defaultVal, productData) {
  return '<p>Custom HTML</p>'
})
```
