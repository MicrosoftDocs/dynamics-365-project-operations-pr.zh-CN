---
title: 管理资源
description: 此主题介绍如何管理资源。
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 05/13/2019
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
ms.openlocfilehash: 5b34ad66750dba9459d551a2527c13111196511e
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/16/2020
ms.locfileid: "4072805"
---
# <a name="manage-resources"></a><span data-ttu-id="4bec8-103">管理资源</span><span class="sxs-lookup"><span data-stu-id="4bec8-103">Manage resources</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="4bec8-104">Dynamics 365 Project Service Automation 有一个资源管理器仪表板，其提供整个组织内的资源需求和利用率的视觉概览。</span><span class="sxs-lookup"><span data-stu-id="4bec8-104">Dynamics 365 Project Service Automation includes a resource manager dashboard that provides a visual overview of resource demand and utilization throughout the organization.</span></span> <span data-ttu-id="4bec8-105">可使用此仪表板中的图表可视化以下信息：</span><span class="sxs-lookup"><span data-stu-id="4bec8-105">You can use the charts on this dashboard to visualize the following information:</span></span>

- <span data-ttu-id="4bec8-106">**资源需求** – **可用的资源请求** 图表显示已提交的资源。</span><span class="sxs-lookup"><span data-stu-id="4bec8-106">**Resource demand** – The **Active Resource Request** chart shows resources that have been submitted.</span></span> <span data-ttu-id="4bec8-107">资源按角色或项目聚合。</span><span class="sxs-lookup"><span data-stu-id="4bec8-107">The resources are aggregated by either role or project.</span></span>
- <span data-ttu-id="4bec8-108">**未提交的资源需求** – **未分派的资源需求** 图表显示尚未提交的所有资源要求。</span><span class="sxs-lookup"><span data-stu-id="4bec8-108">**Unsubmitted resource demand** – The **Unassigned Resource Demand** chart shows all the resource requirements that haven't been submitted.</span></span> <span data-ttu-id="4bec8-109">可帮助资源经理查看不确定且可以通过资源请求提交的需求。</span><span class="sxs-lookup"><span data-stu-id="4bec8-109">It helps resource managers view demand that isn't firm and might be submitted through a resource request.</span></span>
- <span data-ttu-id="4bec8-110">**上周的可记帐利用率** – **按角色列出的利用率** 图表显示组织的按角色实际可记帐利用率占其按角色目标可记帐利用率的百分比。</span><span class="sxs-lookup"><span data-stu-id="4bec8-110">**Billable utilization for the past week** – The **Utilization by Role** chart shows the percentage of the organization's actual billable utilization by role against its target billable utilization by role.</span></span>

    > [!NOTE]
    > <span data-ttu-id="4bec8-111">若要使用 **按角色列出的利用率** 图表，请创建一个使用 UpdateRoleUtilization 工作流的作业。</span><span class="sxs-lookup"><span data-stu-id="4bec8-111">To make the **Utilization by Role** chart available, create a job that runs the UpdateRoleUtilization workflow.</span></span> <span data-ttu-id="4bec8-112">这个定期作业每隔七天运行一次，以计算前七天的可记帐利用率。</span><span class="sxs-lookup"><span data-stu-id="4bec8-112">This recurring job runs every seven days to calculate billable utilization for the previous seven days.</span></span> <span data-ttu-id="4bec8-113">结果按角色聚合。</span><span class="sxs-lookup"><span data-stu-id="4bec8-113">The results are aggregated by role.</span></span>

## <a name="manage-project-team-members"></a><span data-ttu-id="4bec8-114">管理项目团队成员</span><span class="sxs-lookup"><span data-stu-id="4bec8-114">Manage project team members</span></span>

<span data-ttu-id="4bec8-115">项目经理可使用资源管理器仪表板管理项目的资源。</span><span class="sxs-lookup"><span data-stu-id="4bec8-115">Project managers can use the resource manager dashboard to manage the resources on projects.</span></span> <span data-ttu-id="4bec8-116">例如，其可直接向项目添加团队成员和预订团队成员来满足通用资源捕获的资源要求。</span><span class="sxs-lookup"><span data-stu-id="4bec8-116">For example, they can add a team member directly to a project and book a team member to fulfill the resource requirements that were captured by a generic resource.</span></span>

### <a name="add-a-team-member-directly-to-a-project"></a><span data-ttu-id="4bec8-117">直接向项目添加团队成员</span><span class="sxs-lookup"><span data-stu-id="4bec8-117">Add a team member directly to a project</span></span>

<span data-ttu-id="4bec8-118">若要直接向项目添加团队成员，请在 **项目** 页的 **团队** 选项卡上，选择 **新建** 。</span><span class="sxs-lookup"><span data-stu-id="4bec8-118">To add a team member directly to a project, on the **Projects** page, on the **Team** tab, select **New**.</span></span> <span data-ttu-id="4bec8-119">将打开 **快速创建: 项目团队成员** 对话框。</span><span class="sxs-lookup"><span data-stu-id="4bec8-119">The **Quick Create:Project Team Member** dialog box appears.</span></span> <span data-ttu-id="4bec8-120">在此对话框中，可执行以下任务：</span><span class="sxs-lookup"><span data-stu-id="4bec8-120">In this dialog box, you can perform these tasks:</span></span>

- <span data-ttu-id="4bec8-121">**预订指定资源** – 在 **可预订资源** 字段中，选择资源的名称。</span><span class="sxs-lookup"><span data-stu-id="4bec8-121">**Book a named resource** – In the **Bookable Resource** field, select the name of the resource.</span></span> <span data-ttu-id="4bec8-122">然后选择角色，设置期间，再选择分配方法。</span><span class="sxs-lookup"><span data-stu-id="4bec8-122">Then select the role, set the period, and select an allocation method.</span></span> <span data-ttu-id="4bec8-123">将使用所选分配方法和资源日历把所选指定资源添加到项目。</span><span class="sxs-lookup"><span data-stu-id="4bec8-123">The named resource that you selected is added to the project by using the selected allocation method and the resources calendar.</span></span>
- <span data-ttu-id="4bec8-124">**添加通用资源** – 让 **可预订资源** 字段保留为空，然后选择角色，设置期间，再选择首选分配方法。</span><span class="sxs-lookup"><span data-stu-id="4bec8-124">**Add a generic resource** – Leave the **Bookable resource** field blank, and then select the role, set the period, and select the preferred allocation method.</span></span> <span data-ttu-id="4bec8-125">将把通用资源添加到团队来充当占位符，以存储用于为团队预订指定资源的需求模式。</span><span class="sxs-lookup"><span data-stu-id="4bec8-125">A generic resource is added to the team as a placeholder to hold the demand pattern that is used to book named resources on the team.</span></span> <span data-ttu-id="4bec8-126">将根据项目日历创建要求。</span><span class="sxs-lookup"><span data-stu-id="4bec8-126">The requirement is made according to the project calendar.</span></span>
- <span data-ttu-id="4bec8-127">**向团队添加指定资源但不占用资源产能** – 在 **可预订资源** 字段中，选择一个资源。</span><span class="sxs-lookup"><span data-stu-id="4bec8-127">**Add a named resource to the team without consuming resource capacity** – In the **Bookable Resource** field, select a resource.</span></span> <span data-ttu-id="4bec8-128">然后选择角色，并选择 **无** 作为分配方法。</span><span class="sxs-lookup"><span data-stu-id="4bec8-128">Then select the period, and select **None** as the allocation method.</span></span> <span data-ttu-id="4bec8-129">将把该资源添加到团队，但不通过预订占用该资源的产能。</span><span class="sxs-lookup"><span data-stu-id="4bec8-129">The resource is added to the team, but the resource's capacity isn't consumed through a booking.</span></span>

