---
title: 使用项目计划 API 对计划实体执行操作
description: 本主题提供有关使用项目计划 API 的信息和示例。
author: sigitac
ms.date: 06/22/2021
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 4915261c08a3271a919e04084e92a14b297c1b35
ms.sourcegitcommit: 2f16c2bc7c8350676a6a380c61fffa9958db6a0b
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/22/2021
ms.locfileid: "6293216"
---
# <a name="use-project-schedule-apis-to-perform-operations-with-scheduling-entities"></a><span data-ttu-id="8940b-103">使用项目计划 API 对计划实体执行操作</span><span class="sxs-lookup"><span data-stu-id="8940b-103">Use Project schedule APIs to perform operations with Scheduling entities</span></span>

<span data-ttu-id="8940b-104">_**适用于：** 基于资源/非库存场景的 Project Operations，精简部署 - 估价开票交易_</span><span class="sxs-lookup"><span data-stu-id="8940b-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

> [!IMPORTANT] 
> <span data-ttu-id="8940b-105">本主题中所述的部分或所有功能属于预览版内容。</span><span class="sxs-lookup"><span data-stu-id="8940b-105">Some or all of the functionality noted in this topic is available as part of a preview release.</span></span> <span data-ttu-id="8940b-106">相关内容和功能可能会发生更改。</span><span class="sxs-lookup"><span data-stu-id="8940b-106">The content and the functionality are subject to change.</span></span> 

## <a name="scheduling-entities"></a><span data-ttu-id="8940b-107">计划实体</span><span class="sxs-lookup"><span data-stu-id="8940b-107">Scheduling entities</span></span>

<span data-ttu-id="8940b-108">项目计划 API 提供对 **计划实体** 执行创建、更新和删除操作的能力。</span><span class="sxs-lookup"><span data-stu-id="8940b-108">Project schedule APIs provide the ability to perform create, update, and delete operations with **Scheduling entities**.</span></span> <span data-ttu-id="8940b-109">这些实体通过 Web 项目中的计划引擎进行管理。</span><span class="sxs-lookup"><span data-stu-id="8940b-109">These entities are managed through the Scheduling engine in Project for the web.</span></span> <span data-ttu-id="8940b-110">早期 Dynamics 365 Project Operations 版本中限制对 **计划实体** 执行创建、更新和删除操作。</span><span class="sxs-lookup"><span data-stu-id="8940b-110">Create, update, and delete operations with **Scheduling entities** were restricted in earlier Dynamics 365 Project Operations releases.</span></span>

<span data-ttu-id="8940b-111">下表提供了项目计划实体的完整列表。</span><span class="sxs-lookup"><span data-stu-id="8940b-111">The following table provides a full list of the Project schedule entities.</span></span>

| <span data-ttu-id="8940b-112">实体名称</span><span class="sxs-lookup"><span data-stu-id="8940b-112">Entity name</span></span>  | <span data-ttu-id="8940b-113">实体逻辑名称</span><span class="sxs-lookup"><span data-stu-id="8940b-113">Entity logical name</span></span> |
| --- | --- |
| <span data-ttu-id="8940b-114">Project</span><span class="sxs-lookup"><span data-stu-id="8940b-114">Project</span></span> | <span data-ttu-id="8940b-115">msdyn_project</span><span class="sxs-lookup"><span data-stu-id="8940b-115">msdyn_project</span></span> |
| <span data-ttu-id="8940b-116">项目任务</span><span class="sxs-lookup"><span data-stu-id="8940b-116">Project Task</span></span>  | <span data-ttu-id="8940b-117">msdyn_projecttask</span><span class="sxs-lookup"><span data-stu-id="8940b-117">msdyn_projecttask</span></span>  |
| <span data-ttu-id="8940b-118">项目任务依赖关系</span><span class="sxs-lookup"><span data-stu-id="8940b-118">Project Task Dependency</span></span>  | <span data-ttu-id="8940b-119">msdyn_projecttaskdependency</span><span class="sxs-lookup"><span data-stu-id="8940b-119">msdyn_projecttaskdependency</span></span>  |
| <span data-ttu-id="8940b-120">资源分派</span><span class="sxs-lookup"><span data-stu-id="8940b-120">Resource Assignment</span></span> | <span data-ttu-id="8940b-121">msdyn_resourceassignment</span><span class="sxs-lookup"><span data-stu-id="8940b-121">msdyn_resourceassignment</span></span> |
| <span data-ttu-id="8940b-122">项目 Bucket</span><span class="sxs-lookup"><span data-stu-id="8940b-122">Project Bucket</span></span>  | <span data-ttu-id="8940b-123">msdyn_projectbucket</span><span class="sxs-lookup"><span data-stu-id="8940b-123">msdyn_projectbucket</span></span> |
| <span data-ttu-id="8940b-124">项目团队成员</span><span class="sxs-lookup"><span data-stu-id="8940b-124">Project Team Member</span></span> | <span data-ttu-id="8940b-125">msdyn_projectteam</span><span class="sxs-lookup"><span data-stu-id="8940b-125">msdyn_projectteam</span></span> |

## <a name="operationset"></a><span data-ttu-id="8940b-126">OperationSet</span><span class="sxs-lookup"><span data-stu-id="8940b-126">OperationSet</span></span>

<span data-ttu-id="8940b-127">OperationSet 是一种工作单位模式，当必须在交易内处理多个计划影响请求时，可以使用该模式。</span><span class="sxs-lookup"><span data-stu-id="8940b-127">OperationSet is a unit-of-work pattern that can be used when several schedule impacting requests must be processed within a transaction.</span></span>

## <a name="project-schedule-apis"></a><span data-ttu-id="8940b-128">项目计划 API</span><span class="sxs-lookup"><span data-stu-id="8940b-128">Project schedule APIs</span></span>

<span data-ttu-id="8940b-129">下面是当前项目计划 API 的列表。</span><span class="sxs-lookup"><span data-stu-id="8940b-129">The following is a list of current Project schedule APIs.</span></span>

- <span data-ttu-id="8940b-130">**msdyn_CreateProjectV1**：此 API 可用于创建项目。</span><span class="sxs-lookup"><span data-stu-id="8940b-130">**msdyn_CreateProjectV1**: This API can be used to create a project.</span></span> <span data-ttu-id="8940b-131">将立即创建项目和默认项目 Bucket。</span><span class="sxs-lookup"><span data-stu-id="8940b-131">The project and default project bucket is created immediately.</span></span>
- <span data-ttu-id="8940b-132">**msdyn_CreateTeamMemberV1**：此 API 可用于创建项目团队成员。</span><span class="sxs-lookup"><span data-stu-id="8940b-132">**msdyn_CreateTeamMemberV1**: This API can be used to create a project team member.</span></span> <span data-ttu-id="8940b-133">系统会立即创建团队成员记录。</span><span class="sxs-lookup"><span data-stu-id="8940b-133">The team member record is created immediately.</span></span>
- <span data-ttu-id="8940b-134">**msdyn_CreateOperationSetV1**：此 API 可用于安排必须在交易中执行多个请求。</span><span class="sxs-lookup"><span data-stu-id="8940b-134">**msdyn_CreateOperationSetV1**: This API can be used to schedule several requests that must be performed within a transaction.</span></span>
- <span data-ttu-id="8940b-135">**msdyn_PSSCreateV1**：此 API 可用于创建实体。</span><span class="sxs-lookup"><span data-stu-id="8940b-135">**msdyn_PSSCreateV1**: This API can be used to create an entity.</span></span> <span data-ttu-id="8940b-136">该实体可以是支持创建操作的任何项目计划实体。</span><span class="sxs-lookup"><span data-stu-id="8940b-136">The entity can be any of the Project scheduling entities that support the create operation.</span></span>
- <span data-ttu-id="8940b-137">**msdyn_PSSUpdateV1**：此 API 可用于更新实体。</span><span class="sxs-lookup"><span data-stu-id="8940b-137">**msdyn_PSSUpdateV1**: This API can be used to update an entity.</span></span> <span data-ttu-id="8940b-138">该实体可以是支持更新操作的任何项目计划实体。</span><span class="sxs-lookup"><span data-stu-id="8940b-138">The entity can be any of the Project scheduling entities that support the update operation.</span></span>
- <span data-ttu-id="8940b-139">**msdyn_PSSDeleteV1**：此 API 可用于删除实体。</span><span class="sxs-lookup"><span data-stu-id="8940b-139">**msdyn_PSSDeleteV1**: This API can be used to delete an entity.</span></span> <span data-ttu-id="8940b-140">该实体可以是支持删除操作的任何项目计划实体。</span><span class="sxs-lookup"><span data-stu-id="8940b-140">The entity can be any of the Project scheduling entities that support the delete operation.</span></span>
- <span data-ttu-id="8940b-141">**msdyn_ExecuteOperationSetV1**：此 API 用于执行给定操作集内的所有操作。</span><span class="sxs-lookup"><span data-stu-id="8940b-141">**msdyn_ExecuteOperationSetV1**: This API is used to execute all of the operations within the given operation set.</span></span>

## <a name="using-project-schedule-apis-with-operationset"></a><span data-ttu-id="8940b-142">将项目计划 API 与 OperationSet 一起使用</span><span class="sxs-lookup"><span data-stu-id="8940b-142">Using Project schedule APIs with OperationSet</span></span>

<span data-ttu-id="8940b-143">由于会立即创建同时具有 **CreateProjectV1** 和 **CreateTeamMemberV1** 的记录，因此这些 API 不能直接在 **OperationSet** 中使用。</span><span class="sxs-lookup"><span data-stu-id="8940b-143">Because records with both **CreateProjectV1** and **CreateTeamMemberV1** are created immediately, these APIs can't be used in the **OperationSet** directly.</span></span> <span data-ttu-id="8940b-144">但是，可以使用 API 创建所需记录，创建 **OperationSet**，然后在 **OperationSet** 中使用这些预先创建的记录。</span><span class="sxs-lookup"><span data-stu-id="8940b-144">However, you can use the API to create needed records, create an **OperationSet**, and then use these pre-created records in the **OperationSet**.</span></span>

## <a name="supported-operations"></a><span data-ttu-id="8940b-145">不支持的操作</span><span class="sxs-lookup"><span data-stu-id="8940b-145">Supported operations</span></span>

