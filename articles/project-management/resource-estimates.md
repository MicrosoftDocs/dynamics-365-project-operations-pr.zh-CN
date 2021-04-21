---
title: 项目资源时间的财务估算
description: 此主题提供了关于如何计算时间财务估算的信息。
author: rumant
manager: Annbe
ms.date: 03/19/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 91156c5cf79af8c66c12b84a6d2b17aa7fe09ed1
ms.sourcegitcommit: 386921f44f1e9a8a828b140206d52945de07aee7
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/22/2021
ms.locfileid: "5701815"
---
# <a name="financial-estimates-for-resource-time-on-projects"></a><span data-ttu-id="1f7ee-103">项目资源时间的财务估算</span><span class="sxs-lookup"><span data-stu-id="1f7ee-103">Financial estimates for resource time on projects</span></span>

<span data-ttu-id="1f7ee-104">_**适用于：** 基于资源/非库存场景的 Project Operations，精简部署 - 估价开票交易_</span><span class="sxs-lookup"><span data-stu-id="1f7ee-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="1f7ee-105">系统根据三种因素来计算时间财务估算：</span><span class="sxs-lookup"><span data-stu-id="1f7ee-105">Financial estimates for time are calculated based on three factors:</span></span> 

- <span data-ttu-id="1f7ee-106">分派给项目规划的每个叶节点任务的通用或指定团队成员类型。</span><span class="sxs-lookup"><span data-stu-id="1f7ee-106">The type of generic or named team member assigned to each leaf node task on the project plan.</span></span> 
- <span data-ttu-id="1f7ee-107">工作的类型或复杂程度。</span><span class="sxs-lookup"><span data-stu-id="1f7ee-107">The type or complexity of work.</span></span>
- <span data-ttu-id="1f7ee-108">任务资源分配工作分布。</span><span class="sxs-lookup"><span data-stu-id="1f7ee-108">The spread of effort for the resource's assignment on the task.</span></span> 

<span data-ttu-id="1f7ee-109">前两个因素会影响资源分派的单位成本或帐单费率。</span><span class="sxs-lookup"><span data-stu-id="1f7ee-109">The first two factors influence the unit cost or bill rate of a resource's assignment.</span></span> <span data-ttu-id="1f7ee-110">资源分派的单位成本或帐单费率由分派的资源的属性确定。</span><span class="sxs-lookup"><span data-stu-id="1f7ee-110">The unit cost or bill rate of a resource assignment is determined by the attributes of the resource assigned.</span></span> <span data-ttu-id="1f7ee-111">这些属性包括资源所属的部门以及资源的标准角色。</span><span class="sxs-lookup"><span data-stu-id="1f7ee-111">These attributes include the organizational unit to which the resource belongs and the standard role of the resource.</span></span> <span data-ttu-id="1f7ee-112">您还可以为资源添加与您的业务相关的自定义属性（如标准职务或体验级别），并让它们影响分派的单位成本或帐单费率。</span><span class="sxs-lookup"><span data-stu-id="1f7ee-112">You can also add custom attributes relevant to your business for the resource, like standard title or experience level, and have them influence the unit cost or bill rate of the assignment.</span></span>
<span data-ttu-id="1f7ee-113">除了资源的属性之外，工作属性（例如任务）还可能会影响分派的单位帐单费率或成本费率。</span><span class="sxs-lookup"><span data-stu-id="1f7ee-113">In addition to the attributes of the resource, attributes of work, such as the task, can also influence the unit bill rate or cost rate of the assignment.</span></span> <span data-ttu-id="1f7ee-114">例如，如果特定任务更复杂，则将资源分配给这些特定任务会导致比不太复杂的任务更高的单位成本或帐单费率。</span><span class="sxs-lookup"><span data-stu-id="1f7ee-114">For example, when certain tasks are more complex, the resource's assignment to those specific tasks result in a higher unit cost or bill rate than tasks that are less complex.</span></span>   

<span data-ttu-id="1f7ee-115">第三个因素提供按该费率计算的小时数。</span><span class="sxs-lookup"><span data-stu-id="1f7ee-115">The third factor provides the quantity of hours at that rate.</span></span> <span data-ttu-id="1f7ee-116">在任务涉及两个时间段的情况下，该任务资源分派的第一部分的成本计算和定价可能会不同于任务的第二部分。</span><span class="sxs-lookup"><span data-stu-id="1f7ee-116">In cases where a task covers two price periods, it is likely that the first part of the resource assignment for that task is costed and priced differently than the second portion of the task.</span></span> <span data-ttu-id="1f7ee-117">每个资源分派的工作估算是一个复杂的值，此值与每天的工作量每日分配一起存储。</span><span class="sxs-lookup"><span data-stu-id="1f7ee-117">The effort estimate on each resource assignment is a complex value stored with the daily distribution of effort per day.</span></span>

<span data-ttu-id="1f7ee-118">有关如何将工作和资源自定义属性设置为定价和成本计算维度的详细说明，请参阅[定价维度概述](../pricing-costing/pricing-dimensions-overview.md)。</span><span class="sxs-lookup"><span data-stu-id="1f7ee-118">For detailed instructions about how to set up custom attributes of work and resources as pricing and costing dimensions, see [Pricing Dimensions overview](../pricing-costing/pricing-dimensions-overview.md).</span></span>