### <a name="book-a-team-member-to-fulfill-resource-requirements-for-a-generic-resource"></a><span data-ttu-id="4bec8-130">预订团队成员以满足对通用资源的资源要求</span><span class="sxs-lookup"><span data-stu-id="4bec8-130">Book a team member to fulfill resource requirements for a generic resource</span></span>

<span data-ttu-id="4bec8-131">在 PSA 中，可为项目团队预订通用资源，还可以指定角色、所需产能和产能的分配方法。</span><span class="sxs-lookup"><span data-stu-id="4bec8-131">In PSA, you can book a generic resource on a project team, and can specify the role, the required capacity, and how that capacity is distributed.</span></span> <span data-ttu-id="4bec8-132">可以为资源要求指定与通用资源关联的属性。</span><span class="sxs-lookup"><span data-stu-id="4bec8-132">On the resource requirement, you can specify attributes that are associated with the generic resource.</span></span> <span data-ttu-id="4bec8-133">这些属性包括所需技能、首选部门和首选资源。</span><span class="sxs-lookup"><span data-stu-id="4bec8-133">These attributes include required skills, the preferred organizational unit, and preferred resources.</span></span>

<span data-ttu-id="4bec8-134">执行以下步骤指定开发人员通用资源所需技能。</span><span class="sxs-lookup"><span data-stu-id="4bec8-134">Follow these steps to specify required skills on a generic resource for a developer.</span></span>

1. <span data-ttu-id="4bec8-135">在 **项目** 页的 **团队** 选项卡上，选择 **新建** 以预订一个通用资源。</span><span class="sxs-lookup"><span data-stu-id="4bec8-135">On the **Projects** page, on the **Team** tab, select **New** to book a generic resource.</span></span>

    ![团队中预订的通用资源](media/Resource-Management-image9.png)

2. <span data-ttu-id="4bec8-137">在 **所有团队成员** 视图的 **资源要求** 列中，选择用于添加通用资源所需技能的链接。</span><span class="sxs-lookup"><span data-stu-id="4bec8-137">In the **All Team Members** view, in the **Resource Requirement** column, select the link to add required skills for the generic resource.</span></span>

    ![“要求”链接](media/Resource-Management-image10.png)

3. <span data-ttu-id="4bec8-139">在显示的 **资源要求** 页的 **技能** 网格中，选择省略号 ( **...** )，然后选择 **添加新要求特征** 以添加您的开发人员所需技能。</span><span class="sxs-lookup"><span data-stu-id="4bec8-139">On the **Resource Requirement** page that appears, in the **Skills** grid, select the ellipsis ( **...** ) and then select **Add New Requirement Characteristic** to add the required skills for your developer.</span></span>

    ![“添加新要求特征”命令](media/Resource-Management-image11.png)

4. <span data-ttu-id="4bec8-141">在显示的 **快速创建: 要求特征** 对话框的 **特征** 字段中，选择所需技能。</span><span class="sxs-lookup"><span data-stu-id="4bec8-141">In the **Quick Create: Requirement Characteristic** dialog box that appears, in the **Characteristic** field, select the required skill.</span></span> <span data-ttu-id="4bec8-142">然后在 **等级值** 字段中，选择该技能的熟练级别。</span><span class="sxs-lookup"><span data-stu-id="4bec8-142">Then, in the **Rating value** field, select the proficiency level for that skill.</span></span> <span data-ttu-id="4bec8-143">最后，在 **资源要求** 字段中，设置对部门来源资源或指定资源的要求。</span><span class="sxs-lookup"><span data-stu-id="4bec8-143">Finally, in the **Resource Requirement** field, set the requirement to source resources from organizational units or even named resources.</span></span> <span data-ttu-id="4bec8-144">在您完成时，选择 **保存** 。</span><span class="sxs-lookup"><span data-stu-id="4bec8-144">When you've finished, select **Save**.</span></span>

    ![“快速创建: 要求特征”对话框](media/Resource-Management-image12.png)

5. <span data-ttu-id="4bec8-146">在 **资源要求** 页中，选择 **预订** 以满足资源要求。</span><span class="sxs-lookup"><span data-stu-id="4bec8-146">On the **Resource Requirement** page, select **Book** to fulfill the resource requirement.</span></span>

    ![“资源要求”页上的“预订”按钮](media/Resource-Management-image13.png)

    <span data-ttu-id="4bec8-148">也可以在 **所有团队成员** 网格中选择通用资源，然后选择 **预订** 。</span><span class="sxs-lookup"><span data-stu-id="4bec8-148">You can also select the generic resource in the **All Team Members** grid and then select **Book**.</span></span>

    ![“所有团队成员”网格上方的“预订”按钮](media/Resource-Management-image14.png)

    > [!NOTE]
    > <span data-ttu-id="4bec8-150">在此示例中，需要 40 个工时，但是没有实际预订工时，因为通用资源不能有预订。</span><span class="sxs-lookup"><span data-stu-id="4bec8-150">In this example, there are 40 required hours but no actual booked hours, because generic resources don't have bookings.</span></span> <span data-ttu-id="4bec8-151">此外，也没有分派工时，因为通用资源是直接添加到团队的。</span><span class="sxs-lookup"><span data-stu-id="4bec8-151">Additionally, there are no assigned hours, because the generic resource was added directly to the team.</span></span> <span data-ttu-id="4bec8-152">不是通过使用任务分派添加的。</span><span class="sxs-lookup"><span data-stu-id="4bec8-152">It wasn't added by using task assignment.</span></span>

    <span data-ttu-id="4bec8-153">在 **日程安排助理** 页中，可按为资源要求指定的要求筛选可用资源。</span><span class="sxs-lookup"><span data-stu-id="4bec8-153">On the **Scheduling Assistant** page, you can filter available resources by the requirements that are specified on the resource requirement.</span></span> <span data-ttu-id="4bec8-154">将根据日程安排板中指定的排序参数为资源排序。</span><span class="sxs-lookup"><span data-stu-id="4bec8-154">Resources are sorted according to the sorting parameters that are specified on the Schedule Board.</span></span>

    ![“日程安排助理”页](media/Resource-Management-image15.png)

    <span data-ttu-id="4bec8-156">下面是一些常用筛选器：</span><span class="sxs-lookup"><span data-stu-id="4bec8-156">Here are some filters that are often used:</span></span>

    - <span data-ttu-id="4bec8-157">**特征和等级** – 除了熟练等级，还按技能、认证和其他资源资质进行筛选。</span><span class="sxs-lookup"><span data-stu-id="4bec8-157">**Characteristics along with a rating** – Filter by skills, certifications, and other resource qualities, in addition to ratings of proficiency.</span></span>
    - <span data-ttu-id="4bec8-158">**角色** – 按分派给可预订资源的默认角色进行筛选。</span><span class="sxs-lookup"><span data-stu-id="4bec8-158">**Roles** – Filter by the default roles that are assigned to bookable resources.</span></span>
    - <span data-ttu-id="4bec8-159">**部门** – 按分派给的部门筛选可预订资源。</span><span class="sxs-lookup"><span data-stu-id="4bec8-159">**Organizational units** – Filter bookable resources by the organizational units that they are assigned to.</span></span>

