---
title: 为什么价格在支出费用实际值中默认为零？
description: 为什么价格在支出费用实际值中默认为 0 疑难解答。
author: rumant
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 8/22/2018
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
ms.openlocfilehash: 742b0b9c495b4b3ecb4705be3ece5656f0322ca9
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/15/2021
ms.locfileid: "5285832"
---
# <a name="why-is-the-price-defaulting-to-zero-on-expense-cost-actuals"></a>为什么价格在支出费用实际值中默认为零

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

此常见问题适用于交易记录类设置为“支出”且交易记录类型为“成本”的支出实际值。

## <a name="troubleshooting-cost-rates-on-expense-cost-actuals"></a>支出费用实际值上的成本费率疑难解答

转到相关支出条目，确保支出条目字段中有金额。 如果原始支出条目未填写金额，那么您忽略了此问题。
 
若要解决此问题，请使用有效金额重新创建支出条目并批准它。


[!INCLUDE[footer-include](../includes/footer-banner.md)]