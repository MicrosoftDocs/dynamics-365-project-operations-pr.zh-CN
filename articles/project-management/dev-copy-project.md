---
title: 使用“复制项目”开发项目模板
description: 本文提供有关如何使用“复制项目”自定义操作创建项目模板的信息。
author: stsporen
ms.date: 03/10/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: 47c1023bbc4c21e3571bffbf3670bf0f7854f81d
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8923821"
---
# <a name="develop-project-templates-with-copy-project"></a>使用“复制项目”开发项目模板

_**适用于：** 基于资源/非库存场景的 Project Operations，精简部署 - 估价开票交易_

Dynamics 365 Project Operations 支持复制项目并将所有工作重新分配给代表该角色的一般资源的功能。 客户可以使用此功能来构建基本项目模板。

选择 **复制项目** 时，目标项目的状态将更新。 使用 **状态描述** 可以确定复制操作完成的时间。 如果未在目标项目实体中检测到目标日期，选择 **复制项目** 还会将项目的开始日期更新为当前的开始日期。

## <a name="copy-project-custom-action"></a>“复制项目”自定义操作

### <a name="name"></a>Name 

msdyn\_CopyProjectV3

### <a name="input-parameters"></a>输入参数

有三个输入参数：

- **ReplaceNamedResources** 或 **ClearTeamsAndAssignments** – 仅设置其中一个选项。 不要同时设置。

    - **\{"ReplaceNamedResources":true\}** – Project Operations 的默认行为。 任何指定资源都将替换为通用资源。
    - **\{"ClearTeamsAndAssignments":true\}** – Project for the Web 的默认行为。 所有分配和团队成员都将被删除。

- **SourceProject** – 要从中复制的源项目的实体引用。 此参数不能为 null。
- **Target** – 要复制到的目标项目的实体引用。 此参数不能为 null。

下表提供了三个参数的摘要。

| 参数                | 类型​​             | 价值                 |
|--------------------------|------------------|-----------------------|
| ReplaceNamedResources    | 布尔型          | **True** 或 **False** |
| ClearTeamsAndAssignments | 布尔型          | **True** 或 **False** |
| SourceProject            | 实体引用 | 源项目    |
| Target                   | 实体引用 | 目标项目    |

有关操作的更多默认行为，请参阅[使用 Web API 操作](/powerapps/developer/common-data-service/webapi/use-web-api-actions)。

### <a name="validations"></a>验证

已完成以下验证。

1. Null 检查并检索源项目和目标项目，以确认组织中这两个项目是否存在。
2. 系统通过验证以下条件来验证目标项目是否可以复制：

    - 项目上没有以前的活动（包括选择 **任务** 选项卡），项目是新创建的。
    - 项目没有以前的副本，没有请求导入，并且项目没有 **失败** 状态。

3. 操作不使用 HTTP 调用。

## <a name="specify-fields-to-copy"></a>指定要复制的字段

当调用操作时，**复制项目** 将查看项目视图 **复制项目列**，以确定在复制项目时要复制哪些字段。

### <a name="example"></a>示例

以下示例显示如何使用 **removeNamedResources** 参数集调用 **CopyProjectV3** 自定义操作。

```C#
{
    using System;
    using System.Runtime.Serialization;
    using Microsoft.Xrm.Sdk;
    using Newtonsoft.Json;

    public class CopyProjectSample
    {
        private IOrganizationService organizationService;

        public CopyProjectSample(IOrganizationService organizationService)
        {
            this.organizationService = organizationService;
        }

        public void SampleRun()
        {
            // Example source project GUID
            Guid sourceProjectId = new Guid("11111111-1111-1111-1111-111111111111");
            var sourceProject = new Entity("msdyn_project", sourceProjectId);

            Entity targetProject = new Entity("msdyn_project");
            targetProject["msdyn_subject"] = "Example Project - Copy";
            targetProject.Id = organizationService.Create(targetProject);

            CallCopyProjectAPI(sourceProject.ToEntityReference(), targetProject.ToEntityReference(), copyOption, true, false);
            Console.WriteLine("Done ...");
        }

        private void CallCopyProjectAPI(EntityReference sourceProject, EntityReference TargetProject, bool replaceNamedResources = true, bool clearTeamsAndAssignments = false)
        {
            OrganizationRequest req = new OrganizationRequest("msdyn_CopyProjectV3");
            req["SourceProject"] = sourceProject;
            req["Target"] = TargetProject;

            if (replaceNamedResources)
            {
                req["ReplaceNamedResources"] = true;
            }
            else
            {
                req["ClearTeamsAndAssignments"] = true;
            }

            OrganizationResponse response = organizationService.Execute(req);
        }
    }
}
```

[!INCLUDE[footer-include](../includes/footer-banner.md)]
