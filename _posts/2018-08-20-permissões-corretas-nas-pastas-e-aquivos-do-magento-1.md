---
layout: post
title: Permissões corretas nas pastas e arquivos do magento 1
tags: Magento
---
Como não e recomendado você setar 777 na raiz do seu projeto muitas vezes já fiz isso :D  você pode rodar os seguintes comandos para arrumar as permissões corretas.

Navegue ate o diretório do seu projeto e rode os seguintes comandos.

> via terminal Linux

```
sudo find . -type d -exec chmod 755 {} \;
```

```
sudo find . -type f -exec chmod 644 {} \;
```

```
sudo chmod 777 -R app/etc/;
```

```
sudo chmod 777 -R var/;
```

```
sudo chmod 777 -R media/;
```
