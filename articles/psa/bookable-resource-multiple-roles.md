---
title: 估算当可预订资源在项目中担任多个角色时项目的销售额和成本
description: 此主题提供有关如何使用定价维度来支持在项目中担任多个角色的资源的定价和成本核算的信息。
author: rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 10/01/2020
ms.topic: article
ms.service: business-applications
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: 8ddc827a4170c5576c0a4350b51e6a119094ac50
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/16/2020
ms.locfileid: "4072656"
---
# <a name="estimate-project-sales-and-costs-when-a-bookable-resource-fills-mulitple-roles-on-a-project"></a><span data-ttu-id="08330-103">估算当可预订资源在项目中担任多个角色时项目的销售额和成本</span><span class="sxs-lookup"><span data-stu-id="08330-103">Estimate project sales and costs when a bookable resource fills mulitple roles on a project</span></span> 

<span data-ttu-id="08330-104">基于项目的公司通常需要一个资源在项目中执行多个角色。</span><span class="sxs-lookup"><span data-stu-id="08330-104">Project-based companies often have the need for one resource to perform mulitple roles on a project.</span></span> <span data-ttu-id="08330-105">每个角色的定价和成本可能不同，这意味着项目中的同一个资源的时间可能会根据每个角色的记帐费率和成本费率而得到不同的财务估算值。</span><span class="sxs-lookup"><span data-stu-id="08330-105">Each of these roles could be priced and costed differently which means the same resource's time on the project could get a different financial estimate depending on the bill and cost rates for each of the roles.</span></span> <span data-ttu-id="08330-106">使用 Project Service Automation，可设置指定资源的团队成员记录中的值，并可以对分配给团队成员的每个任务执行不同的替代。</span><span class="sxs-lookup"><span data-stu-id="08330-106">Project Service Automation allows the setup of the values on the team member record for the named resource and allows for different overrides on each of the tasks that the team member is assigned to.</span></span>

<span data-ttu-id="08330-107">下面的示例说明了此值的简单替代如何让资源可以在具有不同成本费率和记帐费率的项目中有多个角色。</span><span class="sxs-lookup"><span data-stu-id="08330-107">The following example  explains how the simple override of this value allows a resource to have multiple roles on a project with different cost and bill rates.</span></span>

## <a name="create-tasks"></a><span data-ttu-id="08330-108">创建任务</span><span class="sxs-lookup"><span data-stu-id="08330-108">Create tasks</span></span>
<span data-ttu-id="08330-109">为任务 A 和任务 B 分别创建一个 40 小时的项目任务。选择任务 A 作为任务 B 的前导任务。</span><span class="sxs-lookup"><span data-stu-id="08330-109">Create two project tasks for 40 hours each, Task A and Task B. Select Task A as a predecessor to Task B.</span></span>

## <a name="set-up-role-and-organization-unit-for-a-generic-project-team-member"></a><span data-ttu-id="08330-110">为通用项目团队成员设置角色和部门</span><span class="sxs-lookup"><span data-stu-id="08330-110">Set up Role and Organization Unit for a generic project team member</span></span>

1. <span data-ttu-id="08330-111">在 **计划** 页上，选择任务 A 的 **任务** 行。</span><span class="sxs-lookup"><span data-stu-id="08330-111">On the **Schedule** page, select the **Task** row for Task A.</span></span> 
2. <span data-ttu-id="08330-112">在 **资源** 字段中，从下拉列表中选择 **创建** 。</span><span class="sxs-lookup"><span data-stu-id="08330-112">In the **Resources** field, select **Create** in the drop-down list.</span></span>
3. <span data-ttu-id="08330-113">在 **团队成员快速创建** 页上，指定可执行此任务的通用团队成员的属性。</span><span class="sxs-lookup"><span data-stu-id="08330-113">On the **Team Member Quick Create** page, specify the attributes of the generic team member who can perform this task.</span></span>
4. <span data-ttu-id="08330-114">选择相应的角色和部门，然后选择 **保存并关闭** 。</span><span class="sxs-lookup"><span data-stu-id="08330-114">Select the appropriate role and organizational unit, and then select **Save and Close**.</span></span> <span data-ttu-id="08330-115">将创建一个通用团队成员，并将其分配给此任务。</span><span class="sxs-lookup"><span data-stu-id="08330-115">A generic team member is created and assigned to this task.</span></span> 

