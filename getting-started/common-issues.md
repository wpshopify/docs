# Common Issues

Below are some common issues users have when using the plugin

## Products Not Showing

## Syncing Errors

We've taken great steps to ensure that the syncing process works across multiple different environments. However sometimes a web host may have certain restrictions in place that prevent the process from finishing successfully.

If you're not finding a particular syncing error in the list below, please open an issue on the official WordPress.org forums here: https://wordpress.org/plugins/wpshopify/ . You can also [purchase](https://wpshop.io/purchase) a WP Shopify Pro license to receive dedicated live support in our private Slack channel.

### First things to check

1. Make sure you've set the proper API permissions for your Shopify private app. Specifically, ensure that `Read and Write` is selected for "Product Information".
2. Ensure you meet WP Shopifys minimum requirements.
3. Check your PHP and Apache/Nginx logs to see if any errors are shown. If you don't know how to do this, contact your web host and ask them to look on your behalf. If you find any errors please send them to us by email or in the private Slack channel for further help.
4. Ask your web host if they have a firewall enabled that restricts numerous third-party API requests during a short period of time.
5. If they do have a firewall, ask them to make an exception for requests sent to ".myshopify.com". Afterwards, try resyncing to see if that solves the issue.
6. Make sure you have a working SSL certificate on your WordPress site. This is necessary for any changes made post-sync to show up in WordPress. If you're working in a local dev environment take a look at Ngrok.
