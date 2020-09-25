# Misc PHP Filters

These filter hooks can be added to your theme's functions.php file.

## `wpshopify_skip_compatibility`

Allows you to turn off compatibility mode. Useful if you're running into errors.

| Parameter   | Description                                                     |
| :---------- | :-------------------------------------------------------------- |
| should_skip | Represents whether to skip compatibility mode. Default: `false` |

**Example**

```php
add_filter('wpshopify_skip_compatibility', function($should_skip) {
   return true;
});
```
