---
title: 项目跟踪概述
description: 此主题介绍如何跟踪项目进度和成本消耗。
author: ruhercul
manager: AnnBe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: c998addbbdbbea8fe69c95f65e58a24146f394c8
ms.sourcegitcommit: 56c42d7f5995a674426a1c2a81bae897dceb391c
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/01/2020
ms.locfileid: "3907352"
---
# <a name="project-tracking-overview"></a><span data-ttu-id="28614-103">项目跟踪概述</span><span class="sxs-lookup"><span data-stu-id="28614-103">Project tracking overview</span></span>

<span data-ttu-id="28614-104">_**适用于：** 基于资源/非库存场景的 Project Operations，精简部署 - 估价开票交易_</span><span class="sxs-lookup"><span data-stu-id="28614-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="28614-105">对跟踪进度与计划的需要视行业而定。</span><span class="sxs-lookup"><span data-stu-id="28614-105">The need to track progress against a schedule varies by industry.</span></span> <span data-ttu-id="28614-106">某些行业以粒度级别跟踪，而其他行业则以较高级别跟踪。</span><span class="sxs-lookup"><span data-stu-id="28614-106">Some industries track at a granular level, where other industries track at a higher level.</span></span> <span data-ttu-id="28614-107">此主题介绍如何进行计划以满足组织的要求。</span><span class="sxs-lookup"><span data-stu-id="28614-107">This topic shows how to schedule in order to meet your organization's requirements.</span></span>

## <a name="effort-tracking-view"></a><span data-ttu-id="28614-108">工作量跟踪视图</span><span class="sxs-lookup"><span data-stu-id="28614-108">Effort tracking view</span></span>

<span data-ttu-id="28614-109">**工作量跟踪**视图通过比较在任务花费的实际工时数与任务的计划工时数来跟踪计划中任务的进度。</span><span class="sxs-lookup"><span data-stu-id="28614-109">The **Effort tracking** view tracks the progress of tasks in the schedule by comparing the actual effort hours spent on a task to the task's planned effort hours.</span></span> <span data-ttu-id="28614-110">Dynamics 365 Project Operations 使用以下公式计算跟踪指标：</span><span class="sxs-lookup"><span data-stu-id="28614-110">Dynamics 365 Project Operations uses the following formulas to calculate the tracking metrics:</span></span>

- <span data-ttu-id="28614-111">**进度百分比**：迄今实际已用工作量 ÷ 完工估算 (EAC)</span><span class="sxs-lookup"><span data-stu-id="28614-111">**Progress percentage**: Actual effort spent to date ÷ Estimate at complete (EAC)</span></span> 
- <span data-ttu-id="28614-112">**待完成估算 (ETC)**：计划工作量 – 迄今实际已用工作量</span><span class="sxs-lookup"><span data-stu-id="28614-112">**Estimate to complete (ETC)**: Planned effort – Actual effort spent to date</span></span> 
- <span data-ttu-id="28614-113">**EAC**：剩余工作量 + 迄今实际已用工作量</span><span class="sxs-lookup"><span data-stu-id="28614-113">**EAC**: Remaining effort + Actual effort spent to date</span></span> 
- <span data-ttu-id="28614-114">**预估工作量偏差**：计划工作量 – EAC</span><span class="sxs-lookup"><span data-stu-id="28614-114">**Projected effort variance**: Planned effort – EAC</span></span>

<span data-ttu-id="28614-115">Project Operations 显示任务的工作量偏差预估。</span><span class="sxs-lookup"><span data-stu-id="28614-115">Project Operations shows a projection of the effort variance on the task.</span></span> <span data-ttu-id="28614-116">如果 EAC 大于计划工作量，则会预测任务需要比原来计划的更长的时间且会落后于计划。</span><span class="sxs-lookup"><span data-stu-id="28614-116">If the EAC is more than the planned effort, the task is projected to take more time than was originally planned and is behind schedule.</span></span> <span data-ttu-id="28614-117">如果 EAC 小于计划工作量，则会预测任务需要比原来计划的更短的时间，是提前计划。</span><span class="sxs-lookup"><span data-stu-id="28614-117">If the EAC is less than the planned effort, the task is projected to take less time than was originally planned and is ahead schedule.</span></span>

