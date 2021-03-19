---
title: 在“任务”网格中工作故障排除
description: 本主题提供在“任务”网格中工作时所需的故障排除信息。
author: ruhercul
manager: tfehr
ms.date: 01/19/2021
ms.topic: article
ms.product: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: dedd989cc7c959d9ea97a0abfb13f8f1b2150a56
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/15/2021
ms.locfileid: "5286552"
---
# <a name="troubleshoot-working-in-the-task-grid"></a>在“任务”网格中工作故障排除 

_**适用于：** 基于资源/非库存场景的 Project Operations，精简部署 - 估价开票交易_

本主题介绍如何解决使用成本管理时可能遇到的问题。

## <a name="enable-cookies"></a>启用 Cookie

Project Operations 需要启用第三方 Cookie 来呈现工作分解结构。 如果未启用第三方 Cookie，在选择 **项目** 页上的 **任务** 选项卡时，您会看到空白页面，而不是看到任务。

![未启用第三方 Cookie 时的空白选项卡](media/blankschedule.png)


### <a name="workaround"></a>解决办法
对于 Microsoft Edge 或 Google Chrome 浏览器，以下过程概述了如何更新浏览器设置以启用第三方 Cookie。

#### <a name="microsoft-edge"></a>Microsoft Edge

1. 打开 Edge 浏览器。
2. 在右上角选择 **省略号** (...)，然后选择 **设置**。
3. 在 **Cookie 和站点权限** 下，选择 **Cookie 和站点数据**。
4. 关闭 **阻止第三方 Cookie**。

#### <a name="google-chrome"></a>Google Chrome

1. 打开 Chrome 浏览器。
2. 在右上角，选择三个垂直排列的点，然后选择 **设置**。
3. 在 **隐私和安全性** 下，选择 **Cookie 和其他站点数据**。
4. 选择 **允许所有 Cookie**。

> [!IMPORTANT]
> 如果您阻止第三方 Cookie，将阻止其他站点的所有 Cookie 和站点数据，即使您的例外列表中允许该站点。

## <a name="pex-endpoint"></a>PEX 终结点

Project Operations 需要项目参数引用 PEX 终结点。 需要此终结点与用于呈现工作分解结构的服务进行通信。 如果未启用此参数，您将收到错误“项目参数无效”。 

### <a name="workaround"></a>解决办法
 ![项目参数上的 PEX 终结点字段](media/projectparameter.png)

1. 将 **PEX 终结点** 字段添加到 **项目参数** 页中。
2. 使用以下值更新此字段：`https://project.microsoft.com/<lang>/?org=<cdsServer>#/taskgrid?projectId=\<id>&type=2`
3. 从 **项目参数** 页删除此字段。

## <a name="privileges-for-project-for-the-web"></a>Web 项目的特权

Project Operations 依赖于外部计划服务。 此服务需要用户分配有多个角色以可以读取和写入与工作分解结构相关的实体。 这些实体包括项目任务、资源分配和任务依赖关系。 如果用户在转到 **任务** 选项卡时无法呈现工作分解结构，可能是因为尚未启用 Project Operations 项目。 用户可能会收到安全角色错误或与拒绝访问相关的错误。


## <a name="workaround"></a>解决办法

1. 转到 **设置 > 安全 > 用户 > 应用程序用户**。  

   ![应用程序读取器](media/applicationuser.jpg)
   
2. 双击应用程序用户记录验证以下各项：

 - 用户有权访问项目。 此验证通常通过确保用户具有 **项目经理** 安全角色来完成。
 - Microsoft Project 应用程序用户已存在并且配置正确。
 
3. 如果此用户不存在，您可以创建一个新用户记录。 选择 **新建用户**。 将输入窗体更改为 **应用程序用户**，然后添加 **应用程序 ID**。

   ![应用程序用户详细信息](media/applicationuserdetails.jpg)

4. 在许可证的服务计划详细信息中验证是否已为用户分配了正确的许可证，并且已启用了服务。
5. 验证用户是否可以打开 project.microsoft.com。
6. 通过项目参数验证系统是否指向正确的项目终结点。
7. 验证是否已创建项目应用程序用户。
8. 向用户应用以下安全角色：

  - Dataverse 用户
  - Project Operations 系统
  - 项目系统

## <a name="error-when-updating-the-work-breakdown-structure"></a>更新工作分解结构时出错

当对工作分解结构进行一个或多个更新时，更改最终失败并且未保存。 计划网格中出现错误，指出“无法保存您最近所作的更改。”

### <a name="workaround"></a>解决办法

1. 在许可证的服务计划详细信息中验证是否已为用户分配了正确的许可证，并且已启用了服务。
2. 验证用户是否可以打开 project.microsoft.com。
3. 验证系统是否指向正确的项目终结点。
4. 验证是否已创建项目应用程序用户。
5. 向用户应用以下安全角色：
  
  - Dataverse 用户或基本用户
  - Project Operations 系统
  - 项目系统
  - Project Operations 双重写入系统（如果要部署面向资源/非库存场景的 Project Operations，则需要此角色。）


[!INCLUDE[footer-include](../includes/footer-banner.md)]