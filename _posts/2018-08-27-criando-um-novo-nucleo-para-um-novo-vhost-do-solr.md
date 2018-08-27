---
layout: post
title: 'Criando um novo nucleo para um novo vhost do Solr '
tags: Solr Magento
---
Esse tudo e apenas para adicionar um novo núcleo caso já tenha criado um e configurado o solr em um servidor com vários vhosts

Você pode adicionar um novo núcleo Solr Copiando do núcleo de /home/ROOT/solr/server/solr/core0 para /home/ROOT/solr/server/solr/core1 

Ajustei o novo nome principal no arquivo core.properties para core1. 

Isso criou um novo núcleo que poderia ser usado na instância do no novo vhost DOMINIO.com.br.

Depois disso, eu reiniciei o serviço Solr como usuário para inicializar um núcleo recém-criado



\[jonatan@server bin]$ pwd

/home/mmardegan/solr/bin

\[jonatan@server bin]$ ./solr restart

\================



Instalar o modulo https://github.com/integer-net/solr-magento1

Apos isso ajustei as configurações de conexão no backend do Magento e reindexei o Solr Search Index.
