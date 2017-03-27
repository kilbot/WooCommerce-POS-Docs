---
title: Customers
description:
tags:
---

By default, WooCommerce POS will complete orders using a _Guest_ user account. 
You can use the customer dropdown to select any existing WordPress user from your database. 
Assigning a customer to an order allows you to track purchases, this may be useful for customer relations and marketing. 


* [Default Customer](#default-customer)
* [Customer Search](#customer-search)
* [Customer Select](#customer-select)
* [Remove Customer](#remove-customer)
* [Add New Customer](#add-new-customer) (Pro)


### Default Customer

You can configure the default customer in the [Customer settings](/how-to/configure/customers.md). 


### Customer Search

Customers are listed alphabetically using the last name. 
The following fields are used for search; _email_, _username_, _first_name_, _last_name_, _billing_address.phone_, _billing_address.company_.


### Customer Select

Clicking on the customer search field will open the select dropdown. 
WooCommerce POS will immediately download the first 10 customers. 
You can search the customers, or use your arrow keys to scroll through the customers. 

![Example of the customer dropdown](http://wcpos.com/wp-content/uploads/2017/03/select-customer.png)


### Remove Customer

When a customer is added to the order, an `x` icon will appear new to their name. 
You can use this `x` button to remove the customer from the current cart, this resets the order to use the default customer.

![Remove a customer using the `x` button](http://wcpos.com/wp-content/uploads/2017/03/delete-customer.png)


### Add New Customer

{% hint style='info' %}
This feature is requires an upgrade to [WooCommerce POS Pro](http://wcpos.com/pro).
{% endhint %}

You can add a new customer using the green `+` icon next to the customer search field. 
This will create a new WordPress user with the _customer_ role. 
An email address is required to create a new customer account. 

When creating a new customer, the _email_, *first_name* and *last_name* will be automatically copied to the matching **Billing Address** fields. 

For more configuration settings, please read the [Customer settings](/how-to/configure/customers.md) documentation. 

![Example of the Add New Customer modal window](http://wcpos.com/wp-content/uploads/2017/03/add-new-customer.png)
