# Products PHP Functions

Before using the below functions, you must properly include the WP Shopify class. See below:

## `get_product_ids_from_titles()`

Allows you to fetch a list of product ids from one or more product titles

| Argument      | Description                |
| :------------ | :------------------------- |
| productTitles | An array of product titles |

**Example**

```php
$Products = WP_Shopify\Factories\DB\Products_Factory::build();

$result = $Products->get_product_ids_from_titles(['Super awesome jacket', 'Super awesome jeans']);
```

## `get_product_ids_from_vendors()`

Allows you to fetch a list of product ids from one or more product vendors

| Argument       | Description                 |
| :------------- | :-------------------------- |
| productVendors | An array of product vendors |

**Example**

```php
$Products = WP_Shopify\Factories\DB\Products_Factory::build();

$result = $Products->get_product_ids_from_vendors(['Grant Group', 'Abbott LLC']);
```

## `get_product_ids_from_description()`

Allows you to fetch a list of product ids from a single product description.

| Argument            | Description                     |
| :------------------ | :------------------------------ |
| productDescriptions | A string of product description |

**Example**

```php
$Products = WP_Shopify\Factories\DB\Products_Factory::build();

$result = $Products->get_product_ids_from_description('Commodi autem eligendi eum nesciunt');
```

## `get_product_ids_from_types()`

Allows you to fetch a list of product ids from one or more product types

| Argument     | Description               |
| :----------- | :------------------------ |
| productTypes | An array of product types |

**Example**

```php
$Products = WP_Shopify\Factories\DB\Products_Factory::build();

$result = $Products->get_product_ids_from_types(['Tools', 'Games']);
```

## `get_product_ids_from_handles()`

Allows you to fetch a list of product ids from one or more product handles

| Argument       | Description                 |
| :------------- | :-------------------------- |
| productHandles | An array of product handles |

**Example**

```php
$Products = WP_Shopify\Factories\DB\Products_Factory::build();

$result = $Products->get_product_ids_from_handles(['super-awesome-jacket', 'super-awesome-jeans']);
```

## `get_product_ids_from_tags()`

Allows you to fetch a list of product ids from one or more product tags

| Argument       | Description              |
| :------------- | :----------------------- |
| productHandles | An array of product tags |

**Example**

```php
$Products = WP_Shopify\Factories\DB\Tags_Factory::build();

$result = $Products->get_product_ids_from_tags(['Tag1', 'Tag2']);
```

## `get_product_ids_from_post_ids()`

Allows you to fetch a list of product ids from one or more post ids

| Argument   | Description             |
| :--------- | :---------------------- |
| productIds | An array of product ids |

**Example**

```php
$Products = WP_Shopify\Factories\DB\Products_Factory::build();

$result = $Products->get_product_ids_from_post_ids([123, 456]);
```

## `get_product_ids()`

Allows you to fetch all currenly synced product ids

**Example**

```php
$Products = WP_Shopify\Factories\DB\Products_Factory::build();

$result = $Products->get_product_ids();
```

## `get_post_id_from_product_id()`

Allows you to fetch a post id from a single product ids

| Argument  | Description         |
| :-------- | :------------------ |
| productId | A single product id |

**Example**

```php
$Products = WP_Shopify\Factories\DB\Products_Factory::build();

$result = $Products->get_post_id_from_product_id(4464939827248);
```

## `get_product_from_product_id()`

Allows you to fetch product data from a single product id

| Argument  | Description         |
| :-------- | :------------------ |
| productId | A single product id |

**Example**

```php
$Products = WP_Shopify\Factories\DB\Products_Factory::build();

$result = $Products->get_product_from_product_id(4464939827248);
```

## `get_products_by_collection_id()`

Allows you to fetch a list of products from a single collection id

| Argument     | Description            |
| :----------- | :--------------------- |
| collectionId | A single collection id |

**Example**

```php
$Products = WP_Shopify\Factories\DB\Products_Factory::build();

$result = $Products->get_products_by_collection_id(164430086192);
```

## `get_products()`

Allows you to fetch all currently synced products

**Example**

```php
$Products = WP_Shopify\Factories\DB\Products_Factory::build();

$result = $Products->get_products();
```
