# Cross-domain Tracking

WP Shopify Pro comes with the ability to enable GA cross-domain tracking. The process has a few components to it, let's get started!

## Adding the snippets

First, you’ll need to add the GTM tracking code to **both** your WordPress and Shopify sites. To add it within Shopify, you’ll need to place the embed code within the "Additional scripts" section of the Shopify checkout settings.

## Configuring the snippets

Once you have the snippets added to both your WordPress and Shopify sites, you'll need to edit them to include the **GA Linker plugin**. This is responsible for passing the tracking cookie from WordPress to Shopify. You can do this by setting the "domains" key inside the embed code.

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

You'll want to replace `yoursite.com` and `checkout.yoursite.com` with your WordPress and Shopify domains. The Shopify domain is usually the `.myshopify.com` domain unless you have a custom domain configured. If you have a custom domain, then you'll want to add both. Like this:

```js
['wordpresssite.com', 'checkout.myshopify.com', 'customshopify.com'];
```

## Add domains to the referral exclusion list

The Google Analytics Referral exclusion list is used when you enable cross-domain tracking so that multiple sessions aren't created when a user interacts with more than one of your domains in a single session.

For example, if your Google Analytics is setup for the WordPress domain, and you don't want to trigger a new session when users land on the Shopify checkout page, you'll need to add the Shopify checkout domain to this list.

[Referral exclusion list tutorial](https://support.google.com/analytics/answer/2795830?hl=en)
