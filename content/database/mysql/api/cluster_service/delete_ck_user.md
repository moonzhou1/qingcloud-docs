---
title: "del_ck_user"
description: 本小节主要介绍 MySQL Plus 删除分析示例帐号接口。 
keywords: mysql plus 删除 ClickHouse 帐号,add_ck_user，删除分析实例帐号
weight: 23
collapsible: false
draft: false
---

删除分析实例帐号。

## 请求参数

|<span style="display:inline-block;width:100px">参数</span> |<span style="display:inline-block;width:100px">类型</span>|<span style="display:inline-block;width:380px">描述</span>|<span style="display:inline-block;width:100px">是否必选</span>|
| :--- | :--- | :--- | :--- |
| action        | String | 响应动作。<li>取值 `RunClusterCustomService`  | Yes      |
| cluster        | String | 集群 ID。<li>取值示例 `cl-ouhutv70`  | Yes      |
| role           | String | 节点角色类型。 <li>取值 `analysis`，表示分析实例节点角色类型。 | Yes      |
| service        | String | 自定义服务类型。<li>取值 `del_ck_user`，表示删除分析实例帐号服务。 | Yes      |
| service_params | String | 自定义服务功能配置参数。<br> 取值示例 {"user":"test"} <br>- `user` 表示分析实例帐号名称。<span style="display: block; background-color: #D8ECDE; padding: 10px 24px; margin: 10px 0; border-left: 3px solid #00a971;"><b>说明</b>: <li>该配置参数输入格式，需为 URL 编码 JSON 格式。</li></span>  | Yes |

## 响应消息

|<span style="display:inline-block;width:100px">参数</span> |<span style="display:inline-block;width:100px">类型</span>|<span style="display:inline-block;width:380px">描述</span>|
| :--- | :--- | :--- |
| job_id     | String  | 执行任务的 Job ID。                        |
| service    | String  | 执行任务对应的服务。                           |
| ret_code   | Integer | 执行成功与否。<li>取值 `0` 表示成功，其他值则为错误代码。 |
| role       | String  | 节点对应的角色。                               |
| action     | String  | 响应动作。                                     |
| cluster_id | String  | 集群 ID。                                      |

## 示例

### 请求示例

```url
https://api.qingcloud.com/iaas/?
&action=RunClusterCustomService
&cluster=cl-ouhutv70
&role=analysis
&service=del_ck_user
&service_params=%7B%22user%22%3A%22test%22%7D
&zone=sh1a
&<COMMON_PARAMS>
```

### 响应示例

```json
"{u'job_id': u'j-iaj5uvzxd12',
 u'service': u'del_ck_user', 
 u'ret_code': 0, 
 u'role': u'analysis', 
 u'action': u'RunClusterCustomServiceResponse', 
 u'cluster_id': u'cl-ouhutv70'}"
```
