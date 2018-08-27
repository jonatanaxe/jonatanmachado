---
layout: post
title: 'Criando um novo nucleo para um novo vhost do Solr '
tags: Solr Magento
---


Esse tutorial é apenas para adicionar um novo núcleo caso já tenha criado um e configurado o solr em um servidor com vários vhosts

Caso nao tenha instaldo o java e o server solr no seru server voce deve fazer isso antes de continuar

Você pode adicionar um novo núcleo Solr Copiando do núcleo ja que esta em uso

> /home/ROOT/solr/server/solr/core0 para /home/ROOT/solr/server/solr/core1 

Ajustei o novo nome principal no arquivo core.properties para core1. 

Isso criou um novo núcleo que poderia ser usado na instância do no novo vhost.

Depois disso, eu reiniciei o serviço Solr como usuário para inicializar um núcleo recém-criado

> \[jonatan@server bin]$ pwd
>
> /home/ROOT/solr/bin
>
> \[jonatan@server bin]$ ./solr restart

\================

Instalar o modulo https://github.com/integer-net/solr-magento1

Apos isso ajustei as configurações de conexão no backend do Magento e reindexei o Solr Search Index.
