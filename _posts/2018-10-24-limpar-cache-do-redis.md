---
layout: post
title: Limpar cache do redis
tags: redis
---
Com acesso root voce pode rodar os seguntes comandos

```
redis-cli
```

```
127.0.0.1:6379> FLUSHDB
```

```
OK
```

```
127.0.0.1:6379> FLUSHALL
```

```
OK
```

```
127.0.0.1:6379> exit
```
