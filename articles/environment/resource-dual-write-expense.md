---
title: 支出管理集成
description: 本主题提供有关使用双重写入在 Project Operations 中进行支出报表集成的信息。
author: sigitac
ms.date: 04/28/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 06471532d2e41bb80ebf92f0a8b93c324b3f6d3e845cea8033d85d291ea237eb
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/06/2021
ms.locfileid: "6986570"
---
# <a name="expense-management-integration"></a>支出管理集成

_**适用于：** 面向资源/非库存场景的 Project Operations_

本主题提供有关使用双重写入在 Project Operations [全部支出部署](../expense/expense-overview.md)中进行支出报表集成的信息。

## <a name="expense-categories"></a>支出类别

在全部支出部署中，将在 Finance and Operations 应用中创建和维护支出类别。 要创建新支出类别，请完成以下步骤：

1. 在 Microsoft Dataverse 中，创建 **交易** 类别。 双重写入集成会将此交易类别同步到 Finance and Operations 应用。 有关详细信息，请参阅[配置项目类别](/dynamics365/project-operations/project-accounting/configure-project-categories)和 [Project Operations 设置和配置数据集成](resource-dual-write-setup-integration.md)。 此集成的结果是，系统在 Finance and Operations 应用中创建四个共享类别记录。
2. 在 Finance 中，转到 **支出管理** > **设置** > **共享类别**，选择具有 **支出** 交易类的共享类别。 将 **可以在支出中使用** 参数设置为 **True**，并定义要使用的支出类型。
3. 使用此共享类别记录，转到 **支出管理** > **设置** > **支出类别**，然后选择 **新建**，创建新的支出类别。 保存记录后，双重写入将使用表映射 **Project Operations 集成项目支出类别导出实体 (msdyn\_expensecategories)** 将此记录同步到 Dataverse。

  ![支出类别集成。](./media/DW6ExpenseCategories.png)

Finance and Operations 应用中的支出类别特定于公司或法人。 Dataverse 中有单独的对应的法人特定记录。 当项目经理估算支出时，如果支出类别是为与他们正在处理的项目的负责公司不同的其他公司负责的项目创建的，他们则无法选择该支出类别。 

## <a name="expense-reports"></a>支出报表

支出报表在 Finance and Operations 应用中创建和审批。 有关详细信息，请参阅[在 Dynamics 365 Project Operations 中创建和处理支出报表](/learn/modules/create-process-expense-reports/)。 支出报表由项目经理批准后，将被过帐到总帐。 在 Project Operations 中，与项目相关的支出报表明细将使用特殊过帐规则过帐：

  - 与项目有关的成本（包括非抵扣税）不会立即过帐到总帐中的项目成本帐户，而是过帐到支出集成帐户。 此帐户在 **Dynamics 365 Customer engagement 上的 Project Operations** 选项卡上的 **项目管理和会计** > **设置** > **项目管理和会计参数** 中配置。
  - 双重写入使用 **Project Operations 集成项目支出导出实体 (msdyn\_expenses)** 表映射同步到 Dataverse。
  - 在支出报表过帐时，税子分类帐、供应商子分类帐和其他财务过帐将记录为适用。

  ![支出报表集成。](./media/DW6ExpenseReports.png)

将记录写入 Dataverse 中的 **支出** 实体时，系统将触发该记录的自动审批流程。 如果需要，可以转到 **高级设置** > **系统** > **系统作业**，在 Dataverse 中查看自动审批流程的状态。 审批完成后，将在 **实际值** 实体中创建支出交易类记录。

然后使用双重写入表映射 **Project Operations 集成实际值(msdyn\_actuals)** 处理与支出相关的实际值。 有关详细信息，请参阅[项目估计值和实际值](resource-dual-write-estimates-actuals.md)。

定期流程 **从暂存导入** 在 Project Operations 集成日记帐中创建与支出报表相关的日记帐行。 抵销帐户默认为支出集成帐户。 过帐集成日记帐将清除支出交易的帐户余额，并将支出金额移到项目成本帐户。 系统还将创建项目子分类帐交易记录，用于下游开票和收入确认目的。
