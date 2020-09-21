---
title: 项目进度和成本消耗
description: 此主题介绍如何跟踪项目进度和成本消耗。
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: 0d742164-5469-421d-8917-63160a81f651
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 8aa5814938129f30885d8161a7c86197ab013364
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/24/2020
ms.locfileid: "3749763"
---
# <a name="project-progress-and-cost-consumption"></a><span data-ttu-id="44ae7-103">项目进度和成本消耗</span><span class="sxs-lookup"><span data-stu-id="44ae7-103">Project progress and cost consumption</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="44ae7-104">对跟踪进度与计划的需要视行业而定。</span><span class="sxs-lookup"><span data-stu-id="44ae7-104">The need to track progress against a schedule varies by industry.</span></span> <span data-ttu-id="44ae7-105">某些行业以粒度级别跟踪，而其他行业则以较高级别跟踪。</span><span class="sxs-lookup"><span data-stu-id="44ae7-105">Some industries track at a granular level, whereas other industries track at a higher level.</span></span> <span data-ttu-id="44ae7-106">此主题介绍如何进行计划以满足组织的要求。</span><span class="sxs-lookup"><span data-stu-id="44ae7-106">This topic shows how to schedule in order to meet your organization's requirements.</span></span>

## <a name="effort-tracking-view"></a><span data-ttu-id="44ae7-107">工作量跟踪视图</span><span class="sxs-lookup"><span data-stu-id="44ae7-107">Effort tracking view</span></span>

<span data-ttu-id="44ae7-108">**工作量跟踪**视图跟踪计划中的任务的进度。</span><span class="sxs-lookup"><span data-stu-id="44ae7-108">The **Effort tracking** view tracks the progress of tasks in the schedule.</span></span> <span data-ttu-id="44ae7-109">其比较任务实际已用工时和该任务的计划工时。</span><span class="sxs-lookup"><span data-stu-id="44ae7-109">It compares the actual effort hours that have been spent on a task to the planned effort hours for that task.</span></span> <span data-ttu-id="44ae7-110">PSA 使用以下公式计算跟踪度量：</span><span class="sxs-lookup"><span data-stu-id="44ae7-110">PSA uses the following formulas to calculate the tracking metrics:</span></span>

- <span data-ttu-id="44ae7-111">进度百分比 = 迄今实际已用工作量 ÷ 任务的计划工作量</span><span class="sxs-lookup"><span data-stu-id="44ae7-111">Progress percentage = Actual effort spent to date ÷ Planned effort for the task</span></span> 
- <span data-ttu-id="44ae7-112">待完成估算 (ETC) = 计划工作量 – 迄今实际已用工作量</span><span class="sxs-lookup"><span data-stu-id="44ae7-112">Estimate to complete (ETC) = Planned effort – Actual effort spent to date</span></span> 
- <span data-ttu-id="44ae7-113">完工估算 (EAC) = 剩余工作量 + 迄今实际已用工作量</span><span class="sxs-lookup"><span data-stu-id="44ae7-113">Estimate at complete (EAC) = Remaining effort + Actual effort spent to date</span></span> 
- <span data-ttu-id="44ae7-114">预估工作量偏差 = 计划工作量 – EAC</span><span class="sxs-lookup"><span data-stu-id="44ae7-114">Projected effort variance = Planned effort – EAC</span></span>

<span data-ttu-id="44ae7-115">PSA 显示任务的工作量偏差预估。</span><span class="sxs-lookup"><span data-stu-id="44ae7-115">PSA shows a projection of the effort variance on the task.</span></span> <span data-ttu-id="44ae7-116">如果 EAC 比计划工作量大，则预估任务需要的时间比最初计划的多。</span><span class="sxs-lookup"><span data-stu-id="44ae7-116">If the EAC is more than the planned effort, the task is projected to take more time than was originally planned.</span></span> <span data-ttu-id="44ae7-117">因此，进度比计划落后。</span><span class="sxs-lookup"><span data-stu-id="44ae7-117">Therefore, it's behind schedule.</span></span> <span data-ttu-id="44ae7-118">如果 EAC 比计划工作量小，则预估任务需要的时间比最初计划的少。</span><span class="sxs-lookup"><span data-stu-id="44ae7-118">If the EAC is less than the planned effort, the task is projected to take less time than was originally planned.</span></span> <span data-ttu-id="44ae7-119">因此，进度比计划提前。</span><span class="sxs-lookup"><span data-stu-id="44ae7-119">Therefore, it's ahead of schedule.</span></span>

