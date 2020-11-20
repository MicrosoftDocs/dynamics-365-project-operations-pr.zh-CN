---
title: 估算基于项目的合同子项
description: 此主题提供有关基于项目的合同子项中的估算的信息。
author: rumant
manager: Annbe
ms.date: 10/27/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 24299d997074efcff3776168652809d490c81b17
ms.sourcegitcommit: f6f86e80dfef15a7b5f9174b55dddf410522f7c8
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/31/2020
ms.locfileid: "4180451"
---
# <a name="estimate-a-projectbased-contract-line"></a><span data-ttu-id="9ea37-103">估算基于项目的合同子项</span><span class="sxs-lookup"><span data-stu-id="9ea37-103">Estimate a project–based contract line</span></span>

<span data-ttu-id="9ea37-104">_**适用于：** 面向资源/非库存场景的 Project Operations_</span><span class="sxs-lookup"><span data-stu-id="9ea37-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span> 

<span data-ttu-id="9ea37-105">在 Dynamics 365 Project Operations 中，基于项目的合同子项具有详细信息，帮助估算交付合同子项所涉及的工作的成本和潜在收入。</span><span class="sxs-lookup"><span data-stu-id="9ea37-105">In Dynamics 365 Project Operations, a project-based contract line has details that help estimate the cost and potential revenue of the work involved to deliver the contract line.</span></span>

<span data-ttu-id="9ea37-106">若要估算基于项目的合同子项，请转到基于项目的 **合同子项** 上的 **合同子项详细信息** 选项卡。</span><span class="sxs-lookup"><span data-stu-id="9ea37-106">To estimate a project-based contract line, go to the **Contract Line Detail** tab on the project-based **Contract Line**.</span></span>  <span data-ttu-id="9ea37-107">可通过以下两种方法在基于项目的合同子项上创建估算：</span><span class="sxs-lookup"><span data-stu-id="9ea37-107">There are two ways to create an estimate on a project-based contract line:</span></span>

   - <span data-ttu-id="9ea37-108">通过手动添加合同子项详细信息，直接在合同子项上创建估算。</span><span class="sxs-lookup"><span data-stu-id="9ea37-108">Create an estimate directly on the contract line by manually adding contract line details.</span></span>
   - <span data-ttu-id="9ea37-109">创建项目和项目计划，然后将项目和任务关联到项目的合同子项。</span><span class="sxs-lookup"><span data-stu-id="9ea37-109">Create a project and a project plan, and then associate the project and tasks to the project's contract line.</span></span> <span data-ttu-id="9ea37-110">这样，您可以根据合同子项中包含的组件将项目计划估算导入合同子项。</span><span class="sxs-lookup"><span data-stu-id="9ea37-110">This enables the process by which you can import the project plan estimate into the contract line based on the components included on the contract line.</span></span>

## <a name="create-an-estimate-directly-on-a-projectbased-contract-line"></a><span data-ttu-id="9ea37-111">直接在基于项目的合同子项上创建估算</span><span class="sxs-lookup"><span data-stu-id="9ea37-111">Create an estimate directly on a project–based contract line</span></span>

1. <span data-ttu-id="9ea37-112">转到合同子项，选择 **合同子项详细信息** 选项卡。在此选项卡上创建的合同子项将汇总，显示为此 **合同子项** 的 **合同值**。</span><span class="sxs-lookup"><span data-stu-id="9ea37-112">Go to the contract line and select the **Contract Line Detail** tab. The lines you create on this tab are summarized and display as the **Contracted Value** for this **Contract Line**.</span></span> 
2. <span data-ttu-id="9ea37-113">在 **合同子项详细信息** 子网格中，选择 **+ 新建合同子项详细信息**。</span><span class="sxs-lookup"><span data-stu-id="9ea37-113">In the **Contract Line Details** subgrid, select **+ New Contract Line Detail**.</span></span> <span data-ttu-id="9ea37-114">一个快速创建滑块将打开。</span><span class="sxs-lookup"><span data-stu-id="9ea37-114">A quick-create slider opens.</span></span> <span data-ttu-id="9ea37-115">**合同子项详细信息** 窗体上有以下字段：</span><span class="sxs-lookup"><span data-stu-id="9ea37-115">The following fields are available on the **Contract Line Details** form:</span></span>

