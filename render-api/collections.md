# Render API: Collections

Please first read our [Render API](guides/render-api.md) guide first.

<span class="heading-section">📍 Building Example</span>

```php
$Collections = WPS\Factories\Render\Collections\Collections_Factory::build();
```

<span class="heading-section">🎚 Available Methods</span>

## `collections()`

Displays one or more collections.

| Arguments                                                                |
| :----------------------------------------------------------------------- |
| An array of [collection parameters](shortcodes/wps_collections?id=title) |

The arguments available are the same as the attributes used by the [[wps_collections]](shortcodes/wps_collections?id=title) shortcode.

**Example**

```php
global $post;

$Collections->collections([
   'title' => $post->post_title
]);
```
