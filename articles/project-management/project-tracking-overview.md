---
title: 项目工作量跟踪
description: 此主题提供关于如何跟踪项目工作和工作进度的信息。
author: ruhercul
ms.date: 03/22/2021
ms.topic: article
ms.reviewer: kfend
ms.author: ruhercul
ms.custom: intro-internal
ms.openlocfilehash: 6fe381470326fc4000a9ed096b91fde56c045c38
ms.sourcegitcommit: 0fafe022731f0e1e8693382ff906e3f8541d34ca
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 07/07/2021
ms.locfileid: "6369185"
---
# <a name="project-effort-tracking"></a><span data-ttu-id="408f0-103">项目工作量跟踪</span><span class="sxs-lookup"><span data-stu-id="408f0-103">Project effort tracking</span></span>

<span data-ttu-id="408f0-104">_**适用于：** 基于资源/非库存场景的 Project Operations，精简部署 - 估价开票交易_</span><span class="sxs-lookup"><span data-stu-id="408f0-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="408f0-105">对跟踪进度与计划的需要视行业而定。</span><span class="sxs-lookup"><span data-stu-id="408f0-105">The need to track progress against a schedule varies by industry.</span></span> <span data-ttu-id="408f0-106">某些行业以粒度级别跟踪，而其他行业则以较高级别跟踪。</span><span class="sxs-lookup"><span data-stu-id="408f0-106">Some industries track at a granular level, where other industries track at a higher level.</span></span> <span data-ttu-id="408f0-107">此主题介绍如何进行计划以满足组织的要求。</span><span class="sxs-lookup"><span data-stu-id="408f0-107">This topic shows how to schedule in order to meet your organization's requirements.</span></span>

## <a name="effort-tracking-view"></a><span data-ttu-id="408f0-108">工作量跟踪视图</span><span class="sxs-lookup"><span data-stu-id="408f0-108">Effort tracking view</span></span>

<span data-ttu-id="408f0-109">**工作量跟踪** 视图通过比较在任务花费的实际工时数与任务的计划工时数来跟踪计划中任务的进度。</span><span class="sxs-lookup"><span data-stu-id="408f0-109">The **Effort tracking** view tracks the progress of tasks in the schedule by comparing the actual effort hours spent on a task to the task's planned effort hours.</span></span> <span data-ttu-id="408f0-110">Dynamics 365 Project Operations 使用以下公式计算跟踪度量：</span><span class="sxs-lookup"><span data-stu-id="408f0-110">Dynamics 365 Project Operations uses the following formulas to calculate the tracking metrics:</span></span>

- <span data-ttu-id="408f0-111">**进度百分比**：迄今实际已用工作量 ÷ 完工估算 (EAC)</span><span class="sxs-lookup"><span data-stu-id="408f0-111">**Progress percentage**: Actual effort spent to date ÷ Estimate at complete (EAC)</span></span> 
- <span data-ttu-id="408f0-112">**剩余工作量**：工作量完工估算 - 迄今实际已用工作量</span><span class="sxs-lookup"><span data-stu-id="408f0-112">**Remaining Effort**: Estimated effort at complete – Actual effort spent to date</span></span> 
- <span data-ttu-id="408f0-113">**EAC**：剩余工作量 + 迄今实际已用工作量</span><span class="sxs-lookup"><span data-stu-id="408f0-113">**EAC**: Remaining effort + Actual effort spent to date</span></span> 
- <span data-ttu-id="408f0-114">**预估工作量偏差**：计划工作量 – EAC</span><span class="sxs-lookup"><span data-stu-id="408f0-114">**Projected effort variance**: Planned effort – EAC</span></span>

<span data-ttu-id="408f0-115">Project Operations 显示任务的工作量偏差预估。</span><span class="sxs-lookup"><span data-stu-id="408f0-115">Project Operations shows a projection of the effort variance on the task.</span></span> <span data-ttu-id="408f0-116">如果 EAC 大于计划工作量，则会预测任务需要比原来计划的更长的时间且会落后于计划。</span><span class="sxs-lookup"><span data-stu-id="408f0-116">If the EAC is more than the planned effort, the task is projected to take more time than was originally planned and is behind schedule.</span></span> <span data-ttu-id="408f0-117">如果 EAC 小于计划工作量，则会预测任务需要比原来计划的更短的时间，是提前计划。</span><span class="sxs-lookup"><span data-stu-id="408f0-117">If the EAC is less than the planned effort, the task is projected to take less time than was originally planned and is ahead schedule.</span></span>

