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
# <a name="use-schedule-apis-to-perform-operations-with-scheduling-entities"></a>使用计划 API 对计划实体执行操作

_**适用于：** 基于资源/非库存场景的 Project Operations，精简部署 - 估价开票交易_

> [!IMPORTANT] 
> 本主题中所述的部分或所有功能属于预览版内容。 相关内容和功能可能会发生更改。 

## <a name="scheduling-entities"></a>计划实体

通过计划 API，可以针对 **计划实体** 执行创建、更新和删除操作。 这些实体通过 Web 项目中的计划引擎进行管理。 早期 Dynamics 365 Project Operations 版本中限制对 **计划实体** 执行创建、更新和删除操作。

下表提供了 **计划实体** 的完整列表。

| 实体名称  | 实体逻辑名称 |
| --- | --- |
| Project | msdyn_project |
| 项目任务  | msdyn_projecttask  |
| 项目任务依赖关系  | msdyn_projecttaskdependency  |
| 资源分派 | msdyn_resourceassignment |
| 项目 Bucket  | msdyn_projectbucket |
| 项目团队成员 | msdyn_projectteam |

## <a name="operationset"></a>OperationSet

OperationSet 是一种工作单位模式，当必须在交易内处理多个计划影响请求时，可以使用该模式。

## <a name="schedule-apis"></a>计划 API

下面是当前计划 API 的列表。

- **msdyn_CreateProjectV1**：此 API 可用于创建项目。 将立即创建项目和默认项目 Bucket。
- **msdyn_CreateTeamMemberV1**：此 API 可用于创建项目团队成员。 系统会立即创建团队成员记录。
- **msdyn_CreateOperationSetV1**：此 API 可用于安排必须在交易中执行多个请求。
- **msdyn_PSSCreateV1**：此 API 可用于创建实体。 该实体可以是支持创建操作的任何计划实体。
- **msdyn_PSSUpdateV1**：此 API 可用于更新实体。 该实体可以是支持更新操作的任何计划实体。
- **msdyn_PSSDeleteV1**：此 API 可用于删除实体。 该实体可以是支持删除操作的任何计划实体。
- **msdyn_ExecuteOperationSetV1**：此 API 用于执行给定操作集内的所有操作。

## <a name="using-schedule-apis-with-operationset"></a>将计划 API 与 OperationSet 一同使用

由于会立即创建同时具有 **CreateProjectV1** 和 **CreateTeamMemberV1** 的记录，因此这些 API 不能直接在 **OperationSet** 中使用。 但是，可以使用 API 创建所需记录，创建 **OperationSet**，然后在 **OperationSet** 中使用这些预先创建的记录。

## <a name="supported-operations"></a>不支持的操作

| 计划实体 | 创建​​ | 更新 | Delete | 重要考虑因素 |
| --- | --- | --- | --- | --- |
项目任务 | 是 | 是 | 是 | 无​ |
| 项目任务依赖关系 | 是 | 是 | | 不会更新项目任务依赖关系记录。 而是可以删除旧记录，并可以创建新记录。 |
| 资源分派 | 是 | 是 | | 不支持对以下字段执行操作：**BookableResourceID**、**Effort**、**EffortCompleted**、**EffortRemaining** 和 **PlannedWork**。 资源分派记录不会更新。 而是可以删除旧记录，并可以创建新记录。 |
| 项目 Bucket | 不适用 | 不适用 | 不适用 | 使用 **CreateProjectV1** API 创建了默认 Bucket。 |
| 项目团队成员 | 是 | 是 | 是 | 对于创建操作，请使用 **CreateTeamMemberV1** API。 |
| Project | 是 | 是 | 不适用 | 不支持以下对字段执行操作：**StateCode**、**BulkGenerationStatus**、**GlobalRevisionToken**、**CalendarID**、**Effort**、**EffortCompleted**、**EffortRemaining**、**Progress**、**Finish**、**TaskEarliestStart** 和 **Duration**。 |

可以对包含自定义字段的实体对象调用这些 API。

ID 属性是可选的。 如果提供了此属性，则系统会尝试使用它，如果无法使用它，则会引发异常。 如果未提供此属性，系统将生成它。

## <a name="limitations-and-known-issues"></a>限制和已知问题
下面是一系列限制和已知问题：

- 计划 API 仅供 **具有 Microsoft 项目许可证的用户** 使用。 以下用户不能使用它们：
    - 应用程序用户
    - 系统用户
    - 集成用户
    - 没有所需许可证的其他用户
- 每个 **OperationSets** 最多只能有 100 项操作。
- 每个用户最多只能有 10 个公开的 **OperationSets**。
- Project Operations 目前对一个项目最多支持总共 500 个任务。
- **OperationSet** 故障状态和故障日志当前不可用。
- 计划 API 为公开预览版。 Microsoft 不支持在生产环境中使用这些 API。

## <a name="sample-scenario"></a>示例方案

在此方案中，您将创建一个项目、一个团队成员、四个任务和两个资源分派。 接下来，您将更新一个任务、更新项目、删除一个任务、删除一个资源分派以及创建任务依赖项。

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

## <a name="additional-samples"></a>其他示例

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