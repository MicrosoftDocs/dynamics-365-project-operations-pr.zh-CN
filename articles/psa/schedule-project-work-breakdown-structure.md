---
title: 使用工作分解结构计划项目
description: 如何在 Project Service 中使用工作分解结构计划项目
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
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
ms.openlocfilehash: a00e39f78890426721a49cd569ba8ce4accb30a9
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/15/2021
ms.locfileid: "5282682"
---
# <a name="schedule-a-project-with-a-work-breakdown-structure-project-service"></a><span data-ttu-id="e47bb-103">使用工作分解结构计划项目 (Project Service)</span><span class="sxs-lookup"><span data-stu-id="e47bb-103">Schedule a project with a work breakdown structure (Project Service)</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="e47bb-104">项目计划传达需要执行哪些工作、哪些资源执行工作及工作要求完成的时限。</span><span class="sxs-lookup"><span data-stu-id="e47bb-104">A project schedule communicates what work needs to be performed, which resources will perform the work, and the timeframe in which that work needs to be completed.</span></span> <span data-ttu-id="e47bb-105">项目计划反映与按期交付项目相关的所有工作。</span><span class="sxs-lookup"><span data-stu-id="e47bb-105">The project schedule reflects all the work associated with delivering the project on time.</span></span> <span data-ttu-id="e47bb-106">项目启动阶段准备工作的第一步就是制定项目计划。</span><span class="sxs-lookup"><span data-stu-id="e47bb-106">One of the first steps in the initiation phase of the project is to come up with a project schedule.</span></span> <span data-ttu-id="e47bb-107">若要建立项目计划，您需要创建工作分解结构。</span><span class="sxs-lookup"><span data-stu-id="e47bb-107">To establish a project schedule, you need to create a work breakdown structure.</span></span>  
  
 <span data-ttu-id="e47bb-108">使用工作分解结构创建项目结构，该结构有助于您：</span><span class="sxs-lookup"><span data-stu-id="e47bb-108">Create a project structure with a work breakdown structure, which helps you:</span></span>  
  
- <span data-ttu-id="e47bb-109">将工作分解为可管理的任务</span><span class="sxs-lookup"><span data-stu-id="e47bb-109">Break down work into manageable tasks</span></span>  
  
- <span data-ttu-id="e47bb-110">估计完成任务所需的时间</span><span class="sxs-lookup"><span data-stu-id="e47bb-110">Estimate the time required to complete a task</span></span>  
  
- <span data-ttu-id="e47bb-111">设置任务相关性和任务持续时间</span><span class="sxs-lookup"><span data-stu-id="e47bb-111">Set task dependencies and task duration</span></span>  
  
- <span data-ttu-id="e47bb-112">确定完成每项任务所需的角色</span><span class="sxs-lookup"><span data-stu-id="e47bb-112">Determine the roles required to complete each task</span></span>  
  
  <span data-ttu-id="e47bb-113">工作分解结构中的项目计划具有熟悉的外观和感觉，并配有交互式甘特图。</span><span class="sxs-lookup"><span data-stu-id="e47bb-113">The project schedule in the work breakdown structure has a familiar look and feel, complete with an interactive Gantt chart.</span></span>  
  
## <a name="create-a-work-breakdown-structure-for-a-project"></a><span data-ttu-id="e47bb-114">为项目创建工作分解结构</span><span class="sxs-lookup"><span data-stu-id="e47bb-114">Create a work breakdown structure for a project</span></span>  
 <span data-ttu-id="e47bb-115">创建工作分解结构来表示项目中任务的序列。</span><span class="sxs-lookup"><span data-stu-id="e47bb-115">Create a work breakdown structure to represent the sequence of tasks in a project.</span></span> <span data-ttu-id="e47bb-116">工作分解结构包括任务、每项任务的要求以及收入和成本信息。</span><span class="sxs-lookup"><span data-stu-id="e47bb-116">The work breakdown structure includes tasks, requirements for each task, and revenue and cost information.</span></span> <span data-ttu-id="e47bb-117">在您的工作分解结构中，您可以添加：</span><span class="sxs-lookup"><span data-stu-id="e47bb-117">In your work breakdown structure, you can add:</span></span>  
  
-   <span data-ttu-id="e47bb-118">层次结构中的任务序列</span><span class="sxs-lookup"><span data-stu-id="e47bb-118">The sequence of tasks in a hierarchy</span></span>  
  