| <span data-ttu-id="8940b-146">计划实体</span><span class="sxs-lookup"><span data-stu-id="8940b-146">Scheduling entity</span></span> | <span data-ttu-id="8940b-147">创建​​</span><span class="sxs-lookup"><span data-stu-id="8940b-147">Create</span></span> | <span data-ttu-id="8940b-148">更新</span><span class="sxs-lookup"><span data-stu-id="8940b-148">Update</span></span> | <span data-ttu-id="8940b-149">Delete</span><span class="sxs-lookup"><span data-stu-id="8940b-149">Delete</span></span> | <span data-ttu-id="8940b-150">重要考虑因素</span><span class="sxs-lookup"><span data-stu-id="8940b-150">Important considerations</span></span> |
| --- | --- | --- | --- | --- |
<span data-ttu-id="8940b-151">项目任务</span><span class="sxs-lookup"><span data-stu-id="8940b-151">Project task</span></span> | <span data-ttu-id="8940b-152">是</span><span class="sxs-lookup"><span data-stu-id="8940b-152">Yes</span></span> | <span data-ttu-id="8940b-153">是</span><span class="sxs-lookup"><span data-stu-id="8940b-153">Yes</span></span> | <span data-ttu-id="8940b-154">是</span><span class="sxs-lookup"><span data-stu-id="8940b-154">Yes</span></span> | <span data-ttu-id="8940b-155">无​</span><span class="sxs-lookup"><span data-stu-id="8940b-155">None</span></span> |
| <span data-ttu-id="8940b-156">项目任务依赖关系</span><span class="sxs-lookup"><span data-stu-id="8940b-156">Project task dependency</span></span> | <span data-ttu-id="8940b-157">是</span><span class="sxs-lookup"><span data-stu-id="8940b-157">Yes</span></span> | <span data-ttu-id="8940b-158">是</span><span class="sxs-lookup"><span data-stu-id="8940b-158">Yes</span></span> | | <span data-ttu-id="8940b-159">不会更新项目任务依赖关系记录。</span><span class="sxs-lookup"><span data-stu-id="8940b-159">Project task dependency records aren't updated.</span></span> <span data-ttu-id="8940b-160">而是可以删除旧记录，并可以创建新记录。</span><span class="sxs-lookup"><span data-stu-id="8940b-160">Instead, an old record can be deleted and a new record can be created.</span></span> |
| <span data-ttu-id="8940b-161">资源分派</span><span class="sxs-lookup"><span data-stu-id="8940b-161">Resource assignment</span></span> | <span data-ttu-id="8940b-162">是</span><span class="sxs-lookup"><span data-stu-id="8940b-162">Yes</span></span> | <span data-ttu-id="8940b-163">是</span><span class="sxs-lookup"><span data-stu-id="8940b-163">Yes</span></span> | | <span data-ttu-id="8940b-164">不支持对以下字段执行操作：**BookableResourceID**、**Effort**、**EffortCompleted**、**EffortRemaining** 和 **PlannedWork**。</span><span class="sxs-lookup"><span data-stu-id="8940b-164">Operations with the following fields aren't supported: **BookableResourceID**, **Effort**, **EffortCompleted**, **EffortRemaining**, and **PlannedWork**.</span></span> <span data-ttu-id="8940b-165">资源分派记录不会更新。</span><span class="sxs-lookup"><span data-stu-id="8940b-165">Resource assignment records aren't updated.</span></span> <span data-ttu-id="8940b-166">而是可以删除旧记录，并可以创建新记录。</span><span class="sxs-lookup"><span data-stu-id="8940b-166">Instead, the old record can be deleted and a new record can be created.</span></span> |
| <span data-ttu-id="8940b-167">项目 Bucket</span><span class="sxs-lookup"><span data-stu-id="8940b-167">Project bucket</span></span> | <span data-ttu-id="8940b-168">不适用</span><span class="sxs-lookup"><span data-stu-id="8940b-168">N/A</span></span> | <span data-ttu-id="8940b-169">不适用</span><span class="sxs-lookup"><span data-stu-id="8940b-169">N/A</span></span> | <span data-ttu-id="8940b-170">不适用</span><span class="sxs-lookup"><span data-stu-id="8940b-170">N/A</span></span> | <span data-ttu-id="8940b-171">使用 **CreateProjectV1** API 创建了默认 Bucket。</span><span class="sxs-lookup"><span data-stu-id="8940b-171">The default bucket is created using the **CreateProjectV1** API.</span></span> |
| <span data-ttu-id="8940b-172">项目团队成员</span><span class="sxs-lookup"><span data-stu-id="8940b-172">Project team member</span></span> | <span data-ttu-id="8940b-173">是</span><span class="sxs-lookup"><span data-stu-id="8940b-173">Yes</span></span> | <span data-ttu-id="8940b-174">是</span><span class="sxs-lookup"><span data-stu-id="8940b-174">Yes</span></span> | <span data-ttu-id="8940b-175">是</span><span class="sxs-lookup"><span data-stu-id="8940b-175">Yes</span></span> | <span data-ttu-id="8940b-176">对于创建操作，请使用 **CreateTeamMemberV1** API。</span><span class="sxs-lookup"><span data-stu-id="8940b-176">For the create operation, use the **CreateTeamMemberV1** API.</span></span> |
| <span data-ttu-id="8940b-177">Project</span><span class="sxs-lookup"><span data-stu-id="8940b-177">Project</span></span> | <span data-ttu-id="8940b-178">是</span><span class="sxs-lookup"><span data-stu-id="8940b-178">Yes</span></span> | <span data-ttu-id="8940b-179">是</span><span class="sxs-lookup"><span data-stu-id="8940b-179">Yes</span></span> | <span data-ttu-id="8940b-180">不适用</span><span class="sxs-lookup"><span data-stu-id="8940b-180">N/A</span></span> | <span data-ttu-id="8940b-181">不支持以下对字段执行操作：**StateCode**、**BulkGenerationStatus**、**GlobalRevisionToken**、**CalendarID**、**Effort**、**EffortCompleted**、**EffortRemaining**、**Progress**、**Finish**、**TaskEarliestStart** 和 **Duration**。</span><span class="sxs-lookup"><span data-stu-id="8940b-181">Operations with the following fields aren't supported: **StateCode**, **BulkGenerationStatus**, **GlobalRevisionToken**, **CalendarID**, **Effort**, **EffortCompleted**, **EffortRemaining**, **Progress**, **Finish**, **TaskEarliestStart**, and **Duration**.</span></span> |

<span data-ttu-id="8940b-182">可以对包含自定义字段的实体对象调用这些 API。</span><span class="sxs-lookup"><span data-stu-id="8940b-182">These APIs can be called with entity objects that include custom fields.</span></span>

<span data-ttu-id="8940b-183">ID 属性是可选的。</span><span class="sxs-lookup"><span data-stu-id="8940b-183">The ID property is optional.</span></span> <span data-ttu-id="8940b-184">如果提供了此属性，则系统会尝试使用它，如果无法使用它，则会引发异常。</span><span class="sxs-lookup"><span data-stu-id="8940b-184">If it's provided, the system attempts to use it and throws an exception if it can't be used.</span></span> <span data-ttu-id="8940b-185">如果未提供此属性，系统将生成它。</span><span class="sxs-lookup"><span data-stu-id="8940b-185">If it isn't provided, the system will generate it.</span></span>

## <a name="restricted-fields"></a><span data-ttu-id="8940b-186">受限字段</span><span class="sxs-lookup"><span data-stu-id="8940b-186">Restricted fields</span></span>

<span data-ttu-id="8940b-187">下表定义了限制对其进行 **创建** 和 **编辑** 的字段。</span><span class="sxs-lookup"><span data-stu-id="8940b-187">The following tables define the fields that are restricted from **Create** and **Edit.**</span></span>

### <a name="project-task"></a><span data-ttu-id="8940b-188">项目任务</span><span class="sxs-lookup"><span data-stu-id="8940b-188">Project task</span></span>

