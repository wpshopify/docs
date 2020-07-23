# JavaScript Actions: Checkout

Please first read our [Getting started with JavaScript Hooks](guides/javascript-hooks.md) guide.

## `set.checkout.attributes`

Allows for setting new checkout attributes. Will completely replace the entire list of attributes. The attributes object that you pass must have a property called `key` and a property called `value`.

| Arguments  | Description                                              |
| :--------- | :------------------------------------------------------- |
| attributes | A JavaScript object which represents the new attributes. |

**Example Usage**

```js
wp.hooks.doAction('set.checkout.attributes', {
  key: 'Delivery',
  value: 'Please leave the package at the door.',
})
```

## `update.checkout.attributes`

Allows for updating existing checkout attributes. Will append the attribute to the overall checkout attributes list.

**Example Usage**

```js
wp.hooks.doAction('update.checkout.attributes', {
  key: 'Delivery',
  value: 'Please leave the package at the door.',
})
```

## `set.checkout.note`

Allows for setting a new checkout note. Will completely replace any existing checkout note.

| Arguments | Description                                    |
| :-------- | :--------------------------------------------- |
| noteValue | Represents the note value that you want to set |

**Example Usage**

```js
wp.hooks.doAction('set.checkout.note', 'This is a custom note!')
```

## `on.checkout`

Fires when the checkout button is clicked but before the redirect happens.

| Parameters | Description                                                   |
| :--------- | :------------------------------------------------------------ |
| cartState  | Represents the full cart state like lineItems, quantity, etc. |

**Example Usage**

```js
wp.hooks.addAction('on.checkout', 'wpshopify', function (cartState) {
  // Do something when the checkout begins ...
  console.log('WP Shopify Event 💥 on.checkout', cartState)
})
```

## `set.checkout.discount`

Allows for setting a discount code. Will completely replace any existing discount code already applied.

| Arguments    | Description                                               |
| :----------- | :-------------------------------------------------------- |
| discountCode | Represents the discount code you want applied as a string |

**Example Usage**

```js
wp.hooks.doAction('set.checkout.discount', 'DISCOUNT')
```

## `before.checkout.redirect`

## `on.checkout.note`

## `on.checkout.update`
