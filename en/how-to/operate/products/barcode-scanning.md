---
title: Barcode Scanning
description: WooCommerce POS is able to filter products by the SKU field, this allows you to instantly add products to cart using a barcode scanner.
tags: barcode, barcode-scanning, filtering, search, sku, sku-field
---

* [Searching Products using the Barcode Property](#searching-products-using-the-barcode-property)
* [Barcode Mode](#barcode-mode)
* [Using a Barcode Scanner](#using-a-barcode-scanner)
* [Test Your Barcode Scanner](#test-your-barcode-scanner)
* [Using a Custom Barcode Field](#using-a-custom-barcode-field)


### Searching Products using the Barcode Property

Using the [`barcode` search operator](/how-to/operate/products/searching-filtering.md#property-operators), you can search products by their barcode. 
A simple search using the barcode operator will only display the products.
A search in [_barcode mode_](#barcode-mode) will automatically add the found product to your cart.

![Example of using the barcode operator](http://wcpos.com/wp-content/uploads/2017/03/barcode-prefix.png)


### Barcode Mode

Searching for a product in _barcode mode_ will trigger the following:

1. a search will be executed using the `barcode` operator, eg: `barcode:123456789`
2. then;
	1. if a unique and exact match is found, the product is added to the cart
	2. if the search result is not unique (ie: duplicate barcodes), the found products will be displayed

You can switch to _barcode mode_ using the following methods:

* click on the search icon and select Scan Barcode, or
* use the HotKey, `shift+B` by default, or
* rapid keypresses, such as a [barcode scanner](#using-a-barcode-scanner), will automatically trigger barcode mode

![Search mode menu](http://wcpos.com/wp-content/uploads/2017/03/scan-barcode.png)


### Using a Barcode Scanner

{% hint style='info' %}
Previous to version 0.5, WooCommerce POS used a prefix character to trigger barcode mode. 
This caused a lot of confusion for non-technical users. 
WooCommerce POS now uses a timing trigger to automatically detect barcode scanning.
{% endhint %}

A barcode scanner is an input device, just like your keyboard. 
WooCommerce POS uses a timing mechanism to detect barcode scanning. 
If a sufficient number of keypresses happen in quick succession, the POS will automatically trigger [_barcode mode_](#barcode-mode).


### Test Your Barcode Scanner

To test whether your barcode scanner is compatible with WooCommerce POS, simply click on the input field below and scan a barcode. 
The input field should be populated with your barcode. 
If your barcode scanner adds any prefix or suffix characters, please consult your scanner manual to remove these characters.

<textarea style="width:100%;height:50px;border:1px solid #ddd;" placeholder="click here, then scan a barcode"></textarea>


### Using a Custom Barcode Field

By default, WooCommerce POS will use the SKU as the barcode field. 
It is possible to configure another custom field for your barcodes. 
For information on how to use a custom barcode field, please read the [Custom Barcode Field](/how-to/configure/products/custom-barcode-field.md) documentation.