6. <span data-ttu-id="4bec8-160">如果对要求的原始搜索结果不满意，可以更改筛选条件。</span><span class="sxs-lookup"><span data-stu-id="4bec8-160">If you aren't satisfied with the results of the initial requirement search, you can change the filter criteria.</span></span> <span data-ttu-id="4bec8-161">展开左侧 **筛选器视图** 窗格，然后选择 **搜索** 以查找更多资源。</span><span class="sxs-lookup"><span data-stu-id="4bec8-161">Expand the **Filter View** pane on the left, and then select **Search** to find additional resources.</span></span>

    ![“筛选器视图”窗格](media/Resource-Management-image16.png)

7. <span data-ttu-id="4bec8-163">若要更改结果的排序方法，请选择 **排序** 。</span><span class="sxs-lookup"><span data-stu-id="4bec8-163">To change how the results are sorted, select **Sort**.</span></span>

    ![“排序”命令](media/Resource-Management-image17.png)

8. <span data-ttu-id="4bec8-165">按照网格顶部的指示，根据为要求指定的需求选择资源。</span><span class="sxs-lookup"><span data-stu-id="4bec8-165">Select resources according to the demand that is specified on the requirement, as indicated at the top of the grid.</span></span> <span data-ttu-id="4bec8-166">可以取消选择网格中选择的单元格，以释放资源产能。</span><span class="sxs-lookup"><span data-stu-id="4bec8-166">You can clear the selection of cells in the grid and leave that resource capacity open.</span></span> <span data-ttu-id="4bec8-167">一次只能选择预订一项资源。</span><span class="sxs-lookup"><span data-stu-id="4bec8-167">Only one resource at a time can be selected as booked.</span></span>

9. <span data-ttu-id="4bec8-168">选择 **预订** 以预订所选资源，并且不关闭日程安排板，以便选择更多资源。</span><span class="sxs-lookup"><span data-stu-id="4bec8-168">Select **Book** to book the selected resource and leave the Schedule Board open, so that you can select additional resources.</span></span> <span data-ttu-id="4bec8-169">也可以选择 **预订并退出** 以预订所选资源并关闭日程安排板。</span><span class="sxs-lookup"><span data-stu-id="4bec8-169">Alternatively, select **Book & Exit** to book the selected resource and close the Schedule Board.</span></span>

    ![要预订的资源](media/Resource-Management-image19.png)

    <span data-ttu-id="4bec8-171">您将收到有关所预订工时的通知。</span><span class="sxs-lookup"><span data-stu-id="4bec8-171">You receive a notification about booked hours.</span></span> <span data-ttu-id="4bec8-172">需求指示器显示满足了多少预订要求，还有多少未满足。</span><span class="sxs-lookup"><span data-stu-id="4bec8-172">The demand indicators show how much the booking requirement is satisfied and how much remains.</span></span> <span data-ttu-id="4bec8-173">还可以查看占用了所选资源的多少产能。</span><span class="sxs-lookup"><span data-stu-id="4bec8-173">You can also see how much of the selected resource's capacity is consumed.</span></span> <span data-ttu-id="4bec8-174">选择 **展开** 查看有关资源预订的更多详细信息。</span><span class="sxs-lookup"><span data-stu-id="4bec8-174">Select **Expand** to view more details about resource bookings.</span></span>

9. <span data-ttu-id="4bec8-175">回到 **所有团队成员** 视图。</span><span class="sxs-lookup"><span data-stu-id="4bec8-175">Return to the **All Team Members** view.</span></span> <span data-ttu-id="4bec8-176">请注意，此网格中的通用资源已替换为指定资源，并且列出了向该资源预订的 40 个工时。</span><span class="sxs-lookup"><span data-stu-id="4bec8-176">In the grid, notice that the generic resource has been replaced by the named resource, and 40 hours are listed as booked for that resource.</span></span>

    ![更新后的“所有团队成员”网格](media/Resource-Management-image20.png)

    > [!NOTE]
    > <span data-ttu-id="4bec8-178">不显示分派的工时数，因为它们是直接为团队预订的。</span><span class="sxs-lookup"><span data-stu-id="4bec8-178">No assigned hours are shown, because they were booked directly on the team.</span></span> <span data-ttu-id="4bec8-179">不是使用任务分派预订的。</span><span class="sxs-lookup"><span data-stu-id="4bec8-179">They weren't booked by using task assignment.</span></span>

## <a name="assign-generic-resources-to-tasks-and-generate-resource-requirements"></a><span data-ttu-id="4bec8-180">为任务分派通用资源和生成资源要求</span><span class="sxs-lookup"><span data-stu-id="4bec8-180">Assign generic resources to tasks and generate resource requirements</span></span>

<span data-ttu-id="4bec8-181">在 PSA 中，可以创建任务，然后为其分派通用资源。</span><span class="sxs-lookup"><span data-stu-id="4bec8-181">In PSA, you can create tasks and then assign generic resources to them.</span></span> <span data-ttu-id="4bec8-182">这样就可以在估算计划和财务数字的时候由占位符来表示资源需求。</span><span class="sxs-lookup"><span data-stu-id="4bec8-182">In this way, resource demand can be represented by placeholders while you estimate your schedule and financial numbers.</span></span> <span data-ttu-id="4bec8-183">然后可以为通用资源生成资源要求并满足。</span><span class="sxs-lookup"><span data-stu-id="4bec8-183">You can then generate resource requirements for the generic resources and fulfill them.</span></span>

1. <span data-ttu-id="4bec8-184">在 **项目** 页的 **计划** 选项卡上，选择 **添加** 以创建任务。</span><span class="sxs-lookup"><span data-stu-id="4bec8-184">On the **Projects** page, on the **Schedule** tab, select **Add** to create a task.</span></span>

    ![已创建新任务](media/Resource-Management-image21.png)

2. <span data-ttu-id="4bec8-186">在 **资源** 字段中，选择 **资源选取器** 符号。</span><span class="sxs-lookup"><span data-stu-id="4bec8-186">In the **Resources** field, select the **Resource Picker** symbol.</span></span> <span data-ttu-id="4bec8-187">将显示资源选取器，其中显示项目的现有团队成员。</span><span class="sxs-lookup"><span data-stu-id="4bec8-187">The Resource Picker appears and shows existing team members for the project.</span></span>

    ![资源选取器](media/Resource-Management-image22.png)

3. <span data-ttu-id="4bec8-189">输入新通用资源的名称，然后选择 **创建** 。</span><span class="sxs-lookup"><span data-stu-id="4bec8-189">Enter the name of the new generic resource, and then select **Create**.</span></span>

    ![输入了新通用资源名称](media/Resource-Management-image23.png)

