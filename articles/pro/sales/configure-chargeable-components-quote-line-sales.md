---
title: 配置报价单明细的应计费组件
description: 此主题提供有关在基于项目的报价单明细上设置应计费和非应计费组件的信息。
author: rumant
manager: Annbe
ms.date: 03/30/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 1a9e1851bd8c5a4070df2774c945d1f3eabaaa8a
ms.sourcegitcommit: 5fd529f2308edfe9322082313e6d50146df56aca
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/06/2021
ms.locfileid: "5858282"
---
# <a name="configure-the-chargeable-components-of-a-quote-line"></a><span data-ttu-id="040ef-103">配置报价单明细的应计费组件</span><span class="sxs-lookup"><span data-stu-id="040ef-103">Configure the chargeable components of a quote line</span></span> 

<span data-ttu-id="040ef-104">_**适用于：** 精简部署 - 估价交易开单，基于资源/非库存场景的 Project Operations_</span><span class="sxs-lookup"><span data-stu-id="040ef-104">_**Applies To:** Lite deployment - deal to proforma invoicing, Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="040ef-105">基于项目的报价单明细具有 *包含* 组件和 *应计费* 组件概念。</span><span class="sxs-lookup"><span data-stu-id="040ef-105">A project-based quote line has the concept of *included* components and *chargeable* components.</span></span>

<span data-ttu-id="040ef-106">包含组件受以下各项约束：</span><span class="sxs-lookup"><span data-stu-id="040ef-106">Included components are subject to:</span></span>

  - <span data-ttu-id="040ef-107">计费方法和客户拆分</span><span class="sxs-lookup"><span data-stu-id="040ef-107">Billing method and customer splits</span></span>
  - <span data-ttu-id="040ef-108">上限</span><span class="sxs-lookup"><span data-stu-id="040ef-108">Not-to-exceed limits</span></span> 
  - <span data-ttu-id="040ef-109">基于项目的报价单明细中定义的发票频率设置</span><span class="sxs-lookup"><span data-stu-id="040ef-109">Invoice frequency settings defined on the project-based quote line</span></span>

<span data-ttu-id="040ef-110">包含组件的子集可以使用 **记帐类型** 字段标记为应计费。</span><span class="sxs-lookup"><span data-stu-id="040ef-110">A subset of the included components can be marked as chargeable using the **Billing Type** field.</span></span> <span data-ttu-id="040ef-111">**记帐类型** 字段是一个选项集，允许在报价单明细的上下文中使用以下值：</span><span class="sxs-lookup"><span data-stu-id="040ef-111">The **Billing Type** field is an option-set that allows the following values in the context of a quote line:</span></span>

  - <span data-ttu-id="040ef-112">应计费</span><span class="sxs-lookup"><span data-stu-id="040ef-112">Chargeable</span></span>
  - <span data-ttu-id="040ef-113">非应计费</span><span class="sxs-lookup"><span data-stu-id="040ef-113">Non-chargeable</span></span>

<span data-ttu-id="040ef-114">应计费组件可以在任务、角色和交易类别中定义。</span><span class="sxs-lookup"><span data-stu-id="040ef-114">Chargeable components can be defined on tasks, roles, and transaction categories.</span></span>

<span data-ttu-id="040ef-115">应计费在报价单明细的任务中定义，应用于该报价单明细中包括的所有交易类。</span><span class="sxs-lookup"><span data-stu-id="040ef-115">Chargeability is defined on the tasks for a quote line and applies to all transaction classes included on that line.</span></span> <span data-ttu-id="040ef-116">如果 **包含任务** 字段设置为 **整个项目** 或留空，**应计费任务** 选项卡将不可用。</span><span class="sxs-lookup"><span data-stu-id="040ef-116">If the **Include Tasks** field is set to **Entire project** or left blank, the **Chargeable Tasks** tab isn't available.</span></span>

<span data-ttu-id="040ef-117">应计费在报价单明细的角色中定义，仅应用于 **时间** 交易类。</span><span class="sxs-lookup"><span data-stu-id="040ef-117">Chargeability is defined on roles for a quote line and only applies to the **Time** transaction class.</span></span> <span data-ttu-id="040ef-118">如果 **包含时间** 字段在项目报价单明细中设置为 **否**，**应计费角色** 选项卡将不可用。</span><span class="sxs-lookup"><span data-stu-id="040ef-118">If the field, **Include Time** is set to **No** on a project quote line, the **Chargeable Roles** tab isn't available.</span></span>

