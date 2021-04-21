---
title: 使用计划 API 对计划实体执行操作
description: 该主题提供了关于使用计划 API 的信息和示例。
author: sigitac
manager: Annbe
ms.date: 04/07/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: a50a2c6220bb49de8146d0758019827e120e0526
ms.sourcegitcommit: 8ff9fe396db6dec581c21cd6bb9acc2691c815b0
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/07/2021
ms.locfileid: "5868118"
---
# <a name="use-schedule-apis-to-perform-operations-with-scheduling-entities"></a><span data-ttu-id="58b3e-103">使用计划 API 对计划实体执行操作</span><span class="sxs-lookup"><span data-stu-id="58b3e-103">Use Schedule APIs to perform operations with Scheduling entities</span></span>

<span data-ttu-id="58b3e-104">_**适用于：** 基于资源/非库存场景的 Project Operations，精简部署 - 估价开票交易_</span><span class="sxs-lookup"><span data-stu-id="58b3e-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

> [!IMPORTANT] 
> <span data-ttu-id="58b3e-105">本主题中所述的部分或所有功能属于预览版内容。</span><span class="sxs-lookup"><span data-stu-id="58b3e-105">Some or all of the functionality noted in this topic is available as part of a preview release.</span></span> <span data-ttu-id="58b3e-106">相关内容和功能可能会发生更改。</span><span class="sxs-lookup"><span data-stu-id="58b3e-106">The content and the functionality are subject to change.</span></span> 

## <a name="scheduling-entities"></a><span data-ttu-id="58b3e-107">计划实体</span><span class="sxs-lookup"><span data-stu-id="58b3e-107">Scheduling entities</span></span>

<span data-ttu-id="58b3e-108">通过计划 API，可以针对 **计划实体** 执行创建、更新和删除操作。</span><span class="sxs-lookup"><span data-stu-id="58b3e-108">Schedule APIs provide the ability to perform create, update, and delete operations with **Scheduling entities**.</span></span> <span data-ttu-id="58b3e-109">这些实体通过 Web 项目中的计划引擎进行管理。</span><span class="sxs-lookup"><span data-stu-id="58b3e-109">These entities are managed through the Scheduling engine in Project for the web.</span></span> <span data-ttu-id="58b3e-110">早期 Dynamics 365 Project Operations 版本中限制对 **计划实体** 执行创建、更新和删除操作。</span><span class="sxs-lookup"><span data-stu-id="58b3e-110">Create, update, and delete operations with **Scheduling entities** were restricted in earlier Dynamics 365 Project Operations releases.</span></span>

<span data-ttu-id="58b3e-111">下表提供了 **计划实体** 的完整列表。</span><span class="sxs-lookup"><span data-stu-id="58b3e-111">The following table provides a full list of the **Scheduling entities**.</span></span>

| <span data-ttu-id="58b3e-112">实体名称</span><span class="sxs-lookup"><span data-stu-id="58b3e-112">Entity name</span></span>  | <span data-ttu-id="58b3e-113">实体逻辑名称</span><span class="sxs-lookup"><span data-stu-id="58b3e-113">Entity logical name</span></span> |
| --- | --- |
| <span data-ttu-id="58b3e-114">Project</span><span class="sxs-lookup"><span data-stu-id="58b3e-114">Project</span></span> | <span data-ttu-id="58b3e-115">msdyn_project</span><span class="sxs-lookup"><span data-stu-id="58b3e-115">msdyn_project</span></span> |
| <span data-ttu-id="58b3e-116">项目任务</span><span class="sxs-lookup"><span data-stu-id="58b3e-116">Project Task</span></span>  | <span data-ttu-id="58b3e-117">msdyn_projecttask</span><span class="sxs-lookup"><span data-stu-id="58b3e-117">msdyn_projecttask</span></span>  |
| <span data-ttu-id="58b3e-118">项目任务依赖关系</span><span class="sxs-lookup"><span data-stu-id="58b3e-118">Project Task Dependency</span></span>  | <span data-ttu-id="58b3e-119">msdyn_projecttaskdependency</span><span class="sxs-lookup"><span data-stu-id="58b3e-119">msdyn_projecttaskdependency</span></span>  |
| <span data-ttu-id="58b3e-120">资源分派</span><span class="sxs-lookup"><span data-stu-id="58b3e-120">Resource Assignment</span></span> | <span data-ttu-id="58b3e-121">msdyn_resourceassignment</span><span class="sxs-lookup"><span data-stu-id="58b3e-121">msdyn_resourceassignment</span></span> |
| <span data-ttu-id="58b3e-122">项目 Bucket</span><span class="sxs-lookup"><span data-stu-id="58b3e-122">Project Bucket</span></span>  | <span data-ttu-id="58b3e-123">msdyn_projectbucket</span><span class="sxs-lookup"><span data-stu-id="58b3e-123">msdyn_projectbucket</span></span> |
| <span data-ttu-id="58b3e-124">项目团队成员</span><span class="sxs-lookup"><span data-stu-id="58b3e-124">Project Team Member</span></span> | <span data-ttu-id="58b3e-125">msdyn_projectteam</span><span class="sxs-lookup"><span data-stu-id="58b3e-125">msdyn_projectteam</span></span> |

