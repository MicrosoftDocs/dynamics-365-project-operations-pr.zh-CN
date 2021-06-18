---
title: 项目成本和收入
description: 此主题介绍如何估算项目成本和收入。
author: ruhercul
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 48f313b15f788645b88a4d878e3bece419d63126
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/10/2021
ms.locfileid: "6009155"
---
# <a name="project-costs-and-revenue"></a><span data-ttu-id="88f86-103">项目成本和收入</span><span class="sxs-lookup"><span data-stu-id="88f86-103">Project costs and revenue</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="88f86-104">项目估算提供项目计划中估算和计划工作的财务视图。</span><span class="sxs-lookup"><span data-stu-id="88f86-104">Project estimates provide the financial view for work that is estimated and scheduled in the project schedule.</span></span> <span data-ttu-id="88f86-105">**项目** 页的 **估算** 选项卡显示您计划的工作的成本和收入影响。</span><span class="sxs-lookup"><span data-stu-id="88f86-105">The **Estimates** tab on the **Projects** page shows the cost and revenue impact of the work that you’re planning.</span></span> <span data-ttu-id="88f86-106">还提供有关大量预定义维度的信息。</span><span class="sxs-lookup"><span data-stu-id="88f86-106">It also provides information about many predefined dimensions.</span></span> 

> ![“估算”选项卡](media/project-5.png)

## <a name="cost-and-sales-values-of-the-project"></a><span data-ttu-id="88f86-108">项目的成本和销售值</span><span class="sxs-lookup"><span data-stu-id="88f86-108">Cost and sales values of the project</span></span>

<span data-ttu-id="88f86-109">价目表定义项目中的角色的成本和记帐费率。</span><span class="sxs-lookup"><span data-stu-id="88f86-109">Price lists define the cost and bill rates for roles in a project.</span></span> <span data-ttu-id="88f86-110">可以根据与职位名称关联的角色和为任务分派的指定资源确定工作的成本和收入影响。</span><span class="sxs-lookup"><span data-stu-id="88f86-110">You can determine the cost and revenue impact of the work, based on the roles that are associated with the position name and the named resource that is assigned to a task.</span></span> <span data-ttu-id="88f86-111">如果没有为任务进行任何分派（通用资源和指定资源），则不能获取成本或销售估算。</span><span class="sxs-lookup"><span data-stu-id="88f86-111">If there are tasks that don't have any assignments (generic or named), you can’t get cost or sales estimates.</span></span> <span data-ttu-id="88f86-112">成本和销售值使用价目表中定义的日期。</span><span class="sxs-lookup"><span data-stu-id="88f86-112">Cost and sales values consider the date that is defined in the price lists.</span></span>

### <a name="default-cost-price"></a><span data-ttu-id="88f86-113">默认成本费</span><span class="sxs-lookup"><span data-stu-id="88f86-113">Default cost price</span></span>  

<span data-ttu-id="88f86-114">所有项目都属于组织。</span><span class="sxs-lookup"><span data-stu-id="88f86-114">Every project belongs to an organization.</span></span> <span data-ttu-id="88f86-115">此组织在项目中的 **合同签订部门** 字段中显示。</span><span class="sxs-lookup"><span data-stu-id="88f86-115">This organization is shown in the **Contracting Unit** field in the project.</span></span> <span data-ttu-id="88f86-116">与合同签订部门关联的价目表用于确定成本单价。</span><span class="sxs-lookup"><span data-stu-id="88f86-116">The price list that is associated with the contracting unit is used to determine the unit cost price.</span></span> <span data-ttu-id="88f86-117">若要确定角色在估算明细中定义的日期的正确成本费，请在成本价目表中搜索角色、单位和部门的组合。</span><span class="sxs-lookup"><span data-stu-id="88f86-117">To determine the correct cost prices on roles for the date that is defined on estimate lines, search for the combination of role, unit, and organizational unit in the cost price list.</span></span> 

