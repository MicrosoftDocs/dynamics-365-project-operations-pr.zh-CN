---
title: 计价单位组和计价单位
description: 此主题介绍计价单位组和计价单位。
author: rumant
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 03/05/2019
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 58ce821d11d729f6e2c33e5a50344458e395db4d
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/28/2020
ms.locfileid: "4130567"
---
# <a name="unit-groups-and-units"></a><span data-ttu-id="a0be7-103">计价单位组和计价单位</span><span class="sxs-lookup"><span data-stu-id="a0be7-103">Unit groups and units</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="a0be7-104">计价单位组和计价单位是 Microsoft Dynamics 365 中的基本实体。</span><span class="sxs-lookup"><span data-stu-id="a0be7-104">Unit groups and units are basic entities in Microsoft Dynamics 365.</span></span> <span data-ttu-id="a0be7-105">计价单位是一个度量单位，而多个计价单位则可组合成计价单位组。</span><span class="sxs-lookup"><span data-stu-id="a0be7-105">A unit is a single unit of measure, and multiple units can be grouped into unit groups.</span></span> <span data-ttu-id="a0be7-106">在 Dynamics 365 用户界面 (UI) 中，计价单位组有时称为计价单位计划。</span><span class="sxs-lookup"><span data-stu-id="a0be7-106">A unit group is sometimes referred to as a unit schedule in the Dynamics 365 user interface (UI).</span></span> 

<span data-ttu-id="a0be7-107">下面是计价单位和计价单位组的一些示例：</span><span class="sxs-lookup"><span data-stu-id="a0be7-107">Here are some examples of units and unit groups:</span></span>
 
- <span data-ttu-id="a0be7-108">**计价单位组**：距离</span><span class="sxs-lookup"><span data-stu-id="a0be7-108">**Unit group**: Distance</span></span> 
    - <span data-ttu-id="a0be7-109">**计价单位**：英里、千米等。</span><span class="sxs-lookup"><span data-stu-id="a0be7-109">**Units**: Mile, Kilometer, and so on.</span></span>
- <span data-ttu-id="a0be7-110">**计价单位组**：时间</span><span class="sxs-lookup"><span data-stu-id="a0be7-110">**Unit group**: Time</span></span>
    - <span data-ttu-id="a0be7-111">**计价单位**：小时、天、周等。</span><span class="sxs-lookup"><span data-stu-id="a0be7-111">**Units**: Hour, day, week, and so on.</span></span> 

<span data-ttu-id="a0be7-112">在一个计价单位组中设置多个计价单位时，还必须设置这些计价单位之间的换算系数，方法是指定要充当计价单位组的默认计价单位或基础计价单位的第一个计价单位。</span><span class="sxs-lookup"><span data-stu-id="a0be7-112">When you set up multiple units in a unit group, you must also set up a conversion factor between them by designating the first unit that you set up as the default or primary unit for the unit group.</span></span> 

<span data-ttu-id="a0be7-113">例如，如果在 **时间** 计价单位组中将 **小时** 设置为第一个计价单位，则系统将 **小时** 指定为默认计价单位。</span><span class="sxs-lookup"><span data-stu-id="a0be7-113">For example, in a **Time** unit group, if you set up **Hour** as the first unit, the system designates **Hour** as the default unit.</span></span> <span data-ttu-id="a0be7-114">如果您设置的下一个计价单位为 **天**，则必须将 **天** 的换算系数设置为 **小时**。</span><span class="sxs-lookup"><span data-stu-id="a0be7-114">If the next unit that you set up is **Day**, you must set up a conversion factor for **Day** to **Hour**.</span></span> <span data-ttu-id="a0be7-115">如果然后添加 **周** 作为多少个计价单位，则必须为 **周** 设置 **天** 或 **小时** 形式的换算系数。</span><span class="sxs-lookup"><span data-stu-id="a0be7-115">If you then add **Week** as a third unit, you must set up a conversion factor for **Week** in terms of **Day** or **Hour**.</span></span> 

