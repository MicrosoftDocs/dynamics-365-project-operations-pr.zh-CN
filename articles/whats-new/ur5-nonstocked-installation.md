---
title: 在 Finance 环境中更新 Project Operations
description: 本主题提供有关如何在 Dynamics 365 Finance 环境中更新 Project Operations 的信息。
author: ruhercul
manager: tfehr
ms.date: 12/11/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: d68296ec59f0bd58f848154c90e02c58f275ab12
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/15/2021
ms.locfileid: "5291968"
---
# <a name="update-project-operations-in-your-finance-environment"></a>在 Finance 环境中更新 Project Operations

_**适用于：** 面向资源/非库存场景的 Project Operations_


本主题提供有关如何在 Dynamics 365 Finance 环境中更新 Dynamics 365 Project Operations 的信息。 将 Project Operations 更新为更新 5 (UR5) 需要三个过程：

- [将包导入预览项目](#import)
- [应用更新](#apply)
- [更新 Dataverse 环境](#update)

## <a name="import-the-package-into-your-lcs-project"></a><a name="import"></a>将包导入 LCS 项目

1. 作为项目负责人或环境经理登录到 [Lifecycle Services (LCS)](https://lcs.dynamics.com/)。
2. 从项目列表中，选择您的 LCS 项目。
3. 在 **项目** 页上的 **环境** 组中，打开要更新的环境。
4. 验证环境是否正在运行。 如果未启动，请启动该环境。
5. 在 **可用更新** 下的 **新版本** 部分，选择 10.0.15 对应的 **查看更新**。

![查看更新按钮](media/view-update.png)

6. 在 **二进制更新** 页上，选择 **保存包**。
7. 在 **查看和保存更新** 页上，选择 **保存包**。
8. 在打开的 **将包保存到资产库** 窗格中，输入包名称，然后选择 **保存包**。
9. LCS 保存完包后，**完成** 按钮将启用。 选择 **完成**。 LCS 将验证包。 验证可能花几分钟，最多一小时。


## <a name="apply-the-package-update"></a><a name="apply"></a>应用包更新

1. 在 LCS 中的 **环境详细信息** 页上，选择 **维护** > **应用更新**。
2. 在列表中，选择之前保存的包，然后选择 **应用**。
3. 选择 **是** 确认您要部署该包。

![确认包部署对话框](media/confirm-package-deployment.png)

4. 选择 **是** 确认您要更新应用程序。

![确认应用程序更新对话框](media/confirm-application-update.png)

部署和应用程序更新将开始。 

在 **环境详细信息** 页的右上角，环境状态将更新为 **服务**。 大约两个小时后，更新将完成。 应用程序版本信息将更新为 **Microsoft Dynamics 365 for Finance and Operations 10.0.15)**，环境状态将更新为 **已部署**。


## <a name="update-your-dataverse-environment"></a><a name="update"></a>更新 Dataverse 环境

1. 登录 [Power Platform 管理中心](https://admin.powerplatform.com/)。
2. 在列表中，查找并打开用于安装 Project Operations 的环境。
3. 在 **环境** 页上，选择 **资源** > **Dynamics 365 应用**。
4. 在列表中，找到 **Microsoft Dynamics 365 Project Operations**，在 **状态** 列中，选择 **有可用更新**。
5. 选中 **我同意服务条款** 复选框，然后选择 **更新**。 将安装解决方案的最新版本。

安装完成后，您已安装了版本 4.5.0.134。

## <a name="configure-new-features"></a>配置新功能

### <a name="enable-dual-write-mapping"></a>启用双重写入映射

在 Finance 和 Dataverse 环境上完成更新后，可以启用所需的双重写入映射。 完成以下过程启用双重写入映射。

- [更新 Customer Engagement 环境的安全设置](#security)
- [刷新数据实体](#refresh)
- [更新和运行双重写入映射](#run)

### <a name="update-security-settings-on-the-dataverse-environment"></a><a name="security"></a>更新 Dataverse 环境的安全设置

对实体的安全特权的以下更新是更新 UR5 所必需的。

1. 在 Dataverse 环境中，转到 **设置**，在 **系统** 组中，选择 **安全**。

![Dataverse 环境设置](media/Picture21.png)

2. 选择 **安全角色**。
3. 在角色列表中，选择 **双重写入应用用户**，然后选择 **自定义实体** 选项卡。 
4. 验证角色对以下各项具有 **读取** 和 **追加到** 权限：

      - **货币汇率类型**
      - **会计科目表** 
      - **会计日历** 
      - **分类帐**

5. 更新安全角色后，转到 **设置** > **安全** > **团队**。 确认 **双重写入应用用户** 角色已应用于团队。 

### <a name="refresh-data-entities-from-the-update"></a><a name="refresh"></a>从更新刷新数据实体

1. 在 Finance 环境中，打开 **数据管理** 工作区，然后打开 **Framework 参数** 页。
2. 在 **实体设置** 选项卡上，选择 **刷新实体列表**。
3. 选择 **关闭** 确认实体刷新。

 > [!NOTE]
 > 此过程大约需要 20 分钟完成。 刷新完成后，您会收到通知。

### <a name="update-dual-write-mappings"></a><a name="run"></a>更新双重写入映射

1. 在 **数据管理** 工作区，选择 **双重写入**。
2. 选择 **应用解决方案**，在列表中选择两个解决方案，然后选择 **应用**。
3. 在 **双重写入** 页上，选择以下表映射，然后选择 **停止**。

    - **Project Operations 集成实际值 (msdyn_actuals)**
    - **Project Operations 集成项目支出类别 (msdyn_expensecategories)**
    - **Project Operations 集成实际值项目支出导出实体 (msdyn_expenses)**

4. 在 **表映射版本** 页上，对这三个实体的每个实体应用新版本的映射。
5. 在 **双重写入** 页上，选择运行重新启动映射。
6. 从映射列表中，选择具有所有先决条件的 **分类帐(msdyn_ledgers)** 映射，然后选中 **初始同步** 复选框。 
7. 在 **用于初始同步的主应用** 中，选择 **Finance and Operations 应用**，然后选择 **运行**。
 
 ![分类帐映射同步](media/DW6.png)
 


[!INCLUDE[footer-include](../includes/footer-banner.md)]