## <a name="operationset"></a><span data-ttu-id="58b3e-126">OperationSet</span><span class="sxs-lookup"><span data-stu-id="58b3e-126">OperationSet</span></span>

<span data-ttu-id="58b3e-127">OperationSet 是一种工作单位模式，当必须在交易内处理多个计划影响请求时，可以使用该模式。</span><span class="sxs-lookup"><span data-stu-id="58b3e-127">OperationSet is a unit-of-work pattern that can be used when several schedule impacting requests must be processed within a transaction.</span></span>

## <a name="schedule-apis"></a><span data-ttu-id="58b3e-128">计划 API</span><span class="sxs-lookup"><span data-stu-id="58b3e-128">Schedule APIs</span></span>

<span data-ttu-id="58b3e-129">下面是当前计划 API 的列表。</span><span class="sxs-lookup"><span data-stu-id="58b3e-129">The following is a list of current Schedule APIs.</span></span>

- <span data-ttu-id="58b3e-130">**msdyn_CreateProjectV1**：此 API 可用于创建项目。</span><span class="sxs-lookup"><span data-stu-id="58b3e-130">**msdyn_CreateProjectV1**: This API can be used to create a project.</span></span> <span data-ttu-id="58b3e-131">将立即创建项目和默认项目 Bucket。</span><span class="sxs-lookup"><span data-stu-id="58b3e-131">The project and default project bucket is created immediately.</span></span>
- <span data-ttu-id="58b3e-132">**msdyn_CreateTeamMemberV1**：此 API 可用于创建项目团队成员。</span><span class="sxs-lookup"><span data-stu-id="58b3e-132">**msdyn_CreateTeamMemberV1**: This API can be used to create a project team member.</span></span> <span data-ttu-id="58b3e-133">系统会立即创建团队成员记录。</span><span class="sxs-lookup"><span data-stu-id="58b3e-133">The team member record is created immediately.</span></span>
- <span data-ttu-id="58b3e-134">**msdyn_CreateOperationSetV1**：此 API 可用于安排必须在交易中执行多个请求。</span><span class="sxs-lookup"><span data-stu-id="58b3e-134">**msdyn_CreateOperationSetV1**: This API can be used to schedule several requests that must be performed within a transaction.</span></span>
- <span data-ttu-id="58b3e-135">**msdyn_PSSCreateV1**：此 API 可用于创建实体。</span><span class="sxs-lookup"><span data-stu-id="58b3e-135">**msdyn_PSSCreateV1**: This API can be used to create an entity.</span></span> <span data-ttu-id="58b3e-136">该实体可以是支持创建操作的任何计划实体。</span><span class="sxs-lookup"><span data-stu-id="58b3e-136">The entity can be any of the Scheduling entities that support the create operation.</span></span>
- <span data-ttu-id="58b3e-137">**msdyn_PSSUpdateV1**：此 API 可用于更新实体。</span><span class="sxs-lookup"><span data-stu-id="58b3e-137">**msdyn_PSSUpdateV1**: This API can be used to update an entity.</span></span> <span data-ttu-id="58b3e-138">该实体可以是支持更新操作的任何计划实体。</span><span class="sxs-lookup"><span data-stu-id="58b3e-138">The entity can be any of the Scheduling entities that support the update operation.</span></span>
- <span data-ttu-id="58b3e-139">**msdyn_PSSDeleteV1**：此 API 可用于删除实体。</span><span class="sxs-lookup"><span data-stu-id="58b3e-139">**msdyn_PSSDeleteV1**: This API can be used to delete an entity.</span></span> <span data-ttu-id="58b3e-140">该实体可以是支持删除操作的任何计划实体。</span><span class="sxs-lookup"><span data-stu-id="58b3e-140">The entity can be any of the Scheduling entities that support the delete operation.</span></span>
- <span data-ttu-id="58b3e-141">**msdyn_ExecuteOperationSetV1**：此 API 用于执行给定操作集内的所有操作。</span><span class="sxs-lookup"><span data-stu-id="58b3e-141">**msdyn_ExecuteOperationSetV1**: This API is used to execute all of the operations within the given operation set.</span></span>

