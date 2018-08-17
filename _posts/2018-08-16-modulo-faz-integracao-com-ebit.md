---
layout: post
title: Modulo de integraçao com Ebit Magento 1
categories: 'Modulos, Magento'
---
### O modulo faz integração com o ebit enviando parâmetros solicitado pelo GRUPO BUSCAPÉ para fazer pesquisa de satisfação

* Seguintes parâmetros são enviado


```
<param id="ebitParam" 
value="email={email}
&gender={gender}
&birthDay={birthDay}
&zipCode={zipCode}
&parcels={parcels}
&deliveryTax={deliveryTax}
&deliveryTime={deliveryTime}
&totalSpent={totalSpent}
&value={value}
&quantity={quantity}
&productName={productName}
&transactionId={transactionId}
&ean={eanCode}
&sku={sku}
&buscapeId={BuscapeId}
&storeId={storeId}"
/>
```

Versões: Magento 1.x.x

### Installation

**Send** the 'app/skin' folder to the root of the magento installation

### After installation

**Add** After installation install idEbit and idBuscapé in
System> Configuration> Ceicom> Ebit Integration

[**Download**](https://github.com/Ceicom/Ceicom_EbitIntegration/releases)

Print config:

![null](/img/uploads/687474703a2f2f692e696d6775722e636f6d2f67526c58346a792e706e67.png)
