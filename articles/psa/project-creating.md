---
title: 项目计划
description: 此主题介绍如何创建计划。
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 3/01/2019
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
ms.openlocfilehash: 8f1a0b0ed610ade094546782a1fa517682a390e4
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/15/2021
ms.locfileid: "5283970"
---
# <a name="project-schedules"></a><span data-ttu-id="59385-103">项目计划</span><span class="sxs-lookup"><span data-stu-id="59385-103">Project schedules</span></span> 

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="59385-104">项目计划传达必须执行哪些工作、哪些资源执行工作及必须完成工作的时限。</span><span class="sxs-lookup"><span data-stu-id="59385-104">A project schedule communicates what work must be completed, which resources will do the work, and the timeframe that the work must be finished in.</span></span> <span data-ttu-id="59385-105">它反映与按期交付项目相关的所有工作。</span><span class="sxs-lookup"><span data-stu-id="59385-105">It reflects all the work that is associated with delivering the project on time.</span></span> <span data-ttu-id="59385-106">在 Dynamics 365 Project Service Automation 中，项目计划的创建方法是，将工作分解为可管理任务，估算完成每项任务所需时间，设置任务依赖关系，设置任务持续时间，以及估算执行任务的通用资源。</span><span class="sxs-lookup"><span data-stu-id="59385-106">In Dynamics 365 Project Service Automation, you create a project schedule by breaking the work down into manageable tasks, estimating the time that is required to do each task, setting task dependencies, setting task durations, and estimating the generic resources that will do the tasks.</span></span> <span data-ttu-id="59385-107">项目计划在项目页的 **计划** 选项卡上创建。</span><span class="sxs-lookup"><span data-stu-id="59385-107">The project schedule is created on the **Schedule** tab of the project page.</span></span>
 
## <a name="tasks"></a><span data-ttu-id="59385-108">任务</span><span class="sxs-lookup"><span data-stu-id="59385-108">Tasks</span></span>

<span data-ttu-id="59385-109">创建项目计划的第一步是将工作分解为可管理部分。</span><span class="sxs-lookup"><span data-stu-id="59385-109">The first step in creating a project schedule is to break the work down into manageable portions.</span></span> <span data-ttu-id="59385-110">PSA 中的计划支持以下功能：</span><span class="sxs-lookup"><span data-stu-id="59385-110">The schedule in PSA supports the following features:</span></span>

- <span data-ttu-id="59385-111">项目根节点</span><span class="sxs-lookup"><span data-stu-id="59385-111">Project root node</span></span>
- <span data-ttu-id="59385-112">摘要或容器任务</span><span class="sxs-lookup"><span data-stu-id="59385-112">Summary or container tasks</span></span>
- <span data-ttu-id="59385-113">叶节点任务</span><span class="sxs-lookup"><span data-stu-id="59385-113">Leaf node tasks</span></span>

### <a name="project-root-node"></a><span data-ttu-id="59385-114">项目根节点</span><span class="sxs-lookup"><span data-stu-id="59385-114">Project root node</span></span>

<span data-ttu-id="59385-115">项目根节点是项目的顶级汇总任务。</span><span class="sxs-lookup"><span data-stu-id="59385-115">The project root node is the top-level summary task for the project.</span></span> <span data-ttu-id="59385-116">该任务下方创建所有其他项目任务。</span><span class="sxs-lookup"><span data-stu-id="59385-116">All other project tasks are created under it.</span></span> <span data-ttu-id="59385-117">根节点的名称始终设置为项目名称。</span><span class="sxs-lookup"><span data-stu-id="59385-117">The name of the root node is always set to the project name.</span></span> <span data-ttu-id="59385-118">根节点的工作量、日期和持续时间基于层次结构中其下方的值汇总。</span><span class="sxs-lookup"><span data-stu-id="59385-118">The effort, dates, and duration of the root node are summarized based on the values in the hierarchy below it.</span></span> <span data-ttu-id="59385-119">不能编辑根节点的属性。</span><span class="sxs-lookup"><span data-stu-id="59385-119">You can't edit the properties of the root node.</span></span> <span data-ttu-id="59385-120">也不能删除根节点。</span><span class="sxs-lookup"><span data-stu-id="59385-120">You also can't delete the root node.</span></span>