## <a name="using-schedule-apis-with-operationset"></a><span data-ttu-id="58b3e-142">将计划 API 与 OperationSet 一同使用</span><span class="sxs-lookup"><span data-stu-id="58b3e-142">Using Schedule APIs with OperationSet</span></span>

<span data-ttu-id="58b3e-143">由于会立即创建同时具有 **CreateProjectV1** 和 **CreateTeamMemberV1** 的记录，因此这些 API 不能直接在 **OperationSet** 中使用。</span><span class="sxs-lookup"><span data-stu-id="58b3e-143">Because records with both **CreateProjectV1** and **CreateTeamMemberV1** are created immediately, these APIs can't be used in the **OperationSet** directly.</span></span> <span data-ttu-id="58b3e-144">但是，可以使用 API 创建所需记录，创建 **OperationSet**，然后在 **OperationSet** 中使用这些预先创建的记录。</span><span class="sxs-lookup"><span data-stu-id="58b3e-144">However, you can use the API to create needed records, create an **OperationSet**, and then use these pre-created records in the **OperationSet**.</span></span>

## <a name="supported-operations"></a><span data-ttu-id="58b3e-145">不支持的操作</span><span class="sxs-lookup"><span data-stu-id="58b3e-145">Supported operations</span></span>

| <span data-ttu-id="58b3e-146">计划实体</span><span class="sxs-lookup"><span data-stu-id="58b3e-146">Scheduling entity</span></span> | <span data-ttu-id="58b3e-147">创建​​</span><span class="sxs-lookup"><span data-stu-id="58b3e-147">Create</span></span> | <span data-ttu-id="58b3e-148">更新</span><span class="sxs-lookup"><span data-stu-id="58b3e-148">Update</span></span> | <span data-ttu-id="58b3e-149">Delete</span><span class="sxs-lookup"><span data-stu-id="58b3e-149">Delete</span></span> | <span data-ttu-id="58b3e-150">重要考虑因素</span><span class="sxs-lookup"><span data-stu-id="58b3e-150">Important considerations</span></span> |
| --- | --- | --- | --- | --- |
<span data-ttu-id="58b3e-151">项目任务</span><span class="sxs-lookup"><span data-stu-id="58b3e-151">Project task</span></span> | <span data-ttu-id="58b3e-152">是</span><span class="sxs-lookup"><span data-stu-id="58b3e-152">Yes</span></span> | <span data-ttu-id="58b3e-153">是</span><span class="sxs-lookup"><span data-stu-id="58b3e-153">Yes</span></span> | <span data-ttu-id="58b3e-154">是</span><span class="sxs-lookup"><span data-stu-id="58b3e-154">Yes</span></span> | <span data-ttu-id="58b3e-155">无​</span><span class="sxs-lookup"><span data-stu-id="58b3e-155">None</span></span> |
| <span data-ttu-id="58b3e-156">项目任务依赖关系</span><span class="sxs-lookup"><span data-stu-id="58b3e-156">Project task dependency</span></span> | <span data-ttu-id="58b3e-157">是</span><span class="sxs-lookup"><span data-stu-id="58b3e-157">Yes</span></span> | <span data-ttu-id="58b3e-158">是</span><span class="sxs-lookup"><span data-stu-id="58b3e-158">Yes</span></span> | | <span data-ttu-id="58b3e-159">不会更新项目任务依赖关系记录。</span><span class="sxs-lookup"><span data-stu-id="58b3e-159">Project task dependency records aren't updated.</span></span> <span data-ttu-id="58b3e-160">而是可以删除旧记录，并可以创建新记录。</span><span class="sxs-lookup"><span data-stu-id="58b3e-160">Instead, an old record can be deleted and a new record can be created.</span></span> |
| <span data-ttu-id="58b3e-161">资源分派</span><span class="sxs-lookup"><span data-stu-id="58b3e-161">Resource assignment</span></span> | <span data-ttu-id="58b3e-162">是</span><span class="sxs-lookup"><span data-stu-id="58b3e-162">Yes</span></span> | <span data-ttu-id="58b3e-163">是</span><span class="sxs-lookup"><span data-stu-id="58b3e-163">Yes</span></span> | | <span data-ttu-id="58b3e-164">不支持对以下字段执行操作：**BookableResourceID**、**Effort**、**EffortCompleted**、**EffortRemaining** 和 **PlannedWork**。</span><span class="sxs-lookup"><span data-stu-id="58b3e-164">Operations with the following fields aren't supported: **BookableResourceID**, **Effort**, **EffortCompleted**, **EffortRemaining**, and **PlannedWork**.</span></span> <span data-ttu-id="58b3e-165">资源分派记录不会更新。</span><span class="sxs-lookup"><span data-stu-id="58b3e-165">Resource assignment records aren't updated.</span></span> <span data-ttu-id="58b3e-166">而是可以删除旧记录，并可以创建新记录。</span><span class="sxs-lookup"><span data-stu-id="58b3e-166">Instead, the old record can be deleted and a new record can be created.</span></span> |
| <span data-ttu-id="58b3e-167">项目 Bucket</span><span class="sxs-lookup"><span data-stu-id="58b3e-167">Project bucket</span></span> | <span data-ttu-id="58b3e-168">不适用</span><span class="sxs-lookup"><span data-stu-id="58b3e-168">N/A</span></span> | <span data-ttu-id="58b3e-169">不适用</span><span class="sxs-lookup"><span data-stu-id="58b3e-169">N/A</span></span> | <span data-ttu-id="58b3e-170">不适用</span><span class="sxs-lookup"><span data-stu-id="58b3e-170">N/A</span></span> | <span data-ttu-id="58b3e-171">使用 **CreateProjectV1** API 创建了默认 Bucket。</span><span class="sxs-lookup"><span data-stu-id="58b3e-171">The default bucket is created using the **CreateProjectV1** API.</span></span> |
| <span data-ttu-id="58b3e-172">项目团队成员</span><span class="sxs-lookup"><span data-stu-id="58b3e-172">Project team member</span></span> | <span data-ttu-id="58b3e-173">是</span><span class="sxs-lookup"><span data-stu-id="58b3e-173">Yes</span></span> | <span data-ttu-id="58b3e-174">是</span><span class="sxs-lookup"><span data-stu-id="58b3e-174">Yes</span></span> | <span data-ttu-id="58b3e-175">是</span><span class="sxs-lookup"><span data-stu-id="58b3e-175">Yes</span></span> | <span data-ttu-id="58b3e-176">对于创建操作，请使用 **CreateTeamMemberV1** API。</span><span class="sxs-lookup"><span data-stu-id="58b3e-176">For the create operation, use the **CreateTeamMemberV1** API.</span></span> |
| <span data-ttu-id="58b3e-177">Project</span><span class="sxs-lookup"><span data-stu-id="58b3e-177">Project</span></span> | <span data-ttu-id="58b3e-178">是</span><span class="sxs-lookup"><span data-stu-id="58b3e-178">Yes</span></span> | <span data-ttu-id="58b3e-179">是</span><span class="sxs-lookup"><span data-stu-id="58b3e-179">Yes</span></span> | <span data-ttu-id="58b3e-180">不适用</span><span class="sxs-lookup"><span data-stu-id="58b3e-180">N/A</span></span> | <span data-ttu-id="58b3e-181">不支持以下对字段执行操作：**StateCode**、**BulkGenerationStatus**、**GlobalRevisionToken**、**CalendarID**、**Effort**、**EffortCompleted**、**EffortRemaining**、**Progress**、**Finish**、**TaskEarliestStart** 和 **Duration**。</span><span class="sxs-lookup"><span data-stu-id="58b3e-181">Operations with the following fields aren't supported: **StateCode**, **BulkGenerationStatus**, **GlobalRevisionToken**, **CalendarID**, **Effort**, **EffortCompleted**, **EffortRemaining**, **Progress**, **Finish**, **TaskEarliestStart**, and **Duration**.</span></span> |

