---
title: "产品优势"
description: 本小节主要介绍 MongoDB Cluster 产品优势。 
keywords: MongoDB Cluster 产品优势 
weight: 25
collapsible: false
draft: false
---


## 高可用

MongoDB Cluster 将 Config Server 和 Shard 部署为副本集，可提供更高的可用性。即当一个或多个分片副本集不可用，分片集群也可以继续执行部分读写操作。

## 读/写负载均衡

MongoDB Cluster 将读写工作负载水平分布在 Sharded 集群中的分片上，允许每个分片处理集群操作的一个子集，除了传统数据库的中心化结构（过度依赖主节点进行写入），对数据进行水平拆分之后能使读写更加均衡。

对于包含分片键或复合分片键前缀的查询，Mongos 节点可将查询定位于特定的分片或分片集。这些目标操作通常比向集群中的每个分片广播效率更高。

## 存储容量负载均衡

随着数据量的增长，受到硬盘、内存等限制，单台服务器上运行 MongoDB 实例将越发影响数据库性能。

MongoDB Cluster 将来自客户端的所有请求均匀分配到到各个分片服务器上，允许每个分片包含总集群数据的一个子集。随着数据集的增长，附加的分片将增加集群的存储容量，解决了硬件瓶颈问题。

## 弹性伸缩

MongoDB Cluster 提供了集群资源管理功能，包括 CPU 规格、内存规格、存储空间、节点数量等。

## 监控可视化

AppCenter 控制台提供全面的监控信息，简单易用，灵活管理。
