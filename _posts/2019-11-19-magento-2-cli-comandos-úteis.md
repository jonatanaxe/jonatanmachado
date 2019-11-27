---
layout: post
title: Magento 2 cli Comandos Úteis
tags: Magento2
---
## //Upgrade

```
php bin/magento setup:upgrade
```

## //Compilar backend

```
php bin/magento setup:di:compile
```

## //Compilar front

```
php bin/magento setup:static-content:deploy -t tema/tema_novo  pt_BR -f
```

## //Limpar caches e arquivos gerados

```
php bin/magento cache:flush
```

## //Apagar estáticos

```
rm -rf pub/static/*
```

## //Apagar arquivos gerados

```
rm -rf var/*
```

## //Habilitar todos os caches

```
php bin/magento cache:enable
```

## //Reindexar tudo

```
php bin/magento indexer:reindex
```

## //Criar ou atualizar usuário admin

```
php bin/magento admin:user:create -admin-user='jonatan@jonatanmachado.tk' -admin-password='jonatan123' --admin-email='jonatan@jonatanmachado.tk' -admin-firstname='Admin' -admin-lastname='Admin'
```

## //Listar todos os modulos instalado e o status

```
bin/magento module:status
```

## //Desabilitar modulo

```
bin/magento module:disable Magento_AdminNotification
```

## //Setar configuração do admin pelo cli

```
bin/magento config:set admin/security/password_is_forced 0
```
