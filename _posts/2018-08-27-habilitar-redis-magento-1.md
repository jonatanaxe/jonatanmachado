---
layout: post
title: Habilitar Redis Magento 1
tags: Magento Redis
---
No seu arquivo  local.xml apos session_save adicione

```
<cache>
<backend>Cm_Cache_Backend_Redis</backend>
 <backend_options>
  <server>127.0.0.1</server>
   <port>6379</port>
   <persistent></persistent>
   <password></password>
   <force_standalone>0</force_standalone>
   <connect_retries>1</connect_retries>
   <read_timeout>10</read_timeout>
   <automatic_cleaning_factor>0</automatic_cleaning_factor>
   <compress_data>1</compress_data>
   <compress_tags>1</compress_tags>
   <compress_threshold>20480</compress_threshold>
   <compression_lib>gzip</compression_lib>
   <use_lua>0</use_lua>
 </backend_options>
</cache>
```
