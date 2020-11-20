---
title: 配置支出管理
description: 本文介绍您在 Microsoft Dynamics 365 Finance 中配置“支出管理”前在计划流程中的考虑事项和必须做的决定。
author: KimANelson
manager: AnnBe
ms.date: 08/29/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: GlobalCategory, ProjCategory, TrvLocations, TrvParameters, TrvPaymethod, TrvPerDiems
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 23001
ms.assetid: aa3fd14d-7e94-4603-985f-ca26d6f860ea
ms.search.region: Global
ms.author: suvaidya
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e2291515cc154fb5b34ca5802135791958bea1e5
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/16/2020
ms.locfileid: "4072752"
---
# <a name="configure-expense-management"></a><span data-ttu-id="d0b5d-103">配置支出管理</span><span class="sxs-lookup"><span data-stu-id="d0b5d-103">Configure expense management</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d0b5d-104">本主题介绍您配置“支出管理”前在计划流程中的考虑事项和必须做的决定。</span><span class="sxs-lookup"><span data-stu-id="d0b5d-104">This topic describes the considerations and the decisions that you must make during the planning process before you configure Expense management.</span></span> <span data-ttu-id="d0b5d-105">在支出管理中，您可以存储有关付款方式、出差申请、支出报表和政策等的信息。</span><span class="sxs-lookup"><span data-stu-id="d0b5d-105">In Expense management, you can store information about payment methods, travel requisitions, expense reports, policies, and so on.</span></span>

<span data-ttu-id="d0b5d-106">由于您在计划支出管理的配置时所做的许多决策基于您的组织的层次结构和财务结构，因此您必须是引用这些领域的计划文档。</span><span class="sxs-lookup"><span data-stu-id="d0b5d-106">Because many of the decisions that you make when you plan your configuration for Expense management are based on your organization’s hierarchy and financial structure, you must refer to the planning documents for those areas.</span></span>

## <a name="intercompany-expenses"></a><span data-ttu-id="d0b5d-107">内部公司支出</span><span class="sxs-lookup"><span data-stu-id="d0b5d-107">Intercompany expenses</span></span>

<span data-ttu-id="d0b5d-108">在您启用内部公司支出时，您允许和法人和员工代表您组织中的其他法人产生支出，从您组织中的雇佣法人那里收取付款。</span><span class="sxs-lookup"><span data-stu-id="d0b5d-108">When you enable intercompany expenses, you allow legal entities and employees to incur expenses on behalf of another legal entity, and collect payment from the legal entity of employment within your organization.</span></span> <span data-ttu-id="d0b5d-109">例如，法人 A 中的一名员工完成法人 B 的一个项目，且该项目产生出差支出。</span><span class="sxs-lookup"><span data-stu-id="d0b5d-109">For example, an employee in legal entity A completes a project for legal entity B, and the project incurs travel related expenses.</span></span> <span data-ttu-id="d0b5d-110">如果启用内部公司支出，则该员工可以提交支出报表，将支出过帐到法人 B，且该支出必须由法人 A 支付。如果您的组织不具有多个法人，您就不需要启用内部公司支出。</span><span class="sxs-lookup"><span data-stu-id="d0b5d-110">If intercompany expenses are enabled, the employee can then file an expense report that will post the expense to legal entity B, and the expense must then be paid by legal entity A. If your organization doesn’t have multiple legal entities, you don’t have to enable intercompany expenses.</span></span>

<span data-ttu-id="d0b5d-111">**决策：** 是否要启用内部公司支出？</span><span class="sxs-lookup"><span data-stu-id="d0b5d-111">**Decision:** Do you want to enable intercompany expenses?</span></span>

## <a name="financial-management"></a><span data-ttu-id="d0b5d-112">财务管理</span><span class="sxs-lookup"><span data-stu-id="d0b5d-112">Financial management</span></span>

