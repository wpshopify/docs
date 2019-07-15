# Tools

WP Shopify comes with various Tools to improve the plugin's flexibility. These can be found within the settings page under the "Tools" tab.

## Resync Shopify

Allows you to sync your Shopify data. Similar to the initial sync found within the Connect tab, but it skips various steps like saving the Shopify connection.

Useful for keeping your store updated and current. For Pro users, this will still use the [Selective Sync](getting-started/settings?id=selective-sync) settings that you've chosen.

## Clear Cache

WP Shopfiy stores it's own cache to speed things up. If you're noticing that the plugin isn't behaving as expected try using this tool.

Things stored in the cache are: various shortcode settings, global settings, and generated single pages.

## Remove all synced data

This will remove all WP Shopify data from WordPress. Nothing will be changed in Shopify. Useful for removing any lingering data without reinstalling the plugin. (Note: this can take up to 60 seconds and will delete product posts and any active webhooks).

## Reconnect Automatic Syncing

This will reconnect the Shopify webhooks which are responsible for the automatic sync feature. Useful if you notice your data not auto syncing correctly or if you've upgraded from the free version.
