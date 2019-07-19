# Common Issues

Below are the most common issues that users have when using the plugin. If you don't find and answer here, please email us [hello@wpshop.io](mailto:hello@wpshop.io)

<iframe width="860" height="515" src="https://www.youtube.com/embed/qUX-5pjvODk" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

## Products not showing

Usually this means that you just need to assign your products to the Shopify Sales Channel. This "Sales Channel" is created automatically when you [initially setup your private app](getting-started/syncing) and will have the same name. It's used to control what products are visible in WP Shopify. Below are the steps for assigning your products to the Sales Channel.

### 1. Open the product edit screen within Shopify

First, open Shopify and locate a product that you want to show on WordPress.

![Shopify product sales channel selection](https://wpshop.io/wp-content/uploads/2018/10/products-not-showing-1-1024x558.jpg)

### 2. Assign the products to the WP Shopify Sales Channel

Under Product availability, click manage and ensure that your product is assigned to the custom Sales Channel.

![Shopify Product availability](https://wpshop.io/wp-content/uploads/2018/10/products-not-showing-2-1024x558.jpg)

### 3. Click "Done"

Now head back to WordPress to see if the product shows up. Sometimes this can take up to 60 seconds.

## Syncing Issues

We've taken great steps to ensure that the syncing process works across multiple different environments. However if you're running into trouble, try going through these steps one by one.

### First things to check

1. Make sure you've set the proper [API permissions](getting-started/syncing?id=step-6) for your Shopify private app. Specifically, ensure that `Read and Write` is selected for "Product Information".
2. Try changing the [Items per request](getting-started/settings?id=items-per-request) setting to **25** and turn on [Synchronous Requests](getting-started/settings?id=synchronous-requests). After these are updated try [resyncing](getting-started/tools?id=resync-shopify).
3. Sometimes the syncing can fail due to plugin conflicts. Try deactivating all your other plugins besides WP Shopify and then [resync](getting-started/tools?id=resync-shopify).
4. Ensure your permalinks are _not_ set to Plain. Try setting them to "Post name" or "Custom structure" instead.
5. Ensure you meet the WP Shopify [minimum requirements](/getting-started/requirements).
6. Make sure you have a working SSL certificate on your WordPress site
7. Check your PHP and Apache/Nginx logs for any errors. If you don't know how to do this, contact your web host and ask them to look on your behalf. If you find any errors, please send them to us by email or in the private Slack channel for further help.
8. Ask your web host if they have a firewall enabled that restricts numerous third-party API requests during a short period of time.
9. If they do have a firewall, ask them to make an exception for requests sent to ".myshopify.com".

### Specific Syncing Errors

#### [API] This action requires merchant approval

This error occurs when you have have the incorrect permissions set for your Shopify private app. WP Shopify requires that following to be set to "Read and write":

-  Product Information
-  Customer details and customer groups
-  Orders, transactions and fulfillments
-  Price rules
-  Products, variants and collections

Be sure these permissions are set correctly and then perform a [Resync](getting-started/tools?id=resync-shopify) from within WP Shopify.

![Shopify API permissions screen](https://wpshop.io/wp-content/uploads/2018/03/api-permissions-1024x558.jpg)

#### Error: The data you're trying to sync is too large for the database to handle.

This error happens when the database is unable to handle the amount of data during sync. Usually this happens when your Shopify store either has thousands of products or thousands of product variants.

By default, there's a limit to the amount of data a MySQL server can handle for any given query. This limitation is known as the <b>max_allowed_packet</b> and you can <a href="https://dev.mysql.com/doc/refman/8.0/en/packet-too-large.html" target="_blank" rel="noopener">read more about it here</a>. WP Shopify is continuously making MySQL queries during sync, and sometimes these queries can exceed the max_allowed_packet limit if the store is very large.

The easiest fix is to adjust the "Items per request" option from within the plugin settings. Changing this from 250 to 100 usually works. Setting this lower will force the sync to make many smaller queries, so you may notice the sync taking longer to complete.

![WP Shopify items per request setting](https://wpshop.io/wp-content/uploads/2018/08/setting-items-per-request-768x638.png)

#### 400 Error: The request sent to Shopify was either malformed or corrupt.

If you see this error it usually means that there's something wrong with the JavaScript being sent to the server. <a href="https://stackoverflow.com/questions/66420/how-do-you-launch-the-javascript-debugger-in-google-chrome" target="_blank" rel="noopener">Open your browser's developer tools</a> and check the console for any errors. If you find errors, please send them to us in the <a href="https://wpshop.io/purchase" target="_blank" rel="noopener">official Slack channel</a> for further help.

#### 400 Error: The request was not understood by the server.

This error is usually returned when the Shopify connection to WordPress is either broken or invalid. Disconnecting and reconnecting the plugin from Shopify may fix the issue. For more information please see Shopify's <a href="https://help.shopify.com/api/getting-started/response-status-codes" target="_blank" rel="noopener">status codes</a>.

#### 401 Error: The necessary authentication credentials are not present in the request or are incorrect.

This error is usually returned when the private Shopify app you created was deleted somehow. Disconnecting and reconnecting the plugin from the Connect tab should fix the issue. For more information please see Shopify's <a href="https://help.shopify.com/api/getting-started/response-status-codes" target="_blank" rel="noopener">status codes</a>.

#### 402 Error: The requested shop is currently frozen.

This error is sent when a shop is either unavailable (no payment on record at Shopify), or when it doesn't have access to a specific feature. Make sure that you have an active Shopify plan and that the private app you created has been given read _and_ write access for each&nbsp;scope&nbsp;<a href="https://wpshop.io/docs/connecting" target="_blank" rel="noopener">as described in Step 6.</a> of the connecting process. Once this has been updated, resync your store from the WP Shopify settings page.

#### 403 Error: The server is refusing to respond to the request.

This error is sent when WP Shopify doesn't have access to a specific scope of your private app. Make sure that the private app you created has been given read _and_ write access for each&nbsp;scope <a href="https://wpshop.io/docs/connecting" target="_blank" rel="noopener">as described in Step 6.</a> of the connecting process.&nbsp;Once this has been updated, resync your store from the WP Shopify settings page.

#### 404 Error: The requested resource was not found.

If you receive this error make sure that your Shopify private app has enabled the setting "Allow this app to access your storefront data using the Storefront API". You can find this toward the bottom next to the Storefront API section.

#### 406 Error: The requested resource contained the wrong HTTP method or an invalid URL.

If you're experiencing this error you can be confident that it's probably a bug in the plugin. Please check your PHP / Apache / Nginx logs to see if any additional information is shown and send this information to us in the <a href="https://wpshop.io/purchase" target="_blank" rel="noopener">official Slack channel</a>. Also, here's a resource explaining how to <a href="https://codex.wordpress.org/Debugging_in_WordPress" target="_blank" rel="noopener">enable the PHP debug logging</a> if you're not sure whether it's already enabled.

#### 422 Error: The request body was well-formed but contains semantical errors.

The most common reason for this error is that the value for the setting "Webhooks callback URL" does not have "https" in it. Shopify requires that your site have a valid SSL certificate to function properly. If you don't care about the webooks and simply wish to finish the syncing, just add "https" to the "Webhooks callback URL" setting. Also, please check your PHP / Apache / Nginx logs to see if any additional information is shown and send this information to us in the <a href="https://wpshop.io/purchase" target="_blank" rel="noopener">official Slack channel</a>. Also, here's a resource explaining how to <a href="https://codex.wordpress.org/Debugging_in_WordPress" target="_blank" rel="noopener">enable the PHP debug logging</a> if you're not sure whether it's already enabled.

#### 429 Error: The request was not accepted because the application has exceeded the rate limit.&nbsp;

This error occurs because the syncing process is making too many requests to Shopify at once. You can try enabling the **"Use titles for alt attributes"** setting&nbsp;from within WP Shopify -&gt; Settings and then try resyncing. (Note: this will use the product's title as the alt attribute value for any image it may have).<br><br>Also, please check your PHP / Apache / Nginx logs to see if any additional information is shown and send this information to us in the <a href="https://wpshop.io/purchase" target="_blank" rel="noopener">official Slack channel</a>. Here's a resource explaining how to <a href="https://codex.wordpress.org/Debugging_in_WordPress" target="_blank" rel="noopener">enable the PHP debug logging</a> if you're not sure whether it's already enabled.

#### 500 Error: An internal error occurred at Shopify.

If you receive this error you should try disconnecting and reconnecting from within the WP Shopify Settings page. Sometimes this error is an indication that the Shopify servers are down so be sure to take a look at their <a href="https://status.shopify.com/" target="_blank" rel="noopener">status page</a> as well.<br><br>If this doesn't work,&nbsp;please check your PHP / Apache / Nginx logs to see if any additional information is shown and send this information to us in the <a href="https://wpshop.io/purchase" target="_blank" rel="noopener">official Slack channel</a>. Here's a resource explaining how to <a href="https://codex.wordpress.org/Debugging_in_WordPress" target="_blank" rel="noopener">enable the PHP debug logging</a> if you're not sure whether it's already enabled.

#### 501 Error: The requested endpoint is not available on that particular shop.

If you're receiving this error make sure that the private app you created has been given read _and_ write access for each&nbsp;scope <a href="https://wpshop.io/docs/connecting" target="_blank" rel="noopener">as described in Step 6.</a> of the connecting process. Once this has been updated, resync your store from the WP Shopify settings page.<br><br>If this doesn't work,&nbsp;please check your PHP / Apache / Nginx logs to see if any additional information is shown and send this information to us in the <a href="https://wpshop.io/purchase" target="_blank" rel="noopener">official Slack channel</a>. Here's a resource explaining how to <a href="https://codex.wordpress.org/Debugging_in_WordPress" target="_blank" rel="noopener">enable the PHP debug logging</a> if you're not sure whether it's already enabled.<br>

#### 503 Error: The server is currently unavailable.

When this error is thrown it usually means that either your PHP `memory_limit` or `max_execution_time` is set too low.

The simplest solution is to add the following to the bottom of your .htaccess file and re-sync.
`php_value memory_limit 256`
php_value max_execution_time 300`

If this doesn't work and you're using Nginx, ask your webhost to add the following rules within your http, location, or server blocks. A useful guide for doing this can be <a href="https://distinctplace.com/2017/04/22/nginx-upstream-timed-out/" target="_blank" rel="noopener">found here</a>.

`proxy_read_timeout 300;`
`fastcgi_read_timeout 300;`

Finally, be sure to clear the WP Shopify cache located in the Tools tab on the settings page and reconnect your Shopify store.

#### 504 Error: The request could not complete in time.

When this error is thrown it usually means that either your PHP `memory_limit` or `max_execution_time` is set too low.

The simplest solution is to add the following to the bottom of your .htaccess file and re-sync.

`php_value memory_limit` 256
`php_value max_execution_time` 300

If this doesn't work and you're using Nginx, ask your webhost to add the following rules within your http, location, or server blocks. A useful guide for doing this can be <a href="https://distinctplace.com/2017/04/22/nginx-upstream-timed-out/" target="_blank" rel="noopener">found here</a>.

`proxy_read_timeout 300;`
`fastcgi_read_timeout 300;`

Finally, be sure to clear the WP Shopify cache located in the Tools tab on the settings page and reconnect your Shopify store.

#### 504 Error: The syncing process timed out or exceeded its allocated memory.

When this error is thrown it usually means that either your PHP `memory_limit` or `max_execution_time` is set too low.

The simplest solution is to add the following to the bottom of your .htaccess file and re-sync.

`php_value memory_limit` 256
php_value max_execution_time` 300

If this doesn't work and you're using Nginx, ask your webhost to add the following rules within your http, location, or server blocks. A useful guide for doing this can be <a href="https://distinctplace.com/2017/04/22/nginx-upstream-timed-out/" target="_blank" rel="noopener">found here</a>.

`proxy_read_timeout 300;`
`fastcgi_read_timeout 300;`

Finally, be sure to clear the WP Shopify cache located in the Tools tab on the settings page and reconnect your Shopify store.

#### Error: An unknown Shopify API response was received during syncing.

If you're experiencing this error you can be confident that it's probably a bug in the plugin. Please check your PHP / Apache / Nginx logs to see if any additional information is shown and send this information to us in the <a href="https://wpshop.io/purchase" target="_blank" rel="noopener">official Slack channel</a>. Also, here's a resource explaining how to <a href="https://codex.wordpress.org/Debugging_in_WordPress" target="_blank" rel="noopener">enable the PHP debug logging</a> if you're not sure whether it's already enabled.
