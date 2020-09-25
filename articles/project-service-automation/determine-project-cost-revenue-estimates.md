---
title: 确定项目成本和收入预计
description: 如何在 Project Service 中确定项目成本和收入估算
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: cfa3c0c6-a57d-4d50-90dd-9a517d380257
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 2fd581cdb84a3a1c0dbbd1b9b27d87ddd959f883
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/24/2020
ms.locfileid: "3749670"
---
# <a name="determine-project-cost-and-revenue-estimates"></a><span data-ttu-id="0727b-103">确定项目成本和收入预计</span><span class="sxs-lookup"><span data-stu-id="0727b-103">Determine project cost and revenue estimates</span></span> 

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="0727b-104">项目估算提供项目工作分解结构中预计和计划工作的财务视图。</span><span class="sxs-lookup"><span data-stu-id="0727b-104">Project estimates provide the financial view for the work estimated and scheduled in the project’s work breakdown structure.</span></span> <span data-ttu-id="0727b-105">估算视图通知您计划工作的成本和收入影响。</span><span class="sxs-lookup"><span data-stu-id="0727b-105">The estimates view informs you of the cost and revenue impact of the planned work.</span></span> <span data-ttu-id="0727b-106">估算视图提供查看有关大量预定义维度的信息的一种工具，以让您最佳了解项目的财务影响。</span><span class="sxs-lookup"><span data-stu-id="0727b-106">The estimates view provides a tool to see the information on a number of pre-defined dimensions to best inform you of the financial impact of the project.</span></span>  
  
## <a name="cost-and-sales-value-of-the-project"></a><span data-ttu-id="0727b-107">项目的成本和销售值</span><span class="sxs-lookup"><span data-stu-id="0727b-107">Cost and sales value of the project</span></span>  
[!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]<span data-ttu-id="0727b-108">价目表定义项目所使用角色的成本和记帐费率。</span><span class="sxs-lookup"><span data-stu-id="0727b-108">price lists define the cost and bill rates for roles projects use.</span></span> <span data-ttu-id="0727b-109">根据与项目工作分解结构中任务相关的角色，您可以确定所涉及工作的成本和收入影响。</span><span class="sxs-lookup"><span data-stu-id="0727b-109">Based on the roles associated with the tasks in the project’s work breakdown structure, you can determine the cost and revenue impact of the work involved.</span></span>  
  
## <a name="cost-price-defaulting"></a><span data-ttu-id="0727b-110">默认成本费</span><span class="sxs-lookup"><span data-stu-id="0727b-110">Cost price defaulting</span></span>  
<span data-ttu-id="0727b-111">每个项目属于一个组织（在项目的**负责部门**中指示）。</span><span class="sxs-lookup"><span data-stu-id="0727b-111">Every project belongs to an organization (indicated in **Owning Unit** in the project).</span></span> <span data-ttu-id="0727b-112">与负责部门相关的价目表确定单位成本费。</span><span class="sxs-lookup"><span data-stu-id="0727b-112">The price list associated with the owning organizational unit determines the unit cost price.</span></span> <span data-ttu-id="0727b-113">[!INCLUDE[pn_dyn_365_project_service_auto](../includes/pn-dyn-365-project-service-auto.md)]通过在成本价目表中搜索角色、单位和部门的组合来确定角色的成本费，以获得估算明细生效日期的正确成本费。</span><span class="sxs-lookup"><span data-stu-id="0727b-113">The [!INCLUDE[pn_dyn_365_project_service_auto](../includes/pn-dyn-365-project-service-auto.md)] determine cost prices for roles by searching for the combination of role, unit, and organizational unit in the cost price list to get the correct cost price for the date effective on estimate lines.</span></span>  
  
<span data-ttu-id="0727b-114">如果角色、单位和</span><span class="sxs-lookup"><span data-stu-id="0727b-114">If the combination of role, unit.</span></span> <span data-ttu-id="0727b-115">部门的组合不导致来自负责部门价目表的成本费，则为了支持角色和部门的组合，该单位将被忽略。</span><span class="sxs-lookup"><span data-stu-id="0727b-115">and organizational unit doesn’t result in a cost price from the owning unit’s price list, the unit is disregarded in favor of the combination of role and organizational unit.</span></span> <span data-ttu-id="0727b-116">如果存在成本费，此价格将转换为您在估算明细上选择的单位。</span><span class="sxs-lookup"><span data-stu-id="0727b-116">If there is a cost price, this price is converted to the unit you chose on the estimate line.</span></span>  
  
