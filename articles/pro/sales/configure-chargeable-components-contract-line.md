---
title: 配置基于项目的合同子项的应计费组件
description: 此主题提供有关如何在 Project Operations 中向合同子项添加应计费组件的信息。
author: rumant
ms.date: 10/08/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: b29c912828aa4af2d2d9cb47869012087cb834b4
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/10/2021
ms.locfileid: "6003710"
---
# <a name="configure-chargeable-components-of-a-project-based-contract-line"></a><span data-ttu-id="2381b-103">配置基于项目的合同子项的应计费组件</span><span class="sxs-lookup"><span data-stu-id="2381b-103">Configure chargeable components of a project-based contract line</span></span>

<span data-ttu-id="2381b-104">_**适用于：** 精简部署 - 估价交易开单，基于资源/非库存场景的 Project Operations_</span><span class="sxs-lookup"><span data-stu-id="2381b-104">_**Applies To:** Lite deployment - deal to proforma invoicing, Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="2381b-105">基于项目的合同子项具有 *包含* 组件和 *应计费* 组件。</span><span class="sxs-lookup"><span data-stu-id="2381b-105">A project-based contract line has *included* components and *chargeable* components.</span></span>

<span data-ttu-id="2381b-106">包含组件是受以下各项约束的组件：</span><span class="sxs-lookup"><span data-stu-id="2381b-106">Included components are components that are subject to:</span></span>

  - <span data-ttu-id="2381b-107">计费方法和客户拆分</span><span class="sxs-lookup"><span data-stu-id="2381b-107">Billing method and customer splits</span></span>
  - <span data-ttu-id="2381b-108">上限</span><span class="sxs-lookup"><span data-stu-id="2381b-108">Not-to-exceed limits</span></span> 
  - <span data-ttu-id="2381b-109">基于项目的合同子项上定义的发票频率设置</span><span class="sxs-lookup"><span data-stu-id="2381b-109">Invoice frequency settings defined on the project-based contract line</span></span>

<span data-ttu-id="2381b-110">包含组件的子集可以使用 **记帐类型** 字段标记为应计费。</span><span class="sxs-lookup"><span data-stu-id="2381b-110">A subset of the included components can be marked as chargeable using the **Billing Type** field.</span></span> <span data-ttu-id="2381b-111">**记帐类型** 字段是一个选项集，允许在合同子项的上下文中使用以下值：</span><span class="sxs-lookup"><span data-stu-id="2381b-111">The **Billing Type** field is an option-set that allows the following values in the context of a contract line:</span></span>

  - <span data-ttu-id="2381b-112">应计费</span><span class="sxs-lookup"><span data-stu-id="2381b-112">Chargeable</span></span>
  - <span data-ttu-id="2381b-113">非应计费</span><span class="sxs-lookup"><span data-stu-id="2381b-113">Non-chargeable</span></span>

<span data-ttu-id="2381b-114">应计费组件可以在任务、角色和交易类别中定义。</span><span class="sxs-lookup"><span data-stu-id="2381b-114">Chargeable components can be defined on tasks, roles, and transaction categories.</span></span>

<span data-ttu-id="2381b-115">应计费在项目合同子项的任务中定义，应用于合同子项中包括的所有交易类。</span><span class="sxs-lookup"><span data-stu-id="2381b-115">Chargeability is defined on tasks for a project contract line and applies to all transaction classes included on the line.</span></span> <span data-ttu-id="2381b-116">如果合同子项上的 **包含任务** 字段为空或设置为 **整个项目**，**应计费任务** 选项卡将不可用。</span><span class="sxs-lookup"><span data-stu-id="2381b-116">If the **Include Tasks** field on a contract line is blank or set to **Entire project**, the **Chargeable tasks** tab will not be available.</span></span>

<span data-ttu-id="2381b-117">在项目合同子项的角色中定义的应计费仅应用于 **时间** 交易类。</span><span class="sxs-lookup"><span data-stu-id="2381b-117">Chargeability defined on roles for a project contract line only applies to the **Time** transaction class.</span></span> <span data-ttu-id="2381b-118">如果合同子项上的 **包含时间** 字段设置为 **否**，**应计费角色** 选项卡将不可用。</span><span class="sxs-lookup"><span data-stu-id="2381b-118">If the **Include Time** field on a contract line is set to **No**, the **Chargeable roles** tab will not be available.</span></span>