| <span data-ttu-id="8940b-189">**逻辑名称**</span><span class="sxs-lookup"><span data-stu-id="8940b-189">**Logical name**</span></span>                       | <span data-ttu-id="8940b-190">**可创建**</span><span class="sxs-lookup"><span data-stu-id="8940b-190">**Can create**</span></span> | <span data-ttu-id="8940b-191">**可编辑**</span><span class="sxs-lookup"><span data-stu-id="8940b-191">**Can edit**</span></span>     |
|----------------------------------------|----------------|------------------|
| <span data-ttu-id="8940b-192">msdyn_actualcost</span><span class="sxs-lookup"><span data-stu-id="8940b-192">msdyn_actualcost</span></span>                       | <span data-ttu-id="8940b-193">否</span><span class="sxs-lookup"><span data-stu-id="8940b-193">no</span></span>             | <span data-ttu-id="8940b-194">否</span><span class="sxs-lookup"><span data-stu-id="8940b-194">no</span></span>               |
| <span data-ttu-id="8940b-195">msdyn_actualcost_base</span><span class="sxs-lookup"><span data-stu-id="8940b-195">msdyn_actualcost_base</span></span>                  | <span data-ttu-id="8940b-196">否</span><span class="sxs-lookup"><span data-stu-id="8940b-196">no</span></span>             | <span data-ttu-id="8940b-197">否</span><span class="sxs-lookup"><span data-stu-id="8940b-197">no</span></span>               |
| <span data-ttu-id="8940b-198">msdyn_actualend</span><span class="sxs-lookup"><span data-stu-id="8940b-198">msdyn_actualend</span></span>                        | <span data-ttu-id="8940b-199">否</span><span class="sxs-lookup"><span data-stu-id="8940b-199">no</span></span>             | <span data-ttu-id="8940b-200">否</span><span class="sxs-lookup"><span data-stu-id="8940b-200">no</span></span>               |
| <span data-ttu-id="8940b-201">msdyn_actualsales</span><span class="sxs-lookup"><span data-stu-id="8940b-201">msdyn_actualsales</span></span>                      | <span data-ttu-id="8940b-202">否</span><span class="sxs-lookup"><span data-stu-id="8940b-202">no</span></span>             | <span data-ttu-id="8940b-203">否</span><span class="sxs-lookup"><span data-stu-id="8940b-203">no</span></span>               |
| <span data-ttu-id="8940b-204">msdyn_actualsales_base</span><span class="sxs-lookup"><span data-stu-id="8940b-204">msdyn_actualsales_base</span></span>                 | <span data-ttu-id="8940b-205">否</span><span class="sxs-lookup"><span data-stu-id="8940b-205">no</span></span>             | <span data-ttu-id="8940b-206">否</span><span class="sxs-lookup"><span data-stu-id="8940b-206">no</span></span>               |
| <span data-ttu-id="8940b-207">msdyn_actualstart</span><span class="sxs-lookup"><span data-stu-id="8940b-207">msdyn_actualstart</span></span>                      | <span data-ttu-id="8940b-208">否</span><span class="sxs-lookup"><span data-stu-id="8940b-208">no</span></span>             | <span data-ttu-id="8940b-209">否</span><span class="sxs-lookup"><span data-stu-id="8940b-209">no</span></span>               |
| <span data-ttu-id="8940b-210">msdyn_costatcompleteestimate</span><span class="sxs-lookup"><span data-stu-id="8940b-210">msdyn_costatcompleteestimate</span></span>           | <span data-ttu-id="8940b-211">否</span><span class="sxs-lookup"><span data-stu-id="8940b-211">no</span></span>             | <span data-ttu-id="8940b-212">否</span><span class="sxs-lookup"><span data-stu-id="8940b-212">no</span></span>               |
| <span data-ttu-id="8940b-213">msdyn_costatcompleteestimate_base</span><span class="sxs-lookup"><span data-stu-id="8940b-213">msdyn_costatcompleteestimate_base</span></span>      | <span data-ttu-id="8940b-214">否</span><span class="sxs-lookup"><span data-stu-id="8940b-214">no</span></span>             | <span data-ttu-id="8940b-215">否</span><span class="sxs-lookup"><span data-stu-id="8940b-215">no</span></span>               |
| <span data-ttu-id="8940b-216">msdyn_costconsumptionpercentage</span><span class="sxs-lookup"><span data-stu-id="8940b-216">msdyn_costconsumptionpercentage</span></span>        | <span data-ttu-id="8940b-217">否</span><span class="sxs-lookup"><span data-stu-id="8940b-217">no</span></span>             | <span data-ttu-id="8940b-218">否</span><span class="sxs-lookup"><span data-stu-id="8940b-218">no</span></span>               |
| <span data-ttu-id="8940b-219">msdyn_effortcompleted</span><span class="sxs-lookup"><span data-stu-id="8940b-219">msdyn_effortcompleted</span></span>                  | <span data-ttu-id="8940b-220">否</span><span class="sxs-lookup"><span data-stu-id="8940b-220">no</span></span>             | <span data-ttu-id="8940b-221">否</span><span class="sxs-lookup"><span data-stu-id="8940b-221">no</span></span>               |
| <span data-ttu-id="8940b-222">msdyn_effortestimateatcomplete</span><span class="sxs-lookup"><span data-stu-id="8940b-222">msdyn_effortestimateatcomplete</span></span>         | <span data-ttu-id="8940b-223">否</span><span class="sxs-lookup"><span data-stu-id="8940b-223">no</span></span>             | <span data-ttu-id="8940b-224">否</span><span class="sxs-lookup"><span data-stu-id="8940b-224">no</span></span>               |
| <span data-ttu-id="8940b-225">msdyn_iscritical</span><span class="sxs-lookup"><span data-stu-id="8940b-225">msdyn_iscritical</span></span>                       | <span data-ttu-id="8940b-226">否</span><span class="sxs-lookup"><span data-stu-id="8940b-226">no</span></span>             | <span data-ttu-id="8940b-227">否</span><span class="sxs-lookup"><span data-stu-id="8940b-227">no</span></span>               |
| <span data-ttu-id="8940b-228">msdyn_iscriticalname</span><span class="sxs-lookup"><span data-stu-id="8940b-228">msdyn_iscriticalname</span></span>                   | <span data-ttu-id="8940b-229">否</span><span class="sxs-lookup"><span data-stu-id="8940b-229">no</span></span>             | <span data-ttu-id="8940b-230">否</span><span class="sxs-lookup"><span data-stu-id="8940b-230">no</span></span>               |
| <span data-ttu-id="8940b-231">msdyn_ismanual</span><span class="sxs-lookup"><span data-stu-id="8940b-231">msdyn_ismanual</span></span>                         | <span data-ttu-id="8940b-232">否</span><span class="sxs-lookup"><span data-stu-id="8940b-232">no</span></span>             | <span data-ttu-id="8940b-233">否</span><span class="sxs-lookup"><span data-stu-id="8940b-233">no</span></span>               |
| <span data-ttu-id="8940b-234">msdyn_ismanualname</span><span class="sxs-lookup"><span data-stu-id="8940b-234">msdyn_ismanualname</span></span>                     | <span data-ttu-id="8940b-235">否</span><span class="sxs-lookup"><span data-stu-id="8940b-235">no</span></span>             | <span data-ttu-id="8940b-236">否</span><span class="sxs-lookup"><span data-stu-id="8940b-236">no</span></span>               |
| <span data-ttu-id="8940b-237">msdyn_ismilestone</span><span class="sxs-lookup"><span data-stu-id="8940b-237">msdyn_ismilestone</span></span>                      | <span data-ttu-id="8940b-238">否</span><span class="sxs-lookup"><span data-stu-id="8940b-238">no</span></span>             | <span data-ttu-id="8940b-239">否</span><span class="sxs-lookup"><span data-stu-id="8940b-239">no</span></span>               |
| <span data-ttu-id="8940b-240">msdyn_ismilestonename</span><span class="sxs-lookup"><span data-stu-id="8940b-240">msdyn_ismilestonename</span></span>                  | <span data-ttu-id="8940b-241">否</span><span class="sxs-lookup"><span data-stu-id="8940b-241">no</span></span>             | <span data-ttu-id="8940b-242">否</span><span class="sxs-lookup"><span data-stu-id="8940b-242">no</span></span>               |
| <span data-ttu-id="8940b-243">msdyn_LinkStatus</span><span class="sxs-lookup"><span data-stu-id="8940b-243">msdyn_LinkStatus</span></span>                       | <span data-ttu-id="8940b-244">否</span><span class="sxs-lookup"><span data-stu-id="8940b-244">no</span></span>             | <span data-ttu-id="8940b-245">否</span><span class="sxs-lookup"><span data-stu-id="8940b-245">no</span></span>               |
| <span data-ttu-id="8940b-246">msdyn_linkstatusname</span><span class="sxs-lookup"><span data-stu-id="8940b-246">msdyn_linkstatusname</span></span>                   | <span data-ttu-id="8940b-247">否</span><span class="sxs-lookup"><span data-stu-id="8940b-247">no</span></span>             | <span data-ttu-id="8940b-248">否</span><span class="sxs-lookup"><span data-stu-id="8940b-248">no</span></span>               |
| <span data-ttu-id="8940b-249">msdyn_msprojectclientid</span><span class="sxs-lookup"><span data-stu-id="8940b-249">msdyn_msprojectclientid</span></span>                | <span data-ttu-id="8940b-250">否</span><span class="sxs-lookup"><span data-stu-id="8940b-250">no</span></span>             | <span data-ttu-id="8940b-251">否</span><span class="sxs-lookup"><span data-stu-id="8940b-251">no</span></span>               |
| <span data-ttu-id="8940b-252">msdyn_plannedcost</span><span class="sxs-lookup"><span data-stu-id="8940b-252">msdyn_plannedcost</span></span>                      | <span data-ttu-id="8940b-253">否</span><span class="sxs-lookup"><span data-stu-id="8940b-253">no</span></span>             | <span data-ttu-id="8940b-254">否</span><span class="sxs-lookup"><span data-stu-id="8940b-254">no</span></span>               |
| <span data-ttu-id="8940b-255">msdyn_plannedcost_base</span><span class="sxs-lookup"><span data-stu-id="8940b-255">msdyn_plannedcost_base</span></span>                 | <span data-ttu-id="8940b-256">否</span><span class="sxs-lookup"><span data-stu-id="8940b-256">no</span></span>             | <span data-ttu-id="8940b-257">否</span><span class="sxs-lookup"><span data-stu-id="8940b-257">no</span></span>               |
| <span data-ttu-id="8940b-258">msdyn_plannedsales</span><span class="sxs-lookup"><span data-stu-id="8940b-258">msdyn_plannedsales</span></span>                     | <span data-ttu-id="8940b-259">否</span><span class="sxs-lookup"><span data-stu-id="8940b-259">no</span></span>             | <span data-ttu-id="8940b-260">否</span><span class="sxs-lookup"><span data-stu-id="8940b-260">no</span></span>               |
| <span data-ttu-id="8940b-261">msdyn_plannedsales_base</span><span class="sxs-lookup"><span data-stu-id="8940b-261">msdyn_plannedsales_base</span></span>                | <span data-ttu-id="8940b-262">否</span><span class="sxs-lookup"><span data-stu-id="8940b-262">no</span></span>             | <span data-ttu-id="8940b-263">否</span><span class="sxs-lookup"><span data-stu-id="8940b-263">no</span></span>               |
| <span data-ttu-id="8940b-264">msdyn_pluginprocessingdata</span><span class="sxs-lookup"><span data-stu-id="8940b-264">msdyn_pluginprocessingdata</span></span>             | <span data-ttu-id="8940b-265">否</span><span class="sxs-lookup"><span data-stu-id="8940b-265">no</span></span>             | <span data-ttu-id="8940b-266">否</span><span class="sxs-lookup"><span data-stu-id="8940b-266">no</span></span>               |
| <span data-ttu-id="8940b-267">msdyn_progress</span><span class="sxs-lookup"><span data-stu-id="8940b-267">msdyn_progress</span></span>                         | <span data-ttu-id="8940b-268">否</span><span class="sxs-lookup"><span data-stu-id="8940b-268">no</span></span>             | <span data-ttu-id="8940b-269">否（P4W 为“是”）</span><span class="sxs-lookup"><span data-stu-id="8940b-269">no (yes for P4W)</span></span> |
| <span data-ttu-id="8940b-270">msdyn_remainingcost</span><span class="sxs-lookup"><span data-stu-id="8940b-270">msdyn_remainingcost</span></span>                    | <span data-ttu-id="8940b-271">否</span><span class="sxs-lookup"><span data-stu-id="8940b-271">no</span></span>             | <span data-ttu-id="8940b-272">否</span><span class="sxs-lookup"><span data-stu-id="8940b-272">no</span></span>               |
| <span data-ttu-id="8940b-273">msdyn_remainingcost_base</span><span class="sxs-lookup"><span data-stu-id="8940b-273">msdyn_remainingcost_base</span></span>               | <span data-ttu-id="8940b-274">否</span><span class="sxs-lookup"><span data-stu-id="8940b-274">no</span></span>             | <span data-ttu-id="8940b-275">否</span><span class="sxs-lookup"><span data-stu-id="8940b-275">no</span></span>               |
| <span data-ttu-id="8940b-276">msdyn_remainingsales</span><span class="sxs-lookup"><span data-stu-id="8940b-276">msdyn_remainingsales</span></span>                   | <span data-ttu-id="8940b-277">否</span><span class="sxs-lookup"><span data-stu-id="8940b-277">no</span></span>             | <span data-ttu-id="8940b-278">否</span><span class="sxs-lookup"><span data-stu-id="8940b-278">no</span></span>               |
| <span data-ttu-id="8940b-279">msdyn_remainingsales_base</span><span class="sxs-lookup"><span data-stu-id="8940b-279">msdyn_remainingsales_base</span></span>              | <span data-ttu-id="8940b-280">否</span><span class="sxs-lookup"><span data-stu-id="8940b-280">no</span></span>             | <span data-ttu-id="8940b-281">否</span><span class="sxs-lookup"><span data-stu-id="8940b-281">no</span></span>               |
| <span data-ttu-id="8940b-282">msdyn_requestedhours</span><span class="sxs-lookup"><span data-stu-id="8940b-282">msdyn_requestedhours</span></span>                   | <span data-ttu-id="8940b-283">否</span><span class="sxs-lookup"><span data-stu-id="8940b-283">no</span></span>             | <span data-ttu-id="8940b-284">否</span><span class="sxs-lookup"><span data-stu-id="8940b-284">no</span></span>               |
| <span data-ttu-id="8940b-285">msdyn_resourcecategory</span><span class="sxs-lookup"><span data-stu-id="8940b-285">msdyn_resourcecategory</span></span>                 | <span data-ttu-id="8940b-286">否</span><span class="sxs-lookup"><span data-stu-id="8940b-286">no</span></span>             | <span data-ttu-id="8940b-287">否</span><span class="sxs-lookup"><span data-stu-id="8940b-287">no</span></span>               |
| <span data-ttu-id="8940b-288">msdyn_resourcecategoryname</span><span class="sxs-lookup"><span data-stu-id="8940b-288">msdyn_resourcecategoryname</span></span>             | <span data-ttu-id="8940b-289">否</span><span class="sxs-lookup"><span data-stu-id="8940b-289">no</span></span>             | <span data-ttu-id="8940b-290">否</span><span class="sxs-lookup"><span data-stu-id="8940b-290">no</span></span>               |
| <span data-ttu-id="8940b-291">msdyn_resourceorganizationalunitid</span><span class="sxs-lookup"><span data-stu-id="8940b-291">msdyn_resourceorganizationalunitid</span></span>     | <span data-ttu-id="8940b-292">否</span><span class="sxs-lookup"><span data-stu-id="8940b-292">no</span></span>             | <span data-ttu-id="8940b-293">否</span><span class="sxs-lookup"><span data-stu-id="8940b-293">no</span></span>               |
| <span data-ttu-id="8940b-294">msdyn_resourceorganizationalunitidname</span><span class="sxs-lookup"><span data-stu-id="8940b-294">msdyn_resourceorganizationalunitidname</span></span> | <span data-ttu-id="8940b-295">否</span><span class="sxs-lookup"><span data-stu-id="8940b-295">no</span></span>             | <span data-ttu-id="8940b-296">否</span><span class="sxs-lookup"><span data-stu-id="8940b-296">no</span></span>               |
| <span data-ttu-id="8940b-297">msdyn_salesconsumptionpercentage</span><span class="sxs-lookup"><span data-stu-id="8940b-297">msdyn_salesconsumptionpercentage</span></span>       | <span data-ttu-id="8940b-298">否</span><span class="sxs-lookup"><span data-stu-id="8940b-298">no</span></span>             | <span data-ttu-id="8940b-299">否</span><span class="sxs-lookup"><span data-stu-id="8940b-299">no</span></span>               |
| <span data-ttu-id="8940b-300">msdyn_salesestimateatcomplete</span><span class="sxs-lookup"><span data-stu-id="8940b-300">msdyn_salesestimateatcomplete</span></span>          | <span data-ttu-id="8940b-301">否</span><span class="sxs-lookup"><span data-stu-id="8940b-301">no</span></span>             | <span data-ttu-id="8940b-302">否</span><span class="sxs-lookup"><span data-stu-id="8940b-302">no</span></span>               |
| <span data-ttu-id="8940b-303">msdyn_salesestimateatcomplete_base</span><span class="sxs-lookup"><span data-stu-id="8940b-303">msdyn_salesestimateatcomplete_base</span></span>     | <span data-ttu-id="8940b-304">否</span><span class="sxs-lookup"><span data-stu-id="8940b-304">no</span></span>             | <span data-ttu-id="8940b-305">否</span><span class="sxs-lookup"><span data-stu-id="8940b-305">no</span></span>               |
| <span data-ttu-id="8940b-306">msdyn_salesvariance</span><span class="sxs-lookup"><span data-stu-id="8940b-306">msdyn_salesvariance</span></span>                    | <span data-ttu-id="8940b-307">否</span><span class="sxs-lookup"><span data-stu-id="8940b-307">no</span></span>             | <span data-ttu-id="8940b-308">否</span><span class="sxs-lookup"><span data-stu-id="8940b-308">no</span></span>               |
| <span data-ttu-id="8940b-309">msdyn_salesvariance_base</span><span class="sxs-lookup"><span data-stu-id="8940b-309">msdyn_salesvariance_base</span></span>               | <span data-ttu-id="8940b-310">否</span><span class="sxs-lookup"><span data-stu-id="8940b-310">no</span></span>             | <span data-ttu-id="8940b-311">否</span><span class="sxs-lookup"><span data-stu-id="8940b-311">no</span></span>               |
| <span data-ttu-id="8940b-312">msdyn_scheduleddurationminutes</span><span class="sxs-lookup"><span data-stu-id="8940b-312">msdyn_scheduleddurationminutes</span></span>         | <span data-ttu-id="8940b-313">否</span><span class="sxs-lookup"><span data-stu-id="8940b-313">no</span></span>             | <span data-ttu-id="8940b-314">否</span><span class="sxs-lookup"><span data-stu-id="8940b-314">no</span></span>               |
| <span data-ttu-id="8940b-315">msdyn_scheduledend</span><span class="sxs-lookup"><span data-stu-id="8940b-315">msdyn_scheduledend</span></span>                     | <span data-ttu-id="8940b-316">否</span><span class="sxs-lookup"><span data-stu-id="8940b-316">no</span></span>             | <span data-ttu-id="8940b-317">否</span><span class="sxs-lookup"><span data-stu-id="8940b-317">no</span></span>               |
| <span data-ttu-id="8940b-318">msdyn_scheduledstart</span><span class="sxs-lookup"><span data-stu-id="8940b-318">msdyn_scheduledstart</span></span>                   | <span data-ttu-id="8940b-319">否</span><span class="sxs-lookup"><span data-stu-id="8940b-319">no</span></span>             | <span data-ttu-id="8940b-320">否</span><span class="sxs-lookup"><span data-stu-id="8940b-320">no</span></span>               |
| <span data-ttu-id="8940b-321">msdyn_schedulevariance</span><span class="sxs-lookup"><span data-stu-id="8940b-321">msdyn_schedulevariance</span></span>                 | <span data-ttu-id="8940b-322">否</span><span class="sxs-lookup"><span data-stu-id="8940b-322">no</span></span>             | <span data-ttu-id="8940b-323">否</span><span class="sxs-lookup"><span data-stu-id="8940b-323">no</span></span>               |
| <span data-ttu-id="8940b-324">msdyn_skipupdateestimateline</span><span class="sxs-lookup"><span data-stu-id="8940b-324">msdyn_skipupdateestimateline</span></span>           | <span data-ttu-id="8940b-325">否</span><span class="sxs-lookup"><span data-stu-id="8940b-325">no</span></span>             | <span data-ttu-id="8940b-326">否</span><span class="sxs-lookup"><span data-stu-id="8940b-326">no</span></span>               |
| <span data-ttu-id="8940b-327">msdyn_skipupdateestimatelinename</span><span class="sxs-lookup"><span data-stu-id="8940b-327">msdyn_skipupdateestimatelinename</span></span>       | <span data-ttu-id="8940b-328">否</span><span class="sxs-lookup"><span data-stu-id="8940b-328">no</span></span>             | <span data-ttu-id="8940b-329">否</span><span class="sxs-lookup"><span data-stu-id="8940b-329">no</span></span>               |
| <span data-ttu-id="8940b-330">msdyn_summary</span><span class="sxs-lookup"><span data-stu-id="8940b-330">msdyn_summary</span></span>                          | <span data-ttu-id="8940b-331">否</span><span class="sxs-lookup"><span data-stu-id="8940b-331">no</span></span>             | <span data-ttu-id="8940b-332">否</span><span class="sxs-lookup"><span data-stu-id="8940b-332">no</span></span>               |
| <span data-ttu-id="8940b-333">msdyn_varianceofcost</span><span class="sxs-lookup"><span data-stu-id="8940b-333">msdyn_varianceofcost</span></span>                   | <span data-ttu-id="8940b-334">否</span><span class="sxs-lookup"><span data-stu-id="8940b-334">no</span></span>             | <span data-ttu-id="8940b-335">否</span><span class="sxs-lookup"><span data-stu-id="8940b-335">no</span></span>               |
| <span data-ttu-id="8940b-336">msdyn_varianceofcost_base</span><span class="sxs-lookup"><span data-stu-id="8940b-336">msdyn_varianceofcost_base</span></span>              | <span data-ttu-id="8940b-337">否</span><span class="sxs-lookup"><span data-stu-id="8940b-337">no</span></span>             | <span data-ttu-id="8940b-338">否</span><span class="sxs-lookup"><span data-stu-id="8940b-338">no</span></span>               |

