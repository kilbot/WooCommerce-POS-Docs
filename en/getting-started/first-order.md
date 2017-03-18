---
title: Your First Order
description:  
tags: 
---

1. [Find product](#find-product)
2. [Add to cart](#add-to-cart)
3. [Select customer](#select-customer)
3. [Add note](#add-note)
4. [Checkout](#checkout)
5. [Print receipt](#print-receipt)

### Find product

The first time you open WooCommerce POS it will immediately download 10 products and display them in the Product panel. 
You can use the search field to search by title, or simply scroll through the products until you find what you are looking for. 
Products are listed alphabetically. 

For more complex queries please read the documentation on [Search and Filtering](/how-to/operate/products/search-filtering.md).

### Add to cart

Clicking on the green '+' icon will add the product to cart. 
For variable products you can either open the variations in a popover or 'expand' the variations below the parent product.

![Example showing simple product (Premium Quality) and variable product (Ship Your Idea) with variations (black, green)](http://wcpos.com/wp-content/uploads/2017/03/product-list.png)

Adding a product to the cart will create a new [line item](/how-to/operate/cart/line-items.md) for that product. 
The order total will be calculated, including any tax rates you have set.

![Example of a product in the cart](http://wcpos.com/wp-content/uploads/2017/03/cart.png)


### Select customer

By default, no WordPress user will be attached to the order, this is called the _Guest_ account. 
Using the customer search field you can attach a customer to the current order. 

For more information on selecting customers please read the [Customer](/how-to/operate/cart/customers.md) documentation.

![Example of selecting a customer for the current order](http://wcpos.com/wp-content/uploads/2017/03/customer.png)


### Add note

At the bottom of the cart is several buttons for completing extra tasks in the cart. 
Clicking on the _Note_ button will open a text field for entering notes about the order. 
Deleting the text will remove the notes field.

![Example of using the Notes field](http://wcpos.com/wp-content/uploads/2017/03/notes.png)

### Checkout

Clicking on the _Checkout_ button will replace the cart with a list of payment gateways. 
Using the Cash gateway you have the option of entering an Amount Tendered.

WooCommerce POS comes with two gateways by default; Cash and Card.
The Card gateways is intended for use with external card devices, for example, an EFTPOS machine provided by your bank. 
For more information on gateways please read the [Payment Gateways](/how-to/operate/payment-gateways.md) documentation. 

![Example of Cash checkout](http://wcpos.com/wp-content/uploads/2017/03/checkout.png)

### Print receipt

Processing the payment (checkout) will send the order to your server and carry out the necessary check to confirm the payment has been successful. 
This process should usually only take a few seconds, but can take longer under [certain circumstances](/support/pos-performance.md). 


Once the payment has been confirmed you can now print a receipt for your customer. 
For help on printing receipts or customising the receipt template please see the [Receipts](/how-to/configure/receipts.md) documentation.

![Receipt screen after successful payment](http://wcpos.com/wp-content/uploads/2017/03/receipt.png)