<span data-ttu-id="040ef-119">应计费在报价单明细的交易类别中定义，仅应用于 **支出** 交易类。</span><span class="sxs-lookup"><span data-stu-id="040ef-119">Chargeability is defined on transaction categories for a  quote line and only applies to the **Expense** transaction class.</span></span> <span data-ttu-id="040ef-120">如果 **包含支出** 字段在项目报价单明细中设置为 **否**，**应计费类别** 选项卡将不可用。</span><span class="sxs-lookup"><span data-stu-id="040ef-120">If the field, **Include Expenses** is set to **No** on a project quote line, the **Chargeable Categories** tab isn't available.</span></span>

### <a name="update-a-project-task-to-be-chargeable-or-non-chargeable"></a><span data-ttu-id="040ef-121">将项目任务更新为应计费或非应计费</span><span class="sxs-lookup"><span data-stu-id="040ef-121">Update a project task to be chargeable or non-chargeable</span></span>

<span data-ttu-id="040ef-122">项目任务在特定的基于项目的报价单明细的上下文中可以是应计费或非应计费，这样可以进行以下设置。</span><span class="sxs-lookup"><span data-stu-id="040ef-122">A project task can be chargeable or non-chargeable in the context of a specific project-based quote line, which makes the following setup possible.</span></span>

<span data-ttu-id="040ef-123">如果基于项目的报价单明细包含 **时间** 和任务 **T1**，该任务将作为应计费与报价单明细关联。</span><span class="sxs-lookup"><span data-stu-id="040ef-123">If a project-based quote line includes **Time** and the task **T1**, the task is associated to the quote line as chargeable.</span></span> <span data-ttu-id="040ef-124">如果有另一个包含 **支出** 的报价单明细，您可以将该报价单明细上的 **T1** 任务作为非应计费关联。</span><span class="sxs-lookup"><span data-stu-id="040ef-124">If there is a second quote line that includes **Expenses**, you can associate the **T1** task on the quote line as non-chargeable.</span></span> <span data-ttu-id="040ef-125">结果是，任务中记录的所有时间都为应计费，任务中记录的所有支出都为非应计费。</span><span class="sxs-lookup"><span data-stu-id="040ef-125">The result is that all time recorded on the task is chargeable and all expenses recorded on the task are non-chargeable.</span></span>

<span data-ttu-id="040ef-126">任务的计费类型可以通过更新 **报价单明细任务** 子网格上的 **计费类型** 字段在基于项目的报价单明细的 **应计费任务** 选项卡上配置。</span><span class="sxs-lookup"><span data-stu-id="040ef-126">A task's billing type can be configured on the **Chargeable Tasks** tab of a project-based quote line by updating the **Billing Type** field on the **Quote Line Tasks** subgrid.</span></span> <span data-ttu-id="040ef-127">或者，您可以更新显示与任务关联的报价单明细的项目任务计费设置中，子网格上 **计费类型** 字段中项目任务的计费类型。</span><span class="sxs-lookup"><span data-stu-id="040ef-127">Alternatively, you can update the billing type for a project task in the **Billing Type** field on the subgrid on the task billing setup of a project that shows the quote lines associated to a task.</span></span>

### <a name="update-a-role-to-be-chargeable-or-non-chargeable"></a><span data-ttu-id="040ef-128">将角色更新为应计费或非应计费</span><span class="sxs-lookup"><span data-stu-id="040ef-128">Update a role to be chargeable or non-chargeable</span></span>

<span data-ttu-id="040ef-129">角色在特定的基于项目的报价单明细的上下文中可以为应计费或非应计费。</span><span class="sxs-lookup"><span data-stu-id="040ef-129">A role can be chargeable or non-chargeable in the context of a specific project-based quote line.</span></span>

