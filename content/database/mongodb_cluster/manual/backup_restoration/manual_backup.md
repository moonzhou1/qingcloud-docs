---
title: "创建手动备份"
description: 本小节主要如何创建 MongoDB Cluster 数据手动备份。 
keywords: MongoDB Cluster 数据手动备份；
weight: 10
collapsible: false
draft: false
---



在 AppCenter 集群管理控制台，MongoDB Cluster 提供数据备份管理，集群备份创建成功后，可基于备份点创建一个新集群恢复数据。

- MongoDB Cluster 集群硬盘可以创建多条备份链，每条备份链可包括一个**全量备份**和多个**增量备份**，支持从任意备份点恢复数据。

- 为确保集群数据的全量备份，MongoDB Cluster 还提供数据自动备份管理，通过设置自动备份时间，启动定时备份数据。

> **注意**
> 
> 为节省资源并保留充足的备份份额，可定期手动[清理过期备份](../delete_backup)。
> 
> 创建备份过程，将对集群造成一定的运行压力。为避免影响业务正常运行，建议在业务低峰期进行备份。

本小节主要介绍如何创建 MongoDB Cluster 集群手动备份。

## 约束限制

- 备份只能捕获已经写入磁盘的数据，不能捕获缓存里的数据。
- 多角色节点集群，暂不支持创建增量备份。

## 前提条件

- 已获取管理控制台登录账号和密码，且已获取集群操作权限。
- 已创建 MongoDB Cluster 集群状态为**活跃**。
- 已停止 MongoDB Cluster 集群的写操作。

## 操作步骤

1. 登录管理控制台。
2. 选择**产品与服务** > **数据库与缓存** > **文档数据库 MongoDB Cluster**，进入集群管理页面。
3. 选择目标集群，鼠标右键展开集群快速操作列表。
4. 点击**创建备份**，弹出备份提示窗口。

   <img src="../../../_images/backup_notice.png" alt="备份提示" style="zoom:50%;" />

5. 点击**继续**，配置备份信息。

    输入备份名称，以及勾选**创建新备份链接**。

   <img src="../../../_images/backup_config.png" alt="备份配置" style="zoom:50%;" />

6. 确认参数信息无误后，点击**保存**，返回备份列表页面。

   待集群状态切换为**活跃**，即创建集群当前备份完成。

    <img src="../../../_images/backup_list.png" alt="备份列表" style="zoom:100%;" />

## 相关操作

- [从备份恢复集群](../restore_from_backup)
- [删除备份](../delete_backup)