-   <span data-ttu-id="e47bb-119">必须在任务启动之前完成的其他任务（如果有）</span><span class="sxs-lookup"><span data-stu-id="e47bb-119">Other tasks, if any, that must be completed before a task can be started</span></span>  
  
-   <span data-ttu-id="e47bb-120">任务开始日期、结束日期和持续时间</span><span class="sxs-lookup"><span data-stu-id="e47bb-120">The starting date, ending date, and duration of a task</span></span>  
  
-   <span data-ttu-id="e47bb-121">执行任务所需的小时数</span><span class="sxs-lookup"><span data-stu-id="e47bb-121">The number of hours required for a task</span></span>  
  
-   <span data-ttu-id="e47bb-122">任何所需的工作人员技能和教育</span><span class="sxs-lookup"><span data-stu-id="e47bb-122">Any required worker skills and education</span></span>  
  
-   <span data-ttu-id="e47bb-123">分配给任务的工作人员</span><span class="sxs-lookup"><span data-stu-id="e47bb-123">The workers who are assigned to a task</span></span>  
  
-   <span data-ttu-id="e47bb-124">预计收入和成本</span><span class="sxs-lookup"><span data-stu-id="e47bb-124">Estimated revenue and costs</span></span>  
  
## <a name="task-types"></a><span data-ttu-id="e47bb-125">任务类型</span><span class="sxs-lookup"><span data-stu-id="e47bb-125">Task types</span></span>  
<span data-ttu-id="e47bb-126">创建工作分解结构时，您可以使用下列类型的任务：</span><span class="sxs-lookup"><span data-stu-id="e47bb-126">You’ll use the following types of tasks when creating your work breakdown structure:</span></span>  

| | | 
|---------------------------------------|-----------------------------------------------------------------| 
| <span data-ttu-id="e47bb-127">**项目根节点**</span><span class="sxs-lookup"><span data-stu-id="e47bb-127">**Project root node**</span></span> | <span data-ttu-id="e47bb-128">项目的高级摘要任务。</span><span class="sxs-lookup"><span data-stu-id="e47bb-128">The top-level summary task for the project.</span></span> <span data-ttu-id="e47bb-129">该任务下方创建所有其他项目任务。</span><span class="sxs-lookup"><span data-stu-id="e47bb-129">All other project tasks are created under it.</span></span> <span data-ttu-id="e47bb-130">根任务的名称是项目名称。</span><span class="sxs-lookup"><span data-stu-id="e47bb-130">The name of the root task is the project name.</span></span> <span data-ttu-id="e47bb-131">根节点的工作量、日期和持续时间基于其下方的层次结构的值。</span><span class="sxs-lookup"><span data-stu-id="e47bb-131">The effort, dates, and duration of the root node are based on the values on the hierarchy below it.</span></span> <span data-ttu-id="e47bb-132">您不能编辑根节点属性或删除根节点。</span><span class="sxs-lookup"><span data-stu-id="e47bb-132">You can’t edit root node properties or delete the root node.</span></span> | 
| <span data-ttu-id="e47bb-133">**摘要或容器任务**</span><span class="sxs-lookup"><span data-stu-id="e47bb-133">**Summary or container tasks**</span></span> | <span data-ttu-id="e47bb-134">摘要任务是其下方具有子任务的任务。</span><span class="sxs-lookup"><span data-stu-id="e47bb-134">A summary task is a task that has sub-tasks under it.</span></span> <span data-ttu-id="e47bb-135">摘要任务没有其自己的任何工作量或成本。</span><span class="sxs-lookup"><span data-stu-id="e47bb-135">A summary task doesn’t have any work effort or cost of its own.</span></span> <span data-ttu-id="e47bb-136">它的工作量和成本是其子任务的汇总。</span><span class="sxs-lookup"><span data-stu-id="e47bb-136">Its work effort and cost are a rollup of its sub-tasks.</span></span> <span data-ttu-id="e47bb-137">您可以更改摘要任务的名称，但是无法更改工作量、日期或持续时间，因为这些是自动计算的。</span><span class="sxs-lookup"><span data-stu-id="e47bb-137">You can change the name of a summary task, but you can’t change the effort, dates, or duration, because those are automatically calculated.</span></span> <span data-ttu-id="e47bb-138">删除摘要任务将删除该任务及其所有子任务。</span><span class="sxs-lookup"><span data-stu-id="e47bb-138">Deleting a summary task deletes the task and all of its sub-tasks.</span></span>|  
| <span data-ttu-id="e47bb-139">**叶节点任务**</span><span class="sxs-lookup"><span data-stu-id="e47bb-139">**Leaf node tasks**</span></span> | <span data-ttu-id="e47bb-140">叶节点任务表示有关项目的最详细工作。</span><span class="sxs-lookup"><span data-stu-id="e47bb-140">A leaf node task represents the most detailed work on the project.</span></span> <span data-ttu-id="e47bb-141">它具有估算工作量、计划资源数、计划开始和结束日期以及持续时间。</span><span class="sxs-lookup"><span data-stu-id="e47bb-141">It has an estimated effort, a planned number of resources, planned start and end dates, and a duration.</span></span>|

  
## <a name="task-hierarchy"></a><span data-ttu-id="e47bb-142">任务层次结构</span><span class="sxs-lookup"><span data-stu-id="e47bb-142">Task hierarchy</span></span>  
 <span data-ttu-id="e47bb-143">创建任务层次结构时，您有以下选项：</span><span class="sxs-lookup"><span data-stu-id="e47bb-143">You have the following options when creating a task hierarchy:</span></span>  
  
