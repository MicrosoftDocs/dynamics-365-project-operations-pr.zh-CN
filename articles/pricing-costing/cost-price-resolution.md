---
title: 解析估计值和实际值的成本费
description: 此主题提供有关如何解析估计值和实际值的成本费的信息。
author: rumant
manager: Annbe
ms.date: 10/13/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: c447e725753d738662f33cc9a5f20ec1a72b2e18
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/28/2020
ms.locfileid: "4119678"
---
# <a name="resolving-cost-prices-for-estimates-and-actuals"></a>解析估计值和实际值的成本费

_**适用于：** 面向资源/非库存场景的 Project Operations_

为了解析估计值和实际值的成本费和成本价目表，系统使用相关项目的 **日期**、**货币** 和 **合同签订部门** 字段中的信息。 解析成本价目表后，应用程序将解析成本费率。

## <a name="resolving-cost-rates-on-actual-and-estimate-lines-for-time"></a>解析“时间”的实际值和估计值明细中的成本费率

“时间”的估计值明细引用项目中时间和资源分配的报价单和合同子项详细信息。

解析成本价目表后，系统将使用“时间”的估计值明细中的 **角色**、**资源供给公司** 和 **资源单位** 字段与价目表中的角色价格明细进行匹配。 这一匹配假设您使用的是现成的人工成本定价维度。 如果您将系统配置为匹配代替 **角色**、**资源供给公司** 和 **资源单位** 的字段或除这几个字段外还匹配其他字段，将使用不同的组合来检索匹配的角色价格明细。 如果应用程序发现具有 **角色**、**资源供给公司** 和 **资源单位** 组合的成本费率的角色价格明细，那就是默认成本费率。 如果应用程序无法匹配 **角色**、**资源供给公司** 和 **资源单位** 值，它将检索具有匹配角色的角色价格明细，但 **资源单位** 为 null 值。 在有了匹配的角色价格记录后，成本费率将默认为该记录中的值。 

> [!NOTE]
> 如果您配置不同的 **角色**、**资源供给公司** 和 **资源单位** 优先级，或者您有优先级更高的其他维度，此行为将相应变更。 系统将按优先级顺序使用与每个定价维度值匹配的值检索角色价格记录，这些维度为 null 值的行排在最后。

## <a name="resolving-cost-rates-on-actual-and-estimate-lines-for-expense"></a>解析“支出”的实际值和估计值明细中的成本费率

“支出”的估计值明细引用项目中支出和支出估计值明细的报价单和合同子项详细信息。

解析成本价目表后，系统将使用支出的估计值明细中的 **类别** 和 **单位** 字段的组合与解析的价目表中的 **类别价格** 明细进行匹配。 如果系统发现具有 **类别** 和 **单位** 字段组合的成本费率的类别价格明细，此成本费率将为默认值。 如果系统无法匹配 **类别** 和 **单位** 值，或者能够找到匹配的类别价格明细，但定价方式不是 **单价**，成本费率默认为零 (0)。


[!INCLUDE[footer-include](../includes/footer-banner.md)]