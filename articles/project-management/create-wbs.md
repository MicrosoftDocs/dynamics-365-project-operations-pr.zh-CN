---
title: 创建工作分解结构
description: 本主题说明如何在新计划界面中创建包括基本控件的工作分解结构 (WBS)。
author: ruhercul
manager: tfehr
ms.date: 01/07/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 695bbc2ae1ba1e762472b5f5fa853c89017d2f52
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/15/2021
ms.locfileid: "5287002"
---
# <a name="create-a-work-breakdown-structure-wbs"></a><span data-ttu-id="71840-103">创建工作分解结构 (WBS)</span><span class="sxs-lookup"><span data-stu-id="71840-103">Create a work breakdown structure (WBS)</span></span>

<span data-ttu-id="71840-104">项目计划传达必须执行哪些工作、哪些资源执行工作及必须完成工作的时限。</span><span class="sxs-lookup"><span data-stu-id="71840-104">A project schedule communicates what work must be completed, which resources will do the work, and the timeframe in which the work must be completed.</span></span> <span data-ttu-id="71840-105">计划反映与按期交付项目相关的所有工作。</span><span class="sxs-lookup"><span data-stu-id="71840-105">The schedule reflects all the work associated with delivering the project on time.</span></span> <span data-ttu-id="71840-106">在 Dynamics 365 Project Operations 中，您可以通过以下方式创建项目计划：</span><span class="sxs-lookup"><span data-stu-id="71840-106">In Dynamics 365 Project Operations, you create a project schedule by:</span></span>

  - <span data-ttu-id="71840-107">将工作分解为可管理的任务。</span><span class="sxs-lookup"><span data-stu-id="71840-107">Breaking the work down into manageable tasks.</span></span>
  - <span data-ttu-id="71840-108">估计执行每个任务所需要的时间。</span><span class="sxs-lookup"><span data-stu-id="71840-108">Estimating the time that is required to do each task.</span></span>
  - <span data-ttu-id="71840-109">设置任务依赖关系。</span><span class="sxs-lookup"><span data-stu-id="71840-109">Setting task dependencies.</span></span>
  - <span data-ttu-id="71840-110">设置任务持续时间。</span><span class="sxs-lookup"><span data-stu-id="71840-110">Setting task durations.</span></span>
  - <span data-ttu-id="71840-111">估计将执行这些任务的通用资源。</span><span class="sxs-lookup"><span data-stu-id="71840-111">Estimating the generic resources that will do the tasks.</span></span> 

<span data-ttu-id="71840-112">项目计划在 **项目** 页的 **计划** 选项卡上创建。</span><span class="sxs-lookup"><span data-stu-id="71840-112">The project schedule is created on the **Schedule** tab on the **Project** page.</span></span>

## <a name="tasks"></a><span data-ttu-id="71840-113">任务</span><span class="sxs-lookup"><span data-stu-id="71840-113">Tasks</span></span>

<span data-ttu-id="71840-114">创建项目计划的第一步是将工作分解为可管理部分。</span><span class="sxs-lookup"><span data-stu-id="71840-114">The first step in creating a project schedule is to break the work down into manageable portions.</span></span> <span data-ttu-id="71840-115">Project Operations 中的计划支持以下功能：</span><span class="sxs-lookup"><span data-stu-id="71840-115">The schedule in Project Operations supports the following features:</span></span>

- <span data-ttu-id="71840-116">摘要或容器任务</span><span class="sxs-lookup"><span data-stu-id="71840-116">Summary or container tasks</span></span>
- <span data-ttu-id="71840-117">叶节点任务</span><span class="sxs-lookup"><span data-stu-id="71840-117">Leaf node tasks</span></span>

### <a name="summary-tasks"></a><span data-ttu-id="71840-118">摘要任务</span><span class="sxs-lookup"><span data-stu-id="71840-118">Summary tasks</span></span>

