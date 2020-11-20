---
title: 项目进度和成本消耗
description: 此主题介绍如何跟踪项目进度和成本消耗。
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 08/21/2020
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
ms.openlocfilehash: 0793ee0c75bcbdde0fd92a16634457f73f872b5e
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/28/2020
ms.locfileid: "4120622"
---
# <a name="project-progress-and-cost-consumption"></a><span data-ttu-id="b7c05-103">项目进度和成本消耗</span><span class="sxs-lookup"><span data-stu-id="b7c05-103">Project progress and cost consumption</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="b7c05-104">对跟踪进度与计划的需要视行业而定。</span><span class="sxs-lookup"><span data-stu-id="b7c05-104">The need to track progress against a schedule varies by industry.</span></span> <span data-ttu-id="b7c05-105">某些行业以粒度级别跟踪，而其他行业则以较高级别跟踪。</span><span class="sxs-lookup"><span data-stu-id="b7c05-105">Some industries track at a granular level, whereas other industries track at a higher level.</span></span> <span data-ttu-id="b7c05-106">此主题介绍如何进行计划以满足组织的要求。</span><span class="sxs-lookup"><span data-stu-id="b7c05-106">This topic shows how to schedule in order to meet your organization's requirements.</span></span>

## <a name="effort-tracking-view"></a><span data-ttu-id="b7c05-107">工作量跟踪视图</span><span class="sxs-lookup"><span data-stu-id="b7c05-107">Effort tracking view</span></span>

<span data-ttu-id="b7c05-108">**工作量跟踪** 视图跟踪计划中的任务的进度。</span><span class="sxs-lookup"><span data-stu-id="b7c05-108">The **Effort tracking** view tracks the progress of tasks in the schedule.</span></span> <span data-ttu-id="b7c05-109">该视图比较任务实际所用工时与任务的计划工时。</span><span class="sxs-lookup"><span data-stu-id="b7c05-109">It compares the actual effort hours spent on a task to the task's planned effort hours.</span></span> <span data-ttu-id="b7c05-110">Project Service Automation 使用以下公式计算跟踪度量：</span><span class="sxs-lookup"><span data-stu-id="b7c05-110">Project Service Automation uses the following formulas to calculate the tracking metrics:</span></span>

<span data-ttu-id="b7c05-111">最初在任务创建时：计划成本将设置为完工估算成本。</span><span class="sxs-lookup"><span data-stu-id="b7c05-111">Initially on the task creation: Planned cost will be set to the Estimated cost at complete.</span></span> <span data-ttu-id="b7c05-112">在任务中记录了“实际值”之后，将在“工作量”的“跟踪”视图上进行以下计算</span><span class="sxs-lookup"><span data-stu-id="b7c05-112">Once Actuals are recorded on the task, the following will be calculation on the Tracking view for Effort</span></span>

- <span data-ttu-id="b7c05-113">进度百分比 = 迄今实际已用工作量 ÷ 完工估算 (EAC)</span><span class="sxs-lookup"><span data-stu-id="b7c05-113">Progress percentage = Actual effort spent to date ÷ Estimate at complete (EAC)</span></span> 
- <span data-ttu-id="b7c05-114">待完成估算 (ETC) = 完工估算 (EAC) – 迄今实际已用工作量</span><span class="sxs-lookup"><span data-stu-id="b7c05-114">Estimate to complete (ETC) = Estimate at complete (EAC)  – Actual effort spent to date</span></span> 
- <span data-ttu-id="b7c05-115">EAC = 剩余工作量 + 迄今实际已用工作量</span><span class="sxs-lookup"><span data-stu-id="b7c05-115">EAC = Remaining effort + Actual effort spent to date</span></span> 
- <span data-ttu-id="b7c05-116">预估工作量偏差 = 计划工作量 – EAC</span><span class="sxs-lookup"><span data-stu-id="b7c05-116">Projected effort variance = Planned effort – EAC</span></span>

