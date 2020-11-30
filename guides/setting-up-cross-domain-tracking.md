# Google Analytics

# Google Tag Manager

WP Shopify Pro comes with the ability to enable cross-domain tracking. This allows you to attribute sales to the WordPress site when they occur on the Shopify checkout page.

The process has a few components to it, let's get started!

## Configuring the snippet

Once you have the snippet added to both your WordPress and Shopify sites, you'll need to edit them to include the "GA Linker plugin". This is responsible for passing the tracking cookie from WordPress to Shopify. You can do this by setting the "domains" key inside the embed code.

Here’s an example of how it should roughly look:

```js
<script async src="https://www.googletagmanager.com/gtag/js?id=UA-XXXXXXXXX-X"></script>
<script>
   window.dataLayer = window.dataLayer || [];
   function gtag(){dataLayer.push(arguments);}
      gtag('js', new Date());
      gtag('config', 'XXXXXXXXX-X', {
      'linker': {
         'domains': ['yoursite.com', 'checkout.yoursite.com']
      }
   });
</script>
```

Notice this part specifically:

```js
linker: {
   domains: ['yoursite.com', 'checkout.myshopify.com'],
}
```

You'll want to replace `yoursite.com` and `checkout.yoursite.com` with your WordPress domain, and the domain you're using on the Shopify checkout page. Note: this is usually the `.myshopify.com` domain unless you have a custom domain configured.

## Adding the GTM snippet to your sites

First, you’ll need to add the GTM tracking code to **both** your WordPress and Shopify sites. To add it within Shopify, you’ll need to place the embed code within the "Additional scripts" section of the Shopify checkout settings.

## Referral exclusion list

The Google Analytics Referral exclusion list is used when you enable cross-domain tracking so that multiple sessions aren't created when a user interacts with more than one of your domains in a single session.

For example, if your Google Analytics is setup for the WordPress domain, and you don't want to trigger a new session when users land on the Shopify checkout page, you'll need to add the Shopify checkout domain to this list.

[Referral exclusion list tutorial](https://support.google.com/analytics/answer/2795830?hl=en)
