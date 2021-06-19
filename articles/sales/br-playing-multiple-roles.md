---
title: 当可预订资源在项目中担任多个角色时，估计项目销售和成本
description: 本主题说明如何使用定价维度来支持在项目中担任多个角色的资源的定价和成本估算。
author: rumant
ms.date: 11/16/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 7ef9765b7db1c6650fb0599bf5fb4b4b6304be69
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/10/2021
ms.locfileid: "6013655"
---
# <a name="estimate-project-sales-and-costs-when-a-bookable-resource-fills-multiple-roles-on-a-project"></a><span data-ttu-id="2c71a-103">当可预订资源在项目中担任多个角色时，估计项目销售和成本</span><span class="sxs-lookup"><span data-stu-id="2c71a-103">Estimate project sales and costs when a bookable resource fills multiple roles on a project</span></span> 

<span data-ttu-id="2c71a-104">_**适用范围：** 面向资源/非库存场景的 Project Operations，精简部署 - 估价交易开票，面向库存/生产订单场景的 Project Operations_</span><span class="sxs-lookup"><span data-stu-id="2c71a-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing, Project Operations for stocked/production-based scenarios_</span></span> 

<span data-ttu-id="2c71a-105">基于项目的公司通常需要一个资源来担任项目的多个角色。</span><span class="sxs-lookup"><span data-stu-id="2c71a-105">Project-based companies often have the need for one resource to fill multiple roles on a project.</span></span> <span data-ttu-id="2c71a-106">每个角色的定价和成本可以不同。</span><span class="sxs-lookup"><span data-stu-id="2c71a-106">Each role can be priced and costed differently.</span></span> <span data-ttu-id="2c71a-107">这意味着，根据每个角色的记帐费率和成本费率，相同资源在项目上花费的时间可能会获得不同的财务估算。</span><span class="sxs-lookup"><span data-stu-id="2c71a-107">This means that the same resource's time on a project could get a different financial estimate depending on the bill and cost rates for each role.</span></span> <span data-ttu-id="2c71a-108">对于为团队成员分派的每项任务，您可以使用不同的替代值在团队成员记录上为指定资源设置值。</span><span class="sxs-lookup"><span data-stu-id="2c71a-108">You can set up the values on the team member record for the named resource with different overrides on each of the tasks that the team member is assigned to.</span></span>

<span data-ttu-id="2c71a-109">下面的示例向您介绍简单的值替代如何允许资源在项目中具有成本费率和帐单费率不同的多个角色。</span><span class="sxs-lookup"><span data-stu-id="2c71a-109">The following example walks you through how the simple override of a value allows a resource to have multiple roles on a project with different cost and bill rates.</span></span>

## <a name="create-tasks"></a><span data-ttu-id="2c71a-110">创建任务</span><span class="sxs-lookup"><span data-stu-id="2c71a-110">Create tasks</span></span>
<span data-ttu-id="2c71a-111">若要创建任务，需要添加任务以及摘要任务，之后需要在添加任务持续时间之前分派任务。</span><span class="sxs-lookup"><span data-stu-id="2c71a-111">To create tasks, you need to add tasks, as well as summary tasks, after which you need to assign the task before you add task duration.</span></span> 

### <a name="add-tasks-and-summary-tasks"></a><span data-ttu-id="2c71a-112">添加任务和摘要任务</span><span class="sxs-lookup"><span data-stu-id="2c71a-112">Add tasks and summary tasks</span></span>
<span data-ttu-id="2c71a-113">要添加任务，请完成以下步骤。</span><span class="sxs-lookup"><span data-stu-id="2c71a-113">To add a task, complete the following steps.</span></span>