<span data-ttu-id="b7c05-117">Project Service Automation 显示任务的工作量偏差预估。</span><span class="sxs-lookup"><span data-stu-id="b7c05-117">Project Service Automation shows a projection of the effort variance on the task.</span></span> <span data-ttu-id="b7c05-118">如果 EAC 比计划工作量大，则预估任务需要的时间比最初计划的多。</span><span class="sxs-lookup"><span data-stu-id="b7c05-118">If the EAC is more than the planned effort, the task is projected to take more time than was originally planned.</span></span> <span data-ttu-id="b7c05-119">因此，进度比计划落后。</span><span class="sxs-lookup"><span data-stu-id="b7c05-119">Therefore, it's behind schedule.</span></span> <span data-ttu-id="b7c05-120">如果 EAC 比计划工作量小，则预估任务需要的时间比最初计划的少。</span><span class="sxs-lookup"><span data-stu-id="b7c05-120">If the EAC is less than the planned effort, the task is projected to take less time than was originally planned.</span></span> <span data-ttu-id="b7c05-121">因此，进度比计划提前。</span><span class="sxs-lookup"><span data-stu-id="b7c05-121">Therefore, it's ahead of schedule.</span></span>

## <a name="reprojecting-effort"></a><span data-ttu-id="b7c05-122">重新预估工作量</span><span class="sxs-lookup"><span data-stu-id="b7c05-122">Reprojecting effort</span></span>

<span data-ttu-id="b7c05-123">项目经理经常修订任务的原始估算。</span><span class="sxs-lookup"><span data-stu-id="b7c05-123">It's common for a project manager to revise the original estimates on a task.</span></span> <span data-ttu-id="b7c05-124">项目重新预估是项目经理基于项目当前状态对估算的感知。</span><span class="sxs-lookup"><span data-stu-id="b7c05-124">Project reprojections are a project manager's perception of estimates, given the current state of a project.</span></span> <span data-ttu-id="b7c05-125">但是，建议项目经理不要更改基准数字，因为项目基准代表项目的所有利益干系人均已同意且已确立的项目计划和成本估算来源。</span><span class="sxs-lookup"><span data-stu-id="b7c05-125">However, we don't recommend that project managers change the baseline numbers, because the project baseline represents the established source of truth for the project's schedule and cost estimate, and all project stakeholders have agreed to it.</span></span>

<span data-ttu-id="b7c05-126">项目经理可通过两种方法重新预估任务的工作量：</span><span class="sxs-lookup"><span data-stu-id="b7c05-126">There are two ways that a project manager can reproject effort on tasks:</span></span>

- <span data-ttu-id="b7c05-127">将默认 ETC 替换为任务的实际剩余工作量新估算。</span><span class="sxs-lookup"><span data-stu-id="b7c05-127">Override the default ETC with a new estimate of the actual remaining effort on the task.</span></span> 
- <span data-ttu-id="b7c05-128">将默认进度百分比替换为项目真实进度新估算。</span><span class="sxs-lookup"><span data-stu-id="b7c05-128">Override the default progress percentage with a new estimate of the true progress on the task.</span></span>

<span data-ttu-id="b7c05-129">这些方法都会导致重新计算任务的 ETC、EAC、进度百分比，以及任务的预估工作量偏差。</span><span class="sxs-lookup"><span data-stu-id="b7c05-129">Each of these approaches cause a recalculation of the task's ETC, EAC, and progress percentage, and the projected effort variance on a task.</span></span> <span data-ttu-id="b7c05-130">还会重新计算汇总任务的 EAC、ETC 和进度百分比，并生成新的工作量偏差预估。</span><span class="sxs-lookup"><span data-stu-id="b7c05-130">The EAC, ETC, and progress percentage on the summary tasks are also recalculated, and produce a new projection of effort variance.</span></span>

## <a name="reprojection-of-effort-on-summary-tasks"></a><span data-ttu-id="b7c05-131">重新预估汇总任务的工作量</span><span class="sxs-lookup"><span data-stu-id="b7c05-131">Reprojection of effort on summary tasks</span></span>

<span data-ttu-id="b7c05-132">可以重新预估汇总任务或容器任务的工作量。</span><span class="sxs-lookup"><span data-stu-id="b7c05-132">Effort on summary tasks or container tasks can be reprojected.</span></span> <span data-ttu-id="b7c05-133">无论用户是使用汇总任务的剩余工作量还是进度百分比来重新预估，都会开始进行下面的这组计算：</span><span class="sxs-lookup"><span data-stu-id="b7c05-133">Regardless of whether the user reprojects by using the remaining effort or the progress percentage on the summary tasks, the following set of calculations begins:</span></span>