### <a name="summary-or-container-tasks"></a><span data-ttu-id="59385-121">摘要或容器任务</span><span class="sxs-lookup"><span data-stu-id="59385-121">Summary or container tasks</span></span> 

<span data-ttu-id="59385-122">汇总任务下是子任务或容器任务。</span><span class="sxs-lookup"><span data-stu-id="59385-122">Summary tasks have sub-tasks or container tasks under them.</span></span> <span data-ttu-id="59385-123">这些任务没有自己的工作量或成本。</span><span class="sxs-lookup"><span data-stu-id="59385-123">They have no work effort or cost of their own.</span></span> <span data-ttu-id="59385-124">相反，其工作量和成本是其容器任务的工作量和成本的汇总。</span><span class="sxs-lookup"><span data-stu-id="59385-124">Instead, their work effort and cost are a rollup of the work effort and cost of their container tasks.</span></span> <span data-ttu-id="59385-125">汇总任务的开始日期和结束日期分别是容器任务的开始日期和结束日期。</span><span class="sxs-lookup"><span data-stu-id="59385-125">The start date of the summary task is the start date of the container tasks, and the end date is the end date of the container tasks.</span></span> <span data-ttu-id="59385-126">可以编辑汇总任务的名称，但是不能编辑计划属性（工作量、日期和持续时间）。</span><span class="sxs-lookup"><span data-stu-id="59385-126">The name of a summary task can be edited, but scheduling properties (effort, dates, and duration) can't be edited.</span></span> <span data-ttu-id="59385-127">如果删除一个汇总任务，也会删除其所有容器任务。</span><span class="sxs-lookup"><span data-stu-id="59385-127">If you delete a summary task, you also delete all its container tasks.</span></span>

### <a name="leaf-node-tasks"></a><span data-ttu-id="59385-128">叶节点任务</span><span class="sxs-lookup"><span data-stu-id="59385-128">Leaf node tasks</span></span>

<span data-ttu-id="59385-129">叶节点任务表示有关项目的最详细工作。</span><span class="sxs-lookup"><span data-stu-id="59385-129">Leaf node tasks represent the most granular work on the project.</span></span> <span data-ttu-id="59385-130">它们具有估算工作量、资源、计划开始和结束日期以及持续时间。</span><span class="sxs-lookup"><span data-stu-id="59385-130">They have an estimated effort, resources, planned start and end dates, and a duration.</span></span>
 
## <a name="creating-a-task-hierarchy"></a><span data-ttu-id="59385-131">创建任务层次结构</span><span class="sxs-lookup"><span data-stu-id="59385-131">Creating a task hierarchy</span></span>

<span data-ttu-id="59385-132">可以使用以下选项创建任务层次结构：</span><span class="sxs-lookup"><span data-stu-id="59385-132">You can create a task hierarchy by using the following options:</span></span>

- <span data-ttu-id="59385-133">**添加任务** 按钮</span><span class="sxs-lookup"><span data-stu-id="59385-133">**Add task** button</span></span>
- <span data-ttu-id="59385-134">**缩进任务** 按钮</span><span class="sxs-lookup"><span data-stu-id="59385-134">**Indent task** button</span></span>
- <span data-ttu-id="59385-135">**减少缩进任务** 按钮</span><span class="sxs-lookup"><span data-stu-id="59385-135">**Outdent task** button</span></span>
- <span data-ttu-id="59385-136">**上移** 和 **下移** 按钮</span><span class="sxs-lookup"><span data-stu-id="59385-136">**Move up** and **Move down** buttons</span></span>
- <span data-ttu-id="59385-137">辅助功能和键盘快捷方式</span><span class="sxs-lookup"><span data-stu-id="59385-137">Accessibility and keyboard shortcuts</span></span>

### <a name="add-task"></a><span data-ttu-id="59385-138">添加任务</span><span class="sxs-lookup"><span data-stu-id="59385-138">Add task</span></span>

