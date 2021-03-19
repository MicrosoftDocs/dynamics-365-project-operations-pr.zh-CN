---
title: 工作分解结构的升级注意事项
description: 此主题介绍如何将工作分解结构从 Project Service Automation 2.x 升级到 3.x。
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 10/18/2019
ms.topic: article
author: ruhercul
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
ms.openlocfilehash: a067521410f0fe0d8f5d4c510a35f2a3b018dce3
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/15/2021
ms.locfileid: "5281737"
---
# <a name="upgrade-considerations-for-the-work-breakdown-structure"></a><span data-ttu-id="930c1-103">工作分解结构的升级注意事项</span><span class="sxs-lookup"><span data-stu-id="930c1-103">Upgrade considerations for the work breakdown structure</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="930c1-104">此主题介绍如何将工作分解结构从 Project Service Automation 2.x 升级到 3.x。</span><span class="sxs-lookup"><span data-stu-id="930c1-104">This topic provides information about upgrading the work breakdown structure from Project Service Automation 2.x to 3.x.</span></span> <span data-ttu-id="930c1-105">此主题定义 Project Service Automation (PSA) 中要成功升级需要的项目健康状态。</span><span class="sxs-lookup"><span data-stu-id="930c1-105">This topic defines the healthy state of a project in Project Service Automation (PSA) that is required for a successful upgrade.</span></span> <span data-ttu-id="930c1-106">以及有关将导致升级失败的一般阻碍情况的信息。</span><span class="sxs-lookup"><span data-stu-id="930c1-106">There is also information about the common blocking conditions that will cause upgrade to fail.</span></span> <span data-ttu-id="930c1-107">有关在项目计划内定义项目任务及其职能的详细信息，请参阅[项目计划](project-creating.md)。</span><span class="sxs-lookup"><span data-stu-id="930c1-107">For more information about defining project tasks and their functions within a project schedule, see [Project schedules](project-creating.md).</span></span>

## <a name="key-entities"></a><span data-ttu-id="930c1-108">关键实体</span><span class="sxs-lookup"><span data-stu-id="930c1-108">Key entities</span></span>
<span data-ttu-id="930c1-109">对于已经使用资源加载的准确工作分解结构，需要以下实体：</span><span class="sxs-lookup"><span data-stu-id="930c1-109">For an accurate work breakdown structure that is already loaded with resources, the following entities are required:</span></span>

- [<span data-ttu-id="930c1-110">项目</span><span class="sxs-lookup"><span data-stu-id="930c1-110">Project</span></span>](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_project)
- [<span data-ttu-id="930c1-111">项目团队</span><span class="sxs-lookup"><span data-stu-id="930c1-111">Project Team</span></span>](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projectteam)
- [<span data-ttu-id="930c1-112">项目任务</span><span class="sxs-lookup"><span data-stu-id="930c1-112">Project Task</span></span>](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projecttask)
- [<span data-ttu-id="930c1-113">资源分派</span><span class="sxs-lookup"><span data-stu-id="930c1-113">Resource Assignments</span></span>](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_resourceassignment)
- [<span data-ttu-id="930c1-114">项目任务依赖关系</span><span class="sxs-lookup"><span data-stu-id="930c1-114">Project Task Dependency</span></span>](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projecttaskdependency)
- [<span data-ttu-id="930c1-115">可预订资源</span><span class="sxs-lookup"><span data-stu-id="930c1-115">Bookable Resources</span></span>](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/bookableresource)

<span data-ttu-id="930c1-116">若要定义已加载资源的工作分解结构，必须完成以下步骤：</span><span class="sxs-lookup"><span data-stu-id="930c1-116">To define a resource loaded work breakdown structure, you must complete the following steps:</span></span>

1. <span data-ttu-id="930c1-117">创建新项目。</span><span class="sxs-lookup"><span data-stu-id="930c1-117">Create a new project.</span></span> <span data-ttu-id="930c1-118">有关如何创建新项目的详细信息，请参阅 [msdyn_project](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_project)。</span><span class="sxs-lookup"><span data-stu-id="930c1-118">For more information about how to create a new project, see [msdyn_project](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_project).</span></span>
2. <span data-ttu-id="930c1-119">创建一个或多个任务。</span><span class="sxs-lookup"><span data-stu-id="930c1-119">Create one or more tasks.</span></span> <span data-ttu-id="930c1-120">有关如何创建任务的详细信息，请参阅 [msdyn_projecttask](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projecttask)。</span><span class="sxs-lookup"><span data-stu-id="930c1-120">For more information about how to create a task, see [msdyn_projecttask](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projecttask).</span></span>
3. <span data-ttu-id="930c1-121">定义任务依赖项。</span><span class="sxs-lookup"><span data-stu-id="930c1-121">Define the task dependencies.</span></span> <span data-ttu-id="930c1-122">有关详细信息，请参阅[项目任务依赖关系](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projecttaskdependency)。</span><span class="sxs-lookup"><span data-stu-id="930c1-122">For more information, see [Project Task Dependency](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projecttaskdependency).</span></span>
4. <span data-ttu-id="930c1-123">为项目分派项目团队成员。</span><span class="sxs-lookup"><span data-stu-id="930c1-123">Assign project team members to the project.</span></span> <span data-ttu-id="930c1-124">有关详细信息，请参阅 [msdyn_projectteam](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projectteam)。</span><span class="sxs-lookup"><span data-stu-id="930c1-124">For more information, see [msdyn_projectteam](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projectteam).</span></span>
5. <span data-ttu-id="930c1-125">为任务分派项目团队成员。</span><span class="sxs-lookup"><span data-stu-id="930c1-125">Assign project team members to the tasks.</span></span> <span data-ttu-id="930c1-126">有关详细信息，请参阅 [msdyn_resourceassignment](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_resourceassignment)。</span><span class="sxs-lookup"><span data-stu-id="930c1-126">For more information, see [msdyn_resourceassignment](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_resourceassignment).</span></span>

