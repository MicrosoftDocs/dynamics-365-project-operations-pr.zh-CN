---
title: 在草稿项目发票方案上更正会计
description: 本主题说明了如何在草稿发票方案上调整与会计相关的信息。
author: sigitac
ms.date: 06/07/2021
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 153a239d4b88906909ee0bfae8a18cabebc3766399290d83bb79f5d6375a942c
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/06/2021
ms.locfileid: "6999305"
---
# <a name="correct-the-accounting-on-draft-project-invoice-proposals"></a>在草稿项目发票方案上更正会计

_**适用于：** 面向资源/非库存场景的 Project Operations_

项目发票的 *操作详细信息* 由项目经理针对估价发票进行维护。 这些详细信息包括有关必须开具发票的小时数、支出、材料或里程碑、汇率以及预付款和保留款应用的决策。 在确认原始估价发票后，您可以通过创建并确认[更正估价发票](../proforma-invoicing/corrective-invoices.md)调整操作详细信息。

项目发票的 *会计详细信息* 在面向客户的发票文档中进行维护。 这些详细信息包括应用于发票的销售税款计算和财务维度。 本主题提供有关如何在草稿项目发票方案上调整这些会计详细信息的详细信息。

## <a name="adjust-sales-tax"></a>调整销售税

可以直接在发票方案文档上调整默认的记帐销售税组和物料销售税组。 若要调整这些组，请选择 **编辑**，然后在每个项目发票方案行上，在 **销售税组** 或 **物料销售税组** 字段中输入新值。

## <a name="adjust-financial-dimensions"></a>调整财务维度

不能直接在项目发票方案行上编辑财务维度。 而是按照以下步骤在项目发票方案上调整财务维度。

1. 在项目发票方案上，选择 **全部删除** 以删除项目发票方案行。

    > [!NOTE]
    > **全部删除** 按钮仅在系统管理员在 **功能管理** 工作区中启用 **在针对基于资源/非库存的方案使用 Project Operations 时删除发票方案行** 功能后才可用。

2. 调整财务维度：

    - **记帐交易（记帐里程碑）：** 转到 **所有项目** \> **管理** \> **记帐交易**，并选择需要调整的里程碑。 然后，在 **财务维度** 选项卡上，根据需要更新值。
    - **时间、支出和材料交易：** 在 **过帐的项目交易** 页面上，选择 **调整会计** 以更新财务维度。

3. 调整完财务维度值后，转到 **项目管理和会计** \> **定期** \> **Project Operations 集成**，然后选择 **从暂存表中导入** 以运行定期流程。 该流程使用更新的财务维度值来重新创建项目发票方案行。 然后，在过帐项目发票时，将更新的值用于项目分类帐和总帐。