<span data-ttu-id="a0be7-116">下图显示 **天** 计价单位的示例设置，其中，**数量** 字段显示一天中的小时数，以及 **周** 计价单位的示例设置，其中，**数量** 字段显示一周中的天数。</span><span class="sxs-lookup"><span data-stu-id="a0be7-116">The following image shows an example setup for the **Day** unit, where the **Quantity** field shows the number of hours that are in a day, and **Week**, where the **Quantity** field show the number of days that are in a week.</span></span>

> ![计价单位组：“信息”页](media/advanced-2.png)

## <a name="using-units-and-unit-groups"></a><span data-ttu-id="a0be7-118">使用计价单位和计价单位组</span><span class="sxs-lookup"><span data-stu-id="a0be7-118">Using units and unit groups</span></span>

<span data-ttu-id="a0be7-119">Dynamics 365 Project Service Automation 使用计价单位和计价单位组处理支出和时间的估算和条目。</span><span class="sxs-lookup"><span data-stu-id="a0be7-119">Dynamics 365 Project Service Automation uses units and unit groups to process estimates and entries for both expenses and time.</span></span> 

<span data-ttu-id="a0be7-120">例如，每个支出类别都有默认计价单位组和计价单位。</span><span class="sxs-lookup"><span data-stu-id="a0be7-120">For expenses, each expense category has a default unit group and unit.</span></span> <span data-ttu-id="a0be7-121">这些值作为支出类别的价目表条目中的默认值输入。</span><span class="sxs-lookup"><span data-stu-id="a0be7-121">These values are entered as default values on price list entries for expense categories.</span></span> 

<span data-ttu-id="a0be7-122">例如，您有一个支出类别，名称为 **英里数**。</span><span class="sxs-lookup"><span data-stu-id="a0be7-122">For example, you have an expense category that is named **Mileage**.</span></span> <span data-ttu-id="a0be7-123">它有一个计价单位组，名称为 **距离**，有一个默认计价单位，名称为 **英里**。</span><span class="sxs-lookup"><span data-stu-id="a0be7-123">It has a unit group that is named **Distance** and a default unit that is named **Mile**.</span></span> <span data-ttu-id="a0be7-124">如果设置 **距离** 计价单位组，使其有两个计价单位（**英里** 和 **千米**），则可在一个价目表中为 **里程数** 类别设置两个价格：每英里价格和每千米价格。</span><span class="sxs-lookup"><span data-stu-id="a0be7-124">If you set up the **Distance** unit group so that it has two units (**Mile** and **Kilometer**), you can set two prices for the **Mileage** category on one price list: price per mile and price per kilometer.</span></span>