<span data-ttu-id="d0b5d-113">支出管理与您的组织的财务管理紧密集成。</span><span class="sxs-lookup"><span data-stu-id="d0b5d-113">Expense management is tightly integrated with the financial management of your organization.</span></span> <span data-ttu-id="d0b5d-114">支出管理的许多配置都将基于您作出的关于您的组织的财务决策。</span><span class="sxs-lookup"><span data-stu-id="d0b5d-114">Lots of your configuration for Expense management will be based on the decisions that you’ve made about your organization’s finances.</span></span> <span data-ttu-id="d0b5d-115">以下各节介绍需要基于您的领导团队给出的您组织的财务决策和指导计划和决策的不同领域。</span><span class="sxs-lookup"><span data-stu-id="d0b5d-115">The following sections describe the various areas that require planning and decisions, based on your organization’s financial decisions and guidance from your leadership team.</span></span>

### <a name="per-diems"></a><span data-ttu-id="d0b5d-116">出差津贴</span><span class="sxs-lookup"><span data-stu-id="d0b5d-116">Per diems</span></span>

<span data-ttu-id="d0b5d-117">您必须定义您的组织提供的员工出差津贴。</span><span class="sxs-lookup"><span data-stu-id="d0b5d-117">You must define the employee per diems that your organization provides.</span></span> <span data-ttu-id="d0b5d-118">由于出差津贴通常用于覆盖支出（如津贴、住所和其他附加支出），因此您可以创建您的组织提供的出差津贴补助的规则。</span><span class="sxs-lookup"><span data-stu-id="d0b5d-118">Because per diems are typically used to cover expenses such as meals, lodging, and other incidental expenses, you can create rules for the per diem allowances that your organization offers.</span></span> <span data-ttu-id="d0b5d-119">出差津贴比率可以基于出差时间和/或出差地点。</span><span class="sxs-lookup"><span data-stu-id="d0b5d-119">per diem rates can be based on the time of year, the travel location, or both.</span></span> <span data-ttu-id="d0b5d-120">在定义某一出差津贴规则时，您可以指定将预扣的出差津贴支出百分比（如果工作人员获得了免费提供的餐饮或服务）。</span><span class="sxs-lookup"><span data-stu-id="d0b5d-120">When you define a per diem rule, you can specify that a percentage of the per diem rate will be withheld if a worker receives complimentary meals or services.</span></span> <span data-ttu-id="d0b5d-121">您还可以定义出差津贴费率层，以设置可以对工作人员差旅应用出差津贴费率的最低和最高小时数。</span><span class="sxs-lookup"><span data-stu-id="d0b5d-121">You can also define per diem rate tiers to set the minimum and maximum number of hours that the per diem rate can be applied to a worker’s travel.</span></span>

<span data-ttu-id="d0b5d-122">**决策：**</span><span class="sxs-lookup"><span data-stu-id="d0b5d-122">**Decisions:**</span></span>

- <span data-ttu-id="d0b5d-123">第一天和最后一天的默认出差津贴规则：</span><span class="sxs-lookup"><span data-stu-id="d0b5d-123">Default per diem rules for the first and last days:</span></span>

    - <span data-ttu-id="d0b5d-124">员工可以要求一天下班打卡并仍领取出差津贴的最低小时数是多少？</span><span class="sxs-lookup"><span data-stu-id="d0b5d-124">What is the minimum number of hours that an employee can claim for a day and still receive a per diem?</span></span>
    - <span data-ttu-id="d0b5d-125">为第一天和最后一天的餐饮提供的金额是否减少？</span><span class="sxs-lookup"><span data-stu-id="d0b5d-125">Is there a reduction in the amount that is offered for meals for the first day and last day?</span></span> <span data-ttu-id="d0b5d-126">如果减少，那么减少的百分比是多少？</span><span class="sxs-lookup"><span data-stu-id="d0b5d-126">If there is a reduction, what is the percentage of the reduction?</span></span>
    - <span data-ttu-id="d0b5d-127">为第一天和最后一天的酒店提供的金额是否减少？</span><span class="sxs-lookup"><span data-stu-id="d0b5d-127">Is there a reduction in the amount that is offered for a hotel for the first day and last day?</span></span> <span data-ttu-id="d0b5d-128">如果减少，那么减少的百分比是多少？</span><span class="sxs-lookup"><span data-stu-id="d0b5d-128">If there is a reduction, what is the percentage of the reduction?</span></span>
    - <span data-ttu-id="d0b5d-129">为第一天和最后一天发生的其他支出提供的金额是否减少？</span><span class="sxs-lookup"><span data-stu-id="d0b5d-129">Is there a reduction in the amount that is offered for other expenses that are incurred on the first day and last day?</span></span> <span data-ttu-id="d0b5d-130">如果减少，那么减少的百分比是多少？</span><span class="sxs-lookup"><span data-stu-id="d0b5d-130">If there is a reduction, what is the percentage of the reduction?</span></span>

