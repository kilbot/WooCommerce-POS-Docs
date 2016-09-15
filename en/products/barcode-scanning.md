---
title: Barcode Scanning
description: WooCommerce POS is able to filter products by the SKU field, this allows you to instantly add products to cart using a barcode scanner.
tags: barcode, barcode-scanning, filtering, search, sku, sku-field
---

WooCommerce POS is able to filter products by the SKU field. If a search matches the barcode field exactly the product is added to the cart instantly and the search field is reset. If you have a barcode scanner that is able to populate the search field then you should be use WooCommerce POS for barcode scanning. 

To see the SKU search in action please go to http://demo.wcpos.com/pos/ 

Type (or copy & paste) `BARCODE` and an item will be added to the cart. 

Type (or copy & paste) `VARIATION1` and a variation will be added to the cart. 

![Barcode Scanning in WooCommerce POS](https://wcpos.com/wp-content/uploads/2014/07/barcode-search.png "Filtering by the SKU field in WooCommerce POS")

The following features are being planned for future releases:

*   Add products to WooCommerce using barcode scanner. This will be part of a stocktake mode being planned for a 0.3.x release.
*   Barcode scanning using mobile device camera. This will require a native WooCommerce POS app to gain access to the device hardware. Native apps are on the wish list but adding features to the web version is the highest priority at the moment.
*   Hot key activation

### Updates

**Since Version 0.3.1:** There is now a dedicated mode for Barcode scanning. You can switch between 'Search' mode and 'Scan Barcode' by clicking on the button to the left of the search field. 

![Search Scan Barcode modes](https://wcpos.com/wp-content/uploads/2014/07/search-scan-mode.png)