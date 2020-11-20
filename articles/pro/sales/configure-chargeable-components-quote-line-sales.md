---
title: 配置报价单明细的应计费组件
description: 此主题提供有关在基于项目的报价单明细上设置应计费和非应计费组件的信息。
author: rumant
manager: Annbe
ms.date: 10/13/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: e0b64d7edb21df127bf7544f044de7f3c496dfe3
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/16/2020
ms.locfileid: "4072725"
---
# <a name="configure-the-chargeable-components-of-a-quote-line"></a><span data-ttu-id="881cc-103">配置报价单明细的应计费组件</span><span class="sxs-lookup"><span data-stu-id="881cc-103">Configure the chargeable components of a quote line</span></span>

<span data-ttu-id="881cc-104">_**适用于：** 精简部署 - 估价交易开票_</span><span class="sxs-lookup"><span data-stu-id="881cc-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="881cc-105">基于项目的报价单明细具有 *包含* 组件和 *应计费* 组件概念。</span><span class="sxs-lookup"><span data-stu-id="881cc-105">A project-based quote line has the concept of *included* components and *chargeable* components.</span></span>

<span data-ttu-id="881cc-106">包含组件受以下各项约束：</span><span class="sxs-lookup"><span data-stu-id="881cc-106">Included components are subject to:</span></span>

  - <span data-ttu-id="881cc-107">计费方法和客户拆分</span><span class="sxs-lookup"><span data-stu-id="881cc-107">Billing method and customer splits</span></span>
  - <span data-ttu-id="881cc-108">上限</span><span class="sxs-lookup"><span data-stu-id="881cc-108">Not-to-exceed limits</span></span> 
  - <span data-ttu-id="881cc-109">基于项目的报价单明细中定义的发票频率设置</span><span class="sxs-lookup"><span data-stu-id="881cc-109">Invoice frequency settings defined on the project-based quote line</span></span>

<span data-ttu-id="881cc-110">包含组件的子集可以使用 **记帐类型** 字段标记为应计费。</span><span class="sxs-lookup"><span data-stu-id="881cc-110">A subset of the included components can be marked as chargeable using the **Billing Type** field.</span></span> <span data-ttu-id="881cc-111">**记帐类型** 字段是一个选项集，允许在报价单明细的上下文中使用以下值：</span><span class="sxs-lookup"><span data-stu-id="881cc-111">The **Billing Type** field is an option-set that allows the following values in the context of a quote line:</span></span>

  - <span data-ttu-id="881cc-112">应计费</span><span class="sxs-lookup"><span data-stu-id="881cc-112">Chargeable</span></span>
  - <span data-ttu-id="881cc-113">非应计费</span><span class="sxs-lookup"><span data-stu-id="881cc-113">Non-chargeable</span></span>

<span data-ttu-id="881cc-114">应计费组件可以在任务、角色和交易类别中定义。</span><span class="sxs-lookup"><span data-stu-id="881cc-114">Chargeable components can be defined on tasks, roles, and transaction categories.</span></span>

<span data-ttu-id="881cc-115">应计费在报价单明细的任务中定义，应用于该报价单明细中包括的所有交易类。</span><span class="sxs-lookup"><span data-stu-id="881cc-115">Chargeability is defined on the tasks for a quote line and applies to all transaction classes included on that line.</span></span> <span data-ttu-id="881cc-116">如果 **包含任务** 字段设置为 **整个项目** 或留空， **应计费任务** 选项卡将不可用。</span><span class="sxs-lookup"><span data-stu-id="881cc-116">If the **Include Tasks** field is set to **Entire project** or left blank, the **Chargeable Tasks** tab isn't available.</span></span>

<span data-ttu-id="881cc-117">应计费在报价单明细的角色中定义，仅应用于 **时间** 交易类。</span><span class="sxs-lookup"><span data-stu-id="881cc-117">Chargeability is defined on roles for a quote line and only applies to the **Time** transaction class.</span></span> <span data-ttu-id="881cc-118">如果 **包含时间** 字段在项目报价单明细中设置为 **否** ， **应计费角色** 选项卡将不可用。</span><span class="sxs-lookup"><span data-stu-id="881cc-118">If the field, **Include Time** is set to **No** on a project quote line, the **Chargeable Roles** tab isn't available.</span></span>