- <span data-ttu-id="e47bb-144">**添加任务**。</span><span class="sxs-lookup"><span data-stu-id="e47bb-144">**Add task**.</span></span>   <span data-ttu-id="e47bb-145">您可以将任务添加到在任务层级结构中选择的位置。</span><span class="sxs-lookup"><span data-stu-id="e47bb-145">You can add a task at a position you choose in the task hierarchy.</span></span> <span data-ttu-id="e47bb-146">如果您不选择位置，新的任务将出现在末尾。</span><span class="sxs-lookup"><span data-stu-id="e47bb-146">If you don’t select a position, your new task appears at the end.</span></span>  
  
- <span data-ttu-id="e47bb-147">**缩进任务**。</span><span class="sxs-lookup"><span data-stu-id="e47bb-147">**Indent task**.</span></span>   <span data-ttu-id="e47bb-148">缩进任务，以使它成为其正上方的子任务。</span><span class="sxs-lookup"><span data-stu-id="e47bb-148">Indent a task to make it a child of the task directly above it.</span></span>  
  
- <span data-ttu-id="e47bb-149">**减少缩进任务**。</span><span class="sxs-lookup"><span data-stu-id="e47bb-149">**Outdent task**.</span></span>   <span data-ttu-id="e47bb-150">减少缩进任务，以使它不再是其原始父任务的子任务。</span><span class="sxs-lookup"><span data-stu-id="e47bb-150">Outdent a task to make it so it’s no longer a sub-task of its original parent task.</span></span>  
  
- <span data-ttu-id="e47bb-151">**上移和下移**。</span><span class="sxs-lookup"><span data-stu-id="e47bb-151">**Move up and Move down**.</span></span>   <span data-ttu-id="e47bb-152">将任务在其父任务的层次结构中向上移动和向下移动。</span><span class="sxs-lookup"><span data-stu-id="e47bb-152">Move tasks up and down in the hierarchy of its parent task.</span></span> <span data-ttu-id="e47bb-153">将任务向上或向下移动对其工作量、成本、日期或持续时间没有影响。</span><span class="sxs-lookup"><span data-stu-id="e47bb-153">Moving a task up or down has no effect on its effort, cost, dates, or duration.</span></span>  
  
## <a name="task-attributes"></a><span data-ttu-id="e47bb-154">任务属性</span><span class="sxs-lookup"><span data-stu-id="e47bb-154">Task attributes</span></span>  
 <span data-ttu-id="e47bb-155">任务的名称描述需要完成的工作。</span><span class="sxs-lookup"><span data-stu-id="e47bb-155">A task’s name describes the work that needs to be completed.</span></span> <span data-ttu-id="e47bb-156">您可以使用各种任务属性来描述该任务的计划和人员配备要求。</span><span class="sxs-lookup"><span data-stu-id="e47bb-156">You use various task attributes to describe the schedule and staffing requirements for the task.</span></span>  
  