<span data-ttu-id="71840-119">摘要任务可以存储其他摘要任务或叶级节点任务。</span><span class="sxs-lookup"><span data-stu-id="71840-119">Summary tasks can store other summary tasks or leaf node tasks.</span></span> <span data-ttu-id="71840-120">这些任务没有自己的工作量或成本。</span><span class="sxs-lookup"><span data-stu-id="71840-120">They have no work effort or cost of their own.</span></span> <span data-ttu-id="71840-121">相反，其工作量和成本是其容器任务的工作量和成本的汇总。</span><span class="sxs-lookup"><span data-stu-id="71840-121">Instead, their work effort and cost are a rollup of the work effort and cost of their container tasks.</span></span> <span data-ttu-id="71840-122">汇总任务的开始日期和结束日期分别是容器任务的开始日期和结束日期。</span><span class="sxs-lookup"><span data-stu-id="71840-122">The start date of the summary task is the start date of the container tasks, and the end date is the end date of the container tasks.</span></span> <span data-ttu-id="71840-123">可以编辑汇总任务的名称，但是不能编辑计划属性，包括工作量、日期和持续时间。</span><span class="sxs-lookup"><span data-stu-id="71840-123">The name of a summary task can be edited, but scheduling properties, including effort, dates, and duration, can't be edited.</span></span> <span data-ttu-id="71840-124">如果删除一个汇总任务，也会删除其所有容器任务。</span><span class="sxs-lookup"><span data-stu-id="71840-124">If you delete a summary task, you also delete all its container tasks.</span></span>

### <a name="leaf-node-tasks"></a><span data-ttu-id="71840-125">叶节点任务</span><span class="sxs-lookup"><span data-stu-id="71840-125">Leaf node tasks</span></span>

<span data-ttu-id="71840-126">叶节点任务表示有关项目的最详细工作。</span><span class="sxs-lookup"><span data-stu-id="71840-126">Leaf node tasks represent the most granular work on the project.</span></span> <span data-ttu-id="71840-127">它们具有估算工作量、资源、计划开始和结束日期以及持续时间。</span><span class="sxs-lookup"><span data-stu-id="71840-127">They have an estimated effort, resources, planned start and end dates, and a duration.</span></span>

## <a name="create-a-task-hierarchy"></a><span data-ttu-id="71840-128">创建任务层次结构</span><span class="sxs-lookup"><span data-stu-id="71840-128">Create a task hierarchy</span></span>

### <a name="add-a-task"></a><span data-ttu-id="71840-129">添加任务</span><span class="sxs-lookup"><span data-stu-id="71840-129">Add a task</span></span>

<span data-ttu-id="71840-130">完成以下步骤添加一个或多个任务。</span><span class="sxs-lookup"><span data-stu-id="71840-130">Complete the following steps to add one or more tasks.</span></span>

1. <span data-ttu-id="71840-131">转到 **项目**，然后选择并打开您要为其创建计划的项目记录。</span><span class="sxs-lookup"><span data-stu-id="71840-131">Go to **Projects** and select and open the project record for which you want to create a schedule.</span></span> 
2. <span data-ttu-id="71840-132">选择 **任务** 选项卡。</span><span class="sxs-lookup"><span data-stu-id="71840-132">Select the **Tasks** tab.</span></span> 
3. <span data-ttu-id="71840-133">选择 **添加新任务**，为任务输入名称，然后按 Enter。</span><span class="sxs-lookup"><span data-stu-id="71840-133">Select **Add new task**, enter a name for the task, and then press Enter.</span></span>
2. <span data-ttu-id="71840-134">输入另一个任务名称，再次按 Enter，直到获得完整的任务列表。</span><span class="sxs-lookup"><span data-stu-id="71840-134">Enter another task name and press Enter again until you have a full list of tasks.</span></span>

### <a name="manage-hierarchy-of-a-task"></a><span data-ttu-id="71840-135">管理任务的层次结构</span><span class="sxs-lookup"><span data-stu-id="71840-135">Manage hierarchy of a task</span></span>