## <a name="re-projecting-effort"></a><span data-ttu-id="44ae7-120">重新预估工作量</span><span class="sxs-lookup"><span data-stu-id="44ae7-120">Re-projecting effort</span></span>

<span data-ttu-id="44ae7-121">项目经理经常修订任务的原始估算。</span><span class="sxs-lookup"><span data-stu-id="44ae7-121">It's common for a project manager to revise the original estimates on a task.</span></span> <span data-ttu-id="44ae7-122">项目重新预估是项目经理基于项目当前状态对估算的感知。</span><span class="sxs-lookup"><span data-stu-id="44ae7-122">Project re-projections are a project manager's perception of estimates, given the current state of a project.</span></span> <span data-ttu-id="44ae7-123">但是，建议项目经理不要更改基准数字，因为项目基准代表项目的所有利益干系人均已同意且已确立的项目计划和成本估算来源。</span><span class="sxs-lookup"><span data-stu-id="44ae7-123">However, we don't recommend that project managers change the baseline numbers, because the project baseline represents the established source of truth for the project's schedule and cost estimate, and all project stakeholders have agreed to it.</span></span>

<span data-ttu-id="44ae7-124">项目经理可通过两种方法重新预估任务的工作量：</span><span class="sxs-lookup"><span data-stu-id="44ae7-124">There are two ways that a project manager can re-project effort on tasks:</span></span>

- <span data-ttu-id="44ae7-125">将默认 ETC 替换为任务的实际剩余工作量新估算。</span><span class="sxs-lookup"><span data-stu-id="44ae7-125">Override the default ETC with a new estimate of the actual remaining effort on the task.</span></span> 
- <span data-ttu-id="44ae7-126">将默认进度百分比替换为项目真实进度新估算。</span><span class="sxs-lookup"><span data-stu-id="44ae7-126">Override the default progress percentage with a new estimate of the true progress on the task.</span></span>

<span data-ttu-id="44ae7-127">这些方法都会导致重新计算任务的 ETC、EAC、进度百分比，以及任务的预估工作量偏差。</span><span class="sxs-lookup"><span data-stu-id="44ae7-127">Each of these approaches cause a recalculation of the task's ETC, EAC, and progress percentage, and the projected effort variance on a task.</span></span> <span data-ttu-id="44ae7-128">还会重新计算汇总任务的 EAC、ETC 和进度百分比，并生成新的工作量偏差预估。</span><span class="sxs-lookup"><span data-stu-id="44ae7-128">The EAC, ETC, and progress percentage on the summary tasks are also recalculated, and produce a new projection of effort variance.</span></span>

## <a name="re-projection-of-effort-on-summary-tasks"></a><span data-ttu-id="44ae7-129">重新预估汇总任务的工作量</span><span class="sxs-lookup"><span data-stu-id="44ae7-129">Re-projection of effort on summary tasks</span></span>

<span data-ttu-id="44ae7-130">可以重新预估汇总任务或容器任务的工作量。</span><span class="sxs-lookup"><span data-stu-id="44ae7-130">Effort on summary tasks or container tasks can be re-projected.</span></span> <span data-ttu-id="44ae7-131">无论用户是使用汇总任务的剩余工作量还是进度百分比来重新预估，都会开始进行下面的这组计算：</span><span class="sxs-lookup"><span data-stu-id="44ae7-131">Regardless of whether the user re-projects by using the remaining effort or the progress percentage on the summary tasks, the following set of calculations begins:</span></span>

