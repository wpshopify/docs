# Getting started with JavaScript Hooks

JavaScript hooks were introduce in WordPress version `5.0` with the advent of the highly anticipated Gutenberg release. These hooks are very similar to the standard PHP hooks that WordPress developers have been familiar with for years.

Like PHP hooks, these JavaScript-based hooks allow you to "filter" data and listen to unique "actions". This guide won't be a comprehensive tutorial on how to use WordPress hooks. For that, please take a look at the [official WordPress documentation](https://developer.wordpress.org/block-editor/packages/packages-hooks/) first.

WP Shopify provides many JavaScript hooks allowing you to hook into various parts of the plugin. This enables you to do things such as detect when the cart opens, or when the user clicks the checkout button. You can then run your own code from a callback function to make any customizations you want. Let's see how this works.

## Setting things up

WP Shopify injects it's JavaScript in the footer to improve performance. However it's possible that your theme's JavaScript may run _before_ WP Shopify. If this occurs, none of the custom JavaScript hooks you write will work.

To get around this, be sure to set `wpshopify-public` as a dependency in your theme's wp_enqueue_script, like this:

```php
wp_enqueue_script( 'your-js', '<your path>/stuff.js', ['wpshopify-public'], true);
```

## Adding actions

Let's say we want to detect when a product is added to the cart. We can do this by hooking into the [after.product.addToCart](js/actions/products?id=afterproductaddtocart) action like this:

```js
wp.hooks.addAction('after.product.addToCart', 'wpshopify', function (lineItem, productVariant) {
  // Do something after adding to cart ...
  console.log('lineItem :: ', lineItem)
  console.log('productVariant :: ', productVariant)
})
```

The `after.product.addToCart` action is given two parameters `lineItem` and `productVariant` that you can inspect. Each hook will have useful parameters like this to aid you along the way.

We've listed all of the [available JavaScript hooks](#list-of-available-hooks) in this documentation.

## Adding filters

Let's say we want to change the text of the checkout button. We can do this by hooking into the [default.cart.checkout.text](js/filters/cart?id=defaultcartcheckouttext) filter like this:

```js
wp.hooks.addFilter('default.cart.checkout.text', 'wpshopify', function (buttonText) {
  return 'New checkout button text'
})
```

## List of available hooks

### Actions

- [on.cart.toggle](js/actions/cart?id=oncarttoggle)
- [cart.toggle](/js/actions/cart?id=carttoggle)
- [before.cart.ready](/js/actions/cart?id=beforecartready)
- [after.cart.ready](/js/actions/cart?id=aftercartready)
- [show.cart.title](/js/actions/cart?id=showcarttitle)
- [show.cart.close](/js/actions/cart?id=showcartclose)
- [on.checkout](/js/actions/checkout?id=oncheckout)
- [on.checkout.note](/)
- [on.checkout.update](/)
- [on.checkout.note](/)
- [before.checkout.redirect](/)
- [before.payload.update](/js/actions/misc?id=beforepayloadupdate)
- [after.payload.update](/js/actions/misc?id=afterpayloadupdate)
- [product.addToCart](/)
- [after.product.addToCart](/)
- [before.product.variantDropdown.toggle](/)
- [after.product.variant.selection](/)
- [before.product.addToCart](/)

### Filters

