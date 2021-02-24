---
layout: post
title: Aliases alterar  urlbase do magento 2
tags: Magento2
---
Fiz dois alias, um lista e o outro seta as url base dinamica, com base no diretorio que voce esta, no meu caso se eu estiver na pasta /teste/ ele vai gravar no banco [http://teste.local/](http://veiling-holambra.local/ "http\://veiling-holambra.local/") 

(No caso precisa ter o n98)



> alias n98urlbase='n98 db:query "select * from core_config_data where path like \"%base%url%\";"' 
>
> alias n98urlbaseset='n98 db:query "update core_config_data set value = \"http://${PWD##\*/}.local/\" where path = \"web/unsecure/base_url\";update core_config_data set value = \"http://${PWD##\*/}.local/\" where path = \"web/secure/base_url\";update core_config_data set value = \"http://${PWD##\*/}.local/\" where path = \"web/unsecure/base_link_url\";update core_config_data set value = \"http://${PWD##\*/}.local/\" where path = \"web/secure/base_link_url\";" && n98urlbase'