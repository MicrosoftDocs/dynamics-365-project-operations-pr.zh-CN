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
# <a name="why-is-the-price-defaulting-to-zero-on-expense-cost-actuals"></a><span data-ttu-id="b149e-103">为什么价格在支出费用实际值中默认为零？</span><span class="sxs-lookup"><span data-stu-id="b149e-103">Why is the price defaulting to zero on expense cost actuals?</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="b149e-104">此常见问题适用于交易记录类设置为“支出”且交易记录类型为“成本”的支出实际值。</span><span class="sxs-lookup"><span data-stu-id="b149e-104">This FAQ applies to expense actuals where the transaction class is set to Expense and transaction type is Cost.</span></span>

## <a name="troubleshooting-cost-rates-on-expense-cost-actuals"></a><span data-ttu-id="b149e-105">支出费用实际值上的成本费率疑难解答</span><span class="sxs-lookup"><span data-stu-id="b149e-105">Troubleshooting cost rates on expense cost actuals</span></span>

<span data-ttu-id="b149e-106">转到相关支出条目，确保支出条目字段中有金额。</span><span class="sxs-lookup"><span data-stu-id="b149e-106">Go to the related expense entry and make sure that there’s an amount in the expense entry field.</span></span> <span data-ttu-id="b149e-107">如果原始支出条目未填写金额，那么您忽略了此问题。</span><span class="sxs-lookup"><span data-stu-id="b149e-107">If the originating expense entry didn’t have the amount field filled, then you have isolated the problem.</span></span>
 
<span data-ttu-id="b149e-108">若要解决此问题，请使用有效金额重新创建支出条目并批准它。</span><span class="sxs-lookup"><span data-stu-id="b149e-108">To solve this problem, recreate the expense entry with a valid amount and approve it.</span></span>