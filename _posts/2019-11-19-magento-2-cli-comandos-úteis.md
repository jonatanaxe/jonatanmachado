---
layout: post
title: Magento 2 cli Comandos Úteis
tags: Magento 2
---
//upgrade
> php bin/magento setup:upgrade

//compilar backend
> php bin/magento setup:di:compile

//compilar front
> php bin/magento setup:static-content:deploy --theme tema/tema_novo  pt_BR -f

//limpar caches e arquivos gerados
> php bin/magento cache:flush
> rm -rf pub/static/* 
> rm -rf var/* 

//habilitar todos os caches
> php bin/magento cache:enable

//reindexar tudo
> php bin/magento indexer:reindex

//criar ou atualizar usuário admin
> php bin/magento admin:user:create --admin-user='jonatan@jonatanmachado.tk' --admin-password='jonatan123' --admin-email='jonatan@jonatanmachado.tk' --admin-firstname='Admin' --admin-lastname='Admin'