<span data-ttu-id="88f86-118">这样就可以计算其成本费，并且必须将所有任务分派给一项资源。</span><span class="sxs-lookup"><span data-stu-id="88f86-118">So that their cost prices can be calculated, all tasks must be assigned to a resource.</span></span> <span data-ttu-id="88f86-119">所有未分派任务的成本费均为 0.00。</span><span class="sxs-lookup"><span data-stu-id="88f86-119">Any uwnassigned tasks will have a cost price of 0.00.</span></span>

<span data-ttu-id="88f86-120">如果角色、单位和部门的组合不从合同签订部门的价目表返回成本费，系统将忽略单位。</span><span class="sxs-lookup"><span data-stu-id="88f86-120">If the combination of role, unit, and organizational unit doesn't return a cost price from the contracting unit's price list, the system ignores the unit.</span></span> <span data-ttu-id="88f86-121">而是搜索仅角色和部门的组合。</span><span class="sxs-lookup"><span data-stu-id="88f86-121">Instead, it searches for the combination of just role and organizational unit.</span></span> <span data-ttu-id="88f86-122">如果发现了成本费，将使用换算系数将其转换为您在估算明细中选择的单位。</span><span class="sxs-lookup"><span data-stu-id="88f86-122">If a cost price is found, conversion factors are used to convert it to the unit that you selected on the estimate line.</span></span>

<span data-ttu-id="88f86-123">如果角色和部门的组合不返回成本费，系统将忽略部门。</span><span class="sxs-lookup"><span data-stu-id="88f86-123">If the combination of role and organizational unit doesn't return a cost price, the system ignores the organizational unit.</span></span> <span data-ttu-id="88f86-124">而是搜索角色和单位的组合以设置默认价格（在应用所有转换后）。</span><span class="sxs-lookup"><span data-stu-id="88f86-124">Instead, it searches for the combination of role and unit to set the default price (after any conversion is applied).</span></span>

<span data-ttu-id="88f86-125">如果系统未发现该角色的价格，则估算明细中的成本费设置为默认值 **0.00**。</span><span class="sxs-lookup"><span data-stu-id="88f86-125">If the system doesn't find a price for the role, the cost price on the estimate line is set to a default value of **0.00**.</span></span> <span data-ttu-id="88f86-126">项目成本估算明细上的所有成本额以合同签订部门的货币记录。</span><span class="sxs-lookup"><span data-stu-id="88f86-126">All cost amounts on the project cost estimate lines are recorded in the currency of the contracting unit.</span></span>

> [!NOTE]
> <span data-ttu-id="88f86-127">默认情况下， Microsoft Dynamics 365 使用您的基础货币存储成本金额。</span><span class="sxs-lookup"><span data-stu-id="88f86-127">By default, Microsoft Dynamics 365 stores cost amounts in your base currency.</span></span> <span data-ttu-id="88f86-128">但是，**估算** 选项卡上显示的成本金额采用合同签订部门的货币。</span><span class="sxs-lookup"><span data-stu-id="88f86-128">However, the cost amounts that are shown on the **Estimates** tab are in the currency of the contracting unit.</span></span>  

### <a name="default-sales-price"></a><span data-ttu-id="88f86-129">默认销售价</span><span class="sxs-lookup"><span data-stu-id="88f86-129">Default sales price</span></span> 

<span data-ttu-id="88f86-130">销售价目表由项目附加到的销售实体或由项目客户决定。</span><span class="sxs-lookup"><span data-stu-id="88f86-130">The sales price list is determined by either the sales entity that the project is attached to or the project customer.</span></span> <span data-ttu-id="88f86-131">如果将销售实体（如商机、报价单或合同）与项目关联，该销售实体的销售价由与报价单或合同关联的价目表决定。</span><span class="sxs-lookup"><span data-stu-id="88f86-131">When a sales entity, such as opportunity, quote, or contract, is associated with the project, the sales entity's sales price is determined by the price list that is associated with the quote or contract.</span></span> <span data-ttu-id="88f86-132">如果报价单或合同具有自定义价目表，此价目表将用作项目估算的默认销售价目表。</span><span class="sxs-lookup"><span data-stu-id="88f86-132">If the quote or contract has a custom price list, that price list is used as the default sales price list for project estimates.</span></span> <span data-ttu-id="88f86-133">如果销售实体没有关联项，将把参数中的默认销售价目表用作由项目中定义的客户货币匹配的项目默认销售价目表。</span><span class="sxs-lookup"><span data-stu-id="88f86-133">If there is no association with sales entities, the default sales price list from the parameters is used as the project's default sales price list matched by the customer currency that is defined on the project.</span></span>