| <span data-ttu-id="9ea37-116">字段</span><span class="sxs-lookup"><span data-stu-id="9ea37-116">Field</span></span> | <span data-ttu-id="9ea37-117">地点</span><span class="sxs-lookup"><span data-stu-id="9ea37-117">Location</span></span> | <span data-ttu-id="9ea37-118">描述</span><span class="sxs-lookup"><span data-stu-id="9ea37-118">Description</span></span> | <span data-ttu-id="9ea37-119">下游影响</span><span class="sxs-lookup"><span data-stu-id="9ea37-119">Downstream impact</span></span> |
| --- | --- | --- | --- |
| <span data-ttu-id="9ea37-120">**说明**</span><span class="sxs-lookup"><span data-stu-id="9ea37-120">**Description**</span></span> | <span data-ttu-id="9ea37-121">**快速创建**</span><span class="sxs-lookup"><span data-stu-id="9ea37-121">**Quick Create**</span></span> | <span data-ttu-id="9ea37-122">对特定预估的说明。</span><span class="sxs-lookup"><span data-stu-id="9ea37-122">A description of the specific estimate.</span></span> | <span data-ttu-id="9ea37-123">此字段默认为自动创建的成本的相关合同子项详细信息。</span><span class="sxs-lookup"><span data-stu-id="9ea37-123">This field defaults to the related contract line detail for costs that are automatically created.</span></span> |
| <span data-ttu-id="9ea37-124">**交易分类**</span><span class="sxs-lookup"><span data-stu-id="9ea37-124">**Transaction Class**</span></span> | <span data-ttu-id="9ea37-125">**快速创建**</span><span class="sxs-lookup"><span data-stu-id="9ea37-125">**Quick Create**</span></span> | <span data-ttu-id="9ea37-126">此下拉列表是基于项目的合同子项的 **常规** 选项卡中包含的交易类列表。</span><span class="sxs-lookup"><span data-stu-id="9ea37-126">This drop-down is a list of transaction classes included on the **General** tab of the project-based contract line.</span></span> | <span data-ttu-id="9ea37-127">此字段默认为自动创建的成本的相关合同子项详细信息。</span><span class="sxs-lookup"><span data-stu-id="9ea37-127">This field defaults to the related contract line detail for costs that are automatically created.</span></span> |
| <span data-ttu-id="9ea37-128">**角色**</span><span class="sxs-lookup"><span data-stu-id="9ea37-128">**Role**</span></span> | <span data-ttu-id="9ea37-129">**快速创建**</span><span class="sxs-lookup"><span data-stu-id="9ea37-129">**Quick Create**</span></span> | <span data-ttu-id="9ea37-130">执行此工作或产生此支出的人员的角色。</span><span class="sxs-lookup"><span data-stu-id="9ea37-130">The role of the person who is performing this work or incurring this expense.</span></span> | <span data-ttu-id="9ea37-131">此字段默认为自动创建的成本的相关合同子项详细信息。</span><span class="sxs-lookup"><span data-stu-id="9ea37-131">This field defaults to the related contract line detail for costs that are automatically created.</span></span> |
| <span data-ttu-id="9ea37-132">**类别**</span><span class="sxs-lookup"><span data-stu-id="9ea37-132">**Category**</span></span> | <span data-ttu-id="9ea37-133">**快速创建**</span><span class="sxs-lookup"><span data-stu-id="9ea37-133">**Quick Create**</span></span> | <span data-ttu-id="9ea37-134">工作或支出的类别。</span><span class="sxs-lookup"><span data-stu-id="9ea37-134">The category of the work or expense.</span></span> | <span data-ttu-id="9ea37-135">此字段默认为自动创建的成本的相关合同子项详细信息。</span><span class="sxs-lookup"><span data-stu-id="9ea37-135">This field defaults to the related contract line detail for costs that are automatically created.</span></span> |
| <span data-ttu-id="9ea37-136">**开始日期**</span><span class="sxs-lookup"><span data-stu-id="9ea37-136">**Start Date**</span></span> | <span data-ttu-id="9ea37-137">**快速创建**</span><span class="sxs-lookup"><span data-stu-id="9ea37-137">**Quick Create**</span></span> | <span data-ttu-id="9ea37-138">工作的开始日期。</span><span class="sxs-lookup"><span data-stu-id="9ea37-138">The start date of the work.</span></span> | <span data-ttu-id="9ea37-139">此字段默认为自动创建的成本的相关合同子项详细信息。</span><span class="sxs-lookup"><span data-stu-id="9ea37-139">This field defaults to the related contract line detail for costs that are automatically created.</span></span> |
| <span data-ttu-id="9ea37-140">**结束日期**</span><span class="sxs-lookup"><span data-stu-id="9ea37-140">**End Date**</span></span> | <span data-ttu-id="9ea37-141">**快速创建**</span><span class="sxs-lookup"><span data-stu-id="9ea37-141">**Quick Create**</span></span> | <span data-ttu-id="9ea37-142">工作的结束日期。</span><span class="sxs-lookup"><span data-stu-id="9ea37-142">The end date of the work.</span></span> | <span data-ttu-id="9ea37-143">此字段默认为自动创建的成本的相关合同子项详细信息。</span><span class="sxs-lookup"><span data-stu-id="9ea37-143">This field defaults to the related contract line detail for the cost that is automatically created.</span></span> |
| <span data-ttu-id="9ea37-144">**资源供给公司**</span><span class="sxs-lookup"><span data-stu-id="9ea37-144">**Resourcing Company**</span></span> | <span data-ttu-id="9ea37-145">**快速创建**</span><span class="sxs-lookup"><span data-stu-id="9ea37-145">**Quick Create**</span></span> | <span data-ttu-id="9ea37-146">产生此成本以及提供完成此工作的资源的资源供给公司或法人。</span><span class="sxs-lookup"><span data-stu-id="9ea37-146">The resourcing company or legal entity that is incurring this cost and providing the resource to work on it.</span></span> | <span data-ttu-id="9ea37-147">此字段默认为自动创建的成本的相关合同子项详细信息。</span><span class="sxs-lookup"><span data-stu-id="9ea37-147">This field defaults to the related contract line detail for costs that are automatically created.</span></span> <span data-ttu-id="9ea37-148">此字段也用于成本费检索。</span><span class="sxs-lookup"><span data-stu-id="9ea37-148">This field is also used in cost price retrieval.</span></span> |
| <span data-ttu-id="9ea37-149">**资源单位**</span><span class="sxs-lookup"><span data-stu-id="9ea37-149">**Resourcing Unit**</span></span> | <span data-ttu-id="9ea37-150">**快速创建**</span><span class="sxs-lookup"><span data-stu-id="9ea37-150">**Quick Create**</span></span> | <span data-ttu-id="9ea37-151">产生此成本并提供完成工作的资源的资源提供单位。</span><span class="sxs-lookup"><span data-stu-id="9ea37-151">The resourcing unit that incurs this cost and provies the resource to work on it.</span></span> | <span data-ttu-id="9ea37-152">此字段默认为自动创建的成本的相关合同子项详细信息。</span><span class="sxs-lookup"><span data-stu-id="9ea37-152">This field defaults to the related contract line detail for costs that are automatically created.</span></span> <span data-ttu-id="9ea37-153">此字段也用于成本费检索。</span><span class="sxs-lookup"><span data-stu-id="9ea37-153">This field is also used in cost price retrieval.</span></span> |
| <span data-ttu-id="9ea37-154">**单位计划**</span><span class="sxs-lookup"><span data-stu-id="9ea37-154">**Unit schedule**</span></span> | <span data-ttu-id="9ea37-155">**快速创建**</span><span class="sxs-lookup"><span data-stu-id="9ea37-155">**Quick create**</span></span> | <span data-ttu-id="9ea37-156">工作或支出的计价单位组。</span><span class="sxs-lookup"><span data-stu-id="9ea37-156">The unit group of the work or expense.</span></span> <span data-ttu-id="9ea37-157">单位属于单位计划或单位组。</span><span class="sxs-lookup"><span data-stu-id="9ea37-157">Units belong to a unit schedule or a group of units.</span></span> <span data-ttu-id="9ea37-158">例如，*英里* 和 *公里 (Km)* 是属于描述距离的一组单位的单位。</span><span class="sxs-lookup"><span data-stu-id="9ea37-158">For example, *miles* and *kilometers (Kms)* are units that belong to a group of units that describe distance.</span></span> | <span data-ttu-id="9ea37-159">此字段默认为自动创建的成本的相关合同子项详细信息。</span><span class="sxs-lookup"><span data-stu-id="9ea37-159">This field defaults to the related contract line detail for costs that are automatically created.</span></span> |
| <span data-ttu-id="9ea37-160">**计价单位**</span><span class="sxs-lookup"><span data-stu-id="9ea37-160">**Unit**</span></span> | <span data-ttu-id="9ea37-161">**快速创建**</span><span class="sxs-lookup"><span data-stu-id="9ea37-161">**Quick Create**</span></span> | <span data-ttu-id="9ea37-162">工作或支出的计价单位。</span><span class="sxs-lookup"><span data-stu-id="9ea37-162">The unit of work or expense.</span></span> | <span data-ttu-id="9ea37-163">此字段默认为自动创建的成本的相关合同子项详细信息。</span><span class="sxs-lookup"><span data-stu-id="9ea37-163">This field defaults to the related contract line detail for costs that are automatically created.</span></span> |
| <span data-ttu-id="9ea37-164">**数量**</span><span class="sxs-lookup"><span data-stu-id="9ea37-164">**Quantity**</span></span> | <span data-ttu-id="9ea37-165">**快速创建**</span><span class="sxs-lookup"><span data-stu-id="9ea37-165">**Quick Create**</span></span> | <span data-ttu-id="9ea37-166">工作或支出的数量。</span><span class="sxs-lookup"><span data-stu-id="9ea37-166">The quantity of work or expense.</span></span> | <span data-ttu-id="9ea37-167">此字段默认为自动创建的成本的相关合同子项详细信息。</span><span class="sxs-lookup"><span data-stu-id="9ea37-167">This field defaults to the related contract line detail for costs that are automatically created.</span></span> |
| <span data-ttu-id="9ea37-168">**单价**</span><span class="sxs-lookup"><span data-stu-id="9ea37-168">**Unit price**</span></span> | <span data-ttu-id="9ea37-169">**快速创建**</span><span class="sxs-lookup"><span data-stu-id="9ea37-169">**Quick Create**</span></span> | <span data-ttu-id="9ea37-170">执行工作的角色的帐单费率或支出类别的销售价格。</span><span class="sxs-lookup"><span data-stu-id="9ea37-170">The bill rate of the role that is performing the work or the sales price of the expense category.</span></span> <span data-ttu-id="9ea37-171">此字段根据对开始日期有效的项目价目表上的角色和资源单位组合默认为 **时间**。</span><span class="sxs-lookup"><span data-stu-id="9ea37-171">This field defaults for **Time** based on the role and resourcing unit combination on the project price list that is effective for the start date.</span></span> <span data-ttu-id="9ea37-172">对于支出，此字段的默认值来自于对开始日期有效的项目价目表中交易类别的价格设置。</span><span class="sxs-lookup"><span data-stu-id="9ea37-172">For expenses, this field's default is from the price setup for the transaction category in the project price list that is effective for the start date.</span></span> <span data-ttu-id="9ea37-173">如果交易类别的定价方式不是 **单位成本**，则没有默认值，此字段将保留为空。</span><span class="sxs-lookup"><span data-stu-id="9ea37-173">If the pricing method for the transaction category is not **price-per-unit**, there is no default, and this field is left blank.</span></span> | <span data-ttu-id="9ea37-174">执行工作的角色的成本费率或支出类别的单位成本。</span><span class="sxs-lookup"><span data-stu-id="9ea37-174">The cost rate of the role that is performing the work, or the cost per unit of the expense category.</span></span> <span data-ttu-id="9ea37-175">此字段默认为 **基于角色的时间** 与附加到对开始日期有效的合同签订部门的成本价目表角色价格明细上的资源单位组合。</span><span class="sxs-lookup"><span data-stu-id="9ea37-175">This field defaults for **Time based on the role** and the resourcing unit combination on the role price line of the cost price list attached to the contracting unit effective for the start date.</span></span> <span data-ttu-id="9ea37-176">对于支出，此字段的默认值基于附加到合同签订部门对开始日期有效的成本价目表的类别价格明细。</span><span class="sxs-lookup"><span data-stu-id="9ea37-176">For expenses, this field's default is based on the category price line of the cost price list attached to the contracting unit that is effective for the start date.</span></span> <span data-ttu-id="9ea37-177">如果交易类别的定价方式不是“每单位价格”，则没有默认值，此字段将保留为空。</span><span class="sxs-lookup"><span data-stu-id="9ea37-177">If the pricing method for the transaction category is not price-per-unit, there is no default and this field is left blank.</span></span> |
| <span data-ttu-id="9ea37-178">**预计税款**</span><span class="sxs-lookup"><span data-stu-id="9ea37-178">**Estimated Tax**</span></span> | <span data-ttu-id="9ea37-179">**快速创建**</span><span class="sxs-lookup"><span data-stu-id="9ea37-179">**Quick Create**</span></span> | <span data-ttu-id="9ea37-180">用户输入的此工作或支出的估算税款。</span><span class="sxs-lookup"><span data-stu-id="9ea37-180">The estimated tax for this work or expense as input by the user.</span></span> | <span data-ttu-id="9ea37-181">用户输入的此工作或支出的估算税款。</span><span class="sxs-lookup"><span data-stu-id="9ea37-181">The estimated tax for this work or expense as input by the user.</span></span> |
| <span data-ttu-id="9ea37-182">**金额**</span><span class="sxs-lookup"><span data-stu-id="9ea37-182">**Amount**</span></span> | <span data-ttu-id="9ea37-183">**快速创建**</span><span class="sxs-lookup"><span data-stu-id="9ea37-183">**Quick Create**</span></span> | <span data-ttu-id="9ea37-184">如果 **数量** 和 **价格** 字段保留为空，此字段中的值可以由用户添加。</span><span class="sxs-lookup"><span data-stu-id="9ea37-184">This value in this field can be added by the user if the **Quantity** and **Price** fields are left blank.</span></span> <span data-ttu-id="9ea37-185">如果 **数量** 和 **价格** 已填充，**金额** 字段将为只读，计算公式为 **（数量\*单价）+ 税款**。</span><span class="sxs-lookup"><span data-stu-id="9ea37-185">If **Quantity** and **Price** are filled, the **Amount** field is read-only and is calculated as **(Quantity \* Unit price) + Tax**.</span></span> | &nbsp; |

