---
title: POS Only Products
description: Products can be hidden in your online store or at the point of sale using the POS visibility setting.
tags: filtering, pos-only, product display
---

There may be situations where you need to hide a product from either your Online store or your POS. 
With WooCommerce POS this can be achieved using the POS Visibility setting on the product edit page. 

### Enabling POS Only Products

POS Only Products is not enabled by default.
To enable POS Only Products go to <code>WP Admin > POS > Settings > General</code>

![Enable POS Only Products](https://wcpos.com/wp-content/uploads/2014/09/enable-pos-only-products.png "Enable POS Only Products")

Enabling POS only products will require an extra database lookup and therefore incur an small performance hit. 
If you do not use POS Only Products it is recommended you leave this option disabled. 

### POS & Online Visibility

![POS Visibility](https://wcpos.com/wp-content/uploads/2016/08/pos-visibility.png "POS Visibility settings on the Product edit page")

| Setting | Description |
| - | - |
| **POS & Online**<br>(default) | Products will be visible both online in your web store and in your physical store |
| **POS Only** | Product page will not be visible online |
| **Online Only** | Product will not be visible in the POS |

### Catalog Visibility

If you go directly to a POS Only Product page you will get <code>404 Page Not Found</code>. 
However, POS Only Products may still appear in the online search and category pages. 
To hide the products completely from your website you should set Catalog Visibility to Hidden.

![Catalog Visibility](https://wcpos.com/wp-content/uploads/2016/08/catalog-visibility.png "Catalog Visibility settings on the Product edit page")

### Filter POS Only Products

You can quickly see which products are visible/hidden by using the quick-links on the Products admin page: 

![POS Visibility Filter](https://wcpos.com/wp-content/uploads/2016/08/pos-visibility-filter.png "POS Visibility Filter")

### Bulk Edit

To change the POS Visibility of multiple products, go to your Products list and select <code>Edit</code> from the <code>Bulk Actions</code>. 

![Bulk Edit POS Visibility](https://wcpos.com/wp-content/uploads/2016/08/pos-visibility-bulk-edit.png "Bulk edit POS Visibility")