### <a name="schedule-attributes"></a><span data-ttu-id="e47bb-157">计划属性</span><span class="sxs-lookup"><span data-stu-id="e47bb-157">Schedule attributes</span></span>

 - <span data-ttu-id="e47bb-158">将值分配给 **工作量时数**、**资源数**、**开始日期**、**结束日期** 和 **持续时间**，以确定任务的计划。</span><span class="sxs-lookup"><span data-stu-id="e47bb-158">Assign values to **Effort hours**, **Number of resources**, **Start date**, **End date**, and **Duration** to determine the schedule for the task.</span></span> 
 - <span data-ttu-id="e47bb-159">**工作量** 是完成任务所需的估计小时数。</span><span class="sxs-lookup"><span data-stu-id="e47bb-159">**Effort** is an estimate of the hours it takes to complete the task.</span></span>
 - <span data-ttu-id="e47bb-160">**资源数** 是项目经理投入任务以帮助制定最佳可能计划的估计资源数。</span><span class="sxs-lookup"><span data-stu-id="e47bb-160">**Number of resources** is an estimate that the project manager puts in the task to help come up with the best possible schedule.</span></span> 
 - <span data-ttu-id="e47bb-161">**持续时间**（以天计）指示完成任务所需的工作日数。</span><span class="sxs-lookup"><span data-stu-id="e47bb-161">**Duration** (in days) indicates the number of work days it will take to complete the task.</span></span>  
  
### <a name="staffing-attributes"></a><span data-ttu-id="e47bb-162">人员配备属性</span><span class="sxs-lookup"><span data-stu-id="e47bb-162">Staffing attributes</span></span>

 - <span data-ttu-id="e47bb-163">**角色**、**资源部门**、**资源数** 和 **资源** 描述任务的人员配备要求。</span><span class="sxs-lookup"><span data-stu-id="e47bb-163">**Role**, **Resource organizational unit**, **Number of resources**, and **Resources** describe the staffing requirements for the task.</span></span> 
 - <span data-ttu-id="e47bb-164">**角色** 描述执行任务所需的资源类型。</span><span class="sxs-lookup"><span data-stu-id="e47bb-164">**Role** describes the type of resource needed to perform the task.</span></span> 
 - <span data-ttu-id="e47bb-165">**资源部门** 指示应为该任务调配其资源的部门；它还会影响任务的成本和销售估算值，因为确定资源的单位售价时，需考虑资源部门。</span><span class="sxs-lookup"><span data-stu-id="e47bb-165">**Resource organizational unit** indicates the organizational unit from which resources should be staffed for that task; this also impacts the cost and sales estimate of the task, since this is accounted for when determining the unit sales price for the resource.</span></span> 
 - <span data-ttu-id="e47bb-166">**资源** 保留通用资源或命名资源（若找到）。</span><span class="sxs-lookup"><span data-stu-id="e47bb-166">**Resources** holds a generic resource or a named resource when one is found.</span></span>  
  
## <a name="task-dependencies"></a><span data-ttu-id="e47bb-167">任务依赖关系</span><span class="sxs-lookup"><span data-stu-id="e47bb-167">Task dependencies</span></span>  
 <span data-ttu-id="e47bb-168">您可以在工作分解结构的一个或多个任务之间创建前任关系。</span><span class="sxs-lookup"><span data-stu-id="e47bb-168">You can create predecessor relationships between one or more tasks in the work breakdown structure.</span></span> <span data-ttu-id="e47bb-169">您可以为任务的前任字段设置一个或多个值，以指示其所依赖的任务。</span><span class="sxs-lookup"><span data-stu-id="e47bb-169">You can set one or more values for the predecessor field on tasks to indicate the tasks that it will be dependent on.</span></span> <span data-ttu-id="e47bb-170">当您向任务分配前任值时，该任务仅在所有前任任务都已完成时才会启动。</span><span class="sxs-lookup"><span data-stu-id="e47bb-170">When you assign a predecessor value to a task, the task can only start when all the predecessor tasks have completed.</span></span> <span data-ttu-id="e47bb-171">设置任务的此依赖关系会导致将任务的计划开始日期重新计算为所有其前任的最新结束日期。</span><span class="sxs-lookup"><span data-stu-id="e47bb-171">Setting this dependency on a task will result in the recalculation of the planned start date of the task as the latest end of all of its predecessors.</span></span> <span data-ttu-id="e47bb-172">有关计划的前任相关影响不是通过对任务定义的任务模式进行限制。</span><span class="sxs-lookup"><span data-stu-id="e47bb-172">Predecessor-related impacts on a schedule are not limited by the task mode defined on the task.</span></span>  
  