4. <span data-ttu-id="4bec8-191">在显示的 **快速创建: 项目团队成员** 对话框的 **角色** 字段中，选择通用资源的角色。</span><span class="sxs-lookup"><span data-stu-id="4bec8-191">In the **Quick Create: Project Team Member** dialog box that appears, in the **Role** field, select the role for the generic resource.</span></span> <span data-ttu-id="4bec8-192">在 **资源部门** 字段中，选择通用资源的部门。</span><span class="sxs-lookup"><span data-stu-id="4bec8-192">In the **Resourcing Unit** field, select the organizational unit for the generic resource.</span></span> <span data-ttu-id="4bec8-193">然后选择 **保存** 。</span><span class="sxs-lookup"><span data-stu-id="4bec8-193">Then select **Save**.</span></span>

    ![“快速创建: 项目团队成员”对话框](media/Resource-Management-image24.png)

    <span data-ttu-id="4bec8-195">现在已为任务分派了通用团队成员。</span><span class="sxs-lookup"><span data-stu-id="4bec8-195">The generic team member is now assigned to the task.</span></span>

    ![为任务分派了通用团队成员](media/Resource-Management-image25.png)

    <span data-ttu-id="4bec8-197">在 **团队** 选项卡上，您将看到新的团队成员。</span><span class="sxs-lookup"><span data-stu-id="4bec8-197">On the **Team** tab, you will see the new generic team member.</span></span> <span data-ttu-id="4bec8-198">请注意，其只有分派的工时数。</span><span class="sxs-lookup"><span data-stu-id="4bec8-198">Notice that it has only assigned hours.</span></span> <span data-ttu-id="4bec8-199">这些工时数是分派给通用团队成员的所有任务的工时数之和。</span><span class="sxs-lookup"><span data-stu-id="4bec8-199">These hours are the sum of all tasks that are assigned to the generic team member.</span></span> <span data-ttu-id="4bec8-200">通用团队成员还没有所需工时数或资源要求。</span><span class="sxs-lookup"><span data-stu-id="4bec8-200">The generic team member doesn't yet have required hours or a resource requirement.</span></span>

    ![“团队”选项卡上的通用团队成员](media/Resource-Management-image26.png)

5. <span data-ttu-id="4bec8-202">现在可以使用资源选取器将通用团队成员分派给其他任务。</span><span class="sxs-lookup"><span data-stu-id="4bec8-202">You can now assign the generic team member to other tasks by using the Resource Picker.</span></span>

    ![资源选取器中的通用团队成员](media/Resource-Management-image27.png)

    <span data-ttu-id="4bec8-204">将通用资源分派给任务后，可以为通用资源生成资源要求。</span><span class="sxs-lookup"><span data-stu-id="4bec8-204">When you've finished assigning the generic resource to tasks, you can generate a resource requirement for the generic resource.</span></span>

5. <span data-ttu-id="4bec8-205">在 **团队** 选项卡上，选择通用资源，然后选择 **生成要求** 。</span><span class="sxs-lookup"><span data-stu-id="4bec8-205">On the **Team** tab, select the generic resource, and then select **Generate Requirement**.</span></span>

    ![“生成要求”命令](media/Resource-Management-image28.png)

    <span data-ttu-id="4bec8-207">生成要求后，通用团队成员将有所需工时数，以及资源要求的链接。</span><span class="sxs-lookup"><span data-stu-id="4bec8-207">When the requirement is generated, the generic team member will have required hours and a link for the resource requirement.</span></span>

    ![“资源要求”链接](media/Resource-Management-image29.png)

    <span data-ttu-id="4bec8-209">预订指定资源之后，将从团队中删除通用资源，并替换为该指定资源。</span><span class="sxs-lookup"><span data-stu-id="4bec8-209">After you book a named resource, the generic resource is removed from the team and replaced by the named resource.</span></span>

    ![通用资源被替换为指定资源](media/Resource-Management-image30.png)

    <span data-ttu-id="4bec8-211">在 **计划** 选项卡上，将删除通用资源分派并替换为指定资源。</span><span class="sxs-lookup"><span data-stu-id="4bec8-211">On the **Schedule** tab, the generic resource assignments are removed and replaced by the named resource.</span></span>

    ![“计划”选项卡上的通用资源分派被替换为指定资源](media/Resource-Management-image31.png)

    > [!NOTE]
    > <span data-ttu-id="4bec8-213">仅当为通用资源要求预订满了某项指定资源时，才发生此行为。</span><span class="sxs-lookup"><span data-stu-id="4bec8-213">This behavior occurs only when a named resource is fully booked for the generic resource requirement.</span></span> <span data-ttu-id="4bec8-214">当一项指定资源部分取代通用资源要求或多项指定资源取代通用资源要求时，通用资源仍然分派给任务。</span><span class="sxs-lookup"><span data-stu-id="4bec8-214">When either a named resource partially replaces the generic resource requirement or multiple named resources replace the generic resource requirement, the generic resource remains assigned to the task.</span></span>

    <span data-ttu-id="4bec8-215">下图中，为一个 80 个工时的任务规划了五天的持续时间（五天内每天 16 小时），并将该任务分派给了名称为 **职能** 的通用资源。</span><span class="sxs-lookup"><span data-stu-id="4bec8-215">In the following illustration, an 80-hour task has been planned for a five-day duration (16 hours per day over five days) and assigned to the generic resource that is named **Functional**.</span></span>

    ![为“职能”通用资源分派了为期五天的八十个工时任务](media/Resource-Management-image32.png)

    <span data-ttu-id="4bec8-217">生成要求时，要求为五天内 80 个工时。</span><span class="sxs-lookup"><span data-stu-id="4bec8-217">When you generate the requirement, it's for 80 hours over five days.</span></span>

    ![为五天内 80 个工时生成的要求](media/Resource-Management-image33.png)

    <span data-ttu-id="4bec8-219">因为可用资源每天仅工作八小时，所以需要两项资源才能满足要求。</span><span class="sxs-lookup"><span data-stu-id="4bec8-219">Because available resources work only eight hours per day, two resources are needed to fulfill the requirement.</span></span>

    ![第二个资源](media/Resource-Management-image35.png)

    <span data-ttu-id="4bec8-221">在 **团队** 选项卡上，现在可以看到通用资源没有所需工时数，但是仍然显示分派的工时数和构成用于满足要求的两项指定资源。</span><span class="sxs-lookup"><span data-stu-id="4bec8-221">On the **Team** tab, you can now see that the generic resource has no required hours, but the assigned hours still appear together with the two named resources that make up the fulfillment.</span></span>

    ![“团队”选项卡上的两项指定资源](media/Resource-Management-image36.png)

    <span data-ttu-id="4bec8-223">在 **计划** 选项卡上，通用资源仍然分派给任务。</span><span class="sxs-lookup"><span data-stu-id="4bec8-223">On the **Schedule** tab, the generic resource remains assigned to the task.</span></span>

    ![“计划”选项卡上的通用资源](media/Resource-Management-image37.png)

<span data-ttu-id="4bec8-225">PSA 不能同时为任务分派两项资源，因为此行为将产生不太容易预测的计划。</span><span class="sxs-lookup"><span data-stu-id="4bec8-225">PSA doesn't assign both resources to the task, because that behavior would produce a less predictable schedule.</span></span> <span data-ttu-id="4bec8-226">在这个简单的示例中，可以将工时数轻松地平分给两项资源。</span><span class="sxs-lookup"><span data-stu-id="4bec8-226">In this simple example, it's easy to divide the hours equally between two resources.</span></span> <span data-ttu-id="4bec8-227">但是，在涉及多个任务和多项资源的更复杂方案中，PSA 必须假设应该如何将多项资源收到的预订分配给多项任务。</span><span class="sxs-lookup"><span data-stu-id="4bec8-227">However, in more complex scenarios that involve multiple tasks and multiple resources, PSA would have to make assumptions about how it should allocate the bookings that are received for multiple resources across multiple tasks.</span></span>

