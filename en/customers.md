---
title: Customers
description:  
tags: 
---

{% hint style='info' %}
This feature is requires an upgrade to [WooCommerce POS Pro](http://wcpos.com/pro).
{% endhint %}

### Capabilities

Cashiers will need the *list_users*, *create_users* and *edit_users* capabilities to use all the Customer features.

### WordPress Multisite

When using [WordPress multisite](https://codex.wordpress.org/Create_A_Network) there are some [extra checks](https://github.com/WordPress/WordPress/blob/master/wp-includes/capabilities.php) to prevent non [Super Admins](https://codex.wordpress.org/Roles_and_Capabilities#Super_Admin) from creating and editing customer. 

First, in order for non Super Admins to **create** new customers, please enable the following option in `Network Admin > Settings`. 

![Multisite option to create new users](https://wcpos.com/wp-content/uploads/2016/09/multisite-create-new-users.png "Multisite option to create new users")

Additionally, in order for non Super Admins to **edit** customer details, you will need to add the `manage_network_users` capability to the cashier.

{% gist id="https://gist.github.com/kilbot/6fa518797bd985e7eead651a7f7354ef" %}{% endgist %}