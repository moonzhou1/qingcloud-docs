---
title: "共享备份"
description: 本小节主要如何共享 MongoDB Cluster 数据备份。 
keywords: MongoDB Cluster 共享备份；
weight: 80
collapsible: false
draft: false
---



在 AppCenter 集群管理控制台，MongoDB Cluster 支持将备份链共享给其他用户。

- 共享备份后，其他用户可在**共享备份**列表，根据备份创建集群。

- 共享备份后，可取消共享备份，立即收回集群备份使用权限，

更多集群备份管理说明，请参见[备份](/storage/backup/)。

本小节主要介绍如何共享 MongoDB Cluster 集群备份。

## 约束限制

- 仅共享当前备份主链，增量备份链不增量共享。
- 仅可分享给已注册用户。
- 逻辑备份的备份链不支持共享备份。

## 前提条件

- 已获取管理控制台登录账号和密码，且已获取集群操作权限。
- 已创建 MongoDB Cluster 集群状态为**活跃**。
- 已创建集群备份。
- 已获取其他用户 ID 或邮箱。

## 开启共享备份

1. 登录管理控制台。
2. 选择**产品与服务** > **数据库与缓存** > **文档数据库 MongoDB Cluster**，进入集群管理页面。
3. 选择目标集群，点击目标集群 ID，进入集群详情页面。
4. 在**备份**页签，选择目标备份链，右键展开备份操作列表。
   
   <img src="../../../_images/share_backup_1.png" alt="共享备份" style="zoom:50%;" />

5. 点击**共享备份**，弹出共享配置窗口。

   <img src="../../../_images/share_backup_2.png" alt="共享备份" style="zoom:50%;" />

6. 配置有效用户 ID 或邮箱。
7. 确认参数信息无误后，点击**确认**，返回备份列表页面。

   共享成功后，被共享的用户即可在 AppCenter **备份管理** > **共享备份**列表查看到集群备份信息。

## 取消共享备份

1. 登录管理控制台。
2. 选择**产品与服务** > **数据库与缓存** > **文档数据库 MongoDB Cluster**，进入集群管理页面。
3. 选择目标集群，点击目标集群 ID，进入集群详情页面。
4. 在**备份**页签，选择目标备份链，右键展开备份操作列表。
5. 点击**取消共享备份**，弹出取消共享配置窗口。

   <img src="../../../_images/share_backup_3.png" alt="共享备份" style="zoom:50%;" />

6. 勾选用户，可勾选多个用户。
7. 确认参数信息无误后，点击**确认**，返回备份列表页面。

   取消共享后，集群备份使用权限立即被收回。被共享的用户在 AppCenter **备份管理** > **共享备份**列表不再呈现备份信息。
