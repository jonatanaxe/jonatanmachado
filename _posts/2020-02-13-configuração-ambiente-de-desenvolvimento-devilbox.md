---
layout: post
title: Configuração ambiente de desenvolvimento DevilBox
tags: Devilbox
---
Adicione as configurações no seu arquivo .env do devilbox.

Apos isso rode o comando 

> docker-compose up

As url dos projetos ficam https://nomedapasta.test

```
TLD_SUFFIX=test
NEW_UID=1000
NEW_GID=1000
TIMEZONE=America/Sao_Paulo
DNS_CHECK_TIMEOUT=1
DEVILBOX_UI_SSL_CN=localhost,*.localhost,devilbox,*.devilbox,httpd
MOUNT_OPTIONS=,z
MOUNT_OPTIONS=,cached
HOST_PATH_HTTPD_DATADIR=./data/www
HOST_PATH_SSH_DIR=~/.ssh
PHP_MODULES_ENABLE=

HTTPD_DOCROOT_DIR=htdocs
#HTTPD_DOCROOT_DIR=

HTTPD_NGINX_WORKER_PROCESSES=auto
HTTPD_NGINX_WORKER_CONNECTIONS=1024

BIND_DNS_RESOLVER=8.8.8.8,8.8.4.4
```
