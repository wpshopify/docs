# [wps_cart_icon]

Displays the cart icon component.<br><br>Watch our [quick video tutorial](https://www.youtube.com/watch?v=lYm6G35e8sI) to learn how to use this.

<span class="heading-section">📍 Example Usage</span>

```js
// Overrides the default cart icon
[wps_cart_icon icon="https://yoursite.com/icon.svg"]

// Changes the icon background color
[wps_cart_icon icon_color="red"]

// Show icon without counter
[wps_cart_icon show_counter="false"]

```

<span class="heading-section">🎚 Available Attributes</span>

## `icon`

Changes the actual cart icon. Takes a URL to an icon image. Default: `false`.

```js
[wps_cart_icon icon="https://yoursite.com/icon.svg"]
```

## `icon_color`

Changes the color of the cart icon. Only works when not using the [icon](#icon) attribute. Default: `#000`.

```js
[wps_cart_icon icon_color="#FFF"]
```

## `counter_background_color`

Changes the background color of the cart counter. Default: `#6ae06a`.

```js
[wps_cart_icon counter_background_color="#FFF"]
```

## `counter_text_color`

Changes the text color of the cart counter. Default: `#000`.

```js
[wps_cart_icon counter_text_color="#FFF"]
```

## `show_counter`

Whether to display a "counter" next to the icon indicating the cart quantity. Default: `true`.

```js
[wps_cart_icon show_counter="false"]
```

## `type`

Whether to display the icon as inline or fixed. Default: `inline`.

```js
[wps_cart_icon type="fixed"]
```