## <a name="update-prices-on-contract-line-details"></a><span data-ttu-id="9ea37-186">更新合同子项详细信息中的价格</span><span class="sxs-lookup"><span data-stu-id="9ea37-186">Update prices on contract line details</span></span>

<span data-ttu-id="9ea37-187">如果您在附加到合同的项目价目表或合同签订部门的成本价目表上更改了价格，您可以刷新各个合同子项详细信息中的价格来反映更改。</span><span class="sxs-lookup"><span data-stu-id="9ea37-187">If you change prices on the project price list that is attached to the contract or the cost price list of the contracting unit, you can refresh the prices on the individual contract line details to reflect the change.</span></span> <span data-ttu-id="9ea37-188">在 **合同** 页上，选择 **重新计算**。</span><span class="sxs-lookup"><span data-stu-id="9ea37-188">On the **Contract** page, select **Recalculate**.</span></span> <span data-ttu-id="9ea37-189">将打开一个警告，通知您此合同上所有合同子项的价格已重置。</span><span class="sxs-lookup"><span data-stu-id="9ea37-189">A warning opens to inform you that prices for all contract lines on this contract are reset.</span></span> <span data-ttu-id="9ea37-190">选择 **是** 刷新销售和成本合同子项详细信息的价格。</span><span class="sxs-lookup"><span data-stu-id="9ea37-190">Select **Yes** to refresh prices for both sales and cost contract line details.</span></span>

