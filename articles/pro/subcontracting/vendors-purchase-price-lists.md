---
title: Project Operations 中的供应商和采购价目表管理
description: 本文提供的信息将帮助您为合同分包创建和维护供应商数据和采购价目表。
author: rumant
ms.date: 08/02/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 3cd883fed8a59f1c54c39e2d051b9748833ba692
ms.sourcegitcommit: b2224d1f3c0bd4925d647e6ca3960db81a209521
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/11/2022
ms.locfileid: "9261876"
---
# <a name="vendor-and-purchase-price-list-management-in-project-operations"></a>Project Operations 中的供应商和采购价目表管理


_**适用于：** 精简部署 - 估价交易开票_

## <a name="vendors-in-project-operations"></a>Project Operations 中的供应商

在 Microsoft Dynamics 365 Project Operations 中，供应商客户具有 **供应商** 或 **提供商关系** 类型。 您只能选择在分包合同中将这些关系类型之一作为供应商的客户记录。

您可以将一个或多个购买价目表与供应商记录相关联。 但是，与供应商记录关联的每个购买价目表都应具有明显的日期效果。 Project Operations 不支持采购价目表的重叠日期有效性。

默认情况下，供应商记录上的下列字段和概念用于为供应商创建的任何分包合同：

- 付款方式
- 帐单邮寄地址联系人
- 主要联系人

    > [!NOTE]
    > 默认情况下，供应商的主要联系人用作分包商的供应商客户经理。

- 货币
- 当前采购价目表

## <a name="purchase-price-lists-in-project-operations"></a>Project Operations 中的采购价目表

**上下文** 字段设置为 **购买** 的价目表被视为购买价目表。 可以定义购买价目表以表示时间、支出和材料的购买费率目录。 购买价目表类似于 Project Operations 中的成本和销售价目表。 以下概念适用于购买价目表，其适用方式与适用于成本和销售价目表的方式相同：

- **日期有效性** – 购买价目表具有日期有效性。 日期有效性由每个价目表上的开始日期和结束日期字段来表示。 开始日期和结束日期之间的时间是日期有效期。
- **货币** - 价目表标题上的货币用作表示目录中人工、支出类别和产品的购买价格的货币。
- **默认时间单位** - 默认时间单位表示购买的人工价格。 价目表上的时间单位字段仅用于提供默认值。 该值可在单个角色价格行上更改。

购买价目表可作为称为项目价目表的关联项附加到供应商记录中。 这些价目表用于在分包合同子项上输入违约价格。 默认情况下，当多个购买价目表附加到供应商记录后，最近的价目表用于为供应商创建的分包合同。 只有 **上下文** 字段设置为 **购买** 的价目表才能附加到供应商记录。

### <a name="subcontract-specific-purchase-price-lists"></a>分包特定的采购价目表

购买价目表也可作为称为项目价目表的关联项附加到分包合同。 这些价目表用于在分包合同子项上输入违约价格。 默认情况下，当多个购买价目表附加到分包合同后，每个价目表都必须具有明显的日期效果。 Project Operations 不支持具有重叠日期有效性的采购价目表。 只有 **上下文** 字段设置为 **购买** 的价目表才能附加到分包合同。

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