<span data-ttu-id="1f7ee-119">每项资源分配的财务估算的计算公式为 **分配的费用/小时乘以小时数。**</span><span class="sxs-lookup"><span data-stu-id="1f7ee-119">The financial estimate on each resource assignment is calculated as **rate/hr for the assignment multiplied by the number of hours.**</span></span>  <span data-ttu-id="1f7ee-120">与工作量估算相似，每项资源分配的成本和收入的财务估算是一个复杂值，此值与每天的货币金额每日分配一起存储。</span><span class="sxs-lookup"><span data-stu-id="1f7ee-120">Similar to the effort estimate, the financial estimate for cost and revenue for each resource assignment is a complex value stored with the daily distribution of monetary amount per day.</span></span> 

## <a name="summarizing-financial-estimates-for-time"></a><span data-ttu-id="1f7ee-121">汇总时间财务估算</span><span class="sxs-lookup"><span data-stu-id="1f7ee-121">Summarizing financial estimates for time</span></span>
<span data-ttu-id="1f7ee-122">叶节点任务中的时间财务估算是该任务的所有资源分配的财务估算总和。</span><span class="sxs-lookup"><span data-stu-id="1f7ee-122">A financial estimate for time on a leaf node task is the sum of the financial estimates on all resource assignments for that task.</span></span>

<span data-ttu-id="1f7ee-123">摘要任务或父任务中的时间财务估算是其所有子任务的财务估算总和。</span><span class="sxs-lookup"><span data-stu-id="1f7ee-123">A financial estimate for time on a summary or parent task is the sum of the financial estimates on all of its child tasks.</span></span> <span data-ttu-id="1f7ee-124">这是项目的估算人工成本。</span><span class="sxs-lookup"><span data-stu-id="1f7ee-124">This is the estimated labor cost on the project.</span></span> 

![资源预估](./media/navigation12.png)

## <a name="default-cost-price-and-cost-currency"></a><span data-ttu-id="1f7ee-126">默认成本费和成本货币</span><span class="sxs-lookup"><span data-stu-id="1f7ee-126">Default cost price and cost currency</span></span>

<span data-ttu-id="1f7ee-127">默认成本价格来自附加到项目合同单位的价目表。</span><span class="sxs-lookup"><span data-stu-id="1f7ee-127">The default cost price comes from the price lists attached to the contracting unit of the project.</span></span> <span data-ttu-id="1f7ee-128">项目的成本货币始终是项目的合同单位的货币。</span><span class="sxs-lookup"><span data-stu-id="1f7ee-128">The cost currency of a project is always the currency of the contracting unit of the project.</span></span> <span data-ttu-id="1f7ee-129">分配资源时，成本的财务估算以项目成本货币为单位进行存储。</span><span class="sxs-lookup"><span data-stu-id="1f7ee-129">On a resource assignment, the financial estimate for cost is stored in the cost currency of the project.</span></span> <span data-ttu-id="1f7ee-130">有时，在价目表中设置成本费率所使用的货币不同于项目的成本货币。</span><span class="sxs-lookup"><span data-stu-id="1f7ee-130">Sometimes, the currency in which the cost rate is set up in the price list is different from the project's cost currency.</span></span> <span data-ttu-id="1f7ee-131">在这种情况下，应用程序将针对项目货币转换设置成本价格所采用的货币。</span><span class="sxs-lookup"><span data-stu-id="1f7ee-131">In these cases, the application converts the currency in which the cost price is set up for the currency of the project.</span></span> <span data-ttu-id="1f7ee-132">在 **估算** 网格上，所有成本估算均以项目成本货币显示和汇总。</span><span class="sxs-lookup"><span data-stu-id="1f7ee-132">On the **Estimates** grid, all cost estimates are displayed and summarized in the project's cost currency.</span></span> 

## <a name="default-bill-rate-and-sales-currency"></a><span data-ttu-id="1f7ee-133">默认帐单费率和销售货币</span><span class="sxs-lookup"><span data-stu-id="1f7ee-133">Default bill rate and sales currency</span></span>

<span data-ttu-id="1f7ee-134">如果赢得交易，则默认销售价格来自相关项目合同所附加的项目价目表，如果交易仍处于预售阶段，则来自相关项目报价单。</span><span class="sxs-lookup"><span data-stu-id="1f7ee-134">The default sales price comes from the project price lists attached to the related project contract if the deal is won, or from the related project quote if the deal is still in the pre-sales stage.</span></span> <span data-ttu-id="1f7ee-135">项目的销售货币始终是项目报价单或项目合同的货币。</span><span class="sxs-lookup"><span data-stu-id="1f7ee-135">The sales currency of the project is always the currency of the project quote or the project contract.</span></span> <span data-ttu-id="1f7ee-136">分配资源时，销售的财务估算以项目销售货币为单位进行存储。</span><span class="sxs-lookup"><span data-stu-id="1f7ee-136">On a resource assignment, the financial estimate for sales is stored in the sales currency of the project.</span></span> <span data-ttu-id="1f7ee-137">与成本不同，在价目表中设置的销售价格从不会与项目的销售货币不同。</span><span class="sxs-lookup"><span data-stu-id="1f7ee-137">Unlike cost, the sales price that is set up in the price list can never be different from the project's sales currency.</span></span> <span data-ttu-id="1f7ee-138">不存在需要货币换算的情况。</span><span class="sxs-lookup"><span data-stu-id="1f7ee-138">There is no scenario where currency conversion is needed.</span></span> <span data-ttu-id="1f7ee-139">在 **估算** 网格上，所有销售估算均以项目销售货币显示和汇总。</span><span class="sxs-lookup"><span data-stu-id="1f7ee-139">On the **Estimates** grid, all sales estimates are displayed and summarized in the project's sales currency.</span></span> 

[!INCLUDE[footer-include](../includes/footer-banner.md)]
