# Tools

WP Shopify comes with various Tools to improve the plugin's flexibility. These can be found within the settings page under the "Tools" tab.

<iframe width="860" height="515" src="https://www.youtube.com/embed/0sCqDjl8uWk" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

## Resync Shopify

Allows you to sync your Shopify data. Similar to the initial sync found within the Connect tab, but it skips various steps like saving the Shopify connection.

Useful for keeping your store updated and current. For Pro users, this will still use the [Selective Sync](getting-started/settings?id=selective-sync) settings that you've chosen.

## Clear Cache

WP Shopfiy stores it's own cache to speed things up. If you're noticing that the plugin isn't behaving as expected try using this tool.

Things stored in the cache are: various shortcode settings, global settings, and generated single pages.

## Remove all synced data

This will remove all WP Shopify data from WordPress. Nothing will be changed in Shopify. Useful for removing any lingering data without reinstalling the plugin. (Note: this can take up to 60 seconds and will delete product posts and any active webhooks).

## Reconnect Automatic Post Syncing

This will reconnect the Shopify webhooks which are responsible for keeping WordPress Posts automatically in sync with Shopify. 

_This does not take effect if you're using [Lite sync](getting-started/settings?id=lite-sync)_. However if you have [Sync posts](getting-started/settings?id=sync-posts) enabled, and wish to keep this data in sync with Shopify, you can use this tool to keep the syncing updated automatically.
