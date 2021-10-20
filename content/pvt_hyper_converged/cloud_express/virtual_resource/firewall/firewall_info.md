---
title: "防火墙概述"
description: 本小节主要介绍青立方® 超融合易捷版防火墙。 
keywords: 青立方® 超融合易捷版，防火墙
weight: 05
collapsible: false
draft: false
---

防火墙能极大地提高一个内部网络或主机的安全性，通过策略配置，过滤不安全的服务，从而降低内部网络或主机的风险。为了加强位于基础网络 `vxnet-0` 中主机的安全性，可以在主机之前放置一个防火墙 （Security Group）。

青立方® 超融合易捷版为每个用户提供了一个缺省防火墙（ID 之后带有星标），默认打开 ICMP for ping 和 22 端口。

- 支持创建更多的防火墙。初始状态下，每个防火墙都不包含任何规则，也就是说任何端口都是封闭的，需要建立规则以打开相应的端口。
- 支持通过 “IP/端口组管理” 功能把具有相同特征的一组 IP 或者一组端口设置成为 “IP端口组”，并且在防火墙规则中进行添加，实现批量管理功能。