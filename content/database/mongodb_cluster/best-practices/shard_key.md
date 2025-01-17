---
title: "分片键配置选型"
description: 本小节主要介绍如何选择 MongoDB Cluster 的分片键。 
keywords: MongoDB Cluster 分片键, 分片键选择 
weight: 10
collapsible: false
draft: true
---

MongoDB Cluster 为 MongoDB 的分片集群，即 MongoDB 的分布式版本。相较于 MongoDB 副本集，分片集群架构更加复杂，在性能上突破数据存储瓶颈，并缓解了读/写压力。因为分片集群的数据被均衡的分布在不同分片中，不仅可提升集群的数据容量，也可将读/写的压力分散到不同分片上。

本小节主要介绍如何选择 MongoDB Cluster 的分片键。

## Shard 简介

### 集群组件

一个 MongoDB Cluster 集群由如下三个组件构成：

- Shard：每组分片是整体数据的一部分子集，每组分片都部署包括 3 个副本集节点。

- Mongos：数据库访问接口，提供客户端应用程序与集群之间的接口。

- Config Servers：存储集群的元数据和配置，包括权限认证相关信息。

### Shard 方式

MongoDB Cluster 集群提供三种 Shard 数据分布方式，分别为基于范围、基于 Hash、基于标签。不同的分片方式适用于不同的业务，可能在性能上有不同特点。

- **基于范围**

   基于分片键范围查询性能较好，读性能较好。但可能导致数据分布不均匀，存在冷热点。

- **基于 Hash**

   基于 Hash 数据分布均匀，写性能较好，适用于日志、物联网等高并发场景。但范围查询效率较低。

- **基于标签**
  
  若数据具备基于地域、时间等标签的划分，数据可以基于标签来做区分，具备数据分布较为合理优势。

## 分片键选择

分片键（ Shard Key）是文档中的某一个字段，用来进行路由查询。分片键对 Shard 查询效率影响较大，可基于如下四个因素选择：

- **取值基数**

   取值基数选择尽可能大。
   
   因为小基数的片键的备选值有限，导致块的总数量就有限。随着数据增多，块越来越大，水平扩展时很难移动块，导致数据分布不均匀，影响数据库整体性能。

- **取值分布**

   取值分布选择尽可能均衡。
   
   若片键分布不均匀，可能造成某些块的数据量非常大，导致数据分布不均匀，影响数据库整体性能。

- **带分片查询**

   选择带分片查询。
   
   使用分片键进行条件查询，Mongos 直接定位到分片。否则 Mongos 要将查询分发到所有分片，再等待返回响应，在查询上有所延迟。

- **避免单调增/减**

   单调递增的分片键，数据文件位移小。但会引起写入数据集中，导致最后写入的一篇文档的数据量持续增大，不断发生迁移。

总之，为获取更优数据库性能，有效降低 MoveChuncks 对数据库性能的影响，分片键的选择需尽量满足以上四个条件。