<span data-ttu-id="71840-136">如果缩进某个任务，该任务将成为其上任务的子级。</span><span class="sxs-lookup"><span data-stu-id="71840-136">When a task is indented, it becomes a child of the task that is directly above it.</span></span> <span data-ttu-id="71840-137">然后重新计算该任务的计划 ID，使其基于其新父级的计划 ID，并采用大纲编号方案。</span><span class="sxs-lookup"><span data-stu-id="71840-137">The schedule ID of the task is then recalculated so that it's based on the schedule ID of its new parent and follows the outline numbering scheme.</span></span> <span data-ttu-id="71840-138">现在，父任务是一个摘要任务。</span><span class="sxs-lookup"><span data-stu-id="71840-138">The parent task is now a summary task.</span></span> <span data-ttu-id="71840-139">因此，成为其子任务的汇总。</span><span class="sxs-lookup"><span data-stu-id="71840-139">Therefore, it becomes a rollup of its child tasks.</span></span> <span data-ttu-id="71840-140">任务提升后，该任务不再是原父级任务的子级。</span><span class="sxs-lookup"><span data-stu-id="71840-140">When a task is promoted, it's no longer a child of the task that was its parent.</span></span> <span data-ttu-id="71840-141">然后重新计算计划 ID，以便体现该任务在层次结构中更新后的深度和位置。</span><span class="sxs-lookup"><span data-stu-id="71840-141">The schedule ID is then recalculated so that it reflects the task's updated depth and position in the hierarchy.</span></span> <span data-ttu-id="71840-142">将重新计算原父任务的工作量、成本和日期，以便其不包含此任务。</span><span class="sxs-lookup"><span data-stu-id="71840-142">The effort, cost, and dates of the previous parent task are recalculated so that they don't include this task.</span></span>

<span data-ttu-id="71840-143">完成以下步骤缩进或提升任务。</span><span class="sxs-lookup"><span data-stu-id="71840-143">Complete the following steps to indent or promote a task.</span></span>

1. <span data-ttu-id="71840-144">在 **项目** 页面上的 **任务** 选项卡上，在 **摘要任务** 下，选择任务名称旁边的三个垂直点，然后选择 **设为子任务**。</span><span class="sxs-lookup"><span data-stu-id="71840-144">On the **Project** page, on the **Tasks** tab, under **Summary tasks**, select the three vertical dots by the task name, and then select **Make subtask**.</span></span> 
2. <span data-ttu-id="71840-145">选择要缩进或提升的任务。</span><span class="sxs-lookup"><span data-stu-id="71840-145">Select the task to indent or promote.</span></span> <span data-ttu-id="71840-146">要选择多个任务，请选择任务，请按住 Ctrl，然后选择其他任务。</span><span class="sxs-lookup"><span data-stu-id="71840-146">To select more than one task, select a task, press and hold Ctrl, and then select additional tasks.</span></span>
2. <span data-ttu-id="71840-147">选择 **缩进** 或 **提升子任务** 可以将任务移到摘要任务下或从中移出。</span><span class="sxs-lookup"><span data-stu-id="71840-147">Select **Indent** or **Promote subtask**  to move tasks under or out from under summary tasks.</span></span>

### <a name="move-tasks-up-and-down"></a><span data-ttu-id="71840-148">上移和下移任务</span><span class="sxs-lookup"><span data-stu-id="71840-148">Move tasks up and down</span></span>

<span data-ttu-id="71840-149">可以通过以下两种方法之一将任务转移到工作分解结构的任何级别：</span><span class="sxs-lookup"><span data-stu-id="71840-149">Tasks can me moved to any level in the work breakdown structure in one of two ways:</span></span>

- <span data-ttu-id="71840-150">选择一个或多个任务，然后将其拖动到所需位置。</span><span class="sxs-lookup"><span data-stu-id="71840-150">Select one more tasks and drag them to the desired location.</span></span>
- <span data-ttu-id="71840-151">选择一个或多个任务，右键单击并选择 **剪切**，在计划中选择目标单元格，然后右键单击并选择 **粘贴**。</span><span class="sxs-lookup"><span data-stu-id="71840-151">Select one or more tasks, right-click and select **Cut**, select the destination cell in the schedule, and then right-click and select **Paste**.</span></span>