<span data-ttu-id="59385-139">**添加任务** 按钮用于在层次结构中创建新任务。</span><span class="sxs-lookup"><span data-stu-id="59385-139">The **Add task** button lets you create a new task in the hierarchy.</span></span> <span data-ttu-id="59385-140">如果您不选择位置，将把任务插在末尾。</span><span class="sxs-lookup"><span data-stu-id="59385-140">If you don't select a position, the task is inserted at the end.</span></span> 

<span data-ttu-id="59385-141">将为每个任务分派一个计划 ID。</span><span class="sxs-lookup"><span data-stu-id="59385-141">A schedule ID is assigned to every task.</span></span> <span data-ttu-id="59385-142">计划 ID 表示任务在层次结构中的深度和位置。</span><span class="sxs-lookup"><span data-stu-id="59385-142">The schedule ID represents the task's depth and position in the hierarchy.</span></span> <span data-ttu-id="59385-143">其使用大纲编号。</span><span class="sxs-lookup"><span data-stu-id="59385-143">It uses outline numbering.</span></span> <span data-ttu-id="59385-144">项目根节点下的第一级中的任务使用编号方案 1、2、3，依此类推。</span><span class="sxs-lookup"><span data-stu-id="59385-144">For tasks in the first level under the project root node, a numbering scheme of 1, 2, 3, and so on, is used.</span></span> <span data-ttu-id="59385-145">第一级下的任务使用编号方案 1.1、1.2、1.3，依此类推。</span><span class="sxs-lookup"><span data-stu-id="59385-145">For tasks under the first level, a numbering scheme of 1.1, 1.2, 1.3, and so on, is used.</span></span>

### <a name="indent-task"></a><span data-ttu-id="59385-146">缩进任务</span><span class="sxs-lookup"><span data-stu-id="59385-146">Indent task</span></span>

<span data-ttu-id="59385-147">如果缩进某个任务，该任务将成为其上任务的子级。</span><span class="sxs-lookup"><span data-stu-id="59385-147">When a task is indented, it becomes a child of the task that is directly above it.</span></span> <span data-ttu-id="59385-148">然后重新计算该任务的计划 ID，使其基于其新父级的计划 ID，并采用大纲编号方案。</span><span class="sxs-lookup"><span data-stu-id="59385-148">The schedule ID of the task is then recalculated so that it's based on the schedule ID of its new parent and follows the outline numbering scheme.</span></span> <span data-ttu-id="59385-149">父任务现在成为汇总任务或容器任务。</span><span class="sxs-lookup"><span data-stu-id="59385-149">The parent task is now a summary task or a container task.</span></span> <span data-ttu-id="59385-150">因此，成为其子任务的汇总。</span><span class="sxs-lookup"><span data-stu-id="59385-150">Therefore, it becomes a rollup of its child tasks.</span></span>

### <a name="outdent-task"></a><span data-ttu-id="59385-151">减少缩进任务</span><span class="sxs-lookup"><span data-stu-id="59385-151">Outdent task</span></span> 

<span data-ttu-id="59385-152">减少缩进某个任务后，该任务不再是原父级任务的子级。</span><span class="sxs-lookup"><span data-stu-id="59385-152">When a task is outdented, it's no longer a child of the task that was its parent.</span></span> <span data-ttu-id="59385-153">然后重新计算计划 ID，以便体现该任务在层次结构中更新后的深度和位置。</span><span class="sxs-lookup"><span data-stu-id="59385-153">The schedule ID is then recalculated so that it reflects the task's updated depth and position in the hierarchy.</span></span> <span data-ttu-id="59385-154">将重新计算原父任务的工作量、成本和日期，以便其不包含此任务。</span><span class="sxs-lookup"><span data-stu-id="59385-154">The effort, cost, and dates of the previous parent task are recalculated so that they don't include this task.</span></span>

### <a name="move-up-and-move-down"></a><span data-ttu-id="59385-155">上移和下移</span><span class="sxs-lookup"><span data-stu-id="59385-155">Move up and Move down</span></span> 

