---
title: 设置支出类别
description: 此主题提供有关如何为支出报表设置支出类别和共享类别的信息。
author: suvaidya
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: suvaidya
ms.openlocfilehash: 13e72e4b852fd0edac5ad35d5162e74b016bce33
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/28/2020
ms.locfileid: "4123772"
---
# <a name="set-up-expense-categories"></a><span data-ttu-id="1cdf9-103">设置支出类别</span><span class="sxs-lookup"><span data-stu-id="1cdf9-103">Set up expense categories</span></span>

<span data-ttu-id="1cdf9-104">_**适用于：** 面向资源/非库存场景的 Project Operations_</span><span class="sxs-lookup"><span data-stu-id="1cdf9-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="1cdf9-105">员工在创建支出报表时，其记录的每项支出都必须与支出类别关联。</span><span class="sxs-lookup"><span data-stu-id="1cdf9-105">When employees create expense reports, each expense that they record must be associated with an expense category.</span></span> <span data-ttu-id="1cdf9-106">支出类别派生自可在组织中的法人之间共享的共享类别。</span><span class="sxs-lookup"><span data-stu-id="1cdf9-106">Expense categories are derived from shared categories that can be shared across the legal entities in your organization.</span></span> <span data-ttu-id="1cdf9-107">根据您的组织的定义方式，这些支出类别还可以在其他区域中共享。</span><span class="sxs-lookup"><span data-stu-id="1cdf9-107">Depending on how your organization is defined, these expense categories can also be shared in other areas.</span></span> <span data-ttu-id="1cdf9-108">根据组织的定义和实施团队的指导，您必须确定支出管理中使用的类别是仅在支出管理中使用还是应在其他区域共享。</span><span class="sxs-lookup"><span data-stu-id="1cdf9-108">Based on the definition of your organization and guidance from the implementation team, you must determine whether the categories that are used in Expense management will be used only in Expense management or should be shared in other areas.</span></span>

> [!NOTE]
> <span data-ttu-id="1cdf9-109">这些类别可以在项目管理与会计和支出管理之间共享，也可以在项目管理与会计和生产之间共享。</span><span class="sxs-lookup"><span data-stu-id="1cdf9-109">These categories can be shared between Project management and accounting and Expense management, or between Project management and accounting and Production.</span></span> <span data-ttu-id="1cdf9-110">但是，不能在支出管理和生产之间共享。</span><span class="sxs-lookup"><span data-stu-id="1cdf9-110">However, they can't be shared between Expense management and Production.</span></span>

<span data-ttu-id="1cdf9-111">在开始设置过程之前，每个支出类别必须确定以下方面：</span><span class="sxs-lookup"><span data-stu-id="1cdf9-111">Before you can begin the setup process, the following decisions must be made for each expense category:</span></span>

