---
title: 使用“复制项目”开发项目模板
description: 此主题提供有关如何使用“复制项目”自定义操作创建项目模板的信息。
author: stsporen
ms.date: 01/21/2021
ms.topic: article
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: d12301b4e7baabeb0f045f9a11d4695fc026339af3fa7650db7177c495c71e90
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/06/2021
ms.locfileid: "6989231"
---
# <a name="develop-project-templates-with-copy-project"></a>使用“复制项目”开发项目模板

_**适用于：** 基于资源/非库存场景的 Project Operations，精简部署 - 估价开票交易_

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Dynamics 365 Project Operations 支持复制项目并将所有工作重新分配给代表该角色的一般资源的功能。 客户可以使用此功能来构建基本项目模板。

选择 **复制项目** 时，目标项目的状态将更新。 使用 **状态描述** 可以确定复制操作完成的时间。 如果未在目标项目实体中检测到目标日期，选择 **复制项目** 还会将项目的开始日期更新为当前的开始日期。

## <a name="copy-project-custom-action"></a>“复制项目”自定义操作 

### <a name="name"></a>客户 

**msdyn_CopyProjectV2**

### <a name="input-parameters"></a>输入参数
有三个输入参数：

| 参数          | Type   | 值                                                   | 
|--------------------|--------|----------------------------------------------------------|
| ProjectCopyOption  | String | **{"removeNamedResources":true}** or **{"clearTeamsAndAssignments":true}** |
| SourceProject      | 实体引用 | 源项目 |
| 目标             | 实体引用 | 目标项目 |


- **{"clearTeamsAndAssignments":true}**：Web 版本的 Project 的默认行为，将删除所有工作和团队成员。
- **{"removeNamedResources":true}** Project Operations 的默认行为，将工作还原为通用资源。

有关操作的更多默认行为，请参阅[使用 Web API 操作](/powerapps/developer/common-data-service/webapi/use-web-api-actions)

## <a name="specify-fields-to-copy"></a>指定要复制的字段 
当调用操作时，**复制项目** 将查看项目视图 **复制项目列**，以确定在复制项目时要复制哪些字段。


### <a name="example"></a>示例
以下示例显示了如何使用 **removeNamedResources** 参数集调用 **CopyProject** 自定义操作。
```C#
{
    using System;
    using System.Runtime.Serialization;
    using Microsoft.Xrm.Sdk;
    using Newtonsoft.Json;

    [DataContract]
    public class ProjectCopyOption
    {
        /// <summary>
        /// Clear teams and assignments.
        /// </summary>
        [DataMember(Name = "clearTeamsAndAssignments")]
        public bool ClearTeamsAndAssignments { get; set; }

        /// <summary>
        /// Replace named resource with generic resource.
        /// </summary>
        [DataMember(Name = "removeNamedResources")]
        public bool ReplaceNamedResources { get; set; }
    }

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
            targetProject["msdyn_subject"] = "Example Project";
            targetProject.Id = organizationService.Create(targetProject);

            ProjectCopyOption copyOption = new ProjectCopyOption();
            copyOption.ReplaceNamedResources = true;

            CallCopyProjectAPI(sourceProject.ToEntityReference(), targetProject.ToEntityReference(), copyOption);
            Console.WriteLine("Done ...");
        }

        private void CallCopyProjectAPI(EntityReference sourceProject, EntityReference TargetProject, ProjectCopyOption projectCopyOption)
        {
            OrganizationRequest req = new OrganizationRequest("msdyn_CopyProjectV2");
            req["SourceProject"] = sourceProject;
            req["Target"] = TargetProject;
            req["ProjectCopyOption"] = JsonConvert.SerializeObject(projectCopyOption);
            OrganizationResponse response = organizationService.Execute(req);
        }
    }
}
```


[!INCLUDE[footer-include](../includes/footer-banner.md)]