<span data-ttu-id="2381b-119">在项目合同子项的交易类别中定义的应计费仅应用于 **支出** 交易类。</span><span class="sxs-lookup"><span data-stu-id="2381b-119">Chargeability defined on transaction categories for a project contract line only applies to the **Expense** transaction class.</span></span> <span data-ttu-id="2381b-120">如果 **包含支出** 字段设置为 **否**，**应计费类别** 选项卡将不可用。</span><span class="sxs-lookup"><span data-stu-id="2381b-120">If the **Include Expenses** field is set to **No**, the **Chargeable Categories** tab will not be available.</span></span>

### <a name="update-a-project-task-as-chargeable-or-non-chargeable"></a><span data-ttu-id="2381b-121">将项目任务更新为应计费或非应计费</span><span class="sxs-lookup"><span data-stu-id="2381b-121">Update a project task as chargeable or non-chargeable</span></span>

<span data-ttu-id="2381b-122">项目任务在特定合同子项上可以是应计费或非应计费，这样可以进行以下设置：</span><span class="sxs-lookup"><span data-stu-id="2381b-122">A project task can be chargeable or non-chargeable on a specific contract line, which makes the following setup possible:</span></span>

<span data-ttu-id="2381b-123">如果基于项目的合同子项包含 **时间** 和某个任务，**T1** 将作为应计费与其关联。</span><span class="sxs-lookup"><span data-stu-id="2381b-123">If a project-based contract line includes **Time** and a certain task, **T1** is associated to it as chargeable.</span></span> <span data-ttu-id="2381b-124">如果有另一个包含 **支出** 的合同子项，您可以将该合同子项上的 T1 任务作为非应计费关联。</span><span class="sxs-lookup"><span data-stu-id="2381b-124">If there is a second contract line that includes **Expense**, you can associate the T1 task on the contract line as non-chargeable.</span></span> <span data-ttu-id="2381b-125">结果是，任务中记录的所有时间都为应计费，所有支出都为非应计费。</span><span class="sxs-lookup"><span data-stu-id="2381b-125">The result is that all of the time recorded on the task is chargeable and all expenses are non-chargeable.</span></span>

<span data-ttu-id="2381b-126">任务的计费类型可以通过更新合同子项任务子网格上的 **计费类型** 字段在合同子项的 **应计费任务** 选项卡上配置。</span><span class="sxs-lookup"><span data-stu-id="2381b-126">A task's billing type can be configured on the **Chargeable Tasks** tab of the contract line by updating the **Billing Type** field on the contract line tasks subgrid.</span></span> <span data-ttu-id="2381b-127">或者，您可以更新显示与任务关联的合同子项的项目任务计费设置子网格上的 **计费类型** 字段。</span><span class="sxs-lookup"><span data-stu-id="2381b-127">Alternatively, you can update the **Billing Type** field on the subgrid of the task Billing setup of a project that shows the contract lines associated to a task.</span></span>

### <a name="update-a-role-as-chargeable-or-non-chargeable"></a><span data-ttu-id="2381b-128">将角色更新为应计费或非应计费</span><span class="sxs-lookup"><span data-stu-id="2381b-128">Update a role as chargeable or non-chargeable</span></span>

<span data-ttu-id="2381b-129">角色在特定合同子项上可以为应计费或非应计费。</span><span class="sxs-lookup"><span data-stu-id="2381b-129">A role can be chargeable or non-chargeable on a specific contract line.</span></span>

<span data-ttu-id="2381b-130">角色的计费类型可以在合同子项的 **应计费角色** 选项卡上配置。</span><span class="sxs-lookup"><span data-stu-id="2381b-130">A role's billing type can be configured on the **Chargeable Roles** tab of a contract line.</span></span> <span data-ttu-id="2381b-131">要执行此操作，请更新 **应计费角色** 子网格中的 **计费类型** 字段 。</span><span class="sxs-lookup"><span data-stu-id="2381b-131">To do this, update the **Billing Type** field on the **Chargeable Roles** subgrid.</span></span>

