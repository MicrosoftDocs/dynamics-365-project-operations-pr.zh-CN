---
title: 为什么价格在支出销售额实际值中默认为零？
description: 以下三项检查有助于您解答支出销售额实际值中的价格为何默认为 0。
author: rumant
manager: kfend
ms.prod: ''
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
ms.openlocfilehash: bd474d7c0cd64262fdb21d6269efa781b6dc31f2
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/15/2021
ms.locfileid: "5285862"
---
# <a name="why-is-the-price-defaulting-to-zero-on-expense-sales-actuals"></a>为什么价格在支出销售额实际值中默认为零？

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

此常见问题适用于交易记录类设置为“支出”且交易记录类型为“未记帐销售额”的支出实际值。 以下三项检查有助于您解答支出销售额实际值中的价格（帐单费率）为何默认为 0。

## <a name="check-1-identify-the-sales-price-list-for-project"></a>检查 1：确定项目的销售价目表

从项目的实际值字段查找项目并转至项目页面。 然后转到“销售”选项卡。在“项目合同子项”网格上，单击“项目合同”字段中的链接。 “项目合同”页面将打开。 在“项目合同”页面，转到“项目价目表”选项卡。检查此处是否至少附加了一个价目表。

如果“项目合同”的“项目价目表”网格中没有附加价目表：

- 将价目表附加到“项目价目表”网格。 允许在此处附加的价目表应将上下文字段设置为“销售”，且价目表中的货币字段与“项目合同”上的货币字段匹配。 在您进行必要的修改后，重新创建一个支出条目，批准它，然后确认未记帐的销售额实际值显示有效的价格。
- 如果“项目合同”的“项目价目表”网格中有一个或多个附加的价目表，请转到检查 2。

## <a name="check-2-are-any-of-the-price-lists-identified-above-valid-for-the-specific-date-of-the-expense-actual"></a>检查 2：上方确定的任何价目表是否对支出实际值的特定日期有效？

为了 Project Service 能够在确定默认价格时考虑价目表，该价目表应适用于支出销售额实际值中的日期。 请检查以下内容查看上面确定的价目表是否适用：

- 首先检查附加的价目表的常规选项卡上的开始日期和结束日期是否不是空的。 如果上面确定的价目表上的开始日期和结束日期是空的，您忽略了此问题。 
- 记下支出销售额实际值中的开始日期字段，检查确定的任何价目表是否适用于该日期。 例如，支出实际值的日期应在价目表上的开始日期和结束日期之间。 
    - 如果没有覆盖支出销售额实际值上该日期的价目表，说明您忽略了此问题。 修改价目表的开始日期和结束日期以确保价目表覆盖支出实际值的日期。 
    - 如果有多个覆盖支出销售额实际值上该日期的价目表，说明您忽略了此问题。 编辑价目表的开始日期和结束日期，以只有一个价目表覆盖支出实际值的日期。 
    - 如果只有一个价目表覆盖支出实际值的日期，前往检查 3。
在您进行必要的修改后，重新创建一个支出条目，批准它，然后确认未记帐的销售额实际值显示有效的价格。

## <a name="check-3-is-there-a-valid-price-for-the-expense-category-in-the-applicable-project-price-list"></a>检查 3：适用的项目价目表中是否有支出类别的有效价格？ 

如果成功完成了检查 1 和检查 2，您现在应该只有一个适用于支出销售额实际值的日期的项目价目表。 打开此项目价目表并转到“类别价格”选项卡。确保支出实际值上特定支出类别的网格中有行。
 
- 如果没有，则说明您忽略了此问题。 在支出实际值的类别的“类别价格”网格中创建行。 然后，重新创建一个支出条目，批准它，然后确认未记帐的销售额实际值显示有效的价格。 
- 如果类别价格网格中有支出类别行，请检查其是否有有效价格。

若要了解有效的价格是什么，请使用以下方法：

- 如果类别价格行上的“定价方式”字段设置为“按成本”，那么支出销售额实际值中的单位价格将默认为“支出”条目中的值。
- 如果类别价格行上的“定价方式”字段设置为“加价百分比”，则检查“百分比”字段是否设置为有效值。 支出销售额实际值中的单位价格通过将此加价百分比应用到“支出”条目中的价格来确定默认值。
- 如果类别价格行上的“定价方式”字段设置为“单价”，则检查“价格”字段是否设置为有效值。 支出销售额实际值中的单位价格将默认为“价格”字段中指定的货币金额。

如果支出类别的价格设置无效，则说明您忽略了此问题。 解决方法是根据上述规则编辑包含支出类别的有效价格的类别价格行。 完成后，重新创建一个支出条目，批准它，然后检查未记帐的销售额实际值是否获取了有效价格。

如果在完成上述三项检查后您仍然无法在支出销售额实际值中看到有效价格，请提交支持票证。




[!INCLUDE[footer-include](../includes/footer-banner.md)]