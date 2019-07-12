# JavaScript Filters: Products

Please first read our [Getting started with JavaScript Hooks](guides/javascript-hooks.md) guide.

## `product.title.class`

Allows for filtering the class of the product title h2 element.

| Parameters     | Description                                  |
| :------------- | :------------------------------------------- |
| defaultClasses | Represents the current product title classes |

**Example**

```js
wp.hooks.addFilter('product.title.class', 'wpshopify', defaultClasses => {
   return defaultClasses + ' my-awesome-class'
})
```