## <a name="reprojecting-effort-on-leaf-node-tasks"></a><span data-ttu-id="408f0-118">重新预测叶节点任务的工作量</span><span class="sxs-lookup"><span data-stu-id="408f0-118">Reprojecting effort on leaf node tasks</span></span>

<span data-ttu-id="408f0-119">项目经理经常修订任务的原始估算。</span><span class="sxs-lookup"><span data-stu-id="408f0-119">Project managers often revise the original estimates on a task.</span></span> <span data-ttu-id="408f0-120">项目重新预估是项目经理基于项目当前状态对估算的感知。</span><span class="sxs-lookup"><span data-stu-id="408f0-120">Project reprojections are a project manager's perception of estimates, given the current state of a project.</span></span> <span data-ttu-id="408f0-121">不过，我们不建议项目经理更改计划工作量数值。</span><span class="sxs-lookup"><span data-stu-id="408f0-121">However, we don't recommend that project managers change the planned effort numbers.</span></span> <span data-ttu-id="408f0-122">这是因为项目计划工作量代表项目进度表和成本估算的既定事实来源，并且所有项目利益干系人均已同意。</span><span class="sxs-lookup"><span data-stu-id="408f0-122">This is because the project planned effort represents the established source of truth for the project schedule and cost estimate, and all project stakeholders have agreed to it.</span></span>

<span data-ttu-id="408f0-123">项目经理可以用新的任务估算来更新默认 **剩余工作量**，以重新预测任务的工作量。</span><span class="sxs-lookup"><span data-stu-id="408f0-123">A project manager can reproject effort on tasks by updating the default **Remaining Effort** with a new estimate on the task.</span></span> <span data-ttu-id="408f0-124">此更新将导致重新计算任务的完工估算 (EAC)、进度百分比和任务的预测工作量差异。</span><span class="sxs-lookup"><span data-stu-id="408f0-124">This update causes a recalculation of the task's estimate at complete (EAC), progress percentage, and the projected effort variance on a task.</span></span> <span data-ttu-id="408f0-125">还会重新计算汇总任务的 EAC、ETC 和进度百分比，并生成新的工作量偏差预估。</span><span class="sxs-lookup"><span data-stu-id="408f0-125">The EAC, ETC, and progress percentage on the summary tasks are also recalculated and produce a new projection of effort variance.</span></span>

## <a name="reprojection-of-effort-on-summary-tasks"></a><span data-ttu-id="408f0-126">重新预估汇总任务的工作量</span><span class="sxs-lookup"><span data-stu-id="408f0-126">Reprojection of effort on summary tasks</span></span>

<span data-ttu-id="408f0-127">可以重新预估汇总任务或容器任务的工作量。</span><span class="sxs-lookup"><span data-stu-id="408f0-127">Effort on summary tasks or container tasks can be reprojected.</span></span> <span data-ttu-id="408f0-128">项目经理可以更新摘要任务的剩余工作量。</span><span class="sxs-lookup"><span data-stu-id="408f0-128">Project managers can update remaining effort on the summary tasks.</span></span> <span data-ttu-id="408f0-129">如果更新剩余工作量，则会在应用程序中触发以下一组计算：</span><span class="sxs-lookup"><span data-stu-id="408f0-129">Updating the remaining effort triggers the following set of calculations in the application:</span></span>