- <span data-ttu-id="1cdf9-112">什么是支出类别？</span><span class="sxs-lookup"><span data-stu-id="1cdf9-112">What is the expense category?</span></span> <span data-ttu-id="1cdf9-113">示例包括航班、酒店或里程类别。</span><span class="sxs-lookup"><span data-stu-id="1cdf9-113">Examples include categories for flights, hotel, or mileage.</span></span>
- <span data-ttu-id="1cdf9-114">支出类别是否还可以用于项目管理和会计？</span><span class="sxs-lookup"><span data-stu-id="1cdf9-114">Can the expense category also be used in Project management and accounting?</span></span> <span data-ttu-id="1cdf9-115">如果可以，您还必须确定以下方面：</span><span class="sxs-lookup"><span data-stu-id="1cdf9-115">If it can, you must also make the following decisions:</span></span>

    - <span data-ttu-id="1cdf9-116">哪些成本科目将用于以下支出？</span><span class="sxs-lookup"><span data-stu-id="1cdf9-116">Which cost accounts will be used for the following expenses?</span></span>

        - <span data-ttu-id="1cdf9-117">成本</span><span class="sxs-lookup"><span data-stu-id="1cdf9-117">Cost</span></span>
        - <span data-ttu-id="1cdf9-118">工资分配</span><span class="sxs-lookup"><span data-stu-id="1cdf9-118">Payroll allocation</span></span>
        - <span data-ttu-id="1cdf9-119">WIP-成本值</span><span class="sxs-lookup"><span data-stu-id="1cdf9-119">WIP-cost value</span></span>
        - <span data-ttu-id="1cdf9-120">成本-项</span><span class="sxs-lookup"><span data-stu-id="1cdf9-120">Cost-item</span></span>
        - <span data-ttu-id="1cdf9-121">WIP-成本值-项</span><span class="sxs-lookup"><span data-stu-id="1cdf9-121">WIP-cost value-item</span></span>
        - <span data-ttu-id="1cdf9-122">应计损失</span><span class="sxs-lookup"><span data-stu-id="1cdf9-122">Accrued loss</span></span>
        - <span data-ttu-id="1cdf9-123">WIP-应计损失</span><span class="sxs-lookup"><span data-stu-id="1cdf9-123">WIP-accrued loss</span></span>

    - <span data-ttu-id="1cdf9-124">哪些收入科目将用于以下收入来源？</span><span class="sxs-lookup"><span data-stu-id="1cdf9-124">Which revenue accounts will be used for the following sources of revenue?</span></span>

        - <span data-ttu-id="1cdf9-125">已开票收入</span><span class="sxs-lookup"><span data-stu-id="1cdf9-125">Invoiced revenue</span></span>
        - <span data-ttu-id="1cdf9-126">应计收入-销售值</span><span class="sxs-lookup"><span data-stu-id="1cdf9-126">Accrued revenue-sales value</span></span>
        - <span data-ttu-id="1cdf9-127">WIP-销售值</span><span class="sxs-lookup"><span data-stu-id="1cdf9-127">WIP-sales value</span></span>
        - <span data-ttu-id="1cdf9-128">应计收入生产</span><span class="sxs-lookup"><span data-stu-id="1cdf9-128">Accrued revenue-production</span></span>
        - <span data-ttu-id="1cdf9-129">WIP-生产</span><span class="sxs-lookup"><span data-stu-id="1cdf9-129">WIP-production</span></span>
        - <span data-ttu-id="1cdf9-130">应计收入-利润</span><span class="sxs-lookup"><span data-stu-id="1cdf9-130">Accrued revenue-profit</span></span>
        - <span data-ttu-id="1cdf9-131">WIP-利润</span><span class="sxs-lookup"><span data-stu-id="1cdf9-131">WIP-profit</span></span>
        - <span data-ttu-id="1cdf9-132">应计收入-预订</span><span class="sxs-lookup"><span data-stu-id="1cdf9-132">Accrued revenue-subscription</span></span>
        - <span data-ttu-id="1cdf9-133">WIP-预订</span><span class="sxs-lookup"><span data-stu-id="1cdf9-133">WIP-subscription</span></span>

- <span data-ttu-id="1cdf9-134">什么是支出类型？</span><span class="sxs-lookup"><span data-stu-id="1cdf9-134">What is the expense type?</span></span>
- <span data-ttu-id="1cdf9-135">支出类别的默认付款方式是什么？</span><span class="sxs-lookup"><span data-stu-id="1cdf9-135">What is the default payment method for the expense category?</span></span>
- <span data-ttu-id="1cdf9-136">支出类别中的支出是否必须细化？</span><span class="sxs-lookup"><span data-stu-id="1cdf9-136">Do expenses in the expense category have to be itemized?</span></span>
- <span data-ttu-id="1cdf9-137">支出类别的主要默认科目是什么？</span><span class="sxs-lookup"><span data-stu-id="1cdf9-137">What is the main default account for the expense category?</span></span>
- <span data-ttu-id="1cdf9-138">支出类别的默认项销售税组是什么？</span><span class="sxs-lookup"><span data-stu-id="1cdf9-138">What is the default item sales tax group for the expense category?</span></span>
- <span data-ttu-id="1cdf9-139">是否允许对支出类别使用其他付款方式？</span><span class="sxs-lookup"><span data-stu-id="1cdf9-139">Are additional payment methods allowed for the expense category?</span></span> <span data-ttu-id="1cdf9-140">如果允许，有哪些？</span><span class="sxs-lookup"><span data-stu-id="1cdf9-140">If so, what are they?</span></span>
- <span data-ttu-id="1cdf9-141">此支出类别是否有子类别？</span><span class="sxs-lookup"><span data-stu-id="1cdf9-141">Are there subcategories in this expense category?</span></span> <span data-ttu-id="1cdf9-142">如果有子类别，您还必须确定以下方面：</span><span class="sxs-lookup"><span data-stu-id="1cdf9-142">If there are subcategories, you must also make the following decisions:</span></span>

    - <span data-ttu-id="1cdf9-143">是否将任何子类别排除在退税之外？</span><span class="sxs-lookup"><span data-stu-id="1cdf9-143">Are any of the subcategories excluded from tax recovery?</span></span>
    - <span data-ttu-id="1cdf9-144">子类别的项目销售税组是什么？</span><span class="sxs-lookup"><span data-stu-id="1cdf9-144">What is the item sales tax group of the subcategories?</span></span>