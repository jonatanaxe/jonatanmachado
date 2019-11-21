---
layout: post
title: Magento 2 cli Comandos Úteis
tags: Magento2
---
//upgrade
> php bin/magento setup:upgrade

//compilar backend
> php bin/magento setup:di:compile

//compilar front
> php bin/magento setup:static-content:deploy -theme tema/tema_novo  pt_BR -f

//limpar caches e arquivos gerados
> php bin/magento cache:flush

//apagar estáticos
> rm -rf pub/static/* 

//apagar arquivos gerados
> rm -rf var/* 

//habilitar todos os caches
> php bin/magento cache:enable

//reindexar tudo
> php bin/magento indexer:reindex

//criar ou atualizar usuário admin
> php bin/magento admin:user:create -admin-user='jonatan@jonatanmachado.tk' -admin-password='jonatan123' --admin-email='jonatan@jonatanmachado.tk' -admin-firstname='Admin' -admin-lastname='Admin'

//listar todos os modulos instalado e o status
> bin/magento module:status

//desabilitar modulo
> bin/magento module:disable Magento_AdminNotification

//setar configuração do admin pelo cli
> bin/magento config:set admin/security/password_is_forced 0