### <a name="project-task-dependency"></a><span data-ttu-id="8940b-339">项目任务依赖关系</span><span class="sxs-lookup"><span data-stu-id="8940b-339">Project task dependency</span></span>

| <span data-ttu-id="8940b-340">**逻辑名称**</span><span class="sxs-lookup"><span data-stu-id="8940b-340">**Logical name**</span></span>              | <span data-ttu-id="8940b-341">**可创建**</span><span class="sxs-lookup"><span data-stu-id="8940b-341">**Can create**</span></span> | <span data-ttu-id="8940b-342">**可编辑**</span><span class="sxs-lookup"><span data-stu-id="8940b-342">**Can edit**</span></span> |
|-------------------------------|----------------|--------------|
| <span data-ttu-id="8940b-343">msdyn_linktype</span><span class="sxs-lookup"><span data-stu-id="8940b-343">msdyn_linktype</span></span>                | <span data-ttu-id="8940b-344">否</span><span class="sxs-lookup"><span data-stu-id="8940b-344">no</span></span>             | <span data-ttu-id="8940b-345">否</span><span class="sxs-lookup"><span data-stu-id="8940b-345">no</span></span>           |
| <span data-ttu-id="8940b-346">msdyn_linktypename</span><span class="sxs-lookup"><span data-stu-id="8940b-346">msdyn_linktypename</span></span>            | <span data-ttu-id="8940b-347">否</span><span class="sxs-lookup"><span data-stu-id="8940b-347">no</span></span>             | <span data-ttu-id="8940b-348">否</span><span class="sxs-lookup"><span data-stu-id="8940b-348">no</span></span>           |
| <span data-ttu-id="8940b-349">msdyn_predecessortask</span><span class="sxs-lookup"><span data-stu-id="8940b-349">msdyn_predecessortask</span></span>         | <span data-ttu-id="8940b-350">是</span><span class="sxs-lookup"><span data-stu-id="8940b-350">yes</span></span>            | <span data-ttu-id="8940b-351">否</span><span class="sxs-lookup"><span data-stu-id="8940b-351">no</span></span>           |
| <span data-ttu-id="8940b-352">msdyn_predecessortaskname</span><span class="sxs-lookup"><span data-stu-id="8940b-352">msdyn_predecessortaskname</span></span>     | <span data-ttu-id="8940b-353">是</span><span class="sxs-lookup"><span data-stu-id="8940b-353">yes</span></span>            | <span data-ttu-id="8940b-354">否</span><span class="sxs-lookup"><span data-stu-id="8940b-354">no</span></span>           |
| <span data-ttu-id="8940b-355">msdyn_project</span><span class="sxs-lookup"><span data-stu-id="8940b-355">msdyn_project</span></span>                 | <span data-ttu-id="8940b-356">是</span><span class="sxs-lookup"><span data-stu-id="8940b-356">yes</span></span>            | <span data-ttu-id="8940b-357">否</span><span class="sxs-lookup"><span data-stu-id="8940b-357">no</span></span>           |
| <span data-ttu-id="8940b-358">msdyn_projectname</span><span class="sxs-lookup"><span data-stu-id="8940b-358">msdyn_projectname</span></span>             | <span data-ttu-id="8940b-359">是</span><span class="sxs-lookup"><span data-stu-id="8940b-359">yes</span></span>            | <span data-ttu-id="8940b-360">否</span><span class="sxs-lookup"><span data-stu-id="8940b-360">no</span></span>           |
| <span data-ttu-id="8940b-361">msdyn_projecttaskdependencyid</span><span class="sxs-lookup"><span data-stu-id="8940b-361">msdyn_projecttaskdependencyid</span></span> | <span data-ttu-id="8940b-362">是</span><span class="sxs-lookup"><span data-stu-id="8940b-362">yes</span></span>            | <span data-ttu-id="8940b-363">否</span><span class="sxs-lookup"><span data-stu-id="8940b-363">no</span></span>           |
| <span data-ttu-id="8940b-364">msdyn_successortask</span><span class="sxs-lookup"><span data-stu-id="8940b-364">msdyn_successortask</span></span>           | <span data-ttu-id="8940b-365">是</span><span class="sxs-lookup"><span data-stu-id="8940b-365">yes</span></span>            | <span data-ttu-id="8940b-366">否</span><span class="sxs-lookup"><span data-stu-id="8940b-366">no</span></span>           |
| <span data-ttu-id="8940b-367">msdyn_successortaskname</span><span class="sxs-lookup"><span data-stu-id="8940b-367">msdyn_successortaskname</span></span>       | <span data-ttu-id="8940b-368">是</span><span class="sxs-lookup"><span data-stu-id="8940b-368">yes</span></span>            | <span data-ttu-id="8940b-369">否</span><span class="sxs-lookup"><span data-stu-id="8940b-369">no</span></span>           |

### <a name="resource-assignment"></a><span data-ttu-id="8940b-370">资源分派</span><span class="sxs-lookup"><span data-stu-id="8940b-370">Resource assignment</span></span>