## <a name="reprojecting-effort"></a><span data-ttu-id="28614-118">重新预估工作量</span><span class="sxs-lookup"><span data-stu-id="28614-118">Reprojecting effort</span></span>

<span data-ttu-id="28614-119">项目经理经常修订任务的原始估算。</span><span class="sxs-lookup"><span data-stu-id="28614-119">Project managers often revise the original estimates on a task.</span></span> <span data-ttu-id="28614-120">项目重新预估是项目经理基于项目当前状态对估算的感知。</span><span class="sxs-lookup"><span data-stu-id="28614-120">Project reprojections are a project manager's perception of estimates, given the current state of a project.</span></span> <span data-ttu-id="28614-121">但是，我们不建议项目经理更改基准数字。</span><span class="sxs-lookup"><span data-stu-id="28614-121">However, we don't recommend that project managers change the baseline numbers.</span></span> <span data-ttu-id="28614-122">这是因为项目基准代表项目的所有利益干系人均已同意且已确立的项目计划和成本估算来源。</span><span class="sxs-lookup"><span data-stu-id="28614-122">This is because the project baseline represents the established source of truth for the project schedule and cost estimate, and all project stakeholders have agreed to it.</span></span>

<span data-ttu-id="28614-123">项目经理可通过两种方法重新预估任务的工作量：</span><span class="sxs-lookup"><span data-stu-id="28614-123">There are two ways that a project manager can reproject effort on tasks:</span></span>

- <span data-ttu-id="28614-124">将默认 ETC 替换为任务的实际剩余工作量新估算。</span><span class="sxs-lookup"><span data-stu-id="28614-124">Override the default ETC with a new estimate of the actual remaining effort on the task.</span></span> 
- <span data-ttu-id="28614-125">将默认进度百分比替换为项目真实进度新估算。</span><span class="sxs-lookup"><span data-stu-id="28614-125">Override the default progress percentage with a new estimate of the true progress on the task.</span></span>

<span data-ttu-id="28614-126">每种方法都会导致重新计算任务的 ETC、EAC、进度百分比，以及任务的预估工作量偏差。</span><span class="sxs-lookup"><span data-stu-id="28614-126">Each approach causes a recalculation of the task's ETC, EAC, progress percentage, and the projected effort variance on a task.</span></span> <span data-ttu-id="28614-127">还会重新计算汇总任务的 EAC、ETC 和进度百分比，并生成新的工作量偏差预估。</span><span class="sxs-lookup"><span data-stu-id="28614-127">The EAC, ETC, and progress percentage on the summary tasks are also recalculated and produce a new projection of effort variance.</span></span>

## <a name="reprojection-of-effort-on-summary-tasks"></a><span data-ttu-id="28614-128">重新预估汇总任务的工作量</span><span class="sxs-lookup"><span data-stu-id="28614-128">Reprojection of effort on summary tasks</span></span>

<span data-ttu-id="28614-129">可以重新预估汇总任务或容器任务的工作量。</span><span class="sxs-lookup"><span data-stu-id="28614-129">Effort on summary tasks or container tasks can be reprojected.</span></span> <span data-ttu-id="28614-130">无论用户是使用汇总任务的剩余工作量还是进度百分比来重新预估，都会开始进行下面的这组计算：</span><span class="sxs-lookup"><span data-stu-id="28614-130">Regardless of whether the user reprojects by using the remaining effort or the progress percentage on the summary tasks, the following set of calculations begins:</span></span>