## <a name="project-team-relationships"></a><span data-ttu-id="930c1-127">项目团队关系</span><span class="sxs-lookup"><span data-stu-id="930c1-127">Project team relationships</span></span>

<span data-ttu-id="930c1-128">若要确保升级成功，必须正确维护以下关系：</span><span class="sxs-lookup"><span data-stu-id="930c1-128">To ensure a successful upgrade, the following relationships must be correctly maintained:</span></span>
- <span data-ttu-id="930c1-129">所有项目团队成员必须与一项可预订资源关联。</span><span class="sxs-lookup"><span data-stu-id="930c1-129">All project team members must be associated with a bookable resource.</span></span>
- <span data-ttu-id="930c1-130">所有项目团队成员必须与同一个项目关联。</span><span class="sxs-lookup"><span data-stu-id="930c1-130">All project team members must be associated with the same project.</span></span> 

## <a name="project-task-relationships"></a><span data-ttu-id="930c1-131">项目任务关系</span><span class="sxs-lookup"><span data-stu-id="930c1-131">Project task relationships</span></span>
<span data-ttu-id="930c1-132">若要确保升级成功，必须正确维护以下关系：</span><span class="sxs-lookup"><span data-stu-id="930c1-132">To ensure a successful upgrade, the following relationships must be correctly maintained:</span></span>

- <span data-ttu-id="930c1-133">所有相关任务必须与同一个项目关联。</span><span class="sxs-lookup"><span data-stu-id="930c1-133">Any related tasks must be associated with the same project.</span></span>
- <span data-ttu-id="930c1-134">每个明细任务必须有一个父任务。</span><span class="sxs-lookup"><span data-stu-id="930c1-134">Every line task must have a parent task.</span></span>
- <span data-ttu-id="930c1-135">每个任务必须有一个父项目。</span><span class="sxs-lookup"><span data-stu-id="930c1-135">Every task must have a parent project.</span></span>

### <a name="valid-conditions"></a><span data-ttu-id="930c1-136">有效条件</span><span class="sxs-lookup"><span data-stu-id="930c1-136">Valid conditions</span></span>

- <span data-ttu-id="930c1-137">所有任务持续时间必须大于或等于 (>=) 一个小时，并小于 1,800,000 分钟（1,250 天）。\*</span><span class="sxs-lookup"><span data-stu-id="930c1-137">All task durations must be greater than or equal to (>=) one hour and less than 1,800,000 minutes (1,250 days).\*</span></span>
- <span data-ttu-id="930c1-138">所有任务的开始日期不得早于 2000/01/01。\*</span><span class="sxs-lookup"><span data-stu-id="930c1-138">All tasks must have a start date no earlier than 2000/01/01.\*</span></span>
- <span data-ttu-id="930c1-139">所有任务的开始日期不得晚于当天后的 17 年。\*</span><span class="sxs-lookup"><span data-stu-id="930c1-139">All tasks must have a start date no later than 17 years from the present day.\*</span></span>
- <span data-ttu-id="930c1-140">所有任务的开始日期必须早于或等于其完成日期。</span><span class="sxs-lookup"><span data-stu-id="930c1-140">All tasks must have a start date earlier or equal to their finish date.</span></span>
- <span data-ttu-id="930c1-141">分类（支出、材料、税和时间）的所有交易类型必须有 **默认计价单位** 和 **计价单位组** 值。</span><span class="sxs-lookup"><span data-stu-id="930c1-141">All transaction types on classifications (Expense, Material, Tax, and Time) must have values for **Default Unit** and **Unit Group**.</span></span>
- <span data-ttu-id="930c1-142">应该避免日期格式带字母。</span><span class="sxs-lookup"><span data-stu-id="930c1-142">Date formats with letters should be avoided.</span></span>

