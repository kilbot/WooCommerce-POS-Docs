---
title: POS Access
description: Using the POS Access settings, store owners can grant or remove user privileges to the Point of Sale system.
tags: access, administrator, capabilities, cashier, privileges, roles, shop-manager, users
---

Using the POS Access settings, store owners can grant or remove user privileges to the Point of Sale system. 
By default, the roles **Administrator** and **Shop Manager** are enabled with all capabilities for using the POS. 
It is recommended you keep the default settings unless you are aware of the consequences. 
For example, granting the `publish_shop_orders` to the `Subscribers` role would be a _very_ bad idea. 

![Example of POS Access settings](http://wcpos.com/wp-content/uploads/2015/05/user-capabilities.png "Example of POS Access settings")

| Capability | Access |
| - | - |
| access_woocommerce_pos | Required to access the POS frontend |
| manage_woocommerce_pos | Required to access the POS admin settings |
| read_private_products | Required to view products |
| edit_product <br> edit_published_products <br> edit_others_products | Required to edit products and variations |
| read_private_shop_orders | Required to view orders and receipts |
| publish_shop_orders | Required to create new orders |
| list_users | Required to view customers |
| create_users | Required to create new customers |
| edit_users | Required to update existing customers |
| read_private_shop_coupons | Required to view coupons |

**Resources:**

*   More information on [WordPress Roles & Capabilities](https://codex.wordpress.org/Roles_and_Capabilities)
*   More information on [WooCommerce Roles & Capabilities](http://docs.woothemes.com/document/roles-capabilities/)
*   [User Role Editor](https://wordpress.org/plugins/user-role-editor/) - a great plugin for managing Roles and Capabilities
*   [Members](https://wordpress.org/plugins/members/) - another plugin for managing Roles and Capabilities