| <span data-ttu-id="a0be7-125">支出类别</span><span class="sxs-lookup"><span data-stu-id="a0be7-125">Expense category</span></span>  | <span data-ttu-id="a0be7-126">计价单位组</span><span class="sxs-lookup"><span data-stu-id="a0be7-126">Unit group</span></span>  | <span data-ttu-id="a0be7-127">单位</span><span class="sxs-lookup"><span data-stu-id="a0be7-127">Unit</span></span>      | <span data-ttu-id="a0be7-128">定价方式</span><span class="sxs-lookup"><span data-stu-id="a0be7-128">Pricing method</span></span>  | <span data-ttu-id="a0be7-129">单价</span><span class="sxs-lookup"><span data-stu-id="a0be7-129">Price per unit</span></span>  |
|-------------------|---------------|-----------|-------------------|-------------------|
| <span data-ttu-id="a0be7-130">英里数</span><span class="sxs-lookup"><span data-stu-id="a0be7-130">Mileage</span></span>           | <span data-ttu-id="a0be7-131">距离</span><span class="sxs-lookup"><span data-stu-id="a0be7-131">Distance</span></span>      | <span data-ttu-id="a0be7-132">英里</span><span class="sxs-lookup"><span data-stu-id="a0be7-132">Mile</span></span>      | <span data-ttu-id="a0be7-133">单价</span><span class="sxs-lookup"><span data-stu-id="a0be7-133">Price per unit</span></span>    | <span data-ttu-id="a0be7-134">10 USD</span><span class="sxs-lookup"><span data-stu-id="a0be7-134">10 USD</span></span>            |
| <span data-ttu-id="a0be7-135">英里数</span><span class="sxs-lookup"><span data-stu-id="a0be7-135">Mileage</span></span>           | <span data-ttu-id="a0be7-136">距离</span><span class="sxs-lookup"><span data-stu-id="a0be7-136">Distance</span></span>      | <span data-ttu-id="a0be7-137">千米</span><span class="sxs-lookup"><span data-stu-id="a0be7-137">Kilometer</span></span> | <span data-ttu-id="a0be7-138">单价</span><span class="sxs-lookup"><span data-stu-id="a0be7-138">Price per unit</span></span>    |  <span data-ttu-id="a0be7-139">6 USD</span><span class="sxs-lookup"><span data-stu-id="a0be7-139">6 USD</span></span>            |

<span data-ttu-id="a0be7-140">在项目中输入支出时，系统通过支出的类别和计价单位组合确定价格。</span><span class="sxs-lookup"><span data-stu-id="a0be7-140">When you enter an expense on a project, the system determines the price through the combination of the category and the unit on the expense.</span></span> 

| <span data-ttu-id="a0be7-141">支出描述</span><span class="sxs-lookup"><span data-stu-id="a0be7-141">Expense description</span></span>        | <span data-ttu-id="a0be7-142">支出类别</span><span class="sxs-lookup"><span data-stu-id="a0be7-142">Expense category</span></span>  | <span data-ttu-id="a0be7-143">单位</span><span class="sxs-lookup"><span data-stu-id="a0be7-143">Unit</span></span>  | <span data-ttu-id="a0be7-144">数量</span><span class="sxs-lookup"><span data-stu-id="a0be7-144">Quantity</span></span>  | <span data-ttu-id="a0be7-145">单价</span><span class="sxs-lookup"><span data-stu-id="a0be7-145">Unit price</span></span>   |
|----------------------------|---------------------|-------|-----------|----------------|
| <span data-ttu-id="a0be7-146">开车到客户位置</span><span class="sxs-lookup"><span data-stu-id="a0be7-146">Drive to client location</span></span> | <span data-ttu-id="a0be7-147">英里数</span><span class="sxs-lookup"><span data-stu-id="a0be7-147">Mileage</span></span>             | <span data-ttu-id="a0be7-148">英里</span><span class="sxs-lookup"><span data-stu-id="a0be7-148">Mile</span></span>  | <span data-ttu-id="a0be7-149">10</span><span class="sxs-lookup"><span data-stu-id="a0be7-149">10</span></span>        | <span data-ttu-id="a0be7-150">10 USD</span><span class="sxs-lookup"><span data-stu-id="a0be7-150">10 USD</span></span>         |

<span data-ttu-id="a0be7-151">对于时间，每个价目表标头有一个 **默认时间单位** 字段。</span><span class="sxs-lookup"><span data-stu-id="a0be7-151">For time, each price list header has a **Default Time Unit** field.</span></span> <span data-ttu-id="a0be7-152">该值是在您创建价目表标头时设置的。</span><span class="sxs-lookup"><span data-stu-id="a0be7-152">The value is set when you create the price list header.</span></span> <span data-ttu-id="a0be7-153">然后使用此计价单位设置价目表中所有基于角色的价格。</span><span class="sxs-lookup"><span data-stu-id="a0be7-153">This unit is then used to set all role-based prices on that price list.</span></span>