| <span data-ttu-id="8940b-371">**逻辑名称**</span><span class="sxs-lookup"><span data-stu-id="8940b-371">**Logical name**</span></span>             | <span data-ttu-id="8940b-372">**可创建**</span><span class="sxs-lookup"><span data-stu-id="8940b-372">**Can create**</span></span> | <span data-ttu-id="8940b-373">**可编辑**</span><span class="sxs-lookup"><span data-stu-id="8940b-373">**Can edit**</span></span> |
|------------------------------|----------------|--------------|
| <span data-ttu-id="8940b-374">msdyn_bookableresourceid</span><span class="sxs-lookup"><span data-stu-id="8940b-374">msdyn_bookableresourceid</span></span>     | <span data-ttu-id="8940b-375">是</span><span class="sxs-lookup"><span data-stu-id="8940b-375">yes</span></span>            | <span data-ttu-id="8940b-376">否</span><span class="sxs-lookup"><span data-stu-id="8940b-376">no</span></span>           |
| <span data-ttu-id="8940b-377">msdyn_bookableresourceidname</span><span class="sxs-lookup"><span data-stu-id="8940b-377">msdyn_bookableresourceidname</span></span> | <span data-ttu-id="8940b-378">是</span><span class="sxs-lookup"><span data-stu-id="8940b-378">yes</span></span>            | <span data-ttu-id="8940b-379">否</span><span class="sxs-lookup"><span data-stu-id="8940b-379">no</span></span>           |
| <span data-ttu-id="8940b-380">msdyn_bookingstatusid</span><span class="sxs-lookup"><span data-stu-id="8940b-380">msdyn_bookingstatusid</span></span>        | <span data-ttu-id="8940b-381">否</span><span class="sxs-lookup"><span data-stu-id="8940b-381">no</span></span>             | <span data-ttu-id="8940b-382">否</span><span class="sxs-lookup"><span data-stu-id="8940b-382">no</span></span>           |
| <span data-ttu-id="8940b-383">msdyn_bookingstatusidname</span><span class="sxs-lookup"><span data-stu-id="8940b-383">msdyn_bookingstatusidname</span></span>    | <span data-ttu-id="8940b-384">否</span><span class="sxs-lookup"><span data-stu-id="8940b-384">no</span></span>             | <span data-ttu-id="8940b-385">否</span><span class="sxs-lookup"><span data-stu-id="8940b-385">no</span></span>           |
| <span data-ttu-id="8940b-386">msdyn_committype</span><span class="sxs-lookup"><span data-stu-id="8940b-386">msdyn_committype</span></span>             | <span data-ttu-id="8940b-387">否</span><span class="sxs-lookup"><span data-stu-id="8940b-387">no</span></span>             | <span data-ttu-id="8940b-388">否</span><span class="sxs-lookup"><span data-stu-id="8940b-388">no</span></span>           |
| <span data-ttu-id="8940b-389">msdyn_committypename</span><span class="sxs-lookup"><span data-stu-id="8940b-389">msdyn_committypename</span></span>         | <span data-ttu-id="8940b-390">否</span><span class="sxs-lookup"><span data-stu-id="8940b-390">no</span></span>             | <span data-ttu-id="8940b-391">否</span><span class="sxs-lookup"><span data-stu-id="8940b-391">no</span></span>           |
| <span data-ttu-id="8940b-392">msdyn_effort</span><span class="sxs-lookup"><span data-stu-id="8940b-392">msdyn_effort</span></span>                 | <span data-ttu-id="8940b-393">否</span><span class="sxs-lookup"><span data-stu-id="8940b-393">no</span></span>             | <span data-ttu-id="8940b-394">否</span><span class="sxs-lookup"><span data-stu-id="8940b-394">no</span></span>           |
| <span data-ttu-id="8940b-395">msdyn_effortcompleted</span><span class="sxs-lookup"><span data-stu-id="8940b-395">msdyn_effortcompleted</span></span>        | <span data-ttu-id="8940b-396">否</span><span class="sxs-lookup"><span data-stu-id="8940b-396">no</span></span>             | <span data-ttu-id="8940b-397">否</span><span class="sxs-lookup"><span data-stu-id="8940b-397">no</span></span>           |
| <span data-ttu-id="8940b-398">msdyn_effortremaining</span><span class="sxs-lookup"><span data-stu-id="8940b-398">msdyn_effortremaining</span></span>        | <span data-ttu-id="8940b-399">否</span><span class="sxs-lookup"><span data-stu-id="8940b-399">no</span></span>             | <span data-ttu-id="8940b-400">否</span><span class="sxs-lookup"><span data-stu-id="8940b-400">no</span></span>           |
| <span data-ttu-id="8940b-401">msdyn_finish</span><span class="sxs-lookup"><span data-stu-id="8940b-401">msdyn_finish</span></span>                 | <span data-ttu-id="8940b-402">否</span><span class="sxs-lookup"><span data-stu-id="8940b-402">no</span></span>             | <span data-ttu-id="8940b-403">否</span><span class="sxs-lookup"><span data-stu-id="8940b-403">no</span></span>           |
| <span data-ttu-id="8940b-404">msdyn_plannedcost</span><span class="sxs-lookup"><span data-stu-id="8940b-404">msdyn_plannedcost</span></span>            | <span data-ttu-id="8940b-405">否</span><span class="sxs-lookup"><span data-stu-id="8940b-405">no</span></span>             | <span data-ttu-id="8940b-406">否</span><span class="sxs-lookup"><span data-stu-id="8940b-406">no</span></span>           |
| <span data-ttu-id="8940b-407">msdyn_plannedcost_base</span><span class="sxs-lookup"><span data-stu-id="8940b-407">msdyn_plannedcost_base</span></span>       | <span data-ttu-id="8940b-408">否</span><span class="sxs-lookup"><span data-stu-id="8940b-408">no</span></span>             | <span data-ttu-id="8940b-409">否</span><span class="sxs-lookup"><span data-stu-id="8940b-409">no</span></span>           |
| <span data-ttu-id="8940b-410">msdyn_plannedcostcontour</span><span class="sxs-lookup"><span data-stu-id="8940b-410">msdyn_plannedcostcontour</span></span>     | <span data-ttu-id="8940b-411">否</span><span class="sxs-lookup"><span data-stu-id="8940b-411">no</span></span>             | <span data-ttu-id="8940b-412">否</span><span class="sxs-lookup"><span data-stu-id="8940b-412">no</span></span>           |
| <span data-ttu-id="8940b-413">msdyn_plannedsales</span><span class="sxs-lookup"><span data-stu-id="8940b-413">msdyn_plannedsales</span></span>           | <span data-ttu-id="8940b-414">否</span><span class="sxs-lookup"><span data-stu-id="8940b-414">no</span></span>             | <span data-ttu-id="8940b-415">否</span><span class="sxs-lookup"><span data-stu-id="8940b-415">no</span></span>           |
| <span data-ttu-id="8940b-416">msdyn_plannedsales_base</span><span class="sxs-lookup"><span data-stu-id="8940b-416">msdyn_plannedsales_base</span></span>      | <span data-ttu-id="8940b-417">否</span><span class="sxs-lookup"><span data-stu-id="8940b-417">no</span></span>             | <span data-ttu-id="8940b-418">否</span><span class="sxs-lookup"><span data-stu-id="8940b-418">no</span></span>           |
| <span data-ttu-id="8940b-419">msdyn_plannedsalescontour</span><span class="sxs-lookup"><span data-stu-id="8940b-419">msdyn_plannedsalescontour</span></span>    | <span data-ttu-id="8940b-420">否</span><span class="sxs-lookup"><span data-stu-id="8940b-420">no</span></span>             | <span data-ttu-id="8940b-421">否</span><span class="sxs-lookup"><span data-stu-id="8940b-421">no</span></span>           |
| <span data-ttu-id="8940b-422">msdyn_plannedwork</span><span class="sxs-lookup"><span data-stu-id="8940b-422">msdyn_plannedwork</span></span>            | <span data-ttu-id="8940b-423">否</span><span class="sxs-lookup"><span data-stu-id="8940b-423">no</span></span>             | <span data-ttu-id="8940b-424">否</span><span class="sxs-lookup"><span data-stu-id="8940b-424">no</span></span>           |
| <span data-ttu-id="8940b-425">msdyn_projectid</span><span class="sxs-lookup"><span data-stu-id="8940b-425">msdyn_projectid</span></span>              | <span data-ttu-id="8940b-426">是</span><span class="sxs-lookup"><span data-stu-id="8940b-426">yes</span></span>            | <span data-ttu-id="8940b-427">否</span><span class="sxs-lookup"><span data-stu-id="8940b-427">no</span></span>           |
| <span data-ttu-id="8940b-428">msdyn_projectidname</span><span class="sxs-lookup"><span data-stu-id="8940b-428">msdyn_projectidname</span></span>          | <span data-ttu-id="8940b-429">否</span><span class="sxs-lookup"><span data-stu-id="8940b-429">no</span></span>             | <span data-ttu-id="8940b-430">否</span><span class="sxs-lookup"><span data-stu-id="8940b-430">no</span></span>           |
| <span data-ttu-id="8940b-431">msdyn_projectteamid</span><span class="sxs-lookup"><span data-stu-id="8940b-431">msdyn_projectteamid</span></span>          | <span data-ttu-id="8940b-432">否</span><span class="sxs-lookup"><span data-stu-id="8940b-432">no</span></span>             | <span data-ttu-id="8940b-433">否</span><span class="sxs-lookup"><span data-stu-id="8940b-433">no</span></span>           |
| <span data-ttu-id="8940b-434">msdyn_projectteamidname</span><span class="sxs-lookup"><span data-stu-id="8940b-434">msdyn_projectteamidname</span></span>      | <span data-ttu-id="8940b-435">否</span><span class="sxs-lookup"><span data-stu-id="8940b-435">no</span></span>             | <span data-ttu-id="8940b-436">否</span><span class="sxs-lookup"><span data-stu-id="8940b-436">no</span></span>           |
| <span data-ttu-id="8940b-437">msdyn_start</span><span class="sxs-lookup"><span data-stu-id="8940b-437">msdyn_start</span></span>                  | <span data-ttu-id="8940b-438">否</span><span class="sxs-lookup"><span data-stu-id="8940b-438">no</span></span>             | <span data-ttu-id="8940b-439">否</span><span class="sxs-lookup"><span data-stu-id="8940b-439">no</span></span>           |
| <span data-ttu-id="8940b-440">msdyn_taskid</span><span class="sxs-lookup"><span data-stu-id="8940b-440">msdyn_taskid</span></span>                 | <span data-ttu-id="8940b-441">否</span><span class="sxs-lookup"><span data-stu-id="8940b-441">no</span></span>             | <span data-ttu-id="8940b-442">否</span><span class="sxs-lookup"><span data-stu-id="8940b-442">no</span></span>           |
| <span data-ttu-id="8940b-443">msdyn_taskidname</span><span class="sxs-lookup"><span data-stu-id="8940b-443">msdyn_taskidname</span></span>             | <span data-ttu-id="8940b-444">否</span><span class="sxs-lookup"><span data-stu-id="8940b-444">no</span></span>             | <span data-ttu-id="8940b-445">否</span><span class="sxs-lookup"><span data-stu-id="8940b-445">no</span></span>           |
| <span data-ttu-id="8940b-446">msdyn_userresourceid</span><span class="sxs-lookup"><span data-stu-id="8940b-446">msdyn_userresourceid</span></span>         | <span data-ttu-id="8940b-447">否</span><span class="sxs-lookup"><span data-stu-id="8940b-447">no</span></span>             | <span data-ttu-id="8940b-448">否</span><span class="sxs-lookup"><span data-stu-id="8940b-448">no</span></span>           |

### <a name="project-team-member"></a><span data-ttu-id="8940b-449">项目团队成员</span><span class="sxs-lookup"><span data-stu-id="8940b-449">Project team member</span></span>

| <span data-ttu-id="8940b-450">**逻辑名称**</span><span class="sxs-lookup"><span data-stu-id="8940b-450">**Logical name**</span></span>                                 | <span data-ttu-id="8940b-451">**可创建**</span><span class="sxs-lookup"><span data-stu-id="8940b-451">**Can create**</span></span> | <span data-ttu-id="8940b-452">**可编辑**</span><span class="sxs-lookup"><span data-stu-id="8940b-452">**Can edit**</span></span> |
|--------------------------------------------------|----------------|--------------|
| <span data-ttu-id="8940b-453">msdyn_calendarid</span><span class="sxs-lookup"><span data-stu-id="8940b-453">msdyn_calendarid</span></span>                                 | <span data-ttu-id="8940b-454">否</span><span class="sxs-lookup"><span data-stu-id="8940b-454">no</span></span>             | <span data-ttu-id="8940b-455">否</span><span class="sxs-lookup"><span data-stu-id="8940b-455">no</span></span>           |
| <span data-ttu-id="8940b-456">msdyn_creategenericteammemberwithrequirementname</span><span class="sxs-lookup"><span data-stu-id="8940b-456">msdyn_creategenericteammemberwithrequirementname</span></span> | <span data-ttu-id="8940b-457">否</span><span class="sxs-lookup"><span data-stu-id="8940b-457">no</span></span>             | <span data-ttu-id="8940b-458">否</span><span class="sxs-lookup"><span data-stu-id="8940b-458">no</span></span>           |
| <span data-ttu-id="8940b-459">msdyn_deletestatus</span><span class="sxs-lookup"><span data-stu-id="8940b-459">msdyn_deletestatus</span></span>                               | <span data-ttu-id="8940b-460">否</span><span class="sxs-lookup"><span data-stu-id="8940b-460">no</span></span>             | <span data-ttu-id="8940b-461">否</span><span class="sxs-lookup"><span data-stu-id="8940b-461">no</span></span>           |
| <span data-ttu-id="8940b-462">msdyn_deletestatusname</span><span class="sxs-lookup"><span data-stu-id="8940b-462">msdyn_deletestatusname</span></span>                           | <span data-ttu-id="8940b-463">否</span><span class="sxs-lookup"><span data-stu-id="8940b-463">no</span></span>             | <span data-ttu-id="8940b-464">否</span><span class="sxs-lookup"><span data-stu-id="8940b-464">no</span></span>           |
| <span data-ttu-id="8940b-465">msdyn_effort</span><span class="sxs-lookup"><span data-stu-id="8940b-465">msdyn_effort</span></span>                                     | <span data-ttu-id="8940b-466">否</span><span class="sxs-lookup"><span data-stu-id="8940b-466">no</span></span>             | <span data-ttu-id="8940b-467">否</span><span class="sxs-lookup"><span data-stu-id="8940b-467">no</span></span>           |
| <span data-ttu-id="8940b-468">msdyn_effortcompleted</span><span class="sxs-lookup"><span data-stu-id="8940b-468">msdyn_effortcompleted</span></span>                            | <span data-ttu-id="8940b-469">否</span><span class="sxs-lookup"><span data-stu-id="8940b-469">no</span></span>             | <span data-ttu-id="8940b-470">否</span><span class="sxs-lookup"><span data-stu-id="8940b-470">no</span></span>           |
| <span data-ttu-id="8940b-471">msdyn_effortremaining</span><span class="sxs-lookup"><span data-stu-id="8940b-471">msdyn_effortremaining</span></span>                            | <span data-ttu-id="8940b-472">否</span><span class="sxs-lookup"><span data-stu-id="8940b-472">no</span></span>             | <span data-ttu-id="8940b-473">否</span><span class="sxs-lookup"><span data-stu-id="8940b-473">no</span></span>           |
| <span data-ttu-id="8940b-474">msdyn_finish</span><span class="sxs-lookup"><span data-stu-id="8940b-474">msdyn_finish</span></span>                                     | <span data-ttu-id="8940b-475">否</span><span class="sxs-lookup"><span data-stu-id="8940b-475">no</span></span>             | <span data-ttu-id="8940b-476">否</span><span class="sxs-lookup"><span data-stu-id="8940b-476">no</span></span>           |
| <span data-ttu-id="8940b-477">msdyn_hardbookedhours</span><span class="sxs-lookup"><span data-stu-id="8940b-477">msdyn_hardbookedhours</span></span>                            | <span data-ttu-id="8940b-478">否</span><span class="sxs-lookup"><span data-stu-id="8940b-478">no</span></span>             | <span data-ttu-id="8940b-479">否</span><span class="sxs-lookup"><span data-stu-id="8940b-479">no</span></span>           |
| <span data-ttu-id="8940b-480">msdyn_hours</span><span class="sxs-lookup"><span data-stu-id="8940b-480">msdyn_hours</span></span>                                      | <span data-ttu-id="8940b-481">否</span><span class="sxs-lookup"><span data-stu-id="8940b-481">no</span></span>             | <span data-ttu-id="8940b-482">否</span><span class="sxs-lookup"><span data-stu-id="8940b-482">no</span></span>           |
| <span data-ttu-id="8940b-483">msdyn_markedfordeletiontimer</span><span class="sxs-lookup"><span data-stu-id="8940b-483">msdyn_markedfordeletiontimer</span></span>                     | <span data-ttu-id="8940b-484">否</span><span class="sxs-lookup"><span data-stu-id="8940b-484">no</span></span>             | <span data-ttu-id="8940b-485">否</span><span class="sxs-lookup"><span data-stu-id="8940b-485">no</span></span>           |
| <span data-ttu-id="8940b-486">msdyn_markedfordeletiontimestamp</span><span class="sxs-lookup"><span data-stu-id="8940b-486">msdyn_markedfordeletiontimestamp</span></span>                 | <span data-ttu-id="8940b-487">否</span><span class="sxs-lookup"><span data-stu-id="8940b-487">no</span></span>             | <span data-ttu-id="8940b-488">否</span><span class="sxs-lookup"><span data-stu-id="8940b-488">no</span></span>           |
| <span data-ttu-id="8940b-489">msdyn_msprojectclientid</span><span class="sxs-lookup"><span data-stu-id="8940b-489">msdyn_msprojectclientid</span></span>                          | <span data-ttu-id="8940b-490">否</span><span class="sxs-lookup"><span data-stu-id="8940b-490">no</span></span>             | <span data-ttu-id="8940b-491">否</span><span class="sxs-lookup"><span data-stu-id="8940b-491">no</span></span>           |
| <span data-ttu-id="8940b-492">msdyn_percentage</span><span class="sxs-lookup"><span data-stu-id="8940b-492">msdyn_percentage</span></span>                                 | <span data-ttu-id="8940b-493">否</span><span class="sxs-lookup"><span data-stu-id="8940b-493">no</span></span>             | <span data-ttu-id="8940b-494">否</span><span class="sxs-lookup"><span data-stu-id="8940b-494">no</span></span>           |
| <span data-ttu-id="8940b-495">msdyn_requiredhours</span><span class="sxs-lookup"><span data-stu-id="8940b-495">msdyn_requiredhours</span></span>                              | <span data-ttu-id="8940b-496">否</span><span class="sxs-lookup"><span data-stu-id="8940b-496">no</span></span>             | <span data-ttu-id="8940b-497">否</span><span class="sxs-lookup"><span data-stu-id="8940b-497">no</span></span>           |
| <span data-ttu-id="8940b-498">msdyn_softbookedhours</span><span class="sxs-lookup"><span data-stu-id="8940b-498">msdyn_softbookedhours</span></span>                            | <span data-ttu-id="8940b-499">否</span><span class="sxs-lookup"><span data-stu-id="8940b-499">no</span></span>             | <span data-ttu-id="8940b-500">否</span><span class="sxs-lookup"><span data-stu-id="8940b-500">no</span></span>           |
| <span data-ttu-id="8940b-501">msdyn_start</span><span class="sxs-lookup"><span data-stu-id="8940b-501">msdyn_start</span></span>                                      | <span data-ttu-id="8940b-502">否</span><span class="sxs-lookup"><span data-stu-id="8940b-502">no</span></span>             | <span data-ttu-id="8940b-503">否</span><span class="sxs-lookup"><span data-stu-id="8940b-503">no</span></span>           |

