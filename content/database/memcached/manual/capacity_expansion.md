---
title: "扩容集群"
description: 本小节主要介绍如何扩容 Memcached 集群。 
keywords: memcached 扩容集群
data: 2021-05-14T00:38:25+09:00
weight: 20
collapsible: false
draft: false
---



在缓存服务运行过程中，会出现服务能力不足或者容量不够的情况，可以通过扩容来解决。

## 增加缓存节点

Memcached 缓存服务支持多个缓存节点。当容量或者性能不足时，可以通过增加缓存节点来提升。 

> 默认的 Memcached 客户端使用简单 Hash 来进行数据分片，当增加或删除节点时可能会造成大量的缓存失效。可以采用支持一致性 Hash 算法的 Memcached 客户端来避免这个问题，例如 [hash_ring](https://pypi.python.org/pypi/hash_ring)  客户端。

1. 在集群管理页面，点击集群 ID，进入集群详情页面。
2. 在**节点**页签，点击**新增节点**。
3. 在弹出的节点配置窗口，配置节点数量、节点名称、节点 IP，并点击**提交**。
   
   ![新增节点](../../_images/add_node.png)
   
4. 返回**节点**页签，查看增加的节点。

   ![查看新增节点](../../_images/check_node.png)

## 增加缓存容量

当缓存容量不足时，您可以通过扩容操作来提升缓存容量。

> 注意：
> 
> - 扩容集群可能会导致中断服务, 请在业务空闲期执行扩容操作。
> - 在线扩容期间，缓存服务会被重启。因 Memcached 不支持持久化，当服务重启后，内存中缓存的数据将被重置而失效。
> - 扩容后可以通过配置 `threads` 和 `max_memory`，对缓存服务进行调优。

1. 在集群管理页面，选择目标 Memcached 集群。
2. 在目标集群上点击右键，点击**扩容集群**。
3. 在弹出的扩容集群窗口，选择节点 CPU、内存参数值。确认信息无误后，点击**提交**。
   
   ![扩容集群](../../_images/expansion.png)

4. 进入集群详情页面，在**节点**页签，可查看扩容后配置。

   ![查看扩容后配置](../../_images/check_expansion.png)