## <a name="task-attributes"></a><span data-ttu-id="71840-152">任务属性</span><span class="sxs-lookup"><span data-stu-id="71840-152">Task attributes</span></span>

<span data-ttu-id="71840-153">任务的名称描述必须完成的工作。</span><span class="sxs-lookup"><span data-stu-id="71840-153">A task's name describes the work that must be completed.</span></span> <span data-ttu-id="71840-154">在 Project Operations 中，与任务关联的属性描述任务的计划及其人员配备要求。</span><span class="sxs-lookup"><span data-stu-id="71840-154">In Project Operations, the attributes associated with a task describe the schedule of the task and its staffing requirements.</span></span>

## <a name="schedule-attributes"></a><span data-ttu-id="71840-155">计划属性</span><span class="sxs-lookup"><span data-stu-id="71840-155">Schedule attributes</span></span>

<span data-ttu-id="71840-156">**工作量**、**开始日期**、**结束日期** 和 **持续时间** 属性定义任务的计划。</span><span class="sxs-lookup"><span data-stu-id="71840-156">The **Effort**, **Start date**, **End date**, and **Duration** attributes define the schedule for the task.</span></span>

<span data-ttu-id="71840-157">下表显示了其他计划属性。</span><span class="sxs-lookup"><span data-stu-id="71840-157">The following table shows additional schedule attributes.</span></span>

| <span data-ttu-id="71840-158">**最终显示名称**</span><span class="sxs-lookup"><span data-stu-id="71840-158">**Final display name**</span></span> | <span data-ttu-id="71840-159">**最终说明**</span><span class="sxs-lookup"><span data-stu-id="71840-159">**Final description**</span></span> |
| --- | --- |
| <span data-ttu-id="71840-160">已完成工作量(小时)</span><span class="sxs-lookup"><span data-stu-id="71840-160">Effort Completed (Hours)</span></span> | <span data-ttu-id="71840-161">任务已完成工时，以小时计。</span><span class="sxs-lookup"><span data-stu-id="71840-161">Completed work for the task in hours.</span></span> |
| <span data-ttu-id="71840-162">持续时间</span><span class="sxs-lookup"><span data-stu-id="71840-162">Duration</span></span> | <span data-ttu-id="71840-163">显示任务的持续时间（天）。</span><span class="sxs-lookup"><span data-stu-id="71840-163">Displays the duration in days for the task.</span></span> |
| <span data-ttu-id="71840-164">总工作量</span><span class="sxs-lookup"><span data-stu-id="71840-164">Total Effort</span></span> | <span data-ttu-id="71840-165">任务总工时，以小时计。</span><span class="sxs-lookup"><span data-stu-id="71840-165">Total work for the task in hours.</span></span> |
| <span data-ttu-id="71840-166">完成</span><span class="sxs-lookup"><span data-stu-id="71840-166">Finish</span></span> | <span data-ttu-id="71840-167">完成日期和时间。</span><span class="sxs-lookup"><span data-stu-id="71840-167">Finish date and time.</span></span> |
| <span data-ttu-id="71840-168">已完成百分比</span><span class="sxs-lookup"><span data-stu-id="71840-168">% Complete</span></span> | <span data-ttu-id="71840-169">任务完成的百分比。</span><span class="sxs-lookup"><span data-stu-id="71840-169">The percentage of the task that is complete.</span></span> |
| <span data-ttu-id="71840-170">项目 Bucket</span><span class="sxs-lookup"><span data-stu-id="71840-170">Project Bucket</span></span> | <span data-ttu-id="71840-171">任务板可按 Bucket 分组，这样每个 Bucket 都有自己的列。</span><span class="sxs-lookup"><span data-stu-id="71840-171">The task board can be grouped by bucket so each bucket has its own column.</span></span> |
| <span data-ttu-id="71840-172">剩余工作量(小时)</span><span class="sxs-lookup"><span data-stu-id="71840-172">Effort Remaining (Hours)</span></span> | <span data-ttu-id="71840-173">任务剩余工时，以小时计。</span><span class="sxs-lookup"><span data-stu-id="71840-173">The remaining work for the task in hours.</span></span> |
| <span data-ttu-id="71840-174">开头</span><span class="sxs-lookup"><span data-stu-id="71840-174">Start</span></span> | <span data-ttu-id="71840-175">开始日期和时间。</span><span class="sxs-lookup"><span data-stu-id="71840-175">Start date and time.</span></span> |
| <span data-ttu-id="71840-176">客户</span><span class="sxs-lookup"><span data-stu-id="71840-176">Name</span></span> | <span data-ttu-id="71840-177">任务的名称。</span><span class="sxs-lookup"><span data-stu-id="71840-177">The name of the task.</span></span> |
| <span data-ttu-id="71840-178">ID</span><span class="sxs-lookup"><span data-stu-id="71840-178">ID</span></span> | <span data-ttu-id="71840-179">工作分解结构中的任务的编号。</span><span class="sxs-lookup"><span data-stu-id="71840-179">The ID of the task in the work breakdown structure.</span></span> |

