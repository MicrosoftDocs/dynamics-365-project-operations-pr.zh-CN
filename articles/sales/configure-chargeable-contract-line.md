---
title: 配置项目合同子项的应计费组件
description: 此主题提供有关在合同子项上的包含、应计费和非应计费组件的信息。
author: rumant
manager: Annbe
ms.date: 10/12/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 60a2792f7783053a288303e1dcc01a986e948300
ms.sourcegitcommit: 5fd529f2308edfe9322082313e6d50146df56aca
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/06/2021
ms.locfileid: "5858327"
---
# <a name="configure-chargeable-components-of-a-project-contract-line"></a><span data-ttu-id="43f00-103">配置项目合同子项的应计费组件</span><span class="sxs-lookup"><span data-stu-id="43f00-103">Configure chargeable components of a project contract line</span></span>

<span data-ttu-id="43f00-104">_**适用于：** 面向资源/非库存场景的 Project Operations_</span><span class="sxs-lookup"><span data-stu-id="43f00-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="43f00-105">基于项目的合同子项具有包含组件、应计费组件和非应计费组件概念。</span><span class="sxs-lookup"><span data-stu-id="43f00-105">A project-based contract line has the concept of included, chargeable, and non-chargeable components.</span></span>

<span data-ttu-id="43f00-106">包含组件受基于项目的合同子项上定义的计费方法、客户拆分、上限以及发票频率设置的限制。</span><span class="sxs-lookup"><span data-stu-id="43f00-106">Included components are subject to the billing method, customer splits, not-to-exceed limits, and invoice frequency settings defined on the project-based contract line.</span></span>

<span data-ttu-id="43f00-107">包含组件的子集可以通过更新 **记帐类型** 字段标记为应计费。</span><span class="sxs-lookup"><span data-stu-id="43f00-107">A subset of the included components can be marked as chargeable by updating the **Billing Type** field.</span></span>

<span data-ttu-id="43f00-108">应计费组件可以在角色和交易类别中定义。</span><span class="sxs-lookup"><span data-stu-id="43f00-108">Chargeable components can be defined on roles, and transaction categories.</span></span>

<span data-ttu-id="43f00-109">对于项目合同子项，角色中定义的应计费仅应用于 **时间** 交易类。</span><span class="sxs-lookup"><span data-stu-id="43f00-109">For a project contract line, the chargeability defined on a role only applies to the **Time** transaction class.</span></span> <span data-ttu-id="43f00-110">如果 **包含时间** 在项目合同子项上设置为 **否**，**应计费角色** 选项卡将不可用。</span><span class="sxs-lookup"><span data-stu-id="43f00-110">If **Include Time** is set to **No** on a project contract line, the **Chargeable roles** tab isn't available.</span></span>

<span data-ttu-id="43f00-111">在项目合同子项的交易类别中定义的应计费仅应用于 **支出** 交易类。</span><span class="sxs-lookup"><span data-stu-id="43f00-111">Chargeability defined on transaction categories for a project contract line only applies to the **Expense** transaction class.</span></span> <span data-ttu-id="43f00-112">如果 **包含支出** 在项目合同子项上设置为 **否**，**应计费类别** 选项卡将不可用。</span><span class="sxs-lookup"><span data-stu-id="43f00-112">If **Include Expenses** is set to **No** on a project contract line, the **Chargeable Categories** tab isn't available.</span></span>

### <a name="update-a-role-to-be-chargeable-or-non-chargeable"></a><span data-ttu-id="43f00-113">将角色更新为应计费或非应计费</span><span class="sxs-lookup"><span data-stu-id="43f00-113">Update a role to be chargeable or non-chargeable</span></span>

<span data-ttu-id="43f00-114">角色在特定的基于项目的合同子项上可以为应计费或非应计费。</span><span class="sxs-lookup"><span data-stu-id="43f00-114">A role can be chargeable or non-chargeable on specific project-based contract line.</span></span>

<span data-ttu-id="43f00-115">在基于项目合同子项的 **应计费角色** 选项卡上，在 **应计费类别** 子网格中的 **计费类型** 字段中，更新角色的计费类型。</span><span class="sxs-lookup"><span data-stu-id="43f00-115">On the **Chargeable roles** tab of a projec-based contract line, on the **Chargeable Categories** subgrid, in the **Billing Type** field, update the billing type for a role.</span></span>

### <a name="update-a-transaction-category-to-be-chargeable-or-non-chargeable"></a><span data-ttu-id="43f00-116">将交易类别更新为应计费或非应计费</span><span class="sxs-lookup"><span data-stu-id="43f00-116">Update a transaction category to be chargeable or non-chargeable</span></span>

