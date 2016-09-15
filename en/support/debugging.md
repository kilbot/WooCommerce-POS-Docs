---
title: Debugging
description: If debugging is enabled, WooCommerce POS will log various messages to the console which may assist in diagnosing problems.
tags: browser, console, debugging, developer, javascript, local-storage, support
---

{% hint style='info' %}
This article is intended for web developers, debugging is not something the average user should need to use.
{% endhint %}

WooCommerce POS is largely a JavaScript web application - and as such - most debugging is done through the [browser console](http://codex.wordpress.org/Using_Your_Browser_to_Diagnose_JavaScript_Errors). 
If debugging is enabled, WooCommerce POS will log various messages to the console which may assist in diagnosing problems.

![An open JavaScript Console in Chrome for the Mac](https://wcpos.com/wp-content/uploads/2016/06/javascript-console.png "An open JavaScript Console in Chrome for the Mac")

### Turn on debugging using wp-config.php

By setting the [SCRIPT_DEBUG](https://codex.wordpress.org/Debugging_in_WordPress#SCRIPT_DEBUG) flag in your wp-config.php file, you can enable WooCommerce POS debugging. 
This will load the unminified script files and also enable debug messages in the browser console.

### Turn on debugging using the browser console

If you do not have access to the wp-config.php file, you can enable debug messages by adding a `debug` flag to the Local Storage. 
This can be done by entering `localStorage.setItem('debug', '*')` into the console. 
Now refresh the page and debugging will be on. Console logging can consume browser resources so you'll probably want to turn debugging off once you are finished with it. 
To turn debugging off, simply enter `localStorage.removeItem('debug')` into the console and refresh the page.