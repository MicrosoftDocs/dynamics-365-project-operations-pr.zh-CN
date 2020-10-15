---
title: 浏览用户界面
description: 本主题提供有关 Dynamics 365 Project Operations 中的项目管理的信息。
author: ruhercul
manager: AnnBe
ms.date: 10/05/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: ff624a13ec88ae64dba18715fbe9b94353b070e8
ms.sourcegitcommit: 396e0fea2f1598a5313cb0128eca4fe0bb5aade9
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/05/2020
ms.locfileid: "3961827"
---
# <a name="navigating-the-user-interface"></a><span data-ttu-id="e77a0-103">浏览用户界面</span><span class="sxs-lookup"><span data-stu-id="e77a0-103">Navigating the user interface</span></span>

<span data-ttu-id="e77a0-104">_**适用于：** 基于资源/非库存场景的 Project Operations，精简部署 - 估价开票交易_</span><span class="sxs-lookup"><span data-stu-id="e77a0-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

## <a name="overview"></a><span data-ttu-id="e77a0-105">概述</span><span class="sxs-lookup"><span data-stu-id="e77a0-105">Overview</span></span>

<span data-ttu-id="e77a0-106">主项目窗体分为多个选项卡。</span><span class="sxs-lookup"><span data-stu-id="e77a0-106">The main project form is separated into several tabs.</span></span> <span data-ttu-id="e77a0-107">每个选项卡代表项目中详细信息的不同级别。</span><span class="sxs-lookup"><span data-stu-id="e77a0-107">Each tab represents a different level of detail within the project.</span></span>

- <span data-ttu-id="e77a0-108">**摘要**：提供项目的说明，聚合计划项目绩效和实际项目绩效。</span><span class="sxs-lookup"><span data-stu-id="e77a0-108">**Summary**: Provides a description of the project and aggregates both the planned and actual project performance.</span></span>

    ![“摘要”选项卡和字段](media/navigation7.png)

- <span data-ttu-id="e77a0-110">**任务**：提供有关网格视图、板视图和甘特图表示的工作分解结构的详细信息。</span><span class="sxs-lookup"><span data-stu-id="e77a0-110">**Tasks**: Provides the details regarding the work breakdown structure represented by a grid view, board view, and a gantt.</span></span>

    ![“任务”选项卡和字段](media/navigation8.png)

- <span data-ttu-id="e77a0-112">**团队**：提供有关项目参与者的详细信息。</span><span class="sxs-lookup"><span data-stu-id="e77a0-112">**Team**: Provides details regarding the project participants.</span></span> <span data-ttu-id="e77a0-113">此视图还汇总每个团队成员的分配工作量。</span><span class="sxs-lookup"><span data-stu-id="e77a0-113">The assigned effort of each team member is also summarized in this view.</span></span>

    ![“团队”选项卡和字段](media/navigation9.png)

- <span data-ttu-id="e77a0-115">**资源分配**：为项目中的每个资源提供分时段的工作量视图。</span><span class="sxs-lookup"><span data-stu-id="e77a0-115">**Resource assignments**: Provides a time-phased view of the effort for each resource on a project.</span></span>

    ![“资源分配”选项卡和字段](media/navigation10.png)

- <span data-ttu-id="e77a0-117">**资源协调**：提供每个指定资源的分配与其预订之间的差异的分时段视图。</span><span class="sxs-lookup"><span data-stu-id="e77a0-117">**Resource reconciliation**: Provides a time-phased view of the differences between the assignments of each named resource and their bookings.</span></span>

    ![“资源协调”选项卡和字段](media/navigation11.png)

- <span data-ttu-id="e77a0-119">**预估**：提供项目的成本和销售预估的分时段视图。</span><span class="sxs-lookup"><span data-stu-id="e77a0-119">**Estimates**: Provides a time-phased view of the cost and sales estimates of a project.</span></span>

    ![“预估”选项卡和字段](media/navigation12.png)

- <span data-ttu-id="e77a0-121">**跟踪**：提供显示工作分解结构中工作量、成本和销售的任务进度的视图。</span><span class="sxs-lookup"><span data-stu-id="e77a0-121">**Tracking**: Provides a view that shows the progress of tasks in the work breakdown structure for effort, cost, and sales.</span></span>

    ![“跟踪”选项卡和字段](media/navigation13.png)

- <span data-ttu-id="e77a0-123">**销售**：提供与项目关联的报价单和合同的深层链接。</span><span class="sxs-lookup"><span data-stu-id="e77a0-123">**Sales**: Provides deep links to quotes and contracts associated with the project.</span></span>

- <span data-ttu-id="e77a0-124">**支出预估**：提供根据组织的支出类别定义项目支出的网格。</span><span class="sxs-lookup"><span data-stu-id="e77a0-124">**Expense Estimates**: Provides a grid that defines project expenses based upon organizational expense categories.</span></span>

    ![“支出预估”选项卡和字段](media/navigation14.png)