### <a name="potential-mitigation-steps"></a><span data-ttu-id="930c1-143">可能的缓解步骤</span><span class="sxs-lookup"><span data-stu-id="930c1-143">Potential mitigation steps</span></span>
- <span data-ttu-id="930c1-144">使用“高级查找”可确定不包含项目 ID 的项目任务。</span><span class="sxs-lookup"><span data-stu-id="930c1-144">Use Advanced Find to identify Project tasks that do not contain a Project ID.</span></span>
- <span data-ttu-id="930c1-145">使用“高级查找”可确定计划持续时间大于 1,800,000 的项目任务。</span><span class="sxs-lookup"><span data-stu-id="930c1-145">Use Advanced Find to identify Project tasks where the scheduled duration is greater than > 1,800,000.</span></span>
- <span data-ttu-id="930c1-146">在进行任何数据更改之前，您应调查与实体相关联的任何自定义项，它们可能会导致数据进入错误状态。</span><span class="sxs-lookup"><span data-stu-id="930c1-146">Prior to making any data changes, you should investigate any customizations associated with the entity that may have led to getting the data into a bad state.</span></span> <span data-ttu-id="930c1-147">这些自定义项问题应该首先解决，然后才能继续进行与数据相关的任何更新。</span><span class="sxs-lookup"><span data-stu-id="930c1-147">These customizations should be addressed before proceeding with any data-related updates.</span></span>
- <span data-ttu-id="930c1-148">对于所标识的孤立任务，如果不需要它们，或者如果应该将它们与正确的父项目相关联，请考虑删除这些任务。</span><span class="sxs-lookup"><span data-stu-id="930c1-148">For the identified tasks that have been orphaned, consider deleting these tasks if they are not needed or if they should be associated with the correct parent project.</span></span>
- <span data-ttu-id="930c1-149">对于持续时间超过 1,250 天的任何任务，请考虑添加多个任务以表示总持续时间（如果可行）。</span><span class="sxs-lookup"><span data-stu-id="930c1-149">For any tasks where the duration is greater than 1,250 days, consider adding multiple tasks to represent the total duration, if feasible.</span></span>

> [!NOTE]
> <span data-ttu-id="930c1-150">带有星号 (\*) 标记的项之所以有限制，是因为客户关系管理 (CRM) 仅支持 7,320 个重复扩展。</span><span class="sxs-lookup"><span data-stu-id="930c1-150">Items noted with an asterisk (\*) have limits that are due to the fact that customer relationship management (CRM) supports only 7,320 recurrence expansions.</span></span> <span data-ttu-id="930c1-151">必须低于此限制。</span><span class="sxs-lookup"><span data-stu-id="930c1-151">You must stay below this limit.</span></span>

## <a name="resource-assignment-relationships"></a><span data-ttu-id="930c1-152">资源分派关系</span><span class="sxs-lookup"><span data-stu-id="930c1-152">Resource Assignment relationships</span></span>
<span data-ttu-id="930c1-153">若要确保升级成功，必须正确维护以下关系：</span><span class="sxs-lookup"><span data-stu-id="930c1-153">To ensure a successful upgrade, the following relationships must be correctly maintained:</span></span>

- <span data-ttu-id="930c1-154">必须将同一个工作分解结构中的所有资源分派与同一个项目关联。</span><span class="sxs-lookup"><span data-stu-id="930c1-154">All Resource Assignments in a work breakdown structure must be related to the same project.</span></span>
- <span data-ttu-id="930c1-155">必须将同一个工作分解结构中的所有资源分派与同一个项目中的项目团队成员关联。</span><span class="sxs-lookup"><span data-stu-id="930c1-155">All Resource Assignments in a work breakdown structure must be associated to project team members in the same project.</span></span>

### <a name="potential-mitigation-steps"></a><span data-ttu-id="930c1-156">可能的缓解步骤</span><span class="sxs-lookup"><span data-stu-id="930c1-156">Potential mitigation steps</span></span>
- <span data-ttu-id="930c1-157">确定属于上述情况之外的所有任务。</span><span class="sxs-lookup"><span data-stu-id="930c1-157">Identify all tasks that fall outside the conditions described above.</span></span>  
- <span data-ttu-id="930c1-158">应删除任何不再有效的资源分派。</span><span class="sxs-lookup"><span data-stu-id="930c1-158">Any Resource Assignments that are no longer valid should be deleted.</span></span>

## <a name="project-task-dependency-relationships"></a><span data-ttu-id="930c1-159">项目任务依赖项关系</span><span class="sxs-lookup"><span data-stu-id="930c1-159">Project task dependency relationships</span></span>
<span data-ttu-id="930c1-160">若要确保升级成功，必须正确维护以下关系：</span><span class="sxs-lookup"><span data-stu-id="930c1-160">To ensure a successful upgrade, the following relationships must be correctly maintained:</span></span>

- <span data-ttu-id="930c1-161">所有项目任务依赖项必须与同一个项目关联。</span><span class="sxs-lookup"><span data-stu-id="930c1-161">All project task dependencies must be related to the same project.</span></span>
- <span data-ttu-id="930c1-162">一个任务不能多次引用同一个依赖项。</span><span class="sxs-lookup"><span data-stu-id="930c1-162">A task can't have the same dependency referenced more than once.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]