<span data-ttu-id="88f86-134">每个估算明细都有关联的资源单位。</span><span class="sxs-lookup"><span data-stu-id="88f86-134">Each estimate line has a resourcing unit that is associated with it.</span></span> <span data-ttu-id="88f86-135">资源单位指示为完成任务而预订的资源所属部门。</span><span class="sxs-lookup"><span data-stu-id="88f86-135">The resourcing unit indicates the organizational unit that resources are booked from to complete the task.</span></span> <span data-ttu-id="88f86-136">若要确定关联角色的销售价，请在销售价目表中搜索角色、单位和资源单位的组合。</span><span class="sxs-lookup"><span data-stu-id="88f86-136">To determine the sales price for the associated roles, search for the combination of role, unit, and resourcing unit in the sales price list.</span></span> <span data-ttu-id="88f86-137">如果没有为任务进行分派，则任务的销售价为 0.00。</span><span class="sxs-lookup"><span data-stu-id="88f86-137">If there are no assignments on the task, the sales price for the task is 0.00.</span></span>

<span data-ttu-id="88f86-138">如果角色、单位和资源单位的组合不从销售价目表返回销售价，系统将忽略单位。</span><span class="sxs-lookup"><span data-stu-id="88f86-138">If the combination of role, unit, and resourcing unit doesn't return a sales price from the sales price list, the system ignores the unit.</span></span> <span data-ttu-id="88f86-139">而是搜索仅角色和资源单位的组合。</span><span class="sxs-lookup"><span data-stu-id="88f86-139">Instead, it searches for the combination of just role and resourcing unit.</span></span> <span data-ttu-id="88f86-140">如果发现了销售价，将使用换算系数将其转换为您在销售估算明细中选择的单位。</span><span class="sxs-lookup"><span data-stu-id="88f86-140">If a sales price is found, conversion factors are used to convert it to the unit that you selected on the sales estimate line.</span></span> 

<span data-ttu-id="88f86-141">如果角色和资源单位的组合不从销售价目表返回销售价，系统将忽略资源单位。</span><span class="sxs-lookup"><span data-stu-id="88f86-141">If the combination of role and resourcing unit doesn't return a sales price from the sales price list, the system ignores the resourcing unit.</span></span> <span data-ttu-id="88f86-142">而是搜索角色和单位的组合以设置默认价格（在应用所有转换后）。</span><span class="sxs-lookup"><span data-stu-id="88f86-142">Instead, it searches for the combination of role and unit to set the default price (after any conversion is applied).</span></span>

<span data-ttu-id="88f86-143">如果系统未发现该角色的价格，则估算明细中的销售价设置为默认值 **0.00**。</span><span class="sxs-lookup"><span data-stu-id="88f86-143">If the system doesn't find a price for the role, the sales price on the estimate line is set to a default value of **0.00**.</span></span>

<span data-ttu-id="88f86-144">**估算** 选项卡有一个网格视图，其中显示估算明细。</span><span class="sxs-lookup"><span data-stu-id="88f86-144">The **Estimates** tab has a grid view that shows estimate lines.</span></span> <span data-ttu-id="88f86-145">网格中包含单位、总成本费和总销售价的列，如下图中所示。</span><span class="sxs-lookup"><span data-stu-id="88f86-145">The grid includes columns for the unit, total cost price, and total sales price, as shown in the following illustration.</span></span> 

> ![“估算”选项卡中的网格视图](media/project-6.png)

## <a name="time-phased-view-of-project-estimates"></a><span data-ttu-id="88f86-147">项目估算的分时段视图</span><span class="sxs-lookup"><span data-stu-id="88f86-147">Time-phased view of project estimates</span></span>

