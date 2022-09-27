---
title: 使用项目计划 API 对计划实体执行操作
description: 本文提供有关使用项目计划 API 的信息和示例。
author: sigitac
ms.date: 01/13/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 159d395efff98f2af780e5ed1e5ab3d6483cba89
ms.sourcegitcommit: b1c26ea57be721c5b0b1a33f2de0380ad102648f
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/20/2022
ms.locfileid: "9541113"
---
# <a name="use-project-schedule-apis-to-perform-operations-with-scheduling-entities"></a>使用项目计划 API 对计划实体执行操作

_**适用于：** 基于资源/非库存场景的 Project Operations，精简部署 - 估价开票交易_


**计划实体**

项目计划 API 提供对 **计划实体** 执行创建、更新和删除操作的能力。 这些实体通过 Web 项目中的计划引擎进行管理。 早期 Dynamics 365 Project Operations 版本中限制对 **计划实体** 执行创建、更新和删除操作。

下表提供了项目计划实体的完整列表。

| **实体名称**         | **实体逻辑名称**     |
|-------------------------|-----------------------------|
| Project                 | msdyn_project               |
| 项目任务            | msdyn_projecttask           |
| 项目任务依赖关系 | msdyn_projecttaskdependency |
| 资源分派     | msdyn_resourceassignment    |
| 项目 Bucket          | msdyn_projectbucket         |
| 项目团队成员     | msdyn_projectteam           |
| 项目清单      | msdyn_projectchecklist      |
| 项目标签           | msdyn_projectlabel          |
| 要标记的项目任务   | msdyn_projecttasktolabel    |
| 项目冲刺(sprint)          | msdyn_projectsprint         |

**OperationSet**

OperationSet 是一种工作单位模式，当必须在交易内处理多个计划影响请求时，可以使用该模式。

**项目计划 API**

下面是当前项目计划 API 的列表。

| **API**                                 | 说明                                                                                                                        |
|-----------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| **msdyn_CreateProjectV1**               | 此 API 用于创建项目。 项目和默认项目桶会立即创建。                         |
| **msdyn_CreateTeamMemberV1**            | 此 API 用于创建项目团队成员。 系统会立即创建团队成员记录。                                  |
| **msdyn_CreateOperationSetV1**          | 此 API 用于计划必须在交易中执行的多个请求。                                        |
| **msdyn_PssCreateV1**                   | 此 API 用于创建实体。 该实体可以是支持创建操作的任何项目计划实体。 |
| **msdyn_PssUpdateV1**                   | 此 API 用于更新实体。 实体可以是支持更新操作的任意项目计划实体  |
| **msdyn_PssDeleteV1**                   | 此 API 用于删除实体。 该实体可以是支持删除操作的任何项目计划实体。 |
| **msdyn_ExecuteOperationSetV1**         | 此 API 用于执行给定操作集内的所有操作。                                                 |
| **msdyn_PssUpdateResourceAssignmentV1** | 此 API 用于更新资源分配计划的工作分布。                                                        |



**将项目计划 API 与 OperationSet 一起使用**

由于会立即创建同时具有 **CreateProjectV1** 和 **CreateTeamMemberV1** 的记录，因此这些 API 不能直接在 **OperationSet** 中使用。 但是，可以使用 API 创建所需记录，创建 **OperationSet**，然后在 **OperationSet** 中使用这些预先创建的记录。

**不支持的操作**

| **计划实体**   | **创建** | **Update** | **Delete** | **重要考虑因素**                                                                                                                                                                                                                                                                                                                            |
|-------------------------|------------|------------|------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 项目任务            | 是        | 是        | 是        | **Progress**、**EffortCompleted** 和 **EffortRemaining** 字段可以在 Project for the Web 中进行编辑，但不能在 Project Operations 中编辑。                                                                                                                                                                                             |
| 项目任务依赖关系 | 是        | No         | 是        | 不会更新项目任务依赖关系记录。 而是可以删除旧记录，并可以创建新记录。                                                                                                                                                                                                                                 |
| 资源分派     | 是        | 是\*      | 是        | 不支持对以下字段执行操作：**BookableResourceID**、**Effort**、**EffortCompleted**、**EffortRemaining** 和 **PlannedWork**。 资源分派记录不会更新。 而是可以删除旧记录，并可以创建新记录。 提供了一个单独的 API 来更新资源分配分布。 |
| 项目 Bucket          | 是        | 是        | 是        | 默认桶使用 **CreateProjectV1** API 创建。 更新版 16 中添加了对创建和删除项目桶的支持。                                                                                                                                                                                                   |
| 项目团队成员     | 是        | 是        | 是        | 对于创建操作，请使用 **CreateTeamMemberV1** API。                                                                                                                                                                                                                                                                                           |
| 集成                 | 是        | 是        |            | 不支持以下对字段执行操作：**StateCode**、**BulkGenerationStatus**、**GlobalRevisionToken**、**CalendarID**、**Effort**、**EffortCompleted**、**EffortRemaining**、**Progress**、**Finish**、**TaskEarliestStart** 和 **Duration**。                                                                                       |
| 项目清单      | 是        | 是        | 是        |                                                                                                                                                                                                                                                                                                                                                         |
| 项目标签           | No         | 是        | No         | 标签名称可以更改。 此功能只能用于 Project for the Web                                                                                                                                                                                                                                                                      |
| 要标记的项目任务   | 是        | No         | 是        | 此功能只能用于 Project for the Web                                                                                                                                                                                                                                                                                                  |
| 项目冲刺(sprint)          | 是        | 是        | 是        | **开始** 字段的日期必须早于 **完成** 字段。 同一项目的冲刺不能相互重叠。 此功能只能用于 Project for the Web                                                                                                                                                                    |




