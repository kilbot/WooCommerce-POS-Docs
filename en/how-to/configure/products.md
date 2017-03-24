---
title: Products
description:  
tags: 
---

Settings for your POS products can be found at `WP Admin > POS > Settings > Products`. 

* [Product Visibility](#product-visibility)
* [Allow Decimal Quantity](#allow-decimal-quantity)
* [Barcode Field](#barcode-field)
* [Product Tabs](#product-tabs)


### Product Visibility

Enabling the Product Visibility setting will allow you to configure [POS Only Products](./products/pos-only-products.md). 
Enabling POS only products will require an extra database lookup and therefore incur an small performance hit. 
If you do not use POS Only Products it is recommended you leave this option disabled. 


### Allow Decimal Quantity

By default, WooCommerce will expect [line item](/how-to/operate/cart/line-items.md) quantities to be a positive integer. 
Enabling decimal quantities will use the `woocommerce_stock_amount` filter to allow decimal quantities, eg `0.25`.


### Barcode Field

{% hint style='info' %}
This setting is part of [WooCommerce POS Pro](http://wcpos.com/pro).
{% endhint %}

By default, WooCommerce POS will use the product _SKU_ as the barcode field. 
The barcode field setting allows you to choose any custom field as your barcode field. 
For more information please read the [Custom Barcode Field](./products/custom-barcode-field.md) documentation. 


### Product Tabs

The product tabs settings allows customisation of the tabs in your [POS products panel](/how-to/operate/products.md). 
A tab consists of two parameters; the tab `label` and the tab `filter`.
The tab filter is any valid [search query](/how-to/operate/products/searching-filtering.md).


![Example of Product Tabs settings](http://wcpos.com/wp-content/uploads/2017/03/product-tabs-settings.png)