### <a name="project"></a><span data-ttu-id="8940b-504">Project</span><span class="sxs-lookup"><span data-stu-id="8940b-504">Project</span></span>

| <span data-ttu-id="8940b-505">**逻辑名称**</span><span class="sxs-lookup"><span data-stu-id="8940b-505">**Logical name**</span></span>                       | <span data-ttu-id="8940b-506">**可创建**</span><span class="sxs-lookup"><span data-stu-id="8940b-506">**Can create**</span></span> | <span data-ttu-id="8940b-507">**可编辑**</span><span class="sxs-lookup"><span data-stu-id="8940b-507">**Can edit**</span></span> |
|----------------------------------------|----------------|--------------|
| <span data-ttu-id="8940b-508">msdyn_actualexpensecost</span><span class="sxs-lookup"><span data-stu-id="8940b-508">msdyn_actualexpensecost</span></span>                | <span data-ttu-id="8940b-509">否</span><span class="sxs-lookup"><span data-stu-id="8940b-509">no</span></span>             | <span data-ttu-id="8940b-510">否</span><span class="sxs-lookup"><span data-stu-id="8940b-510">no</span></span>           |
| <span data-ttu-id="8940b-511">msdyn_actualexpensecost_base</span><span class="sxs-lookup"><span data-stu-id="8940b-511">msdyn_actualexpensecost_base</span></span>           | <span data-ttu-id="8940b-512">否</span><span class="sxs-lookup"><span data-stu-id="8940b-512">no</span></span>             | <span data-ttu-id="8940b-513">否</span><span class="sxs-lookup"><span data-stu-id="8940b-513">no</span></span>           |
| <span data-ttu-id="8940b-514">msdyn_actuallaborcost</span><span class="sxs-lookup"><span data-stu-id="8940b-514">msdyn_actuallaborcost</span></span>                  | <span data-ttu-id="8940b-515">否</span><span class="sxs-lookup"><span data-stu-id="8940b-515">no</span></span>             | <span data-ttu-id="8940b-516">否</span><span class="sxs-lookup"><span data-stu-id="8940b-516">no</span></span>           |
| <span data-ttu-id="8940b-517">msdyn_actuallaborcost_base</span><span class="sxs-lookup"><span data-stu-id="8940b-517">msdyn_actuallaborcost_base</span></span>             | <span data-ttu-id="8940b-518">否</span><span class="sxs-lookup"><span data-stu-id="8940b-518">no</span></span>             | <span data-ttu-id="8940b-519">否</span><span class="sxs-lookup"><span data-stu-id="8940b-519">no</span></span>           |
| <span data-ttu-id="8940b-520">msdyn_actualsales</span><span class="sxs-lookup"><span data-stu-id="8940b-520">msdyn_actualsales</span></span>                      | <span data-ttu-id="8940b-521">否</span><span class="sxs-lookup"><span data-stu-id="8940b-521">no</span></span>             | <span data-ttu-id="8940b-522">否</span><span class="sxs-lookup"><span data-stu-id="8940b-522">no</span></span>           |
| <span data-ttu-id="8940b-523">msdyn_actualsales_base</span><span class="sxs-lookup"><span data-stu-id="8940b-523">msdyn_actualsales_base</span></span>                 | <span data-ttu-id="8940b-524">否</span><span class="sxs-lookup"><span data-stu-id="8940b-524">no</span></span>             | <span data-ttu-id="8940b-525">否</span><span class="sxs-lookup"><span data-stu-id="8940b-525">no</span></span>           |
| <span data-ttu-id="8940b-526">msdyn_contractlineproject</span><span class="sxs-lookup"><span data-stu-id="8940b-526">msdyn_contractlineproject</span></span>              | <span data-ttu-id="8940b-527">是</span><span class="sxs-lookup"><span data-stu-id="8940b-527">yes</span></span>            | <span data-ttu-id="8940b-528">否</span><span class="sxs-lookup"><span data-stu-id="8940b-528">no</span></span>           |
| <span data-ttu-id="8940b-529">msdyn_contractorganizationalunitid</span><span class="sxs-lookup"><span data-stu-id="8940b-529">msdyn_contractorganizationalunitid</span></span>     | <span data-ttu-id="8940b-530">是</span><span class="sxs-lookup"><span data-stu-id="8940b-530">yes</span></span>            | <span data-ttu-id="8940b-531">否</span><span class="sxs-lookup"><span data-stu-id="8940b-531">no</span></span>           |
| <span data-ttu-id="8940b-532">msdyn_contractorganizationalunitidname</span><span class="sxs-lookup"><span data-stu-id="8940b-532">msdyn_contractorganizationalunitidname</span></span> | <span data-ttu-id="8940b-533">是</span><span class="sxs-lookup"><span data-stu-id="8940b-533">yes</span></span>            | <span data-ttu-id="8940b-534">否</span><span class="sxs-lookup"><span data-stu-id="8940b-534">no</span></span>           |
| <span data-ttu-id="8940b-535">msdyn_costconsumption</span><span class="sxs-lookup"><span data-stu-id="8940b-535">msdyn_costconsumption</span></span>                  | <span data-ttu-id="8940b-536">否</span><span class="sxs-lookup"><span data-stu-id="8940b-536">no</span></span>             | <span data-ttu-id="8940b-537">否</span><span class="sxs-lookup"><span data-stu-id="8940b-537">no</span></span>           |
| <span data-ttu-id="8940b-538">msdyn_costestimateatcomplete</span><span class="sxs-lookup"><span data-stu-id="8940b-538">msdyn_costestimateatcomplete</span></span>           | <span data-ttu-id="8940b-539">否</span><span class="sxs-lookup"><span data-stu-id="8940b-539">no</span></span>             | <span data-ttu-id="8940b-540">否</span><span class="sxs-lookup"><span data-stu-id="8940b-540">no</span></span>           |
| <span data-ttu-id="8940b-541">msdyn_costestimateatcomplete_base</span><span class="sxs-lookup"><span data-stu-id="8940b-541">msdyn_costestimateatcomplete_base</span></span>      | <span data-ttu-id="8940b-542">否</span><span class="sxs-lookup"><span data-stu-id="8940b-542">no</span></span>             | <span data-ttu-id="8940b-543">否</span><span class="sxs-lookup"><span data-stu-id="8940b-543">no</span></span>           |
| <span data-ttu-id="8940b-544">msdyn_costvariance</span><span class="sxs-lookup"><span data-stu-id="8940b-544">msdyn_costvariance</span></span>                     | <span data-ttu-id="8940b-545">否</span><span class="sxs-lookup"><span data-stu-id="8940b-545">no</span></span>             | <span data-ttu-id="8940b-546">否</span><span class="sxs-lookup"><span data-stu-id="8940b-546">no</span></span>           |
| <span data-ttu-id="8940b-547">msdyn_costvariance_base</span><span class="sxs-lookup"><span data-stu-id="8940b-547">msdyn_costvariance_base</span></span>                | <span data-ttu-id="8940b-548">否</span><span class="sxs-lookup"><span data-stu-id="8940b-548">no</span></span>             | <span data-ttu-id="8940b-549">否</span><span class="sxs-lookup"><span data-stu-id="8940b-549">no</span></span>           |
| <span data-ttu-id="8940b-550">msdyn_duration</span><span class="sxs-lookup"><span data-stu-id="8940b-550">msdyn_duration</span></span>                         | <span data-ttu-id="8940b-551">否</span><span class="sxs-lookup"><span data-stu-id="8940b-551">no</span></span>             | <span data-ttu-id="8940b-552">否</span><span class="sxs-lookup"><span data-stu-id="8940b-552">no</span></span>           |
| <span data-ttu-id="8940b-553">msdyn_effort</span><span class="sxs-lookup"><span data-stu-id="8940b-553">msdyn_effort</span></span>                           | <span data-ttu-id="8940b-554">否</span><span class="sxs-lookup"><span data-stu-id="8940b-554">no</span></span>             | <span data-ttu-id="8940b-555">否</span><span class="sxs-lookup"><span data-stu-id="8940b-555">no</span></span>           |
| <span data-ttu-id="8940b-556">msdyn_effortcompleted</span><span class="sxs-lookup"><span data-stu-id="8940b-556">msdyn_effortcompleted</span></span>                  | <span data-ttu-id="8940b-557">否</span><span class="sxs-lookup"><span data-stu-id="8940b-557">no</span></span>             | <span data-ttu-id="8940b-558">否</span><span class="sxs-lookup"><span data-stu-id="8940b-558">no</span></span>           |
| <span data-ttu-id="8940b-559">msdyn_effortestimateatcompleteeac</span><span class="sxs-lookup"><span data-stu-id="8940b-559">msdyn_effortestimateatcompleteeac</span></span>      | <span data-ttu-id="8940b-560">否</span><span class="sxs-lookup"><span data-stu-id="8940b-560">no</span></span>             | <span data-ttu-id="8940b-561">否</span><span class="sxs-lookup"><span data-stu-id="8940b-561">no</span></span>           |
| <span data-ttu-id="8940b-562">msdyn_effortremaining</span><span class="sxs-lookup"><span data-stu-id="8940b-562">msdyn_effortremaining</span></span>                  | <span data-ttu-id="8940b-563">否</span><span class="sxs-lookup"><span data-stu-id="8940b-563">no</span></span>             | <span data-ttu-id="8940b-564">否</span><span class="sxs-lookup"><span data-stu-id="8940b-564">no</span></span>           |
| <span data-ttu-id="8940b-565">msdyn_finish</span><span class="sxs-lookup"><span data-stu-id="8940b-565">msdyn_finish</span></span>                           | <span data-ttu-id="8940b-566">是</span><span class="sxs-lookup"><span data-stu-id="8940b-566">yes</span></span>            | <span data-ttu-id="8940b-567">是</span><span class="sxs-lookup"><span data-stu-id="8940b-567">yes</span></span>          |
| <span data-ttu-id="8940b-568">msdyn_globalrevisiontoken</span><span class="sxs-lookup"><span data-stu-id="8940b-568">msdyn_globalrevisiontoken</span></span>              | <span data-ttu-id="8940b-569">否</span><span class="sxs-lookup"><span data-stu-id="8940b-569">no</span></span>             | <span data-ttu-id="8940b-570">否</span><span class="sxs-lookup"><span data-stu-id="8940b-570">no</span></span>           |
| <span data-ttu-id="8940b-571">msdyn_islinkedtomsprojectclient</span><span class="sxs-lookup"><span data-stu-id="8940b-571">msdyn_islinkedtomsprojectclient</span></span>        | <span data-ttu-id="8940b-572">否</span><span class="sxs-lookup"><span data-stu-id="8940b-572">no</span></span>             | <span data-ttu-id="8940b-573">否</span><span class="sxs-lookup"><span data-stu-id="8940b-573">no</span></span>           |
| <span data-ttu-id="8940b-574">msdyn_islinkedtomsprojectclientname</span><span class="sxs-lookup"><span data-stu-id="8940b-574">msdyn_islinkedtomsprojectclientname</span></span>    | <span data-ttu-id="8940b-575">否</span><span class="sxs-lookup"><span data-stu-id="8940b-575">no</span></span>             | <span data-ttu-id="8940b-576">否</span><span class="sxs-lookup"><span data-stu-id="8940b-576">no</span></span>           |
| <span data-ttu-id="8940b-577">msdyn_linkeddocumenturl</span><span class="sxs-lookup"><span data-stu-id="8940b-577">msdyn_linkeddocumenturl</span></span>                | <span data-ttu-id="8940b-578">否</span><span class="sxs-lookup"><span data-stu-id="8940b-578">no</span></span>             | <span data-ttu-id="8940b-579">否</span><span class="sxs-lookup"><span data-stu-id="8940b-579">no</span></span>           |
| <span data-ttu-id="8940b-580">msdyn_msprojectdocument</span><span class="sxs-lookup"><span data-stu-id="8940b-580">msdyn_msprojectdocument</span></span>                | <span data-ttu-id="8940b-581">否</span><span class="sxs-lookup"><span data-stu-id="8940b-581">no</span></span>             | <span data-ttu-id="8940b-582">否</span><span class="sxs-lookup"><span data-stu-id="8940b-582">no</span></span>           |
| <span data-ttu-id="8940b-583">msdyn_msprojectdocumentname</span><span class="sxs-lookup"><span data-stu-id="8940b-583">msdyn_msprojectdocumentname</span></span>            | <span data-ttu-id="8940b-584">否</span><span class="sxs-lookup"><span data-stu-id="8940b-584">no</span></span>             | <span data-ttu-id="8940b-585">否</span><span class="sxs-lookup"><span data-stu-id="8940b-585">no</span></span>           |
| <span data-ttu-id="8940b-586">msdyn_plannedexpensecost</span><span class="sxs-lookup"><span data-stu-id="8940b-586">msdyn_plannedexpensecost</span></span>               | <span data-ttu-id="8940b-587">否</span><span class="sxs-lookup"><span data-stu-id="8940b-587">no</span></span>             | <span data-ttu-id="8940b-588">否</span><span class="sxs-lookup"><span data-stu-id="8940b-588">no</span></span>           |
| <span data-ttu-id="8940b-589">msdyn_plannedexpensecost_base</span><span class="sxs-lookup"><span data-stu-id="8940b-589">msdyn_plannedexpensecost_base</span></span>          | <span data-ttu-id="8940b-590">否</span><span class="sxs-lookup"><span data-stu-id="8940b-590">no</span></span>             | <span data-ttu-id="8940b-591">否</span><span class="sxs-lookup"><span data-stu-id="8940b-591">no</span></span>           |
| <span data-ttu-id="8940b-592">msdyn_plannedlaborcost</span><span class="sxs-lookup"><span data-stu-id="8940b-592">msdyn_plannedlaborcost</span></span>                 | <span data-ttu-id="8940b-593">否</span><span class="sxs-lookup"><span data-stu-id="8940b-593">no</span></span>             | <span data-ttu-id="8940b-594">否</span><span class="sxs-lookup"><span data-stu-id="8940b-594">no</span></span>           |
| <span data-ttu-id="8940b-595">msdyn_plannedlaborcost_base</span><span class="sxs-lookup"><span data-stu-id="8940b-595">msdyn_plannedlaborcost_base</span></span>            | <span data-ttu-id="8940b-596">否</span><span class="sxs-lookup"><span data-stu-id="8940b-596">no</span></span>             | <span data-ttu-id="8940b-597">否</span><span class="sxs-lookup"><span data-stu-id="8940b-597">no</span></span>           |
| <span data-ttu-id="8940b-598">msdyn_plannedsales</span><span class="sxs-lookup"><span data-stu-id="8940b-598">msdyn_plannedsales</span></span>                     | <span data-ttu-id="8940b-599">否</span><span class="sxs-lookup"><span data-stu-id="8940b-599">no</span></span>             | <span data-ttu-id="8940b-600">否</span><span class="sxs-lookup"><span data-stu-id="8940b-600">no</span></span>           |
| <span data-ttu-id="8940b-601">msdyn_plannedsales_base</span><span class="sxs-lookup"><span data-stu-id="8940b-601">msdyn_plannedsales_base</span></span>                | <span data-ttu-id="8940b-602">否</span><span class="sxs-lookup"><span data-stu-id="8940b-602">no</span></span>             | <span data-ttu-id="8940b-603">否</span><span class="sxs-lookup"><span data-stu-id="8940b-603">no</span></span>           |
| <span data-ttu-id="8940b-604">msdyn_progress</span><span class="sxs-lookup"><span data-stu-id="8940b-604">msdyn_progress</span></span>                         | <span data-ttu-id="8940b-605">否</span><span class="sxs-lookup"><span data-stu-id="8940b-605">no</span></span>             | <span data-ttu-id="8940b-606">否</span><span class="sxs-lookup"><span data-stu-id="8940b-606">no</span></span>           |
| <span data-ttu-id="8940b-607">msdyn_remainingcost</span><span class="sxs-lookup"><span data-stu-id="8940b-607">msdyn_remainingcost</span></span>                    | <span data-ttu-id="8940b-608">否</span><span class="sxs-lookup"><span data-stu-id="8940b-608">no</span></span>             | <span data-ttu-id="8940b-609">否</span><span class="sxs-lookup"><span data-stu-id="8940b-609">no</span></span>           |
| <span data-ttu-id="8940b-610">msdyn_remainingcost_base</span><span class="sxs-lookup"><span data-stu-id="8940b-610">msdyn_remainingcost_base</span></span>               | <span data-ttu-id="8940b-611">否</span><span class="sxs-lookup"><span data-stu-id="8940b-611">no</span></span>             | <span data-ttu-id="8940b-612">否</span><span class="sxs-lookup"><span data-stu-id="8940b-612">no</span></span>           |
| <span data-ttu-id="8940b-613">msdyn_remainingsales</span><span class="sxs-lookup"><span data-stu-id="8940b-613">msdyn_remainingsales</span></span>                   | <span data-ttu-id="8940b-614">否</span><span class="sxs-lookup"><span data-stu-id="8940b-614">no</span></span>             | <span data-ttu-id="8940b-615">否</span><span class="sxs-lookup"><span data-stu-id="8940b-615">no</span></span>           |
| <span data-ttu-id="8940b-616">msdyn_remainingsales_base</span><span class="sxs-lookup"><span data-stu-id="8940b-616">msdyn_remainingsales_base</span></span>              | <span data-ttu-id="8940b-617">否</span><span class="sxs-lookup"><span data-stu-id="8940b-617">no</span></span>             | <span data-ttu-id="8940b-618">否</span><span class="sxs-lookup"><span data-stu-id="8940b-618">no</span></span>           |
| <span data-ttu-id="8940b-619">msdyn_replaylogheader</span><span class="sxs-lookup"><span data-stu-id="8940b-619">msdyn_replaylogheader</span></span>                  | <span data-ttu-id="8940b-620">否</span><span class="sxs-lookup"><span data-stu-id="8940b-620">no</span></span>             | <span data-ttu-id="8940b-621">否</span><span class="sxs-lookup"><span data-stu-id="8940b-621">no</span></span>           |
| <span data-ttu-id="8940b-622">msdyn_salesconsumption</span><span class="sxs-lookup"><span data-stu-id="8940b-622">msdyn_salesconsumption</span></span>                 | <span data-ttu-id="8940b-623">否</span><span class="sxs-lookup"><span data-stu-id="8940b-623">no</span></span>             | <span data-ttu-id="8940b-624">否</span><span class="sxs-lookup"><span data-stu-id="8940b-624">no</span></span>           |
| <span data-ttu-id="8940b-625">msdyn_salesestimateatcompleteeac</span><span class="sxs-lookup"><span data-stu-id="8940b-625">msdyn_salesestimateatcompleteeac</span></span>       | <span data-ttu-id="8940b-626">否</span><span class="sxs-lookup"><span data-stu-id="8940b-626">no</span></span>             | <span data-ttu-id="8940b-627">否</span><span class="sxs-lookup"><span data-stu-id="8940b-627">no</span></span>           |
| <span data-ttu-id="8940b-628">msdyn_salesestimateatcompleteeac_base</span><span class="sxs-lookup"><span data-stu-id="8940b-628">msdyn_salesestimateatcompleteeac_base</span></span>  | <span data-ttu-id="8940b-629">否</span><span class="sxs-lookup"><span data-stu-id="8940b-629">no</span></span>             | <span data-ttu-id="8940b-630">否</span><span class="sxs-lookup"><span data-stu-id="8940b-630">no</span></span>           |
| <span data-ttu-id="8940b-631">msdyn_salesvariance</span><span class="sxs-lookup"><span data-stu-id="8940b-631">msdyn_salesvariance</span></span>                    | <span data-ttu-id="8940b-632">否</span><span class="sxs-lookup"><span data-stu-id="8940b-632">no</span></span>             | <span data-ttu-id="8940b-633">否</span><span class="sxs-lookup"><span data-stu-id="8940b-633">no</span></span>           |
| <span data-ttu-id="8940b-634">msdyn_salesvariance_base</span><span class="sxs-lookup"><span data-stu-id="8940b-634">msdyn_salesvariance_base</span></span>               | <span data-ttu-id="8940b-635">否</span><span class="sxs-lookup"><span data-stu-id="8940b-635">no</span></span>             | <span data-ttu-id="8940b-636">否</span><span class="sxs-lookup"><span data-stu-id="8940b-636">no</span></span>           |
| <span data-ttu-id="8940b-637">msdyn_scheduleperformance</span><span class="sxs-lookup"><span data-stu-id="8940b-637">msdyn_scheduleperformance</span></span>              | <span data-ttu-id="8940b-638">否</span><span class="sxs-lookup"><span data-stu-id="8940b-638">no</span></span>             | <span data-ttu-id="8940b-639">否</span><span class="sxs-lookup"><span data-stu-id="8940b-639">no</span></span>           |
| <span data-ttu-id="8940b-640">msdyn_scheduleperformancename</span><span class="sxs-lookup"><span data-stu-id="8940b-640">msdyn_scheduleperformancename</span></span>          | <span data-ttu-id="8940b-641">否</span><span class="sxs-lookup"><span data-stu-id="8940b-641">no</span></span>             | <span data-ttu-id="8940b-642">否</span><span class="sxs-lookup"><span data-stu-id="8940b-642">no</span></span>           |
| <span data-ttu-id="8940b-643">msdyn_schedulevariance</span><span class="sxs-lookup"><span data-stu-id="8940b-643">msdyn_schedulevariance</span></span>                 | <span data-ttu-id="8940b-644">否</span><span class="sxs-lookup"><span data-stu-id="8940b-644">no</span></span>             | <span data-ttu-id="8940b-645">否</span><span class="sxs-lookup"><span data-stu-id="8940b-645">no</span></span>           |
| <span data-ttu-id="8940b-646">msdyn_taskearlieststart</span><span class="sxs-lookup"><span data-stu-id="8940b-646">msdyn_taskearlieststart</span></span>                | <span data-ttu-id="8940b-647">否</span><span class="sxs-lookup"><span data-stu-id="8940b-647">no</span></span>             | <span data-ttu-id="8940b-648">否</span><span class="sxs-lookup"><span data-stu-id="8940b-648">no</span></span>           |
| <span data-ttu-id="8940b-649">msdyn_teamsize</span><span class="sxs-lookup"><span data-stu-id="8940b-649">msdyn_teamsize</span></span>                         | <span data-ttu-id="8940b-650">否</span><span class="sxs-lookup"><span data-stu-id="8940b-650">no</span></span>             | <span data-ttu-id="8940b-651">否</span><span class="sxs-lookup"><span data-stu-id="8940b-651">no</span></span>           |
| <span data-ttu-id="8940b-652">msdyn_teamsize_date</span><span class="sxs-lookup"><span data-stu-id="8940b-652">msdyn_teamsize_date</span></span>                    | <span data-ttu-id="8940b-653">否</span><span class="sxs-lookup"><span data-stu-id="8940b-653">no</span></span>             | <span data-ttu-id="8940b-654">否</span><span class="sxs-lookup"><span data-stu-id="8940b-654">no</span></span>           |
| <span data-ttu-id="8940b-655">msdyn_teamsize_state</span><span class="sxs-lookup"><span data-stu-id="8940b-655">msdyn_teamsize_state</span></span>                   | <span data-ttu-id="8940b-656">否</span><span class="sxs-lookup"><span data-stu-id="8940b-656">no</span></span>             | <span data-ttu-id="8940b-657">否</span><span class="sxs-lookup"><span data-stu-id="8940b-657">no</span></span>           |
| <span data-ttu-id="8940b-658">msdyn_totalactualcost</span><span class="sxs-lookup"><span data-stu-id="8940b-658">msdyn_totalactualcost</span></span>                  | <span data-ttu-id="8940b-659">否</span><span class="sxs-lookup"><span data-stu-id="8940b-659">no</span></span>             | <span data-ttu-id="8940b-660">否</span><span class="sxs-lookup"><span data-stu-id="8940b-660">no</span></span>           |
| <span data-ttu-id="8940b-661">msdyn_totalactualcost_base</span><span class="sxs-lookup"><span data-stu-id="8940b-661">msdyn_totalactualcost_base</span></span>             | <span data-ttu-id="8940b-662">否</span><span class="sxs-lookup"><span data-stu-id="8940b-662">no</span></span>             | <span data-ttu-id="8940b-663">否</span><span class="sxs-lookup"><span data-stu-id="8940b-663">no</span></span>           |
| <span data-ttu-id="8940b-664">msdyn_totalplannedcost</span><span class="sxs-lookup"><span data-stu-id="8940b-664">msdyn_totalplannedcost</span></span>                 | <span data-ttu-id="8940b-665">否</span><span class="sxs-lookup"><span data-stu-id="8940b-665">no</span></span>             | <span data-ttu-id="8940b-666">否</span><span class="sxs-lookup"><span data-stu-id="8940b-666">no</span></span>           |
| <span data-ttu-id="8940b-667">msdyn_totalplannedcost_base</span><span class="sxs-lookup"><span data-stu-id="8940b-667">msdyn_totalplannedcost_base</span></span>            | <span data-ttu-id="8940b-668">否</span><span class="sxs-lookup"><span data-stu-id="8940b-668">no</span></span>             | <span data-ttu-id="8940b-669">否</span><span class="sxs-lookup"><span data-stu-id="8940b-669">no</span></span>           |