<span data-ttu-id="43f00-117">交易类别在特定的基于项目的合同子项上可以为应计费或非应计费。</span><span class="sxs-lookup"><span data-stu-id="43f00-117">A transaction category can be chargeable or non-chargeable on a specific project-based contract line.</span></span>

<span data-ttu-id="43f00-118">在基于项目合同子项的 **应计费类别** 选项卡上，在 **应计费类别** 子网格中的 **计费类型** 字段中，更新交易的计费类型。</span><span class="sxs-lookup"><span data-stu-id="43f00-118">On the **Chargeable Categories** tab of a project-based contract line, on the **Chargeable Categories** subgrid, in the **Billing Type** field, update the billing type for a transaction.</span></span>

### <a name="resolve-chargeability"></a><span data-ttu-id="43f00-119">解析应计费</span><span class="sxs-lookup"><span data-stu-id="43f00-119">Resolve chargeability</span></span>

<span data-ttu-id="43f00-120">仅在合同子项上包含时间且角色在合同子项上配置为应计费时，为时间创建的估计值或实际值才会被视为应计费。</span><span class="sxs-lookup"><span data-stu-id="43f00-120">An estimate or actual created for time will only be considered chargeable if time is included on the contract line, and if the role is configured as chargeable on the contract line.</span></span>

<span data-ttu-id="43f00-121">仅在合同子项上包含支出且交易类别在合同子项上配置为应计费时，为支出创建的估计值或实际值才会被视为应计费。</span><span class="sxs-lookup"><span data-stu-id="43f00-121">An estimate or actual created for expense will only be considered chargeable if expense is included on the contract line, and if the transaction category is configured as chargeable on the contract line.</span></span>