<span data-ttu-id="71840-180">作为管理员，您可以对任务实体定义自定义字段。</span><span class="sxs-lookup"><span data-stu-id="71840-180">As an administrator, you can define custom fields on the task entity.</span></span> <span data-ttu-id="71840-181">但是，字段不能显示在计划网格上。</span><span class="sxs-lookup"><span data-stu-id="71840-181">However the fields can't be displayed on the schedule grid.</span></span> <span data-ttu-id="71840-182">要查看自定义字段，可将其添加到 **项目任务** 详细信息页。</span><span class="sxs-lookup"><span data-stu-id="71840-182">To see your custom fields, add them to the **Project Task** details page.</span></span>

## <a name="staffing-attributes"></a><span data-ttu-id="71840-183">人员配备属性</span><span class="sxs-lookup"><span data-stu-id="71840-183">Staffing attributes</span></span>

<span data-ttu-id="71840-184">人员配备属性通过计划中的 **资源** 字段访问。</span><span class="sxs-lookup"><span data-stu-id="71840-184">Staffing attributes are accessed through the **Resources** field in the schedule.</span></span> <span data-ttu-id="71840-185">可搜索现有资源，或选择 **创建**，然后在 **快速创建** 窗格中把项目团队成员作为新资源添加。</span><span class="sxs-lookup"><span data-stu-id="71840-185">You can either search for an existing resource, or select **Create**, and in the **Quick Create** pane, add a project team member as a new resource.</span></span>

<span data-ttu-id="71840-186">**角色**、**资源单位** 和 **位置名称** 字段用于描述任务的人员配备要求。</span><span class="sxs-lookup"><span data-stu-id="71840-186">The **Role**, **Resourcing Unit**, and **Position Name** fields are used to describe the staffing requirements for the task.</span></span> <span data-ttu-id="71840-187">这些人员配备属性与任务计划一起用于查找可用于完成此任务的资源。</span><span class="sxs-lookup"><span data-stu-id="71840-187">These staffing attributes, together with the task schedule are used to find available resources to do this task.</span></span>

   - <span data-ttu-id="71840-188">**角色**：指定完成任务所需资源类型。</span><span class="sxs-lookup"><span data-stu-id="71840-188">**Role**: Specify the type of resource that is required to do the task.</span></span>
   - <span data-ttu-id="71840-189">**资源单位**：指定应该为分派的资源所属单位。</span><span class="sxs-lookup"><span data-stu-id="71840-189">**Resourcing unit**: Specify the unit that resources for the task should be assigned from.</span></span> <span data-ttu-id="71840-190">如果资源的成本和记帐费率是基于资源单位设置的，则此属性会影响任务的成本和销售额估算。</span><span class="sxs-lookup"><span data-stu-id="71840-190">This attribute affects the cost and sales estimate for the task if the cost and bill rate for the resource are set based on resourcing units.</span></span>
   - <span data-ttu-id="71840-191">**职位名称**：为充当最终将执行工作的资源的占位符的通用资源输入名称。</span><span class="sxs-lookup"><span data-stu-id="71840-191">**Position name**: Enter a name for the generic resource that serves as a placeholder for the resource that will ultimately do the work.</span></span>