<span data-ttu-id="881cc-119">应计费在报价单明细的交易类别中定义，仅应用于 **支出** 交易类。</span><span class="sxs-lookup"><span data-stu-id="881cc-119">Chargeability is defined on transaction categories for a  quote line and only applies to the **Expense** transaction class.</span></span> <span data-ttu-id="881cc-120">如果 **包含支出** 字段在项目报价单明细中设置为 **否** ， **应计费类别** 选项卡将不可用。</span><span class="sxs-lookup"><span data-stu-id="881cc-120">If the field, **Include Expenses** is set to **No** on a project quote line, the **Chargeable Categories** tab isn't available.</span></span>

### <a name="update-a-project-task-to-be-chargeable-or-non-chargeable"></a><span data-ttu-id="881cc-121">将项目任务更新为应计费或非应计费</span><span class="sxs-lookup"><span data-stu-id="881cc-121">Update a project task to be chargeable or non-chargeable</span></span>

<span data-ttu-id="881cc-122">项目任务在特定的基于项目的报价单明细的上下文中可以是应计费或非应计费，这样可以进行以下设置：</span><span class="sxs-lookup"><span data-stu-id="881cc-122">A project task can be chargeable or non-chargeable in the context of a specific project-based quote line, which makes the following setup possible:</span></span>

<span data-ttu-id="881cc-123">如果基于项目的报价单明细包含 **时间** 和任务 **T1** ，该任务将作为应计费与报价单明细关联。</span><span class="sxs-lookup"><span data-stu-id="881cc-123">If a project-based quote line includes **Time** and the task **T1** , the task is associated to the quote line as chargeable.</span></span> <span data-ttu-id="881cc-124">如果有另一个包含 **支出** 的报价单明细，您可以将该报价单明细上的 **T1** 任务作为非应计费关联。</span><span class="sxs-lookup"><span data-stu-id="881cc-124">If there is a second quote line that includes **Expenses** , you can associate the **T1** task on the quote line as non-chargeable.</span></span> <span data-ttu-id="881cc-125">结果是，任务中记录的所有时间都为应计费，任务中记录的所有支出都为非应计费。</span><span class="sxs-lookup"><span data-stu-id="881cc-125">The result is that all time recorded on the task is chargeable and all expenses recorded on the task are non-chargeable.</span></span>

<span data-ttu-id="881cc-126">任务的计费类型可以通过更新 **报价单明细任务** 子网格上的 **记帐类型** 字段在基于项目的报价单明细的 **应计费任务** 选项卡上配置。</span><span class="sxs-lookup"><span data-stu-id="881cc-126">A task's billing type can be configured on the **Chargeable Tasks** tab of a project-based quote line by updating the **Billing Type** field on the **Quote Line Tasks** sub-grid.</span></span> <span data-ttu-id="881cc-127">或者，您可以在项目的任务计费设置中子网格上的 **记帐类型** 字段中更新项目任务的计费类型，该字段显示与任务关联的报价单明细。</span><span class="sxs-lookup"><span data-stu-id="881cc-127">Alternatively, you can update the billing type for a project task in the **Billing Type** field on the sub-grid on the task billing setup of a project that shows the quote lines associated to a task.</span></span>

### <a name="update-a-role-to-be-chargeable-or-non-chargeable"></a><span data-ttu-id="881cc-128">将角色更新为应计费或非应计费</span><span class="sxs-lookup"><span data-stu-id="881cc-128">Update a role to be chargeable or non-chargeable</span></span>

<span data-ttu-id="881cc-129">角色在特定的基于项目的报价单明细的上下文中可以为应计费或非应计费。</span><span class="sxs-lookup"><span data-stu-id="881cc-129">A role can be chargeable or non-chargeable in the context of a specific project-based quote line.</span></span>

