# Render API: Storefront

Please first read our [Render API](guides/render-api.md) guide first.

<span class="heading-section">📍 Building Example</span>

```php
$Storefront = WPS\Factories\Render\Storefront\Storefront_Factory::build();
```

<span class="heading-section">🎚 Available Methods</span>

## `storefront()`

Displays the storefront component.

| Arguments                                                                                   |
| :------------------------------------------------------------------------------------------ |
| An array of [storefront parameters](shortcodes/wps_storefront?id=dropzone_payload-required) |

The arguments available are the same as the attributes used by the [[wps_storefront]](shortcodes/wps_storefront?id=dropzone_payload-required) shortcode.

**Example**

```php
// Sort search results by price
$Search->search([
   'dropzone_payload' => '#payload-container',
   'dropzone_options' => '#options-container',
   'dropzone_selections' => '#selections-container',
   'page_size' => 6
]);
```