<span data-ttu-id="71840-192">**资源** 字段存储通用资源或指定资源被发现时的位置名称。</span><span class="sxs-lookup"><span data-stu-id="71840-192">The **Resources** field holds the position name of the generic resource or named resource when one is found.</span></span>

<span data-ttu-id="71840-193">**类别** 字段存储指示可将任务归入的更广泛工作类型的值。</span><span class="sxs-lookup"><span data-stu-id="71840-193">The **Category** field holds the values that indicate a broader type of work that the task can be grouped into.</span></span> <span data-ttu-id="71840-194">此字段不影响计划或人员配备。</span><span class="sxs-lookup"><span data-stu-id="71840-194">This field doesn't affect scheduling or staffing.</span></span> <span data-ttu-id="71840-195">而只是用于报告。</span><span class="sxs-lookup"><span data-stu-id="71840-195">Instead, the field is used only for reporting.</span></span>

## <a name="task-dependencies"></a><span data-ttu-id="71840-196">任务依赖关系</span><span class="sxs-lookup"><span data-stu-id="71840-196">Task dependencies</span></span>

<span data-ttu-id="71840-197">在 Project Operations 中，可使用计划创建任务之间的前置关系。</span><span class="sxs-lookup"><span data-stu-id="71840-197">You can use the schedule in Project Operations to create predecessor relationships between tasks.</span></span> <span data-ttu-id="71840-198">**前置任务** 字段使用一个或多个值来指示任务的依赖任务。</span><span class="sxs-lookup"><span data-stu-id="71840-198">The **Predecessor** field uses one or more values to indicate the tasks that a task depends on.</span></span> <span data-ttu-id="71840-199">当您向任务分配前置任务值时，该任务仅在所有前置任务都已完成时才能启动。</span><span class="sxs-lookup"><span data-stu-id="71840-199">When predecessor values are assigned to a task, the task can start only after all of the predecessor tasks have been completed.</span></span> <span data-ttu-id="71840-200">由于依赖关系，任务的计划开始日期将重置为前置任务的完成日期。</span><span class="sxs-lookup"><span data-stu-id="71840-200">Because of the dependency, the planned start date of the task is reset to the date when the predecessor tasks are completed.</span></span>

<span data-ttu-id="71840-201">任务模式不影响对前置/依赖任务的开始日期和结束日期进行的更新。</span><span class="sxs-lookup"><span data-stu-id="71840-201">The task mode has no effect on updates that are made to the start and end dates of predecessor/dependent tasks.</span></span>

## <a name="accessibility-and-keyboard-shortcuts"></a><span data-ttu-id="71840-202">辅助功能和键盘快捷方式</span><span class="sxs-lookup"><span data-stu-id="71840-202">Accessibility and keyboard shortcuts</span></span>

<span data-ttu-id="71840-203">**计划** 网格拥有完善的辅助功能，可以与讲述人、JAWS 或 NVDA 之类屏幕阅读器配合使用。</span><span class="sxs-lookup"><span data-stu-id="71840-203">The **Schedule** grid is fully accessible and can be used with screen readers such as Narrator, JAWS, or NVDA.</span></span> <span data-ttu-id="71840-204">可使用箭头键在网格区域中移动（和在 Microsoft Excel 中一样），可以使用 Tab 键在交互式用户界面元素中前进，还可以使用向下键、Enter 将或空格键选择和打开下拉菜单。</span><span class="sxs-lookup"><span data-stu-id="71840-204">You can move through the grid area by using arrow keys (as in Microsoft Excel), you can use the Tab key to advance through the interactive user interface elements, and you can use the Down arrow key, the Enter key, or the Spacebar to select and open the drop-down menus.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]