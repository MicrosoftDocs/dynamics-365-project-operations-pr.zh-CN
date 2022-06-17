---
title: 供应商开票 - 概念和创建
description: 本文介绍供应商发票的概念、使用场景以及如何在 Microsoft Dynamics 365 Project Operations 中创建供应商发票。
author: rumant
ms.date: 03/25/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 38f0760697522b7a5e561cec7d38dfd5c3eaf9fc
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8911447"
---
# <a name="vendor-invoicing---concept-and-creation"></a>供应商开票 - 概念和创建

[!include [banner](../../includes/dataverse-preview.md)]

_**适用于：** 精简部署 - 估价交易开票_

Microsoft Dynamics 365 Project Operations 中的供应商开票可用于记录供应商在项目中交付服务和/或材料的成本。

当服务和/或材料分包给供应商时，分包合同代表与该供应商的合同协议。 当供应商交付服务，或收到材料并将其用于项目任务时，成本将记录在项目中。 供应商会定期发送经过验证并与项目中记录的成本相匹配的发票。 验证过程完成后，确认供应商发票并发布以进行付款。

## <a name="scenarios-for-use"></a>使用场景

Project Operations 中的供应商发票可用于支持两个不同的场景。

### <a name="customers-use-the-full-subcontracting-experiences"></a>客户使用完整的分包体验

供应商发票体验提供了一种方法来验证和匹配在供应商发票明细中引用分包组件的时间条目、材料使用和支出条目。 此过程可用于验证供应商发票明细的准确性。 验证过程完成并确认供应商发票后，应用程序将冲销通过批准的时间、支出和材料使用日志记录的实际值，并使用供应商发票明细创建新的实际成本。

### <a name="customers-dont-use-the-full-subcontracting-experiences-but-want-to-have-a-unified-view-of-costs-on-projects-in-project-operations"></a>客户不使用完整的分包体验，但希望在 Project Operations 中获得统一的项目成本视图

如果您在第三方系统中跟踪分包合同流程，您可以通过创建不引用分包合同的供应商发票将成本从该第三方系统记录到 Project Operations 中。 通过这种方式，您的项目经理可以有一个统一的给定项目上所有成本的单一视图。

## <a name="creation-of-vendor-invoices-in-project-operations"></a>在 Project Operations 中创建供应商发票

可以通过两种方法创建供应商发票：

- 从供应商发票列表页或单个供应商发票的详细信息页面
- 从分包合同列表页或单个分包合同的详细信息页面

### <a name="creation-from-the-vendor-invoice-list-page-or-details-page"></a>从供应商发票列表页或详细信息页面创建

1. 转到 **采购** \> **供应商发票**。
2. 在供应商发票列表页或单个供应商发票的详细信息页面上，选择 **新建** 创建新的供应商发票。

以这种方式创建的供应商发票还可以引用分包合同。

### <a name="creation-from-the-subcontract-list-page-or-details-page"></a>从分包合同列表页或详细信息页面创建

1. 转到 **采购** \> **分包合同**。
2. 选择一个或多个分包合同。
3. 在分包合同列表页或单个分包合同的详细信息页面上，选择 **创建供应商发票** 创建新的供应商发票。

将为您选择的每个分包合同创建一个处于 **草稿** 状态的新供应商发票。

您以这种方式创建的供应商发票会始终在供应商发票标题上引用分包合同。 具有时间和材料记帐方法的分包合同中的每个子项都会在供应商发票上对应创建一个明细。 具有固定价格记帐方法的分包合同中的每个子项都会在供应商发票上为状态为 **可开票** 的每个分包合同子项里程碑对应创建一个明细。

以下字段和相关记录将会从分包合同复制到供应商发票的标题中：

- 供应商。
- 相关价目表将作为价目表复制到供应商发票。
- 货币。
- 合同签订部门。
- 付款条款。

对于时间和材料分包合同子项，以下字段和相关记录将从分包合同子项复制到供应商发票明细中：

- 分包合同和分包合同子项引用
- 交易分类
- 角色
- 交易类别
- 产品字段
- 集成
- 任务
- 可预订资源

对于固定价格分包合同子项，以下字段将从分包合同子项和分包合同子项里程碑复制到供应商发票明细中：

- 分包合同和分包合同子项引用。
- 交易类。 默认情况下，此值为 **里程碑**。
- 里程碑名称和金额将从相关的分包合同子项里程碑复制。
- 用户可以在供应商发票明细上选择项目和任务。

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
