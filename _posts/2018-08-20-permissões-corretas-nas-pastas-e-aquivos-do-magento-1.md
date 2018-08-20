---
layout: post
title: Permissões corretas nas pastas e aquivos do magento 1
---
Como não e recomendado você setas 777 na raiz do seu projeto muitas vezes já fiz isso :D  você pode rodar os seguintes comandos para arrumar as permissões

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
