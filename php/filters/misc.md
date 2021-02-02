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

## `wpshopify_use_products_all_template`

Allows you to turn off the default products archive template. Useful if you want to use your own wordpress templates.

| Parameter           | Description                                                                  |
| :------------------ | :--------------------------------------------------------------------------- |
| use_plugin_template | Represents whether to use default products archive template. Default: `true` |

**Example**

```php
add_filter('wpshopify_use_products_all_template', function($use_plugin_template) {
   return false;
});
```

## `wpshopify_use_products_single_template`

Allows you to turn off the default products single template. Useful if you want to use your own wordpress templates.

| Parameter           | Description                                                                 |
| :------------------ | :-------------------------------------------------------------------------- |
| use_plugin_template | Represents whether to use default products single template. Default: `true` |

**Example**

```php
add_filter('wpshopify_use_products_single_template', function($use_plugin_template) {
   return false;
});
```

## `wpshopify_use_collections_all_template`

Allows you to turn off the default collections archive template. Useful if you want to use your own wordpress templates.

| Parameter           | Description                                                                     |
| :------------------ | :------------------------------------------------------------------------------ |
| use_plugin_template | Represents whether to use default collections archive template. Default: `true` |

**Example**

```php
add_filter('wpshopify_use_collections_all_template', function($use_plugin_template) {
   return false;
});
```

## `wpshopify_use_collections_single_template`

Allows you to turn off the default collections single template. Useful if you want to use your own wordpress templates.

| Parameter           | Description                                                                    |
| :------------------ | :----------------------------------------------------------------------------- |
| use_plugin_template | Represents whether to use default collections single template. Default: `true` |

**Example**

```php
add_filter('wpshopify_use_collections_single_template', function($use_plugin_template) {
   return false;
});
```
