---
title: 创建供应商发票
description: 本文介绍供应商发票的概念，并说明如何在 Microsoft Dynamics 365 Project Operations 中进行创建。
author: suvaidya
ms.date: 9/12/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: suvaidya
ms.openlocfilehash: 7f6c1ec46f23b6823734b28755b80ced4e3f9325
ms.sourcegitcommit: 60a34a00e2237b377c6f777612cebcd6380b05e1
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/13/2022
ms.locfileid: "9475405"
---
# <a name="create-vendor-invoices"></a>创建供应商发票

_**适用于：** 面向资源/非库存场景的 Project Operations_

要使用本文所述的功能，您必须在 **功能管理** 工作区启用 **使用 Project Operations 为基于资源的场景启用分包合同实际值处理** 功能。

Microsoft Dynamics 365 Project Operations 中的供应商开票可用于记录供应商完成的项目中交付服务和/或材料的成本。

当服务和/或材料分包给供应商时，分包合同代表与该供应商的合同协议。 当供应商交付服务，或收到材料并将其用于项目任务时，成本将记录在项目中。 然后，供应商将定期发送发票。 这些发票将经过验证并与项目中记录的成本进行匹配。 验证过程完成后，确认供应商发票并发布以进行付款。

## <a name="scenarios-for-use"></a>使用场景

Project Operations 中的供应商发票可用于支持两个不同的场景：

- 客户使用完整的分包体验。
- 客户不使用完整的分包体验，但希望在 Project Operations 中获得统一的项目成本视图。

### <a name="customers-use-the-full-subcontracting-experiences"></a>客户使用完整的分包体验

供应商发票体验提供了一种方法来验证引用分包组件的时间条目、材料使用和支出条目，并将它们与供应商发票明细进行匹配。 此过程可用于验证供应商发票明细的准确性。 验证过程完成并确认供应商发票后，系统将冲销通过批准的时间、支出和材料使用日志记录的实际值，然后使用供应商发票明细创建新的实际成本。

### <a name="customers-dont-use-the-full-subcontracting-experiences-but-want-to-have-a-unified-view-of-costs-on-projects-in-project-operations"></a>客户不使用完整的分包体验，但希望在 Project Operations 中获得统一的项目成本视图

如果您在第三方系统中跟踪分包合同流程，您可以通过创建不引用分包合同的供应商发票将成本从该第三方系统记录到 Project Operations 中。 通过这种方式，您的项目经理可以有一个统一的给定项目上所有成本的单一视图。

## <a name="create-vendor-invoices-in-project-operations"></a>在 Project Operations 中创建供应商发票

供应商发票在 Dynamics 365 Finance 中使用 **应付帐款** 模块创建。 您无法直接在 Dataverse 中创建供应商发票。

### <a name="set-up-vendor-invoice-verification"></a>设置供应商发票验证

如果供应商发票用于 Dataverse 中的分包合同，您必须启用 **Manual verification by PM is required** 参数。 此选项的设置确定是否应在 Dataverse 中自动确认供应商发票，或者是否需要手动确认。 每个项目供应商发票的标题会包含一个相同名称的选项。 默认情况下，所有项目供应商发票标题上的选项都设置为您在此处设置的值。 不过，您可以根据需要更新各个供应商发票标题上的值。

如果此选项设置为 **是**，在 Finance 中创建并同步到 Dataverse 的供应商发票状态将为 **草稿**。 然后，发票必须由项目经理验证和确认，然后才能处理并过帐到 Finance 中的特定项目和分类帐科目。

如果此选项设置为 **否**，将自动确认供应商发票。 无需进一步操作。

要设置供应商发票验证，请按照以下步骤操作。

1. 在 Finance 中，转到 **项目管理和会计** \> **设置** \> **项目管理和会计参数**。
1. 如果公司政策要求验证分包商供应商发票，在 **财务** 选项卡上，将 **需要 PM 手动验证** 选项设置为 **是**。 如果在 Dataverse 中不需要项目经理进行验证，保留此选项为 **否**。 默认情况下，此设置将在 **待定供应商发票** 页面使用。

> [!NOTE]
> 只有将 **需要 PM 手动验证** 选项设置为 **是** 时，才能正确处理为 Dataverse 中的分包合同创建的供应商发票。 仅当此选项设置为 **是** 时，项目经理才能手动将分包商创建的时间、材料和支出费用实际值与供应商发票明细进行匹配。

### <a name="set-up-a-procurement-integration-account-for-vendor-invoices"></a>为供应商发票设置采购集成帐户

在 Project Operations 的 Finance - 集成环境（非库存）中过帐供应商发票时，财务数据将被过帐到采购集成帐户。 系统将在 Dataverse 中为已过帐发票生成实际值。 这些实际值通过使用项目集成日记帐在 Finance 中过帐。 项目集成日记帐的过帐将过帐实际成本并冲销采购集成帐户。

要为供应商发票设置采购集成帐户，请执行以下步骤。

1. 在 Finance 中，转到 **项目管理和会计** \> **设置** \> **项目管理和会计参数**。
1. 在 **Dynamics 365 customer engagement 上的 Project operations** 选项卡上，选择 **材料** \> **采购集成帐户**。

### <a name="create-and-post-subcontract-vendor-invoices"></a>创建和过帐分包供应商发票

当应付帐款职员收到分包商的发票时，新发票将在 Finance 中创建。

1. 在 Finance 中，转到 **应付帐款** \> **发票** \> **待定供应商发票**。
1. 在 **操作窗格** 上，选择 **新建** 创建供应商发票。
1. 在发票标题的 **发票客户** 字段中，选择 **分包商**。
1. 选择发票日期。
1. 在 **标题** 选项卡上，将 **需要 PM 手动验证** 选项设置为 **是**。 此选项的默认设置来自 **项目管理和会计参数** 页面。 但可以在供应商发票级别进行更改。
1. 在 **发票明细** 快速选项卡上，选择 **添加行** 创建供应商发票明细。
1. 选择为分包合同子项创建的采购类别，并输入单价、度量单位和数量。
1. 在供应商发票明细部分的 **项目** 选项卡上，选择分包商共享分包合同发票的项目。
1. 选择项目类别。 可以是 **项目**、**支出**、**材料** 或 **时数** 类型的任何一个。
1. 仅当所选项目类别为 **时数** 类型时才选择角色。
1. 选择 **过帐** 过帐供应商发票。

或者，您可以转到 **应付帐款** \> **发票** \> **打开供应商发票** 并选择 **新建** 来创建供应商发票。

当供应商发票过帐时，它将在 Dataverse 中可供项目经理验证和处理。

## <a name="vendor-invoice-processing-in-dataverse"></a>Dataverse 中的供应商发票处理

在 Dataverse 中创建的供应商发票中，一些字段值来自 Finance 中记录的供应商发票。 其他值是来自分包合同的默认值。

以下字段和相关记录将会从分包合同复制到供应商发票的标题中：

- 货币
- 合同签订部门
- 付款方式

在供应商发票明细上，Project Operations 使用以下字段值输入默认分包合同和分包合同子项引用：

- 交易分类
- 角色
- 交易类别
- 产品字段
- 集成
- 任务

> [!NOTE]
> Project Operations 中不支持固定价格分包合同子项。

[!INCLUDE[footer-include](../includes/footer-banner.md)]
