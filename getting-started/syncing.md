# Syncing

Syncing your Shopify store to WordPress is pretty straight forward. However it does require a little bit of configuration. We've made a short video below that will walk you through the entire process.

<iframe width="860" height="515" src="https://www.youtube.com/embed/lYm6G35e8sI" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

### Step 1.

Install WP Shopify and navigate to the "Connect" tab within the plugin Settings.

![WP Shopify Syncing Step 1](http://localhost:4000/assets/syncing-step1.png)

### Step 2.

Open your Shopify dashboard and click "Apps" within the side menu.

![WP Shopify Syncing Step 2](http://localhost:4000/assets/syncing-step2.png)

### Step 3.

Next, click on the "Manage private apps" link towards the bottom of the new screen.

![WP Shopify Syncing Step 3](http://localhost:4000/assets/syncing-step3.png)

### Step 4.

Click "Create a new private app"

![WP Shopify Syncing Step 4](http://localhost:4000/assets/syncing-step4.png)

### Step 5.

Next, fill in the "Private app name" field. This can be anything you want. We'll use "WP Shopify" so it's easy to distinguish itself from other apps. Fill in your own email within the "Emergency developer email" field.

![WP Shopify Syncing Step 5](http://localhost:4000/assets/syncing-step5.png)

### Step 6.

Make sure that all Admin API permissions are set to "Read and write". You'll also need to click the "Review disabled Admin permissions" to see the rest.

If a permission does not have "Read and write" as an option, choose "Read" instead.

The following permissions can remain set to "No access":

-  Shopify payments balance & payouts
-  Shopify payments disputes
-  Shopify payments bank accounts
-  Shopify payments account, settings, and banking details

You can leave "Webhook API version" alone.

![WP Shopify Syncing Step 6](http://localhost:4000/assets/syncing-step6.png)

### Step 7.

Almost done!

Scroll to the bottom to find the section titled, "Storefront API". Click the checkbox that says: "Allow this app to access your storefront data using the Storefront API". Then, make sure all of the checkboxes are enabled including "Read product tags" and "Read customer tags". Click save.

![WP Shopify Syncing Step 7](http://localhost:4000/assets/syncing-step7.png)

### Step 8.

A modal should appear asking you to confirm. Click "I understand, create the app.".

![WP Shopify Syncing Step 8](http://localhost:4000/assets/syncing-step8.png)

### Step 9.

You should see a newly created Storefront access token. Take note of this value.

![WP Shopify Syncing Step 9](http://localhost:4000/assets/syncing-step9.png)

### Step 10.

Next, go back to WordPress and begin filling in the API credentials generated from the Private App. Once done, click "Connect your Shopify store".

![WP Shopify Syncing Step 10](http://localhost:4000/assets/syncing-step10.png)
![WP Shopify Syncing Step 10-2](http://localhost:4000/assets/syncing-step10-2.png)

### Step 11.

The plugin should begin syncing your store data. Depending on how many products you have, the syncing process can take anywhere from 30 seconds to 10minutes. Once the syncing is finished you should see a "completed" message.

You're now ready to start showing your products.

![WP Shopify Syncing Step 11](http://localhost:4000/assets/syncing-step11.png)

<br><br><br>
Next: :point_right: [Displaying your products](getting-started/displaying)