<span data-ttu-id="4bec8-228">因此，在这些方案中，项目经理应该分析多项预订并根据需要分派。</span><span class="sxs-lookup"><span data-stu-id="4bec8-228">Therefore, in these scenarios, the project manager is responsible for parsing the multiple bookings and assigning them as needed.</span></span> <span data-ttu-id="4bec8-229">为了分配预订，项目经理将通用资源的任务分派给指定资源，然后使用 **协调** 视图确保分派与预订可以协同工作。</span><span class="sxs-lookup"><span data-stu-id="4bec8-229">To allocate the bookings, the project manager assigns the tasks from the generic resources to the named resources and then uses the **Reconciliation** view to make sure that the allocation works with the bookings.</span></span>

### <a name="edit-a-resource-requirement"></a><span data-ttu-id="4bec8-230">编辑资源要求</span><span class="sxs-lookup"><span data-stu-id="4bec8-230">Edit a resource requirement</span></span>

<span data-ttu-id="4bec8-231">创建资源要求之后，项目经理或资源经理可能会希望编辑详细信息以优化使用日程安排板时的搜索条件。</span><span class="sxs-lookup"><span data-stu-id="4bec8-231">After a resource requirement has been created, a project manager or resource manager might want to edit the details to refine the search criteria when the Schedule Board is used.</span></span> <span data-ttu-id="4bec8-232">要编辑资源要求，请执行下列步骤。</span><span class="sxs-lookup"><span data-stu-id="4bec8-232">To edit the resource requirement, follow these steps.</span></span>

1. <span data-ttu-id="4bec8-233">在 **项目** 页的 **团队** 选项卡上，选择通用资源的任何要求的链接。</span><span class="sxs-lookup"><span data-stu-id="4bec8-233">On the **Projects** page, on the **Team** tab, select the link to any requirement on a generic resource.</span></span>
2. <span data-ttu-id="4bec8-234">在显示的 **资源要求** 页上，可以更新多个属性。</span><span class="sxs-lookup"><span data-stu-id="4bec8-234">On the **Resource Requirement** page that appears, you can update several attributes.</span></span> <span data-ttu-id="4bec8-235">以下是一些示例：</span><span class="sxs-lookup"><span data-stu-id="4bec8-235">Here are some examples:</span></span>

    - <span data-ttu-id="4bec8-236">姓名</span><span class="sxs-lookup"><span data-stu-id="4bec8-236">Name</span></span>
    - <span data-ttu-id="4bec8-237">起始日期</span><span class="sxs-lookup"><span data-stu-id="4bec8-237">From Date</span></span>
    - <span data-ttu-id="4bec8-238">截止日期</span><span class="sxs-lookup"><span data-stu-id="4bec8-238">To Date</span></span>
    - <span data-ttu-id="4bec8-239">持续时间</span><span class="sxs-lookup"><span data-stu-id="4bec8-239">Duration</span></span>
    - <span data-ttu-id="4bec8-240">资源类型</span><span class="sxs-lookup"><span data-stu-id="4bec8-240">Resource Type</span></span>

<span data-ttu-id="4bec8-241">在 **资源要求** 页上，项目经理或资源经理也可以定义以下信息：</span><span class="sxs-lookup"><span data-stu-id="4bec8-241">On the **Resource Requirement** page, the project manager or resource manager can also define the following information:</span></span>

- <span data-ttu-id="4bec8-242">技能</span><span class="sxs-lookup"><span data-stu-id="4bec8-242">Skills</span></span>
- <span data-ttu-id="4bec8-243">角色</span><span class="sxs-lookup"><span data-stu-id="4bec8-243">Roles</span></span>
- <span data-ttu-id="4bec8-244">资源首选项</span><span class="sxs-lookup"><span data-stu-id="4bec8-244">Resource preferences</span></span>
- <span data-ttu-id="4bec8-245">首选部门</span><span class="sxs-lookup"><span data-stu-id="4bec8-245">Preferred organizational unit</span></span>

### <a name="update-resource-bookings-after-they-are-booked-on-a-project"></a><span data-ttu-id="4bec8-246">更新已预订给项目的资源的预订</span><span class="sxs-lookup"><span data-stu-id="4bec8-246">Update resource bookings after they are booked on a project</span></span>

<span data-ttu-id="4bec8-247">将通用资源或指定资源添加到项目团队之后，可以更改该资源的预订。</span><span class="sxs-lookup"><span data-stu-id="4bec8-247">After you've added a generic or named resource to a project team, you can change the resource's bookings.</span></span>

1. <span data-ttu-id="4bec8-248">在 **项目** 页的 **团队** 选项卡上，选择一个团队成员，然后选择 **维护预订** 。</span><span class="sxs-lookup"><span data-stu-id="4bec8-248">On the **Projects** page, on the **Team** tab, select a team member, and then select **Maintain Bookings**.</span></span>

    ![为所选团队成员打开了日程安排板](media/Resource-Management-image40.png)

    <span data-ttu-id="4bec8-250">将显示日程安排板，其中显示项目团队成员的预订。</span><span class="sxs-lookup"><span data-stu-id="4bec8-250">The Schedule Board appears and shows the project team member's bookings.</span></span> <span data-ttu-id="4bec8-251">展开该团队成员的记录以查看已经为此项目和占用该团队成员产能的其他项目预订的工时数。</span><span class="sxs-lookup"><span data-stu-id="4bec8-251">Expand the team member's record to view the hours that have been booked against this project and other projects that are consuming the team member's capacity.</span></span>

2. <span data-ttu-id="4bec8-252">选择预订并拖动以延长或缩短该预订。</span><span class="sxs-lookup"><span data-stu-id="4bec8-252">Select and drag the booking to extend or shorten it.</span></span> <span data-ttu-id="4bec8-253">将显示 **创建资源预订** 对话框，供您调整预订。</span><span class="sxs-lookup"><span data-stu-id="4bec8-253">A **Create Resource Booking** dialog box appears that lets you adjust the booking.</span></span>

    ![“创建资源预订”对话框](media/Resource-Management-image41.png)

3. <span data-ttu-id="4bec8-255">右键单击预订。</span><span class="sxs-lookup"><span data-stu-id="4bec8-255">Right-click the booking.</span></span> <span data-ttu-id="4bec8-256">然后可以使用快捷方式菜单完成以下操作：</span><span class="sxs-lookup"><span data-stu-id="4bec8-256">You can then use the shortcut menu to complete the following actions:</span></span>

    - <span data-ttu-id="4bec8-257">预订更改状态。</span><span class="sxs-lookup"><span data-stu-id="4bec8-257">Change the booking status.</span></span>
    - <span data-ttu-id="4bec8-258">编辑预订。</span><span class="sxs-lookup"><span data-stu-id="4bec8-258">Edit the booking.</span></span>
    - <span data-ttu-id="4bec8-259">替代项目团队中的资源。</span><span class="sxs-lookup"><span data-stu-id="4bec8-259">Substitute a resource on the project team.</span></span>

### <a name="change-the-booking-status"></a><span data-ttu-id="4bec8-260">预订更改状态</span><span class="sxs-lookup"><span data-stu-id="4bec8-260">Change the booking status</span></span>

<span data-ttu-id="4bec8-261">可以更改任何默认或自定义预订状态。</span><span class="sxs-lookup"><span data-stu-id="4bec8-261">You can change any default or custom booking status.</span></span>

![“更改状态”命令](media/Resource-Management-image42.png)

<span data-ttu-id="4bec8-263">PSA 中有以下状态：</span><span class="sxs-lookup"><span data-stu-id="4bec8-263">The following statuses are included in PSA:</span></span>

