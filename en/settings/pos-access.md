---
title: POS Access
description: Using the POS Access settings, store owners can grant or remove user privileges to the Point of Sale system.
tags: access, administrator, capabilities, cashier, privileges, roles, shop-manager, users
---

Using the POS Access settings, store owners can grant or remove user privileges to the Point of Sale system.

### POS privileges

The main privileges for the POS system are: 

- Accessing and operating the POS - `access_woocommerce_pos`
- Managing the POS - `manage_woocommerce_pos`

### POS default roles

By default, the roles **Administrator** (WordPress role) and **Shop Manager** (WooCommerce role) are enabled with all capabilities for using the POS. They can both _access_ and _manage_ the POS.

In addition to those default roles WC POS creates a **Cashier** Role that can only _access_ the POS and _run_ it.

The _Cashier_ role does not allow regular WooCommerce operations (like editing products, creating customers ...) nor anything related to the WordPress site management.

A _Cashier_ is the same as a regular _[WP Subscriber](https://codex.wordpress.org/Roles_and_Capabilities#Subscriber)_ with just the extra capabilities necessary to operate the POS.

The default capabilities for this role are:

```
read
access_woocommerce_pos
read_private_products
read_private_shop_orders    
publish_shop_orders
list_users
read_private_shop_coupons
```
_see the `Capability | Access` table below for more infos._

### Adding WooCommerce related capabilities to the Cashier role
If they wish to promote the _Cashier_ role Store owners can use the POS Access settings to grant additional WooCommerce privileges.

For instance, using the _Pro Version_ of the plugin, the Cashier role could be added the ability to manage the Products (change prices, adjust stock ...) by adding the `edit_product`, `edit_published_products` and `edit_others_products` WooCommerce capabilities.  

If more options are needed regarding roles & capabilities one can refer to the resources section below to find and install a dedicated _roles & capabilities_ management plugin.

##### Tips

**Promoting default WP Roles:**
A quick way to allow a user to both operate the WP website and the POS is to add the `access_woocommerce_pos` capability and any WooCommerce capabilities deemed necessary to any of the default WordPress roles.

For instance: to allow users with the _Editor_ role to access and run the POS add the following capabilities to the _Editor_ role: 

```
access_woocommerce_pos
read_private_products
read_private_shop_orders    
publish_shop_orders
list_users
read_private_shop_coupons
```

If you want to allow Editors to also manage Products add the following capabalities:

```
edit_product
edit_published_products
edit_others_products
```

You can refer to the table below for guidance.

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

It is nevertheless recommended you keep the default settings unless you are aware of the consequences.
It would, for example, be a _very_ bad idea to grant the `publish_shop_orders` privilege to the `Subscribers` role. 

![Example of POS Access settings](http://wcpos.com/wp-content/uploads/2015/05/user-capabilities.png "Example of POS Access settings")

**Resources:**

*   More information on [WordPress Roles & Capabilities](https://codex.wordpress.org/Roles_and_Capabilities)
*   More information on [WooCommerce Roles & Capabilities](http://docs.woothemes.com/document/roles-capabilities/)
*   [User Role Editor](https://wordpress.org/plugins/user-role-editor/) - a great plugin for managing Roles and Capabilities
*   [Members](https://wordpress.org/plugins/members/) - another plugin for managing Roles and Capabilities