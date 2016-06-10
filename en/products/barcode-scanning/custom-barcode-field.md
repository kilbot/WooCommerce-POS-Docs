---
title: Custom Barcode Field
description:  
tags: barcode, filters, postmeta
---

By default WooCommerce POS will use the SKU field as the barcode. If you wish to use a custom barcode field you can use the `woocommerce_pos_product_barcode` filter combined with the [get_post_meta](https://codex.wordpress.org/Function_Reference/get_post_meta) function. See below for an example of how you might use your own custom barcode field. 

https://gist.github.com/kilbot/88cbd3ac5613eca90eea 

**Please note:** a barcode must be unique for each product.