- <span data-ttu-id="4bec8-264">**已取消** – 此状态取消资源的预订并释放该资源的产能。</span><span class="sxs-lookup"><span data-stu-id="4bec8-264">**Canceled** – This status cancels a resource's booking and frees up the resource's capacity.</span></span>
- <span data-ttu-id="4bec8-265">**硬预订** – 此状态占用资源的产能。</span><span class="sxs-lookup"><span data-stu-id="4bec8-265">**Hard Book** – This status consumes a resource's capacity.</span></span> <span data-ttu-id="4bec8-266">如果从 **项目** 页 **所有团队成员** 网格打开 **维护预订** ，预订通常有此状态。</span><span class="sxs-lookup"><span data-stu-id="4bec8-266">A booking typically has this status when you open **Maintain Bookings** from the **All Team Members** grid on the **Projects** page.</span></span>
- <span data-ttu-id="4bec8-267">**软预订** – 此状态将资源添加到团队，但是不占用该资源的产能。</span><span class="sxs-lookup"><span data-stu-id="4bec8-267">**Soft Book** – This status adds a resource to a team but doesn't consume the resource's capacity.</span></span> <span data-ttu-id="4bec8-268">它指示将该资源保留给了潜在工作，但是如果其他作业需要，该资源仍然有产能。</span><span class="sxs-lookup"><span data-stu-id="4bec8-268">It indicates that the resource has been reserved for potential work but still has capacity if it's needed on other jobs.</span></span> <span data-ttu-id="4bec8-269">在整体资源可用性视图中，软预订的状态与硬预订的不同。</span><span class="sxs-lookup"><span data-stu-id="4bec8-269">In the view of overall resource availability, soft bookings have a different status than hard bookings.</span></span>
- <span data-ttu-id="4bec8-270">**已建议** – 此状态表示资源经理或项目经理对资源的建议。</span><span class="sxs-lookup"><span data-stu-id="4bec8-270">**Proposed** – This status represents a resource manager's or project manager's proposal for a resource.</span></span> <span data-ttu-id="4bec8-271">建议不占用资源的产能，不会将资源添加到项目团队。</span><span class="sxs-lookup"><span data-stu-id="4bec8-271">Proposals don't consume the capacity of a resource, and the resource isn't added to the project team.</span></span> <span data-ttu-id="4bec8-272">若要为团队硬预订资源，项目经理必须接受建议。</span><span class="sxs-lookup"><span data-stu-id="4bec8-272">To hard-book the resource on the team, the project manager must accept the proposal.</span></span>

### <a name="submit-resource-requests"></a><span data-ttu-id="4bec8-273">提交资源请求</span><span class="sxs-lookup"><span data-stu-id="4bec8-273">Submit resource requests</span></span>

<span data-ttu-id="4bec8-274">资源要求用于传递资源经理必须满足的需求（资源要求）。</span><span class="sxs-lookup"><span data-stu-id="4bec8-274">Resource requests are used to carry the demand (resource requirement) that must be fulfilled by a resource manager.</span></span> <span data-ttu-id="4bec8-275">对于已经属于团队的通用资源，可以直接提交资源请求。</span><span class="sxs-lookup"><span data-stu-id="4bec8-275">For a generic resource that is already on the team, you can submit a resource request directly.</span></span> <span data-ttu-id="4bec8-276">可以通过两种方法满足资源请求：</span><span class="sxs-lookup"><span data-stu-id="4bec8-276">A resource request can be fulfilled in two ways:</span></span>

- <span data-ttu-id="4bec8-277">资源经理直接满足请求。</span><span class="sxs-lookup"><span data-stu-id="4bec8-277">The resource manager directly fulfills the request.</span></span> <span data-ttu-id="4bec8-278">在此情况下，将把通用资源替换为具有指定资源的硬预订。</span><span class="sxs-lookup"><span data-stu-id="4bec8-278">In this case, the generic resource is replaced by a hard booking that has a named resource.</span></span>
- <span data-ttu-id="4bec8-279">资源经理向项目经理建议资源，而项目经理则批准或拒绝建议的资源。</span><span class="sxs-lookup"><span data-stu-id="4bec8-279">The resource manager proposes a resource to the project manager, and the project manager approves or rejects the proposed resource.</span></span>

#### <a name="direct-fulfillment-of-resource-requests"></a><span data-ttu-id="4bec8-280">直接满足资源请求</span><span class="sxs-lookup"><span data-stu-id="4bec8-280">Direct fulfillment of resource requests</span></span>

<span data-ttu-id="4bec8-281">生成资源要求时，项目经理可提交对通用资源的资源请求，方法是选择资源，然后选择 **提交请求** 。</span><span class="sxs-lookup"><span data-stu-id="4bec8-281">When a resource requirement is generated, a project manager can submit a resource request for a generic resource by selecting the resource and then selecting **Submit Request**.</span></span>

![“提交请求”按钮](media/Resource-Management-image45.png)

<span data-ttu-id="4bec8-283">可以向要满足请求的资源经理提供有关资源的注释。</span><span class="sxs-lookup"><span data-stu-id="4bec8-283">Comments about the resource can be provided to the resource manager who is fulfilling the request.</span></span> <span data-ttu-id="4bec8-284">提交请求之后，团队成员的 **状态** 字段将变为 **已提交** 。</span><span class="sxs-lookup"><span data-stu-id="4bec8-284">After the request is submitted, the **Status** field for the team member is changed to **Submitted**.</span></span>

![输入可选注释](media/Resource-Management-image46.png)

<span data-ttu-id="4bec8-286">当资源经理满足请求时， **所有团队成员** 网格中将把通用团队成员替换为指定资源。</span><span class="sxs-lookup"><span data-stu-id="4bec8-286">When the resource manager fulfills the request, the generic team member is replaced by the named resource in the **All Team Members** grid.</span></span>

![“所有团队成员”网格中通用团队成员已替换为指定资源](media/Resource-Management-image47.png)

#### <a name="use-a-resource-proposal-for-resource-requests"></a><span data-ttu-id="4bec8-288">对资源请求使用资源建议</span><span class="sxs-lookup"><span data-stu-id="4bec8-288">Use a resource proposal for resource requests</span></span>

<span data-ttu-id="4bec8-289">资源经理可以直接向项目经理建议资源，而不是直接为资源请求预订资源。</span><span class="sxs-lookup"><span data-stu-id="4bec8-289">Instead of directly booking a resource on a resource request, a resource manager can propose a resource to the project manager.</span></span> <span data-ttu-id="4bec8-290">如果没有要求的精确匹配项，资源经理可以使用此选项。</span><span class="sxs-lookup"><span data-stu-id="4bec8-290">A resource manager might use this option when an exact match for the requirements isn't available.</span></span> <span data-ttu-id="4bec8-291">当资源经理建议资源时，项目经理将发现通用团队成员的 **状态** 字段已更改为 **需要审阅** 。</span><span class="sxs-lookup"><span data-stu-id="4bec8-291">When a resource manager proposes a resource, the project manager sees that the **Status** field for the generic team member is changed to **Needs Review**.</span></span>

![通用团队成员的状态已更改为“需要审阅”](media/Resource-Management-image48.png)

<span data-ttu-id="4bec8-293">若要查看建议的资源和资源的预订影响可视性表示，请双击状态为 **需要审阅** 的团队成员。</span><span class="sxs-lookup"><span data-stu-id="4bec8-293">To view the proposed resource together with a visualization of the effect of the proposal's booking, double-click the team member that has a status of **Needs Review**.</span></span> <span data-ttu-id="4bec8-294">然后选择 **建议资源** 选项卡。</span><span class="sxs-lookup"><span data-stu-id="4bec8-294">Then select the **Proposed Resources** tab.</span></span>