- <span data-ttu-id="28614-131">计算任务的 EAC、ETC 和进度百分比。</span><span class="sxs-lookup"><span data-stu-id="28614-131">The EAC, ETC, and progress percentage on the task are calculated.</span></span>
- <span data-ttu-id="28614-132">按任务原始 EAC 的相同比例将新 EAC 分配给子任务。</span><span class="sxs-lookup"><span data-stu-id="28614-132">The new EAC is distributed down to the child tasks in the same proportion as the original EAC was on the task.</span></span>
- <span data-ttu-id="28614-133">计算向下到叶节点任务的每一个任务的新 EAC。</span><span class="sxs-lookup"><span data-stu-id="28614-133">The new EAC on each of the individual tasks down to the leaf node tasks is calculated.</span></span> 
- <span data-ttu-id="28614-134">基于 EAC 值重新计算向下到叶节点的受影响子任务的 ETC 和进度百分比。</span><span class="sxs-lookup"><span data-stu-id="28614-134">The affected child tasks down to the leaf nodes have their ETC and progress percentage recalculated based on the EAC value.</span></span> <span data-ttu-id="28614-135">这会导致重新估算任务工作量偏差。</span><span class="sxs-lookup"><span data-stu-id="28614-135">This results in a new projection for the effort variance of the task.</span></span> 
- <span data-ttu-id="28614-136">重新计算绘制任务直到根节点的 EAC。</span><span class="sxs-lookup"><span data-stu-id="28614-136">The EACs of the summary tasks all the way to the root node are recalculated.</span></span>

### <a name="cost-tracking-view"></a><span data-ttu-id="28614-137">成本跟踪视图</span><span class="sxs-lookup"><span data-stu-id="28614-137">Cost tracking view</span></span> 

<span data-ttu-id="28614-138">**成本跟踪**视图比较任务的已用实际成本与任务的计划成本。</span><span class="sxs-lookup"><span data-stu-id="28614-138">The **Cost tracking** view compares the actual cost that was spent on a task to the planned cost on a task.</span></span> 

> [!NOTE]
> <span data-ttu-id="28614-139">此视图仅显示人员成本，不包括支出估算的成本。</span><span class="sxs-lookup"><span data-stu-id="28614-139">This view shows only labor costs and doesn’t include costs from the expense estimates.</span></span> <span data-ttu-id="28614-140">Project Operations 使用以下公式计算跟踪指标：</span><span class="sxs-lookup"><span data-stu-id="28614-140">Project Operations uses the following formulas to calculate the tracking metrics:</span></span>

- <span data-ttu-id="28614-141">**消耗成本百分比**：迄今实际已用成本 ÷ 完工估算成本</span><span class="sxs-lookup"><span data-stu-id="28614-141">**Percentage of cost consumed**: Actual cost spent to date ÷ Estimated cost at completion</span></span>
- <span data-ttu-id="28614-142">**待完成成本 (CTC)**：计划成本 – 迄今实际已用成本</span><span class="sxs-lookup"><span data-stu-id="28614-142">**Cost to complete (CTC)**: Planned cost – Actual cost spent to date</span></span>
- <span data-ttu-id="28614-143">**EAC**：剩余成本 + 迄今实际已用成本</span><span class="sxs-lookup"><span data-stu-id="28614-143">**EAC**: Remaining cost + Actual cost spent to date</span></span>
- <span data-ttu-id="28614-144">**预估成本偏差**：计划成本 – EAC</span><span class="sxs-lookup"><span data-stu-id="28614-144">**Projected cost variance**: Planned cost – EAC</span></span>

<span data-ttu-id="28614-145">显示任务的成本偏差预估。</span><span class="sxs-lookup"><span data-stu-id="28614-145">A projection of the cost variance is shown on the task.</span></span> <span data-ttu-id="28614-146">如果 EAC 比计划成本大，则预估成本需要的时间比最初计划的多。</span><span class="sxs-lookup"><span data-stu-id="28614-146">If the EAC is more than the planned cost, the task is projected to cost more than was originally planned.</span></span> <span data-ttu-id="28614-147">因此，趋向超出预算。</span><span class="sxs-lookup"><span data-stu-id="28614-147">Therefore, it's trending over budget.</span></span> <span data-ttu-id="28614-148">如果 EAC 比计划成本小，则预估成本需要的时间比最初计划的少。</span><span class="sxs-lookup"><span data-stu-id="28614-148">If the EAC is less than the planned cost, the task is projected to cost less than was originally planned.</span></span> <span data-ttu-id="28614-149">因此，趋向低于预算。</span><span class="sxs-lookup"><span data-stu-id="28614-149">Therefore, it's trending under budget.</span></span>

