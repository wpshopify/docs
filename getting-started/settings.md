# Settings

WP Shopify comes with a lot of settings. We've made a video walking through each setting in detail.

We're always adding additional settings so if you have any requests, <a href="mailto:hello@wpshop.io">please let us know!</a>

## General

#### Products URL

Determines the default products page slug. Your permalinks must be set to "Post name" for this URL to work. You can set this by going to `Settings -> Permalinks`.

#### Collections URL

Determines the default collections page slug. Your permalinks must be set to "Post name" for this URL to work. You can set this by going to `Settings -> Permalinks`.

#### Disable default pages

When enabled, will remove all default plugin pages like `/products` and `/collections`.

#### Products per page

Determines how many products to show per page. Defaults to the standard WordPress post count set within `Settings - Reading`. You can also override this value within each shortcode.

#### Products link to Shopify

When enabled, all products will link directly to their corresponding Shopify product detail page (PDP). By default, the product title and product images will contain the link. Toggling this on/off will require you to clear the WP Shopify cache.

Note: will not work when Shopify store is password protected, if product is not assigned to the Online Store sales channel, or if using the Shopify Lite plan.

## Syncing

#### Items per request

Determines the number of "items" (products, collections, etc) that are transfered per second during the syncing process. Reduce this number if you're running into syncing issues.

#### Synchronous requests

When enabled, will use an alternative syncing method which is slower but sometimes more stable. Turn this on if you're running into syncing issues.

#### Lite Sync

When enabled, will skip syncing Shopify data as WordPress posts. This will instead fetch the data directly from Shopify on page load.

If you want PDP pages (product detail page), you must turn this off and manually resync your store under the Tools tab.

#### Sync posts

When enabled, will create posts from your products and collections. Turn on if you want to create PDP pages (product detail page).

#### Selective sync

Determines which type of Shopify data to sync. Defaults to `products` and `collections`.

#### Sync products by collection

Allows for syncing products that only belong to one or more specific collections.

#### Webhooks domain

The Webhooks callback URL will be the location where Shopify sends it's updates. For example, after changing Product information within Shopify, the updated data will be sent here.

