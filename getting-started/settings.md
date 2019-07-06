# Settings

WP Shopify comes with a lot of settings. We've made a video walking through each setting in detail.

We're always adding additional settings so if you have any requests, <a href="mailto:hello@wpshop.io">please let us know!</a>

## Overriding the global settings

We've tried our best to strike a balance between what you can change _globally_, and what you can modify within shortcodes. As a general rule, any setting used within a shortcode will override the same setting that is configured globally. For example, if you turn pagination off within the global plugin settings, you can manually turn it on for a specific shortcode by settings `pagination="true"`.

## Products URL

Determines the main URL for your products. The default value is set to <span class="code-inline">/products</span>

## Collections URL

Determines the default URL for your collections. The default value is set to <span class="code-inline">/collections</span>

## Products per page

Determines how many products will show at any given time. This also adjusts the pagination accordingly.

## Webhooks callback URL

The Webhooks callback URL enables WordPress to stay in sync with Shopify. This needs to be set to a publicly accessible URL which points to your WordPress site. Note: If you're not working within a local dev environment or don't know what that means, don't change this.

## Use titles for alt attributes

This will use the product's title as the alt attribute value for images. Useful for speeding up the syncing process or if you're experiencing timeout issues during sync.

## Load cart

This will load the front-end cart experience. You can uncheck to completely remove the built-in cart. Useful for incorporating your own Shopify cart using their buy button SDK.

## Load styles

This allows you to customize which styles are loaded on the front-end.</p

## Selective sync

This allows you to sync only specific types of data. Useful for re-syncing or debugging purposes.

## Price formatting

The price formatting setting will allow you to show the currency symbol along with the price. E.g, \$100.00 USD <a href="mailto:hello@wpshop.io"></a>

## Products link to Shopify

Enabling this will link the products you display on WordPress site back to your Shopify single product pages. Keep in mind that this will only work for users not using a Shopify Lite plan.

## Show breadcrumbs

Enabling this option will show breadcrumbs for products and collections.

## Hide all pagination

When enabled, all pagination for both products and collections will be hidden.
