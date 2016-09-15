---
title: Custom Barcode Field
description:  
tags: barcode, filters, postmeta
---

By default WooCommerce POS will use the SKU field as the barcode. 

![By default WooCommerce POS will use the SKU field as the barcode. ](https://wcpos.com/wp-content/uploads/2016/06/product-sku.png "By default WooCommerce POS will use the SKU field as the barcode")

[WooCommerce POS Pro](http://wcpos.com/pro) users can use any product meta field by selecting a Barcode Field in `WP Admin > POS > Settings > General`

![Select custom barcode field in WooCommerce POS Pro](https://wcpos.com/wp-content/uploads/2016/06/select-custom-barcode-field.png "Select custom barcode field in WooCommerce POS Pro")

Custom barcode meta fields can also be set by using the `woocommerce_pos_barcode_meta_key` filter. 

{% gist id="kilbot/88cbd3ac5613eca90eea" %}{% endgist %}

{% hint style='info' %}
A barcode must be unique for each product.
{% endhint %}