<span data-ttu-id="a0be7-154">可以使用任何时间单位表示 **报价单中的时间** 字段的估算明细。</span><span class="sxs-lookup"><span data-stu-id="a0be7-154">Estimate lines for the **Time on Quote** field can be expressed in any unit of time.</span></span> <span data-ttu-id="a0be7-155">但是计划中的估算明细和项目的时间条目只能使用 **小时** 这种时间单位。</span><span class="sxs-lookup"><span data-stu-id="a0be7-155">However, estimate lines on projects and time entries for projects can use only the **Hour** unit of time.</span></span> <span data-ttu-id="a0be7-156">如果时间条目或估算明细中的计价单位与该角色的价目表明细中的计价单位不匹配，系统将把价格转换为在项目估算或项目实际值交易中定义的计价单位。</span><span class="sxs-lookup"><span data-stu-id="a0be7-156">If the unit on the time entry or estimate line doesn't match the unit on the price list line for that role, the system converts the price to the units that are defined in the project estimate or the project actual transaction.</span></span>

<span data-ttu-id="a0be7-157">以下示例显示 PSA 如何使用计价单位组、计价单位和换算系数。</span><span class="sxs-lookup"><span data-stu-id="a0be7-157">The following example shows how PSA uses the unit group, units, and conversion factors.</span></span>
- <span data-ttu-id="a0be7-158">计价单位</span><span class="sxs-lookup"><span data-stu-id="a0be7-158">Units</span></span>

   - <span data-ttu-id="a0be7-159">**计价单位组**：时间</span><span class="sxs-lookup"><span data-stu-id="a0be7-159">**Unit group**: Time</span></span> 
   - <span data-ttu-id="a0be7-160">**计价单位**：小时</span><span class="sxs-lookup"><span data-stu-id="a0be7-160">**Units**: Hour</span></span> 
    
    - <span data-ttu-id="a0be7-161">**天** - 换算系数：8 小时</span><span class="sxs-lookup"><span data-stu-id="a0be7-161">**Day** - Conversion factor: 8 hours</span></span>       
    - <span data-ttu-id="a0be7-162">**周** - 换算系数：40 小时</span><span class="sxs-lookup"><span data-stu-id="a0be7-162">**Week** - Conversion factor: 40 hours</span></span>  
        
- <span data-ttu-id="a0be7-163">项目 A 中的价目表设置：</span><span class="sxs-lookup"><span data-stu-id="a0be7-163">Price list setup on Project A:</span></span>

    - <span data-ttu-id="a0be7-164">**名称**：2016 年英国销售价</span><span class="sxs-lookup"><span data-stu-id="a0be7-164">**Name**: UK sales prices 2016</span></span> 
    - <span data-ttu-id="a0be7-165">**默认时间单位**：天</span><span class="sxs-lookup"><span data-stu-id="a0be7-165">**Default time unit**: Day</span></span> 
    - <span data-ttu-id="a0be7-166">**货币**：GBP</span><span class="sxs-lookup"><span data-stu-id="a0be7-166">**Currency**: GBP</span></span>

| <span data-ttu-id="a0be7-167">角色</span><span class="sxs-lookup"><span data-stu-id="a0be7-167">Role</span></span>      | <span data-ttu-id="a0be7-168">计价单位组</span><span class="sxs-lookup"><span data-stu-id="a0be7-168">Unit group</span></span> | <span data-ttu-id="a0be7-169">单位</span><span class="sxs-lookup"><span data-stu-id="a0be7-169">Unit</span></span> | <span data-ttu-id="a0be7-170">部门</span><span class="sxs-lookup"><span data-stu-id="a0be7-170">Organizational unit</span></span> | <span data-ttu-id="a0be7-171">价格</span><span class="sxs-lookup"><span data-stu-id="a0be7-171">Price</span></span>   |
|-----------|------------|------|---------------------|---------|
| <span data-ttu-id="a0be7-172">开发人员</span><span class="sxs-lookup"><span data-stu-id="a0be7-172">Developer</span></span> | <span data-ttu-id="a0be7-173">Time</span><span class="sxs-lookup"><span data-stu-id="a0be7-173">Time</span></span>       | <span data-ttu-id="a0be7-174">Day</span><span class="sxs-lookup"><span data-stu-id="a0be7-174">Day</span></span>  | <span data-ttu-id="a0be7-175">Contoso 英国</span><span class="sxs-lookup"><span data-stu-id="a0be7-175">Contoso UK</span></span>          | <span data-ttu-id="a0be7-176">800 GBP</span><span class="sxs-lookup"><span data-stu-id="a0be7-176">800 GBP</span></span> |