<span data-ttu-id="881cc-130">角色的计费类型可以通过更新 **应计费角色** 子网格上的 **记帐类型** 字段在报价单明细的 **应计费角色** 选项卡上配置。</span><span class="sxs-lookup"><span data-stu-id="881cc-130">A role's billing type can be configured on the **Chargeable Roles** tab of a quote line by updating the **Billing Type** field on the **Chargeable Roles** sub-grid.</span></span>

### <a name="update-a-transaction-category-to-be-chargeable-or-non-chargeable"></a><span data-ttu-id="881cc-131">将交易类别更新为应计费或非应计费</span><span class="sxs-lookup"><span data-stu-id="881cc-131">Update a transaction category to be chargeable or non-chargeable</span></span>

<span data-ttu-id="881cc-132">交易类别在特定报价单明细中可以为应计费或非应计费。</span><span class="sxs-lookup"><span data-stu-id="881cc-132">A transaction category can be chargeable or non-chargeable on a specific quote line.</span></span>

<span data-ttu-id="881cc-133">交易的计费类型可以通过更新 **应计费类别** 子网格上的 **记帐类型** 字段在报价单明细的 **应计费类别** 选项卡上配置。</span><span class="sxs-lookup"><span data-stu-id="881cc-133">A transaction's billing type can be configured on the **Chargeable Categories** tab of a quote line by updating the **Billing Type** field on the **Chargeable Categories** sub-grid.</span></span>

### <a name="resolve-chargeability"></a><span data-ttu-id="881cc-134">解析应计费</span><span class="sxs-lookup"><span data-stu-id="881cc-134">Resolve chargeability</span></span>
<span data-ttu-id="881cc-135">仅在报价单明细中包含 **时间** 且 **任务** 和 **角色** 在报价单明细中配置为应计费时，为时间创建的估计值或实际值才会被视为应计费。</span><span class="sxs-lookup"><span data-stu-id="881cc-135">An estimate or actual created for time will only be considered chargeable if **Time** is included on the quote line, and if **Task** and **Role** are configured as chargeable on the quote line.</span></span>

<span data-ttu-id="881cc-136">仅在报价单明细中包含 **支出** 且 **任务** 和 **交易类别** 在报价单明细中配置为应计费时，为支出创建的估计值或实际值才会被视为应计费。</span><span class="sxs-lookup"><span data-stu-id="881cc-136">An estimate or actual created for expense will only be considered chargeable if **Expense** is included on the quote line, and if **Task** and **Transaction Category** are configured as chargeable on the quote line.</span></span>