- <span data-ttu-id="44ae7-132">计算任务的 EAC、ETC 和进度百分比。</span><span class="sxs-lookup"><span data-stu-id="44ae7-132">The EAC, ETC, and progress percentage on the task are calculated.</span></span>
- <span data-ttu-id="44ae7-133">按任务原始 EAC 的相同比例将新 EAC 分配给子任务。</span><span class="sxs-lookup"><span data-stu-id="44ae7-133">The new EAC is distributed down to the child tasks in the same proportion as the original EAC was on the task.</span></span>
- <span data-ttu-id="44ae7-134">计算向下到叶节点任务的每一个任务的新 EAC。</span><span class="sxs-lookup"><span data-stu-id="44ae7-134">The new EAC on each of the individualt tasks down to the leaf node tasks is calculated.</span></span> 
- <span data-ttu-id="44ae7-135">基于 EAC 值重新计算向下到叶节点的受影响子任务的 ETC 和进度百分比。</span><span class="sxs-lookup"><span data-stu-id="44ae7-135">The affected child tasks down to the leaf nodes have their ETC and progress percentage recalculated based on the EAC value.</span></span> <span data-ttu-id="44ae7-136">这会导致重新估算任务工作量偏差。</span><span class="sxs-lookup"><span data-stu-id="44ae7-136">This results in a new projection for the effort variance of the task.</span></span> 
- <span data-ttu-id="44ae7-137">重新计算绘制任务直到根节点的 EAC。</span><span class="sxs-lookup"><span data-stu-id="44ae7-137">The EACs of the summary tasks all the way to the root node are recalculated.</span></span>

### <a name="cost-tracking-view"></a><span data-ttu-id="44ae7-138">成本跟踪视图</span><span class="sxs-lookup"><span data-stu-id="44ae7-138">Cost tracking view</span></span> 

<span data-ttu-id="44ae7-139">**成本跟踪**视图比较任务的已用实际成本与任务的计划成本。</span><span class="sxs-lookup"><span data-stu-id="44ae7-139">The **Cost tracking** view compares the actual cost that was spent on a task to the planned cost on a task.</span></span> 

> [!NOTE]
> <span data-ttu-id="44ae7-140">此视图仅显示人员成本，不包括支出估算的成本。</span><span class="sxs-lookup"><span data-stu-id="44ae7-140">This view shows only labor costs and doesn’t include costs from the expense estimates.</span></span> 

<span data-ttu-id="44ae7-141">PSA 使用以下公式计算跟踪度量：</span><span class="sxs-lookup"><span data-stu-id="44ae7-141">PSA uses the following formulas to calculate the tracking metrics:</span></span>

- <span data-ttu-id="44ae7-142">消耗成本百分比 = 迄今实际已用成本 ÷ 任务的计划成本</span><span class="sxs-lookup"><span data-stu-id="44ae7-142">Percentage of cost consumed = Actual cost spent to date ÷ Planned cost for the task</span></span>
- <span data-ttu-id="44ae7-143">待完成成本 (CTC) = 计划成本 – 迄今实际已用成本</span><span class="sxs-lookup"><span data-stu-id="44ae7-143">Cost to complete (CTC) = Planned cost – Actual cost spent to date</span></span>
- <span data-ttu-id="44ae7-144">EAC = CTC + 迄今实际已用成本</span><span class="sxs-lookup"><span data-stu-id="44ae7-144">EAC = CTC + Actual cost spent to date</span></span>
- <span data-ttu-id="44ae7-145">预估成本偏差 = 计划成本 – EAC</span><span class="sxs-lookup"><span data-stu-id="44ae7-145">Projected cost variance = Planned cost – EAC</span></span>

<span data-ttu-id="44ae7-146">显示任务的成本偏差预估。</span><span class="sxs-lookup"><span data-stu-id="44ae7-146">A projection of the cost variance is shown on the task.</span></span> <span data-ttu-id="44ae7-147">如果 EAC 比计划成本大，则预估成本需要的时间比最初计划的多。</span><span class="sxs-lookup"><span data-stu-id="44ae7-147">If the EAC is more than the planned cost, the task is projected to cost more than was originally planned.</span></span> <span data-ttu-id="44ae7-148">因此，趋向超出预算。</span><span class="sxs-lookup"><span data-stu-id="44ae7-148">Therefore, it's trending over budget.</span></span> <span data-ttu-id="44ae7-149">如果 EAC 比计划成本小，则预估成本需要的时间比最初计划的少。</span><span class="sxs-lookup"><span data-stu-id="44ae7-149">If the EAC is less than the planned cost, the task is projected to cost less than was originally planned.</span></span> <span data-ttu-id="44ae7-150">因此，趋向低于预算。</span><span class="sxs-lookup"><span data-stu-id="44ae7-150">Therefore, it's trending under budget.</span></span>