<span data-ttu-id="0727b-117">如果角色和部门的组合不导致成本费，则为了支持角色和部门组合，部门将被忽略，并且如果需要，在应用任何转换后，价格为默认价格。</span><span class="sxs-lookup"><span data-stu-id="0727b-117">If the combination of role and organizational unit doesn’t result in a cost price, the organizational unit is disregarded in favor of the role and unit combination, and the price is defaulted after applying any conversion, if required.</span></span>  
  
 <span data-ttu-id="0727b-118">如果该角色没有价格，则成本费在估算明细上默认为 0.00。</span><span class="sxs-lookup"><span data-stu-id="0727b-118">If there isn’t a price for the role, then the cost price defaults to 0.00 on the estimate line.</span></span>  
  
 <span data-ttu-id="0727b-119">项目成本估算明细上的所有成本额以负责部门的货币记帐。</span><span class="sxs-lookup"><span data-stu-id="0727b-119">All cost amounts on project cost estimate lines are in the currency of the owning organizational unit.</span></span>  
  
## <a name="sales-price-defaulting"></a><span data-ttu-id="0727b-120">默认售价</span><span class="sxs-lookup"><span data-stu-id="0727b-120">Sales price defaulting</span></span>  
<span data-ttu-id="0727b-121">销售价目表基于项目被附加的销售实体。</span><span class="sxs-lookup"><span data-stu-id="0727b-121">The sales price list is based on the sales entity that the project is attached to.</span></span> <span data-ttu-id="0727b-122">与报价单或合同相关的销售价目表确定销售单价。</span><span class="sxs-lookup"><span data-stu-id="0727b-122">The sales price list associated with the quote or contract determines the unit sales price.</span></span> <span data-ttu-id="0727b-123">如果报价单或合同具有自定义价目表，此价目表将为项目估算的默认销售价目表。</span><span class="sxs-lookup"><span data-stu-id="0727b-123">If the quote or contract has a custom price list, this will be the default sales price list for project estimates.</span></span> <span data-ttu-id="0727b-124">如果与销售实体没有关联，则在参数设置中配置的默认销售价目表将为项目的默认销售价目表。</span><span class="sxs-lookup"><span data-stu-id="0727b-124">If there is no association to the sales entities, then the default sales price list configured in parameters settings will be the default sales price list for the project.</span></span> <span data-ttu-id="0727b-125">每个估算明细都具有关联的资源部门，以指示为完成任务将预订其资源的部门。</span><span class="sxs-lookup"><span data-stu-id="0727b-125">Each estimate line has a resource organizational unit associated to indicate the organizational unit from which the resources will be booked for completing the task.</span></span> <span data-ttu-id="0727b-126">关联角色的售价通过在销售价目表中搜索角色、单位和资源部门的组合来确定，以获得估算明细生效日期的正确售价。</span><span class="sxs-lookup"><span data-stu-id="0727b-126">The sales price for the associated roles is determined by searching for the combination of role, unit, and resource organizational unit in the sales price list to get the correct sales price for the date effective on the estimate lines.</span></span>  
  
<span data-ttu-id="0727b-127">如果角色、单位和资源部门的组合不导致销售价目表中的售价，则系统将忽略单位，并将搜索角色和资源部门的组合。</span><span class="sxs-lookup"><span data-stu-id="0727b-127">If the combination of role, unit, and resource organizational unit doesn’t result in a sales price from the sales price list, the system will disregard unit and search for the combination of role and resource organizational unit.</span></span> <span data-ttu-id="0727b-128">如果发现有售价，此售价将转换为您在销售估算明细上选择的单位。</span><span class="sxs-lookup"><span data-stu-id="0727b-128">If a sales price is found, this will be converted to the unit you chose on the sales estimate line.</span></span>  
  
<span data-ttu-id="0727b-129">如果系统未发现该角色的价格，则售价在估算明细上必须默认为 0.00。</span><span class="sxs-lookup"><span data-stu-id="0727b-129">If the system doesn’t find a price for the role, then the sales price must default to 0.00 on the estimate line.</span></span>  
  
<span data-ttu-id="0727b-130">估算视图具有一个网格视图，该视图显示了具有单位、总成本和售价的估算明细的平面网格。</span><span class="sxs-lookup"><span data-stu-id="0727b-130">The estimates view has a grid view that displays a flat grid of estimate lines with unit and total cost and sales price.</span></span>  
  
