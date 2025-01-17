---
title: "远程控制 Windows 出现凭据无法工作问题"
weight: 12
draft: false
enableToc: false
---

## 问题背景
使用远程桌面访问 Windows 系统的云服务器时，出现如下错误。使用 web 终端连接服务器可正常登录。
![image-20210728204645945](../../../_images/win_not_work02-01.png)

## 解决方案

1. 打开组策略编辑器
   1. 找到**开始** >**运行** > **输入** `gpedit.msc`，打开注册表编辑器  
   2. 然后依次找到菜单，**计算机配置** > **管理模板** > **凭据分配** > **允许分配保存的凭据用于 NTLM 服务器身份验证**  

2. 选择**已启用**， 然后在**显示**里面输入 `TERMSRV/*  #允许保存所有`  

3. 刷新组策略，让设置生效。  

   1. **开始** > **运行** > **输入** `gpupdate /force` 强制刷新，如下图设置  
      ![image-20210728215249178](../../../_images/win_not_work02-02.png)

   2. 修改**允许分配保存的凭据用于仅 NTLM 服务器身份验证**的组策略，若以上方法无效，根据下面的步骤操作

      ![image-20210728214949330](../../../_images/win_not_work02-03.png)

   3. 快捷键 Win+R，在运行窗里输入 gpedit.msc，如图修改本地组策略编辑器。  

      **网络访问：本地账户的共享和安全模型**修改成**经典 - 对本地用户进行身份验证，不改变其本来身份**。  

      这样就可以重新 mstsc 远程控制了。