<span data-ttu-id="58b3e-182">可以对包含自定义字段的实体对象调用这些 API。</span><span class="sxs-lookup"><span data-stu-id="58b3e-182">These APIs can be called with entity objects that include custom fields.</span></span>

<span data-ttu-id="58b3e-183">ID 属性是可选的。</span><span class="sxs-lookup"><span data-stu-id="58b3e-183">The ID property is optional.</span></span> <span data-ttu-id="58b3e-184">如果提供了此属性，则系统会尝试使用它，如果无法使用它，则会引发异常。</span><span class="sxs-lookup"><span data-stu-id="58b3e-184">If it's provided, the system attempts to use it and throws an exception if it can't be used.</span></span> <span data-ttu-id="58b3e-185">如果未提供此属性，系统将生成它。</span><span class="sxs-lookup"><span data-stu-id="58b3e-185">If it isn't provided, the system will generate it.</span></span>

## <a name="limitations-and-known-issues"></a><span data-ttu-id="58b3e-186">限制和已知问题</span><span class="sxs-lookup"><span data-stu-id="58b3e-186">Limitations and known issues</span></span>
<span data-ttu-id="58b3e-187">下面是一系列限制和已知问题：</span><span class="sxs-lookup"><span data-stu-id="58b3e-187">The following is a list of limitations and known issues:</span></span>