![“建议资源”选项卡](media/Resource-Management-image49.png)

<span data-ttu-id="4bec8-296">选择 **接受所有建议** 以接受所有建议资源，或选择 **拒绝所有建议** 以拒绝这些资源。</span><span class="sxs-lookup"><span data-stu-id="4bec8-296">Select **Accept All Proposals** to accept all proposed resources or **Reject All Proposals** to reject them.</span></span> <span data-ttu-id="4bec8-297">如果接受建议资源，将在把这些资源硬预订为项目的团队成员，并替换通用资源。</span><span class="sxs-lookup"><span data-stu-id="4bec8-297">If you accept the proposed resources, they are hard-booked on the project as team members and replace the generic resources.</span></span>

> [!NOTE]
> <span data-ttu-id="4bec8-298">必须接受或拒绝所有建议资源。</span><span class="sxs-lookup"><span data-stu-id="4bec8-298">You must either accept or reject all proposed resources.</span></span> <span data-ttu-id="4bec8-299">不能部分接受或拒绝。</span><span class="sxs-lookup"><span data-stu-id="4bec8-299">You can't partially accept or reject them.</span></span>

### <a name="substitute-a-resource-on-the-project-team"></a><span data-ttu-id="4bec8-300">替代项目团队中的资源</span><span class="sxs-lookup"><span data-stu-id="4bec8-300">Substitute a resource on the project team</span></span>

<span data-ttu-id="4bec8-301">有时，项目经理必须替代为项目预订的某个团队成员。</span><span class="sxs-lookup"><span data-stu-id="4bec8-301">Sometimes, a project manager must substitute a booked team member on a project.</span></span>

1. <span data-ttu-id="4bec8-302">在 **项目** 页的 **团队** 选项卡上，选择需要替代的资源，然后选择 **维护预订** 。</span><span class="sxs-lookup"><span data-stu-id="4bec8-302">On the **Projects** page, on the **Team** tab, select the resource that needs a substitute, and then select **Maintain Bookings**.</span></span>
2. <span data-ttu-id="4bec8-303">展开该资源以查看将其分派给的项目。</span><span class="sxs-lookup"><span data-stu-id="4bec8-303">Expand the resource to view the projects that it's assigned to.</span></span>

    ![资源已展开并显示分配给的项目](media/Resource-Management-image50.png)

3. <span data-ttu-id="4bec8-305">右键单击该项目，然后选择 **替代资源** 。</span><span class="sxs-lookup"><span data-stu-id="4bec8-305">Right-click the project, and then select **Substitute Resource**.</span></span>
4. <span data-ttu-id="4bec8-306">如果知道要用于替代当前资源的资源，请选择或键入名称，然后选择 **重新分派** 。</span><span class="sxs-lookup"><span data-stu-id="4bec8-306">If you know the resource that you want to substitute for the current resource, select or type the name, and then select **Re-assign**.</span></span>

    ![指定替代资源](media/Resource-Management-image51.png)

    <span data-ttu-id="4bec8-308">也可以执行以下步骤搜索资源：</span><span class="sxs-lookup"><span data-stu-id="4bec8-308">Alternatively, follow these steps to search for a resource:</span></span>

    1. <span data-ttu-id="4bec8-309">选择 **查找替代项** 。</span><span class="sxs-lookup"><span data-stu-id="4bec8-309">Select **Find Substitution**.</span></span>

        ![搜索替代资源](media/Resource-Management-image52.png)

        <span data-ttu-id="4bec8-311">日程安排助理将返回可用替代项列表。</span><span class="sxs-lookup"><span data-stu-id="4bec8-311">The Schedule Assistant returns a list of available substitutes.</span></span> <span data-ttu-id="4bec8-312">在日程安排助理中，可以进一步筛选可用资源以查找适合的替代项。</span><span class="sxs-lookup"><span data-stu-id="4bec8-312">In the Schedule Assistant, you can further filter the available resources to find a suitable substitute.</span></span>

        ![可用替代项列表](media/Resource-Management-image53.png)

    2. <span data-ttu-id="4bec8-314">若要替代资源，请选择所需资源，然后选择 **替代** 。</span><span class="sxs-lookup"><span data-stu-id="4bec8-314">To substitute the resource, select the resource that you want, and then select **Substitute**.</span></span>

        ![已选择替代资源](media/Resource-Management-image54.png)

    <span data-ttu-id="4bec8-316">将把预订和分派替代为新资源。</span><span class="sxs-lookup"><span data-stu-id="4bec8-316">The bookings and assignments are substituted with the new resource.</span></span>

    ![预订和分派已替代为新资源](media/Resource-Management-image55.png)

## <a name="reconcile-team-member-bookings-and-assignments"></a><span data-ttu-id="4bec8-318">协调团队成员预订和分派</span><span class="sxs-lookup"><span data-stu-id="4bec8-318">Reconcile team member bookings and assignments</span></span>

<span data-ttu-id="4bec8-319">团队成员的预订和分派之间关系不紧密。</span><span class="sxs-lookup"><span data-stu-id="4bec8-319">For team members, bookings and assignments are loosely coupled.</span></span> <span data-ttu-id="4bec8-320">换句话说，资源可以有分派但无预订，也可以有预订但无分派。</span><span class="sxs-lookup"><span data-stu-id="4bec8-320">In other words, resources can have assignments but no bookings, or they can have bookings but no assignments.</span></span> <span data-ttu-id="4bec8-321">理想情况下，预订和分派应一致，这样资源就可以落实产能以执行任务分派。</span><span class="sxs-lookup"><span data-stu-id="4bec8-321">Ideally, bookings and assignments should be aligned, so that resources have committed capacity to perform the task assignments.</span></span> <span data-ttu-id="4bec8-322">但是，预订可能基于可用性，而任务的时间安排可能会随着项目的进行而改变。</span><span class="sxs-lookup"><span data-stu-id="4bec8-322">However, the bookings might be based on availability, and task timings might change as the project continues.</span></span> <span data-ttu-id="4bec8-323">因此，预订和分派之间的这种松散关系可以为您提供灵活的选择。</span><span class="sxs-lookup"><span data-stu-id="4bec8-323">Therefore, the loose coupling of bookings and assignments provides flexibility.</span></span>

<span data-ttu-id="4bec8-324">PSA 中有一个 **协调** 选项卡，可供项目经理在项目团队中协调项目成员的预订及其分派。</span><span class="sxs-lookup"><span data-stu-id="4bec8-324">PSA has a **Reconciliation** tab that lets project managers reconcile team members' bookings and their assignments for project teams.</span></span>

![“协调”选项卡](media/Resource-Management-image56.png)

<span data-ttu-id="4bec8-326">**协调** 选项卡显示深入到每个成员的单个任务分派级别的预订和分派。</span><span class="sxs-lookup"><span data-stu-id="4bec8-326">The **Reconciliation** tab shows bookings and assignments down to the level of the individual task assignment for each team member.</span></span> <span data-ttu-id="4bec8-327">它通过单元格显示可表示时间段（从数月到数天）的工时。</span><span class="sxs-lookup"><span data-stu-id="4bec8-327">It shows hours in cells that represent time periods from months down to days.</span></span>

