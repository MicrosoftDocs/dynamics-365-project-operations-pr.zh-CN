---
title: 升级注意事项 - Microsoft Dynamics 365 Project Service Automation 版本 2.x 或 1.x 到版本 3
description: 此主题介绍从 Project Service Automation 版本 2.x 或 1.x 升级到版本 3 时必须考虑的注意事项。
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 11/13/2018
ms.topic: article
author: JohnPBurrows
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: 19d6d312c7cedd2d7b9b5649452b85dd24fae761
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/16/2020
ms.locfileid: "4072684"
---
# <a name="upgrade-considerations---psa-version-2x-or-1x-to-version-3"></a><span data-ttu-id="77043-103">升级注意事项 - PSA 版本 2.x 或 1.x 到版本 3.x</span><span class="sxs-lookup"><span data-stu-id="77043-103">Upgrade considerations - PSA version 2.x or 1.x to version 3</span></span>
[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

## <a name="project-service-automation-and-field-service"></a><span data-ttu-id="77043-104">Project Service Automation 和 Field Service</span><span class="sxs-lookup"><span data-stu-id="77043-104">Project Service Automation and Field Service</span></span>
<span data-ttu-id="77043-105">Dynamics 365 Project Service Automation 和 Dynamics 365 Field Service 都使用 Universal Resourcing Scheduling (URS) 解决方案计划资源。</span><span class="sxs-lookup"><span data-stu-id="77043-105">Both Dynamics 365 Project Service Automation and Dynamics 365 Field Service use the Universal Resourcing Scheduling (URS) solution for resource scheduling.</span></span> <span data-ttu-id="77043-106">如果您的实例中同时具有 Project Service Automation 和 Field Service，则应该计划将这两个解决方案升级到最新版本（Project Service Automation 版本 3.x 和 Field Service 版本 8.x）。</span><span class="sxs-lookup"><span data-stu-id="77043-106">If you have both Project Service Automation and Field Service in your instance, you should plan on upgrading both solutions to the latest version (version 3.x for Project Service Automation, version 8.x for Field Service).</span></span> <span data-ttu-id="77043-107">升级 Project Service Automation 或 Field Service 将安装最新版本的 URS，这意味着如果不将同一个实例中的 Project Service Automation 和 Field Service 解决方案都升级到最新版本，行为可能会不一致。</span><span class="sxs-lookup"><span data-stu-id="77043-107">Upgrading Project Service Automation or Field Service will install the latest version of URS, which means that inconsistent behavior is possible if both Project Service Automation and Field Service solutions in the same instance aren’t upgraded to the latest version.</span></span>

## <a name="resource-assignments"></a><span data-ttu-id="77043-108">资源分派</span><span class="sxs-lookup"><span data-stu-id="77043-108">Resource assignments</span></span>
<span data-ttu-id="77043-109">在 Project Service Automation 版本 2 和版本 1 中，任务分派作为子任务（也称为明细任务）存储在 **任务实体** 中，并直接与 **资源分派** 实体关联。</span><span class="sxs-lookup"><span data-stu-id="77043-109">In Project Service Automation version 2 and version 1, task assignments were stored as child tasks (also called line tasks) in the **Task entity** , and indirectly related to the **Resource Assignment** entity.</span></span> <span data-ttu-id="77043-110">明细任务在工作分解结构 (WBS) 中的任务分派弹出窗口中显示。</span><span class="sxs-lookup"><span data-stu-id="77043-110">The line task was visible in the assignment pop-up window on the Work Breakdown Structure (WBS).</span></span>

![Project Service Automation 版本 2 和版本 1 中 WBS 上的明细任务](media/upgrade-line-task-01.png)

<span data-ttu-id="77043-112">在 Project Service Automation 版本 3 中，已更改了将可预订资源分派给任务时采用的基础架构。</span><span class="sxs-lookup"><span data-stu-id="77043-112">In version 3 of Project Service Automation, the underlying schema of assigning bookable resources to tasks has changed.</span></span> <span data-ttu-id="77043-113">明细任务已弃用， **任务实体** 中的任务与 **资源分派** 视图中的团队成员之间存在直接的 1:1 关系。</span><span class="sxs-lookup"><span data-stu-id="77043-113">The line task has been deprecated and there is a direct 1:1 relationship between the task in the **Task entity** and the team member in the **Resource Assignment** entity.</span></span> <span data-ttu-id="77043-114">分派给项目团队成员的任务现在直接存储在资源分派实体中。</span><span class="sxs-lookup"><span data-stu-id="77043-114">Tasks that are assigned to a project team member are now stored directly in the Resource Assignment entity.</span></span>  

<span data-ttu-id="77043-115">这些更改影响项目团队中具有指定可预订资源和通用资源的资源分派的所有现有项目的升级。</span><span class="sxs-lookup"><span data-stu-id="77043-115">These changes impact the upgrade of any existing projects that have resource assignments for named bookable resources and generic resources on a project team.</span></span> <span data-ttu-id="77043-116">此主题提供升级到版本 3 时需要对项目注意的事项。</span><span class="sxs-lookup"><span data-stu-id="77043-116">This topic provides the considerations that you will need to take into account for your projects when you upgrade to version 3.</span></span> 

### <a name="tasks-assigned-to-named-resources"></a><span data-ttu-id="77043-117">任务分派给指定资源</span><span class="sxs-lookup"><span data-stu-id="77043-117">Tasks assigned to named resources</span></span>
<span data-ttu-id="77043-118">如果使用基础任务实体，则版本 2 和版本 1 中的任务允许团队成员扮演非默认为其定义的角色。</span><span class="sxs-lookup"><span data-stu-id="77043-118">Using the underlying task entity, tasks in version 2 and version 1 allowed team members to portray a role other than their default defined role.</span></span> <span data-ttu-id="77043-119">例如，为康辉默认分派的角色为项目经理，但可以将她分派给需要开发人员角色的任务。</span><span class="sxs-lookup"><span data-stu-id="77043-119">For example, Gracie George, who’s by default assigned the role of Program Manager, could be assigned to a task with the role of Developer.</span></span> <span data-ttu-id="77043-120">在版本 3 中，指定团队成员的角色始终为默认角色，所以为康辉分派的所有角色都使用她的默认角色，即项目经理。</span><span class="sxs-lookup"><span data-stu-id="77043-120">In version 3, the role of a named team member is always the default, so any task that Gracie George is assigned to uses her default role of Program Manager.</span></span>

<span data-ttu-id="77043-121">如果已经在版本 2 和版本 1 中将资源分派给了需要非其默认角色的任务，在您升级时，将为该指定资源分派所有任务分派的默认角色，无论版本 2 中的角色分派是怎样的。</span><span class="sxs-lookup"><span data-stu-id="77043-121">If you have assigned a resource to a task outside of their default role in version 2 and version 1, when you upgrade, the named resource will be assigned the default role for all task assignments, regardless of role assignment in version 2.</span></span> <span data-ttu-id="77043-122">则会导致计算出的估算在版本 2 或版本 1 与版本 3 之间存在差异，因为计算估算时基于资源的角色，而不是基于明细任务分派。</span><span class="sxs-lookup"><span data-stu-id="77043-122">This will result in differences in the calculated estimates from version 2 or version 1 to version 3 because estimates are calculated based on the role of the resource and not the line task assignment.</span></span> <span data-ttu-id="77043-123">例如，在版本 2 中，为候婵分派了两个任务。</span><span class="sxs-lookup"><span data-stu-id="77043-123">For example, in version 2, two tasks have been assigned to Ashley Chinn.</span></span> <span data-ttu-id="77043-124">任务 1 的明细任务的角色为开发人员，任务 2 的角色为项目经理。</span><span class="sxs-lookup"><span data-stu-id="77043-124">The role on the line task for task 1 is Developer and for task 2, Program Manager.</span></span> <span data-ttu-id="77043-125">候婵的默认角色为项目经理。</span><span class="sxs-lookup"><span data-stu-id="77043-125">Ashley Chinn has the default role of Program Manager.</span></span>

![为一项资源分派了多个角色](media/upgrade-multiple-roles-02.png)

<span data-ttu-id="77043-127">因为开发人员角色和项目经理角色不同，所以成本和销售额估算计算方法如下：</span><span class="sxs-lookup"><span data-stu-id="77043-127">Because the roles of Developer and Program Manager differ, the cost and sales estimates are as follows:</span></span>

![资源角色的成本估算](media/upggrade-cost-estimates-03.png)

![资源角色的销售额估算](media/upgrade-sales-estimates-04.png)

<span data-ttu-id="77043-130">升级到版本 3 时，明细任务替换为可预订资源团队成员的任务资源分派。</span><span class="sxs-lookup"><span data-stu-id="77043-130">When you upgrade to version 3, line tasks are replaced with resource assignments on the task of the bookable resource team member.</span></span> <span data-ttu-id="77043-131">此分派使用可预订资源的默认角色。</span><span class="sxs-lookup"><span data-stu-id="77043-131">The assignment will use the default role of the bookable resource.</span></span> <span data-ttu-id="77043-132">下图中，资源是角色为项目经理的候婵。</span><span class="sxs-lookup"><span data-stu-id="77043-132">In the following graphic, Ashley Chinn who has a role of Program Manager, is the resource.</span></span>

![资源分派](media/resource-assignment-v2-05.png)

<span data-ttu-id="77043-134">因为估算基于资源的默认角色，所以销售额和成本估算可能改变。</span><span class="sxs-lookup"><span data-stu-id="77043-134">Because the estimates are based on the default role for the resource, the sales and cost estimates may change.</span></span> <span data-ttu-id="77043-135">请注意，下图中不再看到 **开发人员** 角色，因为该角色现在取自可预订资源的默认角色。</span><span class="sxs-lookup"><span data-stu-id="77043-135">Note that in the following graphic, you no longer see the **Developer** role as the role is now taken from the bookable resource’s default role.</span></span>

<span data-ttu-id="77043-136">![默认角色的成本估算](media/resource-assignment-cost-estimate-06.png)
![默认数据的销售额估算](media/resource-assignment-sales-estimate-07.png)</span><span class="sxs-lookup"><span data-stu-id="77043-136">![Cost estimates for default roles](media/resource-assignment-cost-estimate-06.png)
![Sales estimate for default roles](media/resource-assignment-sales-estimate-07.png)</span></span>

<span data-ttu-id="77043-137">升级完成后，可以将团队成员的角色编辑为非默认分派的角色。</span><span class="sxs-lookup"><span data-stu-id="77043-137">After upgrade is complete, you can edit a team member's role to be something other than the assigned default.</span></span> <span data-ttu-id="77043-138">但是，如果更改某个团队成员角色，为其分派的所有任务的角色也会改变，因为版本 3 中不再允许为团队成员分派多个角色。</span><span class="sxs-lookup"><span data-stu-id="77043-138">However, if you change a team members role, it will be changed on all of their assigned tasks because team members are no longer allowed to be assigned multiple roles in version 3.</span></span>

![更新资源角色](media/resource-role-assignment-08.png)

<span data-ttu-id="77043-140">将资源的部门从默认部门更改为另一个部门时，这一条对分派给指定资源的明细任务也成立。</span><span class="sxs-lookup"><span data-stu-id="77043-140">This is also true for line tasks that were assigned to named resources when you change the resource’s organization unit from the default to another organization unit.</span></span> <span data-ttu-id="77043-141">版本 3 升级完成后，分派将使用资源的默认部门，而不是明细任务中设置的部门。</span><span class="sxs-lookup"><span data-stu-id="77043-141">After the version 3 upgrade is complete, the assignment will use the resource’s default organization unit instead of the one set on the line task.</span></span>

### <a name="tasks-assigned-to-generic-resources"></a><span data-ttu-id="77043-142">任务分派给通用资源</span><span class="sxs-lookup"><span data-stu-id="77043-142">Tasks assigned to generic resources</span></span>
<span data-ttu-id="77043-143">在版本 2 和版本 1 中，可以为任务设置角色和部门，然后使用 **生成团队** 功能基于为任务设置的属性生成通用资源。</span><span class="sxs-lookup"><span data-stu-id="77043-143">In version 2 and version 1, you can set the role and org unit on a task and then use the **Generate team** feature to generate generic resources based on the attributes set on the task.</span></span> <span data-ttu-id="77043-144">在版本 3 中，将创建具有角色和部门的通用团队成员，然后将团队分派给任务。</span><span class="sxs-lookup"><span data-stu-id="77043-144">In version 3, you create the generic team members with role and org unit, and then assign the team members to tasks.</span></span>

<span data-ttu-id="77043-145">在版本 2 和版本 1 中，采用通用资源的项目可以为两种状态，或者两种状态均在任务级别。</span><span class="sxs-lookup"><span data-stu-id="77043-145">In version 2 and version 1, projects with generic resources can be in two states, or a mix of both at the task level.</span></span> <span data-ttu-id="77043-146">例如，可以采用以下方案：</span><span class="sxs-lookup"><span data-stu-id="77043-146">For example, you can have the following scenarios:</span></span>

- <span data-ttu-id="77043-147">设置具有角色和部门的任务，但是未生成附属资源分派。</span><span class="sxs-lookup"><span data-stu-id="77043-147">Tasks with roles and org units set, but no affiliated resource assignment has been generated.</span></span>
- <span data-ttu-id="77043-148">具有使用 **生成团队** 功能通过创建通用资源分派的通用团队成员资源分派的任务。</span><span class="sxs-lookup"><span data-stu-id="77043-148">Tasks with generic team member resource assignments that were assigned by creating generic resource using the **Generate team** feature.</span></span>

<span data-ttu-id="77043-149">开始升级之前，建议您为满足以下条件的每个项目重新生成团队：将任务分派给了通用资源，或必须运行生成团队流程。</span><span class="sxs-lookup"><span data-stu-id="77043-149">Before you begin your upgrade, we recommend that you re-generate the team for each project that has tasks assigned to generic resources or has yet to have the generate team process run on them.</span></span>

<span data-ttu-id="77043-150">对于分派给使用 **生成团队** 生成的通用团队成员的任务，升级将保留团队的通用资源，并且保留该通用团队成员的分派。</span><span class="sxs-lookup"><span data-stu-id="77043-150">For tasks that are assigned to generic team members that were generated with **Generate Team** , the upgrade will leave the generic resource on the team and leave the assignment to that generic team member.</span></span> <span data-ttu-id="77043-151">建议仅在升级后，但预订或提交资源请求之前为通用团队成员生成资源要求。</span><span class="sxs-lookup"><span data-stu-id="77043-151">We recommend that you generate the resource requirement for the generic team member after the upgrade but before you book or submit a resource request.</span></span> <span data-ttu-id="77043-152">这将保留通用团队成员的所有与项目合同签订部门不同的部门分派。</span><span class="sxs-lookup"><span data-stu-id="77043-152">This will preserve any org unit assignments on the generic team members that are different than the project’s contracting org unit.</span></span>

<span data-ttu-id="77043-153">例如，在 Project Z 项目中，合同签订部门为 Contoso 美国。</span><span class="sxs-lookup"><span data-stu-id="77043-153">For example, in the Project Z project, the contracting org unit is Contoso US.</span></span> <span data-ttu-id="77043-154">在项目计划中，已经为实施阶段的测试任务分派了技术顾问角色，而分派的部门则为 Contoso 印度。</span><span class="sxs-lookup"><span data-stu-id="77043-154">In the project plan, testing tasks within the Implementation phase have been assigned the role Technical Consultant and the assigned org unit is Contoso India.</span></span>

![实施阶段部门分派](media/org-unit-assignment-09.png)

<span data-ttu-id="77043-156">实施阶段后，为技术顾问角色分派了集成测试任务，但是部门设置为 Contoso 美国。</span><span class="sxs-lookup"><span data-stu-id="77043-156">After the implementation phase, the integration test task is assigned to the role Technical consultant, but the org is set to Contoso US.</span></span>  

![集成测试任务部门分派](media/org-unit-generate-team-10.png)

<span data-ttu-id="77043-158">为项目生成团队时，由于任务的部门不同，所以将创建两个通用团队成员。</span><span class="sxs-lookup"><span data-stu-id="77043-158">When you generate a team for the project, two generic team members are created due to the different org units on the tasks.</span></span> <span data-ttu-id="77043-159">将为技术顾问 1 分派 Contoso 印度任务，为技术顾问 2 分派 Contoso 美国任务。</span><span class="sxs-lookup"><span data-stu-id="77043-159">Technical consultant 1 will be assigned the Contoso India tasks and Technical consultant 2 will have the Contoso US tasks.</span></span>  

![生成的通用团队成员](media/org-unit-assignments-multiple-resources-11.png)

> [!NOTE]
> <span data-ttu-id="77043-161">在 Project Service Automation 版本 2 和版本 1 中，团队成员不存储部门，部门在明细任务中维护。</span><span class="sxs-lookup"><span data-stu-id="77043-161">In Project Service Automation version 2 and version 1, the team member does not hold the organization unit, that is maintained on the line task.</span></span>

![Project Service Automation 中的版本 2 和版本 1 明细任务](media/line-tasks-12.png)

<span data-ttu-id="77043-163">可以在估算视图中查看部门。</span><span class="sxs-lookup"><span data-stu-id="77043-163">You can see the organization unit on the estimates view.</span></span> 

![部门估算](media/org-unit-estimates-view-13.png)
 
<span data-ttu-id="77043-165">升级完成后时，将把与通用团队成员对应的明细任务中的部门添加到通用团队成员，并删除明细任务。</span><span class="sxs-lookup"><span data-stu-id="77043-165">When the upgrade is complete, the organization unit on the line task that corresponds to the generic team member is added to the generic team member and the line task is removed.</span></span> <span data-ttu-id="77043-166">因此，建议您在升级前为包含通用资源的每个项目生成团队。</span><span class="sxs-lookup"><span data-stu-id="77043-166">Because of this, we recommend that before you upgrade, you generate or re-generate the team on each project that contains generic resources.</span></span>

<span data-ttu-id="77043-167">对于分派给部门与合同签订项目部门不同的角色，并且尚未生成团队的任务，升级将为该角色创建一个通用团队成员，但是对该团队成员的部门使用项目的合同签订部门。</span><span class="sxs-lookup"><span data-stu-id="77043-167">For tasks that are assigned to a role with an org unit that differs from the org unit of the contracting project, and a team has not been generated, upgrade will create a generic team member for the role, but will use the contracting unit of the project for the team member's org unit.</span></span> <span data-ttu-id="77043-168">请回去参考 Project Z 的示例，这意味着已经为合同签订部门 Contoso 美国和实施阶段内的项目计划测试任务分派了技术顾问角色，并且采用了分派给 Contoso 印度的部门。</span><span class="sxs-lookup"><span data-stu-id="77043-168">Referring back to the example with Project Z, this means that the contracting org unit Contoso US, and the project plan testing tasks within the Implementation phase have been assigned the role Technical Consultant with the org unit assigned to Contoso India.</span></span> <span data-ttu-id="77043-169">已经为实施阶段后完成的集成测试任务分派了技术顾问角色。</span><span class="sxs-lookup"><span data-stu-id="77043-169">The Integration test task that is completed after the Implementation phase has been assigned to the role Technical consultant.</span></span> <span data-ttu-id="77043-170">部门为 Contoso 美国，未生成团队。</span><span class="sxs-lookup"><span data-stu-id="77043-170">The org unit is Contoso US and a team has not been generated.</span></span> <span data-ttu-id="77043-171">升级将创建一个通用团队成员（这是分派有所有三个任务的工时的技术顾问），以及部门 Contoso 美国（这是项目的合同签订部门）。</span><span class="sxs-lookup"><span data-stu-id="77043-171">Upgrade will create one generic team member, a Technical consultant that has the assigned hours of all three tasks, and an org unit of Contoso US, the project’s contracting org unit.</span></span>   
 
<span data-ttu-id="77043-172">更改不生成的团队成员中不同资源部门的默认设置是我们之所以建议您在升级之前为包含通用资源的每个项目生成或重新生成团队，以便不丢失部门分派的原因。</span><span class="sxs-lookup"><span data-stu-id="77043-172">Changing the default of the different resourcing org units on un-generated team members is the reason we recommend that you generate or re-generate the team on each project that contains generic resources prior to the upgrade so that the org unit assignments are not lost.</span></span>

