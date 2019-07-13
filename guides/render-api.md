# Render API

WP Shopify allows you to display your Shopify data programmatically. We call this the "Render API". The Render API is a set of PHP classes that you can leverage inside your own files. Each class has various methods which allow you to display your data. Let's see how it's done.

Watch our [quick video tutorial](https://www.youtube.com/watch?v=lYm6G35e8sI) to learn how to use this.

## Getting started

The Render API is built using a factory pattern. Therefore before we use the classes, we must first "build" them. We'll use the Products class as an example.

Start by placing the following near the top of your file:

```php
$Products = WPS\Factories\Render\Products\Products_Factory::build();
```

The `$Products` variable is now assigned an "instance" of the Render API's Products class. The build method takes no parameters and should be called directly.

See the [full list of available classes](#list-of-available-classes).

## Using the methods

Now that we have the class built, we can begin using it!

Let's say we want to show a product based on the post title. We can do so like this:

```js
global $post;

$Products->products([
   'title' => $post->post_title
]);
```

The first thing you probably noticed is that we're calling a method on our `$Products` class called "products". There are [many more methods](#list-of-available-class-methods) like this. For now, let's just walk through this example.

As you can see, we're first getting access to the WordPress post title from the global `$post` object. We then pass this value to a parameter called `title`. Each class method accepts an Array of parameters that are used to customize the output.

We've conveniently matched the Render API method parameters with the [available shortcode attributes](shortcodes/wps_products). For example, all of the `[wps_products]` shortcode attributes will work with the `Products()` method. The _are_ some parameters available only to the class method that do not exist in the shortcode. These can be very useful so we'll cover some examples below.

Finally, it's important to note that the `Products()` method is responsible for outputting one or more "full" products. By "full", we simply mean they contain all the _other_ product components like title, description, buy button, etc. Here is a [live demo](https://demo.wpshop.io/products-example/) of a "full" product.

## List of available classes

-  [Products](/)
-  [Collections](/)
-  [Search](/)
-  [Storefront](/)
-  [Cart Icon](/)

## List of available class methods

-  [Products->products()](/)
-  [Products->title()](/)
-  [Products->buy_button()](/)
-  [Products->description()](/)
-  [Products->pricing()](/)
-  [Products->gallery()](/)
-  [Collections->collections()](/)
-  [Search->search()](/)
-  [Storefront->storefront()](/)
-  [Cart->cart_icon()](/)