## <a name="project-managers-reprojection-of-cost"></a><span data-ttu-id="28614-150">项目经理对成本的重新预估</span><span class="sxs-lookup"><span data-stu-id="28614-150">Project manager’s reprojection of cost</span></span>

<span data-ttu-id="28614-151">重新预估工作量时，**成本跟踪**视图中将全部重新计算 CTC、EAC、消耗成本百分比和预估成本偏差。</span><span class="sxs-lookup"><span data-stu-id="28614-151">When effort is reprojected, the CTC, EAC, percentage of cost consumed, and projected cost variance are all recalculated in the **Cost tracking** view.</span></span>

## <a name="project-status-summary"></a><span data-ttu-id="28614-152">项目状态汇总</span><span class="sxs-lookup"><span data-stu-id="28614-152">Project status summary</span></span>

<span data-ttu-id="28614-153">**工作量跟踪**和**成本跟踪**视图中的跟踪数据显示项目根节点、汇总任务和叶节点任务级的进度和成本消耗。</span><span class="sxs-lookup"><span data-stu-id="28614-153">Tracking data in the **Effort tracking** and **Cost tracking** views shows the progress and cost consumption at the project root node, summary tasks, and leaf node tasks levels.</span></span> <span data-ttu-id="28614-154">**项目实体**页中的**状态**部分显示项目级状态的汇总。</span><span class="sxs-lookup"><span data-stu-id="28614-154">The **Status** section on the **Project entity** page shows a summary of project-level status.</span></span>

## <a name="status-summary-fields"></a><span data-ttu-id="28614-155">“状态摘要”字段</span><span class="sxs-lookup"><span data-stu-id="28614-155">Status summary fields</span></span>

<span data-ttu-id="28614-156">**总体项目状态**字段是一个可编辑字段，其中显示项目的总体状态。</span><span class="sxs-lookup"><span data-stu-id="28614-156">The **Overall project status** field is an editable field that shows the overall status of the project.</span></span> <span data-ttu-id="28614-157">其使用颜色编码（如绿色、黄色和红色）来指示上升的风险。</span><span class="sxs-lookup"><span data-stu-id="28614-157">It uses color-coding, such as green, yellow, and red, to indicate increasing risk.</span></span> <span data-ttu-id="28614-158">项目经理可使用**注释**字段输入有关状态的特定注释。</span><span class="sxs-lookup"><span data-stu-id="28614-158">The **Comments** field lets the project manager enter specific comments about the status.</span></span> <span data-ttu-id="28614-159">**状态更新时间**字段不可编辑，其值是时间戳，用于指示状态的上次更新时间。</span><span class="sxs-lookup"><span data-stu-id="28614-159">The **Status updated on** field is not editable and the value is a timestamp that indicates when the status was last updated.</span></span>

<span data-ttu-id="28614-160">**计划绩效**和**成本绩效**字段从跟踪日期设置。</span><span class="sxs-lookup"><span data-stu-id="28614-160">The **Schedule performance** and **Cost performance** fields are set from the tracking date.</span></span> <span data-ttu-id="28614-161">如果**工作量跟踪**视图中根节点的计划与成本的偏差为正，可将这些字段设置为**提前**。</span><span class="sxs-lookup"><span data-stu-id="28614-161">When the schedule and cost variance for the root node in the **Effort tracking** view are positive, you can set these fields to **Ahead**.</span></span> <span data-ttu-id="28614-162">如果根节点的计划与成本偏差为负，可将其设置为**落后**。</span><span class="sxs-lookup"><span data-stu-id="28614-162">When the schedule and cost variance for the root node are negative, you can set them to **Behind**.</span></span>