<span data-ttu-id="88f86-148">项目估算的分时段视图按照您选择的时间刻度显示时间线内网格视图的估算数据。</span><span class="sxs-lookup"><span data-stu-id="88f86-148">The time-phased view of project estimates shows the estimate data from the grid view across the timeline, in a time scale that you select.</span></span> <span data-ttu-id="88f86-149">默认情况下，按 **角色** 维度透视估算数据。</span><span class="sxs-lookup"><span data-stu-id="88f86-149">By default, the estimate data is pivoted on the **Role** dimension.</span></span>

> ![项目估算的分时段视图](media/project-7.png)

## <a name="allocating-estimated-effort-based-on-the-task-mode"></a><span data-ttu-id="88f86-151">基于任务模式分配估算的工作量</span><span class="sxs-lookup"><span data-stu-id="88f86-151">Allocating estimated effort based on the task mode</span></span>

<span data-ttu-id="88f86-152">在分时段视图中，通过分配所选时间刻度的每单位时间段工作量时数来分配估算的总工作量。</span><span class="sxs-lookup"><span data-stu-id="88f86-152">In the time-phased view, you distribute the total effort that is estimated for the task by allocating effort hours per unit time period in the selected time scale.</span></span> <span data-ttu-id="88f86-153">任务模式确定如何在任务的持续时间内分配工作量。</span><span class="sxs-lookup"><span data-stu-id="88f86-153">The task mode determines how effort is allocated across the duration of the task.</span></span> <span data-ttu-id="88f86-154">这两种分配分别为 **平均** 分配和 **基于工作时间的** 分配。</span><span class="sxs-lookup"><span data-stu-id="88f86-154">The two kinds of allocation are **Even** and **Work hours–based**.</span></span>

### <a name="work-hours-based-allocation"></a><span data-ttu-id="88f86-155">基于工作时间的分配</span><span class="sxs-lookup"><span data-stu-id="88f86-155">Work hours-based allocation</span></span>
 
<span data-ttu-id="88f86-156">在自动计划任务模式中，按完整工作时间费率设置任务资源的日默认工时。</span><span class="sxs-lookup"><span data-stu-id="88f86-156">In auto-scheduling task mode, the daily default hours for task resources are set at the full work hour rate.</span></span> <span data-ttu-id="88f86-157">当通过在分时段视图中在任务的持续时间内进行分割来分配工作量时，适用此行为。</span><span class="sxs-lookup"><span data-stu-id="88f86-157">This behavior applies when effort is allocated by splitting it across the duration of the task in the time-phased view.</span></span> <span data-ttu-id="88f86-158">例如，如果估计在 **天** 时间刻度内一项资源可以完成某项任务，则每天分配的工作量将不会超过项目日历中定义的每天工作时间。</span><span class="sxs-lookup"><span data-stu-id="88f86-158">For example, if you estimate that a task will be completed by one resource in the **Day** time scale, the effort that is allocated per day won't exceed the work hours per day that are defined in the project calendar.</span></span> <span data-ttu-id="88f86-159">因此，工作量分配总是确保资源估计可使用一整天。</span><span class="sxs-lookup"><span data-stu-id="88f86-159">Therefore, the effort allocation always makes sure that the resources are estimated to be used for the full day.</span></span>

### <a name="even-allocation"></a><span data-ttu-id="88f86-160">平均分配</span><span class="sxs-lookup"><span data-stu-id="88f86-160">Even allocation</span></span>

<span data-ttu-id="88f86-161">在手动计划任务模式中，不使用项目日历中的工作时间。</span><span class="sxs-lookup"><span data-stu-id="88f86-161">In manually scheduled task mode, the work hours from the project calendar aren't used.</span></span> <span data-ttu-id="88f86-162">相反，任务计划基于用户输入。</span><span class="sxs-lookup"><span data-stu-id="88f86-162">Instead, the task schedule is based on user input.</span></span> <span data-ttu-id="88f86-163">对于这些任务，所选时间刻度的每单位时间工作量分配没有任何限制因素。</span><span class="sxs-lookup"><span data-stu-id="88f86-163">For these tasks, the effort allocation per unit time period in the selected time scale doesn't have any limiting factor.</span></span> <span data-ttu-id="88f86-164">任务的总工作量均匀分割并对所选时间刻度内的每单位时间进行分配。</span><span class="sxs-lookup"><span data-stu-id="88f86-164">The total effort on the task is equally split and allocated for each unit time period in the selected time scale.</span></span> <span data-ttu-id="88f86-165">因此，在任务上定义的任务模式确定工作量分配或分时段估算中每单位时间的工作量分配。</span><span class="sxs-lookup"><span data-stu-id="88f86-165">Therefore, the task mode that is defined on the task determines the effort distribution, or the allocation of effort per unit time period in time-phased estimates.</span></span>

