---
title: Filtering orders by POS or Online sales
description: Separate POS and Online orders by using the quick-links in the WooCommerce admin.
tags: admin, filtering, orders
---

You can quickly separate your POS and Online orders in the WooCommerce admin by using the quick-links to the top left. 
**Please note:** this will only filter POS orders after version 0.3.1, orders prior to 0.3.1 will default to Online. 

![Filter Orders](https://wcpos.com/wp-content/uploads/2014/09/filter-orders-e1409558012346.png "Filter Orders")

Additionally, if you wanted to filter all the completed orders from your admin area so you can focus on the pending/processing orders, you can add the following code to your [functions.php](http://codex.wordpress.org/Functions_File_Explained) file. 

{% gist id="kilbot/4843e5278dfa4b05063a" %}{% endgist %}