1. <span data-ttu-id="2c71a-114">转到 **项目** 并打开要向其添加任务的项目。</span><span class="sxs-lookup"><span data-stu-id="2c71a-114">Go to **Projects** and open the project to which you want to add tasks.</span></span>
2. <span data-ttu-id="2c71a-115">选择 **添加新任务**。</span><span class="sxs-lookup"><span data-stu-id="2c71a-115">Select **Add new task**.</span></span> <span data-ttu-id="2c71a-116">命名任务，然后按 **Enter**。</span><span class="sxs-lookup"><span data-stu-id="2c71a-116">Name the task, and then press **Enter**.</span></span>
3. <span data-ttu-id="2c71a-117">输入另一个任务名称，然后按 **Enter**。</span><span class="sxs-lookup"><span data-stu-id="2c71a-117">Enter another task name and press **Enter**.</span></span> <span data-ttu-id="2c71a-118">重复此操作，直到您拥有完整的任务列表。</span><span class="sxs-lookup"><span data-stu-id="2c71a-118">Repeat this until you have a full list of tasks.</span></span>
3. <span data-ttu-id="2c71a-119">若要在 **摘要任务** 下缩进任务，请选择任务名称旁边的三个垂直点，然后选择 **设为子任务**。</span><span class="sxs-lookup"><span data-stu-id="2c71a-119">To indent tasks under **Summary** tasks, select the three vertical dots by the task name, and then select **Make subtask**.</span></span> 

  > [!TIP]
  > <span data-ttu-id="2c71a-120">要选择多个任务，请选择任务，请按住 **Ctrl**，然后选择另一个任务。</span><span class="sxs-lookup"><span data-stu-id="2c71a-120">To select more than one task, select a task, press and hold **Ctrl**, and then select another task.</span></span>
  >
  > <span data-ttu-id="2c71a-121">您还可以选择 **提升子任务**，以从 **摘要** 任务下面移出任务。</span><span class="sxs-lookup"><span data-stu-id="2c71a-121">You can also choose **Promote subtask** to move tasks out from under **Summary** tasks.</span></span>

### <a name="assign-tasks"></a><span data-ttu-id="2c71a-122">分派任务</span><span class="sxs-lookup"><span data-stu-id="2c71a-122">Assign tasks</span></span>

<span data-ttu-id="2c71a-123">要分派任务，请完成以下步骤。</span><span class="sxs-lookup"><span data-stu-id="2c71a-123">Complete the following steps to assign tasks.</span></span>

1. <span data-ttu-id="2c71a-124">在任务的 **分配到** 列中，选择人员图标。</span><span class="sxs-lookup"><span data-stu-id="2c71a-124">In the  **Assigned to**  column for a task, select the person icon.</span></span>
2. <span data-ttu-id="2c71a-125">从列表中选择一个团队成员，或输入文本来搜索姓名。</span><span class="sxs-lookup"><span data-stu-id="2c71a-125">Choose a team member from the list or enter text to search for a name.</span></span>

### <a name="add-task-duration-and-columns"></a><span data-ttu-id="2c71a-126">添加任务持续时间和列</span><span class="sxs-lookup"><span data-stu-id="2c71a-126">Add task duration and columns</span></span>

<span data-ttu-id="2c71a-127">通常开始构建具有持续时间的项目最容易。</span><span class="sxs-lookup"><span data-stu-id="2c71a-127">It's often easiest to begin constructing your project with duration.</span></span> <span data-ttu-id="2c71a-128">要添加任务持续时间，请完成以下步骤。</span><span class="sxs-lookup"><span data-stu-id="2c71a-128">Complete the following steps to add a task duration.</span></span>

1. <span data-ttu-id="2c71a-129">在任务的 **持续时间** 列中，键入您认为完成任务所需的天数。</span><span class="sxs-lookup"><span data-stu-id="2c71a-129">In the **Duration** column for a task, type the number of days you think it will take to accomplish the task.</span></span> <span data-ttu-id="2c71a-130">如果要使用不同的时间单位，请输入一个数字加上字词 **小时**、**周** 或 **月**。</span><span class="sxs-lookup"><span data-stu-id="2c71a-130">If you want to use a different unit of time, enter a number plus the word **hours**, **weeks**, or **months**.</span></span>
2. <span data-ttu-id="2c71a-131">如果希望任务在 **时间轴** 视图中显示为菱形里程碑，请在 **持续时间** 列中输入 **0 天**。</span><span class="sxs-lookup"><span data-stu-id="2c71a-131">If you want your task to appear as a diamond-shaped milestone in the **Timeline** view, in the **Duration** column, enter **0 days** .</span></span>
3. <span data-ttu-id="2c71a-132">按 **Enter** 转到下一个任务的 **持续时间** 字段并继续输入持续时间。</span><span class="sxs-lookup"><span data-stu-id="2c71a-132">Press **Enter**  to go to the next task's **Duration** field and continue entering durations.</span></span>

  > [!NOTE]
  > <span data-ttu-id="2c71a-133">不能输入摘要任务的持续时间。</span><span class="sxs-lookup"><span data-stu-id="2c71a-133">You can't enter a duration for summary tasks.</span></span>

