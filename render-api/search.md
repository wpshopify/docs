# Render API: Search

Please first read our [Render API](guides/render-api.md) guide first.

<span class="heading-section">📍 Building Example</span>

```php
$Search = WPS\Factories\Render\Search\Search_Factory::build();
```

<span class="heading-section">🎚 Available Methods</span>

## `search()`

Displays the search component.

| Arguments                                                         |
| :---------------------------------------------------------------- |
| An array of [search parameters](shortcodes/wps_search?id=sort_by) |

The arguments available are the same as the attributes used by the [[wps_search]](shortcodes/wps_search?id=sort_by) shortcode.

**Example**

```php
// Sort search results by price
$Search->search([
   'sort_by' => 'price'
]);
```
