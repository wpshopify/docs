# [wps_cart_icon]

Displays the cart "icon" component.

## 🎯 Example Usage

```js
// Defaults to showing titles for the latest 10 products
[wps_cart_icon]

// Show titles for products with vendors "Apple"
[wps_cart_icon vendor="Apple"]

// Show titles for products with tags "tag-a", "tag-b", or "tag-c"
[wps_cart_icon tag="tag-a, tag-b, tag-c"]

```

## ⚡️ Available Attributes

### `icon`

Changes the actual cart icon. Takes a URL to an icon which will be passed to an `<img>` tag.

Default: `false`

```js
[wps_cart_icon icon="https://yoursite.com/icon.svg"]
```

### `icon_color`

Changes the color of the cart icon.

Default: `#000`

```js
[wps_cart_icon icon_color="#FFF"]
```

### `counter_background_color`

Changes the background color of the cart counter.

Default: `#6ae06a`

```js
[wps_cart_icon counter_background_color="#FFF"]
```

### `counter_text_color`

Changes the text color of the cart counter.

Default: `#000`

```js
[wps_cart_icon counter_text_color="#FFF"]
```

### `show_counter`

Whether to display a "counter" next to the icon indicating the cart quantity.

Default: `true`

```js
[wps_cart_icon show_counter="false"]
```

### `type`

Whether to display the icon as inline or fixed.

Default: `inline`

```js
[wps_cart_icon type="fixed"]
```