You most likely want this to be the same domain as the WordPress site. This _must_ be publicly accesible. You can change this to a proxy URL during local development using something like [ngrok](https://ngrok.com/). Also, if you have WordPress installed in a subdirectory be sure to include that in the url, e.g., `https://localhost:3000/wp`

#### Sync featured images

Sync featured images will allow you to sync your Shopify images as native WordPress featured images. The image itself will be uploaded into the WordPress media library, allowing you to use standard functions like `the_post_thumbnail` and `get_the_post_thumbnail_url`.

## Pricing

#### Show compare at pricing

When enabled, all products will show the "compare at" price. Useful for enabling [Shopify sales pricing](https://help.shopify.com/en/manual/promoting-marketing/discount-codes/sales).

#### Show price ranges

When enabled, shows a product's range of variant prices. E.g., "From $1.00 - $5.00".

#### Currency display style

Determines the currency display style. For example: setting to "symbol" will display 19.99 as \$19.99. Setting to "code" will display 19.99 as USD 19.99. Setting to "name" will display 19.99 as 19.99 US dollars.

- `symbol` \$19.99
- `code` USD 19.99
- `name` 19.99 US dollars

#### Hide decimals

When enabled, will hide the decimals of prices. Useful if you want to turn your `$60.00` into `$60`.

#### Enable local currency

When enabled, shows prices in customer's local currency instead of Shopify's base currency. A valid HTTPs certificate is required.

## Layout

#### Show breadcrumbs

When enabled, will show breadcrumbs above all PDP and PLP pages.

#### Hide all pagination

When enabled, pagination will be hidden globally from all pages and shortcodes. You can still "turn on" pagination on a per shortcode basis by using the "pagination" shortcode attribute.

#### Align height

When enabled, will align the height of products and collections when viewed as lists.

## Products

#### Color: Add to cart buttons

Changes the background color of the add to cart button. Changing this value may potentially override any custom CSS from your theme.

#### Color: Variant buttons

Changes the background color of all product variant dropdowns. Changing this value may potentially override any custom CSS from your theme.

#### Show heading

Hide / show the heading found on the default Products page.

#### Heading

Changes the heading found on the default Products page.

#### Show image zoom

When enabled, will turn on an "image zoom" feature for product images. An example of how it looks [can be found here](https://imgix.github.io/drift/).

#### Custom sizing

When enabled, will "turn on" the product image sizing.

#### Image width

Sets a custom width for all product images. Maximum size of 5760 x 5760. Both the width and height values will maintain the image aspect ratio. Therefore, if you want to force all images to the same dimensions make sure to specify the crop option below as well. If you want to size by one dimension only, keep the other dimension blank.

#### Image height

Sets a custom height for all product images. Maximum size of 5760 x 5760. Both the height and height values will maintain the image aspect ratio. Therefore, if you want to force all images to the same dimensions make sure to specify the crop option below as well. If you want to size by one dimension only, keep the other dimension blank.

#### Crop position

Specify a crop parameter to make sure that the resulting image's dimensions match the requested dimensions. If the entire image won't fit in your requested dimensions, the crop parameter specifies what part of the image to show.

#### Scale

Sets a custom scale for all product images. The number here will be multiplied by the dimensions set above. For example, an image originally 450x450 will return an image 900x900 pixels. Will only scale up if the original image is large enough. If original image is too small, the closest image in size will be returned.

#### Thumbnail Custom sizing

When enabled, will "turn on" the product image thumbail sizing.

#### Thumbnail Image width

Same as :point_up: [Image width](#image-width)

#### Thumbnail Image height

Same as :point_up: [Image height](#image-height)

#### Thumbnail Crop position

Same as :point_up: [Crop position](#crop-position)

#### Thumbnail Scale

Same as :point_up: [Scale](#scale)

## Collections

#### Show heading

Hide / show the heading found on the default Collections page.

#### Heading

Changes the heading found on the default Collections page.

#### Custom sizing

When enabled, will "turn on" the collection image thumbail sizing.

#### Image width

Same as :point_up: [Image width](#image-width)

#### Image height

Same as :point_up: [Image height](#image-height)

#### Crop position

Same as :point_up: [Crop position](#crop-position)

#### Scale

Same as :point_up: [Scale](#scale)

## Cart

#### Load cart

When this is turned off, the default cart experience will _not_ load. Useful if you plan on linking products to Shopify directly.

#### Show fixed cart icon

When this is turned on, a fixed cart icon will display on the side of every page.

#### Cart terms

When enabled, generates a mandatory checkbox within the cart that must be checked before the user can proceed to checkout.

#### Cart terms text

This is the text that will show next to the terms checkbox. HTML tags `<a>`, `<b>`, `<i>`, `<em>`, and `<strong>` are allowed.

#### Cart notes

When enabled, will show an input box inside the cart that users can use to attach custom notes to an order.

#### Cart notes placeholder

The cart notes placeholder text

#### Color: Checkout button

Determines the background color for the checkout button

#### Color: Cart inline icon

Determines the color for the inline cart icon

#### Color: Cart inline counter

Determines the background color for the inline cart icon counter

#### Color: Cart fixed icon

Determines the color of the fixed cart icon

#### Color: Cart fixed counter

Determines the color of the fixed cart counter

#### Color: Cart fixed background

Determines the background color of the fixed cart icon

## Search

#### Search by

Determines the criteria by which the search term is used to find a match. Possible values are: Product title, Product tag, Product vendor, Product type, or Product variants title.

#### Search exact match

Determines whether to match exactly what the user types or not. For example when turned off, if the user types "Shoe", products with the title "Shoe" and "Shoes" will be returned.

## Checkout

#### Enable custom domain

When enabled, will use your custom primary domain (e.g., yourstore.com) when redirecting to the checkout page instead of the default `.myshopify.com` domain.

#### Checkout button target

Determines whether the checkout button will open a new tab or not. Only applicable to desktop. Mobile will always open checkout page in the current tab.

#### Direct Checkout

Direct Checkout allows you to replace the "add to cart" buttons with a link that takes the user directly to the checkout page. This is great if you don't need a cart experience and simply want to send users to pay immediately.

The main limitation with this feature at the moment is that it only works with single products. Meaning, you can’t use this to checkout with more than one product at a time. If you have two products side-by-side, both using direct checkout, they won’t share the “same” line items. Each button will take the user to a unique checkout page.

Direct Checkout can be enabled globally within the plugin settings under the "Checkout" subnav, or by using the new shortcode attribute `direct_checkout="true"`

## Plugin

#### Load styles

Allows you to specify what WP Shopify stylesheets are loaded on the front-end. Useful for users looking to customize.

#### Enable Beta Updates

When enabled, you'll gain access to WP Shopify updates before they are publicly released.