<span data-ttu-id="59385-156">**上移** 和 **下移** 按钮用于更改任务在其父层次结构中的位置。</span><span class="sxs-lookup"><span data-stu-id="59385-156">The **Move up** and **Move down** buttons change the position of a task within its parent hierarchy.</span></span> <span data-ttu-id="59385-157">更改此类型不会影响任务的工作量、成本、日期或持续时间。</span><span class="sxs-lookup"><span data-stu-id="59385-157">Changes of this type don't affect the task's effort, cost, dates, or duration.</span></span> <span data-ttu-id="59385-158">只会影响任务的计划 ID。</span><span class="sxs-lookup"><span data-stu-id="59385-158">Only the task's schedule ID is affected.</span></span> <span data-ttu-id="59385-159">将重新计算计划 ID，以便体现该任务在父级的子任务列表中的新位置。</span><span class="sxs-lookup"><span data-stu-id="59385-159">The schedule ID is recalculated so that it reflects the task's new position in the parent's list of child tasks.</span></span>

### <a name="accessibility-and-keyboard-shortcuts"></a><span data-ttu-id="59385-160">辅助功能和键盘快捷方式</span><span class="sxs-lookup"><span data-stu-id="59385-160">Accessibility and keyboard shortcuts</span></span>

<span data-ttu-id="59385-161">**计划** 网格拥有完善的辅助功能，可以与讲述人、JAWS 或 NVDA 之类屏幕阅读器配合使用。</span><span class="sxs-lookup"><span data-stu-id="59385-161">The **Schedule** grid is fully accessible and can be used with screen readers such as Narrator, JAWS, or NVDA.</span></span> <span data-ttu-id="59385-162">可使用箭头键在网格区域中移动（和在 Microsoft Excel 中一样），可以使用 Tab 键在交互式 UI 元素中前进，还可以使用向下键、Enter 将或空格键选择和调用下拉菜单。</span><span class="sxs-lookup"><span data-stu-id="59385-162">You can move through the grid area by using arrow keys (as in Microsoft Excel), you can use the Tab key to advance through the interactive UI elements, and you can use the Down arrow key, the Enter key, or the Spacebar to select and invoke the drop-down menus.</span></span> <span data-ttu-id="59385-163">列标题也支持交互。</span><span class="sxs-lookup"><span data-stu-id="59385-163">The column headers are also interactive.</span></span> <span data-ttu-id="59385-164">可使用 Tab 键和箭头键隐藏和显示列，一遍浏览列标题，也可以使用工具栏中的操作按钮。</span><span class="sxs-lookup"><span data-stu-id="59385-164">You can hide and show columns, use the Tab key and arrow keys to move through the column headers, and use the action buttons on the toolbar.</span></span> <span data-ttu-id="59385-165">此外，还可以使用以下键盘快捷键：</span><span class="sxs-lookup"><span data-stu-id="59385-165">In addition, you can use the following keyboard shortcuts:</span></span>

- <span data-ttu-id="59385-166">**刷新**：ALT+SHIFT+F5</span><span class="sxs-lookup"><span data-stu-id="59385-166">**Refresh**: ALT+SHIFT+F5</span></span>
- <span data-ttu-id="59385-167">**添加**：ALT+SHIFT+Insert</span><span class="sxs-lookup"><span data-stu-id="59385-167">**Add**: ALT+SHIFT+Insert</span></span>
- <span data-ttu-id="59385-168">**删除**：ALT+SHIFT+Delete</span><span class="sxs-lookup"><span data-stu-id="59385-168">**Delete**: ALT+SHIFT+Delete</span></span>
- <span data-ttu-id="59385-169">**上移/下移**：ALT+SHIFT+向上键/向下键</span><span class="sxs-lookup"><span data-stu-id="59385-169">**Move up/down**: ALT+SHIFT+Up/Down arrows</span></span>
- <span data-ttu-id="59385-170">**缩减/减少缩进** Down arrowsALT_SHIFT+向左键/向右键</span><span class="sxs-lookup"><span data-stu-id="59385-170">**Indent/Outdent**: ALT_SHIFT+Left/Right arrows</span></span>
- <span data-ttu-id="59385-171">**展开/折叠层次结构** Down arrowsALT+SHIFT+加号键/减号键</span><span class="sxs-lookup"><span data-stu-id="59385-171">**Expand/Collapse Hierarchies**: ALT+SHIFT+Plus/Minus keys</span></span>