## <a name="task-mode"></a><span data-ttu-id="e47bb-173">任务模式</span><span class="sxs-lookup"><span data-stu-id="e47bb-173">Task mode</span></span>  
 <span data-ttu-id="e47bb-174">任务模式是确定计划叶节点任务的重要因素之一。</span><span class="sxs-lookup"><span data-stu-id="e47bb-174">Task mode is one of the important factors that determine scheduling leaf node tasks.</span></span> <span data-ttu-id="e47bb-175">每项任务都有两个任务模式：自动计划模式和手动计划模式。</span><span class="sxs-lookup"><span data-stu-id="e47bb-175">There are two task modes for every task: auto scheduling mode and manual scheduling mode.</span></span>  
  
-   <span data-ttu-id="e47bb-176">**自动计划**。</span><span class="sxs-lookup"><span data-stu-id="e47bb-176">**Auto scheduling**.</span></span>   <span data-ttu-id="e47bb-177">当您将任务模式设置为“自动计划”时，任务计划引擎将使用有关下列任务属性的计划规则来确定任务的计划：</span><span class="sxs-lookup"><span data-stu-id="e47bb-177">When you set the task mode to Automatically Scheduled, the task scheduling engine uses the scheduling rules on the following task attributes to determine the schedule for the task:</span></span>  
  
    -   <span data-ttu-id="e47bb-178">前任</span><span class="sxs-lookup"><span data-stu-id="e47bb-178">Predecessors</span></span>  
  
    -   <span data-ttu-id="e47bb-179">工作量</span><span class="sxs-lookup"><span data-stu-id="e47bb-179">Effort</span></span>  
  
    -   <span data-ttu-id="e47bb-180">资源数</span><span class="sxs-lookup"><span data-stu-id="e47bb-180">Number of resources</span></span>  
  
    -   <span data-ttu-id="e47bb-181">开始和结束日期</span><span class="sxs-lookup"><span data-stu-id="e47bb-181">Start and end dates</span></span>  
  
-   <span data-ttu-id="e47bb-182">**计划规则**。</span><span class="sxs-lookup"><span data-stu-id="e47bb-182">**Scheduling rules**.</span></span>   <span data-ttu-id="e47bb-183">不具有前任的叶节点任务的开始日期默认为项目的计划开始日期。</span><span class="sxs-lookup"><span data-stu-id="e47bb-183">The start date of a leaf node task that does not have predecessors defaults to the project’s scheduling start date.</span></span> <span data-ttu-id="e47bb-184">叶节点任务的持续时间总是计算为其开始日期与结束日期之间的工作日数。</span><span class="sxs-lookup"><span data-stu-id="e47bb-184">The duration of a leaf node task is always calculated as the number of working days between its start and end dates.</span></span> <span data-ttu-id="e47bb-185">当任务自动计划时，计划引擎遵守如下规则：</span><span class="sxs-lookup"><span data-stu-id="e47bb-185">When a task is automatically scheduled, the scheduling engine follows the rules below:</span></span>  
  
    -   <span data-ttu-id="e47bb-186">任务的开始和结束日期必须总是为符合项目计划日历的工作日</span><span class="sxs-lookup"><span data-stu-id="e47bb-186">Start and end dates of a task must always be working days according to the project’s scheduling calendar</span></span>  
  
    -   <span data-ttu-id="e47bb-187">具有前任的任务的开始日期默认为其前任的最新结束日期</span><span class="sxs-lookup"><span data-stu-id="e47bb-187">The start date of a task that has predecessors defaults to the latest end date of its predecessors</span></span>  
  
    -   <span data-ttu-id="e47bb-188">工作量 = 项目日历中一个标准工作日内的人数 \* 持续时间 \* 小时数</span><span class="sxs-lookup"><span data-stu-id="e47bb-188">Effort = Number of people \* Duration \* hours in a standard work day of the project calendar</span></span>  
  
-   <span data-ttu-id="e47bb-189">**手动计划**。</span><span class="sxs-lookup"><span data-stu-id="e47bb-189">**Manual scheduling**.</span></span>   <span data-ttu-id="e47bb-190">在某些情况下，您可能想要不遵守这些规则。</span><span class="sxs-lookup"><span data-stu-id="e47bb-190">In some cases, you might want to deviate from these rules.</span></span> <span data-ttu-id="e47bb-191">在这些情况下，您可将任务的任务模式设置为手动计划。</span><span class="sxs-lookup"><span data-stu-id="e47bb-191">In these cases, you can set the task mode for the task to be manually scheduled.</span></span> <span data-ttu-id="e47bb-192">这会阻止计划引擎计算其他计划属性的值。</span><span class="sxs-lookup"><span data-stu-id="e47bb-192">This stops the scheduling engine from calculating the values for other scheduling attributes.</span></span> <span data-ttu-id="e47bb-193">设置任务前任总是会影响依赖任务的开始日期。</span><span class="sxs-lookup"><span data-stu-id="e47bb-193">Setting predecessors on tasks always impacts the dependent task’s start date.</span></span>  
  
