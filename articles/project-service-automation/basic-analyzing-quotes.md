---
title: 分析项目报价单
description: 此主题介绍如何分析项目报价单。
author: rumant
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/05/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: 57ac8407-26f5-49dd-97ea-e97642789ff5
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 63c826d27863df62301ec1548fdc94158220c3a2
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/24/2020
ms.locfileid: "3749646"
---
# <a name="analysis-of-project-quotes"></a><span data-ttu-id="262c9-103">分析项目报价单</span><span class="sxs-lookup"><span data-stu-id="262c9-103">Analysis of project quotes</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="262c9-104">Dynamics 365 Project Service Automation 分析项目报价单以估算利润率。</span><span class="sxs-lookup"><span data-stu-id="262c9-104">Dynamics 365 Project Service Automation analyzes project quotes to estimate profitability.</span></span> <span data-ttu-id="262c9-105">还分析报价单与客户的预期交付日期或完成日期和预算之间的匹配情况。</span><span class="sxs-lookup"><span data-stu-id="262c9-105">It also analyzes how well the quote is aligned with customer expectations about the delivery date or completion date, and about the budget.tions.</span></span>

## <a name="profitability-analysis"></a><span data-ttu-id="262c9-106">利润率分析</span><span class="sxs-lookup"><span data-stu-id="262c9-106">Profitability analysis</span></span>

<span data-ttu-id="262c9-107">Project Service Automation 使用毛利和调整后的毛利分析利润率。</span><span class="sxs-lookup"><span data-stu-id="262c9-107">Project Service Automation analyzes profitability by using the gross margin and the adjusted gross margin.</span></span>

- <span data-ttu-id="262c9-108">毛利使用以下公式计算：</span><span class="sxs-lookup"><span data-stu-id="262c9-108">Gross margins are calculated by using the following formula:</span></span>

  `
    (Sum of estimated chargeable sales value – Sum of estimated chargeable costs) x 100
  `
- <span data-ttu-id="262c9-109">调整后的毛利使用以下公式计算：</span><span class="sxs-lookup"><span data-stu-id="262c9-109">The adjusted gross margin is calculated by using the following formula:</span></span>

  `
    (Sum of estimated chargeable sales value – Sum of all estimated costs) x 100
  `

<span data-ttu-id="262c9-110">如果毛利和调整后的毛利的值相差很大，则将报价单的大量工作归类为非应计费。</span><span class="sxs-lookup"><span data-stu-id="262c9-110">If the values for gross margin and adjusted gross margin differ by a wide margin, much of the work in the quote is classified as non-chargeable.</span></span>

## <a name="analysis-of-customer-expectations"></a><span data-ttu-id="262c9-111">分析客户期望值</span><span class="sxs-lookup"><span data-stu-id="262c9-111">Analysis of customer expectations</span></span>

<span data-ttu-id="262c9-112">如果您输入以下字段的值，则可分析报价单并生成客户有关计划和预算的期望图表：</span><span class="sxs-lookup"><span data-stu-id="262c9-112">You can analyze quotes and generate charts for customer expectations about the schedule and budget if you enter values for the following fields:</span></span>

- <span data-ttu-id="262c9-113">报价单标头中的**请求交付日期**字段。</span><span class="sxs-lookup"><span data-stu-id="262c9-113">The **Requested delivery date** field on the quote header.</span></span>
- <span data-ttu-id="262c9-114">每个报价单明细的**客户预算**（对于基于项目的明细和基于产品的明细）。</span><span class="sxs-lookup"><span data-stu-id="262c9-114">The **Customer budget** field for each quote line (for project-based lines and product-based lines).</span></span>

<span data-ttu-id="262c9-115">客户的预期计划的分析方法是，将报价单明细详细信息的最新结束日期与报价单中所有报价单明细的请求交付日期进行比较。</span><span class="sxs-lookup"><span data-stu-id="262c9-115">Analysis of customer expectations about the schedule is done by comparing the latest end date of the quote line detail with the requested delivery date across all quote lines in the quote.</span></span>

<span data-ttu-id="262c9-116">客户的预期预算的分析方法是，将客户总预算之和与所有报价单明细中的报价金额进行比较。</span><span class="sxs-lookup"><span data-stu-id="262c9-116">Analysis of customer expectations about the budget is done by comparing the sum of the total customer budget with the quoted amount across all quote lines.</span></span>