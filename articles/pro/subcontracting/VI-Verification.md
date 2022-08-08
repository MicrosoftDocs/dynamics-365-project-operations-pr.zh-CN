---
title: 使用已批准的实际值验证供应商发票
description: 本文说明 Microsoft Dynamics 365 Project Operations 如何让项目经理使用承包商在执行工作和记录时间时批准的实际值验证供应商发票，以及项目团队成员使用的支出和材料。
author: rumant
ms.date: 03/30/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 7bf48dd17063daece5df3ce44c0375eec3dc3cae
ms.sourcegitcommit: 49c2a668b8d7bf0acb9e9b0bb44687e6d3dcaa8c
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 07/28/2022
ms.locfileid: "9204163"
---
# <a name="verification-of-vendor-invoices-with-approved-actuals"></a>使用已批准的实际值验证供应商发票

[!include [banner](../../includes/dataverse-preview.md)]

_**适用于：** 精简部署 - 估价交易开票_

Microsoft Dynamics 365 Project Operations 允许项目经理通过以下方式验证供应商发票明细：

- 在供应商发票明细上使用 **验证状态** 字段。
- 如果供应商发票明细引用分包合同子项，则将分包商活动的实际成本链接到这些供应商发票明细。 链接通过将实际成本与供应商发票明细进行匹配来创建。

    > [!NOTE]
    > 虽然可以为不引用分包合同的供应商发票明细跟踪验证状态，但无法将实际成本链接到这些供应商发票明细。

## <a name="verification-status"></a>验证状态

供应商发票明细上的 **验证状态** 字段指示验证的状态。 支持以下状态：

1. 未开始
2. 正在进行
3. 完成

可以编辑验证状态为 **未开始** 的供应商发票明细。

验证状态为 **正在进行** 的供应商发票明细无法再编辑。 对于引用分包合同的供应商发票明细，只要第一个实际成本与供应商发票明细匹配，验证状态就会自动设置为 **正在进行**。

验证状态为 **完成** 的供应商发票明细无法再编辑。 当供应商发票上的所有明细都具有此验证状态时，可以确认供应商发票。

## <a name="match-cost-actuals-to-vendor-invoice-lines"></a>将实际成本与供应商发票明细进行匹配

匹配实际成本可以帮助执行供应商发票明细的验证过程。 要将实际成本与供应商发票明细进行匹配，请执行以下步骤。

1. 打开供应商发票明细，选择 **与实际成本不匹配** 选项卡。网格将显示引用与供应商发票明细相同的分包合同子项的实际成本列表。
2. 选择一个或多个实际成本，然后选择网格上方工具栏上的 **匹配**。 系统将验证所选实际成本是否匹配。 通过验证后，实际成本将链接到供应商发票明细。

### <a name="validation-criteria-that-are-used-to-link-cost-actuals-to-vendor-invoice-lines"></a>用于将实际成本链接到供应商发票明细的验证条件

在匹配过程中，只有同时满足以下两个条件，才能在实际成本和供应商发票明细之间建立链接：

- 每个选定的实际成本的 **调整状态** 字段必须为空。 换言之，在撤消、审批取消或更正日记帐流程期间，实际成本不能被其他实际成本替换。
- 以下字段的值在供应商发票明细和所选实际成本之间匹配。 如果供应商发票明细上未设置任何字段，则不会考虑对其进行匹配。

    - 项目合同
    - 项目合同子项
    - 交易分类
    - 集成
    - 任务
    - 资源类别
    - 交易类别
    - 产品
    - 分包合同子项
    - 可预订资源

## <a name="unmatch-cost-actuals-from-a-vendor-invoice-line"></a>取消实际成本与供应商发票明细的匹配

取消实际成本的匹配通过删除先前建立的链接还可以帮助执行验证供应商发票的过程。 实际成本只能取消与验证状态为 **正在进行** 的供应商发票明细的匹配。 要取消实际成本与供应商发票明细的匹配，请执行以下步骤。

1. 打开供应商发票明细，选择 **与实际成本匹配** 选项卡。网格将显示引用供应商发票明细的实际成本列表。
2. 选择一个或多个实际成本，然后选择网格上方工具栏上的 **取消匹配**。

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
