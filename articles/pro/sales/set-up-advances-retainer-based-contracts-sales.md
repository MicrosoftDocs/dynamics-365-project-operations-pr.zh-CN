---
title: 预付款和保留款合同
description: 此主题提供有关 Project Operations 中基于保留款的合同签订模型和预付款的信息。
author: rumant
manager: Annbe
ms.date: 10/20/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: e098d25a3e96adf2a1b8e43a19da3a14f446fba9
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/15/2021
ms.locfileid: "5272332"
---
# <a name="advances-and-retainer-based-contracts"></a><span data-ttu-id="efb8c-103">预付款和保留款合同</span><span class="sxs-lookup"><span data-stu-id="efb8c-103">Advances and retainer-based contracts</span></span>


<span data-ttu-id="efb8c-104">_**适用于：** 基于资源/非库存场景的 Project Operations，精简部署 - 估价开票交易_</span><span class="sxs-lookup"><span data-stu-id="efb8c-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="efb8c-105">Dynamics 365 Project Operations 支持基于保留款的合同。</span><span class="sxs-lookup"><span data-stu-id="efb8c-105">Dynamics 365 Project Operations supports retainer-based contracts.</span></span> <span data-ttu-id="efb8c-106">基于保留款的合同是一组商定的平均分配的付款，将在整个项目持续时间内为客户开票。</span><span class="sxs-lookup"><span data-stu-id="efb8c-106">A retainer-based contract is a negotiated set of equally distributed payments that the customer will be invoiced for throughout the duration of a project.</span></span> <span data-ttu-id="efb8c-107">此合同类型通常用于时间和材料或基于使用的记帐模型，这些模型需要向客户提供可预测发票和付款计划。</span><span class="sxs-lookup"><span data-stu-id="efb8c-107">This type of contract is typically used for time and material or consumption-based billing models where there is a need to give the customer a predictable invoice and payment schedule.</span></span> <span data-ttu-id="efb8c-108">每个期间应计的收入实际值与期间开始时从客户处收到的付款进行对帐。</span><span class="sxs-lookup"><span data-stu-id="efb8c-108">Revenue actuals accrued each period are reconciled against the payment received from the customer at the beginning of the period.</span></span> <span data-ttu-id="efb8c-109">根据时间和材料记帐模型概念，每个期间应计的收入值可能因产生的成本而异。</span><span class="sxs-lookup"><span data-stu-id="efb8c-109">In accordance with the concept of the Time and Material billing model, revenue values accrued in each period can vary with the costs incurred.</span></span> <span data-ttu-id="efb8c-110">如果应计收入超过期间开始时收到的金额，项目交付公司可以：</span><span class="sxs-lookup"><span data-stu-id="efb8c-110">If the revenue accrued is more than the amount received at the beginning of the period, the project delivery company could:</span></span>

- <span data-ttu-id="efb8c-111">仅为客户开具超额部分的发票</span><span class="sxs-lookup"><span data-stu-id="efb8c-111">Only invoice the customer for the excess</span></span> 
- <span data-ttu-id="efb8c-112">将收入对帐推迟到下一个开票周期，在项目结束时为所有剩余的未对帐收入创建一个最终账单</span><span class="sxs-lookup"><span data-stu-id="efb8c-112">Defer the reconciliation of the revenue to the next invoicing period and do one final bill at the end of the project for any remaining unreconciled revenue</span></span>

<span data-ttu-id="efb8c-113">在 Project Operations 中，基于保留款的合同签订模型与固定价格合同模型之间的主要区别在于，在固定价格合同模型中，发票金额与产生的成本不关联。</span><span class="sxs-lookup"><span data-stu-id="efb8c-113">The main difference between a retainer-based contracting model and a fixed price contract model in Project Operations is that in the fixed price contract model, the invoice amount is not linked or tied to costs incurred.</span></span> <span data-ttu-id="efb8c-114">开票将采用与该期间产生的成本保持一致的基于里程碑的方法。</span><span class="sxs-lookup"><span data-stu-id="efb8c-114">Invoicing follows a milestone-based approach that is aligned to the costs incurred for that period.</span></span> <span data-ttu-id="efb8c-115">在基于保留款的合同中，可以开票的收入基于合同子项上的记帐方法记录。</span><span class="sxs-lookup"><span data-stu-id="efb8c-115">In a retainer-based contract, revenue that can be invoiced is recorded based on the billing method on the contract line.</span></span> <span data-ttu-id="efb8c-116">当使用时间和材料记帐方法时，可开票收入将与在任何给定期间内产生的成本关联，并会随期间改变发生变化。</span><span class="sxs-lookup"><span data-stu-id="efb8c-116">When the billing method is time and material, the invoiceable revenue is tied to costs incurred in any given period and can vary from period to period.</span></span> <span data-ttu-id="efb8c-117">但是，仅为客户开具定期保留款中金额的发票。</span><span class="sxs-lookup"><span data-stu-id="efb8c-117">However, the customer is only invoiced for the amount on the periodic retainer.</span></span> <span data-ttu-id="efb8c-118">系统将在期末使用另一个发票将期间内记录的可开票收入与期初为客户开票的金额进行对帐。</span><span class="sxs-lookup"><span data-stu-id="efb8c-118">The system uses another invoice at the end of the period to reconcile the invoiceable revenue recorded during the period against the amount that the customer was invoiced for at the start of the period.</span></span>

