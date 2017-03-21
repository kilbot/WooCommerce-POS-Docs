---
title: Receipts
description: 
tags: 
---


The settings for receipts can be found via `WP Admin > POS > Settings > Receipts`. 
Under the *Receipt Options* tab you can choose to automatically print a receipt after every sale, you can also set the print method and template language. 
Under the *Receipt Template* tab you can customise the receipt template.

* [Setting up your printer](#setting-up-your-printer) 
* [Editing your receipt template](#editing-your-receipt-template)


### Setting up your printer 


WooCommerce POS is a javascript web application which runs in the browser. 
Printing from the browser to a standard A4 laser printer should be straight forward for most users, however, printing to a thermal receipt printer often presents a lot of technical challenges. 
Version 0.5 introduces some experimental settings which may assist to print to a thermal receipt printer. 

We are aware that using WooCommerce POS with a thermal receipt printer can be a confusing and frustrating task - especially for non-technical users. 
Improving this experience is a high priority before WooCommerce POS graduates to version 1.0, but you should be aware of the current limitations when evaluating whether WooCommerce POS is suitable for your store.

![Experimental print options introduced in version 0.5](http://wcpos.com/wp-content/uploads/2017/03/experimental-print-options.png)

The default print settings are HTML via the browser, it is recommended you keep these settings unless you are comfortable to experiment and troubleshoot any issues that may arise. 
The table below is intended as a guide for common combinations of settings.

| Method | Language | When to use |
| - | - | - |
| [Browser](./receipts/print-method.md#browser) | [HTML](./receipts/template-language.md#html) | For standard laser printers |
| [Network](./receipts/print-method.md#network) | [ePOS Print](./receipts/template-language.md#html) | For network connected Epson TM thermal receipt printers |
| [QZ Tray](./receipts/print-method.md#qz-tray) | [ESC/POS](./receipts/template-language.md#escpos) | For other thermal receipt printers |
| [Print to File](./receipts/print-method.md#print-to-file) | Any | For debugging |

### Editing your receipt template

![Editing the receipt template](http://wcpos.com/wp-content/uploads/2017/03/receipt-template.png)

Editing the receipt template can be done easily through the `WP Admin > POS > Settings > Receipts > Receipt Template` interface. 
Raw template code is shown in the left panel, while a preview is shown in the right panel. 
Previews for HTML templates can be seen immediately on save. 
Previews for other [template languages](./receipts/template-language.md) are not currently available, but users can still click the _Print_ button to test any changes.
Each receipt template is stored in the WordPress database.

For more information on customising your receipt template, please read the [Customising the Template](./receipts/customising-the-template.md) documentation.