<span data-ttu-id="040ef-130">角色的计费类型可以通过更新 **应计费角色** 子网格上的 **计费类型** 字段在报价单明细的 **应计费角色** 选项卡上配置。</span><span class="sxs-lookup"><span data-stu-id="040ef-130">A role's billing type can be configured on the **Chargeable Roles** tab of a quote line by updating the **Billing Type** field on the **Chargeable Roles** subgrid.</span></span>

### <a name="update-a-transaction-category-to-be-chargeable-or-non-chargeable"></a><span data-ttu-id="040ef-131">将交易类别更新为应计费或非应计费</span><span class="sxs-lookup"><span data-stu-id="040ef-131">Update a transaction category to be chargeable or non-chargeable</span></span>

<span data-ttu-id="040ef-132">交易类别在特定报价单明细中可以为应计费或非应计费。</span><span class="sxs-lookup"><span data-stu-id="040ef-132">A transaction category can be chargeable or non-chargeable on a specific quote line.</span></span>

<span data-ttu-id="040ef-133">交易的计费类型可以通过更新 **应计费类别** 子网格上的 **计费类型** 字段在报价单明细的 **应计费类别** 选项卡上配置。</span><span class="sxs-lookup"><span data-stu-id="040ef-133">A transaction's billing type can be configured on the **Chargeable Categories** tab of a quote line by updating the **Billing Type** field on the **Chargeable Categories** subgrid.</span></span>

### <a name="resolve-chargeability"></a><span data-ttu-id="040ef-134">解析应计费</span><span class="sxs-lookup"><span data-stu-id="040ef-134">Resolve chargeability</span></span>
<span data-ttu-id="040ef-135">仅在以下情况下才会将为时间创建的估算或实际值视为应计费：</span><span class="sxs-lookup"><span data-stu-id="040ef-135">An estimate or actual created for time will only be considered chargeable if:</span></span>

   - <span data-ttu-id="040ef-136">报价单明细中包含 **时间**。</span><span class="sxs-lookup"><span data-stu-id="040ef-136">**Time** is included on the quote line.</span></span>
   - <span data-ttu-id="040ef-137">在报价单明细上将 **角色** 配置为应计费。</span><span class="sxs-lookup"><span data-stu-id="040ef-137">**Role** is configured as chargeable on the quote line.</span></span>
   - <span data-ttu-id="040ef-138">在报价单明细上将 **包括的任务** 设置为 **选定任务**。</span><span class="sxs-lookup"><span data-stu-id="040ef-138">**Included Tasks** is set to **Selected tasks** on the quote line.</span></span> 

<span data-ttu-id="040ef-139">如果这三种情况属实，则还会将 **任务** 配置为应计费。</span><span class="sxs-lookup"><span data-stu-id="040ef-139">If these three things are true, the **Task** is also configured as chargeable.</span></span> 

<span data-ttu-id="040ef-140">仅在以下情况下才会将为支出创建的估算或实际值视为应计费：</span><span class="sxs-lookup"><span data-stu-id="040ef-140">An estimate or actual created for expense is only considered chargeable if:</span></span> 

   - <span data-ttu-id="040ef-141">报价单明细中包含 **支出**。</span><span class="sxs-lookup"><span data-stu-id="040ef-141">**Expense** is included on the quote line.</span></span>
   - <span data-ttu-id="040ef-142">在报价单明细上将 **交易类别** 配置为应计费。</span><span class="sxs-lookup"><span data-stu-id="040ef-142">**Transaction category** is configured as chargeable on the quote line.</span></span>
   - <span data-ttu-id="040ef-143">在报价单明细上将 **包括的任务** 设置为 **选定任务**。</span><span class="sxs-lookup"><span data-stu-id="040ef-143">**Included Tasks** is set to **Selected tasks** on the quote line.</span></span>

<span data-ttu-id="040ef-144">如果这三种情况属实，则还会将 **任务** 配置为应计费。</span><span class="sxs-lookup"><span data-stu-id="040ef-144">If these three things are true, the **Task** is also configured as chargeable.</span></span> 

<span data-ttu-id="040ef-145">仅在以下情况下才会将为材料创建的估算或实际值视为应计费：</span><span class="sxs-lookup"><span data-stu-id="040ef-145">An estimate or actual created for material will only be considered chargeable if:</span></span>

   - <span data-ttu-id="040ef-146">报价单明细中包含 **材料**。</span><span class="sxs-lookup"><span data-stu-id="040ef-146">**Materials** is included on the quote line.</span></span>
   - <span data-ttu-id="040ef-147">在报价单明细上将 **包括的任务** 设置为 **选定任务**。</span><span class="sxs-lookup"><span data-stu-id="040ef-147">**Included Tasks** is set to **Selected tasks** on the quote line.</span></span>

