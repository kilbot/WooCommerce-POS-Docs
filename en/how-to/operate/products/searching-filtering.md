---
title: Product Searching and Filtering
description: You can use search phrases to filter products by any attribute such as id, category and type.
tags: categories, category, filtering, product-tabs, searching
---

Products are listed alphabetically by title in the Products Panel. 
Using the search field, users can apply a filter the product list. 
Simple queries will filter by product _title_, for example, searching `woo` will display all products with _woo_ in the title. 
WooCommerce POS also supports operators to make your search results more precise. 
For example, a search for `cat:music` will return all products in the music category. 
 
Below is a list of supported search operators with example usage.

* [Property Operators](#property-operators)
* [Quote Operators (")](#quote-operators)
* [Pipe Operators (|)](#pipe-operators)
* [Combinations](#combinations)


### Property Operators

Property operators can be used to filter products by property, for example, the `id`, `sku` and `categories` are considered _properties_ of the product. 
A colon is used to separate the property from the search term, eg: `property:term`.

| Property | Example Search | Result |
| - | - |
| **id** | `id:99` | Returns single product with ID = 99 |
| **sku** | `sku:123` | Returns all products that have 23 in the SKU |
| **barcode** | `barcode:123` | Returns all products that have 23 in the barcode<br>Note: the barcode will equal the SKU unless you are using a [custom barcode field](/how-to/configure/products/custom-barcode-field.md) |
| **cat** or **categories** | `cat:music` or `categories:music` | Returns all products which belong to the _Music_ category |
| **tags** | `tags:jazz` | Returns all products which are tagged _jazz_ |
| **on_sale** | `on_sale:true` | Returns all products which are currently on sale, ie: discounted |
| **featured** | `featured:true` | Returns all products which are being [featured](https://docs.woocommerce.com/document/managing-products/) |
| **type** | `type:variable` | Returns all the [variable products](https://docs.woocommerce.com/document/variable-product/) |
| **downloadable** | `downloadable:true` | Returns all the products which are [downloadable](https://docs.woocommerce.com/document/digitaldownloadable-product-handling/) |
| **virtual** | `virtual:true` | Returns all the products which are [virtual](https://docs.woocommerce.com/document/managing-products/) |
| **taxable** | `taxable:false` | Returns all the products which are not [taxable](https://docs.woocommerce.com/document/setting-up-taxes-in-woocommerce/) |
| **in_stock** | `in_stock:true` | Returns all the products which are in stock, ie: either stock is not managed, or stock quantity is greater than 0 |


### Quote Operators

Search terms that contain a space can be wrapped in quotation marks to ensure a precise match. 
For example, a search for `logo woo` will return all products with _woo_ AND _logo_ in the title. 
A search for `"logo woo"` will only return products with those precise characters in the title. 
Quotation operators are necessary for category and tag search terms which contain a space.

| Example Search | Result |
| - | - |
| `"logo woo"` | Returns exact matches in the title, eg: _Logo Woodcut_ |
| `cat:"jazz albums"` | Returns all products which belong to the _Jazz Albums_ category |
| `tags:"men's hoodie"` | Returns all products which are tagged _Men's Hoodie_ |


### Pipe Operators

A pipe can be used between search terms as a logical OR operator.
For example, a search for `woo | logo` will return all products with _woo_ OR _logo_ in the title. 
Pipe operators are necessary if you wish to filter by multiple product IDs, for example, a search for `id:93 | id:96 | id:99` will return three products (if all match).

| Example Search | Result |
| - | - |
| <code>woo &#124; logo</code> | Returns products with _woo_ OR _logo_ in the title, eg: _Woo Album_, _Woo Logo_, _Woo Ninja_ etc  |
| <code>id:93&nbsp;&#124;&nbsp;id:96&nbsp;&#124;&nbsp;id:99</code> | Returns all products with IDs 93, 96 OR 99, ie: three products |
| <code>cat:music&nbsp;&#124;&nbsp;cat:posters</code> | Returns products which belong to the _Music_ OR _Posters_ categories |


### Combinations

Search operators can be combined to further refine searches. 

| Example Search | Result |
| - | - |
| `woo cat:music` | Returns all products which belong to the _Music_ category AND have _woo_ in the title |
| <code>on_sale:true&nbsp;in_stock:true</code> | Returns all products which are on sale (discounted) AND in stock |