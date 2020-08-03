# Add filter and sorting to products

WP Shopify Pro comes with the ability to add filter and sorting functionality to your products. To accomplish this, you’ll need to use the `[wps_storefront]` shortcode and a little HTML.

## Add the shortcode

Open the page that you wish the products to show and add the below shortcode:

```
[wps_storefront dropzone_payload="#wps-storefront-dropzone-payload" dropzone_options="#wps-storefront-dropzone-options" dropzone_selections="#wps-storefront-dropzone-selections" dropzone_page_size="#wps-storefront-dropzone-page-size" dropzone_sorting="#wps-storefront-dropzone-sorting" show_featured_only="true" items_per_row="4" excludes="description"]
```

## Add the HTML

Once you have the shortcode added to your page, insert the below HTML as well. If you're using a page builder, you can do this by adding an HTML block or module.

```html
<style>
  .wps-row {
    display: flex;
    align-items: flex-start;
  }

  #wps-storefront-dropzone-options {
    width: 250px;
    position: sticky;
    top: 25px;
  }

  #wps-storefront-dropzone-payload,
  #wps-storefront-dropzone-selections {
    flex: 1;
  }

  #wps-storefront-dropzone-selections {
    min-height: 80px;
    margin-top: -57px;
    display: flex;
    align-items: flex-end;
  }

  #wps-storefront-controls {
    width: 400px;
  }

  #wps-storefront-dropzone-payload {
    margin-top: 63px;
  }

  #wps-storefront-dropzone-page-size {
    margin-left: 30px;
  }

  .wps-storefront-heading {
    margin-bottom: 15px;
  }

  #wps-storefront-dropzone-payload .wps-items-list {
    max-width: 860px;
    margin: 0 auto;
    margin-right: 0;
  }
</style>

<section id="wps-storefront">
  <div class="wps-row">
    <div id="wps-storefront-dropzone-selections"></div>

    <div id="wps-storefront-controls">
      <div class="wps-row">
        <div id="wps-storefront-dropzone-sorting"></div>
        <div id="wps-storefront-dropzone-page-size"></div>
      </div>
    </div>
  </div>

  <div class="wps-row">
    <div id="wps-storefront-dropzone-options"></div>
    <div id="wps-storefront-dropzone-payload"></div>
  </div>

  <div class="wps-row">
    <div id="wps-storefront-dropzone-pagination"></div>
  </div>
</section>
```
