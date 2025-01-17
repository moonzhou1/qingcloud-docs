---
title: "跨区域复制备份"
description: 本小节主要如何跨区域复制 MongoDB Cluster 数据备份。 
keywords: MongoDB Cluster 跨区域复制备份；
weight: 70
collapsible: false
draft: false
---



在 AppCenter 集群管理控制台，MongoDB Cluster 支持将集群备份跨区域复制。某一区域的实例故障后，可跨区域使用备份文件恢复到新的集群，用来恢复业务。

本小节主要介绍如何跨区域复制 MongoDB Cluster 集群备份。

## 前提条件

- 已获取管理控制台登录账号和密码，且已获取集群操作权限。
- 已创建 MongoDB Cluster 集群状态为**活跃**。
- 已创建集群备份。

## 操作步骤

1. 登录管理控制台。
2. 选择**产品与服务** > **数据库与缓存** > **文档数据库 MongoDB Cluster**，进入集群管理页面。
3. 选择目标集群，点击目标集群 ID，进入集群详情页面。
4. 在**备份**页签，选择目标备份链，展开备份链示意图。
5. 选择目标备份节点，展开备份节点操作列表。
   
   <img src="../../../_images/replication_backup_1.png" alt="跨区域复制备份" style="zoom:50%;" />

6. 点击**跨区域复制备份**，弹出跨区域备份配置窗口。

   <img src="../../../_images/replication_backup_2.png" alt="跨区域复制备份" style="zoom:50%;" />

7. 勾选目标区域。
8. 确认参数信息无误后，点击**确认**，返回备份列表页面。

   -在**全局操作日志**，查看备份复制进度。

   -复制成功后，即可基于备份在目标区域创建集群，详情请参见[从备份恢复集群](../restore_from_backup)。
