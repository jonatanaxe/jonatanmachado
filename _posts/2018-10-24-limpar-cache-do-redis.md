---
layout: post
title: Limpar cache do redis
tags: redis
---
Com acesso root você pode rodar os seguintes comandos

> \[jonatan@server]$ redis-cli
>
> 127.0.0.1:0000> FLUSHDB
> OK
>
> 127.0.0.1:0000> FLUSHALL
> OK
>
> 127.0.0.1:0000> exit