### <a name="update-a-transaction-category-as-chargeable-or-non-chargeable"></a><span data-ttu-id="2381b-132">将交易类别更新为应计费或非应计费</span><span class="sxs-lookup"><span data-stu-id="2381b-132">Update a transaction category as chargeable or non-chargeable</span></span>

<span data-ttu-id="2381b-133">交易类别在特定合同子项上可以为应计费或非应计费。</span><span class="sxs-lookup"><span data-stu-id="2381b-133">A transaction category can be chargeable or non-chargeable on a specific contract line.</span></span>

<span data-ttu-id="2381b-134">交易的计费类型可以在基于项目的合同子项的 **应计费类别** 选项卡上配置。</span><span class="sxs-lookup"><span data-stu-id="2381b-134">A transaction's billing type can be configured on the **Chargeable Categories** tab of a project-based contract line.</span></span> <span data-ttu-id="2381b-135">要执行此操作，请更新 **应计费类别** 子网格中的 **计费类型** 字段 。</span><span class="sxs-lookup"><span data-stu-id="2381b-135">To do this, update the **Billing Type** field on the **Chargeable Categories** subgrid.</span></span>

### <a name="resolve-chargeability"></a><span data-ttu-id="2381b-136">解析应计费</span><span class="sxs-lookup"><span data-stu-id="2381b-136">Resolve chargeability</span></span>

<span data-ttu-id="2381b-137">仅在以下情况下才会将为时间创建的估算或实际值视为应计费：</span><span class="sxs-lookup"><span data-stu-id="2381b-137">An estimate or actual created for time is only considered chargeable if:</span></span>

   - <span data-ttu-id="2381b-138">合同子项中包含 **时间**。</span><span class="sxs-lookup"><span data-stu-id="2381b-138">**Time** is included on the contract line.</span></span>
   - <span data-ttu-id="2381b-139">在合同子项上将 **角色** 配置为应计费。</span><span class="sxs-lookup"><span data-stu-id="2381b-139">**Role** is configured as chargeable on the contract line.</span></span>
   - <span data-ttu-id="2381b-140">在合同子项上将 **包括的任务** 设置为 **选定任务**。</span><span class="sxs-lookup"><span data-stu-id="2381b-140">**Included Tasks** is set to **Selected tasks** on the contract line.</span></span>
 
 <span data-ttu-id="2381b-141">如果这三种情况属实，则还会将任务配置为应计费。</span><span class="sxs-lookup"><span data-stu-id="2381b-141">If these three things are true, the task is configured as chargeable.</span></span> 

<span data-ttu-id="2381b-142">仅在以下情况下才会将为支出创建的估算或实际值视为应计费：</span><span class="sxs-lookup"><span data-stu-id="2381b-142">An estimate or actual created for expense is only considered chargeable if:</span></span>

   - <span data-ttu-id="2381b-143">合同子项中包含 **支出**</span><span class="sxs-lookup"><span data-stu-id="2381b-143">**Expense** is included on the contract line</span></span>
   - <span data-ttu-id="2381b-144">在合同子项上将 **交易类别** 配置为应计费</span><span class="sxs-lookup"><span data-stu-id="2381b-144">**Transaction category** is configured as chargeable on the contract line</span></span>
   - <span data-ttu-id="2381b-145">在合同子项上将 **包括的任务** 设置为 **选定任务**</span><span class="sxs-lookup"><span data-stu-id="2381b-145">**Included Tasks** is set to **Selected task** on the contract line</span></span>
  
 <span data-ttu-id="2381b-146">如果这三种情况属实，则还会将 **任务** 配置为应计费。</span><span class="sxs-lookup"><span data-stu-id="2381b-146">If these three things are true, the **Task** is configured as chargeable.</span></span> 

<span data-ttu-id="2381b-147">仅在以下情况下才会将为材料创建的估算或实际值视为应计费：</span><span class="sxs-lookup"><span data-stu-id="2381b-147">An estimate or actual created for material is only considered chargeable if:</span></span>

   - <span data-ttu-id="2381b-148">合同子项中包含 **材料**</span><span class="sxs-lookup"><span data-stu-id="2381b-148">**Materials** is included on the contract line</span></span>
   - <span data-ttu-id="2381b-149">在合同子项上将 **包括的任务** 设置为 **选定任务**</span><span class="sxs-lookup"><span data-stu-id="2381b-149">**Included Tasks** is set to **Selected tasks** on the contract line</span></span>

