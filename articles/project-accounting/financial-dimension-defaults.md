---
title: 财务维度默认值
description: 此主题提供有关如何设置财务维度默认值的信息。
author: sigitac
manager: Annbe
ms.date: 10/26/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: aa6771ba5346fd4133b82c3e670badfa7655299f
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/28/2020
ms.locfileid: "4131872"
---
# <a name="financial-dimension-defaults"></a>财务维度默认值

_**适用于：** 面向资源/非库存场景的 Project Operations_

Dynamics 365 Project Operations 使用 Dynamics 365 Finance 中的[财务维度](https://docs.microsoft.com/dynamics365/finance/general-ledger/financial-dimensions)框架提供有关项目子分类帐和总帐交易的其他见解。

默认财务维度可以在客户、项目资金来源、里程碑、项目合同子项或项目上设置。

## <a name="define-default-financial-dimensions-for-a-customer"></a>定义客户的默认财务维度

客户维度默认值在 Finance 中指定。 完成以下步骤设置维度默认值。

1. 转到 **应收帐款** > **客户** > **所有客户**。
2. 在 **客户** 页上的 **财务维度** 选项卡上，为特定客户设置财务维度值。

## <a name="define-default-financial-dimensions-for-project-contracts"></a>定义项目合同的默认财务维度

项目合同在 Common Data Service (CDS) 中创建和维护。 项目合同的会计属性在 Finance 中的 **项目管理和会计** 模块中设置。

### <a name="set-financial-dimensions-for-a-project-funding-source"></a>为项目资金来源设置财务维度

1. 转到 **项目管理和会计** > **项目** > **项目合同**。
2. 选择要更新的记录，然后在 **项目合同** 选项卡上，选择 **显示默认会计**。
3. 展开 **相关信息**，选择 **资金来源** 选项卡。
4. 设置财务维度默认值。 请注意，财务维度默认来自客户帐户。

### <a name="set-financial-dimensions-for-a-project-contract-line"></a>为项目合同子项设置财务维度

1. 转到 **项目管理和会计** > **项目** > **项目合同**。
2. 选择要更新的记录，然后在 **项目合同** 选项卡上，选择 **显示默认会计**。
3. 展开 **相关信息**，选择 **合同子项** 选项卡。
4. 设置财务维度默认值。 财务维度默认值适用，但只能用于固定价格（里程碑）合同子项。

这些默认值用于相关的项目分期付款交易和发票明细。

## <a name="define-default-financial-dimensions-for-projects"></a>定义项目的默认财务维度

项目在 CDS 中创建和维护。 项目的会计属性在 Finance 中的 **项目管理和会计** 模块中设置。

1. 转到 **项目管理和会计** > **项目** > **所有项目**。
2. 选择要更新的记录，然后在 **项目** 选项卡上，选择 **显示默认会计**。
3. 展开 **相关信息**，选择 **设置** 选项卡。
4. 设置财务维度默认值。 请注意，财务维度默认来自客户帐户。 如果项目与具有多个项目合同客户的合同子项关联，主要客户将用于确定默认财务维度。

项目默认财务维度用于设置 **Project Operations 集成日记帐** 和相关项目发票明细上的时间、支出和费用交易的日记帐行默认值。
