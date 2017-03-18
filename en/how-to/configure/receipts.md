---
title: Receipts
description: Receipts can be customised by copying the receipt.php template in your theme directory.
tags: customise, date, handlebars, moment.js, printing, receipts, template, theme
---

The POS receipt print templates reside in the `includes/views/print/tmpl-receipt.php` file of both the free and the Pro plugins. Receipt templates can be customised by creating a `woocommerce-pos/print/tmpl-receipt.php` file in your theme directory. The code for both templates is included below.

### Basic Receipt Template

{% gist id="kilbot/04b4a4f1c2792b4efff5" %}{% endgist %}

### Pro Receipt Template

The Pro Receipt Template allows additional information from the [Stores](stores.html) admin such as logo, store address, opening hours and special messages. 

{% gist id="kilbot/c9485366a73ceda12041" %}{% endgist %}

### Customising the receipt date

WooCommerce POS uses [moment.js](http://momentjs.com/) to localise the date strings. The default date format is `"MMMM Do YYYY, h:mm:ss a"`, eg: May 31st 2015, 7:20:44 pm. Please consult the [moment.js documentation](http://momentjs.com/docs/#/parsing/string-format/) for more information on customising the date format.

### Order Properties

WooCommerce POS uses the json output from the WC REST API to populate the order receipt template. [The WC REST API docs show an example](http://woothemes.github.io/woocommerce-rest-api-docs/#view-an-order) of the standard json output. Some additional properties have been added by WooCommerce POS using the `woocommerce_api_order_response` filter.

| Property | Description |
| - | - |
| cart_discount_tax |  The tax portion of the cart discount |
| cashier.id | User ID of the Cashier |
| cashier.first_name | First name of the Cashier |
| cashier.last_name | Last name of the Cashier |
| payment_details.result | Payment gateway success or failure |
| payment_details.message | Any messages from the payment gateway |
| payment_details.redirect | Redirect URL for offsite payments, eg: PayPal Standard |
| payment\_details.method_{gateway} | Any gateway specific messages, eg: Amount Tendered and Change |
| shipping_lines[i].total_tax | Add tax amount for each shipping line |
| subtotal_tax | The tax portion of the subtotal |

{% gist id="kilbot/d224c0d4f7a8ed26bf28" %}{% endgist %}