- [default.cart.title](js/filters/cart?id=defaultcarttitle)
- [default.cart.checkout.text](js/filters/cart?id=defaultcartcheckouttext)
- [cart.lineItems.link](js/filters/cart?id=cartlineItemslink)
- [cart.lineItems.disableLink](js/filters/cart?id=cartlineItemsdisableLink)
- [cart.lineItems.maxQuantity](js/filters/cart?id=cartlineItemsmaxQuantity)
- [cart.lineItems.minQuantity](js/filters/cart?id=cartlineItemsminQuantity)
- [cart.lineItems.quantityStep](js/filters/cart?id=cartlineItemsquantityStep)
- [default.cart.notes.label](js/filters/cart?id=defaultcartnoteslabel)
- [cart.note.placeholder](js/filters/cart?id=cartnoteplaceholder)
- [cart.empty.text](js/filters/cart?id=cartemptytext)
- [cart.subtotal.text](js/filters/cart?id=cartsubtotaltext)
- [cart.lineItem.remove.text](js/filters/cart?id=cartlineItemremovetext)
- [cart.lineItem.price.sale](js/filters/cart?id=cartlineItempricesale)
- [cart.lineItem.title.text](js/filters/cart?id=cartlineItemtitletext)
- [cart.lineItem.variant.title](js/filters/cart?id=cartlineItemvarianttitle)
- [before.cart.checkout.button](js/filters/cart?id=beforecartcheckoutbutton)
- [after.cart.checkout.button](js/filters/cart?id=aftercartcheckoutbutton)
- [before.cart.title](js/filters/cart?id=beforecarttitle)
- [after.cart.title](js/filters/cart?id=aftercarttitle)
- [before.checkout.lineItems](js/filters/checkout?id=beforecheckoutlineItems)
- [global.loading.text](js/filters/global?id=globalloadingtext)
- [misc.inventory.leftInStock.total](js/filters/misc?id=miscinventoryleftInStocktotal)
- [misc.link.target](js/filters/misc?id=misclinktarget)
- [misc.layout.mobileColumns](js/filters/misc?id=misclayoutmobileColumns)
- [notice.storefront.noGroup.text](js/filters/notices?id=noticestorefrontnoGrouptext)
- [notice.product.addToCart.text](js/filters/notices?id=noticeproductaddToCarttext)
- [notice.unavailable.text](js/filters/notices?id=noticeunavailabletext)
- [pagination.loadMore.text](js/filters/pagination?id=paginationloadMoretext)
- [products.buyButton.unavailable.html](js/filters/product-buy-button?id=productsbuyButtonunavailablehtml)
- [products.variant.title.text](js/filters/product-buy-button?id=productsvarianttitletext)
- [products.quantity.label.text](js/filters/product-buy-button?id=productsquantitylabeltext)
- [product.variant.styles.colorSwatch.names](js/filters/product-buy-button?id=productvariantstylescolorSwatchnames)
- [product.variant.styles.colorSwatch.value](js/filters/product-buy-button?id=productvariantstylescolorSwatchvalue)
- [product.variant.styles](js/filters/product-buy-button?id=productvariantstyles)
- [product.addToCart.text](js/filters/product-buy-button?id=productaddToCarttext)
- [product.missingSelection.text](js/filters/product-buy-button?id=productmissingSelectiontext)
- [before.product.buyButton](js/filters/product-buy-button?id=beforeproductbuyButton)
- [after.product.buyButton](js/filters/product-buy-button?id=afterproductbuyButton)
- [buyButton.quantityStep](js/filters/product-buy-button?id=buyButtonquantityStep)
- [default.image.zoom.options](js/filters/product-images?id=defaultimagezoomoptions)
- [misc.pricing.defaultCurrencyCode](js/filters/product-pricing?id=miscpricingdefaultCurrencyCode)
- [product.pricing.from.text](js/filters/product-pricing?id=productpricingfromtext)
- [product.title.class](js/filters/product-title?id=producttitleclass)
- [product.title.text](js/filters/product-title?id=producttitletext)
- [before.product.title](js/filters/product-title?id=beforeproducttitle)
- [after.product.title](js/filters/product-title?id=afterproducttitle)
- [search.placeholder.text](js/filters/search?id=searchplaceholdertext)
- [default.storefront.tags.heading](js/filters/storefront?id=defaultstorefronttagsheading)
- [default.storefront.vendors.heading](js/filters/storefront?id=defaultstorefrontvendorsheading)
- [default.storefront.types.heading](js/filters/storefront?id=defaultstorefronttypesheading)
- [storefront.group.loading.text](js/filters/storefront?id=storefrontgrouploadingtext)
- [storefront.selections.filter.label](js/filters/storefront?id=storefrontselectionsfilterlabel)
- [storefront.selections.clear.text](js/filters/storefront?id=storefrontselectionscleartext)
- [storefront.selections.type.text](js/filters/storefront?id=storefrontselectionstypetext)
- [storefront.selections.available.text](js/filters/storefront?id=storefrontselectionsavailabletext)
- [storefront.sorting.label.text](js/filters/storefront?id=storefrontsortinglabeltext)
- [storefront.sorting.default.text](js/filters/storefront?id=storefrontsortingdefaulttext)
- [storefront.sorting.price.text](js/filters/storefront?id=storefrontsortingpricetext)
- [storefront.sorting.priceReverse.text](js/filters/storefront?id=storefrontsortingpriceReversetext)
- [storefront.sorting.newArrival.text](js/filters/storefront?id=storefrontsortingnewArrivaltext)
- [storefront.sorting.bestSelling.text](js/filters/storefront?id=storefrontsortingbestSellingtext)
- [storefront.sorting.title.text](js/filters/storefront?id=storefrontsortingtitletext)
- [storefront.sorting.titleReverse.text](js/filters/storefront?id=storefrontsortingtitleReversetext)
