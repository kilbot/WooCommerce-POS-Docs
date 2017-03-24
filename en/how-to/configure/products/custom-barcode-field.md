---
title: Custom Barcode Field
description:  
tags: barcode, filters, postmeta
---

* [Select a Custom Barcode Field](#select-a-custom-barcode-field) (Pro only)
* [Add Custom Barcode](#add-custom-barcode) (Pro only)
* [Using the Meta Key Filter](#using-the-meta-key-filter)

By default, WooCommerce POS will use the SKU field as the barcode. 

![By default WooCommerce POS will use the SKU field as the barcode. ](http://wcpos.com/wp-content/uploads/2016/06/product-sku.png "By default WooCommerce POS will use the SKU field as the barcode")


### Select a Custom Barcode Field

[WooCommerce POS Pro](http://wcpos.com/pro) users can use any product meta field by selecting a Barcode Field in `WP Admin > POS > Settings > Products`. 
The select dropdown will allow you to search all existing post meta field keys. 
If the post meta field for your barcodes does not exist, you can create a custom field using the _Add new field_ link.

![Select custom barcode field in WooCommerce POS Pro](http://wcpos.com/wp-content/uploads/2017/03/set-custom-barcode-field.png "Select custom barcode field in WooCommerce POS Pro")


### Add Custom Barcode

If you select a barcode field that is not the SKU, you will have an extra field to enter your POS barcode in the product edit screen.

![Extra field for the POS barcode](http://wcpos.com/wp-content/uploads/2017/03/add-pos-barcode.png)



### Using the Meta Key Filter

Custom barcode meta fields can also be set by using the `woocommerce_pos_barcode_meta_key` filter. 

{% gist id="kilbot/88cbd3ac5613eca90eea" %}{% endgist %}