- <span data-ttu-id="d0b5d-131">默认出差津贴规则：</span><span class="sxs-lookup"><span data-stu-id="d0b5d-131">Default per diem rules:</span></span>

    - <span data-ttu-id="d0b5d-132">如果（例如）就餐是免费的，那么每次就餐的出差津贴补助是否存在百分比减少？</span><span class="sxs-lookup"><span data-stu-id="d0b5d-132">Is there a percentage reduction in the per diem allowance for each meal if, for example, the meal is complimentary?</span></span> <span data-ttu-id="d0b5d-133">如果减少，那么每餐减少的百分比是多少？</span><span class="sxs-lookup"><span data-stu-id="d0b5d-133">If there is a reduction, what is the reduction percentage for each meal?</span></span>
    - <span data-ttu-id="d0b5d-134">餐费减少是按天、按行程计算的，还是按每天的就餐次数计算的？</span><span class="sxs-lookup"><span data-stu-id="d0b5d-134">Is the meal reduction calculated per day, per trip, or by the number of meals per day?</span></span>
    - <span data-ttu-id="d0b5d-135">出差津贴金额是否应按常规方式四舍五入或向上化整？</span><span class="sxs-lookup"><span data-stu-id="d0b5d-135">Should per diem amounts be rounded in the regular manner or rounded up?</span></span>
    - <span data-ttu-id="d0b5d-136">出差津贴是按 24 小时期间计算的还是按一个日历天计算的？</span><span class="sxs-lookup"><span data-stu-id="d0b5d-136">Are per diems calculated on a 24-hour period or on a calendar day?</span></span>

- <span data-ttu-id="d0b5d-137">基于位置的出差津贴规则：</span><span class="sxs-lookup"><span data-stu-id="d0b5d-137">Per diem rules that are based on location:</span></span>

    - <span data-ttu-id="d0b5d-138">出差津贴比率根据位置而存在差异？</span><span class="sxs-lookup"><span data-stu-id="d0b5d-138">Do per diem rates vary according to location?</span></span> <span data-ttu-id="d0b5d-139">哪些位置包括在内？</span><span class="sxs-lookup"><span data-stu-id="d0b5d-139">What locations are included?</span></span>
    - <span data-ttu-id="d0b5d-140">如果出差津贴比率根据位置而存在差异，那么对于每个位置，为以下支出类型提供的金额百分比是多少：</span><span class="sxs-lookup"><span data-stu-id="d0b5d-140">If per diem rates vary according to location, for each location, what percentage amount is provided for the following types of expenses:</span></span>

        - <span data-ttu-id="d0b5d-141">餐费</span><span class="sxs-lookup"><span data-stu-id="d0b5d-141">Meals</span></span>
        - <span data-ttu-id="d0b5d-142">酒店</span><span class="sxs-lookup"><span data-stu-id="d0b5d-142">Hotel</span></span>
        - <span data-ttu-id="d0b5d-143">其他支出</span><span class="sxs-lookup"><span data-stu-id="d0b5d-143">Other expenses</span></span>

### <a name="expense-management-journals-and-accounts"></a><span data-ttu-id="d0b5d-144">支出管理日记帐和帐户</span><span class="sxs-lookup"><span data-stu-id="d0b5d-144">Expense management journals and accounts</span></span>

<span data-ttu-id="d0b5d-145">支出管理要求您使用多个日记帐和帐户。</span><span class="sxs-lookup"><span data-stu-id="d0b5d-145">Expense management requires that you use multiple journals and accounts.</span></span> <span data-ttu-id="d0b5d-146">例如，您必须确定同一帐户是否用于预付现金和信用卡争议。</span><span class="sxs-lookup"><span data-stu-id="d0b5d-146">You must decide, for example, whether the same account is used for cash advances and credit card disputes.</span></span>

<span data-ttu-id="d0b5d-147">**决策：**</span><span class="sxs-lookup"><span data-stu-id="d0b5d-147">**Decisions:**</span></span>

