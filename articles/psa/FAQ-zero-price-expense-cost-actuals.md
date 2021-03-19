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
# <a name="why-is-the-price-defaulting-to-zero-on-expense-cost-actuals"></a><span data-ttu-id="982f7-103">为什么价格在支出费用实际值中默认为零</span><span class="sxs-lookup"><span data-stu-id="982f7-103">Why is the price defaulting to zero on expense cost actuals</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="982f7-104">此常见问题适用于交易记录类设置为“支出”且交易记录类型为“成本”的支出实际值。</span><span class="sxs-lookup"><span data-stu-id="982f7-104">This FAQ applies to expense actuals where the transaction class is set to Expense and transaction type is Cost.</span></span>

## <a name="troubleshooting-cost-rates-on-expense-cost-actuals"></a><span data-ttu-id="982f7-105">支出费用实际值上的成本费率疑难解答</span><span class="sxs-lookup"><span data-stu-id="982f7-105">Troubleshooting cost rates on expense cost actuals</span></span>

<span data-ttu-id="982f7-106">转到相关支出条目，确保支出条目字段中有金额。</span><span class="sxs-lookup"><span data-stu-id="982f7-106">Go to the related expense entry and make sure that there’s an amount in the expense entry field.</span></span> <span data-ttu-id="982f7-107">如果原始支出条目未填写金额，那么您忽略了此问题。</span><span class="sxs-lookup"><span data-stu-id="982f7-107">If the originating expense entry didn’t have the amount field filled, then you have isolated the problem.</span></span>
 
<span data-ttu-id="982f7-108">若要解决此问题，请使用有效金额重新创建支出条目并批准它。</span><span class="sxs-lookup"><span data-stu-id="982f7-108">To solve this problem, recreate the expense entry with a valid amount and approve it.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]