| <span data-ttu-id="881cc-137">包括时间</span><span class="sxs-lookup"><span data-stu-id="881cc-137">Includes Time</span></span> | <span data-ttu-id="881cc-138">包括支出</span><span class="sxs-lookup"><span data-stu-id="881cc-138">Includes Expense</span></span> | <span data-ttu-id="881cc-139">包含的任务</span><span class="sxs-lookup"><span data-stu-id="881cc-139">Included Tasks</span></span> | <span data-ttu-id="881cc-140">角色</span><span class="sxs-lookup"><span data-stu-id="881cc-140">Role</span></span> | <span data-ttu-id="881cc-141">类别</span><span class="sxs-lookup"><span data-stu-id="881cc-141">Category</span></span> | <span data-ttu-id="881cc-142">任务</span><span class="sxs-lookup"><span data-stu-id="881cc-142">Task</span></span> | <span data-ttu-id="881cc-143">记帐</span><span class="sxs-lookup"><span data-stu-id="881cc-143">Billing</span></span> |
| --- | --- | --- | --- | --- | --- | --- |
| <span data-ttu-id="881cc-144">是</span><span class="sxs-lookup"><span data-stu-id="881cc-144">Yes</span></span> | <span data-ttu-id="881cc-145">是</span><span class="sxs-lookup"><span data-stu-id="881cc-145">Yes</span></span> | <span data-ttu-id="881cc-146">整个项目</span><span class="sxs-lookup"><span data-stu-id="881cc-146">Entire project</span></span> | <span data-ttu-id="881cc-147">应计费</span><span class="sxs-lookup"><span data-stu-id="881cc-147">Chargeable</span></span> | <span data-ttu-id="881cc-148">应计费</span><span class="sxs-lookup"><span data-stu-id="881cc-148">Chargeable</span></span> | <span data-ttu-id="881cc-149">无法设置</span><span class="sxs-lookup"><span data-stu-id="881cc-149">Can't be set</span></span> | <span data-ttu-id="881cc-150">时间实际值的计费：应计费</span><span class="sxs-lookup"><span data-stu-id="881cc-150">Billing on a time actual: Chargeable</span></span> </br><span data-ttu-id="881cc-151">支出实际值的计费：应计费</span><span class="sxs-lookup"><span data-stu-id="881cc-151">Billing type on expense actual: Chargeable</span></span> |
| <span data-ttu-id="881cc-152">是</span><span class="sxs-lookup"><span data-stu-id="881cc-152">Yes</span></span> | <span data-ttu-id="881cc-153">是</span><span class="sxs-lookup"><span data-stu-id="881cc-153">Yes</span></span> | <span data-ttu-id="881cc-154">仅所选任务</span><span class="sxs-lookup"><span data-stu-id="881cc-154">Selected tasks only</span></span> | <span data-ttu-id="881cc-155">应计费</span><span class="sxs-lookup"><span data-stu-id="881cc-155">Chargeable</span></span> | <span data-ttu-id="881cc-156">应计费</span><span class="sxs-lookup"><span data-stu-id="881cc-156">Chargeable</span></span> | <span data-ttu-id="881cc-157">应计费</span><span class="sxs-lookup"><span data-stu-id="881cc-157">Chargeable</span></span> | <span data-ttu-id="881cc-158">时间实际值的计费：应计费</span><span class="sxs-lookup"><span data-stu-id="881cc-158">Billing on a time actual: Chargeable</span></span></br><span data-ttu-id="881cc-159">支出实际值的计费：应计费</span><span class="sxs-lookup"><span data-stu-id="881cc-159">Billing type on expense actual: Chargeable</span></span> |
| <span data-ttu-id="881cc-160">是</span><span class="sxs-lookup"><span data-stu-id="881cc-160">Yes</span></span> | <span data-ttu-id="881cc-161">是</span><span class="sxs-lookup"><span data-stu-id="881cc-161">Yes</span></span> | <span data-ttu-id="881cc-162">仅所选任务</span><span class="sxs-lookup"><span data-stu-id="881cc-162">Selected tasks only</span></span> | <span data-ttu-id="881cc-163">非应计费</span><span class="sxs-lookup"><span data-stu-id="881cc-163">Non-chargeable</span></span> | <span data-ttu-id="881cc-164">应计费</span><span class="sxs-lookup"><span data-stu-id="881cc-164">Chargeable</span></span> | <span data-ttu-id="881cc-165">应计费</span><span class="sxs-lookup"><span data-stu-id="881cc-165">Chargeable</span></span> | <span data-ttu-id="881cc-166">时间实际值的计费：非应计费</span><span class="sxs-lookup"><span data-stu-id="881cc-166">Billing on a time actual: Non-Chargeable</span></span></br><span data-ttu-id="881cc-167">支出实际值的计费：应计费</span><span class="sxs-lookup"><span data-stu-id="881cc-167">Billing type on expense actual: Chargeable</span></span> |
| <span data-ttu-id="881cc-168">是</span><span class="sxs-lookup"><span data-stu-id="881cc-168">Yes</span></span> | <span data-ttu-id="881cc-169">是</span><span class="sxs-lookup"><span data-stu-id="881cc-169">Yes</span></span> | <span data-ttu-id="881cc-170">仅所选任务</span><span class="sxs-lookup"><span data-stu-id="881cc-170">Selected tasks only</span></span> | <span data-ttu-id="881cc-171">应计费</span><span class="sxs-lookup"><span data-stu-id="881cc-171">Chargeable</span></span> | <span data-ttu-id="881cc-172">应计费</span><span class="sxs-lookup"><span data-stu-id="881cc-172">Chargeable</span></span> | <span data-ttu-id="881cc-173">非应计费</span><span class="sxs-lookup"><span data-stu-id="881cc-173">Non-Chargeable</span></span> | <span data-ttu-id="881cc-174">时间实际值的计费：非应计费</span><span class="sxs-lookup"><span data-stu-id="881cc-174">Billing on a time actual: Non-Chargeable</span></span></br> <span data-ttu-id="881cc-175">支出实际值的计费：非应计费</span><span class="sxs-lookup"><span data-stu-id="881cc-175">Billing type on expense actual: Non-Chargeable</span></span> |
| <span data-ttu-id="881cc-176">是</span><span class="sxs-lookup"><span data-stu-id="881cc-176">Yes</span></span> | <span data-ttu-id="881cc-177">是</span><span class="sxs-lookup"><span data-stu-id="881cc-177">Yes</span></span> | <span data-ttu-id="881cc-178">仅所选任务</span><span class="sxs-lookup"><span data-stu-id="881cc-178">Selected tasks only</span></span> | <span data-ttu-id="881cc-179">非应计费</span><span class="sxs-lookup"><span data-stu-id="881cc-179">Non-Chargeable</span></span> | <span data-ttu-id="881cc-180">应计费</span><span class="sxs-lookup"><span data-stu-id="881cc-180">Chargeable</span></span> | <span data-ttu-id="881cc-181">非应计费</span><span class="sxs-lookup"><span data-stu-id="881cc-181">Non- Chargeable</span></span> | <span data-ttu-id="881cc-182">时间实际值的计费：非应计费</span><span class="sxs-lookup"><span data-stu-id="881cc-182">Billing on a time actual: Non-Chargeable</span></span></br> <span data-ttu-id="881cc-183">支出实际值的计费：非应计费</span><span class="sxs-lookup"><span data-stu-id="881cc-183">Billing type on expense actual: Non-Chargeable</span></span> |
| <span data-ttu-id="881cc-184">是</span><span class="sxs-lookup"><span data-stu-id="881cc-184">Yes</span></span> | <span data-ttu-id="881cc-185">是</span><span class="sxs-lookup"><span data-stu-id="881cc-185">Yes</span></span> | <span data-ttu-id="881cc-186">仅所选任务</span><span class="sxs-lookup"><span data-stu-id="881cc-186">Selected tasks only</span></span> | <span data-ttu-id="881cc-187">非应计费</span><span class="sxs-lookup"><span data-stu-id="881cc-187">Non-Chargeable</span></span> | <span data-ttu-id="881cc-188">非应计费</span><span class="sxs-lookup"><span data-stu-id="881cc-188">Non-Chargeable</span></span> | <span data-ttu-id="881cc-189">应计费</span><span class="sxs-lookup"><span data-stu-id="881cc-189">Chargeable</span></span> | <span data-ttu-id="881cc-190">时间实际值的计费：非应计费</span><span class="sxs-lookup"><span data-stu-id="881cc-190">Billing on a time actual: Non-Chargeable</span></span></br> <span data-ttu-id="881cc-191">支出实际值的计费：非应计费</span><span class="sxs-lookup"><span data-stu-id="881cc-191">Billing type on expense actual: Non-Chargeable</span></span> |
| <span data-ttu-id="881cc-192">No</span><span class="sxs-lookup"><span data-stu-id="881cc-192">No</span></span> | <span data-ttu-id="881cc-193">是</span><span class="sxs-lookup"><span data-stu-id="881cc-193">Yes</span></span> | <span data-ttu-id="881cc-194">整个项目</span><span class="sxs-lookup"><span data-stu-id="881cc-194">Entire project</span></span> | <span data-ttu-id="881cc-195">无法设置</span><span class="sxs-lookup"><span data-stu-id="881cc-195">Can't be set</span></span> | <span data-ttu-id="881cc-196">应计费</span><span class="sxs-lookup"><span data-stu-id="881cc-196">Chargeable</span></span> | <span data-ttu-id="881cc-197">无法设置</span><span class="sxs-lookup"><span data-stu-id="881cc-197">Can't be set</span></span> | <span data-ttu-id="881cc-198">时间实际值的计费：不可用</span><span class="sxs-lookup"><span data-stu-id="881cc-198">Billing on a time actual: Not available</span></span> </br><span data-ttu-id="881cc-199">支出实际值的计费：应计费</span><span class="sxs-lookup"><span data-stu-id="881cc-199">Billing type on expense actual: Chargeable</span></span> |
| <span data-ttu-id="881cc-200">No</span><span class="sxs-lookup"><span data-stu-id="881cc-200">No</span></span> | <span data-ttu-id="881cc-201">是</span><span class="sxs-lookup"><span data-stu-id="881cc-201">Yes</span></span> | <span data-ttu-id="881cc-202">整个项目</span><span class="sxs-lookup"><span data-stu-id="881cc-202">Entire project</span></span> | <span data-ttu-id="881cc-203">无法设置</span><span class="sxs-lookup"><span data-stu-id="881cc-203">Can't be set</span></span> | <span data-ttu-id="881cc-204">非应计费</span><span class="sxs-lookup"><span data-stu-id="881cc-204">Non-chargeable</span></span> | <span data-ttu-id="881cc-205">无法设置</span><span class="sxs-lookup"><span data-stu-id="881cc-205">Can't be set</span></span> | <span data-ttu-id="881cc-206">时间实际值的计费：不可用</span><span class="sxs-lookup"><span data-stu-id="881cc-206">Billing on a time actual: Not available</span></span> </br><span data-ttu-id="881cc-207">支出实际值的计费：非应计费</span><span class="sxs-lookup"><span data-stu-id="881cc-207">Billing type on expense actual: Non-chargeable</span></span> |
| <span data-ttu-id="881cc-208">是</span><span class="sxs-lookup"><span data-stu-id="881cc-208">Yes</span></span> | <span data-ttu-id="881cc-209">No</span><span class="sxs-lookup"><span data-stu-id="881cc-209">No</span></span> | <span data-ttu-id="881cc-210">整个项目</span><span class="sxs-lookup"><span data-stu-id="881cc-210">Entire project</span></span> | <span data-ttu-id="881cc-211">应计费</span><span class="sxs-lookup"><span data-stu-id="881cc-211">Chargeable</span></span> | <span data-ttu-id="881cc-212">无法设置</span><span class="sxs-lookup"><span data-stu-id="881cc-212">Can't be set</span></span> | <span data-ttu-id="881cc-213">无法设置</span><span class="sxs-lookup"><span data-stu-id="881cc-213">Can't be set</span></span> | <span data-ttu-id="881cc-214">时间实际值的计费：应计费</span><span class="sxs-lookup"><span data-stu-id="881cc-214">Billing on a time actual: Chargeable</span></span></br><span data-ttu-id="881cc-215">支出实际值的计费：不可用</span><span class="sxs-lookup"><span data-stu-id="881cc-215">Billing type on expense actual: Not available</span></span> |
| <span data-ttu-id="881cc-216">是</span><span class="sxs-lookup"><span data-stu-id="881cc-216">Yes</span></span> | <span data-ttu-id="881cc-217">No</span><span class="sxs-lookup"><span data-stu-id="881cc-217">No</span></span> | <span data-ttu-id="881cc-218">整个项目</span><span class="sxs-lookup"><span data-stu-id="881cc-218">Entire project</span></span> | <span data-ttu-id="881cc-219">非应计费</span><span class="sxs-lookup"><span data-stu-id="881cc-219">Non-chargeable</span></span> | <span data-ttu-id="881cc-220">无法设置</span><span class="sxs-lookup"><span data-stu-id="881cc-220">Can't be set</span></span> | <span data-ttu-id="881cc-221">无法设置</span><span class="sxs-lookup"><span data-stu-id="881cc-221">Can't be set</span></span> | <span data-ttu-id="881cc-222">时间实际值的计费：非应计费</span><span class="sxs-lookup"><span data-stu-id="881cc-222">Billing on a time actual: Non-chargeable</span></span> </br><span data-ttu-id="881cc-223">支出实际值的计费：不可用</span><span class="sxs-lookup"><span data-stu-id="881cc-223">Billing type on expense actual: Not available</span></span> |