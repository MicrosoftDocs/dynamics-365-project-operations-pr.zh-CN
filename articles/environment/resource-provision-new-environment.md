---
title: 设置新环境
description: 此主题提供有关如何设置新的 Project Operations 环境的信息。
author: sigitac
manager: Annbe
ms.date: 12/11/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 09af2a7693c45d1d0b9c75420d018cc50d2cc0fa
ms.sourcegitcommit: 04c446746aad97fc3f4c3d441983c586b918a3a6
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/11/2020
ms.locfileid: "4727779"
---
# <a name="provision-a-new-environment"></a>设置新环境

_**适用于：** 面向资源/非库存场景的 Project Operations_

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

此主题提供有关如何为资源/非库存场景预配新 Dynamics 365 Project Operations 环境的信息。

## <a name="enable-project-operations-automated-provisioning-in-an-lcs-project"></a>在 LCS 项目中启用 Project Operations 自动设置

请使用以下步骤为 LCS 项目启用 Project Operations 自动设置流。

1. 转到 [LCS](https://lcs.dynamics.com/v2)，选择 **预览功能管理** 磁贴。
2. 在 **预览功能** 列表中，选择 **Project Operations 功能**，然后选择 **已启用预览功能** 启用 Project Operations。

> [!NOTE]
> 每个 LCS 项目仅执行一次此步骤。

## <a name="provision-a-project-operations-environment"></a>设置 Project Operations 环境

1. 打开新的 Dynamics 365 Finance [演示环境](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment)或[沙盒/生产环境](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deployenvironment-newinfrastructure)部署。 
2. **环境设置** 向导演练。 

> [!IMPORTANT]
> 确保所选的应用程序版本为 10.0.13 或更高版本。

3. 若要设置 Project Operations，在 **高级设置** 下选择 **Common Data Service**。 
4. 选择 **是** 启用 **Common Data Service 设置**，然后在必填字段中输入信息：

  - 客户
  - 区域
  - 语言
  - 货币
 
5. 在 **Common Data Service 模板** 字段中，选择 **Project Operations** 

6. 选择部署的环境类型。 通过基于订阅的试用，您可以在 30 天内部署 CDS 环境。 

![部署设置](./media/1DeploymentSettings.png)

> [!IMPORTANT]
> 选择 **同意** 确认服务条款，然后选择 **完成** 返回部署设置。

![同意部署](./media/2DeploymentConsent.png)

7. 可选 - 将演示数据应用到环境。 转到 **高级设置**，选择 **自定义 SQL 数据库配置**，将 **为应用程序数据库指定数据集** 设置为 **演示**。

8. 完成向导中的其余必填字段，并确认部署。 预配环境的时间因环境类型而异。 设置最多可能需要 6 个小时。

  在成功完成部署后，环境将显示 **已部署**。

9. 要确认环境已成功部署，请选择 **登录**，然后登录到环境进行确认。

![ 环境详细信息](./media/3EnvironmentDetails.png)

## <a name="apply-updates-to-the-finance-environment"></a>将更新应用于 Finance 环境

Project Operations 需要应用程序版本为 **10.0.13 (10.0.569.20009)** 或更高的 Finance 环境。

您可能需要对您的 Finance 环境应用高质量更新才能获得此版本。

1. 在 LCS 中，在 **环境详细信息** 页上的 **可用更新** 部分，选择 **查看更新**。

![查看更新](./media/5ViewUpdates.png)

2. 在 **二进制更新** 页上，选择 **保存包**。

![保存包](./media/6SavePackage.png)

3. 单击 **全选**，然后选择 **保存包**。

![查看和保存更新](./media/7ReviewAndSaveUpdates.png)

4. 输入包的名称和说明，然后选择 **保存**。 根据 Internet 连接的不同，此过程可能需要一些时间。

![将包上载到资产库](./media/8UploadPackageToAssetsLibrary.png)

5. 保存包后，请选择 **完成**，然后将此包保存到您的 LCS 项目的资产库中。

保存和验证包可能需要约 15 分钟时间。

6. 若要应用更新，导航到 LCS 中的 **环境详细信息** 页，选择 **维护** > **应用更新**。

![维护环境](./media/9MaintainEnvironment.png)

7. 在更新列表中，选择您创建的包，然后选择 **应用**。

![应用更新](./media/10ApplyUpdates.png)

维护环境需要一些时间。 完成后，环境将返回到已部署状态。

![环境已部署](./media/11EnvironmentDeployed.png)

## <a name="establish-a-dual-write-connection"></a>建立双写入连接 

1. 在您的 LCS 项目中，转到 **环境详细信息** 页。
2. 在 **Common Data Service 环境信息** 下，选择 **链接到面向应用程序的 CDS**。
3. 链接完成后，再次选择 **链接到面向应用程序的 CDS**。 您将被重定向到 Finance 中的“双写入”。

![指向 CDS 的链接](./media/12LinktoCDS.png)

4. 选择 **应用解决方案** 访问将在集成中映射的实体。

![应用解决方案](./media/13ApplySolutions.png)

5. 选择 **Dynamics 365 Finance and Operations 双重写入实体映射** 和 **Dynamics 365 Project Operations 双重写入实体映射** 这两个解决方案，然后选择 **应用**。

![确认解决方案](./media/14ConfirmSolutions.png)

应用解决方案后，双写入实体将应用于环境。

![应用解决方案](./media/15ApplyingSolutions.png)

应用实体后，所有可用映射都将在环境中列出。

![双写入映射](./media/15DWMappings.png)

## <a name="refresh-the-data-entities-after-the-update"></a>更新后刷新数据实体

1. 在 Finance 中，转到 **数据管理** 工作区。

![数据管理工作区](./media/16DataManagement.png)

2. 选择 **框架参数** 磁贴。

![框架参数](./media/17FrameworkParameters.png)

3. 在 **实体设置** 页上，选择 **刷新实体列表**。

![刷新实体列表](./media/18RefreshEntityList.png)

刷新时间大约需要 20 分钟。 完成时，您将收到警报。

![刷新确认](./media/19RefreshConfirmation.png)

## <a name="update-security-settings-on-project-operations-on-dataverse"></a>在 Dataverse 上更新 Project Operations 上的安全设置

1. 在您的 Dataverse 环境中转到 Project Operations。 
2. 转至 **设置** > **安全** > **安全角色**。 
3. 在 **安全角色** 页上的角色列表中，选择 **双重写入应用用户**，然后选择 **自定义实体** 选项卡。  
4. 验证角色对以下各项具有 **读取** 和 **追加到** 权限：
      
      - **货币汇率类型**
      - **会计科目表**
      - **会计日历**
      - **分类帐**

5. 更新安全角色后，转到 **设置** > **安全** > **团队**，然后在 **本地企业负责人** 团队视图中选择默认团队。
6. 选择 **管理角色**，验证 **双重写入应用用户** 安全特权是否应用于此团队。

## <a name="run-project-operations-dual-write-maps"></a>运行 Project Operations 双写入映射

1. 在您的 LCS 项目中，转到 **环境详细信息** 页。
2. 在 **Common Data Service 环境信息** 下，选择 **链接到面向应用程序的 CDS**。 选择链接后，您将被重定向到映射中的实体列表。
3. 如下表所述启动映射。 请确保按照列出的顺序操作。

| **实体映射** | **刷新实体** | **初始同步** | **用于初始同步的主服务器** | **运行先决条件** | **先决条件初始同步** |
| --- | --- | --- | --- | --- | --- |
| **所有公司的项目资源角色 (bookableresourcecategories)** | No | 是 | Common Data Service | No | 不适用 |
| **法人 (cdm\_companies)** | No | 是 | Finance and Operations 应用 | No | 不适用 |
| **分类帐 (msdyn_ledgers)** | No | 是 | Finance and Operations 应用 | 是 | 是，Finance and Operations 应用 |
| **Project Operations 集成实际值 (msdyn\_actuals)** | No | No | 不适用 | 是 | No |
| **项目合同子项 (salesorderdetails)** | No | No | 不适用 | No | No |
| **项目交易关系的集成实体 (msdyn\_transactionconnections)** | No | No | 不适用 | No | 不适用 |
| **Project Operations 集成合同子项里程碑 (msdyn\_contractlinesscheduleofvalues)** | No | No | 不适用 | No | 不适用 |
| **用于支出预估的 Project Operations 集成实体 (msdyn\_estimateslines)** | No | No | 不适用 | No | 不适用 |
| **Project Operations 集成项目支出类别导出实体 (msdyn\_expensecategories)** | No | No | 不适用 | No | 不适用 |
| **Project Operations 集成项目支出导出实体 (msdyn\_expenses)** | 是 | No | 不适用 | No | 不适用 |
| **用于工时预估的 Project Operations 集成实体 (msdyn\_resourceassignments)** | 是 | No | 不适用 | No | 不适用 |


4. 若要刷新实体，选择映射名称，然后选择 **刷新实体**。 


![刷新映射](./media/20RefreshMapping.png)

5. 刷新完成后，运行映射。 在启用下一个映射之前，验证表中的映射是否处于 **正在运行** 状态。 运行具有大量先决条件的映射可能需要一些时间。

要运行具有先决条件的映射，请启用 **显示相关实体映射** 切换。 如果表中指示 **先决条件初始同步** 为 **否**，请在运行前确认 **初始同步** 标志在所有先决条件映射中均为 **关闭**。

![运行映射](./media/21RunMap.png)

6. 验证所有项目相关映射是否处于运行状态。

![所有映射正在运行](./media/22AllMapsRunning.png)


## <a name="apply-configuration-data-in-cds-for-project-operations-optional"></a>在 Project Operations 的 CDS 中应用配置数据（可选）

如果已将演示数据应用到 Finance 环境，请参阅[在 Project Operations 的 Common Data Service 中设置和应用配置数据](resource-apply-pro-setup-config-data.md)将演示数据应用到 CDS 环境。


您的 Project Operations 环境现在已经完成了设置和配置。 


[!INCLUDE[footer-include](../includes/footer-banner.md)]