---
layout: post
title: Aliases setar host no etc/hosts com base na pasta
---
Aliases setar o etc/hosts com base na pasta, no meu caso se eu estiver na pasta /teste/ ele vai gravar no /etc/hosts '127.0.0.1 teste.local'
```
alias ehostset='sudo sed -i "2i127.0.0.1 ${PWD##*/}.local" /etc/hosts'
```