## <a name="task-attributes"></a><span data-ttu-id="59385-172">任务属性</span><span class="sxs-lookup"><span data-stu-id="59385-172">Task attributes</span></span>

<span data-ttu-id="59385-173">任务的名称描述必须完成的工作。</span><span class="sxs-lookup"><span data-stu-id="59385-173">A task's name describes the work that must be completed.</span></span> <span data-ttu-id="59385-174">在 PSA 中，与任务关联的属性描述任务的计划及其人员配备要求。</span><span class="sxs-lookup"><span data-stu-id="59385-174">In PSA, the attributes that are associated with a task describe the schedule of the task and its staffing requirements.</span></span>

> ![任务属性](media/project-2.png)
 
### <a name="schedule-attributes"></a><span data-ttu-id="59385-176">计划属性</span><span class="sxs-lookup"><span data-stu-id="59385-176">Schedule attributes</span></span>

<span data-ttu-id="59385-177">**工作量**、**开始日期**、**结束日期** 和 **持续时间** 属性定义任务的计划。</span><span class="sxs-lookup"><span data-stu-id="59385-177">The **Effort**, **Start date**, **End date**, and **Duration** attributes define the schedule for the task.</span></span>

<span data-ttu-id="59385-178">其他计划属性包括：</span><span class="sxs-lookup"><span data-stu-id="59385-178">Additional schedule attributes include:</span></span>

- <span data-ttu-id="59385-179">**工作量时数**：输入完成任务所需工时数估算。</span><span class="sxs-lookup"><span data-stu-id="59385-179">**Effort hours**: Enter an estimate of the hours that are required to complete the task.</span></span> 
- <span data-ttu-id="59385-180">**持续时间**：指定完成任务所需工作日天数。</span><span class="sxs-lookup"><span data-stu-id="59385-180">**Duration**: Specify the number of workdays that are required to complete the task.</span></span>
- <span data-ttu-id="59385-181">**计划 ID**：这个自动生成的 ID 用于为任务在层次结构中排序。</span><span class="sxs-lookup"><span data-stu-id="59385-181">**Schedule ID**: This automatically generated ID is used to order tasks in the hierarchy.</span></span> <span data-ttu-id="59385-182">任务之间的依赖关系管理任务的实际执行顺序。</span><span class="sxs-lookup"><span data-stu-id="59385-182">Dependencies between the tasks manage the actual order in which the tasks are worked on.</span></span>
 
### <a name="staffing-attributes"></a><span data-ttu-id="59385-183">人员配备属性</span><span class="sxs-lookup"><span data-stu-id="59385-183">Staffing attributes</span></span>

<span data-ttu-id="59385-184">人员配备属性通过计划中的 **资源** 字段访问。</span><span class="sxs-lookup"><span data-stu-id="59385-184">Staffing attributes are accessed through the **Resources** field in the schedule.</span></span> <span data-ttu-id="59385-185">可搜索现有资源，或单击 **创建**，然后在 **快速创建** 窗格中把项目团队成员作为新资源添加。</span><span class="sxs-lookup"><span data-stu-id="59385-185">You can either search for an existing resource, or click **Create** and in the **Quick Create** pane, add a project team member as a new resource.</span></span>

<span data-ttu-id="59385-186">**角色**、**资源单位** 和 **位置名称** 字段用于描述任务的人员配备要求。</span><span class="sxs-lookup"><span data-stu-id="59385-186">The **Role**, **Resourcing Unit**, and **Position Name** fields are used to describe the staffing requirements for the task.</span></span> <span data-ttu-id="59385-187">这些人员配备属性与任务计划一起用于查找可用于完成此任务的资源。</span><span class="sxs-lookup"><span data-stu-id="59385-187">These staffing attributes together with the task schedule are used to find available resources to do this task.</span></span>

