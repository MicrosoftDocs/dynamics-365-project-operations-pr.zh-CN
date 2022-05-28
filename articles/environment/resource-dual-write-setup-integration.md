---
title: Project Operations 设置和配置数据集成
description: 本主题提供有关设置和配置 Project Operations 双重写入映射的信息。
author: sigitac
ms.date: 4/23/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 1ffa25ff36c39010d6aee31d928c3eaa0086c3d8
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/14/2022
ms.locfileid: "8586885"
---
# <a name="project-operations-setup-and-configuration-data-integration"></a>Project Operations 设置和配置数据集成

_**适用于：** 面向资源/非库存场景的 Project Operations_

本主题提供有关用于设置和配置实体的 Project Operations 双重写入集成的信息。

## <a name="project-contracts-contract-lines-and-projects"></a>项目合同、合同子项和项目

项目合同、合同子项和项目在 Dataverse 中创建并同步到财务和运营应用，用于其他会计工作。 这些实体中的记录只能在 Dataverse 中创建和删除。 但是，可以将销售税组默认值和财务维度等会计属性添加到财务和运营应用中的这些记录中。

  ![项目合同集成概念。](./media/1ProjectContract.jpg)

销售活动潜在顾客、商机和报价单在 Dataverse 中进行跟踪，不会同步到财务和运营应用，因为没有与此活动关联的下游会计。

Dataverse 中的项目合同功能使用 **项目合同抬头（销售订单）** 表映射在财务和运营应用中创建项目合同记录。 在 Dataverse 中保存项目合同还将开始创建项目合同客户实体记录。 此记录使用 **项目资金来源 (msdyn\_projectcontractssplitbillingrules)** 表映射同步到财务和运营应用。 此映射还同步项目合同客户的添加、更新和删除。 项目合同客户之间的拆分记帐百分比仅在 Dataverse 中进行控制，不会同步到财务和运营应用。

在 Dataverse 中创建项目合同后，项目会计可以转到 **项目管理和会计** > **项目合同** > **设置** > **显示默认会计**，在财务和运营应用中更新此项目合同的会计属性。 会计可以通过在财务和运营应用中选择项目合同 ID 来查看运营项目合同属性，如请求的交货日期和合同金额，这将在 Dataverse 中打开相关的项目合同记录。

项目实体将使用 **项目 V2 (msdyn\_projects)** 表映射同步到财务和运营应用。 项目会计可以：

  - 转到 **项目管理和会计** > **所有项目**，在财务和运营应用中查看项目。 
  - 转到 **项目管理和会计** > **所有项目** > **设置** > **显示默认会计**，在财务和运营应用中更新项目的会计属性。  
  - 在财务和运营应用中选择项目 ID 来查看运营项目属性，如估算开始和结束日期，这会在 Dataverse 中打开相关项目记录。

项目通过 **项目合同子项** 实体与项目合同关联。

Dataverse 中的项目合同子项使用 **项目合同子项 (salesorderdetails)** 表映射在财务和运营应用中创建项目合同记帐规则。 记帐方法定义财务和运营应用中的项目合同记帐规则类型：

  - 使用时间和材料记帐方法的项目合同子项创建时间和材料类型的记帐规则。
  - 固定价格记帐方法合同子项创建里程碑记帐规则。

转到 **项目管理和会计** > **项目合同** > **设置** > **显示默认会计**，项目会计可以在财务和运营应用中查看项目合同子项，并查看 **合同子项** 选项卡上的详细信息。会计还可以在此选项卡上为固定价格记帐方法合同子项设置默认财务维度。

## <a name="billing-milestones"></a>记帐里程碑

使用固定价格记帐方法的项目合同子项通过记帐里程碑来开票。 使用 **Project Operations 集成合同子项里程碑 (msdyn\_contractlinescheduleofvalues)** 表映射，记帐里程碑可与财务和运营应用中的项目记帐交易同步。

  ![记帐里程碑集成。](./media/2Milestones.jpg)

会计可以转到 **项目管理和会计** > **项目合同** > **维护** > **帐户内交易** 或 **项目管理和会计** > **所有项目** > **维护** > **帐户内交易**，查看帐户内交易并调整这些交易的会计属性。

当您首次为给定项目合同子项创建记帐里程碑时，系统会自动为与此合同子项关联的项目创建固定价格收入估算项目。 固定价格收入估算项目可以转到 **项目管理和会计** > **固定价格收入估算项目** 查看。

### <a name="project-tasks"></a>项目任务

项目任务通过 **项目任务 (msdyn\_projecttasks)** 表映射同步到财务和运营应用，仅用于参考目的。 财务和运营应用不支持创建、更新和删除操作。

  ![项目任务集成。](./media/3Tasks.jpg)

## <a name="project-resources"></a>项目资源

**项目资源角色** 实体使用 **所有公司的项目资源角色 (bookableresourcecategories)** 表映射同步到财务和运营应用，仅用于参考目的。 由于 Dataverse 中的资源角色不特定于公司，系统会自动在财务和运营应用中为包含在双写入集成范围内的所有法人自动创建各自的公司特定资源角色记录。

![资源角色集成。](./media/5Resources.jpg)

Project Operations 中的项目资源在 Dataverse 中维护，不会同步到财务和运营应用。

### <a name="transaction-categories"></a>交易记录类别

交易类别在 Dataverse 中维护，并使用 **项目交易类别 (msdyn\_transactioncategories)** 表映射同步到财务和运营应用。 交易类别记录同步后，系统将自动创建四个共享类别记录。 每个记录对应于财务和运营应用中的一个交易类型，并将它们链接到交易类别记录。

![交易类别集成。](./media/4TransactionCategories.jpg)

为估计值和实际值使用交易类别需要项目会计或系统管理员在每个法人中创建相应的项目类别。 有关详细信息，请参阅[配置项目类别](../project-accounting/configure-project-categories.md)。