## <a name="create-a-work-breakdown-structure"></a><span data-ttu-id="e47bb-194">创建工作分解结构</span><span class="sxs-lookup"><span data-stu-id="e47bb-194">Create a work breakdown structure</span></span>  
  
1.  <span data-ttu-id="e47bb-195">转到 **Project Service > 项目**。</span><span class="sxs-lookup"><span data-stu-id="e47bb-195">Go to **Project Service > Projects**.</span></span>  
  
2.  <span data-ttu-id="e47bb-196">单击要处理的项目。</span><span class="sxs-lookup"><span data-stu-id="e47bb-196">Click the project you want to work on.</span></span>  
  
3.  <span data-ttu-id="e47bb-197">在屏幕顶部横栏中，选择项目名称旁边的向下箭头，然后单击工作分解结构。</span><span class="sxs-lookup"><span data-stu-id="e47bb-197">In the bar across the top of the screen, select the down arrow next to the project name, and then click Work breakdown structure.</span></span>  
  
4.  <span data-ttu-id="e47bb-198">若要添加任务，请单击 **添加任务**。</span><span class="sxs-lookup"><span data-stu-id="e47bb-198">To add a task, click **Add Task**.</span></span> <span data-ttu-id="e47bb-199">填写任务的字段，然后单击 **保存**。</span><span class="sxs-lookup"><span data-stu-id="e47bb-199">Fill in the fields for the task, and then click **Save**.</span></span>  
  
5.  <span data-ttu-id="e47bb-200">继续添加任务，直到您的工作分解结构完成。</span><span class="sxs-lookup"><span data-stu-id="e47bb-200">Continue adding tasks until your work breakdown structure is complete.</span></span> <span data-ttu-id="e47bb-201">创建工作分解结构时，您可以执行以下操作来组织您的任务：</span><span class="sxs-lookup"><span data-stu-id="e47bb-201">While creating your work breakdown structure, you can do the following to organize your tasks:</span></span>  
  
    -   <span data-ttu-id="e47bb-202">选择一个任务并单击 **缩进** 以将其移动到其他任务的下方或单击“减少缩进“以将其移出位置。</span><span class="sxs-lookup"><span data-stu-id="e47bb-202">Select a task and click **Indent** to move it under another task or click Outdent to move it out a level.</span></span>  
  
    -   <span data-ttu-id="e47bb-203">选择一个任务并单击 **上移** 或 **下移** 以在列表中将其向上或向下移动。</span><span class="sxs-lookup"><span data-stu-id="e47bb-203">Select a task and click **Move Up** or **Move Down** to move it up or down in the list.</span></span>  
  
    -   <span data-ttu-id="e47bb-204">单击 **隐藏甘特图** 隐藏甘特图，或单击 **显示甘特图** 以再次显示甘特图。</span><span class="sxs-lookup"><span data-stu-id="e47bb-204">Click **Hide Gantt** to hide the Gantt chart, and click **Show Gantt** to display it again.</span></span>  
  
    -   <span data-ttu-id="e47bb-205">在 **时间刻度** 中为甘特图选择不同的时间段。</span><span class="sxs-lookup"><span data-stu-id="e47bb-205">Select a different period of time for the Gantt chart in **Time Scale**.</span></span>  
  
6.  <span data-ttu-id="e47bb-206">若要将您在工作分解结构中指定的角色添加至项目团队成员，单击 **生成项目团队**。</span><span class="sxs-lookup"><span data-stu-id="e47bb-206">To add the roles you specified in your work breakdown structure to your project’s team members, click **Generate Project Team**.</span></span>  
  
7.  <span data-ttu-id="e47bb-207">更改完毕之后，单击屏幕右下角的 **保存**。</span><span class="sxs-lookup"><span data-stu-id="e47bb-207">Click **Save** at the bottom right corner of the screen when you’re done making changes.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="e47bb-208">另请参阅</span><span class="sxs-lookup"><span data-stu-id="e47bb-208">See Also</span></span>  
 [<span data-ttu-id="e47bb-209">项目经理指南</span><span class="sxs-lookup"><span data-stu-id="e47bb-209">Project manager guide</span></span>](../psa/project-manager-guide.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]