<span data-ttu-id="040ef-148">如果这两种情况属实，则还应将 **任务** 配置为应计费。</span><span class="sxs-lookup"><span data-stu-id="040ef-148">If these two things are true, the **Task** should also be configured as chargeable.</span></span> 


<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="70" valign="top">
                <p><span data-ttu-id="040ef-149">
                    <strong>包括时间</strong>
                </span><span class="sxs-lookup"><span data-stu-id="040ef-149">
                    <strong>Includes Time</strong>
                </span></span></p>
            </td>
            <td width="78" valign="top">
                <p><span data-ttu-id="040ef-150">
                    <strong>包括支出</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="040ef-150">
                    <strong>Includes Expense</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="63" valign="top">
                <p><span data-ttu-id="040ef-151">
                    <strong>包括材料</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="040ef-151">
                    <strong>Includes Materials</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="75" valign="top">
                <p><span data-ttu-id="040ef-152">
                    <strong>包含的任务</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="040ef-152">
                    <strong>Included Tasks</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="040ef-153">
                    <strong>角色</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="040ef-153">
                    <strong>Role</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="040ef-154">
                    <strong>类别</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="040ef-154">
                    <strong>Category</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="040ef-155">
                    <strong>任务</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="040ef-155">
                    <strong>Task</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="350" valign="top">
                <p><span data-ttu-id="040ef-156">
                    <strong>应计费影响</strong>
                </span><span class="sxs-lookup"><span data-stu-id="040ef-156">
                    <strong>Chargeability impact</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="040ef-157">是</span><span class="sxs-lookup"><span data-stu-id="040ef-157">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="040ef-158">是</span><span class="sxs-lookup"><span data-stu-id="040ef-158">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="040ef-159">是</span><span class="sxs-lookup"><span data-stu-id="040ef-159">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="040ef-160">整个项目</span><span class="sxs-lookup"><span data-stu-id="040ef-160">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="040ef-161">应计费</span><span class="sxs-lookup"><span data-stu-id="040ef-161">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="040ef-162">应计费</span><span class="sxs-lookup"><span data-stu-id="040ef-162">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="040ef-163">无法设置</span><span class="sxs-lookup"><span data-stu-id="040ef-163">Cannot be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="040ef-164">时间实际值的计费：应计费</span><span class="sxs-lookup"><span data-stu-id="040ef-164">Billing on a time actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="040ef-165">支出实际值的计费：应计费</span><span class="sxs-lookup"><span data-stu-id="040ef-165">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="040ef-166">材料实际值的计费类型：应计费</span><span class="sxs-lookup"><span data-stu-id="040ef-166">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="040ef-167">是</span><span class="sxs-lookup"><span data-stu-id="040ef-167">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="040ef-168">是</span><span class="sxs-lookup"><span data-stu-id="040ef-168">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="040ef-169">是</span><span class="sxs-lookup"><span data-stu-id="040ef-169">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="040ef-170">仅所选任务</span><span class="sxs-lookup"><span data-stu-id="040ef-170">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="040ef-171">应计费</span><span class="sxs-lookup"><span data-stu-id="040ef-171">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="040ef-172">应计费</span><span class="sxs-lookup"><span data-stu-id="040ef-172">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="040ef-173">应计费</span><span class="sxs-lookup"><span data-stu-id="040ef-173">Chargeable</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="040ef-174">时间实际值的计费：应计费</span><span class="sxs-lookup"><span data-stu-id="040ef-174">Billing on a time actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="040ef-175">支出实际值的计费：应计费</span><span class="sxs-lookup"><span data-stu-id="040ef-175">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="040ef-176">材料实际值的计费类型：应计费</span><span class="sxs-lookup"><span data-stu-id="040ef-176">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="040ef-177">是</span><span class="sxs-lookup"><span data-stu-id="040ef-177">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="040ef-178">是</span><span class="sxs-lookup"><span data-stu-id="040ef-178">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="040ef-179">是</span><span class="sxs-lookup"><span data-stu-id="040ef-179">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="040ef-180">仅所选任务</span><span class="sxs-lookup"><span data-stu-id="040ef-180">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="040ef-181">
                    <strong>非应计费</strong>
                </span><span class="sxs-lookup"><span data-stu-id="040ef-181">
                    <strong>Non - Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="040ef-182">应计费</span><span class="sxs-lookup"><span data-stu-id="040ef-182">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="040ef-183">应计费</span><span class="sxs-lookup"><span data-stu-id="040ef-183">Chargeable</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="040ef-184">时间实际值的计费：<strong>非应计费</strong>
                </span><span class="sxs-lookup"><span data-stu-id="040ef-184">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="040ef-185">支出实际值的计费：应计费</span><span class="sxs-lookup"><span data-stu-id="040ef-185">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="040ef-186">材料实际值的计费类型：应计费</span><span class="sxs-lookup"><span data-stu-id="040ef-186">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="040ef-187">是</span><span class="sxs-lookup"><span data-stu-id="040ef-187">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="040ef-188">是</span><span class="sxs-lookup"><span data-stu-id="040ef-188">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="040ef-189">是</span><span class="sxs-lookup"><span data-stu-id="040ef-189">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="040ef-190">仅所选任务</span><span class="sxs-lookup"><span data-stu-id="040ef-190">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="040ef-191">应计费</span><span class="sxs-lookup"><span data-stu-id="040ef-191">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="040ef-192">应计费</span><span class="sxs-lookup"><span data-stu-id="040ef-192">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="040ef-193">
                    <strong>非应计费</strong>
                </span><span class="sxs-lookup"><span data-stu-id="040ef-193">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="040ef-194">时间实际值的计费：<strong>非应计费</strong>
                </span><span class="sxs-lookup"><span data-stu-id="040ef-194">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="040ef-195">支出实际值的计费类型：<strong>非应计费</strong>
                </span><span class="sxs-lookup"><span data-stu-id="040ef-195">Billing type on expense actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="040ef-196">材料实际值的计费类型：<strong>非应计费</strong>
                </span><span class="sxs-lookup"><span data-stu-id="040ef-196">Billing type on material actual: <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="040ef-197">是</span><span class="sxs-lookup"><span data-stu-id="040ef-197">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="040ef-198">是</span><span class="sxs-lookup"><span data-stu-id="040ef-198">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="040ef-199">是</span><span class="sxs-lookup"><span data-stu-id="040ef-199">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="040ef-200">仅所选任务</span><span class="sxs-lookup"><span data-stu-id="040ef-200">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="040ef-201">
                    <strong>非应计费</strong>
                </span><span class="sxs-lookup"><span data-stu-id="040ef-201">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="040ef-202">应计费</span><span class="sxs-lookup"><span data-stu-id="040ef-202">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="040ef-203">
                    <strong>非应计费</strong>
                </span><span class="sxs-lookup"><span data-stu-id="040ef-203">
                    <strong>Non- Chargeable</strong>
                </span></span></p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="040ef-204">时间实际值的计费：<strong>非应计费</strong>
                </span><span class="sxs-lookup"><span data-stu-id="040ef-204">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="040ef-205">支出实际值的计费类型：<strong>非应计费</strong>
                </span><span class="sxs-lookup"><span data-stu-id="040ef-205">Billing type on expense actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="040ef-206">材料实际值的计费类型：<strong>非应计费</strong>
                </span><span class="sxs-lookup"><span data-stu-id="040ef-206">Billing type on material actual: <strong> Non-Chargeable</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="040ef-207">是</span><span class="sxs-lookup"><span data-stu-id="040ef-207">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="040ef-208">是</span><span class="sxs-lookup"><span data-stu-id="040ef-208">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="040ef-209">是</span><span class="sxs-lookup"><span data-stu-id="040ef-209">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="040ef-210">仅所选任务</span><span class="sxs-lookup"><span data-stu-id="040ef-210">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="040ef-211">
                    <strong>非应计费</strong>
                </span><span class="sxs-lookup"><span data-stu-id="040ef-211">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="040ef-212">
                    <strong>非应计费</strong>
                </span><span class="sxs-lookup"><span data-stu-id="040ef-212">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="040ef-213">应计费</span><span class="sxs-lookup"><span data-stu-id="040ef-213">Chargeable</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="040ef-214">时间实际值的计费：<strong>非应计费</strong>
                </span><span class="sxs-lookup"><span data-stu-id="040ef-214">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="040ef-215">支出实际值的计费类型：<strong>非应计费</strong>
                </span><span class="sxs-lookup"><span data-stu-id="040ef-215">Billing type on expense actual: <strong> Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="040ef-216">材料实际值的计费类型：应计费</span><span class="sxs-lookup"><span data-stu-id="040ef-216">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p><span data-ttu-id="040ef-217">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="040ef-217">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="040ef-218">是</span><span class="sxs-lookup"><span data-stu-id="040ef-218">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="040ef-219">是</span><span class="sxs-lookup"><span data-stu-id="040ef-219">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="040ef-220">整个项目</span><span class="sxs-lookup"><span data-stu-id="040ef-220">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="040ef-221">无法设置</span><span class="sxs-lookup"><span data-stu-id="040ef-221">Cannot be set</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="040ef-222">
                    <strong>应计费</strong>
                </span><span class="sxs-lookup"><span data-stu-id="040ef-222">
                    <strong>Chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="040ef-223">无法设置</span><span class="sxs-lookup"><span data-stu-id="040ef-223">Cannot be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="040ef-224">时间实际值的计费：<strong>不可用</strong>
                </span><span class="sxs-lookup"><span data-stu-id="040ef-224">Billing on a time actual: <strong>Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="040ef-225">支出实际值的计费：应计费</span><span class="sxs-lookup"><span data-stu-id="040ef-225">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="040ef-226">材料实际值的计费类型：应计费</span><span class="sxs-lookup"><span data-stu-id="040ef-226">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p><span data-ttu-id="040ef-227">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="040ef-227">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="040ef-228">是</span><span class="sxs-lookup"><span data-stu-id="040ef-228">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="040ef-229">是</span><span class="sxs-lookup"><span data-stu-id="040ef-229">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="040ef-230">整个项目</span><span class="sxs-lookup"><span data-stu-id="040ef-230">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="040ef-231">无法设置</span><span class="sxs-lookup"><span data-stu-id="040ef-231">Cannot be set</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="040ef-232">
                    <strong>非应计费</strong>
                </span><span class="sxs-lookup"><span data-stu-id="040ef-232">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="040ef-233">无法设置</span><span class="sxs-lookup"><span data-stu-id="040ef-233">Cannot be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="040ef-234">时间实际值的计费：<strong>不可用</strong>
                </span><span class="sxs-lookup"><span data-stu-id="040ef-234">Billing on a time actual: <strong>Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="040ef-235">支出实际值的计费类型：<strong>非应计费</strong>
                </span><span class="sxs-lookup"><span data-stu-id="040ef-235">Billing type on expense actual: <strong> Non-chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="040ef-236">材料实际值的计费类型：应计费</span><span class="sxs-lookup"><span data-stu-id="040ef-236">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="040ef-237">是</span><span class="sxs-lookup"><span data-stu-id="040ef-237">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p><span data-ttu-id="040ef-238">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="040ef-238">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="040ef-239">是</span><span class="sxs-lookup"><span data-stu-id="040ef-239">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="040ef-240">整个项目</span><span class="sxs-lookup"><span data-stu-id="040ef-240">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="040ef-241">应计费</span><span class="sxs-lookup"><span data-stu-id="040ef-241">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="040ef-242">无法设置</span><span class="sxs-lookup"><span data-stu-id="040ef-242">Cannot be set</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="040ef-243">无法设置</span><span class="sxs-lookup"><span data-stu-id="040ef-243">Cannot be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="040ef-244">时间实际值的计费：应计费</span><span class="sxs-lookup"><span data-stu-id="040ef-244">Billing on a time actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="040ef-245">支出实际值的计费类型：<strong>不可用</strong>
                </span><span class="sxs-lookup"><span data-stu-id="040ef-245">Billing type on expense actual:<strong> Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="040ef-246">材料实际值的计费类型：应计费</span><span class="sxs-lookup"><span data-stu-id="040ef-246">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="040ef-247">是</span><span class="sxs-lookup"><span data-stu-id="040ef-247">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p><span data-ttu-id="040ef-248">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="040ef-248">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="040ef-249">是</span><span class="sxs-lookup"><span data-stu-id="040ef-249">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="040ef-250">整个项目</span><span class="sxs-lookup"><span data-stu-id="040ef-250">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="040ef-251">
                    <strong>非应计费</strong>
                </span><span class="sxs-lookup"><span data-stu-id="040ef-251">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="040ef-252">无法设置</span><span class="sxs-lookup"><span data-stu-id="040ef-252">Cannot be set</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="040ef-253">无法设置</span><span class="sxs-lookup"><span data-stu-id="040ef-253">Cannot be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="040ef-254">时间实际值的计费：<strong>非应计费</strong>
                </span><span class="sxs-lookup"><span data-stu-id="040ef-254">Billing on a time actual: <strong>Non-chargeable </strong>
                </span></span></p>
                <p>
