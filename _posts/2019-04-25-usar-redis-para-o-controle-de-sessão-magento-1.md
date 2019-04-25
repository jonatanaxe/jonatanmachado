---
layout: post
title: Usar redis para o controle de sessão magento 1
tags: magento redis
---
Voce deve ter instalado no servidor o **redis**

Para verificar pode acessar o ssh do servidor ou sua maquina e rodar o comando **redis-cli**

Aparecer algo assim ip e porta isso confirma que voce tem o redis instalado

```
[magento-server]:$ redis-cli
127.0.0.1:6379>
```

Opos isso habilite o uso do redis no magento seguindo esse tutorial
https://jonatanmachado.tk/habilitar-redis-magento-1/


No seu arquivo  local.xml no lugar de session_save adicione

```
<session_save>db</session_save>
<redis_session>
    <host>127.0.0.1</host>
    <port>6379</port>
    <password></password>
    <timeout>2.5</timeout>
    <persistent></persistent>
    <db>0</db>
    <compression_threshold>2048</compression_threshold>
    <log_level>1</log_level>
    <max_concurrency>6</max_concurrency>
    <break_after_frontend>5</break_after_frontend>
    <fail_after>10</fail_after>
    <break_after_adminhtml>30</break_after_adminhtml>
    <first_lifetime>600</first_lifetime>
    <bot_first_lifetime>60</bot_first_lifetime>
    <bot_lifetime>7200</bot_lifetime>
    <disable_locking>0</disable_locking>
    <min_lifetime>60</min_lifetime>
    <max_lifetime>2592000</max_lifetime>
</redis_session>
```

Por padrao o modulo do Cm_RedisSession  magento 1 vem desabilitado deve mudar pra **true**

/var/www/loja.com.br/app/etc/modules/Cm_RedisSession.xml

```
<config>
  <modules>
    <Cm_RedisSession>
      <active>true</active>
      <codePool>community</codePool>
    </Cm_RedisSession>
  </modules>
</config>
```