- <span data-ttu-id="58b3e-188">计划 API 仅供 **具有 Microsoft 项目许可证的用户** 使用。</span><span class="sxs-lookup"><span data-stu-id="58b3e-188">Schedule APIs can only be used by **Users with Microsoft Project License.**</span></span> <span data-ttu-id="58b3e-189">以下用户不能使用它们：</span><span class="sxs-lookup"><span data-stu-id="58b3e-189">They can't be used by:</span></span>
    - <span data-ttu-id="58b3e-190">应用程序用户</span><span class="sxs-lookup"><span data-stu-id="58b3e-190">Application users</span></span>
    - <span data-ttu-id="58b3e-191">系统用户</span><span class="sxs-lookup"><span data-stu-id="58b3e-191">System users</span></span>
    - <span data-ttu-id="58b3e-192">集成用户</span><span class="sxs-lookup"><span data-stu-id="58b3e-192">Integration users</span></span>
    - <span data-ttu-id="58b3e-193">没有所需许可证的其他用户</span><span class="sxs-lookup"><span data-stu-id="58b3e-193">Other users that don't have the required license</span></span>
- <span data-ttu-id="58b3e-194">每个 **OperationSets** 最多只能有 100 项操作。</span><span class="sxs-lookup"><span data-stu-id="58b3e-194">Each **OperationSet** can only have a maximum of 100 operations.</span></span>
- <span data-ttu-id="58b3e-195">每个用户最多只能有 10 个公开的 **OperationSets**。</span><span class="sxs-lookup"><span data-stu-id="58b3e-195">Each user can only have a maximum of 10 open **OperationSets**.</span></span>
- <span data-ttu-id="58b3e-196">Project Operations 目前对一个项目最多支持总共 500 个任务。</span><span class="sxs-lookup"><span data-stu-id="58b3e-196">Project Operations currently supports a maximum of 500 total tasks on a project.</span></span>
- <span data-ttu-id="58b3e-197">**OperationSet** 故障状态和故障日志当前不可用。</span><span class="sxs-lookup"><span data-stu-id="58b3e-197">**OperationSet** failure status and failure logs aren't currently available.</span></span>
- <span data-ttu-id="58b3e-198">计划 API 为公开预览版。</span><span class="sxs-lookup"><span data-stu-id="58b3e-198">Schedule APIs are in Public preview.</span></span> <span data-ttu-id="58b3e-199">Microsoft 不支持在生产环境中使用这些 API。</span><span class="sxs-lookup"><span data-stu-id="58b3e-199">Using these APIs in a Production environment isn't supported by Microsoft.</span></span>