<span data-ttu-id="2381b-150">如果这两种情况属实，则还会将 **任务** 配置为应计费。</span><span class="sxs-lookup"><span data-stu-id="2381b-150">If these two things are true, the **Task** is configured as chargeable.</span></span> 

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="70" valign="top">
                <p><span data-ttu-id="2381b-151">
                    <strong>包括时间</strong>
                </span><span class="sxs-lookup"><span data-stu-id="2381b-151">
                    <strong>Includes Time</strong>
                </span></span></p>
            </td>
            <td width="78" valign="top">
                <p><span data-ttu-id="2381b-152">
                    <strong>包括支出</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="2381b-152">
                    <strong>Includes Expense</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="63" valign="top">
                <p><span data-ttu-id="2381b-153">
                    <strong>包括材料</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="2381b-153">
                    <strong>Includes Materials</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="75" valign="top">
                <p><span data-ttu-id="2381b-154">
                    <strong>包含的任务</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="2381b-154">
                    <strong>Included Tasks</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="2381b-155">
                    <strong>角色</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="2381b-155">
                    <strong>Role</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="2381b-156">
                    <strong>类别</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="2381b-156">
                    <strong>Category</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="2381b-157">
                    <strong>任务</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="2381b-157">
                    <strong>Task</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="350" valign="top">
                <p><span data-ttu-id="2381b-158">
                    <strong>应计费影响</strong>
                </span><span class="sxs-lookup"><span data-stu-id="2381b-158">
                    <strong>Chargeability impact</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="2381b-159">是</span><span class="sxs-lookup"><span data-stu-id="2381b-159">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="2381b-160">是</span><span class="sxs-lookup"><span data-stu-id="2381b-160">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="2381b-161">是</span><span class="sxs-lookup"><span data-stu-id="2381b-161">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="2381b-162">整个项目</span><span class="sxs-lookup"><span data-stu-id="2381b-162">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="2381b-163">应计费</span><span class="sxs-lookup"><span data-stu-id="2381b-163">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="2381b-164">应计费</span><span class="sxs-lookup"><span data-stu-id="2381b-164">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="2381b-165">无法设置</span><span class="sxs-lookup"><span data-stu-id="2381b-165">Can't be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="2381b-166">时间实际值的计费：<strong>应计费</strong>
                </span><span class="sxs-lookup"><span data-stu-id="2381b-166">Billing on a time actual: <strong>Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="2381b-167">支出实际值的计费：<strong>应计费</strong>
                </span><span class="sxs-lookup"><span data-stu-id="2381b-167">Billing type on expense actual: <strong>Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="2381b-168">材料实际值的计费类型：<strong>应计费</strong>
                </span><span class="sxs-lookup"><span data-stu-id="2381b-168">Billing type on material actual: <strong>Chargeable</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="2381b-169">是</span><span class="sxs-lookup"><span data-stu-id="2381b-169">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="2381b-170">是</span><span class="sxs-lookup"><span data-stu-id="2381b-170">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="2381b-171">是</span><span class="sxs-lookup"><span data-stu-id="2381b-171">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="2381b-172">仅所选任务</span><span class="sxs-lookup"><span data-stu-id="2381b-172">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="2381b-173">应计费</span><span class="sxs-lookup"><span data-stu-id="2381b-173">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="2381b-174">应计费</span><span class="sxs-lookup"><span data-stu-id="2381b-174">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="2381b-175">应计费</span><span class="sxs-lookup"><span data-stu-id="2381b-175">Chargeable</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="2381b-176">时间实际值的计费：<strong>应计费</strong>
                </span><span class="sxs-lookup"><span data-stu-id="2381b-176">Billing on a time actual: <strong>Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="2381b-177">支出实际值的计费：<strong>应计费</strong>
                </span><span class="sxs-lookup"><span data-stu-id="2381b-177">Billing type on expense actual: <strong>Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="2381b-178">材料实际值的计费类型：<strong>应计费</strong>
                </span><span class="sxs-lookup"><span data-stu-id="2381b-178">Billing type on material actual: <strong>Chargeable</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="2381b-179">是</span><span class="sxs-lookup"><span data-stu-id="2381b-179">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="2381b-180">是</span><span class="sxs-lookup"><span data-stu-id="2381b-180">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="2381b-181">是</span><span class="sxs-lookup"><span data-stu-id="2381b-181">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="2381b-182">仅所选任务</span><span class="sxs-lookup"><span data-stu-id="2381b-182">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="2381b-183">
                    <strong>非应计费</strong>
                </span><span class="sxs-lookup"><span data-stu-id="2381b-183">
                    <strong>Non - Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="2381b-184">应计费</span><span class="sxs-lookup"><span data-stu-id="2381b-184">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="2381b-185">应计费</span><span class="sxs-lookup"><span data-stu-id="2381b-185">Chargeable</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="2381b-186">时间实际值的计费：<strong>非应计费</strong>
                </span><span class="sxs-lookup"><span data-stu-id="2381b-186">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="2381b-187">支出实际值的计费：应计费</span><span class="sxs-lookup"><span data-stu-id="2381b-187">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="2381b-188">材料实际值的计费类型：应计费</span><span class="sxs-lookup"><span data-stu-id="2381b-188">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="2381b-189">是</span><span class="sxs-lookup"><span data-stu-id="2381b-189">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="2381b-190">是</span><span class="sxs-lookup"><span data-stu-id="2381b-190">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="2381b-191">是</span><span class="sxs-lookup"><span data-stu-id="2381b-191">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="2381b-192">仅所选任务</span><span class="sxs-lookup"><span data-stu-id="2381b-192">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="2381b-193">应计费</span><span class="sxs-lookup"><span data-stu-id="2381b-193">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="2381b-194">应计费</span><span class="sxs-lookup"><span data-stu-id="2381b-194">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="2381b-195">
                    <strong>非应计费</strong>
                </span><span class="sxs-lookup"><span data-stu-id="2381b-195">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="2381b-196">时间实际值的计费：<strong>非应计费</strong>
                </span><span class="sxs-lookup"><span data-stu-id="2381b-196">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="2381b-197">支出实际值的计费类型：<strong>非应计费</strong>
                </span><span class="sxs-lookup"><span data-stu-id="2381b-197">Billing type on expense actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="2381b-198">材料实际值的计费类型：<strong>非应计费</strong>
                </span><span class="sxs-lookup"><span data-stu-id="2381b-198">Billing type on material actual: <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="2381b-199">是</span><span class="sxs-lookup"><span data-stu-id="2381b-199">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="2381b-200">是</span><span class="sxs-lookup"><span data-stu-id="2381b-200">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="2381b-201">是</span><span class="sxs-lookup"><span data-stu-id="2381b-201">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="2381b-202">仅所选任务</span><span class="sxs-lookup"><span data-stu-id="2381b-202">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="2381b-203">
                    <strong>非应计费</strong>
                </span><span class="sxs-lookup"><span data-stu-id="2381b-203">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="2381b-204">应计费</span><span class="sxs-lookup"><span data-stu-id="2381b-204">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="2381b-205">
                    <strong>非应计费</strong>
                </span><span class="sxs-lookup"><span data-stu-id="2381b-205">
                    <strong>Non- Chargeable</strong>
                </span></span></p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="2381b-206">时间实际值的计费：<strong>非应计费</strong>
                </span><span class="sxs-lookup"><span data-stu-id="2381b-206">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="2381b-207">支出实际值的计费类型：<strong>非应计费</strong>
                </span><span class="sxs-lookup"><span data-stu-id="2381b-207">Billing type on expense actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="2381b-208">材料实际值的计费类型：<strong>非应计费</strong>
                </span><span class="sxs-lookup"><span data-stu-id="2381b-208">Billing type on material actual: <strong> Non-Chargeable</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="2381b-209">是</span><span class="sxs-lookup"><span data-stu-id="2381b-209">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="2381b-210">是</span><span class="sxs-lookup"><span data-stu-id="2381b-210">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="2381b-211">是</span><span class="sxs-lookup"><span data-stu-id="2381b-211">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="2381b-212">仅所选任务</span><span class="sxs-lookup"><span data-stu-id="2381b-212">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="2381b-213">
                    <strong>非应计费</strong>
                </span><span class="sxs-lookup"><span data-stu-id="2381b-213">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="2381b-214">
                    <strong>非应计费</strong>
                </span><span class="sxs-lookup"><span data-stu-id="2381b-214">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="2381b-215">应计费</span><span class="sxs-lookup"><span data-stu-id="2381b-215">Chargeable</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="2381b-216">时间实际值的计费：<strong>非应计费</strong>
                </span><span class="sxs-lookup"><span data-stu-id="2381b-216">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="2381b-217">支出实际值的计费类型：<strong>非应计费</strong>
                </span><span class="sxs-lookup"><span data-stu-id="2381b-217">Billing type on expense actual: <strong> Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="2381b-218">材料实际值的计费类型：应计费</span><span class="sxs-lookup"><span data-stu-id="2381b-218">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p><span data-ttu-id="2381b-219">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="2381b-219">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="2381b-220">是</span><span class="sxs-lookup"><span data-stu-id="2381b-220">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="2381b-221">是</span><span class="sxs-lookup"><span data-stu-id="2381b-221">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="2381b-222">整个项目</span><span class="sxs-lookup"><span data-stu-id="2381b-222">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="2381b-223">无法设置</span><span class="sxs-lookup"><span data-stu-id="2381b-223">Can't be set</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="2381b-224">
                    <strong>应计费</strong>
                </span><span class="sxs-lookup"><span data-stu-id="2381b-224">
                    <strong>Chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="2381b-225">无法设置</span><span class="sxs-lookup"><span data-stu-id="2381b-225">Can't be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="2381b-226">时间实际值的计费：<strong>不可用</strong>
                </span><span class="sxs-lookup"><span data-stu-id="2381b-226">Billing on a time actual: <strong>Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="2381b-227">支出实际值的计费：应计费</span><span class="sxs-lookup"><span data-stu-id="2381b-227">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="2381b-228">材料实际值的计费类型：应计费</span><span class="sxs-lookup"><span data-stu-id="2381b-228">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p><span data-ttu-id="2381b-229">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="2381b-229">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="2381b-230">是</span><span class="sxs-lookup"><span data-stu-id="2381b-230">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="2381b-231">是</span><span class="sxs-lookup"><span data-stu-id="2381b-231">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="2381b-232">整个项目</span><span class="sxs-lookup"><span data-stu-id="2381b-232">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="2381b-233">无法设置</span><span class="sxs-lookup"><span data-stu-id="2381b-233">Can't be set</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="2381b-234">
                    <strong>非应计费</strong>
                </span><span class="sxs-lookup"><span data-stu-id="2381b-234">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="2381b-235">无法设置</span><span class="sxs-lookup"><span data-stu-id="2381b-235">Can't be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="2381b-236">时间实际值的计费：<strong>不可用</strong>
                </span><span class="sxs-lookup"><span data-stu-id="2381b-236">Billing on a time actual: <strong>Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="2381b-237">支出实际值的计费类型：<strong>非应计费</strong>
                </span><span class="sxs-lookup"><span data-stu-id="2381b-237">Billing type on expense actual: <strong> Non-chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="2381b-238">材料实际值的计费类型：应计费</span><span class="sxs-lookup"><span data-stu-id="2381b-238">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="2381b-239">是</span><span class="sxs-lookup"><span data-stu-id="2381b-239">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p><span data-ttu-id="2381b-240">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="2381b-240">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="2381b-241">是</span><span class="sxs-lookup"><span data-stu-id="2381b-241">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="2381b-242">整个项目</span><span class="sxs-lookup"><span data-stu-id="2381b-242">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="2381b-243">应计费</span><span class="sxs-lookup"><span data-stu-id="2381b-243">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="2381b-244">无法设置</span><span class="sxs-lookup"><span data-stu-id="2381b-244">Can't be set</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="2381b-245">无法设置</span><span class="sxs-lookup"><span data-stu-id="2381b-245">Can't be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="2381b-246">时间实际值的计费：应计费</span><span class="sxs-lookup"><span data-stu-id="2381b-246">Billing on a time actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="2381b-247">支出实际值的计费类型：<strong>不可用</strong>
                </span><span class="sxs-lookup"><span data-stu-id="2381b-247">Billing type on expense actual:<strong> Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="2381b-248">材料实际值的计费类型：应计费</span><span class="sxs-lookup"><span data-stu-id="2381b-248">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="2381b-249">是</span><span class="sxs-lookup"><span data-stu-id="2381b-249">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p><span data-ttu-id="2381b-250">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="2381b-250">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="2381b-251">是</span><span class="sxs-lookup"><span data-stu-id="2381b-251">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="2381b-252">整个项目</span><span class="sxs-lookup"><span data-stu-id="2381b-252">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="2381b-253">
                    <strong>非应计费</strong>
                </span><span class="sxs-lookup"><span data-stu-id="2381b-253">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="2381b-254">无法设置</span><span class="sxs-lookup"><span data-stu-id="2381b-254">Can't be set</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="2381b-255">无法设置</span><span class="sxs-lookup"><span data-stu-id="2381b-255">Can't be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="2381b-256">时间实际值的计费：<strong>非应计费</strong>
                </span><span class="sxs-lookup"><span data-stu-id="2381b-256">Billing on a time actual: <strong>Non-chargeable </strong>
                </span></span></p>
                <p>
