---
title: "配置解析线路"
description: dns配置解析线路
date: 2021-04-28T00:38:25+09:00
weight: 4
draft: false
keyword: DNS解析线路,
---



QingCloud DNS 为客户提供逾1600条解析线路，国内精确到运营商，海外精确到国家。

- 当前 QingCloud DNS 默认提供5条线路，包括**全网默认**、**中国电信**、**中国联通**、**中国移动**、**港澳台及海外** 。

- 若业务环境对解析线路有特殊要求，且为了高效管理域名，建议提前规划域名的有效线路。

本小节主要介绍如何配置自定义解析线路。

## 操作步骤

1. 登录 QingCloud 管理控制台。
2. 选择**产品与服务** > **网络服务** > **云解析 DNS**，进入域名列表页。
3. 点击域名名称，进入域名解析记录页面。
4. 选择**域名配置**页签，展开域名域名配置管理信息。

   ![域名配置](../_images/dns_route_config.png)

5. 在**功能配置**区域，点击**编辑线路**，弹出线路编辑窗口。

   ![修改线路配置](../_images/modify_dns_route.png)

6. 在对话框中添加或移除线路。

   > 默认全国线路不支持移除。
   > 已在域名解析中使用的线路不支持移除。

7. 点击**保存**，即可在该域名**解析记录**的配置线路下拉框中，查看到配置的线路。