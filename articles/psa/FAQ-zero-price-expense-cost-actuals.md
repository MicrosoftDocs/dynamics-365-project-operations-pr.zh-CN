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
ms.openlocfilehash: f6ea664f9f38621ce5d1b0dd033d7df491f845ff
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/10/2021
ms.locfileid: "5146337"
---
# <a name="why-is-the-price-defaulting-to-zero-on-expense-cost-actuals"></a><span data-ttu-id="7fd7e-103">为什么价格在支出费用实际值中默认为零</span><span class="sxs-lookup"><span data-stu-id="7fd7e-103">Why is the price defaulting to zero on expense cost actuals</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="7fd7e-104">此常见问题适用于交易记录类设置为“支出”且交易记录类型为“成本”的支出实际值。</span><span class="sxs-lookup"><span data-stu-id="7fd7e-104">This FAQ applies to expense actuals where the transaction class is set to Expense and transaction type is Cost.</span></span>

## <a name="troubleshooting-cost-rates-on-expense-cost-actuals"></a><span data-ttu-id="7fd7e-105">支出费用实际值上的成本费率疑难解答</span><span class="sxs-lookup"><span data-stu-id="7fd7e-105">Troubleshooting cost rates on expense cost actuals</span></span>

<span data-ttu-id="7fd7e-106">转到相关支出条目，确保支出条目字段中有金额。</span><span class="sxs-lookup"><span data-stu-id="7fd7e-106">Go to the related expense entry and make sure that there’s an amount in the expense entry field.</span></span> <span data-ttu-id="7fd7e-107">如果原始支出条目未填写金额，那么您忽略了此问题。</span><span class="sxs-lookup"><span data-stu-id="7fd7e-107">If the originating expense entry didn’t have the amount field filled, then you have isolated the problem.</span></span>
 
<span data-ttu-id="7fd7e-108">若要解决此问题，请使用有效金额重新创建支出条目并批准它。</span><span class="sxs-lookup"><span data-stu-id="7fd7e-108">To solve this problem, recreate the expense entry with a valid amount and approve it.</span></span>
