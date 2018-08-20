---
layout: post
title: Alterar o bloco do totals no carrinho com xml
tags: Magento XML
---
Alterar o bloco phtml do totals no carrinho

```
<checkout_cart_index translate="label">
    <reference name="content">
        <reference name="checkout.cart.totals">
            <block type="checkout/cart_totals" name="ceicom.checkout.cart.totals" as="totals" template="ceicom/checkout/cart/totals.phtml"/>
            <action method="setTemplate"><template>ceicom/checkout/cart/totals.phtml</template></action>
        </reference>
    </reference>
</checkout_cart_index>
```