- <span data-ttu-id="b7c05-134">计算任务的 EAC、ETC 和进度百分比。</span><span class="sxs-lookup"><span data-stu-id="b7c05-134">The EAC, ETC, and progress percentage on the task are calculated.</span></span>
- <span data-ttu-id="b7c05-135">按任务原始 EAC 的相同比例将新 EAC 分配给子任务。</span><span class="sxs-lookup"><span data-stu-id="b7c05-135">The new EAC is distributed down to the child tasks in the same proportion as the original EAC was on the task.</span></span>
- <span data-ttu-id="b7c05-136">计算向下到叶节点任务的每一个任务的新 EAC。</span><span class="sxs-lookup"><span data-stu-id="b7c05-136">The new EAC on each of the individual tasks down to the leaf node tasks is calculated.</span></span> 
- <span data-ttu-id="b7c05-137">基于 EAC 值重新计算向下到叶节点的受影响子任务的 ETC 和进度百分比。</span><span class="sxs-lookup"><span data-stu-id="b7c05-137">The affected child tasks down to the leaf nodes have their ETC and progress percentage recalculated based on the EAC value.</span></span> <span data-ttu-id="b7c05-138">这会导致重新估算任务工作量偏差。</span><span class="sxs-lookup"><span data-stu-id="b7c05-138">This results in a new projection for the effort variance of the task.</span></span> 
- <span data-ttu-id="b7c05-139">重新计算绘制任务直到根节点的 EAC。</span><span class="sxs-lookup"><span data-stu-id="b7c05-139">The EACs of the summary tasks all the way to the root node are recalculated.</span></span>

### <a name="cost-tracking-view"></a><span data-ttu-id="b7c05-140">成本跟踪视图</span><span class="sxs-lookup"><span data-stu-id="b7c05-140">Cost tracking view</span></span> 

<span data-ttu-id="b7c05-141">**成本跟踪** 视图比较任务的已用实际成本与计划成本。</span><span class="sxs-lookup"><span data-stu-id="b7c05-141">The **Cost tracking** view compares the actual cost that was spent on a task to the planned cost.</span></span> 

> [!NOTE]
> <span data-ttu-id="b7c05-142">此视图仅显示人员成本，不包括支出估算的成本。</span><span class="sxs-lookup"><span data-stu-id="b7c05-142">This view shows only labor costs and doesn’t include costs from the expense estimates.</span></span> 

<span data-ttu-id="b7c05-143">Project Service Automation 使用以下公式计算跟踪度量：</span><span class="sxs-lookup"><span data-stu-id="b7c05-143">Project Service Automation uses the following formulas to calculate the tracking metrics:</span></span>

<span data-ttu-id="b7c05-144">在创建任务时，计划成本等于完工估算成本。</span><span class="sxs-lookup"><span data-stu-id="b7c05-144">When a task is created, the planned cost is equal to the estimated cost at complete.</span></span> <span data-ttu-id="b7c05-145">在任务中记录了“实际值”之后，将在成本的 **跟踪** 视图上计算以下值：</span><span class="sxs-lookup"><span data-stu-id="b7c05-145">After actuals are recorded on the task, the following is calculated on the **Tracking** view for cost:</span></span>

 - <span data-ttu-id="b7c05-146">消耗成本百分比 = 迄今实际已用成本 ÷ 任务的完工估算成本</span><span class="sxs-lookup"><span data-stu-id="b7c05-146">Percentage of cost consumed = Actual cost spent to date ÷ Estimated cost at complete for the task</span></span>
 - <span data-ttu-id="b7c05-147">待完成成本 (CTC) = 完工估算成本 – 迄今实际已用成本</span><span class="sxs-lookup"><span data-stu-id="b7c05-147">Cost to complete (CTC) = Estimated cost at complete – Actual cost spent to date</span></span>
 - <span data-ttu-id="b7c05-148">完工估算成本 = CTC + 迄今实际已用成本</span><span class="sxs-lookup"><span data-stu-id="b7c05-148">Estimated cost at complete = CTC + Actual cost spent to date</span></span>
 - <span data-ttu-id="b7c05-149">预估成本偏差 = 计划成本 – 完工估算成本</span><span class="sxs-lookup"><span data-stu-id="b7c05-149">Projected cost variance = Planned cost – Estimated cost at complete</span></span>

