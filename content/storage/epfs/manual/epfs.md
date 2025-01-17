---
title: "创建文件存储 EPFS"
date: 2020-01-30T00:39:25+09:00
description: Test description
draft: false
enableToc: false
keyword: 镜像, QingCloud
weight: 1
---

## 前提条件

文件存储 EPFS 仅能在济南1区创建。

## 操作步骤

1. 登录 [QingCloud 管理控制台](https://console.qingcloud.com/login)，选择**产品与服务** > **存储** > **文件存储 EFPS**，进入**文件存储 EFPS**页签。

   ![](../_images/efps1.png)

2. 点击立即开通，开通文件存储 epfs 服务。

3. 点击**去创建**进入购买界面。

   ![](../_images/efps2.png)

4. 创建挂载点。

   ![](../_images/efps3.png)

5. 创建后的挂载点如图所示。

   ![](../_images/efps4.png)

6. 可以对当前挂载点进行扩容操作，根据需要进行扩容。

   <img src="../_images/efps20.png" style="zoom:50%;" />

7. 点击创建的挂载点进入如下界面

   ![](../_images/efps5.png)

8. 进入文件系统界面，可以查看基本属性，包括共享目录，配额，使用率，创建时间，gid/uid。

   ![](../_images/efps6.png)

9. 在权限组点击添加规则，跳出如下界面：

   ![](../_images/efps7.png)

   > **说明**
   >
   > 添加授权 IP，该权限组内所添加的授权 IP 地址允许以最高权限(读写)访问共享目录。为了最大限度保障您的数据安全，建议您谨慎添加权限组规则，仅为必要的地址授权。如添加1条acl，比如添加66.66.66.66，就是允许后端(IB网络)IP为66.66.66.66的主机挂载这个挂载点对应的目录。

8. 删除该挂载点的规则，如下所示：

   ![](../_images/efps8.png)

   ![](../_images/efps9.png)

> **说明**
>
> 删除授权 IP，就是删除该权限组内所添加的授权 IP 地址对该挂载点的最高权限(读写)访问共享目录。删除1条acl，比如删除6.6.6.6，就是移除后端(IB网络)IP为7.7.7.7的主机对这个挂载点的挂载权限。

