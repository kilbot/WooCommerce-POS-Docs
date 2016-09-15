---
title: Legacy Servers
description: If your web host blocks modern RESTful HTTP methods you will need to enable legacy server support.
tags: errors, http, legacy, REST
---

HTTP (and HTTPS) are the protocols used by every browser to talk to web applications. 
A key part of the protocol is the [HTTP method](https://tools.ietf.org/html/rfc2616#section-5.1.1). 
Traditionally, web applications used a very limited set of HTTP methods such as GET (retrieve a web page) and POST (submit a web form). 

Modern web applications, such as WooCommerce POS, use a REST/HTTP approach with following HTTP Methods:
   
   * GET
   * POST
   * PUT
   * PATCH
   * DELETE

In some rare cases a web host may choose to block some of these HTTP methods. 
If your web host blocks modern RESTful HTTP methods you will need to enable legacy server support.

![Legacy Server Support](https://wcpos.com/wp-content/uploads/2016/06/enable-legacy-server-support.png "WP Admin > POS > Settings > Tools > Enable legacy server support")