## <a name="grouping-and-time-phasing-options"></a><span data-ttu-id="88f86-166">分组和分时段选项</span><span class="sxs-lookup"><span data-stu-id="88f86-166">Grouping and time-phasing options</span></span>

<span data-ttu-id="88f86-167">分时段视图显示每天、每周、每月或每年的工作量、成本和销售估算的分配。</span><span class="sxs-lookup"><span data-stu-id="88f86-167">The time-phased view shows the distribution of the effort, cost, and sales estimates on a daily, weekly, monthly, or yearly basis.</span></span> <span data-ttu-id="88f86-168">默认情况下，按 **角色** 维度透视估算数据。</span><span class="sxs-lookup"><span data-stu-id="88f86-168">By default, the estimate data is pivoted on the **Role** dimension.</span></span> <span data-ttu-id="88f86-169">但是，可使用 **分组依据** 选项透视其他两个维度：**类别** 和 **资源**。</span><span class="sxs-lookup"><span data-stu-id="88f86-169">However, you can use the **Group By** option to pivot on two other dimensions: **Category** and **Resource**.</span></span>

<span data-ttu-id="88f86-170">在网格视图和分时段视图中，都可以选择要显示哪些字段。</span><span class="sxs-lookup"><span data-stu-id="88f86-170">In both the grid view and the time-phased view, you can select which fields are shown.</span></span> <span data-ttu-id="88f86-171">每个时段的总计在项目底部显示。</span><span class="sxs-lookup"><span data-stu-id="88f86-171">Totals for each time block are shown at the bottom of the project.</span></span> <span data-ttu-id="88f86-172">其显示天、周、月或年的总估算工作量、成本和销售额。</span><span class="sxs-lookup"><span data-stu-id="88f86-172">They show the total estimated effort, cost, and sales for the day, week, month, or year.</span></span> <span data-ttu-id="88f86-173">默认成本费和销售价具有时效性。</span><span class="sxs-lookup"><span data-stu-id="88f86-173">The default cost price and sales price are date-effective.</span></span> <span data-ttu-id="88f86-174">换句话说，根据您选择的分时段视图对每个资源改变。</span><span class="sxs-lookup"><span data-stu-id="88f86-174">In other words, they change for each resource, based on the time-phased view that you select.</span></span>

## <a name="expense-estimates"></a><span data-ttu-id="88f86-175">费用估算</span><span class="sxs-lookup"><span data-stu-id="88f86-175">Expense estimates</span></span>

<span data-ttu-id="88f86-176">网格视图中的 **添加新的支出估算** 按钮用于记录项目中发生，但是与人工没有直接关系的任何支出。</span><span class="sxs-lookup"><span data-stu-id="88f86-176">The **Add a New Expense Estimate** button in the grid view lets you record any expenses that are incurred in the project, but that aren't directly related to labor.</span></span> <span data-ttu-id="88f86-177">可记录特定任务或整个项目的支出估算。</span><span class="sxs-lookup"><span data-stu-id="88f86-177">You can record the expense estimates for a specific task or for the entire project.</span></span> <span data-ttu-id="88f86-178">选择支出类别和预计要产生支出的暂定日期。</span><span class="sxs-lookup"><span data-stu-id="88f86-178">Select expense categories and the tentative date when you expect to incur the expense.</span></span> <span data-ttu-id="88f86-179">如果相关成本价目表和销售价目表具有默认价格（或为支出类别定义了加价百分比），则在关联时在估算明细中自动输入这些默认值。</span><span class="sxs-lookup"><span data-stu-id="88f86-179">If the associated cost price list and sales price list have default prices (or if markup percentages are defined for expense categories), they are automatically entered on the estimate line when the association occurs.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]