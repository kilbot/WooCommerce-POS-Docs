---
title: Card Reader
description:  
tags: 
---

* [Supported Card Readers](#supported-card-readers)
* [Test Your Card Reader](#test-your-card-reader)
* [Supported Gateways](#supported-gateways)


### Supported Card Readers

WooCommerce POS currently only supports non-encrypting card readers, some card readers call this _keyboard emulation_. 
Most non-encrypting card readers seem to be USB attached, we are unaware of any card readers that will work via the phone jack.

Online stores, such as [NewEgg](https://www.newegg.com/Credit-Card-Reader/SubCategory/ID-3034), offer many types of card readers. 
Please do your own research to make sure the card reader has a keyboard emulation mode and that is it compatible with your device. 

### Test Your Card Reader

<textarea style="width:100%;height:50px;border:1px solid #ddd;" placeholder="click here, then swipe a card"></textarea>
<br>

If your card reader outputs something like the sting of characters below, then it will be compatible with WooCommerce POS.

```
%B4111111111111111^DOE/JANE^1805101000000000000000503000000?
```


### Supported Gateways

Any gateway that uses the [standard WooCommerce credit card form](https://mikejolley.com/2013/12/14/using-new-credit-card-form-woocommerce-2-1/) will be supported by WooCommerce POS. 
Other gateways may require some customisation to populate the card data to the correct fields. 
Please contact [support](http://wcpos.com/support) if your non-encrypting card reader is not populating the credit card fields for your gateway.