---
title: Emails
description: Using the WooCommerce POS settings, store owners can choose to enable or disable the email notifications from WooCommerce.
tags: checkout, emails, new-orders, notifications
---

By default, WooCommerce sends emails to notify the store owner and customer about the status of their orders. 
Many of these emails are unnecessary for Point of Sale orders, for example, the store owner may make hundreds of POS orders in a day, receiving a new order notification for each order would only clutter the inbox and distract from other important alerts about an online order. 

Using the WooCommerce POS settings store owners can choose to enable or disable the email notifications from WooCommerce, this will affect only the orders processed through the POS system. 

![Email settings for POS orders.](http://wcpos.com/wp-content/uploads/2015/07/email-settings.png "Email settings for POS orders")

Enabling admin emails will send notifications to the admin email address. Enabling customer emails will send notifications to the billing email address (requires an existing customer to be selected at checkout). Low stock and no stock notifications will always be sent to the admin email address.


| Type | Hooks |
| - | - |
| ** Customer emails ** <br> * disabled by default * | woocommerce_order_status_pending_to_processing_notification <br> woocommerce_order_status_pending_to_on-hold_notification <br> woocommerce_order_status_completed_notification |
| ** Admin emails ** <br> * disabled by default * | woocommerce_order_status_pending_to_processing_notification <br> woocommerce_order_status_pending_to_completed_notification <br> woocommerce_order_status_pending_to_on-hold_notification <br> woocommerce_order_status_failed_to_processing_notification <br> woocommerce_order_status_failed_to_completed_notification <br> woocommerce_order_status_failed_to_on-hold_notification |
| ** Admin emails ** <br> * always sent * | woocommerce_low_stock_notification <br> woocommerce_no_stock_notification <br> woocommerce_product_on_backorder_notification |