- <span data-ttu-id="d0b5d-148">已审核的支出报表过帐到哪个分类帐日记帐？</span><span class="sxs-lookup"><span data-stu-id="d0b5d-148">Which ledger journal are approved expense reports posted to?</span></span>
- <span data-ttu-id="d0b5d-149">哪个帐户用于预付现金？</span><span class="sxs-lookup"><span data-stu-id="d0b5d-149">Which account is used for cash advances?</span></span>
- <span data-ttu-id="d0b5d-150">是否应立即过帐预付现金？</span><span class="sxs-lookup"><span data-stu-id="d0b5d-150">Should cash advances be posted immediately?</span></span>

### <a name="payment-methods"></a><span data-ttu-id="d0b5d-151">付款方式</span><span class="sxs-lookup"><span data-stu-id="d0b5d-151">Payment methods</span></span>

<span data-ttu-id="d0b5d-152">当您允许员工代表您的企业产生支出时，您必须定义允许员工使用的付款方式。</span><span class="sxs-lookup"><span data-stu-id="d0b5d-152">When you allow employees to incur expenses on behalf of your business, you must define the payment methods that employees are allowed to use.</span></span> <span data-ttu-id="d0b5d-153">例如，您可能允许员工使用现金或公司信用卡。</span><span class="sxs-lookup"><span data-stu-id="d0b5d-153">For example, you might allow employees to use cash or a corporate credit card.</span></span> <span data-ttu-id="d0b5d-154">您可能还允许员工使用个人信用卡，然后偿还员工。</span><span class="sxs-lookup"><span data-stu-id="d0b5d-154">You might also allow employees to use personal credit cards, and then reimburse the employees.</span></span> <span data-ttu-id="d0b5d-155">您必须为允许您的每个付款方式做出以下决策。</span><span class="sxs-lookup"><span data-stu-id="d0b5d-155">You must make the following decisions for each payment method that you allow.</span></span>

<span data-ttu-id="d0b5d-156">**决策：**</span><span class="sxs-lookup"><span data-stu-id="d0b5d-156">**Decisions:**</span></span>

- <span data-ttu-id="d0b5d-157">允许什么付款方式？</span><span class="sxs-lookup"><span data-stu-id="d0b5d-157">What payment methods are allowed?</span></span>
- <span data-ttu-id="d0b5d-158">谁拥有付款方式支出？</span><span class="sxs-lookup"><span data-stu-id="d0b5d-158">Who owns the payment method expenses?</span></span>
- <span data-ttu-id="d0b5d-159">是否有对方科目类型？</span><span class="sxs-lookup"><span data-stu-id="d0b5d-159">Is there an offset account type?</span></span> <span data-ttu-id="d0b5d-160">如果存在一个对方科目类型，该类型是什么？</span><span class="sxs-lookup"><span data-stu-id="d0b5d-160">If there is an offset account type, what is it?</span></span>
- <span data-ttu-id="d0b5d-161">如果存在一个对方科目，该科目是什么？</span><span class="sxs-lookup"><span data-stu-id="d0b5d-161">If there is an offset account, what is the account?</span></span>
- <span data-ttu-id="d0b5d-162">如果付款方式是信用卡，那么是否付款方式仅用于导入的交易记录？</span><span class="sxs-lookup"><span data-stu-id="d0b5d-162">If the payment method is a credit card, should the payment method be used only with imported transactions?</span></span>

### <a name="expense-categories-and-shared-categories"></a><span data-ttu-id="d0b5d-163">支出类别和共享类别</span><span class="sxs-lookup"><span data-stu-id="d0b5d-163">Expense categories and shared categories</span></span>