| <span data-ttu-id="43f00-122">包括时间</span><span class="sxs-lookup"><span data-stu-id="43f00-122">Includes time</span></span> | <span data-ttu-id="43f00-123">包括支出</span><span class="sxs-lookup"><span data-stu-id="43f00-123">Includes expense</span></span> | <span data-ttu-id="43f00-124">角色</span><span class="sxs-lookup"><span data-stu-id="43f00-124">Role</span></span> | <span data-ttu-id="43f00-125">类别</span><span class="sxs-lookup"><span data-stu-id="43f00-125">Category</span></span> | <span data-ttu-id="43f00-126">任务</span><span class="sxs-lookup"><span data-stu-id="43f00-126">Task</span></span> |
| --- | --- | --- | --- | --- |
| <span data-ttu-id="43f00-127">是</span><span class="sxs-lookup"><span data-stu-id="43f00-127">Yes</span></span> | <span data-ttu-id="43f00-128">是</span><span class="sxs-lookup"><span data-stu-id="43f00-128">Yes</span></span> | <span data-ttu-id="43f00-129">应计费</span><span class="sxs-lookup"><span data-stu-id="43f00-129">Chargeable</span></span> | <span data-ttu-id="43f00-130">应计费</span><span class="sxs-lookup"><span data-stu-id="43f00-130">Chargeable</span></span> | <span data-ttu-id="43f00-131">时间实际值的计费：应计费</span><span class="sxs-lookup"><span data-stu-id="43f00-131">Billing on a time actual: Chargeable</span></span> </br><span data-ttu-id="43f00-132">支出实际值的计费：应计费</span><span class="sxs-lookup"><span data-stu-id="43f00-132">Billing type on an expense actual: Chargeable</span></span> |
| <span data-ttu-id="43f00-133">是</span><span class="sxs-lookup"><span data-stu-id="43f00-133">Yes</span></span> | <span data-ttu-id="43f00-134">是</span><span class="sxs-lookup"><span data-stu-id="43f00-134">Yes</span></span> | <span data-ttu-id="43f00-135">非应计费</span><span class="sxs-lookup"><span data-stu-id="43f00-135">Non - Chargeable</span></span> | <span data-ttu-id="43f00-136">应计费</span><span class="sxs-lookup"><span data-stu-id="43f00-136">Chargeable</span></span> | <span data-ttu-id="43f00-137">时间实际值的计费：非应计费</span><span class="sxs-lookup"><span data-stu-id="43f00-137">Billing on a time actual: Non-Chargeable</span></span> </br><span data-ttu-id="43f00-138">支出实际值的计费：应计费</span><span class="sxs-lookup"><span data-stu-id="43f00-138">Billing type on an expense actual: Chargeable</span></span> |
| <span data-ttu-id="43f00-139">是</span><span class="sxs-lookup"><span data-stu-id="43f00-139">Yes</span></span> | <span data-ttu-id="43f00-140">是</span><span class="sxs-lookup"><span data-stu-id="43f00-140">Yes</span></span> | <span data-ttu-id="43f00-141">非应计费</span><span class="sxs-lookup"><span data-stu-id="43f00-141">Non-Chargeable</span></span> | <span data-ttu-id="43f00-142">非应计费</span><span class="sxs-lookup"><span data-stu-id="43f00-142">Non-Chargeable</span></span> | <span data-ttu-id="43f00-143">时间实际值的计费：非应计费</span><span class="sxs-lookup"><span data-stu-id="43f00-143">Billing on a time actual: Non-Chargeable</span></span> </br><span data-ttu-id="43f00-144">支出实际值的计费：非应计费</span><span class="sxs-lookup"><span data-stu-id="43f00-144">Billing type on an expense actual: Non-Chargeable</span></span> |
| <span data-ttu-id="43f00-145">No</span><span class="sxs-lookup"><span data-stu-id="43f00-145">No</span></span> | <span data-ttu-id="43f00-146">是</span><span class="sxs-lookup"><span data-stu-id="43f00-146">Yes</span></span> | <span data-ttu-id="43f00-147">无法设置</span><span class="sxs-lookup"><span data-stu-id="43f00-147">Can't be set</span></span> | <span data-ttu-id="43f00-148">应计费</span><span class="sxs-lookup"><span data-stu-id="43f00-148">Chargeable</span></span> | <span data-ttu-id="43f00-149">时间实际值的计费：不可用</span><span class="sxs-lookup"><span data-stu-id="43f00-149">Billing on a time actual: Not available</span></span> </br><span data-ttu-id="43f00-150">支出实际值的计费：应计费</span><span class="sxs-lookup"><span data-stu-id="43f00-150">Billing type on an expense actual:Chargeable</span></span> |
| <span data-ttu-id="43f00-151">No</span><span class="sxs-lookup"><span data-stu-id="43f00-151">No</span></span> | <span data-ttu-id="43f00-152">是</span><span class="sxs-lookup"><span data-stu-id="43f00-152">Yes</span></span> | <span data-ttu-id="43f00-153">无法设置</span><span class="sxs-lookup"><span data-stu-id="43f00-153">Can't be set</span></span> | <span data-ttu-id="43f00-154">非应计费</span><span class="sxs-lookup"><span data-stu-id="43f00-154">Non-Chargeable</span></span> | <span data-ttu-id="43f00-155">时间实际值的计费：不可用</span><span class="sxs-lookup"><span data-stu-id="43f00-155">Billing on a time actual: Not available</span></span> </br><span data-ttu-id="43f00-156">支出实际值的计费：非应计费</span><span class="sxs-lookup"><span data-stu-id="43f00-156">Billing type on an expense actual: Non-chargeable</span></span> |
| <span data-ttu-id="43f00-157">是</span><span class="sxs-lookup"><span data-stu-id="43f00-157">Yes</span></span> | <span data-ttu-id="43f00-158">No</span><span class="sxs-lookup"><span data-stu-id="43f00-158">No</span></span> | <span data-ttu-id="43f00-159">应计费</span><span class="sxs-lookup"><span data-stu-id="43f00-159">Chargeable</span></span> | <span data-ttu-id="43f00-160">无法设置</span><span class="sxs-lookup"><span data-stu-id="43f00-160">Can't be set</span></span> | <span data-ttu-id="43f00-161">时间实际值的计费：应计费</span><span class="sxs-lookup"><span data-stu-id="43f00-161">Billing on a time actual: Chargeable</span></span> </br><span data-ttu-id="43f00-162">支出实际值的计费：不可用</span><span class="sxs-lookup"><span data-stu-id="43f00-162">Billing type on an expense actual: Not available</span></span> |
| <span data-ttu-id="43f00-163">是</span><span class="sxs-lookup"><span data-stu-id="43f00-163">Yes</span></span> | <span data-ttu-id="43f00-164">No</span><span class="sxs-lookup"><span data-stu-id="43f00-164">No</span></span> | <span data-ttu-id="43f00-165">非应计费</span><span class="sxs-lookup"><span data-stu-id="43f00-165">Non-Chargeable</span></span> | <span data-ttu-id="43f00-166">无法设置</span><span class="sxs-lookup"><span data-stu-id="43f00-166">Can't be set</span></span> | <span data-ttu-id="43f00-167">时间实际值的计费：非应计费</span><span class="sxs-lookup"><span data-stu-id="43f00-167">Billing on a time actual: Non-chargeable</span></span> </br> <span data-ttu-id="43f00-168">支出实际值的计费：不可用</span><span class="sxs-lookup"><span data-stu-id="43f00-168">Billing type on an expense actual: Not available</span></span> |


[!INCLUDE[footer-include](../includes/footer-banner.md)]