<span data-ttu-id="2381b-257">支出实际值的计费类型：<strong>不可用</strong>
                </span><span class="sxs-lookup"><span data-stu-id="2381b-257">Billing type on expense actual:<strong> Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="2381b-258">材料实际值的计费类型：应计费</span><span class="sxs-lookup"><span data-stu-id="2381b-258">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="2381b-259">是</span><span class="sxs-lookup"><span data-stu-id="2381b-259">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="2381b-260">是</span><span class="sxs-lookup"><span data-stu-id="2381b-260">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p><span data-ttu-id="2381b-261">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="2381b-261">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="2381b-262">整个项目</span><span class="sxs-lookup"><span data-stu-id="2381b-262">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="2381b-263">应计费</span><span class="sxs-lookup"><span data-stu-id="2381b-263">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="2381b-264">应计费</span><span class="sxs-lookup"><span data-stu-id="2381b-264">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="2381b-265">无法设置</span><span class="sxs-lookup"><span data-stu-id="2381b-265">Can't be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="2381b-266">时间实际值的计费：应计费</span><span class="sxs-lookup"><span data-stu-id="2381b-266">Billing on a time actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="2381b-267">支出实际值的计费：应计费</span><span class="sxs-lookup"><span data-stu-id="2381b-267">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="2381b-268">材料实际值的计费类型：<strong>不可用</strong>
                </span><span class="sxs-lookup"><span data-stu-id="2381b-268">Billing type on material actual: <strong> Not available</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="2381b-269">是</span><span class="sxs-lookup"><span data-stu-id="2381b-269">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="2381b-270">是</span><span class="sxs-lookup"><span data-stu-id="2381b-270">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p><span data-ttu-id="2381b-271">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="2381b-271">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="2381b-272">整个项目</span><span class="sxs-lookup"><span data-stu-id="2381b-272">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="2381b-273">
                    <strong>非应计费</strong>
                </span><span class="sxs-lookup"><span data-stu-id="2381b-273">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="2381b-274">
                    <strong>非应计费</strong>
                </span><span class="sxs-lookup"><span data-stu-id="2381b-274">
                    <strong>Non-chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="2381b-275">无法设置</span><span class="sxs-lookup"><span data-stu-id="2381b-275">Can't be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="2381b-276">时间实际值的计费：<strong>非应计费</strong>
                </span><span class="sxs-lookup"><span data-stu-id="2381b-276">Billing on a time actual: <strong>Non-chargeable </strong>
                </span></span></p>
                <p>
<span data-ttu-id="2381b-277">支出实际值的计费类型：<strong>非应计费</strong>
                </span><span class="sxs-lookup"><span data-stu-id="2381b-277">Billing type on expense actual:<strong> Non-chargeable </strong>
                </span></span></p>
                <p>
<span data-ttu-id="2381b-278">材料实际值的计费类型：<strong>不可用</strong>
                </span><span class="sxs-lookup"><span data-stu-id="2381b-278">Billing type on material actual:<strong> Not available</strong>
                </span></span></p>
            </td>
        </tr>
    </tbody>
</table>





[!INCLUDE[footer-include](../../includes/footer-banner.md)]