<span data-ttu-id="d0b5d-164">当员工创建支出报表时，他们记录的每个支出都必须与支出类别关联。</span><span class="sxs-lookup"><span data-stu-id="d0b5d-164">When employees create an expense report, each expense that they record must be associated with an expense category.</span></span> <span data-ttu-id="d0b5d-165">支出类别派生自可在组织中的法人之间共享的共享类别。</span><span class="sxs-lookup"><span data-stu-id="d0b5d-165">Expense categories are derived from shared categories that can be shared across the legal entities in your organization.</span></span> <span data-ttu-id="d0b5d-166">这些类别还可以在项目管理和会计中共享，具体取决于您的组织的定义方式。</span><span class="sxs-lookup"><span data-stu-id="d0b5d-166">These categories can also be shared in Project management and accounting, depending on the way that your organization is defined.</span></span> <span data-ttu-id="d0b5d-167">根据您组织的定义和实施团队的指导，确定在支出管理中使用的类别是否要仅在支出管理中使用，或者它们是否应在项目管理和会计和支出管理之间共享。</span><span class="sxs-lookup"><span data-stu-id="d0b5d-167">Based on the definition of your organization and guidance from the implementation team, determine whether the categories that are used in Expense management will be used only in Expense management, or whether they should be shared between Project management and accounting and Expense management.</span></span> <span data-ttu-id="d0b5d-168">请注意，这些类别可以在项目和支出或项目和生产之间共享，不过，不在支出和生产之间共享。</span><span class="sxs-lookup"><span data-stu-id="d0b5d-168">Note that these categories can be shared between Project and Expense or Project and Production, but not between Expense and Production.</span></span> <span data-ttu-id="d0b5d-169">您必须为每个支出类别做出以下决策。</span><span class="sxs-lookup"><span data-stu-id="d0b5d-169">You must make the following decisions for each expense category.</span></span>

<span data-ttu-id="d0b5d-170">**决策：**</span><span class="sxs-lookup"><span data-stu-id="d0b5d-170">**Decisions:**</span></span>

- <span data-ttu-id="d0b5d-171">什么是支出类别？</span><span class="sxs-lookup"><span data-stu-id="d0b5d-171">What is the expense category?</span></span> <span data-ttu-id="d0b5d-172">示例包括航班、酒店或里程类别。</span><span class="sxs-lookup"><span data-stu-id="d0b5d-172">Examples include categories for flights, hotel, or mileage.</span></span>
- <span data-ttu-id="d0b5d-173">支出类别是否还可以用于项目管理和会计？</span><span class="sxs-lookup"><span data-stu-id="d0b5d-173">Can the expense category also be used in Project management and accounting?</span></span>
- <span data-ttu-id="d0b5d-174">什么是支出类型？</span><span class="sxs-lookup"><span data-stu-id="d0b5d-174">What is the expense type?</span></span>
- <span data-ttu-id="d0b5d-175">支出类别的默认付款方式是什么？</span><span class="sxs-lookup"><span data-stu-id="d0b5d-175">What is the default payment method for the expense category?</span></span>
- <span data-ttu-id="d0b5d-176">支出类别中的支出是否必须细化？</span><span class="sxs-lookup"><span data-stu-id="d0b5d-176">Do expenses in the expense category have to be itemized?</span></span>
- <span data-ttu-id="d0b5d-177">支出类别的主要默认科目是什么？</span><span class="sxs-lookup"><span data-stu-id="d0b5d-177">What is the main default account for the expense category?</span></span>
- <span data-ttu-id="d0b5d-178">支出类别的默认项销售税组是什么？</span><span class="sxs-lookup"><span data-stu-id="d0b5d-178">What is the default item sales tax group for the expense category?</span></span>
- <span data-ttu-id="d0b5d-179">是否允许对支出类别使用其他付款方式？</span><span class="sxs-lookup"><span data-stu-id="d0b5d-179">Are additional payment methods allowed for the expense category?</span></span> <span data-ttu-id="d0b5d-180">如果允许其他付款方式，有哪些付款方式？</span><span class="sxs-lookup"><span data-stu-id="d0b5d-180">If additional payment methods are allowed, what are they?</span></span>
- <span data-ttu-id="d0b5d-181">此支出类别是否有子类别？</span><span class="sxs-lookup"><span data-stu-id="d0b5d-181">Are there subcategories in this expense category?</span></span> <span data-ttu-id="d0b5d-182">如果有子类别，您还必须确定以下方面：</span><span class="sxs-lookup"><span data-stu-id="d0b5d-182">If there are subcategories, you must also make the following decisions:</span></span>

    - <span data-ttu-id="d0b5d-183">是否将任何子类别排除在退税之外？</span><span class="sxs-lookup"><span data-stu-id="d0b5d-183">Are any of the subcategories excluded from tax recovery?</span></span>
    - <span data-ttu-id="d0b5d-184">子类别的项目销售税组是什么？</span><span class="sxs-lookup"><span data-stu-id="d0b5d-184">What is the item sales tax group of the subcategories?</span></span>