- <span data-ttu-id="408f0-130">计算任务的 EAC 和进度百分比。</span><span class="sxs-lookup"><span data-stu-id="408f0-130">The EAC and progress percentage on the task are calculated.</span></span>
- <span data-ttu-id="408f0-131">按任务原始 EAC 的相同比例将新 EAC 分配给子任务。</span><span class="sxs-lookup"><span data-stu-id="408f0-131">The new EAC is distributed down to the child tasks in the same proportion as the original EAC was on the task.</span></span>
- <span data-ttu-id="408f0-132">计算向下到叶节点任务的每一个任务的新 EAC。</span><span class="sxs-lookup"><span data-stu-id="408f0-132">The new EAC on each of the individual tasks down to the leaf node tasks is calculated.</span></span> 
- <span data-ttu-id="408f0-133">基于 EAC 值重新计算向下到叶节点的受影响子任务的剩余工作量和进度百分比。</span><span class="sxs-lookup"><span data-stu-id="408f0-133">The affected child tasks down to the leaf nodes have their remaining effort and progress percentage recalculated based on the EAC value.</span></span> <span data-ttu-id="408f0-134">这会导致重新估算任务工作量偏差。</span><span class="sxs-lookup"><span data-stu-id="408f0-134">This results in a new projection for the effort variance of the task.</span></span> 
- <span data-ttu-id="408f0-135">重新计算绘制任务直到根节点的 EAC。</span><span class="sxs-lookup"><span data-stu-id="408f0-135">The EACs of the summary tasks all the way to the root node are recalculated.</span></span>


## <a name="project-status-summary"></a><span data-ttu-id="408f0-136">项目状态汇总</span><span class="sxs-lookup"><span data-stu-id="408f0-136">Project status summary</span></span>

<span data-ttu-id="408f0-137">**工作量跟踪** 和 **成本跟踪** 视图中的跟踪数据显示项目根节点、汇总任务和叶节点任务级的进度和成本消耗。</span><span class="sxs-lookup"><span data-stu-id="408f0-137">Tracking data in the **Effort tracking** and **Cost tracking** views shows the progress and cost consumption at the project root node, summary tasks, and leaf node tasks levels.</span></span> <span data-ttu-id="408f0-138">**项目实体** 页中的 **状态** 部分显示项目级状态的汇总。</span><span class="sxs-lookup"><span data-stu-id="408f0-138">The **Status** section on the **Project entity** page shows a summary of project-level status.</span></span>

## <a name="status-summary-fields"></a><span data-ttu-id="408f0-139">“状态摘要”字段</span><span class="sxs-lookup"><span data-stu-id="408f0-139">Status summary fields</span></span>

<span data-ttu-id="408f0-140">**总体项目状态** 字段是一个可编辑字段，其中显示项目的总体状态。</span><span class="sxs-lookup"><span data-stu-id="408f0-140">The **Overall project status** field is an editable field that shows the overall status of the project.</span></span> <span data-ttu-id="408f0-141">其使用颜色编码（如绿色、黄色和红色）来指示上升的风险。</span><span class="sxs-lookup"><span data-stu-id="408f0-141">It uses color-coding, such as green, yellow, and red, to indicate increasing risk.</span></span> <span data-ttu-id="408f0-142">项目经理可使用 **注释** 字段输入有关状态的特定注释。</span><span class="sxs-lookup"><span data-stu-id="408f0-142">The **Comments** field lets the project manager enter specific comments about the status.</span></span> <span data-ttu-id="408f0-143">**状态更新时间** 字段不可编辑，其值是时间戳，用于指示状态的上次更新时间。</span><span class="sxs-lookup"><span data-stu-id="408f0-143">The **Status updated on** field is not editable and the value is a timestamp that indicates when the status was last updated.</span></span>

<span data-ttu-id="408f0-144">**计划绩效** 和 **成本绩效** 字段从跟踪日期设置。</span><span class="sxs-lookup"><span data-stu-id="408f0-144">The **Schedule performance** and **Cost performance** fields are set from the tracking date.</span></span> <span data-ttu-id="408f0-145">如果 **工作量跟踪** 视图中根节点的计划与成本的偏差为正，可将这些字段设置为 **提前**。</span><span class="sxs-lookup"><span data-stu-id="408f0-145">When the schedule and cost variance for the root node in the **Effort tracking** view are positive, you can set these fields to **Ahead**.</span></span> <span data-ttu-id="408f0-146">如果根节点的计划与成本偏差为负，可将其设置为 **落后**。</span><span class="sxs-lookup"><span data-stu-id="408f0-146">When the schedule and cost variance for the root node are negative, you can set them to **Behind**.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
