---
title: 项目估计值和实际值集成
description: 本主题提供有关项目估计值和实际值的 Project Operations 双重写入集成的信息。
author: sigitac
ms.date: 4/26/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: c558ab1eb5070f6d1a2db06b630e8807cc67819f9bdd57c15ec346f484e04fe9
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/06/2021
ms.locfileid: "7006280"
---
# <a name="project-estimates-and-actuals-integration"></a>项目估计值和实际值集成

_**适用于：** 面向资源/非库存场景的 Project Operations_

本主题提供有关项目估计值和实际值的 Project Operations 双重写入集成的信息。

## <a name="project-estimates"></a>项目估算

在 Microsoft Dataverse 中创建和维护项目人力、支出和材料估算，并出于会计目的将其同步到 Finance and Operations 应用。 不支持通过 Finance and Operations 应用创建、更新和删除操作。

创建估算需要对项目进行有效的会计配置。 与合同子项关联的项目必须具有在项目成本和收入配置文件规则中定义的有效项目成本和收入配置文件。 有关详细信息，请参阅[配置收费项目会计](../project-accounting/configure-accounting-billable-projects.md#configure-project-cost-and-revenue-profile-rules)。

## <a name="labor-estimates"></a>人力估算

人力估算由项目经理或资源经理创建，他们同时负责为项目任务分配通用或指定资源。 可以在 Dataverse 中 **项目详细信息** 页上的 **资源分配** 选项卡上查看资源分配记录。 Dataverse 中的资源分配记录使用 **用于工时估算的 Project Operations 集成实体 (msdyn\_resourceassignments)** 在 Finance and Operations 应用中创建工时预测记录。

   ![人力估算集成。](./Media/DW4LaborEstimates.png)

双重写入将资源分配记录同步到暂存表 (**ProjCDSEstimateHoursImport**)，然后使用业务逻辑创建和更新工时预测记录 (**ProjForecastEmpl**)。

项目会计通过转到 **项目管理和会计** > **所有项目** > **计划** > **工时预测** 查看在 Finance and Operations 应用中创建的预测时间记录。

## <a name="expense-estimates"></a>费用估算

支出估算由项目经理在 Dataverse 中 **项目详细信息** 页上的 **支出估算** 选项卡上创建。 支出估算记录存储在 Dataverse 中的 **估算明细** 实体中。 这些估算记录的交易类为 **支出**，记录将使用 **支出估算的 Project Operations 集成实体 (msdyn\_estimatelines)** 同步到 Finance and Operations 应用中的支出预测记录。

   ![支出估算集成。](./Media/DW4ExpenseEstimates.png)

双重写入将支出估算记录同步到暂存表 **(ProjCDSEstimateExpenseImport)**，然后使用业务逻辑创建和更新支出预测记录 (**ProjForecastCost**)。 估算明细分别存储销售估算和成本估算记录。 Finance and Operations 应用中的业务逻辑使用暂存表中的这一详细信息填充单个支出预测记录。

项目会计可以转到 **项目管理和会计** > **所有项目** > **计划** > **支出预测**，在 Finance and Operations 应用中查看支出预测记录。

## <a name="material-estimates"></a>材料估算

材料估算由项目经理在 Dataverse 中 **项目详细信息** 页上的 **材料估算** 选项卡上创建。 材料估算记录存储在 Dataverse 中的 **估算明细** 实体中。 这些估算记录的交易类为 **材料**，记录将使用 **材料估算的 Project Operations 集成表 (msdyn\_estimatelines)** 同步到 Finance and Operations 应用中的物料预测记录。

   ![材料估算集成。](./Media/DW4MaterialEstimates.png)

双重写入将材料估算记录同步到暂存表 **ProjForecastSalesImpor**，然后使用业务逻辑创建和更新物料预测记录 (**ForecastSales**)。 估算明细分别存储销售估算和成本估算记录。 Finance and Operations 应用中的业务逻辑使用暂存表中的这一详细信息填充单个物料预测记录。

项目会计可以转到 **项目管理和会计** > **所有项目** > **计划** > **物料预测**，在 Finance and Operations 应用中查看物料预测记录。

## <a name="project-actuals"></a>项目实际值

项目实际值在 Dataverse 中根据时间、支出、材料和记帐活动创建。 这些交易的所有操作属性（包括数量、成本费、售价和项目）都在此 Dataverse 实体中捕获。 有关详细信息，请参阅[实际值](../actuals/actuals-overview.md)。 实际值记录将使用双重写入表映射 **Project Operations 集成实际值 (msdyn\_actuals)** 同步到 Finance and Operations 应用，以进行下游会计工作。

   ![实际值集成。](./Media/DW4Actuals.png)

**Project Operations 集成实际值** 表映射将同步 Dataverse 中 **实际值** 实体中的所有记录，属性 **跳过同步(仅供内部使用)** 设置为 **False**。 此属性值在创建记录时在 Dataverse 中自动设置。 将此属性设置为 **True** 的示例有：

  - 内部公司交易的项目成本实际值。 有关详细信息，请参阅[创建内部公司交易](../project-accounting/create-intercompany-transactions.md)。 跳过这些记录是因为过帐内部公司供应商发票时，系统会在 Finance and Operations 应用中重新创建项目成本实际值。
  - 确认估价发票时创建的负未记帐销售记录。 跳过这些记录是因为 Finance and Operations 应用中的项目子分类帐不会在开票时冲销未记帐销售记录，但会将状态更改为完全开票。

双重写入表映射将实际值记录同步到暂存表 **ProjCDSActualsImport**。 在创建 Project Operations 集成日记帐行和项目发票方案明细时，这些记录由定期流程 **从暂存表导入** 处理。 有关详细信息，请参阅 [Project Operations 中的集成日记帐](../project-accounting/project-operations-integration-journal.md)。

Dataverse 还会在 **交易连接** 实体中捕获项目实际值交易之间的链接。 有关详细信息，请参阅[将实际值链接到原始记录](../actuals/linkingactuals.md)。 实际值交易之间的链接还将使用双重写入表映射 **项目交易关系的集成实体 (msdyn\_transactionconnections)** 同步到 Finance and Operations 应用。 在创建 Project Operations 集成日记帐行和项目发票方案明细时，这些记录由定期流程 **从暂存表导入** 使用。

过帐 Project Operations 集成日记帐和项目发票方案将触发暂存表 **ProjCDSActualsImport** 中相应记录的更新。 系统将捕获并记录实际值交易的以下会计属性：

- 会计币种金额
- 汇率
- 凭证号
- 销售税金额

**Project Operations 集成实际值** 表映射使用此信息更新 Dataverse 中的相应实际值记录。
