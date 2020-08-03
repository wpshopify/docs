# Fix SG Optimizer Conflict

If you're using the SG Optimizer plugin because you're using [SiteGround web hosting](https://www.siteground.com/index.htm?afcode=6f709cddc22520adccecb68901d1eb80), you'll need to add a PHP snippet to your `functions.php` file to fix loading issues.

By default, the SG Optimizer plugin will attempt to modify the WP Shopify JavaScript to improve performance. However, since these improvements are already made in WP Shopify itself, we can turn the SG optimizations off.

## Add snippet to functions.php

Open your `functions.php` file inside your WordPress theme and add the following:

```php
function wpshopify_sg_exclude_handles($exclude_list) {

   $exclude_list[] = 'wpshopify-runtime';
   $exclude_list[] = 'wpshopify-vendors-public';
   $exclude_list[] = 'wpshopify-public';

   return $exclude_list;
}

add_filter( 'sgo_js_minify_exclude', 'wpshopify_sg_exclude_handles' );
add_filter( 'sgo_js_async_exclude', 'wpshopify_sg_exclude_handles' );
add_filter( 'sgo_javascript_combine_exclude', 'wpshopify_sg_exclude_handles' );
```