### <a name="time-entry"></a><span data-ttu-id="a0be7-177">时间条目</span><span class="sxs-lookup"><span data-stu-id="a0be7-177">Time entry</span></span>

<span data-ttu-id="a0be7-178">下表显示 PSA 为一个三小时项目创建的销售端结果交易。</span><span class="sxs-lookup"><span data-stu-id="a0be7-178">The following table shows the resulting sales-side transaction created by PSA for a three hour project.</span></span>


| <span data-ttu-id="a0be7-179">项目</span><span class="sxs-lookup"><span data-stu-id="a0be7-179">Project</span></span>   | <span data-ttu-id="a0be7-180">任务</span><span class="sxs-lookup"><span data-stu-id="a0be7-180">Task</span></span>    | <span data-ttu-id="a0be7-181">角色</span><span class="sxs-lookup"><span data-stu-id="a0be7-181">Role</span></span>      | <span data-ttu-id="a0be7-182">数量</span><span class="sxs-lookup"><span data-stu-id="a0be7-182">Quantity</span></span> | <span data-ttu-id="a0be7-183">单位</span><span class="sxs-lookup"><span data-stu-id="a0be7-183">Unit</span></span>  | <span data-ttu-id="a0be7-184">单价</span><span class="sxs-lookup"><span data-stu-id="a0be7-184">Unit price</span></span> | <span data-ttu-id="a0be7-185">未记帐的销售额</span><span class="sxs-lookup"><span data-stu-id="a0be7-185">Unbilled sales amount</span></span> |
|-----------|---------|-----------|----------|-------|------------|-----------------------|
| <span data-ttu-id="a0be7-186">项目 A</span><span class="sxs-lookup"><span data-stu-id="a0be7-186">Project A</span></span> | <span data-ttu-id="a0be7-187">设计</span><span class="sxs-lookup"><span data-stu-id="a0be7-187">Design</span></span>  | <span data-ttu-id="a0be7-188">开发人员</span><span class="sxs-lookup"><span data-stu-id="a0be7-188">Developer</span></span> | <span data-ttu-id="a0be7-189">3</span><span class="sxs-lookup"><span data-stu-id="a0be7-189">3</span></span>        | <span data-ttu-id="a0be7-190">Hour</span><span class="sxs-lookup"><span data-stu-id="a0be7-190">Hour</span></span>  | <span data-ttu-id="a0be7-191">100 GBP</span><span class="sxs-lookup"><span data-stu-id="a0be7-191">100 GBP</span></span>    | <span data-ttu-id="a0be7-192">300 GBP</span><span class="sxs-lookup"><span data-stu-id="a0be7-192">300 GBP</span></span>               |

## <a name="time-unit-faq"></a><span data-ttu-id="a0be7-193">时间单位常见问题</span><span class="sxs-lookup"><span data-stu-id="a0be7-193">Time unit FAQ</span></span>

