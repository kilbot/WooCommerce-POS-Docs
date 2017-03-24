---
title: Receipt Template Language
description:
tags:
---

Not to be confused with English or Español, in this case language refers to the `code` used to render and print the receipt. 
Most of us are familiar with HTML which is used to render a webpage and prints to the common laser printer. 
However, HTML lacks certain instructions which are common for point of sales receipt printing, such as `line feed` and `paper cut`. 
To allow an expanded set of instructions, most thermal receipt printers use either ePOS Print or ESC/POS. 
The right template language for you will depend on your printer.

| Template language | Printer |
| - | - | 
| [HTML](#html) | Laser printers |
| [ePOS Print](#epos-print) | Epson TM thermal receipt printers |
| [ESC/POS](#escpos) | Other thermal receipt printers |

* Note: there are many other proprietary languages used by printer manufacturers.
The template languages supported by WooCommerce POS may be expanded based on user feedback.

### HTML

HTML is the standard markup language for creating webpages. 
Most WordPress users are familiar with HTML and CSS syntax, which makes it the most accessible language for creating a custom receipt template. 

[Click here](https://github.com/kilbot/WooCommerce-POS/blob/master/includes/views/print/receipt-html.php) for an example of a HTML receipt template for WooCommerce POS.

### ePOS Print

ePOS Print is an attempt from Epson to update their proprietary print commands for use in modern point of sales scenarios. 
ePOS Print allows for direct communication between a web application and the printer via SOAP/XML. 

[Click here](https://github.com/kilbot/WooCommerce-POS/blob/master/includes/views/print/receipt-epos-print.php) for an example of an ePOS Print receipt template for WooCommerce POS.

### ESC/POS
 
ESC/POS is a set of _raw_ print commands with each command starting with an ESC character, ie: `\x1B`. 
ESC/POS is the defacto standard for thermal receipt printing at the point of sale, most receipt printers support it in some form. 
However, the _raw commands_ are not human readable therefore creating a custom template can be a challenging task, even for technically literate users.

[Click here](https://github.com/kilbot/WooCommerce-POS/blob/master/includes/views/print/receipt-escp.php) for an example of an ESC/POS receipt template for WooCommerce POS.