## <a name="grid-controls"></a><span data-ttu-id="e77a0-126">网格控件</span><span class="sxs-lookup"><span data-stu-id="e77a0-126">Grid controls</span></span>

<span data-ttu-id="e77a0-127">以下是在各个项目规划选项卡上找到的典型控件的简要概览。</span><span class="sxs-lookup"><span data-stu-id="e77a0-127">The follow is a brief overview of the typical controls found on the various project planning tabs.</span></span>

### <a name="refresh"></a><span data-ttu-id="e77a0-128">刷新​​</span><span class="sxs-lookup"><span data-stu-id="e77a0-128">Refresh</span></span>

<span data-ttu-id="e77a0-129">**刷新**：在加载网格后发生更改时从服务器检索最新数据。</span><span class="sxs-lookup"><span data-stu-id="e77a0-129">**Refresh**: Retrieves the latest data from the server if any changes occurred after the grid was loaded.</span></span>

![“刷新”按钮](media/navigation7.png)

### <a name="group-by"></a><span data-ttu-id="e77a0-131">分组依据</span><span class="sxs-lookup"><span data-stu-id="e77a0-131">Group by</span></span>

<span data-ttu-id="e77a0-132">**分组依据**：根据用户的需求更新网格中行的分组以反映资源、角色或类别。</span><span class="sxs-lookup"><span data-stu-id="e77a0-132">**Group by**: Updates the grouping of the rows in the grid to reflect either resources, roles, or categories based on the user's needs.</span></span>

![“分组依据”按钮](media/navigation6.png)

### <a name="previousnext"></a><span data-ttu-id="e77a0-134">上一个/下一个</span><span class="sxs-lookup"><span data-stu-id="e77a0-134">Previous/Next</span></span>

<span data-ttu-id="e77a0-135">**上一个**/**下一个**：更新分时段网格上的可见时间段。</span><span class="sxs-lookup"><span data-stu-id="e77a0-135">**Previous**/**Next**: Update the visible time periods on the time-phased grids.</span></span>

![“上一个”和“下一个”按钮](media/navigation2.png)

### <a name="timescale"></a><span data-ttu-id="e77a0-137">时间刻度</span><span class="sxs-lookup"><span data-stu-id="e77a0-137">Timescale</span></span>

<span data-ttu-id="e77a0-138">**时间刻度**：在天、周、月和年之间更改分时段数据的聚合。</span><span class="sxs-lookup"><span data-stu-id="e77a0-138">**Timescale**: Change the aggregation of the time-phased data between days, weeks, months, and years.</span></span>

![“时间刻度”按钮](media/navigation3.png)

### <a name="expand"></a><span data-ttu-id="e77a0-140">扩展</span><span class="sxs-lookup"><span data-stu-id="e77a0-140">Expand</span></span>

<span data-ttu-id="e77a0-141">**展开**：全屏呈现可见网格，以提供更多功能来查看其他角色。</span><span class="sxs-lookup"><span data-stu-id="e77a0-141">**Expand**: Render the visible grid to full screen providing more ability to see additional roles.</span></span>

![“展开”按钮](media/navigation4.png)

### <a name="time-phase-by"></a><span data-ttu-id="e77a0-143">时间分段依据</span><span class="sxs-lookup"><span data-stu-id="e77a0-143">Time-phase by</span></span>

<span data-ttu-id="e77a0-144">**时间分段依据**：更新网格中行的分组以反映销售预估的成本预估。</span><span class="sxs-lookup"><span data-stu-id="e77a0-144">**Time-phase by**: Update the grouping of the rows in the grid to reflect cost estimates for sales estimates.</span></span> <span data-ttu-id="e77a0-145">此控件也适用于预估脚本和跟踪网格。</span><span class="sxs-lookup"><span data-stu-id="e77a0-145">This control also applies to the estimate script and the tracking grid.</span></span>

![“时间分段依据”按钮](media/navigation0.png)

### <a name="add-column"></a><span data-ttu-id="e77a0-147">添加列</span><span class="sxs-lookup"><span data-stu-id="e77a0-147">Add column</span></span>

<span data-ttu-id="e77a0-148">**添加列**：允许用户在网格中定义可见列。</span><span class="sxs-lookup"><span data-stu-id="e77a0-148">**Add column**: Allows the user to define the visible columns in the grid.</span></span> <span data-ttu-id="e77a0-149">只能将现成的列添加到**项目规划**窗体的网格中。</span><span class="sxs-lookup"><span data-stu-id="e77a0-149">Only out-of-the-box columns can be added to the grids in the **Project Planning** form.</span></span>

![“添加列”按钮](media/navigation5.png)
