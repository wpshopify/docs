# Add back to site link to checkout page

One very common requirement is to add a "back to site" link to the Shopify checkout confirmation page. Unfourtantely Shopify doesn't provide something like this out of the box, so you need to add it yourself. Thankfully it's fairly easy to do!

> [!NOTE|className:warning sm]
> This will only show on the checkout confirmation / order status page.

## Find the checkout settings

Within the Shopify dashboard, go to your store Settings and open the Checkout section. From there, find the "Order processing" area.

![WP Shopify Sync the Detail Pages](https://wpshop.io/wp-content/uploads/2021/02/back-to-cart-1.jpg)

![WP Shopify Sync the Detail Pages](https://wpshop.io/wp-content/uploads/2021/02/back-to-cart-2.jpg)

![WP Shopify Sync the Detail Pages](https://wpshop.io/wp-content/uploads/2021/02/back-to-cart-4.jpg)

## Add the custom JavaScript

Within Order processing, find the _**Additional scripts**_ section. Any customizations you add here will show on the checkout page. You can add any valid HTML (including script tags), liquid code, etc. Shopify does a great job of explaining how this works in detail [here](https://help.shopify.com/en/manual/orders/status-tracking/customize-order-status#add-additional-scripts).

For our purposes, we want to add a piece of JavaScript that will add a little HTML to the page for us. This HTML will contain a link pointing back to our WordPress site.

![WP Shopify Sync the Detail Pages](https://wpshop.io/wp-content/uploads/2021/02/back-to-cart-3.jpg)

> [!NOTE|className:warning sm]
> If you have existing code inside Additional scripts, place this at the very bottom below everything else.

Place the below code inside Additional scripts (including the script tags) and click save.

```html
<script>
  var element = document.querySelector('.main__header .logo');

  if (element) {
    element.insertAdjacentHTML(
      'beforebegin',
      '<a href="https://google.com" style="display:block;margin-bottom:0px;margin-bottom:15px;">< Back to site</a>'
    );
  }
</script>
```

## Confirm that it shows

The final step is to confirm that the back to site link is showing up. Navigate to your checkout confirmation page and look toward the top left. You should see it there.

If you'd like to have the link show somewhere else on the page, you'll need to modify the `document.querySelector` in the above code. You can always email us at hello@wpshop.io for additional help.

![Order status page with back to site link](https://wpshop.io/wp-content/uploads/2021/02/back-to-cart-5.jpg)
