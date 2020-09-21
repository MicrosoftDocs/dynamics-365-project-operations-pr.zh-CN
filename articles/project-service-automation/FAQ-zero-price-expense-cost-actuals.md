---
title: 为什么价格在支出费用实际值中默认为零？
description: 为什么价格在支出费用实际值中默认为 0 疑难解答。
author: rumant
manager: kfend
ms.service: business-applications
ms.custom:
- dyn365-projectservice
ms.date: 8/22/2018
ms.topic: article
ms.prod: Project Service
ms.technology: ''
ms.assetid: bc1ebc58-c733-4310-8435-572ed9a9fef9
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 3fb678822877a61d141de75aea29b7d5cdf292c4
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/24/2020
ms.locfileid: "3749697"
---
# <a name="why-is-the-price-defaulting-to-zero-on-expense-cost-actuals"></a>为什么价格在支出费用实际值中默认为零？

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

此常见问题适用于交易记录类设置为“支出”且交易记录类型为“成本”的支出实际值。

## <a name="troubleshooting-cost-rates-on-expense-cost-actuals"></a>支出费用实际值上的成本费率疑难解答

转到相关支出条目，确保支出条目字段中有金额。 如果原始支出条目未填写金额，那么您忽略了此问题。
 
若要解决此问题，请使用有效金额重新创建支出条目并批准它。
