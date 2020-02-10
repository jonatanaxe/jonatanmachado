---
layout: post
title: Redirecionar 301 .aspx ou outra extensão pra um link novo
tags: Rewriterule
---
Muitas vezes quando mudamos de linguagem de um site temos muitos problemas com os links antigos que já estão indexado no google, no apache você pode usar regra do rewrite como no exemplo.

No caso eu estou redirecionando todos os links final ".aspx" para a home do site.

`
RewriteRule ^(.*).aspx$ http://www.jonatanaxe.com.br? [R=301,L,QSA]
`

Obrigado :D
