---
title: Project Operations 双重写入映射版本
description: 本主题提供 Dynamics 365 Project Operations 所需的双重写入映射的列表。
author: sigitac
ms.date: 04/22/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 385893e8ecdb29f4dc411c233b9ae19bb2448dfd
ms.sourcegitcommit: 9916f536a71b6a0078297402564ac79308ec6890
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/18/2022
ms.locfileid: "8612739"
---
# <a name="project-operations-dual-write-map-versions"></a>Project Operations 双重写入映射版本

_**适用于：** 面向资源/非库存场景的 Project Operations_

在资源/非库存场景中使用 Dynamics 365 Project Operations 需要在环境中运行一组双重写入映射。 

## <a name="prerequisite-maps-dual-write-orchestration-solution"></a>必备映射：双重写入业务流程解决方案

以下映射是 Project Operations 解决方案的必备先决条件。 请确保在您的环境中运行下表中列出的映射以及所有相关的表映射。

| 表映射 | 初始同步 |
| --- | --- |
| 分类帐 (msdyn_ledgers) | 需要对表映射和所有先决条件进行初始同步。 初始同步的主控方是财务和运营应用。 |
| 法人 (cdm_companies) | 不需要。 使用双重写入链接环境时，系统会自动填充此实体。 |
| 客户 V3 (accounts) | 预配时不需要。 |
| 供应商 V2 (msdyn_vendors) | 预配时不需要。 |

1. 从映射列表中，选择具有所有先决条件的分类帐 **(msdyn\_ledgers)** 映射，然后选中 **初始同步** 复选框。 在 **初始同步的主控方** 字段中，为分类帐映射和所有先决条件映射选择 **财务和运营应用**。 选择 **运行**。

![分类帐映射同步。](media/DW6.png)

2. 对上表中列出的所有其余表映射执行相同的步骤。 运行这些映射时，不要选中 **初始同步** 复选框。

## <a name="project-operations-dual-write-maps"></a>Project Operations 双重写入映射

以下映射是 Project Operations 解决方案所必需的。 从 Project Operations 的 2021 年 5 月更新版本 4.10.0.186 开始列出了双重写入映射版本。

| 实体映射 | 最新版本 | 初始同步 | 所需的 Dynamics 365 Finance 版本 |
| --- | --- | --- | --- |
| 项目交易关系的集成实体 (msdyn\_transactionconnections) | 1.0.0.0 | 预配时不需要。 ||
| 项目合同抬头 (sales orders) | 1.0.0.1 | 预配时不需要。 ||
| 项目合同子项 (salesorderdetails) | 1.0.0.0 | 预配时不需要。 ||
| 项目资金来源 (msdyn_projectcontractsplitbillingrules) | 1.0.0.2 | 预配时不需要。 ||
| 用于材料估算的 Project Operations 集成表 (msdyn\_estimatelines) | 1.0.0.0 | 预配时不需要。 ||
| 项目发票方案 V2 (invoices) | 1.0.0.3 | 预配时不需要。 ||
| Project Operations 集成实际值 (msdyn_actuals) | 1.0.0.14 | 预配时不需要。 ||
| Project Operations 集成合同子项里程碑 (msdyn_contractlinescheduleofvalues) | 1.0.0.4 | 预配时不需要。 ||
| 用于支出估算的 Project Operations 集成实体 (msdyn_estimatelines) | 1.0.0.2 | 预配时不需要。 ||
| 用于工时估算的 Project Operations 集成实体 (msdyn_resourceassignments) | 1.0.0.5 | 预配时不需要。 ||
| Project Operations 集成项目支出类别导出实体 (msdyn_expensecategories) | 1.0.0.1 | 预配时不需要。 ||
| Project Operations 集成项目支出导出实体 (msdyn_expenses) | 1.0.0.3 | 预配时不需要。 ||
| Project Operations 集成项目供应商发票导出实体 (msdyn_projectvendorinvoices) | 1.0.0.0 | 预配时不需要。 ||
| Project Operations 集成项目供应商发票明细导出实体 (msdyn_projectvendorinvoicelines) | 1.0.0.4 | 预配时不需要。 | 10.0.26 或更高版本 |
| 所有公司的项目资源角色 (bookableresourcecategories) | 1.0.0.1 | 需要对表映射进行初始同步，以同步预配期间在 Dynamics 365 Dataverse 环境中填充的项目经理和团队成员资源角色。 Dataverse 是初始同步的主要来源。 ||
| 项目任务 (msdyn_projecttasks) | 1.0.0.4 | 预配时不需要。 ||
| 项目交易类别 (msdyn_transactioncategories) | 1.0.0.0 | 预配时不需要。 ||
| 项目 V2 (msdyn_projects) | 1.0.0.2 | 预配时不需要。 ||

完成以下步骤运行列出的映射。

1. 为 **所有公司 (bookableresourcecategories)** 表映射启用项目资源角色，因为此映射需要初始同步。在 **初始同步的主体** 字段中，选择 **Common data service**。 

 ![资源角色表映射同步。](media/6ResourceInitialSync.jpg)

 等待映射的状态进入 **正在运行**，进行下一步。

2. 选择其余所有必需映射。 您可以在右上角的搜索中使用 **项目** 关键字在双重写入映射列表中对它们进行筛选。 您可以多选所有映射，然后运行。 有关详细信息，请参阅[管理多个表映射](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/multiple-entity-maps)。 确保另外还启用并运行了相关的实体映射。

### <a name="project-operations-dual-write-map-versions"></a>Project Operations 双重写入映射版本

始终在您的环境中运行最新版本的映射。 如果存在以下任一情况，某些功能可能无法正常工作：

- 未激活映射。
- 未激活映射的最新版本。 
- 未激活相关表映射。

您可以在 **双重写入** 页的 **版本** 列中查看映射的活动版本。 您可以通过选择 **表映射版本**，选择最新版本，然后保存所选版本来激活映射的新版本。 如果您自定义了现成的表映射，将需要重新应用更改。 有关详细信息，请参阅[应用程序生命周期管理](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management)。