<span data-ttu-id="d0b5d-185">如果此支出类别还用于项目管理和会计，则回答剩余的问题。</span><span class="sxs-lookup"><span data-stu-id="d0b5d-185">If the expense category is also used in Project management and accounting, answer the remaining questions.</span></span> <span data-ttu-id="d0b5d-186">否则，移至下一部分。</span><span class="sxs-lookup"><span data-stu-id="d0b5d-186">Otherwise, move on to the next section.</span></span>

- <span data-ttu-id="d0b5d-187">哪些成本科目将用于以下支出？</span><span class="sxs-lookup"><span data-stu-id="d0b5d-187">Which cost accounts will be used for the following expenses?</span></span>

    - <span data-ttu-id="d0b5d-188">成本</span><span class="sxs-lookup"><span data-stu-id="d0b5d-188">Cost</span></span>
    - <span data-ttu-id="d0b5d-189">工资分配</span><span class="sxs-lookup"><span data-stu-id="d0b5d-189">Payroll allocation</span></span>
    - <span data-ttu-id="d0b5d-190">WIP-成本值</span><span class="sxs-lookup"><span data-stu-id="d0b5d-190">WIP-cost value</span></span>
    - <span data-ttu-id="d0b5d-191">成本-项</span><span class="sxs-lookup"><span data-stu-id="d0b5d-191">Cost-item</span></span>
    - <span data-ttu-id="d0b5d-192">WIP-成本值-项</span><span class="sxs-lookup"><span data-stu-id="d0b5d-192">WIP-cost value-item</span></span>
    - <span data-ttu-id="d0b5d-193">应计损失</span><span class="sxs-lookup"><span data-stu-id="d0b5d-193">Accrued loss</span></span>
    - <span data-ttu-id="d0b5d-194">WIP-应计损失</span><span class="sxs-lookup"><span data-stu-id="d0b5d-194">WIP-accrued loss</span></span>

- <span data-ttu-id="d0b5d-195">哪些收入科目用于以下各项？</span><span class="sxs-lookup"><span data-stu-id="d0b5d-195">Which revenue accounts will be used for the following?</span></span>

    - <span data-ttu-id="d0b5d-196">已开票收入</span><span class="sxs-lookup"><span data-stu-id="d0b5d-196">Invoiced revenue</span></span>
    - <span data-ttu-id="d0b5d-197">应计收入-销售值</span><span class="sxs-lookup"><span data-stu-id="d0b5d-197">Accrued revenue-sales value</span></span>
    - <span data-ttu-id="d0b5d-198">WIP-销售值</span><span class="sxs-lookup"><span data-stu-id="d0b5d-198">WIP-sales value</span></span>
    - <span data-ttu-id="d0b5d-199">应计收入生产</span><span class="sxs-lookup"><span data-stu-id="d0b5d-199">Accrued revenue-production</span></span>
    - <span data-ttu-id="d0b5d-200">WIP-生产</span><span class="sxs-lookup"><span data-stu-id="d0b5d-200">WIP-production</span></span>
    - <span data-ttu-id="d0b5d-201">应计收入-利润</span><span class="sxs-lookup"><span data-stu-id="d0b5d-201">Accrued revenue-profit</span></span>
    - <span data-ttu-id="d0b5d-202">WIP-利润</span><span class="sxs-lookup"><span data-stu-id="d0b5d-202">WIP-profit</span></span>
    - <span data-ttu-id="d0b5d-203">应计收入-预订</span><span class="sxs-lookup"><span data-stu-id="d0b5d-203">Accrued revenue-subscription</span></span>
    - <span data-ttu-id="d0b5d-204">WIP-预订</span><span class="sxs-lookup"><span data-stu-id="d0b5d-204">WIP-subscription</span></span>

### <a name="taxes"></a><span data-ttu-id="d0b5d-205">税费</span><span class="sxs-lookup"><span data-stu-id="d0b5d-205">Taxes</span></span>

