---
title: Barcode Scanning
description: WooCommerce POS is able to filter products by the SKU field, this allows you to instantly add products to cart using a barcode scanner.
tags: barcode, barcode-scanning, filtering, search, sku, sku-field
---

* [Searching with the Barcode Prefix](#searching-with-the-barcode-prefix)
* [Barcode Mode](#barcode-mode)
* [Using a Barcode Scanner](#using-a-barcode-scanner)
* [Test Your Barcode Scanner](#test-your-barcode-scanner)
* [Using a Custom Barcode Field](#using-a-custom-barcode-field)

### Searching with the Barcode Prefix



### Barcode Mode

Searching for a product in _barcode mode_ will trigger the following:

1. a search will be executed using the `barcode` prefix, eg: `barcode:123456789`
2. then;
	1. if a unique and exact match is found, the product is added to the cart
	2. if the search result is not unique and exact, the found products will be displayed

You can switch to _barcode mode_ using the following methods:

* click on the search icon and select Scan Barcode, or
* use the HotKey, `shift+B` by default, or
* rapid keypresses, such as a [barcode scanner](#using-a-barcode-scanner), will automatically trigger barcode mode

![Search Scan Barcode modes](http://wcpos.com/wp-content/uploads/2014/07/search-scan-mode.png)

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