ID 属性是可选的。 如果提供了此属性，则系统会尝试使用它，如果无法使用它，则会引发异常。 如果未提供此属性，系统将生成它。

**限制和已知问题**

下面是一系列限制和已知问题：

-   项目计划 API 仅供 **具有 Microsoft Project 许可证的用户** 使用。 以下用户不能使用它们：
    -   应用程序用户
    -   系统用户
    -   集成用户
    -   没有所需许可证的其他用户
-   每个 **OperationSets** 最多只能有 100 项操作。
-   每个用户最多只能有 10 个公开的 **OperationSets**。
-   Project Operations 目前对一个项目最多支持总共 500 个任务。
-   每个更新资源分配分布操作计为一次操作。
-   每个更新分布的列表最多可以包含 100 个时间片段。
-   **OperationSet** 故障状态和故障日志当前不可用。
-   每个项目最多有 400 个冲刺。
-   [项目和任务的限制和界限](/project-for-the-web/project-for-the-web-limits-and-boundaries)。
-   标签目前只能用于 Project for the Web。

**错误处理**

-   要查看操作集生成的错误，转到 **设置** \> **计划集成** \> **操作集**。
-   若要查看项目计划服务生成的错误，请转到 **设置** \> **计划集成** \> **PSS 错误日志**。

**编辑资源分配分布**

与更新实体的所有其他项目计划 API 不同，资源分配分布 API 仅负责单个实体 msydn_resourceassignment 上的单个字段 msdyn_plannedwork 的更新。

给定计划模式为：

-   **固定单位**
-   项目日历是 9-5p 是 9-5pst，周一、周二、周四、周五（周三无工作）
-   资源日历为太平洋标准时间周一到周五 9-1p

此分配为期一周，每天四个小时。 这是因为资源日历是从太平洋标准时间 9-1 开始，或每天四个小时。

| &nbsp;     | 任务 | 开始日期 | 结束日期  | 数量 | 2022 年 6 月 13 日 | 2022 年 6 月 14 日 | 2022 年 6 月 15 日 | 2022 年 6 月 16 日 | 2022 年 6 月 17 日 |
|------------|------|------------|-----------|----------|-----------|-----------|-----------|-----------|-----------|
| 9-1 工作人员 |  T1  | 2022 年 6 月 13 日  | 2022 年 6 月 17 日 | 20       | 4         | 4         | 4         | 4         | 4         |

例如，如果您希望工作人员本周每天只工作三个小时，为其他任务留出一小时。

#### <a name="updatedcontours-sample-payload"></a>UpdatedContours 示例有效负载：

```json
[{

"minutes":900.0,

"start":"2022-06-13T00:00:00-07:00",

"end":"2022-06-18T00:00:00-07:00"

}]
```

这是更新分布计划 API 运行后的分配。

| &nbsp;     | 任务 | 开始日期 | 结束日期  | 数量 | 2022 年 6 月 13 日 | 2022 年 6 月 14 日 | 2022 年 6 月 15 日 | 2022 年 6 月 16 日 | 2022 年 6 月 17 日 |
|------------|------|------------|-----------|----------|-----------|-----------|-----------|-----------|-----------|
| 9-1 工作人员 | T1   | 2022 年 6 月 13 日  | 2022 年 6 月 17 日 | 15       | 3         | 3         | 3         | 3         | 3         |


**示例方案**

在此方案中，您将创建一个项目、一个团队成员、四个任务和两个资源分派。 接下来，您将更新一个任务、更新项目、删除一个任务、删除一个资源分派以及创建任务依赖项。

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

**其他示例

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