<span data-ttu-id="d0b5d-206">对于支出相关的税，必须确定支出报表上包括或启用什么。</span><span class="sxs-lookup"><span data-stu-id="d0b5d-206">For expense-related taxes, you must determine what is included or enabled on expense reports.</span></span>

<span data-ttu-id="d0b5d-207">**决策：**</span><span class="sxs-lookup"><span data-stu-id="d0b5d-207">**Decisions:**</span></span>

- <span data-ttu-id="d0b5d-208">销售税是否包括在支出金额中？</span><span class="sxs-lookup"><span data-stu-id="d0b5d-208">Is sales tax included in the expense amounts?</span></span>
- <span data-ttu-id="d0b5d-209">是否在支出上启用退税？</span><span class="sxs-lookup"><span data-stu-id="d0b5d-209">Should tax recovery be enabled on expenses?</span></span>

    > [!NOTE]
    > <span data-ttu-id="d0b5d-210">计划总帐时，如果决定应用美国销售税和销项税规则，则无法启用支出退税。</span><span class="sxs-lookup"><span data-stu-id="d0b5d-210">When you were planning the general ledger, if you decided to apply U.S. sales tax and use tax rules, you can’t enable tax recovery on expenses.</span></span> <span data-ttu-id="d0b5d-211">（若要应用美国销售税和采用销项税规则，则将 **应用销售税税务规则** 选项设置为 **是** 。）</span><span class="sxs-lookup"><span data-stu-id="d0b5d-211">(To apply U.S. sales tax and use tax rules, set the **Apply sales tax taxations rules** option to **Yes**.)</span></span>

## <a name="policies"></a><span data-ttu-id="d0b5d-212">策略</span><span class="sxs-lookup"><span data-stu-id="d0b5d-212">Policies</span></span>

<span data-ttu-id="d0b5d-213">通过创建支出报表策略，当员工代表您的组织产生支出时，您可以帮助您的组织节省时间和金钱。</span><span class="sxs-lookup"><span data-stu-id="d0b5d-213">By creating expense report policies, you can help your organization save time and money when employees incur expenses on its behalf.</span></span> <span data-ttu-id="d0b5d-214">策略有助于保证员工保持在预算中，提供所有必需的信息，并且只在需要时花钱。</span><span class="sxs-lookup"><span data-stu-id="d0b5d-214">Policies help guarantee that employees stay in budget, provide all required information, and spend money only as they require it.</span></span> <span data-ttu-id="d0b5d-215">您必须为您创建的每个支出报表策略和每个支出报表审核策略做出以下决策。</span><span class="sxs-lookup"><span data-stu-id="d0b5d-215">You must make the following decisions for each expense report policy and each expense report approval policy that you create.</span></span>

<span data-ttu-id="d0b5d-216">**决策：**</span><span class="sxs-lookup"><span data-stu-id="d0b5d-216">**Decisions:**</span></span>

- <span data-ttu-id="d0b5d-217">策略的名称是什么？</span><span class="sxs-lookup"><span data-stu-id="d0b5d-217">What is the name of the policy?</span></span>
- <span data-ttu-id="d0b5d-218">支出策略的目的是什么？</span><span class="sxs-lookup"><span data-stu-id="d0b5d-218">What is the expense policy for?</span></span>
- <span data-ttu-id="d0b5d-219">如果您已经决定启用内部公司支出，则此策略将应用于您组织中的哪个公司？</span><span class="sxs-lookup"><span data-stu-id="d0b5d-219">If you previously decided to enable intercompany expenses, which companies in your organization will this policy apply to?</span></span>
- <span data-ttu-id="d0b5d-220">策略什么时候生效？</span><span class="sxs-lookup"><span data-stu-id="d0b5d-220">When does the policy become effective?</span></span>
- <span data-ttu-id="d0b5d-221">策略什么时候到期？</span><span class="sxs-lookup"><span data-stu-id="d0b5d-221">When does the policy expire?</span></span>
- <span data-ttu-id="d0b5d-222">策略规则是什么？</span><span class="sxs-lookup"><span data-stu-id="d0b5d-222">What is the policy rule?</span></span>
- <span data-ttu-id="d0b5d-223">策略规则的结果是什么？</span><span class="sxs-lookup"><span data-stu-id="d0b5d-223">What is the outcome of the policy rule?</span></span>