<span data-ttu-id="4bec8-328">此选项卡还使用总额列显示项目的整体净总额。</span><span class="sxs-lookup"><span data-stu-id="4bec8-328">The tab also shows an overall net total for the project, together with a total column.</span></span>

<span data-ttu-id="4bec8-329">对于每个资源，此选项卡计算团队成员的预订与团队成员任务分派汇总之差。</span><span class="sxs-lookup"><span data-stu-id="4bec8-329">For each resource, the tab calculates the difference between the team member's bookings and a rollup of the team member's task assignments.</span></span> <span data-ttu-id="4bec8-330">理想情况下，此差应该为 0（零）。</span><span class="sxs-lookup"><span data-stu-id="4bec8-330">Ideally, this difference should be 0 (zero).</span></span> <span data-ttu-id="4bec8-331">换句话说，预订与分派之间应该无差额。</span><span class="sxs-lookup"><span data-stu-id="4bec8-331">In other words, there should be no difference between bookings and assignments.</span></span> <span data-ttu-id="4bec8-332">将为差额着色并添加阴影，以便您注意以下两种情况：</span><span class="sxs-lookup"><span data-stu-id="4bec8-332">Differences are colored and shaded to draw attention to two conditions:</span></span>

- <span data-ttu-id="4bec8-333">**预订不足** - 资源的分派比预订的多时，发生预订不足。</span><span class="sxs-lookup"><span data-stu-id="4bec8-333">**Booking shortage** – A booking shortage occurs when a resource has more assignments than bookings.</span></span> <span data-ttu-id="4bec8-334">因为尚未保留此产能，所以项目经理可能希望解决这个问题，方法是扩展资源的预订以弥补不足额。</span><span class="sxs-lookup"><span data-stu-id="4bec8-334">Because this capacity hasn't been reserved, a project manager might want to correct this condition by extending the resource's bookings to cover the deficit.</span></span>
- <span data-ttu-id="4bec8-335">**超出预订** – 当已经将某个资源预订给项目，但是尚未将其分派给任务时，发生超出预订。</span><span class="sxs-lookup"><span data-stu-id="4bec8-335">**Excess bookings** – Excess bookings occur when a resource has been booked to the project but hasn't been assigned to tasks.</span></span> <span data-ttu-id="4bec8-336">如果资源是在进行任务分派之前为项目预订的，则可以接受这种情况。</span><span class="sxs-lookup"><span data-stu-id="4bec8-336">This condition might be acceptable in the cases where the resource was booked to the project before task assignment occurred.</span></span> <span data-ttu-id="4bec8-337">但是，如果是其他情况，则不会计划把资源分派给任务。</span><span class="sxs-lookup"><span data-stu-id="4bec8-337">However, in other cases, the resource isn't planned to be assigned to tasks.</span></span> <span data-ttu-id="4bec8-338">在这些情况下，项目经理应该考虑取消资源的预订，以便将产能用于其他项目。</span><span class="sxs-lookup"><span data-stu-id="4bec8-338">In these cases, the project manager should consider canceling the resource's bookings, so that the capacity can be used for another project.</span></span>

<span data-ttu-id="4bec8-339">在某些情况下，在高于天的级别（如月级别）查看时间时，可能会发现资源的净差额为零（换句话说，预订 = 分派）。</span><span class="sxs-lookup"><span data-stu-id="4bec8-339">In some cases, when you view time at a higher level than the day level (for example, the month level), you might see a net difference of zero for a resource (in other words, bookings = assignments).</span></span> <span data-ttu-id="4bec8-340">但是，如果在周级别查看时间，可能会发现第一周的分派为零小时，预订为 40 小时，但是第二周的分派为 40 小时，预订为零小时。</span><span class="sxs-lookup"><span data-stu-id="4bec8-340">However, if you view time at the week level, you might see that there are assignments of zero hours and bookings of 40 hours in the first week, but assignments of 40 hours and bookings of zero hours in the second week.</span></span> <span data-ttu-id="4bec8-341">总体而言，已协调预订和分派，但是一周与下一周不同。</span><span class="sxs-lookup"><span data-stu-id="4bec8-341">Overall, the bookings and assignments are reconciled, but they differ from one week to the next.</span></span>

<span data-ttu-id="4bec8-342">在更高级别查看时间时， **协调** 选项卡中的单元格有一个指示器，用于说明较低级别存在差额。</span><span class="sxs-lookup"><span data-stu-id="4bec8-342">When you view time at higher levels, cells in the **Reconciliation** tab have an indicator to inform you that there are differences at lower levels.</span></span> <span data-ttu-id="4bec8-343">可通过在单元格中双击进行放大来查看差额。</span><span class="sxs-lookup"><span data-stu-id="4bec8-343">By double-clicking in a cell, you can zoom in to view the difference.</span></span> <span data-ttu-id="4bec8-344">然后可以右键单击进行缩小。通过选择资源，然后使用网格工具栏上的 **下一个差异** 控件，可以转到该资源的订阅与分派之间的下一个差额。</span><span class="sxs-lookup"><span data-stu-id="4bec8-344">You can then right-click to zoom out. By selecting a resource and then using the **Next difference** control on the grid toolbar, you can go to the next difference between bookings and assignments for that resource.</span></span> <span data-ttu-id="4bec8-345">然后可以使用 **上一个差异** 控件后退。</span><span class="sxs-lookup"><span data-stu-id="4bec8-345">You can then use the **Previous difference** control to go back.</span></span> <span data-ttu-id="4bec8-346">也可以在 **设置** 下关闭差额指示器和导航行为。</span><span class="sxs-lookup"><span data-stu-id="4bec8-346">You can also turn off the difference indicator and navigation behavior under **Settings**.</span></span>

![差额指示器](media/Resource-Management-image57.png)

<span data-ttu-id="4bec8-348">如果某个资源有任务分派，但是无预订，请在 **项目** 页的 **协调** 选项卡上选择预订不足，然后选择 **扩展预订** 。</span><span class="sxs-lookup"><span data-stu-id="4bec8-348">If you have task assignments for a resource but no bookings, on the **Projects** page, on the **Reconciliation** tab, select the booking shortage, and then select **Extend Booking**.</span></span> <span data-ttu-id="4bec8-349">将显示 **扩展预订** 对话框，其中显示需要来解决资源不足的预订。</span><span class="sxs-lookup"><span data-stu-id="4bec8-349">The **Extend Booking** dialog box appears and shows the booking that is needed to address the resource's shortage.</span></span> <span data-ttu-id="4bec8-350">还显示该资源在所有项目或其他可计划实体中的现有预订。</span><span class="sxs-lookup"><span data-stu-id="4bec8-350">It also shows the resource's existing bookings across all projects or other schedulable entities.</span></span> <span data-ttu-id="4bec8-351">如果选择 **确定** 为资源创建预订，无论该资源是否可用，都可能导致超额预订。</span><span class="sxs-lookup"><span data-stu-id="4bec8-351">If you select **OK** to create the booking for the resource, regardless of that resource's availability, you might cause overbooking.</span></span>

![“扩展预订”对话框](media/Resource-Management-image58.png)

<span data-ttu-id="4bec8-353">然后，项目经理或资源经理可使用日程安排板管理资源超额预订超过其产能的任何情况。</span><span class="sxs-lookup"><span data-stu-id="4bec8-353">The project manager or resource manager can then use the Schedule Board to manage any situations where a resource is overbooked beyond its capacity.</span></span>
