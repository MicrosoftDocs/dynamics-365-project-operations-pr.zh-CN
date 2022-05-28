---
title: 通过 Power Automate 使用项目计划 API
description: 本主题提供了一个使用项目计划应用程序编程接口 (API) 的示例流。
author: ruhercul
ms.date: 01/26/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: ruhercul
ms.openlocfilehash: 9708226b0955cfa6c405b9616c14765f9ebc21f7
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/14/2022
ms.locfileid: "8597695"
---
# <a name="use-project-schedule-apis-with-power-automate"></a>通过 Power Automate 使用项目计划 API

_**适用于：** 基于资源/非库存场景的 Project Operations，精简部署 - 估价开票交易_

本主题描述了一个示例流，展示了如何使用 Microsoft Power Automate 创建完整的项目计划、如何创建操作集以及如何更新实体。 示例演示了如何创建项目、项目团队成员、操作集、项目任务和资源分配。。 本主题还解释了如何更新实体和执行操作集。

以下是本主题的示例流中记录的步骤的完整列表：

1. [创建 PowerApps 触发器](#1)
2. [创建项目](#2)
3. [为团队成员初始化变量](#3)
4. [创建通用团队成员](#4)
5. [创建操作集](#5)
6. [创建项目桶](#6)
7. [为链接状态初始化变量](#7)
8. [为任务数初始化变量](#8)
9. [为项目任务 ID 初始化变量](#9)
10. [执行，直至](#10)
11. [设置项目任务](#11)
12. [创建项目任务](#12)
13. [创建资源分配](#13)
14. [减少变量](#14)
15. [重命名项目任务](#15)
16. [运行操作集](#16)

## <a name="assumptions"></a>假设

本主题假设您具备 Dataverse 平台、云端流和项目计划应用程序编程接口 (API) 的基本知识。 有关详细信息，请参阅本主题后面的[参考](#references)一节。

## <a name="create-a-flow"></a>创建流

### <a name="select-an-environment"></a>选择环境

您可以在您的环境中创建 Power Automate 流。

1. 转到 <https://flow.microsoft.com>，使用您的管理员凭据登录。
2. 在右上角，选择 **环境**。
3. 在列表中，选择安装了 Dynamics 365 Project Operations 的环境。

### <a name="create-a-solution"></a>创建解决方案

请按照以下步骤创建[解决方案识别流](/power-automate/overview-solution-flows)。 通过创建解决方案识别流，您可以更轻松地导出流以供以后使用。

1. 在导航窗格中，选择 **解决方案**。
2. 在 **解决方案** 页上，选择 **新建解决方案**。
3. 在 **新建解决方案** 对话框中，设置所需字段，然后选择 **创建**。

## <a name="step-1-create-a-powerapps-trigger"></a><a id="1"></a>步骤 1：创建 PowerApps 触发器

1. 在 **解决方案** 页面上，选择您创建的解决方案，然后选择 **新建**。
2. 在左侧窗格中，选择 **云端流** \> **自动化** \> **云端流** \> **即时**。
3. 在 **流名称** 字段中，输入 **计划 API 演示流**。
4. 在 **选择如何触发此流** 列表中，选择 **Power Apps**。 创建 Power Apps 触发器时，逻辑由您（作者）决定。 在本主题中，将输入参数留空以进行测试。
5. 选择 **创建**。

## <a name="step-2-create-a-project"></a><a id="2"></a>步骤 2：创建项目

执行以下步骤创建一个示例项目。

1. 在您创建的流中，选择 **新建步骤**。

    ![添加一个新步骤。](media/newstep.png)

2. 在 **选择操作** 对话框的搜索字段中，输入 **执行解除绑定操作**。 然后在 **操作** 选项卡上，在结果列表中选择操作。

    ![选择一个操作。](media/chooseactiontab.png)

3. 在新步骤中，选择省略号 (**...**)，然后选择 **重命名**。

![重命名一个步骤。](media/renamestep.png)

4. 重命名步骤 **创建项目**。
5. 在 **操作名称** 字段中，选择 **msdyn\_CreateProjectV1**。
6. 在 **msdyn\_subject** 字段下，选择 **添加动态内容**。
7. 在 **表达式** 选项卡的函数字段中，输入 **Project name - utcNow()**。
8. 选择 **确定**。

## <a name="step-3-initialize-a-variable-for-the-team-member"></a><a id="3"></a>步骤 3：为团队成员初始化变量

1. 在流中，选择 **新建步骤**。
2. 在 **选择操作** 对话框的搜索字段中，输入 **初始化变量**。 然后在 **操作** 选项卡上，在结果列表中选择操作。
3. 在新步骤中，选择省略号 (**...**)，然后选择 **重命名**。
4. 重命名步骤 **初始化团队成员**。
5. 在 **名称** 字段中，输入 **TeamMemberAction**。
6. 在 **类型** 字段中，选择 **字符串**。
7. 在 **值** 字段中，输入 **msdyn\_CreateTeamMemberV1**。

## <a name="step-4-create-a-generic-team-member"></a><a id="4"></a>步骤 4：创建一般团队成员

1. 在流中，选择 **新建步骤**。
2. 在 **选择操作** 对话框的搜索字段中，输入 **执行解除绑定操作**。 然后在 **操作** 选项卡上，在结果列表中选择操作。
3. 在新步骤中，选择省略号 (**...**)，然后选择 **重命名**。
4. 重命名步骤 **创建团队成员**。
5. 对于 **操作名称** 字段，在 **动态内容** 对话框中选择 **TeamMemberAction**。
6. 在 **操作参数** 字段中，输入以下参数信息。

    ```
    {
        "TeamMember": {
            "@@odata.type": "Microsoft.Dynamics.CRM.msdyn_projectteam",
            "msdyn_projectteamid": "@{guid()}",
            "msdyn_project@odata.bind": "/msdyn_projects(@{outputs('Create_Project')?['body/ProjectId']})",
            "msdyn_name": "ScheduleAPIDemoTM1"
        }
    } 
    ```

    以下是对参数的说明：

    - **\@\@odata.type** – 实体名称。 例如，输入 **"Microsoft.Dynamics.CRM.msdyn\_projectteam"**。
    - **msdyn\_projectteamid** – 项目团队 ID 的主键。 此值是一个全局唯一标识符 (GUID) 表达式。   ID 从表达式选项卡生成。

    - **msdyn\_project\@odata.bind** – 所负责项目的项目 ID。 此值将是来自“创建项目”步骤响应的动态内容。 请确保输入完整路径并在括号之间添加动态内容。 需要使用引号。 例如，输入 **"/msdyn\_projects(ADD DYNAMIC CONTENT)"**。
    - **msdyn\_name** – 团队成员的名称。 例如，输入 **"ScheduleAPIDemoTM1"**。

## <a name="step-5-create-an-operation-set"></a><a id="5"></a>步骤 5：创建操作集

1. 在流中，选择 **新建步骤**。
2. 在 **选择操作** 对话框的搜索字段中，输入 **执行解除绑定操作**。 然后在 **操作** 选项卡上，在结果列表中选择操作。
3. 在新步骤中，选择省略号 (**...**)，然后选择 **重命名**。
4. 重命名步骤 **创建操作集**。
5. 在 **操作名称** 字段中，选择 **msdyn\_CreateOperationSetV1** Dataverse 自定义操作。
6. 在 **说明** 字段中，输入 **ScheduleAPIDemoOperationSet**。
7. 在 **项目** 字段中，输入 **/msdyn\_projects(**。
8. 在 **动态内容** 对话框中，选择 **msdyn\_CreateProjectV1Response ProjectId**。
9. 在 **项目** 字段中，输入 **)**。

## <a name="step-6-create-a-project-bucket"></a><a id="6"></a>步骤 6：创建项目桶

1. 在流中，选择 **新建步骤**。
2. 在 **选择操作** 对话框的搜索字段中，输入 **添加新行**。 然后在 **操作** 选项卡上，在结果列表中选择操作。
3. 在新步骤中，选择省略号 (**...**)，然后选择 **重命名**。
4. 重命名步骤 **创建桶**。
5. 在 **表名称** 字段中，选择 **项目桶**。
6. 在 **名称** 字段中，输入 **ScheduleAPIDemoBucket1**。
7. 对于 **项目** 字段，在 **动态内容** 对话框中选择 **msdyn\_CreateProjectV1Response ProjectId**。

## <a name="step-7-initialize-a-variable-for-the-link-status"></a><a id="7"></a>步骤 7：为链接状态初始化变量

1. 在流中，选择 **新建步骤**。
2. 在 **选择操作** 对话框的搜索字段中，输入 **初始化变量**。 然后在 **操作** 选项卡上，在结果列表中选择操作。
3. 在新步骤中，选择省略号 (**...**)，然后选择 **重命名**。
4. 重命名步骤 **Init linkstatus**。
5. 在 **名称** 字段中，输入 **linkstatus**。
6. 在 **类型** 字段中，选择 **整数**。
7. 在 **值** 字段中，输入 **192350000**。

## <a name="step-8-initialize-a-variable-for-the-number-of-tasks"></a><a id="8"></a>步骤 8：为任务数初始化变量

1. 在流中，选择 **新建步骤**。
2. 在 **选择操作** 对话框的搜索字段中，输入 **初始化变量**。 然后在 **操作** 选项卡上，在结果列表中选择操作。
3. 在新步骤中，选择省略号 (**...**)，然后选择 **重命名**。
4. 重命名步骤 **初始化任务数**。
5. 在 **名称** 字段中，输入 **任务数**。
6. 在 **类型** 字段中，选择 **整数**。
7. 在 **值** 字段中，输入 **5**。

## <a name="step-9-initialize-a-variable-for-the-project-task-id"></a><a id="9"></a>步骤 9：为项目任务 ID 初始化变量

1. 在流中，选择 **新建步骤**。
2. 在 **选择操作** 对话框的搜索字段中，输入 **初始化变量**。 然后在 **操作** 选项卡上，在结果列表中选择操作。
3. 在新步骤中，选择省略号 (**...**)，然后选择 **重命名**。
4. 重命名步骤 **Init ProjectTaskID**。
5. 在 **名称** 字段中，输入 **任务数**。
6. 在 **类型** 字段中，选择 **字符串**。
7. 对于 **值** 字段，在表达式生成器中输入 **guid()**。

## <a name="step-10-do-until"></a><a id="10"></a>步骤 10：执行，直至

1. 在流中，选择 **新建步骤**。
2. 在 **选择操作** 对话框的搜索字段中，输入 **执行，直至**。 然后在 **操作** 选项卡上，在结果列表中选择操作。
3. 将条件语句中的第一个值设置为 **动态内容** 对话框中的 **number of tasks** 变量。
4. 将条件设置为 **less than equal to**。
5. 将条件语句中的第二个值设置为 **0**。

## <a name="step-11-set-a-project-task"></a><a id="11"></a>步骤 11：设置项目任务

1. 在流中，选择 **新建步骤**。
2. 在 **选择操作** 对话框的搜索字段中，输入 **设置变量**。 然后在 **操作** 选项卡上，在结果列表中选择操作。
3. 在新步骤中，选择省略号 (**...**)，然后选择 **重命名**。
4. 重命名步骤 **设置项目任务**。
5. 在 **名称** 字段中，选择 **msdyn\_projecttaskid**。
6. 对于 **值** 字段，在表达式生成器中输入 **guid()**。

## <a name="step-12-create-a-project-task"></a><a id="12"></a>步骤 12：创建项目任务

按照以下步骤创建一个项目任务，该任务具有属于当前项目和您创建的项目桶的唯一 ID。

1. 在流中，选择 **新建步骤**。
2. 在 **选择操作** 对话框的搜索字段中，输入 **执行解除绑定操作**。 然后在 **操作** 选项卡上，在结果列表中选择操作。
3. 在步骤中，选择省略号 (**...**)，然后选择 **重命名**。
4. 重命名步骤 **创建项目任务**。
5. 在 **操作名称** 字段中，选择 **msdyn\_PssCreateV1**。
6. 在 **实体** 字段中，输入以下参数信息。

    ```
    {
        "@@odata.type": "Microsoft.Dynamics.CRM.msdyn_projecttask",
        "msdyn_projecttaskid": "@{variables('msdyn_projecttaskid')}",
        "msdyn_project@odata.bind": "/msdyn_projects(@{outputs('Create_Project')?['body/ProjectId']})",
        "msdyn_subject": "ScheduleAPIDemoTask1",
        "msdyn_projectbucket@odata.bind": "/msdyn_projectbuckets(@{outputs('Create_Project_Buckets')?['body/msdyn_projectbucketid']})",
        "msdyn_start": "@{addDays(utcNow(), 1)}",
        "msdyn_scheduledstart": "@{utcNow()}",
        "msdyn_scheduledend": "@{addDays(utcNow(), 5)}",
        "msdyn_LinkStatus": "192350000"
    }
    ```

    以下是对参数的说明：

    - **\@\@odata.type** – 实体名称。 例如，输入 **"Microsoft.Dynamics.CRM.msdyn\_projecttask"**。
    - **msdyn\_projecttaskid** – 任务的唯一 ID。 此值应设置为 **msdyn\_projecttaskid** 中的动态变量。
    - **msdyn\_project\@odata.bind** – 所负责项目的项目 ID。 此值将是来自“创建项目”步骤响应的动态内容。 请确保输入完整路径并在括号之间添加动态内容。 需要使用引号。 例如，输入 **"/msdyn\_projects(ADD DYNAMIC CONTENT)"**。
    - **msdyn\_subject** – 任意任务名称。
    - **msdyn\_projectbucket\@odata.bind** – 包含任务的项目桶。 此值将是来自“创建桶”步骤响应的动态内容。 请确保输入完整路径并在括号之间添加动态内容。 需要使用引号。 例如，输入 **"/msdyn\_projectbuckets(ADD DYNAMIC CONTENT)"**。
    - **msdyn\_start** – 开始日期的动态内容。 例如，明天将表示为 **"addDays(utcNow(), 1)"**。
    - **msdyn\_scheduledstart** – 计划开始日期。 例如，明天将表示为 **"addDays(utcNow(), 1)"**。
    - **msdyn\_scheduleend** – 计划结束日期。 选择一个未来的日期。 例如，指定 **"addDays(utcNow(), 5)"**。
    - **msdyn\_LinkStatus** – 链接状态。 例如，输入 **"192350000"**。

7. 对于 **OperationSetId** 字段，在 **动态内容** 对话框中选择 **msdyn\_CreateOperationSetV1Response**。

## <a name="step-13-create-a-resource-assignment"></a><a id="13"></a>步骤 13：创建资源分配

1. 在流中，选择 **新建步骤**。
2. 在 **选择操作** 对话框的搜索字段中，输入 **执行解除绑定操作**。 然后在 **操作** 选项卡上，在结果列表中选择操作。
3. 在步骤中，选择省略号 (**...**)，然后选择 **重命名**。
4. 重命名步骤 **创建分配**。
5. 在 **操作名称** 字段中，选择 **msdyn\_PssCreateV1**。
6. 在 **实体** 字段中，输入以下参数信息。

    ```
    {
        "@odata.type": "Microsoft.Dynamics.CRM.msdyn_resourceassignment",
        "msdyn_resourceassignmentid": "@{guid()}",
        "msdyn_name": "ScheduleAPIDemoAssign1",
        "msdyn_taskid@odata.bind": "/msdyn_projecttasks(@{variables('msdyn_projecttaskid')})",
        "msdyn_projectteamid@odata.bind": "/msdyn_projectteams(@{outputs('Create_Team_Member')?['body/TeamMemberId']})",
        "msdyn_projectid@odata.bind": "/msdyn_projects(@{outputs('Create_Project')?['body/ProjectId']})"
    }
    ```

7. 对于 **OperationSetId** 字段，在 **动态内容** 对话框中选择 **msdyn\_CreateOperationSetV1Response**。

## <a name="step-14-decrement-a-variable"></a><a id="14"></a>步骤 14：减少变量

1. 在流中，选择 **新建步骤**。
2. 在 **选择操作** 对话框的搜索字段中，输入 **减少变量**。 然后在 **操作** 选项卡上，在结果列表中选择操作。
3. 在 **名称** 字段中，选择 **任务数**。
4. 在 **值** 字段中，输入 **1**。

## <a name="step-15-rename-a-project-task"></a><a id="15"></a>步骤 15：重命名项目任务

1. 在流中，选择 **新建步骤**。
2. 在 **选择操作** 对话框的搜索字段中，输入 **执行解除绑定操作**。 然后在 **操作** 选项卡上，在结果列表中选择操作。
3. 在步骤中，选择省略号 (**...**)，然后选择 **重命名**。
4. 重命名步骤 **重命名项目任务**。
5. 在 **操作名称** 字段中，选择 **msdyn\_PssUpdateV1**。
6. 在 **实体** 字段中，输入以下参数信息。

    ```
    {
        "@@odata.type": "Microsoft.Dynamics.CRM.msdyn_projecttask",
        "msdyn_projecttaskid": "@{variables('msdyn_projecttaskid')}",
        "msdyn_subject": "ScheduleDemoTask1-UpdatedName"
    }
    ```

7. 对于 **OperationSetId** 字段，在 **动态内容** 对话框中选择 **msdyn\_CreateOperationSetV1Response**。

## <a name="step-16-run-an-operation-set"></a><a id="16"></a>步骤 16：运行操作集

1. 在流中，选择 **新建步骤**。
2. 在 **选择操作** 对话框的搜索字段中，输入 **执行解除绑定操作**。 然后在 **操作** 选项卡上，在结果列表中选择操作。
3. 在步骤中，选择省略号 (**...**)，然后选择 **重命名**。
4. 重命名步骤 **执行操作集**。
5. 在 **操作名称** 字段中，选择 **msdyn\_ExecuteOperationSetV1**。
6. 对于 **OperationSetId** 字段，在 **动态内容** 对话框中选择 **msdyn\_CreateOperationSetV1Response OperationSetId**。

## <a name="references"></a>引用

- [如何将流与 Dataverse 集成概述 - Power Automate](/power-automate/dataverse/overview?WT.mc_id=email)
- [使用项目计划 API 对计划实体执行操作](schedule-api-preview.md)
- [云端流概述 - Power Automate](/power-automate/overview-cloud?WT.mc_id=email)
- [解决方案识别流概述 - Power Automate](/power-automate/overview-solution-flows?WT.mc_id=email)
