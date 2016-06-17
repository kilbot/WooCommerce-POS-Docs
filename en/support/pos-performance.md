---
title: POS Performance
description: 
tags: connection, hosting, optimization, performance, plugins, speed
---

WooCommerce POS is a single-page javascript web application which communicates to your server via the [WooCommerce REST API](http://woothemes.github.io/woocommerce-rest-api-docs/). Performance issues can be separated into two categories; server-side and clients-side.

### Server-side Performance

Server-side performance refers to actions such as downloading a page of products (10 products), or processing an order. Issues which can affect the speed of such actions include:

*   The speed of your internet connection
*   The speed of your server, ie: processing power, RAM, server load etc
*   How many plugins you have active
*   Payment gateway processing

The [demo site](http://demo.wcpos.com/pos) represents a 'best case' senario. The demo site uses [a very good web host](/wpe) and has a very small number of plugins activated.

<table class="table">

<thead>

<tr>

<th colspan="2">Average speeds for [demo.wcpos.com/pos](http://demo.wcpos.com/pos)<sup>*</sup></th>

</tr>

</thead>

<tbody>

<tr>

<td>Fetching 10 products</td>

<td>1 - 2 seconds</td>

</tr>

<tr>

<td>Processing a Cash sale</td>

<td>1 - 2 seconds</td>

</tr>

<tr>

<td>Processing a Stripe sale</td>

<td>2 - 3 seconds</td>

</tr>

</tbody>

<tfoot>

<tr>

<td colspan="2"><sup>*</sup> <small>average times for a broadband connection. Times may vary depending on your internet speed.</small></td>

</tr>

</tfoot>

</table>

If your POS is taking significantly longer than the above times you may wish to conduct the following tests:

1.  Switch your theme to the default Twenty Fifteen theme from WordPress
2.  Disable all plugins except for WooCommerce and WooCommerce POS
3.  [Clear the local storage data](http://wcpos.com/faq/clear-local-data/)
4.  Now, use the POS to see if there is a performance increase
5.  **If there is a performance increase:** reactivate your theme and plugins one-by-one to see which plugin is impacting your performance
6.  **If there is no performance increase:** you may want to move to a better web host or invest in a faster internet connection

### Client-side Performance

WooCommerce POS uses Javascript, HTML and CSS to display the data retrieved from the WooCommerce REST API, ie: [products](http://woothemes.github.io/woocommerce-rest-api-docs/#view-a-product) and [orders](http://woothemes.github.io/woocommerce-rest-api-docs/?shell#view-an-order). To improve client-side performance the POS stores the data in the browser using [IndexedDB](https://en.wikipedia.org/wiki/Indexed_Database_API). For example, when a product is fetched for the first time a request will be sent to the server, once the product data is downloaded it will be stored locally so that subsequent searches are instantaneous. [caption id="attachment_1782" align="aligncenter" width="577"]![An example of product stored locally.](http://wcpos.com/wp-content/uploads/2015/07/local-products.png) An example of products being stored locally.[/caption] IndexedDB data persists even when you close the browser or restart your computer. If you notice that your product data is out of sync for any reason, you can [clear the local storage](http://wcpos.com/faq/clear-local-data/) and fetch a fresh set of data from the server.