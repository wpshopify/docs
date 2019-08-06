# Render API: Cart Icon

Please first read our [Render API](guides/render-api.md) guide first.

<span class="heading-section">📍 Building Example</span>

```php
$Cart_Icon = WP_Shopify\Factories\Render\Cart\Cart_Factory::build();
```

<span class="heading-section">🎚 Available Methods</span>

## `cart_icon()`

Displays the cart icon component

| Arguments                                                            |
| :------------------------------------------------------------------- |
| An array of [cart icon parameters](shortcodes/wps_cart_icon?id=icon) |

The arguments available are the same as the attributes used by the [[wps_cart_icon]](shortcodes/wps_cart_icon?id=icon) shortcode.

**Example**

```php
// Show cart icon with custom image
$Cart->cart_icon([
   'icon' => "https://yoursite.com/icon.svg"
]);
```