### <a name="does-psa-convert-to-different-units-in-the-case-of-expenses"></a><span data-ttu-id="a0be7-194">对于支出，PSA 是否会转换为不同计价单位？</span><span class="sxs-lookup"><span data-stu-id="a0be7-194">Does PSA convert to different units in the case of expenses?</span></span>
<span data-ttu-id="a0be7-195">编号</span><span class="sxs-lookup"><span data-stu-id="a0be7-195">No.</span></span> <span data-ttu-id="a0be7-196">计价单位转换仅适用于时间。</span><span class="sxs-lookup"><span data-stu-id="a0be7-196">Unit conversion works only for time.</span></span> <span data-ttu-id="a0be7-197">例如，如果系统找不到支出类别与计价单位组合的价格，则默认将价格设置为 0.00。</span><span class="sxs-lookup"><span data-stu-id="a0be7-197">For expenses, if the system can't find a price for the combination of the expense category and unit, the price is set to 0.00 by default.</span></span>

### <a name="why-does-psa-convert-time-units"></a><span data-ttu-id="a0be7-198">为什么 PSA 会转换时间单位？</span><span class="sxs-lookup"><span data-stu-id="a0be7-198">Why does PSA convert time units?</span></span>
<span data-ttu-id="a0be7-199">在某些国家或地区，法律要求记帐费率以天为单位。</span><span class="sxs-lookup"><span data-stu-id="a0be7-199">In some countries or regions, there is a legal requirement that bill rates be set up in days.</span></span> <span data-ttu-id="a0be7-200">在报价单周期内，通过对每个可记帐角色使用天费率进行价格协商和折扣。</span><span class="sxs-lookup"><span data-stu-id="a0be7-200">Price negotiation and discounting during the quote cycle is done by using day rates for each billable role.</span></span> <span data-ttu-id="a0be7-201">计划估算和时间条目以天为单位进行。</span><span class="sxs-lookup"><span data-stu-id="a0be7-201">Schedule estimation and time entry are done in hours.</span></span> <span data-ttu-id="a0be7-202">为了支持时间单位方面的这项差异，PSA 转换时间单位。</span><span class="sxs-lookup"><span data-stu-id="a0be7-202">To support this difference in time units, PSA converts time units.</span></span>

### <a name="can-time-units-be-changed-on-project-estimates"></a><span data-ttu-id="a0be7-203">是否可以更改项目估算中的时间单位？</span><span class="sxs-lookup"><span data-stu-id="a0be7-203">Can time units be changed on project estimates?</span></span>
<span data-ttu-id="a0be7-204">不可以。</span><span class="sxs-lookup"><span data-stu-id="a0be7-204">No.</span></span> <span data-ttu-id="a0be7-205">目前计划估算只能采用小时时间单位，不能更改。</span><span class="sxs-lookup"><span data-stu-id="a0be7-205">Schedule estimation is currently restricted to hours and can’t be changed.</span></span>

### <a name="can-units-and-unit-groups-be-edited-deleted-and-added"></a><span data-ttu-id="a0be7-206">是否可编辑、删除和添加计价单位和计价单位组？</span><span class="sxs-lookup"><span data-stu-id="a0be7-206">Can units and unit groups be edited, deleted, and added?</span></span>
<span data-ttu-id="a0be7-207">可以。</span><span class="sxs-lookup"><span data-stu-id="a0be7-207">Yes.</span></span> <span data-ttu-id="a0be7-208">除了 **时间** 计价单位组和 **小时** 计价单位，可以删除或编辑所有计价单位，还可以添加新的计价单位。</span><span class="sxs-lookup"><span data-stu-id="a0be7-208">With exception of the **Time** unit group and the **Hour** unit, all units can be deleted or edited, and new units can be added.</span></span> <span data-ttu-id="a0be7-209">在 PSA 中，不能删除 **时间** 计价单位组和 **小时** 计价单位。</span><span class="sxs-lookup"><span data-stu-id="a0be7-209">In PSA, the **Time** unit group and the **Hour** unit can't be deleted.</span></span> <span data-ttu-id="a0be7-210">但是，可以使用 **名称** 字段的译文更新它们。</span><span class="sxs-lookup"><span data-stu-id="a0be7-210">However, they can be updated with a translated text for the **Name** field.</span></span>
