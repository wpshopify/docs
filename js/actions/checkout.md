# JavaScript Actions: Checkout

## set.checkout.attributes

Allows for setting new checkout attributes. Will completely replace the entire list of attributes. The attributes object that you pass must have a property called key and a property called value.

| Parameters | Description                                              |
| :--------- | :------------------------------------------------------- |
| attributes | A JavaScript object which represents the new attributes. |

**Example Usage**

```js
wp.hooks.doAction('set.checkout.attributes', {
   key: 'Delivery',
   value: 'Please leave the package at the door.'
})
```

## update.checkout.attributes

Allows for updating existing checkout attributes. Will append the attribute to the overall checkout attributes list.

**Example Usage**

```js
wp.hooks.doAction('update.checkout.attributes', {
   key: 'Delivery',
   value: 'Please leave the package at the door.'
})
```

## set.checkout.note

Allows for setting a new checkout note. Will completely replace any existing checkout note.

| Parameters | Description                                    |
| :--------- | :--------------------------------------------- |
| noteValue  | Represents the note value that you want to set |

**Example Usage**

```js
wp.hooks.doAction('set.checkout.note', 'This is a custom note!')
```

# on.checkout

Fires when the checkout button is clicked.

| Parameters    | Description                                                 |
| :------------ | :---------------------------------------------------------- |
| checkoutState | Represents the checkout data like lineItems, quantity, etc. |

**Example Usage**

```js
wp.hooks.addAction('on.checkout', 'wpshopify', function(checkoutState) {
   // Do something on checkout ...
})
```