<span data-ttu-id="040ef-255">支出实际值的计费类型：<strong>不可用</strong>
                </span><span class="sxs-lookup"><span data-stu-id="040ef-255">Billing type on expense actual:<strong> Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="040ef-256">材料实际值的计费类型：应计费</span><span class="sxs-lookup"><span data-stu-id="040ef-256">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="040ef-257">是</span><span class="sxs-lookup"><span data-stu-id="040ef-257">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="040ef-258">是</span><span class="sxs-lookup"><span data-stu-id="040ef-258">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p><span data-ttu-id="040ef-259">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="040ef-259">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="040ef-260">整个项目</span><span class="sxs-lookup"><span data-stu-id="040ef-260">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="040ef-261">应计费</span><span class="sxs-lookup"><span data-stu-id="040ef-261">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="040ef-262">应计费</span><span class="sxs-lookup"><span data-stu-id="040ef-262">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="040ef-263">无法设置</span><span class="sxs-lookup"><span data-stu-id="040ef-263">Cannot be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="040ef-264">时间实际值的计费：应计费</span><span class="sxs-lookup"><span data-stu-id="040ef-264">Billing on a time actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="040ef-265">支出实际值的计费：应计费</span><span class="sxs-lookup"><span data-stu-id="040ef-265">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="040ef-266">材料实际值的计费类型：<strong>不可用</strong>
                </span><span class="sxs-lookup"><span data-stu-id="040ef-266">Billing type on material actual: <strong> Not available</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="040ef-267">是</span><span class="sxs-lookup"><span data-stu-id="040ef-267">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="040ef-268">是</span><span class="sxs-lookup"><span data-stu-id="040ef-268">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p><span data-ttu-id="040ef-269">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="040ef-269">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="040ef-270">整个项目</span><span class="sxs-lookup"><span data-stu-id="040ef-270">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="040ef-271">
                    <strong>非应计费</strong>
                </span><span class="sxs-lookup"><span data-stu-id="040ef-271">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="040ef-272">
                    <strong>非应计费</strong>
                </span><span class="sxs-lookup"><span data-stu-id="040ef-272">
                    <strong>Non-chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="040ef-273">无法设置</span><span class="sxs-lookup"><span data-stu-id="040ef-273">Cannot be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="040ef-274">时间实际值的计费：<strong>非应计费</strong>
                </span><span class="sxs-lookup"><span data-stu-id="040ef-274">Billing on a time actual: <strong>Non-chargeable </strong>
                </span></span></p>
                <p>
<span data-ttu-id="040ef-275">支出实际值的计费类型：<strong>非应计费</strong>
                </span><span class="sxs-lookup"><span data-stu-id="040ef-275">Billing type on expense actual:<strong> Non-chargeable </strong>
                </span></span></p>
                <p>
<span data-ttu-id="040ef-276">材料实际值的计费类型：<strong>不可用</strong>
                </span><span class="sxs-lookup"><span data-stu-id="040ef-276">Billing type on material actual:<strong> Not available</strong>
                </span></span></p>
            </td>
        </tr>
    </tbody>
</table>



[!INCLUDE[footer-include](../../includes/footer-banner.md)]
