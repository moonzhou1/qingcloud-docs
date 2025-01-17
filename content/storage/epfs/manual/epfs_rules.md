---
title: "添加文件存储 EPFS 规则"
date: 2020-01-30T00:39:25+09:00
description: Test description
draft: false
enableToc: false
weight: 10
keyword: 镜像, QingCloud
---

## 操作步骤

1. 在权限组点击添加规则，跳出如下界面：

   ![](../_images/efps7.png)

> **说明**
>
> 添加授权 IP，该权限组内所添加的授权 IP 地址允许以最高权限(读写)访问共享目录。为了最大限度保障您的数据安全，建议您谨慎添加权限组规则，仅为必要的地址授权。如添加1条acl，比如添加66.66.66.66，就是允许后端(IB网络)IP为66.66.66.66的主机挂载这个挂载点对应的目录。

2. 删除该挂载点的规则，如下所示：

   ![](../_images/efps8.png)

   ![](../_images/efps9.png)

> **说明**
>
> 删除授权 IP，就是删除该权限组内所添加的授权 IP 地址对该挂载点的最高权限(读写)访问共享目录。删除1条acl，比如删除6.6.6.6，就是移除后端(IB网络)IP为7.7.7.7的主机对这个挂载点的挂载权限。