## <a name="time-phased-view-of-project-estimates"></a><span data-ttu-id="0727b-131">项目估算的分时段视图</span><span class="sxs-lookup"><span data-stu-id="0727b-131">Time-phased view of project estimates</span></span>  
<span data-ttu-id="0727b-132">在项目估算的分时段视图中，网格视图中的估算数据默认按角色透视，并显示所选时间刻度的某个时间表的一系列估算数据。</span><span class="sxs-lookup"><span data-stu-id="0727b-132">In the time-phased view for project estimates, the estimates data from the grid view is pivoted by default by role, and shows a spread of estimate data across the timeline in the chosen timescale.</span></span>  
  
## <a name="effort-estimate-allocation-based-on-task-mode"></a><span data-ttu-id="0727b-133">基于任务模式的工作量估算分配</span><span class="sxs-lookup"><span data-stu-id="0727b-133">Effort estimate allocation based on task mode</span></span>  
<span data-ttu-id="0727b-134">在分时段视图中，通过分配所选时间刻度的每单位时间的特定工作量小时数来发布任务的总估算工作量。</span><span class="sxs-lookup"><span data-stu-id="0727b-134">In the time-phased view, total effort estimated for the task is distributed by allocating a certain number of effort hours per unit time period of the chosen timescale.</span></span> <span data-ttu-id="0727b-135">在 Project Service 中，任务模式确定如何在任务的持续时间内分配工作量。</span><span class="sxs-lookup"><span data-stu-id="0727b-135">In project service, the task mode determines how effort is allocated across the duration of the task.</span></span> <span data-ttu-id="0727b-136">这两种分配分别为均匀分配和基于工作时间的分配</span><span class="sxs-lookup"><span data-stu-id="0727b-136">The two kinds of allocation are even allocation and work hours based allocation</span></span>  
  
## <a name="work-hours-based-allocation"></a><span data-ttu-id="0727b-137">基于工作时间的分配</span><span class="sxs-lookup"><span data-stu-id="0727b-137">Work hours based allocation</span></span>  
<span data-ttu-id="0727b-138">任务的自动计划任务模式管理对于任务估算的资源数，估算为每天完整工作时间要使用的资源数。</span><span class="sxs-lookup"><span data-stu-id="0727b-138">Auto scheduling task mode for a task governs that for the number of resources estimated on the task, they are estimated to be utilized for the full work hours per day.</span></span> <span data-ttu-id="0727b-139">当通过在分时段视图中在任务的持续时间内进行分割来分配工作量时，上述也适用。</span><span class="sxs-lookup"><span data-stu-id="0727b-139">This applies when allocating the effort by splitting it across the duration of tasks in the time phased view as well.</span></span> <span data-ttu-id="0727b-140">例如，在“天”时间刻度，对于估算通过一个资源完工的任务，每天分配的工作量将不会超过项目日历中定义的每天工作时间。</span><span class="sxs-lookup"><span data-stu-id="0727b-140">For instance, on a ‘Day’ timescale, for a task estimated to be completed by one resource, the effort allocated per day will not exceed work hours per day defined in the project’s calendar.</span></span> <span data-ttu-id="0727b-141">因此，工作量分配总是确保资源估计可使用一整天。</span><span class="sxs-lookup"><span data-stu-id="0727b-141">Therefore, the effort allocation always ensures that the resources are estimated to be utilized for the full day.</span></span>  
  
## <a name="even-distribution"></a><span data-ttu-id="0727b-142">均匀分配</span><span class="sxs-lookup"><span data-stu-id="0727b-142">Even distribution</span></span>  
<span data-ttu-id="0727b-143">手动计划任务模式不接受任务上定义的工作时间、项目日历或资源数。</span><span class="sxs-lookup"><span data-stu-id="0727b-143">Manually scheduled task mode doesn't honor the work hours, project calendar, or number of resources defined on the task.</span></span> <span data-ttu-id="0727b-144">任务计划基于用户输入。</span><span class="sxs-lookup"><span data-stu-id="0727b-144">The task schedule is based on user input.</span></span> <span data-ttu-id="0727b-145">对于此类任务，所选时间刻度的每单位时间工作量分配没有任何限制因素。</span><span class="sxs-lookup"><span data-stu-id="0727b-145">For such tasks, the effort allocation per unit time period of the chosen timescale doesn't have any limiting factors.</span></span> <span data-ttu-id="0727b-146">任务的总工作量均匀分割并对所选时间刻度上的每单位时间进行分配。</span><span class="sxs-lookup"><span data-stu-id="0727b-146">The total effort on the task is equally split and allocated for each unit time period on the chosen timescale.</span></span>  
  
