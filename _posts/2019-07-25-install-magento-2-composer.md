---
layout: post
title: Install magento 2 composer
tags: magento2
---
Creio que você já tenha o ambiente instalado e configurado caso não tenha você pode usar meu tutorial

[Ambiente de desenvolvimento Magento 2](https://jonatanmachado.tk/install-ambiente-desenvolvimento-magento-2-ubuntu-19/)

```
composer --version && sudo composer self-update && composer clear-cache
```
```
sudo chown -R $USER $HOME/.composer
```
```
composer create-project --repository-url=https://repo.magento.com/ magento/project-community-edition projeto1.test
```

Após isso vai pedir usuário e senha
Acesse com sua conta https://marketplace.magento.com/
Você vai gerar usuário(Public Key) senha(Private Key)

```
Public Key: 11111111111111111111111111111

Private Key: 11111111111111111111111111111111
```

Agora pode acessar o a url do projeto e seguir os passos

http://projeto1.test
