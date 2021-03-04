---
title: 为什么价格在时间成本实际值中默认为零？
description: 为什么价格在时间成本实际值中默认为 0 疑难解答。
author: rumant
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 8/21/2018
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 635fe6dfb547e8b9f96ca1786912309a770e24c2
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/10/2021
ms.locfileid: "5146247"
---
# <a name="why-is-the-price-defaulting-to-zero-on-time-cost-actuals"></a>为什么价格在时间成本实际值中默认为零？

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

此常见问题适用于交易记录类设置为“时间”且交易记录类型为“成本”的实际值。 以下三项检查有助于您解答时间成本实际值中的价格为何默认为 0。
 
## <a name="check-1-identify-the-cost-price-list-for-the-project"></a>检查 1：确定项目的成本价目表

从项目的实际值字段查找项目，然后转至项目页面。 单击该字段中的合同签订部门链接。 在“合同签订部门”页上，检查合同签订部门在“成本价目表”网格中是否有价目表。

如果有多个价目表，说明您忽略了此问题。 Project Service 只为每个部门支持一个价目表。 删除该实体的所有价目表，直到部门的“成本价目表”网格中只有一个附加的价目表。

如果没有价目表附加到部门，记下部门的货币。 转至 Project Service，然后转到“参数”，打开“价目表”选项卡。检查是否有任何价目表的上下文设置为“成本”以及与部门的货币匹配的货币。
 
如果没有与该条件匹配的价目表，说明您忽略了此问题。 请确保至少有一个价目表的上下文设置为“成本”且货币与部门的货币匹配。

如果有多个价目表与该条件匹配，请继续阅读本文档以进行更多检查。

## <a name="check-2-are-any-of-the-price-lists-identified-above-valid-for-the-specific-date-of-the-time-cost-actual"></a>检查 2：上方确定的任何价目表是否对时间成本实际值的特定日期有效？

为了 Project Service 能够在确定默认价格时考虑价目表，该价目表应适用于时间成本实际值中的日期。 请检查以下内容查看上面确定的价目表是否适用：

- 检查附加的价目表的常规选项卡上的开始日期和结束日期是否不是空的。 如果上面确定的价目表上的开始日期和结束日期是空的，说明您忽略了此问题。 
- 记下时间成本实际值中的开始日期字段，检查确定的任何价目表是否适用于该日期。 例如，时间成本实际值的日期应在价目表上的开始日期和结束日期之间。 
    - 如果没有覆盖时间成本实际值上该日期的价目表，说明您忽略了此问题。 修改价目表的开始日期和结束日期以确保价目表覆盖时间成本实际值的日期。 
    - 如果有多个覆盖时间成本实际值上该日期的价目表，说明您忽略了此问题。 您可以解决此问题，方法是编辑价目表的开始日期和结束日期，以只有一个价目表覆盖时间成本实际值的日期。 
    - 如果只有一个价目表覆盖时间成本实际值的日期，移至文档中的下一项检查。
在您进行必要的修改后，重新创建一个时间条目，批准它，然后确认时间成本实际值显示有效的价格。

## <a name="check-3-is-there-a-price-in-the-price-list-for-the-pricing-dimensions-on-the-time-cost-actual"></a>检查 3：价目表中是否有价格用于时间成本实际值中的定价维度？

如果成功完成了检查 1 和检查 2，您现在应该只有一个适用于时间成本实际值的日期的价目表。 打开此价目表并转到“角色价格”选项卡。确保时间成本实际值上定价维度的网格中有行。

如果时间成本实际值中的定价维度的角色价格网格中没有行，则说明您忽略了此问题。 在时间成本实际值中定价维度的“角色价格”网格中创建行。 完成后，重新创建时间条目，批准它，然后确认时间成本实际值显示有效的价格。
 
如果在完成上述三项检查后您仍然无法在时间成本实际值中看到有效价格，请提交支持票证。