## <a name="limitations-and-known-issues"></a><span data-ttu-id="8940b-670">限制和已知问题</span><span class="sxs-lookup"><span data-stu-id="8940b-670">Limitations and known issues</span></span>
<span data-ttu-id="8940b-671">下面是一系列限制和已知问题：</span><span class="sxs-lookup"><span data-stu-id="8940b-671">The following is a list of limitations and known issues:</span></span>

- <span data-ttu-id="8940b-672">项目计划 API 仅供 **具有 Microsoft Project 许可证的用户** 使用。</span><span class="sxs-lookup"><span data-stu-id="8940b-672">Project Schedule APIs can only be used by **Users with Microsoft Project License.**</span></span> <span data-ttu-id="8940b-673">以下用户不能使用它们：</span><span class="sxs-lookup"><span data-stu-id="8940b-673">They can't be used by:</span></span>
    - <span data-ttu-id="8940b-674">应用程序用户</span><span class="sxs-lookup"><span data-stu-id="8940b-674">Application users</span></span>
    - <span data-ttu-id="8940b-675">系统用户</span><span class="sxs-lookup"><span data-stu-id="8940b-675">System users</span></span>
    - <span data-ttu-id="8940b-676">集成用户</span><span class="sxs-lookup"><span data-stu-id="8940b-676">Integration users</span></span>
    - <span data-ttu-id="8940b-677">没有所需许可证的其他用户</span><span class="sxs-lookup"><span data-stu-id="8940b-677">Other users that don't have the required license</span></span>
