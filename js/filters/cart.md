# JavaScript Filters: Cart

Please first read our [Getting started with JavaScript Hooks](guides/javascript-hooks.md) guide.

## `default.cart.title`

Allows you to change the default cart title.

| Parameter | Description                       |
| :-------- | :-------------------------------- |
| title     | Represents the current cart title |

**Example**

```js
wp.hooks.addFilter('default.cart.title', 'wpshopify', title => {
   return 'New cart title'
})
```

## `default.cart.checkout.text`

Allows you to change the default checkout button text.

**Example**

| Parameter  | Description                                 |
| :--------- | :------------------------------------------ |
| buttonText | Represents the current checkout button text |

```js
wp.hooks.addFilter('default.cart.checkout.text', 'wpshopify', buttonText => {
   return 'New checkout button text'
})
```
