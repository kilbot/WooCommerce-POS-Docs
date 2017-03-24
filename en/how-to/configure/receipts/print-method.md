---
title: Receipt Print Method
description:
tags:
---

* [Browser](#browser)
* [Network](#network)
* [QZ Tray](#qz-tray)
* [Print to file](#print-to-file)


### Browser

Printing via the browser will show a print dialog with the system print options. 
The print dialog will usually show you a preview of what is about to be printed, along with some options for selecting the printer. 
Printing via the browser is recommended for all laser printers. 

### Network

Some modern printers are able to receive raw commands directly over the network.
These printers are ideal for use with tablets or mobile phones as they don't need a special printer driver.
Espon often calls these *intelligent* printers, such as the [Epson TM-T70-i Intelligent Printer](http://www.epson.com.au/pos/products/receiptprinters/DisplayMain.asp?id=TM-T70-i) or the [Epson TM-T88V-i Intelligent Printer](http://www.epson.com.au/pos/products/receiptprinters/DisplayMain.asp?id=tmt88v-i).

To use the network setting you will need to supply a URL for your printer or print server. 
An example URL for Epson TM printers is `http://192.168.192.168/cgi-bin/epos/service.cgi?devid=local_printer&timeout=10000`, where `192.168.192.168` is the static IP address of your printer. 

To find the correct URL for your printer please consult your printer manual, or try google, eg: 'Epson TM-T88V-i static IP address'.

To test whether your browser can print to your network attached printer, please try the [ePOS Network Print Test](http://wcpos.com/support/epos-network-print.html).

### QZ Tray

[QZ Tray](https://qz.io/) is a free application for Windows, Mac OSX and Linux computers.
QZ Tray allows the browser to send raw commands to printers connected via USB, Serial or the Network.
For more information please see [*What is Raw Printing*](https://qz.io/wiki/What-is-Raw-Printing).

If you have installed QZ Tray you can test various printers using the [QZ Tray demo page](https://demo.qz.io/).

### Print to file

Printing to file will output the raw receipt data to a designated folder on your computer.
This can be useful for debugging or custom print processes.