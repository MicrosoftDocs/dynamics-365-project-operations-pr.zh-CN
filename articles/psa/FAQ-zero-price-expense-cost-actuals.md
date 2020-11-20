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
ms.openlocfilehash: 306f169ee25d42ac3c9e63fa70956b9c50315829
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/28/2020
ms.locfileid: "4122107"
---
# <a name="why-is-the-price-defaulting-to-zero-on-expense-cost-actuals"></a><span data-ttu-id="b48c4-103">为什么价格在支出费用实际值中默认为零？</span><span class="sxs-lookup"><span data-stu-id="b48c4-103">Why is the price defaulting to zero on expense cost actuals?</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="b48c4-104">此常见问题适用于交易记录类设置为“支出”且交易记录类型为“成本”的支出实际值。</span><span class="sxs-lookup"><span data-stu-id="b48c4-104">This FAQ applies to expense actuals where the transaction class is set to Expense and transaction type is Cost.</span></span>

## <a name="troubleshooting-cost-rates-on-expense-cost-actuals"></a><span data-ttu-id="b48c4-105">支出费用实际值上的成本费率疑难解答</span><span class="sxs-lookup"><span data-stu-id="b48c4-105">Troubleshooting cost rates on expense cost actuals</span></span>

<span data-ttu-id="b48c4-106">转到相关支出条目，确保支出条目字段中有金额。</span><span class="sxs-lookup"><span data-stu-id="b48c4-106">Go to the related expense entry and make sure that there’s an amount in the expense entry field.</span></span> <span data-ttu-id="b48c4-107">如果原始支出条目未填写金额，那么您忽略了此问题。</span><span class="sxs-lookup"><span data-stu-id="b48c4-107">If the originating expense entry didn’t have the amount field filled, then you have isolated the problem.</span></span>
 
<span data-ttu-id="b48c4-108">若要解决此问题，请使用有效金额重新创建支出条目并批准它。</span><span class="sxs-lookup"><span data-stu-id="b48c4-108">To solve this problem, recreate the expense entry with a valid amount and approve it.</span></span>
