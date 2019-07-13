# Render API: Products

Please first read our [Render API](guides/render-api.md) guide first.

<span class="heading-section">📍 Building Example</span>

```php
$Products = WPS\Factories\Render\Products\Products_Factory::build();
```

<span class="heading-section">🎚 Available Methods</span>

## `products()`

Displays one or more product components.

| Arguments                                                          |
| :----------------------------------------------------------------- |
| An array of [product parameters](shortcodes/wps_products?id=title) |

The arguments available are the same as the attributes used by the [[wps_products]](shortcodes/wps_products?id=title) shortcode.

**Example**

```php
global $post;

$Products->products([
   'title' => $post->post_title
]);
```

## `title()`

Displays one or more product title components.

| Arguments                                                                      |
| :----------------------------------------------------------------------------- |
| An array of [product title parameters](shortcodes/wps_products_title?id=title) |

The arguments available are the same as the attributes used by the [[wps_products_title]](shortcodes/wps_products_title?id=title) shortcode.

**Example**

```php
global $post;

$Products->title([
   'title' => $post->post_title
]);
```

## `description()`

Displays one or more product description components.

| Arguments                                                                                  |
| :----------------------------------------------------------------------------------------- |
| An array of [product description parameters](shortcodes/wps_products_description?id=title) |

The arguments available are the same as the attributes used by the [[wps_products_description]](shortcodes/wps_products_description?id=title) shortcode.

**Example**

```php
global $post;

$Products->description([
   'title' => $post->post_title
]);
```

## `buy_button()`

Displays one or more product buy button components.

| Arguments                                                                                |
| :--------------------------------------------------------------------------------------- |
| An array of [product buy button parameters](shortcodes/wps_products_buy_button?id=title) |

The arguments available are the same as the attributes used by the [[wps_products_buy_button]](shortcodes/wps_products_buy_button?id=title) shortcode.

**Example**

```php
global $post;

$Products->buy_button([
   'title' => $post->post_title
]);
```

## `pricing()`

Displays one or more product pricing components.

| Arguments                                                                          |
| :--------------------------------------------------------------------------------- |
| An array of [product pricing parameters](shortcodes/wps_products_pricing?id=title) |

The arguments available are the same as the attributes used by the [[wps_products_pricing]](shortcodes/wps_products_pricing?id=title) shortcode.

**Example**

```php
global $post;

$Products->pricing([
   'title' => $post->post_title
]);
```

## `gallery()`

Displays one or more product gallery components.

| Arguments                                                                          |
| :--------------------------------------------------------------------------------- |
| An array of [product gallery parameters](shortcodes/wps_products_gallery?id=title) |

The arguments available are the same as the attributes used by the [[wps_products_gallery]](shortcodes/wps_products_gallery?id=title) shortcode.

**Example**

```php
global $post;

$Products->gallery([
   'title' => $post->post_title
]);
```