<span data-ttu-id="b7c05-150">显示任务的成本偏差预估。</span><span class="sxs-lookup"><span data-stu-id="b7c05-150">A projection of the cost variance is shown on the task.</span></span> <span data-ttu-id="b7c05-151">如果完工估算成本比计划成本大，则预估成本需要的时间比最初计划的多。</span><span class="sxs-lookup"><span data-stu-id="b7c05-151">If the estimated cost at complete is more than the planned cost, the task is projected to cost more than was originally planned.</span></span> <span data-ttu-id="b7c05-152">因此，趋向超出预算。</span><span class="sxs-lookup"><span data-stu-id="b7c05-152">Therefore, it's trending over budget.</span></span> <span data-ttu-id="b7c05-153">如果完工估算成本比计划成本小，则预估成本需要的时间比最初计划的少，并且趋向低于预算。</span><span class="sxs-lookup"><span data-stu-id="b7c05-153">If the Estimated cost at complete is less than the planned cost, the task is projected to cost less than was originally planned and is trending under budget.</span></span>

## <a name="project-managers-reprojection-of-cost"></a><span data-ttu-id="b7c05-154">项目经理对成本的重新预估</span><span class="sxs-lookup"><span data-stu-id="b7c05-154">Project manager’s reprojection of cost</span></span>

<span data-ttu-id="b7c05-155">重新预估工作量时，**成本跟踪** 视图中将全部重新计算 CTC、完工估算成本、消耗成本百分比和预估成本偏差。</span><span class="sxs-lookup"><span data-stu-id="b7c05-155">When effort is reprojected, the CTC, Estimated cost at complete, percentage of cost consumed, and projected cost variance are all recalculated in the **Cost tracking** view.</span></span>

## <a name="project-status-summary"></a><span data-ttu-id="b7c05-156">项目状态汇总</span><span class="sxs-lookup"><span data-stu-id="b7c05-156">Project status summary</span></span>

<span data-ttu-id="b7c05-157">**工作量跟踪** 和 **成本跟踪** 视图中的跟踪数据显示项目根节点、汇总任务和叶节点任务级的进度和成本消耗。</span><span class="sxs-lookup"><span data-stu-id="b7c05-157">Tracking data in the **Effort tracking** and **Cost tracking** views shows the progress and cost consumption at the project root node, summary tasks, and leaf node tasks levels.</span></span> <span data-ttu-id="b7c05-158">**项目实体** 页中的 **状态** 部分显示项目级状态的汇总。</span><span class="sxs-lookup"><span data-stu-id="b7c05-158">The **Status** section on the **Project entity** page shows a summary of project-level status.</span></span>

## <a name="status-summary-fields"></a><span data-ttu-id="b7c05-159">“状态摘要”字段</span><span class="sxs-lookup"><span data-stu-id="b7c05-159">Status summary fields</span></span>

<span data-ttu-id="b7c05-160">**总体项目状态** 字段是一个可编辑字段，其中显示项目的总体状态。</span><span class="sxs-lookup"><span data-stu-id="b7c05-160">The **Overall project status** field is an editable field that shows the overall status of the project.</span></span> <span data-ttu-id="b7c05-161">其使用颜色编码（如绿色、黄色和红色）来指示上升的风险。</span><span class="sxs-lookup"><span data-stu-id="b7c05-161">It uses color-coding, such as green, yellow, and red, to indicate increasing risk.</span></span> <span data-ttu-id="b7c05-162">项目经理可使用 **注释** 字段输入有关状态的特定注释。</span><span class="sxs-lookup"><span data-stu-id="b7c05-162">The **Comments** field lets the project manager enter specific comments about the status.</span></span> <span data-ttu-id="b7c05-163">**状态更新时间** 字段不可编辑，其值是时间戳，用于指示状态的上次更新时间。</span><span class="sxs-lookup"><span data-stu-id="b7c05-163">The **Status updated on** field is not editable and the value is a timestamp that indicates when the status was last updated.</span></span>

<span data-ttu-id="b7c05-164">**计划绩效** 和 **成本绩效** 字段从跟踪日期设置。</span><span class="sxs-lookup"><span data-stu-id="b7c05-164">The **Schedule performance** and **Cost performance** fields are set from the tracking date.</span></span> <span data-ttu-id="b7c05-165">如果 **工作量跟踪** 视图中根节点的计划与成本的偏差为正，可将这些字段设置为 **提前**。</span><span class="sxs-lookup"><span data-stu-id="b7c05-165">When the schedule and cost variance for the root node in the **Effort tracking** view are positive, you can set these fields to **Ahead**.</span></span> <span data-ttu-id="b7c05-166">如果根节点的计划与成本偏差为负，可将其设置为 **落后**。</span><span class="sxs-lookup"><span data-stu-id="b7c05-166">When the schedule and cost variance for the root node are negative, you can set them to **Behind**.</span></span>
