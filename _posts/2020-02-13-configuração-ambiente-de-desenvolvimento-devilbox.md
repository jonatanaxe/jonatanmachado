---
layout: post
title: Configuração ambiente de desenvolvimento DevilBox
tags: Devilbox
---
Adicione as configurações no seu arquivo .env do devilbox.

Apos isso rode o comando 

> docker-composer up

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

### Varnish version to choose

```
VARNISH_SERVER=6
```

### Varnish settings

```
VARNISH_CONFIG=/etc/varnish/default.vcl
VARNICS_CACHE_SIZE=128m
VARNISH_PARAMS=-p default_ttl=3600 -p default_grace=3600
HOST_PORT_VARNISH=6081
```