## <a name="sample-scenario"></a><span data-ttu-id="58b3e-200">示例方案</span><span class="sxs-lookup"><span data-stu-id="58b3e-200">Sample scenario</span></span>

<span data-ttu-id="58b3e-201">在此方案中，您将创建一个项目、一个团队成员、四个任务和两个资源分派。</span><span class="sxs-lookup"><span data-stu-id="58b3e-201">In this scenario, you will create a project, a team member, four tasks, and two resource assignments.</span></span> <span data-ttu-id="58b3e-202">接下来，您将更新一个任务、更新项目、删除一个任务、删除一个资源分派以及创建任务依赖项。</span><span class="sxs-lookup"><span data-stu-id="58b3e-202">Next, you will update one task, update the project, delete one task, delete one resource assignment, and create a task dependency.</span></span>

```C#
Entity project = CreateProject();
project.Id = CallCreateProjectAction(project);
var projectReference = project.ToEntityReference();

var teamMember = new Entity("msdyn_projectteam", Guid.NewGuid());
teamMember["msdyn_name"] = $"TM {DateTime.Now.ToShortTimeString()}";
teamMember["msdyn_project"] = projectReference;
var createTeamMemberResponse = CallCreateTeamMemberAction(teamMember);

var description = $"My demo {DateTime.Now.ToShortTimeString()}";
var operationSetId = CallCreateOperationSetAction(project.Id, description);

var task1 = GetTask("1WW", projectReference);
var task2 = GetTask("2XX", projectReference, task1.ToEntityReference());
var task3 = GetTask("3YY", projectReference);
var task4 = GetTask("4ZZ";, projectReference);

var assignment1 = GetResourceAssignment("R1", teamMember, task2, project);
var assignment2 = GetResourceAssignment"R2", teamMember, task3, project);

var task1Response = CallPssCreateAction(task1, operationSetId);
var task2Response = CallPssCreateAction(task2, operationSetId);
var task3Response = CallPssCreateAction(task3, operationSetId);
var task4Response = CallPssCreateAction(task4, operationSetId);

varassignment1Response = CallPssCreateAction(assignment1, operationSetId);
varassignment2Response = CallPssCreateAction(assignment2, operationSetId);

task2["msdyn_subject"] = "Updated Task";
var task2UpdateResponse = CallPssUpdateAction(task2, operationSetId);

project["msdyn_subject"] = $"Proj update {DateTime.Now.ToShortTimeString()}";
var projectUpdateResponse = CallPssUpdateAction(project, operationSetId);

var task4DeleteResponse = CallPssDeleteAction(task4.Id.ToString(), task4.LogicalName, operationSetId);

varassignment2DeleteResponse = CallPssDeleteAction(assignment2.Id.ToString(), assignment2.LogicalName, operationSetId);

var dependency1 = GetTaskDependency(project, task2, task3);
var dependency1Response = CallPssCreateAction(dependency1, operationSetId);

CallExecuteOperationSetAction(operationSetId);
Console.WriteLine("Done....");
```

## <a name="additional-samples"></a><span data-ttu-id="58b3e-203">其他示例</span><span class="sxs-lookup"><span data-stu-id="58b3e-203">Additional samples</span></span>