## <a name="access-contract-line-details-for-cost"></a><span data-ttu-id="9ea37-191">访问成本的合同子项详细信息</span><span class="sxs-lookup"><span data-stu-id="9ea37-191">Access contract line details for cost</span></span>

<span data-ttu-id="9ea37-192">在 **合同子项详细信息** 选项卡上，在网格中选择一行以显示子网格工具栏上的操作。</span><span class="sxs-lookup"><span data-stu-id="9ea37-192">On the **Contract Line Details** tab, select a row in the grid to display actions on the toolbar of the subgrid.</span></span> <span data-ttu-id="9ea37-193">子网格工具栏上的第一个操作是 **打开成本详细信息**。</span><span class="sxs-lookup"><span data-stu-id="9ea37-193">The first action on the subgrid tool bar is **Open Cost Detail**.</span></span> <span data-ttu-id="9ea37-194">若要查看此合同子项详细信息的相关成本费率和金额，请选择 **打开成本详细信息**。</span><span class="sxs-lookup"><span data-stu-id="9ea37-194">To see the related cost rate and amount for this contract line detail, select **Open Cost Detail**.</span></span> 

> [!NOTE]
> <span data-ttu-id="9ea37-195">更改 **成本** 的合同子项详细信息中的资源供给公司、资源单位、数量、日期、角色或类别值还将更改 **销售** 的合同子项详细信息中的相应值。</span><span class="sxs-lookup"><span data-stu-id="9ea37-195">Changing the resourcing company, resourcing unit, quantity, dates, role, or category values on the contract line detail for **Cost** also changes the corresponding values on the contract line detail for **Sales**.</span></span>

