# Notices JavaScript Filters

You may want to read our [Getting started with JavaScript Hooks](guides/javascript-hooks.md) guide first.

## `notice.storefront.noGroup.text`

Allows for customizing the Storefront's "no group found" text. For example, this would show in place of tags if none exist.

| Parameter   | Description                                   |
| :---------- | :-------------------------------------------- |
| defaultText | Represents the default "no group found" text. |

**Example**

```js
wp.hooks.addFilter('notice.storefront.noGroup.text', 'wpshopify', function (defaultText) {
  return 'Custom text'
})
```

## `notice.product.addToCart.text`

Allows for customizing the add to cart notice message

| Parameter   | Description                         |
| :---------- | :---------------------------------- |
| defaultText | Represents the default notice text. |

**Example**

```js
wp.hooks.addFilter('notice.product.addToCart.text', 'wpshopify', function (defaultText) {
  return 'Custom text'
})
```

## `notice.unavailable.text`

Allows for customizing the sold out notice text

| Parameter   | Description                                  |
| :---------- | :------------------------------------------- |
| defaultText | Represents the default sold out notice text. |

**Example**

```js
wp.hooks.addFilter('notice.unavailable.text', 'wpshopify', function (defaultText) {
  return 'Custom text'
})
```
