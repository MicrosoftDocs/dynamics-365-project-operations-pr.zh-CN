---
title: 项目计划日志
description: 本文提供的信息和示例将帮助您使用项目计划日志来跟踪与项目计划服务和项目计划 API 相关的故障。
author: ruhercul
ms.date: 11/30/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: ruhercul
ms.openlocfilehash: c57419642e90e4def01f2cd2474c9e82dc162b86
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8923684"
---
# <a name="project-scheduling-logs"></a>项目计划日志

_**适用于：** 基于资源/非库存场景的 Project Operations、精简部署 - 估价交易开单_、_Project for the Web_

Microsoft Dynamics 365 Project Operations 将 [Project for the Web](https://support.microsoft.com/office/what-is-project-for-the-web-c19b2421-3c9d-4037-97c6-f66b6e1d2eb5) 用作其主计划引擎。 Project Operations 使用新的项目计划 API 创建、更新和删除项目任务、资源分配、任务依赖项、项目 Bucket 和项目团队成员，而不是使用标准 Microsoft Dataverse Web 应用程序编程接口 (API)。 但是，以编程方式对工作分解结构 (WBS) 实体运行创建、更新或删除操作时，可能会发生错误。 为了跟踪这些错误和操作历史记录，已经实施了两个新管理日志：**操作集** 和 **项目计划服务 (PSS)**。 若要访问这些日志，请转到 **设置** \> **计划集成**。

下图显示了项目计划日志的数据模型。

![项目计划日志的数据模型。](media/LOGDATAMODEL.jpg)

## <a name="operation-set-log"></a>操作集日志

操作集日志跟踪操作集的执行情况，此操作集用于对项目、项目任务、资源分配、任务依赖项、项目 Bucket 或项目团队成员分批运行一个或多个创建、更新或删除操作。 **操作状态** 字段显示操作集的整体状态。 相关操作集详细信息记录中捕获了操作集有效负载的详细信息。

### <a name="operation-set"></a>操作集

下表显示了与 **操作集** 实体相关的字段。

| 架构名称            | Description                                                                                                  | DisplayName            |
|-----------------------|--------------------------------------------------------------------------------------------------------------|------------------------|
| msdyn_completedon     | 操作集完成或失败的日期/时间。                                                | CompletedOn            |
| msdyn_correlationid   | 请求的 **correlationId** 值。                                                                  | CorrelationId          |
| msdyn_description     | 操作集的说明。                                                                        | Description            |
| msdyn_executedon      | 运行记录的日期/时间。                                                                       | 执行时间            |
| msdyn_operationsetId  | 实体实例的唯一标识符。                                                                   | OperationSet           |
| msdyn_Project         | 与操作集相关的项目。                                                            | Project                |
| msdyn_projectid       | 请求的 **projectId** 值。                                                                      | ProjectId (已弃用) |
| msdyn_projectName     | 不适用。                                                                                              | 不适用         |
| msdyn_PSSErrorLog     | 与操作集关联的项目计划服务错误日志的唯一标识符。 | PSS 错误日志          |
| msdyn_PSSErrorLogName | 不适用。                                                                                              | 不适用         |
| msdyn_status          | 操作集的状态。                                                                             | Status                 |
| msdyn_statusName      | 不适用。                                                                                              | 不适用         |
| msdyn_useraadid       | 此请求所属的用户的 Azure Active Directory (Azure AD) 对象 ID。                     | UserAADID              |

### <a name="operation-set-detail"></a>操作集详细信息

下表显示了与 **操作集详细信息** 实体相关的字段。

| 架构名称                 | Description                                                                                 | DisplayName           |
|----------------------------|---------------------------------------------------------------------------------------------|-----------------------|
| msdyn_cdspayload           | 请求的序列化 Dataverse 字段。                                            | CdsPayload            |
| msdyn_entityname           | 此请求的实体的名称。                                                     | EntityName            |
| msdyn_httpverb             | 请求方法。                                                                         | HTTP 谓词(已弃用) |
| msdyn_httpverbName         | 不适用。                                                                             | 不适用        |
| msdyn_operationset         | 此记录所属的操作集的唯一标识符。                      | OperationSet          |
| msdyn_operationsetdetailId | 实体实例的唯一标识符。                                                  | OperationSet 详细信息   |
| msdyn_operationsetName     | 不适用。                                                                             | 不适用        |
| msdyn_operationtype        | 操作集的操作类型详细信息。                                             | OperationType         |
| msdyn_operationtypeName    | 不适用。                                                                             | 不适用        |
| msdyn_psspayload           | 请求的序列化项目计划服务字段。                           | PssPayload            |
| msdyn_recordid             | 请求记录的标识符。                                                       | 记录 ID             |
| msdyn_requestnumber        | 用于标识收到请求的顺序的自动生成编号。 | 请求编号        |

## <a name="project-scheduling-service-error-logs"></a>项目计划服务错误日志

项目计划服务错误日志捕获项目计划服务尝试 **保存** 或 **打开** 操作时发生的失败。 生成这些日志的受支持场景有以下三种：

- 用户启动的操作严重失败（例如，由于缺少特权而无法创建分配）。
- 项目计划服务无法以编程方式对实体创建、更新、删除或执行任何其他级联操作。
- 当记录无法打开时（例如，打开项目或更新团队成员信息时），用户会遇到错误。

### <a name="project-scheduling-service-log"></a>项目计划服务日志

下表显示了项目计划服务日志中包含的字段。

| 架构名称          | Description                                                                    | DisplayName    |
|---------------------|--------------------------------------------------------------------------------|----------------|
| msdyn_CallStack     | 异常的调用堆栈。                                               | 调用堆栈     |
| msdyn_correlationid | 错误的相关 ID。                                               | CorrelationId  |
| msdyn_errorcode     | 用于存储 Dataverse 错误代码或 HTTP 错误代码的字段。 | 错误代码     |
| msdyn_HelpLink      | 指向公共帮助文档的链接。                                       | 帮助链接      |
| msdyn_log           | 项目计划服务中的日志。                                   | 日志            |
| msdyn_project       | 与错误日志关联的项目。                             | Project        |
| msdyn_projectName   | 项目名称（如果将保留操作集有效负载）。 | 不适用 |
| msdyn_psserrorlogId | 实体实例的唯一标识符。                                     | PSS 错误日志  |
| msdyn_SessionId     | 项目会话 ID。                                                        | 会话 ID     |

## <a name="error-log-cleanup"></a>错误日志清理

默认情况下，项目计划服务错误日志和“操作集”日志可以每 90 天清理一次。 将删除任何超过 90 天的记录。 但是，通过更改 **项目参数** 页面上 **msdyn_StateOperationSetAge** 字段的值，管理员可以调整清理范围，使其介于 1 到 120 天之间。 可以使用多种方法来更改此值：

- 通过创建自定义页面并添加 **已过期的操作集存在时间** 字段来自定义 **项目参数** 实体。
- 使用利用 [WebApi 软件开发工具包 (SDK)](/powerapps/developer/model-driven-apps/clientapi/reference/xrm-webapi/updaterecord) 的客户端代码。
- 在模型驱动应用中使用利用 Xrm SDK **updateRecord** 方法（客户端 API 参考）的服务 SDK 代码。 Power Apps 包含 **updateRecord** 方法的描述和受支持参数。

    ```C#
    Xrm.WebApi.retrieveMultipleRecords('msdyn_projectparameter').then(function (response) {
        parameter = response.entities[0];
        var staleOperationValue = prompt("All records older than (x) days will be deleted, please enter X between 1 to 90 days", 1)
        var newData = {};
        newData.msdyn_projectparameterid = parameter.msdyn_projectparameterid;
        newData.msdyn_staleoperationsetage = parseInt(staleOperationValue);
        Xrm.WebApi.updateRecord("msdyn_projectparameter", parameter.msdyn_projectparameterid, newData).then(
            function success(result) {
                console.log("Project Parameter: Stale Operation Expiry is set to: " + newData.msdyn_staleoperationsetage);
                // perform operations on record update
                Xrm.WebApi.retrieveMultipleRecords('msdyn_projectparameter')
                .then(function (response2) { console.log("Confirmed Project Parameter: Stale Operation Expiry is set to: " + response2.entities[0].msdyn_staleoperationsetage) });
            },
            function (error) {
                console.log("Failed to Update Project Ednpoint with error: " + error.message);
            // handle error conditions
            }
        );
    });
    ```