- <span data-ttu-id="8940b-678">每个 **OperationSets** 最多只能有 100 项操作。</span><span class="sxs-lookup"><span data-stu-id="8940b-678">Each **OperationSet** can only have a maximum of 100 operations.</span></span>
- <span data-ttu-id="8940b-679">每个用户最多只能有 10 个公开的 **OperationSets**。</span><span class="sxs-lookup"><span data-stu-id="8940b-679">Each user can only have a maximum of 10 open **OperationSets**.</span></span>
- <span data-ttu-id="8940b-680">Project Operations 目前对一个项目最多支持总共 500 个任务。</span><span class="sxs-lookup"><span data-stu-id="8940b-680">Project Operations currently supports a maximum of 500 total tasks on a project.</span></span>
- <span data-ttu-id="8940b-681">**OperationSet** 故障状态和故障日志当前不可用。</span><span class="sxs-lookup"><span data-stu-id="8940b-681">**OperationSet** failure status and failure logs aren't currently available.</span></span>
- [<span data-ttu-id="8940b-682">项目和任务的限制和界限</span><span class="sxs-lookup"><span data-stu-id="8940b-682">Limits and boundaries on projects and tasks</span></span>](/project-for-the-web/project-for-the-web-limits-and-boundaries)

## <a name="error-handling"></a><span data-ttu-id="8940b-683">错误处理</span><span class="sxs-lookup"><span data-stu-id="8940b-683">Error handling</span></span>

   - <span data-ttu-id="8940b-684">要查看操作集生成的错误，转到 **设置** \> **计划集成** \> **操作集**。</span><span class="sxs-lookup"><span data-stu-id="8940b-684">To review errors generated from the Operation Sets, go to **Settings** \> **Schedule Integration** \> **Operations Sets**.</span></span>
   - <span data-ttu-id="8940b-685">若要查看项目计划服务生成的错误，请转到 **设置** \> **计划集成** \> **PSS 错误日志**。</span><span class="sxs-lookup"><span data-stu-id="8940b-685">To review errors generated from the Project schedule Service, go to **Settings** \> **Schedule Integration** \> **PSS Error Logs**.</span></span>

## <a name="sample-scenario"></a><span data-ttu-id="8940b-686">示例方案</span><span class="sxs-lookup"><span data-stu-id="8940b-686">Sample scenario</span></span>

<span data-ttu-id="8940b-687">在此方案中，您将创建一个项目、一个团队成员、四个任务和两个资源分派。</span><span class="sxs-lookup"><span data-stu-id="8940b-687">In this scenario, you will create a project, a team member, four tasks, and two resource assignments.</span></span> <span data-ttu-id="8940b-688">接下来，您将更新一个任务、更新项目、删除一个任务、删除一个资源分派以及创建任务依赖项。</span><span class="sxs-lookup"><span data-stu-id="8940b-688">Next, you will update one task, update the project, delete one task, delete one resource assignment, and create a task dependency.</span></span>

```csharp
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
var task4 = GetTask("4ZZ", projectReference);

var assignment1 = GetResourceAssignment("R1", teamMember, task2, project);
var assignment2 = GetResourceAssignment("R2", teamMember, task3, project);

var task1Response = CallPssCreateAction(task1, operationSetId);
var task2Response = CallPssCreateAction(task2, operationSetId);
var task3Response = CallPssCreateAction(task3, operationSetId);
var task4Response = CallPssCreateAction(task4, operationSetId);

var assignment1Response = CallPssCreateAction(assignment1, operationSetId);
var assignment2Response = CallPssCreateAction(assignment2, operationSetId);

task2["msdyn_subject"] = "Updated Task";
var task2UpdateResponse = CallPssUpdateAction(task2, operationSetId);

project["msdyn_subject"] = $"Proj update {DateTime.Now.ToShortTimeString()}";
var projectUpdateResponse = CallPssUpdateAction(project, operationSetId);

var task4DeleteResponse = CallPssDeleteAction(task4.Id.ToString(), task4.LogicalName, operationSetId);

var assignment2DeleteResponse = CallPssDeleteAction(assignment2.Id.ToString(), assignment2.LogicalName, operationSetId);

var dependency1 = GetTaskDependency(project, task2, task3);
var dependency1Response = CallPssCreateAction(dependency1, operationSetId);

CallExecuteOperationSetAction(operationSetId);
Console.WriteLine("Done....");
```

## <a name="additional-samples"></a><span data-ttu-id="8940b-689">其他示例</span><span class="sxs-lookup"><span data-stu-id="8940b-689">Additional samples</span></span>

```csharp
#region Call actions --- Sample code ----

/// <summary>
/// Calls the action to create an operationSet
/// </summary>
/// <param name="projectId">project id for the operations to be included in this operationSet</param>
/// <param name="description">description of this operationSet</param>
/// <returns>operationSet id</returns>
private string CallCreateOperationSetAction(Guid projectId, string description)
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
/// <param name="entity">Task or Resource Assignment</param>
/// <param name="operationSetId">operationSet id</param>
/// <returns>OperationSetResponse</returns>

private OperationSetResponse CallPssCreateAction(Entity entity, string operationSetId)
{
    OrganizationRequest operationSetRequest = new OrganizationRequest("msdyn_PssCreateV1");
    operationSetRequest["Entity"] = entity;
    operationSetRequest["OperationSetId"] = operationSetId;
    return GetOperationSetResponseFromOrgResponse(organizationService.Execute(operationSetRequest));
}

/// <summary>
/// Calls the action to update an entity, only Task for now
/// </summary>
/// <param name="entity">Task or Resource Assignment</param>
/// <param name="operationSetId">operationSet Id</param>
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
/// </summary>
/// <param name="recordId">Id of the record to be deleted</param>
/// <param name="entityLogicalName">Entity logical name of the record</param>
/// <param name="operationSetId">OperationSet Id</param>
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
/// </summary>
/// <param name="operationSetId">operationSet id</param>
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
/// <param name="operationSetId">operationSet id</param>
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
/// <param name="project">Project</param>
/// <returns>project Id</returns>
private Guid CallCreateProjectAction(Entity project)
{
    OrganizationRequest createProjectRequest = new OrganizationRequest("msdyn_CreateProjectV1");
    createProjectRequest["Project"] = project;
    OrganizationResponse response = organizationService.Execute(createProjectRequest);
    var projectId = Guid.Parse((string)response["ProjectId"]);
    return projectId;
}

/// <summary>
/// Calls the action to create a new project team member
/// </summary>
/// <param name="teamMember">Project team member</param>
/// <returns>project team member Id</returns>
private string CallCreateTeamMemberAction(Entity teamMember)
{
    OrganizationRequest request = new OrganizationRequest("msdyn_CreateTeamMemberV1");
    request["TeamMember"] = teamMember;
    OrganizationResponse response = organizationService.Execute(request);
    return (string)response["TeamMemberId"];
}

private OperationSetResponse GetOperationSetResponseFromOrgResponse(OrganizationResponse orgResponse)
{
    return JsonConvert.DeserializeObject<OperationSetResponse>((string)orgResponse.Results["OperationSetResponse"]);
}

private EntityCollection GetDefaultBucket(EntityReference projectReference)
{
    var columnsToFetch = new ColumnSet("msdyn_project", "msdyn_name");
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
    task["msdyn_effort"] = 4d;
    task["msdyn_scheduledstart"] = DateTime.Today;
    task["msdyn_scheduledend"] = DateTime.Today.AddDays(5);
    task["msdyn_progress"] = 0.34m;
    task["msdyn_start"] = DateTime.Now.AddDays(1);
    task["msdyn_projectbucket"] = GetBucket(projectReference).ToEntityReference();
    task["msdyn_LinkStatus"] = new OptionSetValue(192350000);

    //Custom field handling
    /*
    task["new_custom1"] = "Just my test";
    task["new_age"] = 98;
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
public class OperationSetResponse
{
[DataMember(Name = "operationSetId")]
public Guid OperationSetId { get; set; }

[DataMember(Name = "operationSetDetailId")]
public Guid OperationSetDetailId { get; set; }

[DataMember(Name = "operationType")]
public string OperationType { get; set; }

[DataMember(Name = "recordId")]
public string RecordId { get; set; }

[DataMember(Name = "correlationId")]
public string CorrelationId { get; set; }
}

#endregion
```
