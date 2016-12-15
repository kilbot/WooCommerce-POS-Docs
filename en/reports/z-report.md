---
title: Z-Report
description:  
tags: data, export, reports, sales
---

A Z-Report is a daily sales report that will gather different indicators for a given Point Of Sale.

Before the integration of a fully fledged Reports screen into the POS interface (coming in 0.6 release and including a Z-report section) **we make available a simple [WordPress page template](https://developer.wordpress.org/themes/template-files-section/page-templates) that will allow store owners to display and print a Z-report for the current day** (from midnight until the time of the report generation).

### Indicators
We make the following indicators available for now:

| **Z-report indicators** |
| - |
| **Generic indicators** |
| Total Sales, Net Sales, Total Tax, Total Shipping, Total Shipping Tax, Total Fees, Total Fees Tax, Total Orders, Total Items,Total Discounts |
| **Sales by gateways** |
| Total Sales, Total Tax, Total Orders, Total Shipping |
| **Sales by categories** |
| Total Sales, Total Tax, Total Items |
| **Taxes** |
| Total Tax, Shipping tax, Tax Rate Code |

![a basic non-styled Z-report](http://take.ms/OVAMz)

### Store reports
If you have setup multiple stores you can generate a report for any of them by clicking on its name in the Stores menu.

![Z-report Stores menu](http://take.ms/O36c2)


### Usage
1. Download the template: [Z-Report WordPress template](https://gist.github.com/thomasmery/6f16a79999081ce184a8424c88215444/archive/37fa8b965226abec452529b657811a9e449d146f.zip) or copy the template's code from the the code embed below.
2. Add the template to your theme's directory
3. Create a regular WordPress Page with its custom template set to the _Z-report template_ name (defaults to _Z-Report_).
4. Access your z-report at its page's url 

![a Page with the Z-report Custom Template](http://take.ms/mr6d7)

The Z-report template includes the Page title and any content you might want to add (displayed above the actual report).

![Z-report Title and content](http://take.ms/SvEV4)

*********

#### The Template's code
{% gist id="https://gist.github.com/thomasmery/6f16a79999081ce184a8424c88215444" %}{% endgist %}