<span data-ttu-id="59385-188">**角色** - 指定完成任务所需资源类型。</span><span class="sxs-lookup"><span data-stu-id="59385-188">**Role** - Specify the type of resource that is required to do the task.</span></span>

<span data-ttu-id="59385-189">**资源单位** - 指定应该为分派的资源所属单位。</span><span class="sxs-lookup"><span data-stu-id="59385-189">**Resourcing unit** - Specify the unit that resources for the task should be assigned from.</span></span> <span data-ttu-id="59385-190">如果资源的成本和记帐费率是基于资源单位设置的，则此属性会影响任务的成本和销售额估算。</span><span class="sxs-lookup"><span data-stu-id="59385-190">This attribute affects the cost and sales estimate for the task if the cost and bill rate for the resource are set based on resourcing units.</span></span>

<span data-ttu-id="59385-191">**职位名称** – 为充当最终将执行工作的资源的占位符的通用资源输入友好名称。</span><span class="sxs-lookup"><span data-stu-id="59385-191">**Position name** – Enter a friendly name for the generic resource that serves as a placeholder for the resource that will ultimately do the work.</span></span>

<span data-ttu-id="59385-192">**资源** 字段存储通用资源或指定资源被发现时的位置名称。</span><span class="sxs-lookup"><span data-stu-id="59385-192">The **Resources** field holds the position name of the generic resource or named resource when one is found.</span></span>

<span data-ttu-id="59385-193">**类别** 字段存储指示可将任务归入的更广泛工作类型的值。</span><span class="sxs-lookup"><span data-stu-id="59385-193">The **Category** field holds the values that indicate a broader type of work that the task can be grouped into.</span></span> <span data-ttu-id="59385-194">此字段不影响计划或人员配备。</span><span class="sxs-lookup"><span data-stu-id="59385-194">This field doesn't affect scheduling or staffing.</span></span> <span data-ttu-id="59385-195">仅用于报告。</span><span class="sxs-lookup"><span data-stu-id="59385-195">It's used only for reporting.</span></span>

### <a name="task-dependencies"></a><span data-ttu-id="59385-196">任务依赖关系</span><span class="sxs-lookup"><span data-stu-id="59385-196">Task dependencies</span></span> 

<span data-ttu-id="59385-197">在 PSA 中，可使用计划创建任务之间的前置关系。</span><span class="sxs-lookup"><span data-stu-id="59385-197">You can use the schedule in PSA to create predecessor relationships between tasks.</span></span> <span data-ttu-id="59385-198">**任务** 下的 **前置任务** 字段采用一个或多个值来指示任务的依赖任务。</span><span class="sxs-lookup"><span data-stu-id="59385-198">The **Predecessor** field under **Tasks** takes one or more values to indicate the tasks that a task depends on.</span></span> <span data-ttu-id="59385-199">当您向任务分派前置任务值时，该任务仅在所有前置任务都已完成时才能启动。</span><span class="sxs-lookup"><span data-stu-id="59385-199">When predecessor values are assigned to a task, the task can start only after all the predecessor tasks have been completed.</span></span> <span data-ttu-id="59385-200">由于依赖关系，任务的计划开始日期将重置为前置任务的完成日期。</span><span class="sxs-lookup"><span data-stu-id="59385-200">Because of the dependency, the planned start date of the task is reset to the date when the predecessor tasks are completed.</span></span>

<span data-ttu-id="59385-201">任务模式不影响对前置/依赖任务的开始日期和结束日期进行的更新。</span><span class="sxs-lookup"><span data-stu-id="59385-201">The task mode has no effect on updates that are made to the start and end dates of predecessor/dependent tasks.</span></span>

## <a name="task-mode"></a><span data-ttu-id="59385-202">任务模式</span><span class="sxs-lookup"><span data-stu-id="59385-202">Task mode</span></span> 

