---
title: Customising the Template
description: 
tags: customise, date, handlebars, moment.js, printing, receipts, template, theme
---

* [Overview](#overview)
* [Order Properties](#order-properties)
* [Example Order Output](#example-order-output)
* [Using Order Properties](#using-order-properties)
* [Localising the receipt date](#localising-the-receipt-date)
* [Resources](#resources)

### Overview

Customising the receipt template can be done easily through the `WP Admin > POS > Settings > Receipts > Receipt Template` interface. 
Each template is stored in the WordPress database, so there is no need to FTP to your server to upload theme files. 
The settings include an option to restore the default template should you encounter an error with your custom template. 

**Receipt templates in WooCommerce POS are rendered in the browser at runtime - they are not generated on the server like a webpage**. 
You can not use PHP functions or object properties in your template, this will cause an error. 
Each receipt is populated with order properties from WC REST API, this data is rendered using a Javascript templating library called [Handlebars](http://handlebarsjs.com/).

### Order Properties

WooCommerce POS uses the JSON output from the WC REST API to populate the order receipt template. [The WC REST API documentation shows an example](http://woothemes.github.io/woocommerce-rest-api-docs/#view-an-order) of the standard JSON output. Some additional properties have been added by WooCommerce POS using the `woocommerce_api_order_response` filter.

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

### Example Order Output

{% gist id="kilbot/d224c0d4f7a8ed26bf28" %}{% endgist %}

### Using Order Properties

WooCommerce POS uses [Handlebars](http://handlebarsjs.com/) to display the order properties in the receipt template. 
To display an order property in your receipt template you need to wrap the property in double braces `{{ }}`. 
Using the above order output as an example, `{{order_number}}` will display `645`, `{{currency}}` will display `USD` and so on. 

Nested properties can be displayed using dot notation. 
Using the above order output as an example, `{{billing_address.first_name}}` will display `John`.

An array of properties, such as line items, can be displayed using `{{#each line_items}}{{name}}{{/each}}`.

In addition to the standard Handlebars syntax, WooCommerce POS also offers some helpers to display formatted properties. 
The `money` helper will localise the decimal price.
Using the above order output as an example, `{{money total_tax}}` might display `€ 5,90` depending on your store settings.

Please review the [default WooCommerce POS receipt template](https://gist.github.com/kilbot/04b4a4f1c2792b4efff5) for more examples of using order properties in your receipt template.

### Localising the receipt date

WooCommerce POS uses [moment.js](http://momentjs.com/) to localise the date strings. The default date format is `"MMMM Do YYYY, h:mm:ss a"`, eg: `May 31st 2015, 7:20:44 pm`.

WooCommerce POS will also use your site language settings to further localise the date. For example, if your site language is set to `Español` the default date will be translated, eg: `mayo 31º 2015, 7:20:44 pm`.

Please consult the [moment.js documentation](http://momentjs.com/docs/#/parsing/string-format/) for more information on customising the date format.

### Resources

* [Default HTML Receipt Template for WooCommerce POS](https://gist.github.com/kilbot/04b4a4f1c2792b4efff5)
* [Default HTML Receipt Template for WooCommerce POS Pro](https://gist.github.com/kilbot/c9485366a73ceda12041)