<span data-ttu-id="efb8c-119">此方法的优点是，与典型的时间和材料模型不同，客户的成本在保留款计划中将变为可预测。</span><span class="sxs-lookup"><span data-stu-id="efb8c-119">The advantage of this method is that the customer's costs become predictable in the retainer schedule unlike in a typical time and material model.</span></span> <span data-ttu-id="efb8c-120">交付项目的组织还有一定的余地，可以弥补因固定价格模型不允许的范围扩大导致的成本收回风险。</span><span class="sxs-lookup"><span data-stu-id="efb8c-120">The organization delivering the project also has some room to cover the risk of recovering the costs incurred due to any increases in scope that a fixed price model would not have allowed them to.</span></span>

<span data-ttu-id="efb8c-121">除了基于定期保留款的计划外，Project Operations 还可以记录来自客户的一次性预付款，然后将其与不同的项目成本组成进行对帐。</span><span class="sxs-lookup"><span data-stu-id="efb8c-121">In addition to a periodic retainer-based schedule, Project Operations can record a one-time advance from a customer and reconcile that against the different project cost components.</span></span>

<span data-ttu-id="efb8c-122">在向客户开票之前，Project Operations 中的保留款不能使用。</span><span class="sxs-lookup"><span data-stu-id="efb8c-122">The retainer in Project Operations isn't available for use until it is invoiced to the customer.</span></span> <span data-ttu-id="efb8c-123">这由预付款和保留款子网格上的以下字段指示。</span><span class="sxs-lookup"><span data-stu-id="efb8c-123">This is indicated by the following fields on the subgrid for advances and retainers.</span></span>

| <span data-ttu-id="efb8c-124">字段</span><span class="sxs-lookup"><span data-stu-id="efb8c-124">Field</span></span> | <span data-ttu-id="efb8c-125">描述</span><span class="sxs-lookup"><span data-stu-id="efb8c-125">Description</span></span> | <span data-ttu-id="efb8c-126">下游影响</span><span class="sxs-lookup"><span data-stu-id="efb8c-126">Downstream impact</span></span> |
| --- | --- | --- |
| <span data-ttu-id="efb8c-127">可用金额</span><span class="sxs-lookup"><span data-stu-id="efb8c-127">Available Amount</span></span> | <span data-ttu-id="efb8c-128">可以用于保留款或预付款记录的金额。</span><span class="sxs-lookup"><span data-stu-id="efb8c-128">The amount that is available to be used on the retainer or advance record.</span></span> | <span data-ttu-id="efb8c-129">在开票之前，预付款或保留款不能使用，这意味着可用金额为零。</span><span class="sxs-lookup"><span data-stu-id="efb8c-129">Until the advance or retainer is invoiced, it isn't available to be used which means the available amount will be zero.</span></span> |
| <span data-ttu-id="efb8c-130">已用金额</span><span class="sxs-lookup"><span data-stu-id="efb8c-130">Used Amount</span></span> | <span data-ttu-id="efb8c-131">已在保留款或预付款中使用的金额。</span><span class="sxs-lookup"><span data-stu-id="efb8c-131">The amount that is already used on the retainer or advance.</span></span> | <span data-ttu-id="efb8c-132">预付款或保留款可以在发票上与实际成本进行部分对帐，这会将某个部分标记为已使用。</span><span class="sxs-lookup"><span data-stu-id="efb8c-132">An advance or retainer can be partially reconciled on an invoice with actual costs which will have some part marked as already used or consumed.</span></span> <span data-ttu-id="efb8c-133">预付款或保留款金额的其余部分可以在将来的发票上与实际成本进行对帐。</span><span class="sxs-lookup"><span data-stu-id="efb8c-133">The rest of the advance or retainer amount is available to reconcile on a future invoice with actual costs.</span></span> |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]