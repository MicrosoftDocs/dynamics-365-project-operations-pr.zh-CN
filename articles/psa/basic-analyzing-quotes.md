---
title: 分析项目报价单
description: 此主题介绍如何分析项目报价单。
author: rumant
ms.custom:
- dyn365-projectservice
ms.date: 03/05/2019
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
ms.openlocfilehash: b50f419d2c13cff4914f4b589c8d7ad9099c8734834d75f8d17104d2db40049b
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/06/2021
ms.locfileid: "7002815"
---
# <a name="analysis-of-project-quotes"></a>分析项目报价单

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Dynamics 365 Project Service Automation 分析项目报价单以估算利润率。 还分析报价单与客户的预期交付日期或完成日期和预算之间的匹配情况。

## <a name="profitability-analysis"></a>利润率分析

Project Service Automation 使用毛利和调整后的毛利分析利润率。

- 毛利使用以下公式计算：

  `
    (Sum of estimated chargeable sales value – Sum of estimated chargeable costs) x 100
  `
- 调整后的毛利使用以下公式计算：

  `
    (Sum of estimated chargeable sales value – Sum of all estimated costs) x 100
  `

如果毛利和调整后的毛利的值相差很大，则将报价单的大量工作归类为非应计费。

## <a name="analysis-of-customer-expectations"></a>分析客户期望值

如果您输入以下字段的值，则可分析报价单并生成客户有关计划和预算的期望图表：

- 报价单标头中的 **请求交付日期** 字段。
- 每个报价单明细的 **客户预算**（对于基于项目的明细和基于产品的明细）。

客户的预期计划的分析方法是，将报价单明细详细信息的最新结束日期与报价单中所有报价单明细的请求交付日期进行比较。

客户的预期预算的分析方法是，将客户总预算之和与所有报价单明细中的报价金额进行比较。


[!INCLUDE[footer-include](../includes/footer-banner.md)]