## <a name="currency-on-contract-line-details-for-cost-and-sales"></a><span data-ttu-id="9ea37-196">成本和销售的合同子项详细信息中的货币</span><span class="sxs-lookup"><span data-stu-id="9ea37-196">Currency on contract line details for cost and sales</span></span>

<span data-ttu-id="9ea37-197">**销售** 的合同子项详细信息设置对合同子项详细信息的开始日期有效的项目价目表中的默认货币。</span><span class="sxs-lookup"><span data-stu-id="9ea37-197">The contract line detail for **Sales** sets the default currency from the project price list that is effective for the start date of the contract line detail.</span></span>

<span data-ttu-id="9ea37-198">**成本** 的合同子项详细信息设置合同的合同签订部门的项目价目表（对 **成本** 的合同子项详细信息的开始日期有效）中的默认货币。</span><span class="sxs-lookup"><span data-stu-id="9ea37-198">The contract line detail for **Cost** sets the default currency from the price list of the contracting unit of the contract that is effective for the start date of the contract line detail for **Cost**.</span></span>

<span data-ttu-id="9ea37-199">利润率计算将 **成本** 和 **销售** 的合同子项详细信息的金额转换为环境的基础货币，来报告合同上的总实际利润和估计利润。</span><span class="sxs-lookup"><span data-stu-id="9ea37-199">Profitability calculations convert the amounts for the contract line details for **Cost** and **Sales** into the base currency of the environment to report the overall actual and estimated margins on the contract.</span></span>

> [!NOTE]
> <span data-ttu-id="9ea37-200">可能会由于缺少有时效性的汇率，出现货币舍入错误和利润变化。</span><span class="sxs-lookup"><span data-stu-id="9ea37-200">Currency rounding errors and changed margins could occur because of the lack of date effective exchange rates.</span></span> <span data-ttu-id="9ea37-201">在项目合同中使用这些计算得出的只是近似值，不能用于需要更高舍入精度并需要了解汇率有效期的实际的法定报告或其他报告。</span><span class="sxs-lookup"><span data-stu-id="9ea37-201">Use these calculations on project contracts only as approximations and not for actual statutory or other reporting that requires higher precision of rounding and awareness of date effectivity for exchange rates.</span></span>