---
title: Products
description:  
tags: 
---

Your products will appear in the left panel on the main POS page. 
Products are organised alphabetically by _title_ in an infinitely scrolling list. 
WooCommerce POS will immediately download the first 10 products from your inventory. 
As you use the POS more products are downloaded and stored locally in the browser. 
Storing the products in the browser reduces the number of server requests, making product search much faster.

The product panel consists of:

* [Search Bar](#search-bar)
* [Product Tabs](#product-tabs)
* [Products List](#products-list)
* [Status Bar](#status-bar)

![An example of the Product Panel](http://wcpos.com/wp-content/uploads/2017/03/products-panel.png)


### Search Bar

The search field can be used to query your product list. 
Simple search queries will filter by product _title_. 
[Search operators](./products/searching-filtering.md) can also be used to further refine your search. 

To the left of the search field is the **search mode button**. 
Clicking the button will open the search mode options. 
You can also switch between search modes using [HotKeys](./hotkeys.md), eg: `shift+B`.
Searching in [_Barcode Mode_](./products/barcode-scanning.md) triggers some extra functionality required for barcode scanners.

![Search mode menu](http://wcpos.com/wp-content/uploads/2017/03/scan-barcode.png)

To the right of the search field is the **sync button**. 
Clicking this button will check the server for any updated products. 
You can also trigger the sync using a [HotKey](./hotkeys.md), eg: `shift+S`.


### Product Tabs

Product tabs provide a quick way to apply filters to your product list. 
WooCommerce POS is configured with three tabs by default. 
Custom tabs can be configured in the [product settings](/how-to/configure/products/tabs.md) using [search phrases](./products/searching-filtering.md). 


### Products List

Your products are organised alphabetically by _title_ in an infinitely scrolling list. 
WooCommerce POS currently supports _simple_ and _variable_ products. 
Simple products can be added to the cart using the green `+` button. 
For variable products, the _variations_ can be accessed using the `>` button, or by clicking on the 'Expand' link.

![Example of the Product List with simple and variable products](http://wcpos.com/wp-content/uploads/2017/03/product-list.png)


### Status Bar

The status bar shows the current number of products in the product list.