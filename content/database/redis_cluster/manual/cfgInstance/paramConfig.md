---
title: "配置集群参数"
description: 本小节介绍如何配置集群参数。
weight: 8
collapsible: false
draft: false
keywords: QingCloud，Redis Cluster，参数配置
---

 Redis Cluster 支持自定义部分参数的值，您可以根据自己的业务情况对集群运行参数进行调整，使缓存服务发挥出最优性能。

## 背景信息

不同 Redis 版本支持的参数有所区别，详细说明请参见[参数支持](../../../intro/para_list/)。本文为您介绍各参数的设置方法。

## 操作步骤

1. 登录 [QingCloud 管理控制台](https://console.qingcloud.com/login)。

2. 在控制台顶部的导航菜单中，选择**产品与服务** > **数据库与缓存** > **键值数据库 Redis**，进入 Redis Cluster 管理页面。

3. 点击目标集群 **ID** 号，进入集群详情页面。

4. 在页面右侧区域，点击**配置参数**页签。

   页面显示当前版本所支持的所有参数配置项、参数描述及参数当前值。

   <img src="../../../_images/mdy_paras.png" alt="参数配置" />

5. 点击**修改属性**，参数值变为可编辑状态。

   > **说明**
   >
   > 部分参数仅支持在创建集群时配置，此处不可修改，仅作为展示。

6. 根据实际情况进行参数值修改。

7. 修改完成后，点击**保存**，弹出提示框。

8. 确认无误后，点击**确认**。