<span data-ttu-id="0727b-147">这样，在任务上定义的任务模式确定工作量分配或分时段估算中每单位时间的工作量分配。</span><span class="sxs-lookup"><span data-stu-id="0727b-147">In this way, the task mode defined on the task determines the effort distribution or allocation of effort per unit time period in time-phased estimates.</span></span>  
  
## <a name="grouping-and-time-phasing-options"></a><span data-ttu-id="0727b-148">分组和分时段选项</span><span class="sxs-lookup"><span data-stu-id="0727b-148">Grouping and time-phasing options</span></span>  
<span data-ttu-id="0727b-149">该视图可帮助您了解每天、每周、每月或每年的工作量、成本和销售估算的分配。</span><span class="sxs-lookup"><span data-stu-id="0727b-149">This view helps you understand the distribution of the effort, cost, and sales estimates on a per day, week, month, or year basis.</span></span> <span data-ttu-id="0727b-150">按选项分组允许在两个其他维度透视估算数据：类别和资源。</span><span class="sxs-lookup"><span data-stu-id="0727b-150">The Group By option allows pivoting the estimates data on two other dimensions: category and resource.</span></span> <span data-ttu-id="0727b-151">在网格视图和分时段视图上，您可以选择要显示的字段。</span><span class="sxs-lookup"><span data-stu-id="0727b-151">On both the grid view and the time-phased view you can choose the fields to be displayed.</span></span> <span data-ttu-id="0727b-152">每个时间块的总值显示在底部，指示该日、周、月或年的总估算工作量、成本</span><span class="sxs-lookup"><span data-stu-id="0727b-152">Totals for each of the time blocks is displayed at the bottom indicating the total estimated effort, cost.</span></span> <span data-ttu-id="0727b-153">和销售。</span><span class="sxs-lookup"><span data-stu-id="0727b-153">and sales for the day, week, month, or year.</span></span>  
  
<span data-ttu-id="0727b-154">成本和售价默认为生效日期—当角色的费率发生变化时，若按周查看“资源”和分时段视图中透视的估算数据时，则在分时段视图中更为明显。</span><span class="sxs-lookup"><span data-stu-id="0727b-154">The cost and sales price defaulting takes is date effective—when the rates for the roles change it will be more transparent in the time-phased view when viewing estimate data pivoted on ‘Resource’ and time-phased by week.</span></span>  
  
## <a name="expense-estimates"></a><span data-ttu-id="0727b-155">费用估算</span><span class="sxs-lookup"><span data-stu-id="0727b-155">Expense estimates</span></span>  
<span data-ttu-id="0727b-156">项目中招致且与人力花费不直接相关的任何费用可记录在项目估算的网格视图中。</span><span class="sxs-lookup"><span data-stu-id="0727b-156">Any expense that will be incurred in the project that is notdirectly related to labor to be expended can be recorded in the project estimates in the grid view.</span></span> <span data-ttu-id="0727b-157">使用网格视图中的**添加费用估算**选项，可完成此操作。</span><span class="sxs-lookup"><span data-stu-id="0727b-157">Using the **Add expense estimate** option in the grid view, you can accomplish this.</span></span> <span data-ttu-id="0727b-158">可对特定的任务或整个项目记录费用估算；您可在这些行上选择费用类别，并选择费用预期发生的一个暂定日期。</span><span class="sxs-lookup"><span data-stu-id="0727b-158">The expense estimates can be recorded for a specific task or for the entire project;you can choose expense categories on these lines and choose a tentative date when the expense is expected to be incurred.</span></span> <span data-ttu-id="0727b-159">如果相关成本和销售价目表具有默认价格，或为费用类别定义了加价百分比，则在关联时将为估算明细上的默认值。</span><span class="sxs-lookup"><span data-stu-id="0727b-159">If the associated cost and sales price list have default prices, or markup percentages defined for expense categories, it will be defaulted on the estimate line on association.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="0727b-160">另请参阅</span><span class="sxs-lookup"><span data-stu-id="0727b-160">See Also</span></span>  
 [<span data-ttu-id="0727b-161">项目经理指南</span><span class="sxs-lookup"><span data-stu-id="0727b-161">Project Manager Guide</span></span>](../project-service/project-manager-guide.md)