<span data-ttu-id="59385-203">任务模式决定叶节点任务的计划。</span><span class="sxs-lookup"><span data-stu-id="59385-203">The task mode determines the scheduling of leaf node tasks.</span></span> <span data-ttu-id="59385-204">PSA 每项任务有两个任务模式：自动计划模式和手动计划模式。</span><span class="sxs-lookup"><span data-stu-id="59385-204">PSA supports two task modes for every task: automatic scheduling and manual scheduling.</span></span>

### <a name="auto-scheduling"></a><span data-ttu-id="59385-205">自动计划</span><span class="sxs-lookup"><span data-stu-id="59385-205">Auto-scheduling</span></span> 
 
<span data-ttu-id="59385-206">如果任务的任务模式设置为 **自动计划**，任务计划引擎将使用有关任务属性的计划规则来确定任务的计划。</span><span class="sxs-lookup"><span data-stu-id="59385-206">When task mode is set to **Automatically Scheduled** for a task, the task scheduling engine uses the scheduling rules on task attributes to determine the schedule for the task.</span></span>

#### <a name="scheduling-rules"></a><span data-ttu-id="59385-207">计划规则</span><span class="sxs-lookup"><span data-stu-id="59385-207">Scheduling rules</span></span>

<span data-ttu-id="59385-208">默认情况下，如果某个叶节点任务没有前置任务，则其开始日期设置为项目的计划开始日期。</span><span class="sxs-lookup"><span data-stu-id="59385-208">By default, if a leaf node task doesn't have predecessors, its start date is set to the project's scheduled start date.</span></span> <span data-ttu-id="59385-209">叶节点任务的持续时间总是计算为其开始日期与结束日期之间的工作日数。</span><span class="sxs-lookup"><span data-stu-id="59385-209">The duration of a leaf node task is always calculated as the number of working days between its start and end dates.</span></span> <span data-ttu-id="59385-210">当任务自动计划时，计划引擎遵守如下规则：</span><span class="sxs-lookup"><span data-stu-id="59385-210">When a task is automatically scheduled, the scheduling engine follows these rules:</span></span>

- <span data-ttu-id="59385-211">任务的开始和结束日期必须为符合项目计划日历的工作日。</span><span class="sxs-lookup"><span data-stu-id="59385-211">The start and end dates of the task must be working days, according to the project's scheduling calendar.</span></span> 
- <span data-ttu-id="59385-212">对于具有前置任务的任何任务，将把开始日期自动设置为其前置任务的最近结束日期。</span><span class="sxs-lookup"><span data-stu-id="59385-212">For any task that has predecessor tasks, the start date is automatically set to the latest end date of its predecessors.</span></span>
- <span data-ttu-id="59385-213">工作量使用以下公式计算：人数 × 持续时间 × 项目日历中标准工作日的小时数</span><span class="sxs-lookup"><span data-stu-id="59385-213">Effort is calculated by using this formula: Number of people × Duration × Hours in a standard workday in the project calendar.</span></span>

### <a name="manual-scheduling"></a><span data-ttu-id="59385-214">手动计划</span><span class="sxs-lookup"><span data-stu-id="59385-214">Manual scheduling</span></span>

<span data-ttu-id="59385-215">如果自动计划规则无法满足您的要求，您可以将任务的任务模式设置为 **手动计划**。</span><span class="sxs-lookup"><span data-stu-id="59385-215">If the rules of automatic scheduling don't meet your requirements, you can set the task mode for the task to **Manually Scheduled**.</span></span> <span data-ttu-id="59385-216">此设置会阻止计划引擎计算其他计划属性的值。</span><span class="sxs-lookup"><span data-stu-id="59385-216">This setting stops the scheduling engine from calculating the values of other scheduling attributes.</span></span> <span data-ttu-id="59385-217">无论采用哪种任务模式，如果为任务设置前置任务，始终会影响依赖任务的开始日期。</span><span class="sxs-lookup"><span data-stu-id="59385-217">Regardless of the task mode, if you set predecessors on tasks, you always affect the dependent task's start date.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]