<span data-ttu-id="2c71a-134">您可以向项目添加列以提供更多详细信息。</span><span class="sxs-lookup"><span data-stu-id="2c71a-134">You can add columns to your project to provide more details.</span></span> <span data-ttu-id="2c71a-135">为此，请选择 **添加列**。</span><span class="sxs-lookup"><span data-stu-id="2c71a-135">To do this, select **Add column**.</span></span> 

<span data-ttu-id="2c71a-136">有关详细信息，请参阅[创建项目](https://support.microsoft.com/en-us/office/create-a-project-a5b5e823-fb2e-45fd-be00-7d84422d9749)。</span><span class="sxs-lookup"><span data-stu-id="2c71a-136">For more information, see [Create a project](https://support.microsoft.com/en-us/office/create-a-project-a5b5e823-fb2e-45fd-be00-7d84422d9749).</span></span>

## <a name="set-up-the-role-and-organization-unit-for-a-generic-project-team-member"></a><span data-ttu-id="2c71a-137">为一般项目团队成员设置角色和部门</span><span class="sxs-lookup"><span data-stu-id="2c71a-137">Set up the role and organization unit for a generic project team member</span></span>
<span data-ttu-id="2c71a-138">完成以下步骤，为一般团队成员设置角色和部门。</span><span class="sxs-lookup"><span data-stu-id="2c71a-138">Complete the following steps to set up a role and organizational unit for a generic team member.</span></span>

1. <span data-ttu-id="2c71a-139">在 **任务** 页上，为 **任务 A** 选择 **任务** 行。</span><span class="sxs-lookup"><span data-stu-id="2c71a-139">On the **Tasks** page, select the **Task** row for **Task A**.</span></span> 
2. <span data-ttu-id="2c71a-140">在 **分配到** 中，选择 **添加通用资源**。</span><span class="sxs-lookup"><span data-stu-id="2c71a-140">In **Assigned To**, select **Add generic resource**.</span></span> <span data-ttu-id="2c71a-141">这将打开 **团队成员快速创建** 页面。</span><span class="sxs-lookup"><span data-stu-id="2c71a-141">This opens the **Team Member Quick Create** page.</span></span>
3. <span data-ttu-id="2c71a-142">在 **团队成员快速创建** 页上，指定可执行此任务的通用团队成员的属性。</span><span class="sxs-lookup"><span data-stu-id="2c71a-142">On the **Team Member Quick Create** page, specify the attributes of the generic team member who can perform this task.</span></span>
4. <span data-ttu-id="2c71a-143">选择相应的角色和部门，然后选择 **保存并关闭**。</span><span class="sxs-lookup"><span data-stu-id="2c71a-143">Select the appropriate role and organizational unit, and then select **Save and Close**.</span></span> <span data-ttu-id="2c71a-144">将创建一个通用团队成员，并将其分配给此任务。</span><span class="sxs-lookup"><span data-stu-id="2c71a-144">A generic team member is created and assigned to this task.</span></span> 
5. <span data-ttu-id="2c71a-145">对 **任务 B** 重复步骤 1-4。但是，对于 **任务 B**，为一般团队成员分配的角色和部门不得与 **任务 A** 中所分配的角色和部门相同。</span><span class="sxs-lookup"><span data-stu-id="2c71a-145">Repeat steps 1-4 for **Task B**. However, **Task B** must have a different role and organizational unit assigned for the generic team member than **Task A**.</span></span> 

## <a name="set-up-the-role-and-organization-unit-for-a-project-task"></a><span data-ttu-id="2c71a-146">为项目任务设置角色和部门</span><span class="sxs-lookup"><span data-stu-id="2c71a-146">Set up the role and organization unit for a project task</span></span>
<span data-ttu-id="2c71a-147">完成以下步骤，为任务设置角色和部门。</span><span class="sxs-lookup"><span data-stu-id="2c71a-147">Complete the following steps to set up a role and organizational unit for a task.</span></span>

1. <span data-ttu-id="2c71a-148">创建 **任务 A** 后，选择此任务，然后选择 **i** 图标打开 **任务详细信息** 窗格。</span><span class="sxs-lookup"><span data-stu-id="2c71a-148">After you create **Task A**, select the task, and then select the **i** icon to open the **Task Details** pane.</span></span> 
2. <span data-ttu-id="2c71a-149">在 **任务详细信息** 窗格上，滚动到底部并选择 **查看详细信息**，以打开 **任务详细信息** 页。</span><span class="sxs-lookup"><span data-stu-id="2c71a-149">On the **Task Details** pane, scroll to the bottom and select **View Details** to open the **Task Details** page.</span></span>
3. <span data-ttu-id="2c71a-150">在 **任务详细信息** 页上的 **角色** 和 **部门** 中，添加为资源执行此任务所需的值。</span><span class="sxs-lookup"><span data-stu-id="2c71a-150">On the **Task Details** page, in **Role** and **Organizational Unit**, add the values that are required to perform this task for the resource.</span></span> 

  > [!NOTE]
  > <span data-ttu-id="2c71a-151">如果使用 Project Operations 演示数据完成此方案，请为角色选择 **咨询负责人**，并选择 **Fabrikam US** 作为部门。</span><span class="sxs-lookup"><span data-stu-id="2c71a-151">If you complete this scenario using the Project Operations demo data, select **Consulting Lead** for the role, and **Fabrikam US** as the organizational unit.</span></span>

4. <span data-ttu-id="2c71a-152">选择 **任务 B**，然后选择此任务。</span><span class="sxs-lookup"><span data-stu-id="2c71a-152">Select **Task B**, and then select the task.</span></span>
5. <span data-ttu-id="2c71a-153">选择 **i** 图标以打开 **任务详细信息** 窗格。</span><span class="sxs-lookup"><span data-stu-id="2c71a-153">Select the **i** icon to open **Task Details** pane.</span></span> 
6. <span data-ttu-id="2c71a-154">在 **任务详细信息** 窗格上，滚动到底部并选择 **查看详细信息**，以打开 **任务详细信息** 页。</span><span class="sxs-lookup"><span data-stu-id="2c71a-154">On the **Task Details** pane, scroll to the bottom and select **View details** to open the **Task Details** page.</span></span>
7. <span data-ttu-id="2c71a-155">在 **任务详细信息** 页上的 **角色** 和 **部门** 中，添加将执行此任务的资源所需的值。</span><span class="sxs-lookup"><span data-stu-id="2c71a-155">On the **Task Details** page, in **Role** and **Organizational Unit**, add the values that are required of a resource that would perform this task.</span></span> <span data-ttu-id="2c71a-156">**任务 B** 的 **角色** 和 **部门** 中的值必须与 **任务 A** 的那些相应值不同。</span><span class="sxs-lookup"><span data-stu-id="2c71a-156">The values in **Role** and **Organizational Unit** for **Task B** must be different than those for **Task A**.</span></span> 

  > [!NOTE]
  > <span data-ttu-id="2c71a-157">如果使用 Project Operations 演示数据完成此方案，请为角色选择 **网络技术人员**，并选择 **Fabrikam US** 作为部门。</span><span class="sxs-lookup"><span data-stu-id="2c71a-157">If you complete this scenario using the Project Operations demo data, select **Network Technician** for the role, and **Fabrikam US** as the organizational unit.</span></span>

8. <span data-ttu-id="2c71a-158">保存并关闭 **任务详细信息** 页。</span><span class="sxs-lookup"><span data-stu-id="2c71a-158">Save and close the **Task Details** page.</span></span> 

## <a name="team-member-and-estimates-behavior"></a><span data-ttu-id="2c71a-159">团队成员和估计行为</span><span class="sxs-lookup"><span data-stu-id="2c71a-159">Team member and estimates behavior</span></span> 
<span data-ttu-id="2c71a-160">若要了解 **团队成员** 网格上的行为和估计值，请完成以下步骤。</span><span class="sxs-lookup"><span data-stu-id="2c71a-160">To understand the behavior on the **Team Member** grid and the estimates, complete the following steps.</span></span>

1. <span data-ttu-id="2c71a-161">在 **团队成员** 网格上，选择两个一般团队成员，然后选择 **生成要求**。</span><span class="sxs-lookup"><span data-stu-id="2c71a-161">On the **Team Member** grid, select the two generic team members, and then select **Generate Requirements**.</span></span> <span data-ttu-id="2c71a-162">这将生成资源要求。</span><span class="sxs-lookup"><span data-stu-id="2c71a-162">This will generate resource requirements.</span></span> 
2. <span data-ttu-id="2c71a-163">选择 **咨询负责人** 的团队成员行，然后选择 **预订**。</span><span class="sxs-lookup"><span data-stu-id="2c71a-163">Select the team member row for **Consulting Lead**, and then select **Book**.</span></span> <span data-ttu-id="2c71a-164">日程安排板将打开，并列出资源。</span><span class="sxs-lookup"><span data-stu-id="2c71a-164">The schedule board opens with a list of resources.</span></span> <span data-ttu-id="2c71a-165">选择资源，然后选择 **预订** 以按该要求预订此资源。</span><span class="sxs-lookup"><span data-stu-id="2c71a-165">Select a resource and then select **Book** to book the resource to that requirement.</span></span>
3. <span data-ttu-id="2c71a-166">选择 **网络技术人员** 的团队成员行，然后选择 **预订**。</span><span class="sxs-lookup"><span data-stu-id="2c71a-166">Select the team member row for **Network Technician**, and then select **Book**.</span></span> <span data-ttu-id="2c71a-167">日程安排板将打开，并列出资源。</span><span class="sxs-lookup"><span data-stu-id="2c71a-167">The schedule board opens with a list of resources.</span></span> <span data-ttu-id="2c71a-168">选择以上相同资源，然后选择 **预订** 以按该要求预订此资源。</span><span class="sxs-lookup"><span data-stu-id="2c71a-168">Select the same resource as above and then select **Book** to book the resource to that requirement.</span></span>

### <a name="team-member-grid"></a><span data-ttu-id="2c71a-169">团队成员网格</span><span class="sxs-lookup"><span data-stu-id="2c71a-169">Team Member grid</span></span> 

<span data-ttu-id="2c71a-170">在 **团队成员** 网格上，将删除这两个一般团队成员记录，并仅替换为一个资源。</span><span class="sxs-lookup"><span data-stu-id="2c71a-170">On the **Team Member** grid, the two generic team member records are deleted and replaced with only one resource.</span></span> <span data-ttu-id="2c71a-171">该资源有一组值，这组值是 **角色** 和 **部门** 的默认值集。</span><span class="sxs-lookup"><span data-stu-id="2c71a-171">There is one set of values for that resource, which are a default set of values for **Role** and **Organizational Unit**.</span></span>

<span data-ttu-id="2c71a-172">展开该团队成员记录的行时，可以在两个任务的团队成员记录上看到不同的工作。</span><span class="sxs-lookup"><span data-stu-id="2c71a-172">When you expand the row for that team member record, you can see distinct assignments on the team member record for both tasks.</span></span> <span data-ttu-id="2c71a-173">每个工作行都具有任务特定的 **角色** 和 **部门** 值。</span><span class="sxs-lookup"><span data-stu-id="2c71a-173">Each assignment row has task-specific values for **Role** and **Organizational Unit**.</span></span> 

### <a name="estimates-grid"></a><span data-ttu-id="2c71a-174">估算网格</span><span class="sxs-lookup"><span data-stu-id="2c71a-174">Estimates grid</span></span> 

<span data-ttu-id="2c71a-175">在 **估计** 网格上，同一资源的两个工作的定价不同。</span><span class="sxs-lookup"><span data-stu-id="2c71a-175">On the **Estimates** grid, both assignments for the same resource are priced differently.</span></span> <span data-ttu-id="2c71a-176">**任务 A** 中的资源的工作使用 **咨询负责人** 的 **角色** 属性值定价。</span><span class="sxs-lookup"><span data-stu-id="2c71a-176">The assignment for the resource on **Task A** is priced using the **Role** attribute value of **Consulting Lead**.</span></span> <span data-ttu-id="2c71a-177">**任务 B** 中的同一个资源的工作使用 **网络技术人员** 的 **角色** 属性值定价。</span><span class="sxs-lookup"><span data-stu-id="2c71a-177">The assignment for the same resource on **Task B** is priced using the **Role** attribute value of **Network Technician**.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]