<span data-ttu-id="08330-116">对任务 B 重复这些步骤，并确保为任务 B 创建的通用团队成员中的角色和部门与任务 A 不同。</span><span class="sxs-lookup"><span data-stu-id="08330-116">Repeat these steps for Task B and make sure that the role and organizational unit on the generic team member created for Task B is different than Task A.</span></span> 

## <a name="set-up-role-and-organization-unit-for-a-project-task"></a><span data-ttu-id="08330-117">为项目任务设置角色和部门</span><span class="sxs-lookup"><span data-stu-id="08330-117">Set up role and organization unit for a project task</span></span>

1. <span data-ttu-id="08330-118">创建任务后，选择该任务，然后选择 **编辑任务** 。</span><span class="sxs-lookup"><span data-stu-id="08330-118">After you create Task A, select the task, and then select **Edit task**.</span></span>
2. <span data-ttu-id="08330-119">在 **任务详细信息** 页上，找到 **角色** 和 **部门** 字段，添加要执行此任务的资源所需的值。</span><span class="sxs-lookup"><span data-stu-id="08330-119">On the **Task Details** page, find the **Role** and **Organizational Unit** fields, add the values that are required of a resource that would perform this task.</span></span> 

  > [!NOTE]
  > <span data-ttu-id="08330-120">如果您使用 Project Service Automation 演示数据完成此场景，角色选择 **咨询负责人** ，部门选择 **Fabrikam US** 。</span><span class="sxs-lookup"><span data-stu-id="08330-120">If you are completing this scenarios using Project Service Automation demo data, select **Consulting Lead** for the role, and **Fabrikam US** as the organizational unit.</span></span>

3. <span data-ttu-id="08330-121">选择任务 B，然后选择 **编辑任务** 。</span><span class="sxs-lookup"><span data-stu-id="08330-121">Select Task B and then select **Edit task**.</span></span>
4. <span data-ttu-id="08330-122">在 **任务详细信息** 页上，找到 **角色** 和 **部门** 字段，添加要执行此任务的资源所需的值。</span><span class="sxs-lookup"><span data-stu-id="08330-122">On the **Task Details** page, find the **Role** and **Organizational Unit** fields, add the values that are required of a resource that would perform this task.</span></span> <span data-ttu-id="08330-123">确保 **角色** 和 **部门** 字段中的值对于任务 A 和任务 B 是不同的。</span><span class="sxs-lookup"><span data-stu-id="08330-123">Make sure that the values in the **Role** and **Organizational Unit** fields are different for Task B from those for Task A.</span></span> 

  > [!NOTE]
  > <span data-ttu-id="08330-124">如果您使用 Project Service Automation 演示数据完成此场景，角色选择 **网络技术人员** ，部门选择 **Fabrikam US** 。</span><span class="sxs-lookup"><span data-stu-id="08330-124">If you are completing this scenarios using Project Service Automation demo data, select **Network Technician** for the role, and **Fabrikam US** as the organizational unit.</span></span>

5. <span data-ttu-id="08330-125">保存并关闭 **任务详细信息** 页。</span><span class="sxs-lookup"><span data-stu-id="08330-125">Save and close the **Task Details** page.</span></span> 

## <a name="team-member-and-estimates-behaviour"></a><span data-ttu-id="08330-126">团队成员和估算行为</span><span class="sxs-lookup"><span data-stu-id="08330-126">Team member and estimates behaviour</span></span> 

