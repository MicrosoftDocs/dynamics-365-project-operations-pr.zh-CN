---
title: 如何在 Web 应用程序中将可预订资源分派给任务
description: 可预订资源分派方法的概述。
author: JohnPBurrows
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 8/21/2018
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: cc1859540ede064c4ab3e2ac128573972912a207
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/28/2020
ms.locfileid: "4125167"
---
# <a name="how-do-i-assign-a-bookable-resource-to-a-task-in-the-web-app-project-service-app-v2x"></a><span data-ttu-id="e733d-103">如何在 Web 应用程序（Project Service 应用程序 v2.x）中将可预订资源分派到任务？</span><span class="sxs-lookup"><span data-stu-id="e733d-103">How do I assign a bookable resource to a task in the web app (Project Service app v2.x)?</span></span>

[!INCLUDE[cc-applies-to-psa-app-1.x-2.x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="e733d-104">在 Project Service 中可通过两种方法将资源分派到任务。</span><span class="sxs-lookup"><span data-stu-id="e733d-104">There are two ways to assign a resource to a task in Project Service.</span></span> <span data-ttu-id="e733d-105">您可以作为团队成员预订资源，然后将它分派到任务。</span><span class="sxs-lookup"><span data-stu-id="e733d-105">You can book a resource as a team member and then assign it to a task.</span></span> <span data-ttu-id="e733d-106">或者，可以通过任务的角色分派创建通用团队成员，生成团队，然后通过指定资源满足备份要求。</span><span class="sxs-lookup"><span data-stu-id="e733d-106">Or, you can create a generic team member through role assignment on tasks, generate a team, and then fulfill the backing requirements with a named resource.</span></span>

<span data-ttu-id="e733d-107">请注意，如果您要将可预订资源分派到任务，可预订资源团队成员必须有足够的可用预订。</span><span class="sxs-lookup"><span data-stu-id="e733d-107">Note that if you’d like to assign a bookable resource to a task, the bookable resource team member must have enough available bookings.</span></span> <span data-ttu-id="e733d-108">预订的状态必须为“提交类型硬性预订”和“已提交状态”。</span><span class="sxs-lookup"><span data-stu-id="e733d-108">The status of the booking must be Commit Type Hard Book and Status Committed.</span></span> <span data-ttu-id="e733d-109">如果资源没有足够的预订，Project Service 将删除分派并显示以下错误消息：</span><span class="sxs-lookup"><span data-stu-id="e733d-109">If there aren’t enough bookings for the resource, Project Service removes the assignment and displays the following error message:</span></span>

<span data-ttu-id="e733d-110">*无法将资源分派到任务 - 以下资源没有为项目预订的足够时间*</span><span class="sxs-lookup"><span data-stu-id="e733d-110">*Unable to assign resource to task - Following resource(s) do not have sufficient hours booked against project*</span></span>

## <a name="book-a-resource-as-a-team-member-and-then-assign-the-resource-to-a-task"></a><span data-ttu-id="e733d-111">作为团队成员预订资源，然后将资源分派到任务。</span><span class="sxs-lookup"><span data-stu-id="e733d-111">Book a resource as a team member and then assign the resource to a task</span></span>

<span data-ttu-id="e733d-112">使用该方法，您将资源添加到项目团队，然后在项目计划中将任务分派给资源。</span><span class="sxs-lookup"><span data-stu-id="e733d-112">With this method you add a resource to the project team and then assign tasks to the resource in the project schedule.</span></span> <span data-ttu-id="e733d-113">以下是如何操作：</span><span class="sxs-lookup"><span data-stu-id="e733d-113">Here’s how you do this:</span></span>
1.  <span data-ttu-id="e733d-114">在团队成员网格中，通过选中 **新建** 添加新团队成员。</span><span class="sxs-lookup"><span data-stu-id="e733d-114">On the team member grid, add a new team member by selecting **New**.</span></span>
2.  <span data-ttu-id="e733d-115">在“团队成员快速创建”屏幕上，选择可预订资源名称并设置角色。</span><span class="sxs-lookup"><span data-stu-id="e733d-115">On the Team Member Quick Create screen, select the bookable resource name and set a role.</span></span>
3.  <span data-ttu-id="e733d-116">选择 **起始** 和 **截止** 日期。</span><span class="sxs-lookup"><span data-stu-id="e733d-116">Select the **From** and **To** dates.</span></span>

    > [!div class="mx-imgBorder"] 
    > <span data-ttu-id="e733d-117">![添加团队成员的屏幕截图](media/FAQ-Resources-to-Tasks2-1.png "添加团队成员的屏幕截图")</span><span class="sxs-lookup"><span data-stu-id="e733d-117">![Screenshot of adding team member](media/FAQ-Resources-to-Tasks2-1.png "Screenshot of adding team member")</span></span>
 
4.  <span data-ttu-id="e733d-118">选择以下分配方法之一预订资源：</span><span class="sxs-lookup"><span data-stu-id="e733d-118">Select one of the following allocation methods for booking the resource:</span></span>
    - <span data-ttu-id="e733d-119">**完全产能** 为指定的起始日期和截止日期预订资源的完全产能。</span><span class="sxs-lookup"><span data-stu-id="e733d-119">**Full Capacity** books the resource’s full capacity for the specified from and to dates.</span></span>
    - <span data-ttu-id="e733d-120">**产能百分比** 为指定的起始日期和截止日期预订资源产能的百分比。</span><span class="sxs-lookup"><span data-stu-id="e733d-120">**Percentage Capacity** books the resource for a percentage of the resource's capacity for the specified from and to dates.</span></span>
    - <span data-ttu-id="e733d-121">**按时数平均分配** 预订资源指定的小时数，根据指定的起始日期和截止日期按天平均分配时间。</span><span class="sxs-lookup"><span data-stu-id="e733d-121">**By Hours Distribute Evenly** books the resource for a specified number of hours, distributing it evenly per day over the specified from and to dates.</span></span>
    - <span data-ttu-id="e733d-122">**按时数前期负荷** 预订资源指定的小时数，根据指定的起始日期和截止日期前期负荷每天的时间。</span><span class="sxs-lookup"><span data-stu-id="e733d-122">**By Hours Front Load** books the resource for a specified number of hours, front-loading the per-day hours over the specified from and to dates.</span></span>

    <span data-ttu-id="e733d-123">请勿选择 **无**，因为这会将资源添加到团队，但不创建任何分配资源产能的预订。</span><span class="sxs-lookup"><span data-stu-id="e733d-123">Don’t select **None** because it adds the resource to the team but doesn’t create any bookings that absorb the resource's capacity.</span></span>
5.  <span data-ttu-id="e733d-124">选择 **保存**。</span><span class="sxs-lookup"><span data-stu-id="e733d-124">Select **Save**.</span></span>

    <span data-ttu-id="e733d-125">请注意，预订小时数必须足够覆盖您向其分派此资源的任务的工作时间和日期范围。</span><span class="sxs-lookup"><span data-stu-id="e733d-125">Note that the hours of the booking must be enough to cover the effort hours and date ranges of the tasks that you assign this resource to.</span></span> <span data-ttu-id="e733d-126">如果它们不一致，则无法将资源分派到任务。</span><span class="sxs-lookup"><span data-stu-id="e733d-126">If they aren’t in alignment, you can’t assign the resource to the task.</span></span>

6.  <span data-ttu-id="e733d-127">在任务的工作分解结构 (WBS) 上，单击资源单元格下拉列表。</span><span class="sxs-lookup"><span data-stu-id="e733d-127">On the work breakdown structure (WBS) for the task, click the resource cell dropdown.</span></span> <span data-ttu-id="e733d-128">然后：</span><span class="sxs-lookup"><span data-stu-id="e733d-128">Then:</span></span> 

    1. <span data-ttu-id="e733d-129">选择 **添加**。</span><span class="sxs-lookup"><span data-stu-id="e733d-129">Select **Add**.</span></span>
    2. <span data-ttu-id="e733d-130">选择 **资源** 下的下拉列表，并选择您上面添加的团队成员。</span><span class="sxs-lookup"><span data-stu-id="e733d-130">Select the dropdown under **Resources** and select the team member you added above.</span></span>
    3. <span data-ttu-id="e733d-131">选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="e733d-131">Select **OK**.</span></span> <span data-ttu-id="e733d-132">团队成员现在分派到了任务。</span><span class="sxs-lookup"><span data-stu-id="e733d-132">The team member is now assigned to the task.</span></span>

    > [!div class="mx-imgBorder"] 
    > <span data-ttu-id="e733d-133">![使用 WBS 添加资源的屏幕截图](media/FAQ-Resources-to-Tasks2-2.png "使用 WBS 添加资源的屏幕截图")</span><span class="sxs-lookup"><span data-stu-id="e733d-133">![Screenshot of adding resources with WBS](media/FAQ-Resources-to-Tasks2-2.png "Screenshot of adding resources with WBS")</span></span>
 
<span data-ttu-id="e733d-134">在团队成员网格上，您将在“分派的时数”下看到资源的已分派时数的总和。</span><span class="sxs-lookup"><span data-stu-id="e733d-134">On the team member grid, you’ll see the aggregate of the resource’s assigned hours under Assigned Hours.</span></span> <span data-ttu-id="e733d-135">它将小于或等于资源的预订时数。</span><span class="sxs-lookup"><span data-stu-id="e733d-135">It will be less than or equal to the booked hours for the resource.</span></span> 

> [!div class="mx-imgBorder"] 
> <span data-ttu-id="e733d-136">![资源的已分派时数的屏幕截图](media/FAQ-Resources-to-Tasks2-3.png "资源的已分派时数的屏幕截图")</span><span class="sxs-lookup"><span data-stu-id="e733d-136">![Screenshot of assigned hours for a resource](media/FAQ-Resources-to-Tasks2-3.png "Screenshot of assigned hours for a resource")</span></span>
 
<span data-ttu-id="e733d-137">如果您尝试分派到资源的任务在资源预订的结束日期之后开始，此资源将不会显示在下拉列表中。</span><span class="sxs-lookup"><span data-stu-id="e733d-137">If the task you’re attempting to assign to the resource starts after the end date of the resources bookings, the resource won’t appear in the dropdown.</span></span>

<span data-ttu-id="e733d-138">请注意，如果资源有一些剩余的未分派产能，那么您可以将资源分派给多于其已预订时数的时数。</span><span class="sxs-lookup"><span data-stu-id="e733d-138">Note that you can assign a resource to more hours than their booked hours if the resource has some remaining unassigned capacity.</span></span> <span data-ttu-id="e733d-139">在这种情况下，资源仅部分分派到其预订。</span><span class="sxs-lookup"><span data-stu-id="e733d-139">In this case the resource will only be partially assigned up to their bookings.</span></span> <span data-ttu-id="e733d-140">您可以通过将“未分派时数”列添加到工作分解结构来查看这些剩余的未分派任务时数。</span><span class="sxs-lookup"><span data-stu-id="e733d-140">You can see these remaining unassigned task hours by adding the Unstaffed Hours column to the work breakdown structure.</span></span>

<span data-ttu-id="e733d-141">如果资源被分派给他们预订的时数（其已预订时数等于其已分派时数），在您尝试向他们分派其他任务时，您将看到以下错误消息：</span><span class="sxs-lookup"><span data-stu-id="e733d-141">If resources are assigned to their booked hours (their booked hours equals their assigned hours), you’ll see the following error message when you attempt to assign them further tasks:</span></span>

<span data-ttu-id="e733d-142">*无法将资源分派到任务 - 以下资源没有为项目预订的足够时间。*</span><span class="sxs-lookup"><span data-stu-id="e733d-142">*Unable to assign resource to task - Following resource(s) do not have sufficient hours booked against project.*</span></span>

<span data-ttu-id="e733d-143">此外，在您创建项目时添加到团队的默认项目经理团队成员也将被添加且无任何预订，并且无法被分派到任何任务。</span><span class="sxs-lookup"><span data-stu-id="e733d-143">Additionally, the default project manager team member that is added to the team when you create the project is added without any bookings and can’t be assigned to any task.</span></span> <span data-ttu-id="e733d-144">它们不会显示在任务的资源下拉列表中。</span><span class="sxs-lookup"><span data-stu-id="e733d-144">They won’t show up in the resource dropdown for tasks.</span></span>

<span data-ttu-id="e733d-145">如果要分派此资源，您需要从团队中将其删除，然后使用“无”以外的分配方法重新添加它们。</span><span class="sxs-lookup"><span data-stu-id="e733d-145">If you want to assign this resource, you need to remove them from the team and then re-add them with an allocation method other than None.</span></span> <span data-ttu-id="e733d-146">在创建项目时将它们添加到团队的原因是为了项目在默认情况下至少有一个项目审批者。</span><span class="sxs-lookup"><span data-stu-id="e733d-146">The reason they’re added to the team when the project is created is so that a project has at least one project approver by default.</span></span>

## <a name="create-a-generic-team-member-through-role-assignment-on-tasks"></a><span data-ttu-id="e733d-147">通过任务上的角色分派创建通用团队成员</span><span class="sxs-lookup"><span data-stu-id="e733d-147">Create a generic team member through role assignment on tasks</span></span>

<span data-ttu-id="e733d-148">此方法将确保资源有足够的任务的预订。</span><span class="sxs-lookup"><span data-stu-id="e733d-148">This method assures that resources have enough bookings for tasks.</span></span> <span data-ttu-id="e733d-149">首先，在将角色分派到任务后生成团队，通过此方式创建描述指定资源（您最终希望处理任务的资源）的特征的占位符或通用资源。</span><span class="sxs-lookup"><span data-stu-id="e733d-149">First, you create a placeholder or generic resource that describes the characteristics of the named resource you ultimately want to work on the tasks by generating a team after assigning roles to tasks.</span></span> <span data-ttu-id="e733d-150">以下是如何操作：</span><span class="sxs-lookup"><span data-stu-id="e733d-150">Here’s how you do this:</span></span>

1. <span data-ttu-id="e733d-151">在工作分解结构上，选择一项任务。</span><span class="sxs-lookup"><span data-stu-id="e733d-151">On the work breakdown structure, select a task.</span></span>
2. <span data-ttu-id="e733d-152">在资源单元格中选择 **已分派角色** 下拉列表图标。</span><span class="sxs-lookup"><span data-stu-id="e733d-152">Select the **Assigned Role** dropdown icon in the resource cell.</span></span>
3. <span data-ttu-id="e733d-153">选择 **角色** 下拉列表并选择通用资源的角色。</span><span class="sxs-lookup"><span data-stu-id="e733d-153">Select the **Role** dropdown and select the role for the generic resource.</span></span>
4. <span data-ttu-id="e733d-154">选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="e733d-154">Select **OK**.</span></span>

    > [!div class="mx-imgBorder"] 
    > <span data-ttu-id="e733d-155">![使用 WBS 添加资源的屏幕截图](media/FAQ-Resources-to-Tasks2-4.png "使用 WBS 添加资源的屏幕截图")</span><span class="sxs-lookup"><span data-stu-id="e733d-155">![Screenshot of using WBS to add resource](media/FAQ-Resources-to-Tasks2-4.png "Screenshot of using WBS to add resource")</span></span>
 
<span data-ttu-id="e733d-156">在 WBS 中将角色分派到任务后，选择 **生成项目团队**。</span><span class="sxs-lookup"><span data-stu-id="e733d-156">Once you’ve completed assigning roles to the tasks in the WBS, select **Generate Project Team**.</span></span> <span data-ttu-id="e733d-157">Project Service 根据角色、资源部门和项目日历通过聚合任务分派来创建最低数量的通用团队成员。</span><span class="sxs-lookup"><span data-stu-id="e733d-157">Project Service creates the minimum number of generic team members based on the roles, resourcing organization units, and project calendar by aggregating the task assignments.</span></span>

> [!div class="mx-imgBorder"] 
> <span data-ttu-id="e733d-158">![生成项目团队的屏幕截图](media/FAQ-Resources-to-Tasks2-5.png "生成项目团队的屏幕截图")</span><span class="sxs-lookup"><span data-stu-id="e733d-158">![Screenshot of generating project team](media/FAQ-Resources-to-Tasks2-5.png "Screenshot of generating project team")</span></span>
 
<span data-ttu-id="e733d-159">在团队成员网格中，您将会看到具有此角色和职位名称的通用资源类型的资源。</span><span class="sxs-lookup"><span data-stu-id="e733d-159">On the Team Member grid, you’ll see resources of the Generic Resource type with the role and position name.</span></span> <span data-ttu-id="e733d-160">如果角色需要两个资源来完成工作，“生成团队”功能将创建两个团队成员，并使用职位名称来区分它们。</span><span class="sxs-lookup"><span data-stu-id="e733d-160">If two resources are needed for a role to complete the work, the Generate Team feature creates two team members and uses position name to set them apart.</span></span>

> [!div class="mx-imgBorder"] 
> <span data-ttu-id="e733d-161">![添加两个通用资源的屏幕截图](media/FAQ-Resources-to-Tasks2-6.png "添加两个通用资源的屏幕截图")</span><span class="sxs-lookup"><span data-stu-id="e733d-161">![Screenshot of adding two generic resources](media/FAQ-Resources-to-Tasks2-6.png "Screenshot of adding two generic resources")</span></span>
 
<span data-ttu-id="e733d-162">您可以通过选择“资源要求”下的链接来打开通用团队成员的支持资源要求。</span><span class="sxs-lookup"><span data-stu-id="e733d-162">You can open the backing resource requirement for the generic team member by selecting the link under Resource Requirement.</span></span>

> [!div class="mx-imgBorder"] 
> <span data-ttu-id="e733d-163">![打开支持资源要求的屏幕截图](media/FAQ-Resources-to-Tasks2-7.png "打开支持资源要求的屏幕截图")</span><span class="sxs-lookup"><span data-stu-id="e733d-163">![Screenshot of opening backing resource requirement](media/FAQ-Resources-to-Tasks2-7.png "Screenshot of opening backing resource requirement")</span></span>

<span data-ttu-id="e733d-164">为通用资源选择 **预订**，然后您可以使用日程安排板查找和预订实际资源。</span><span class="sxs-lookup"><span data-stu-id="e733d-164">Select **Book** for the generic resource, and then you can use the schedule board to find and book a real resource.</span></span> <span data-ttu-id="e733d-165">您还可以通过选择 **提交请求** 来提交由资源经理满足的要求。</span><span class="sxs-lookup"><span data-stu-id="e733d-165">You can also submit the requirement for fulfillment by a resource manager by selecting **Submit Request**.</span></span>

<span data-ttu-id="e733d-166">在通用资源要求由指定资源满足时，通用资源将被从团队中移除，通用资源的任务分派将被分派到满足通用资源的资源要求的指定资源。</span><span class="sxs-lookup"><span data-stu-id="e733d-166">When the generic resource is fulfilled with a named resource, the generic resource is removed from the team and the task assignments for the generic resource are assigned to the named resource that fulfilled the generic resource’s resource requirement.</span></span>
 