## <a name="project-managers-re-projection-of-cost"></a><span data-ttu-id="44ae7-151">项目经理对成本的重新预估</span><span class="sxs-lookup"><span data-stu-id="44ae7-151">Project manager’s re-projection of cost</span></span>

<span data-ttu-id="44ae7-152">重新预估工作量时，**成本跟踪**视图中将全部重新计算 CTC、EAC、消耗成本百分比和预估成本偏差。</span><span class="sxs-lookup"><span data-stu-id="44ae7-152">When effort is re-projected, the CTC, EAC, percentage of cost consumed, and projected cost variance are all recalculated in the **Cost tracking** view.</span></span>

## <a name="project-status-summary"></a><span data-ttu-id="44ae7-153">项目状态汇总</span><span class="sxs-lookup"><span data-stu-id="44ae7-153">Project status summary</span></span>

<span data-ttu-id="44ae7-154">**工作量跟踪**和**成本跟踪**视图中的跟踪数据显示项目根节点、汇总任务和叶节点任务级的进度和成本消耗。</span><span class="sxs-lookup"><span data-stu-id="44ae7-154">Tracking data in the **Effort tracking** and **Cost tracking** views shows the progress and cost consumption at the project root node, summary tasks, and leaf node tasks levels.</span></span> <span data-ttu-id="44ae7-155">**项目实体**页中的**状态**部分显示项目级状态的汇总。</span><span class="sxs-lookup"><span data-stu-id="44ae7-155">The **Status** section on the **Project entity** page shows a summary of project-level status.</span></span>

## <a name="status-summary-fields"></a><span data-ttu-id="44ae7-156">“状态摘要”字段</span><span class="sxs-lookup"><span data-stu-id="44ae7-156">Status summary fields</span></span>

<span data-ttu-id="44ae7-157">**总体项目状态**字段是一个可编辑字段，其中显示项目的总体状态。</span><span class="sxs-lookup"><span data-stu-id="44ae7-157">The **Overall project status** field is an editable field that shows the overall status of the project.</span></span> <span data-ttu-id="44ae7-158">其使用颜色编码（如绿色、黄色和红色）来指示上升的风险。</span><span class="sxs-lookup"><span data-stu-id="44ae7-158">It uses color-coding, such as green, yellow, and red, to indicate increasing risk.</span></span> <span data-ttu-id="44ae7-159">项目经理可使用**注释**字段输入有关状态的特定注释。</span><span class="sxs-lookup"><span data-stu-id="44ae7-159">The **Comments** field lets the project manager enter specific comments about the status.</span></span> <span data-ttu-id="44ae7-160">**状态更新时间**字段不可编辑，其值是时间戳，用于指示状态的上次更新时间。</span><span class="sxs-lookup"><span data-stu-id="44ae7-160">The **Status updated on** field is not editable and the value is a timestamp that indicates when the status was last updated.</span></span>

<span data-ttu-id="44ae7-161">**计划绩效**和**成本绩效**字段从跟踪日期设置。</span><span class="sxs-lookup"><span data-stu-id="44ae7-161">The **Schedule performance** and **Cost performance** fields are set from the tracking date.</span></span> <span data-ttu-id="44ae7-162">如果**工作量跟踪**视图中根节点的计划与成本的偏差为正，可将这些字段设置为**提前**。</span><span class="sxs-lookup"><span data-stu-id="44ae7-162">When the schedule and cost variance for the root node in the **Effort tracking** view are positive, you can set these fields to **Ahead**.</span></span> <span data-ttu-id="44ae7-163">如果根节点的计划与成本偏差为负，可将其设置为**落后**。</span><span class="sxs-lookup"><span data-stu-id="44ae7-163">When the schedule and cost variance for the root node are negative, you can set them to **Behind**.</span></span>
