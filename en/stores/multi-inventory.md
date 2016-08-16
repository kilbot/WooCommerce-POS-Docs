---
title: Multi Inventory Stores
description:  
tags: 
---

{% hint style='info' %}
Multi-inventory is not currently a feature of the Pro plugin. 
The following information is intended to assist users until WooCommerce POS Pro officially supports multi-inventory.
{% endhint %}

Multi-inventory stores is one of the most requested features for WooCommerce POS Pro. 
This feature would allow stores owners to assign products to different stores and manage the stock between each physical store and the online store. 

Creating multi-inventory functionality is a non-trivial task. 
There are a couple of plugins already working on the problem, such as [WooCommerce Warehouses](https://codecanyon.net/item/woocommerce-warehouses/13087646) and [WooCommerce MultiStore](http://woomultistore.com/).
Currently it makes sense to focus development on other core POS features and integrate with one of these plugins once they mature to stable solutions.

In the short term, you may be able to meet most of your requirements using the [WordPress MultiSite feature](https://codex.wordpress.org/Create_A_Network). 
By creating a site for each store, you can then install WooCommerce and WooCommerce POS on each site, keeping each store inventory completely separate. 
WooCommerce Multisite (mentioned above) uses this approach with an added layer to manage inventory between sites.