```C#
#region Call actions 

///<summary>
/// Calls the action to create an operationSet
/// </summary>
/// <paramname="projectId">project id for the operations to be included in this operationSet>/param>
/// <paramname="description">description of this operationSet</param>
/// <returns>operationSet id</returns>
privatestring CallCreateOperationSetAction(Guid projectId, string description)
{
    OrganizationRequest operationSetRequest = new OrganizationRequest("msdyn_CreateOperationSetV1");
    operationSetRequest["ProjectId"] = projectId.ToString();
    operationSetRequest["Description"] = description;
    OrganizationResponse response = organizationService.Execute(operationSetRequest);
    return response["OperationSetId"].ToString();
}

/// <summary>
/// Calls the action to create an entity, only Task and Resource Assignment for now
/// </summary>
/// <paramname="entity">Task or Resource Assignment</param>
/// <paramname="operationSetId">operationSet id</param>
/// <returns>OperationSetResponse</returns>
private OperationSetResponse CallPssCreateAction(Entity entity, string operationSetId)
{
    OrganizationRequest operationSetRequest = new OrganizationRequest("msdyn_PssCreateV1");
    operationSetRequest["Entity"] = entity;
    operationSetRequest["OperationSetId"] = operationSetId;
    return GetOperationSetResponseFromOrgResponse(organizationService.Execute(operationSetRequest));
}

/// <summary<
/// Calls the action to update an entity, only Task for now
/// </summary>
/// <paramname="entity">Task or Resource Assignment</param>
/// <paramname="operationSetId">operationSet Id</param>
/// <returns>OperationSetResponse</returns>
private OperationSetResponse CallPssUpdateAction(Entity entity, string operationSetId)
{
    OrganizationRequest operationSetRequest = new OrganizationRequest("msdyn_PssUpdateV1");
    operationSetRequest["Entity"] = entity;
    operationSetRequest["OperationSetId"] = operationSetId;
    return GetOperationSetResponseFromOrgResponse(organizationService.Execute(operationSetRequest));
}

/// <summary>
/// Calls the action to update an entity, only Task and Resource Assignment for now
/// <summary>
/// <paramname="recordId">Id of the record to be deleted</param>
/// <paramname="entityLogicalName">Entity logical name of the record</param>
/// <paramname="operationSetId">OperationSet Id</param>
/// <returns>OperationSetResponse</returns>
private OperationSetResponse CallPssDeleteAction(string recordId, string entityLogicalName, string operationSetId)
{
    OrganizationRequest operationSetRequest = new OrganizationRequest("msdyn_PssDeleteV1");
    operationSetRequest["RecordId"] = recordId;
    operationSetRequest["EntityLogicalName"] = entityLogicalName;
    operationSetRequest["OperationSetId"] = operationSetId;
    return GetOperationSetResponseFromOrgResponse(organizationService.Execute(operationSetRequest));
}

/// <summary>
/// Calls the action to execute requests in an operationSet
/// <summary>
/// <paramname="operationSetId">operationSet id</param>
/// <returns>OperationSetResponse</returns>
private OperationSetResponse CallExecuteOperationSetAction(string operationSetId)
{
    OrganizationRequest operationSetRequest = new OrganizationRequest("msdyn_ExecuteOperationSetV1");
    operationSetRequest["OperationSetId"] = operationSetId;
    return GetOperationSetResponseFromOrgResponse(organizationService.Execute(operationSetRequest));
}

/// <summary>
/// This can be used to abandon an operationSet that is no longer needed
/// </summary>
/// <paramname="operationSetId">operationSet id</param>
/// <returns>OperationSetResponse</returns>
protected OperationSetResponse CallAbandonOperationSetAction(Guid operationSetId)
{
    OrganizationRequest operationSetRequest = new OrganizationRequest("msdyn_AbandonOperationSetV1");
    operationSetRequest["OperationSetId"] = operationSetId.ToString();
    return GetOperationSetResponseFromOrgResponse(organizationService.Execute(operationSetRequest));
}

/// <summary>
/// Calls the action to create a new project
/// </summary>
/// <paramname="project">Project</param>
/// <returns>project Id</returns>
private Guid CallCreateProjectAction(Entity project)
{
    OrganizationRequest createProjectRequest = new OrganizationRequest("msdyn_CreateProjectV1";
    createProjectRequest["Project"] = project;
    OrganizationResponse response = organizationService.Execute(createProjectRequest);
    var projectId = Guid.Parse((string)response["ProjectId"]);

    return projectId;
}

/// <summary>
/// Calls the action to create a new project team member
/// </summary>
/// <paramname="teamMember">Project team member</param>
/// <returns>project team member Id</returns>
privatestring CallCreateTeamMemberAction(Entity teamMember)
{
    OrganizationRequest request = new OrganizationRequest("msdyn_CreateTeamMemberV1");
    request["TeamMember"] = teamMember;
    OrganizationResponse response = organizationService.Execute(request);
    return (string)response["TeamMemberId"];
}

private OperationSetResponse GetOperationSetResponseFromOrgResponse(OrganizationResponse orgResponse)
{
    return JsonConvert.DeserializeObject><OperationSetResponse>
    ((string)orgResponse.Results["OperationSetResponse";]);
}

private EntityCollection GetDefaultBucket(EntityReference projectReference)
{
    var columnsToFetch = new ColumnSet(";msdyn_project", "msdyn_name");
    var getDefaultBucket = new QueryExpression("msdyn_projectbucket")
    {
        ColumnSet = columnsToFetch,
        Criteria =
        {
            Conditions =
            {
                new ConditionExpression("msdyn_project", ConditionOperator.Equal, projectReference.Id),
                new ConditionExpression("msdyn_name", ConditionOperator.Equal, "Bucket 1")
            }
        }
    };
    return organizationService.RetrieveMultiple(getDefaultBucket);
}

private Entity GetBucket(EntityReference projectReference)
{
    var bucketCollection = GetDefaultBucket(projectReference);
    if (bucketCollection.Entities.Count > 0)
    {
    return bucketCollection[0].ToEntity<Entity>();
    }

    throw new Exception($"Please open project with id {projectReference.Id} in the Dynamics UI and navigate to the Tasks tab");
}

private Entity CreateProject()
{
    var project = new Entity("msdyn_project", Guid.NewGuid());
    project["msdyn_subject"] = $"Proj {DateTime.Now.ToShortTimeString()}";
    return project;
}

private Entity GetTask(string name, EntityReference projectReference, EntityReference parentReference = null)
{
    var task = new Entity("msdyn_projecttask", Guid.NewGuid());
    task["msdyn_project"] = projectReference;
    task["msdyn_subject"] = name;
    task["msdyn_effort";] = 4d;
    task["msdyn_scheduledstart"] = DateTime.Today;
    task["msdyn_scheduledend"] = DateTime.Today.AddDays(5);
    task["msdyn_progress"] = 0.34m;
    task["msdyn_start"] = DateTime.Now.AddDays(1);
    task["msdyn_projectbucket"] = GetBucket(projectReference).ToEntityReference();
    task["msdyn_LinkStatus"] = new OptionSetValue(192350000);

    //Custom field handling
    /*
        task["new_custom1"] = "Just my test";
        task[";new_age"] = 98;
        task["new_amount"] = 591.34m;
        task["new_isready"] = new OptionSetValue(100000000);
    */

    if (parentReference == null)
    {
        task["msdyn_outlinelevel"] = 1;
    }
    else
    {
        task["msdyn_parenttask"] = parentReference;
    }
    return task;
}

private Entity GetResourceAssignment(string name, Entity teamMember, Entity task, Entity project)
{
    var assignment = new Entity("msdyn_resourceassignment", Guid.NewGuid());
    assignment["msdyn_projectteamid"] = teamMember.ToEntityReference();
    assignment["msdyn_taskid"] = task.ToEntityReference();
    assignment["msdyn_projectid"] = project.ToEntityReference();
    assignment["msdyn_name"] = name;
    assignment["msdyn_start"] = DateTime.Now;
    assignment["msdyn_finish"] = DateTime.Now;
    return assignment;
}

protected Entity GetTaskDependency(Entity project, Entity predecessor, Entity successor)
{
    var taskDependency = new Entity("msdyn_projecttaskdependency", Guid.NewGuid());
    taskDependency["msdyn_project"] = project.ToEntityReference();
    taskDependency["msdyn_predecessortask"] = predecessor.ToEntityReference();
    taskDependency["msdyn_successortask"] = successor.ToEntityReference();
    taskDependency["msdyn_linktype"] = new OptionSetValue(192350000);
    return taskDependency;
}

#endregion

#region OperationSetResponse DataContract --- Sample code ----

[DataContract]
publicclassOperationSetResponse
{
    [DataMember(Name = "operationSetId")]
    public Guid OperationSetId { get; set; }

    [DataMember(Name = "operationSetDetailId")]
    public Guid OperationSetDetailId { get; set; }

    [DataMember(Name = "operationType")]
    publicstring OperationType { get; set; }

    [DataMember(Name = "recordId")]
    publicstring RecordId { get; set; }

    [DataMember(Name = "correlationId")]
    publicstring CorrelationId { get; set; }
}

#endregion
```