1. <span data-ttu-id="08330-127">在 **任务详细信息** 页上的 **团队成员** 中，选择两个通用团队成员，然后选择 **生成要求** 。</span><span class="sxs-lookup"><span data-stu-id="08330-127">On the **Task Details** page, on the **Team Member** , select the two generic team Members and then select **Generate Requirements**.</span></span> <span data-ttu-id="08330-128">这将生成资源要求。</span><span class="sxs-lookup"><span data-stu-id="08330-128">This will generate resource requirements.</span></span> 
2. <span data-ttu-id="08330-129">选择 **咨询负责人** 的团队成员行，然后选择 **预订** 。</span><span class="sxs-lookup"><span data-stu-id="08330-129">Select the team member row for **Consulting Lead** and then select **Book**.</span></span> <span data-ttu-id="08330-130">日程安排板将打开并为该要求预订资源。</span><span class="sxs-lookup"><span data-stu-id="08330-130">The schedule board opens and books a resource to that requirement.</span></span>
3. <span data-ttu-id="08330-131">选择 **网络技术人员** 的团队成员行，然后选择 **预订** 。</span><span class="sxs-lookup"><span data-stu-id="08330-131">Select the team member row for **Network Technician** and the select **Book**.</span></span> <span data-ttu-id="08330-132">日程安排板将打开并在该要求中预订同一个资源。</span><span class="sxs-lookup"><span data-stu-id="08330-132">The schedule board opens and books the same resource on that requirement.</span></span>

### <a name="team-member-grid"></a><span data-ttu-id="08330-133">团队成员网格</span><span class="sxs-lookup"><span data-stu-id="08330-133">Team Member grid</span></span> 
<span data-ttu-id="08330-134">在 **团队成员** 网格上，注意两个通用团队成员记录已删除，并替换为一个资源。</span><span class="sxs-lookup"><span data-stu-id="08330-134">On the **Team Member** grid, notice that the two generic team member records are deleted and have been replaced one resource.</span></span> <span data-ttu-id="08330-135">该资源有一组值，显示 **角色** 和 **部门** 的一组默认值。</span><span class="sxs-lookup"><span data-stu-id="08330-135">There is one set of values for that resource that shows a default set of values for **Role** and **Organizational Unit**.</span></span>
<span data-ttu-id="08330-136">当您展开该团队成员记录的行时，您可以看到这两个任务的团队成员记录中显示不同的工作。</span><span class="sxs-lookup"><span data-stu-id="08330-136">When you expand the row of that Team Member record, you can see distinct assignments on the team member record for both of those tasks.</span></span> <span data-ttu-id="08330-137">每个工作行具有任务特定的 **角色** 和 **部门** 值。</span><span class="sxs-lookup"><span data-stu-id="08330-137">Each assignment row has task specific values for **Role** and **Organizational Unit**.</span></span> 

### <a name="estimates-grid"></a><span data-ttu-id="08330-138">估算网格</span><span class="sxs-lookup"><span data-stu-id="08330-138">Estimates grid</span></span> 
<span data-ttu-id="08330-139">当您导航到 **估算** 网格时，您会注意到同一资源的两项工作的定价不同。</span><span class="sxs-lookup"><span data-stu-id="08330-139">When you navigate to the **Estimates** grid, you will notice that both assignments for the same resource are priced differently.</span></span>
<span data-ttu-id="08330-140">任务 A 中的资源的工作使用 **咨询负责人** 的 **角色** 属性值定价。</span><span class="sxs-lookup"><span data-stu-id="08330-140">The assignment for the resource on Task A is priced using the **Role** attribute value of **Consulting Lead**.</span></span> <span data-ttu-id="08330-141">任务 B 中的同一个资源的工作使用 **网络技术人员** 的 **角色** 属性值定价。</span><span class="sxs-lookup"><span data-stu-id="08330-141">The assignment for the same resource on Task B is priced using the **Role** attribute value of **Network Technician**.</span></span>





