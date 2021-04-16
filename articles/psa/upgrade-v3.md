---
title: 升级注意事项 - 从 Microsoft Dynamics 365 Project Service Automation 版本 2.x 或 1.x 升级到版本 3
description: 此主题介绍从 Project Service Automation 版本 2.x 或 1.x 升级到版本 3 时必须考虑的注意事项。
manager: kfend
ms.prod: ''
ms.service: project-operations
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
ms.openlocfilehash: ff0777705c6d0e2c0d8aa4ed191f4ae6b1786100
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/15/2021
ms.locfileid: "5281647"
---
# <a name="upgrade-considerations---psa-version-2x-or-1x-to-version-3"></a>升级注意事项 - PSA 版本 2.x 或 1.x 到版本 3.x

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

## <a name="project-service-automation-and-field-service"></a>Project Service Automation 和 Field Service
Dynamics 365 Project Service Automation 和 Dynamics 365 Field Service 都使用 Universal Resourcing Scheduling (URS) 解决方案计划资源。 如果您的实例中有 Project Service Automation 和 Field Service，请将两个解决方案都升级到最新版本。 对于 Project Service Automation，是版本 3.x。 对于 Field Service，是版本 8.x。 升级 Project Service Automation 或 Field Service 将安装最新版本的 URS。 如果同一实例中的 Project Service Automation 和 Field Service 解决方案都未升级到最新版本，则可能会有不一致的行为。

## <a name="resource-assignments"></a>资源分派
在 Project Service Automation 版本 2 和版本 1 中，任务分派作为子任务（也称为明细任务）存储在 **任务实体** 中，并直接与 **资源分派** 实体关联。 明细任务在工作分解结构 (WBS) 中的任务分派弹出窗口中显示。

![Project Service Automation 版本 2 和版本 1 中 WBS 上的明细任务](media/upgrade-line-task-01.png)

在 Project Service Automation 版本 3 中，已更改了将可预订资源分派给任务时采用的基础架构。 明细任务已弃用，**任务实体** 中的任务与 **资源分派** 视图中的团队成员之间存在直接的 1:1 关系。 分派给项目团队成员的任务现在直接存储在资源分派实体中。  

这些更改影响项目团队中具有指定可预订资源和通用资源的资源分派的所有现有项目的升级。 此主题提供升级到版本 3 时需要对项目注意的事项。 

### <a name="tasks-assigned-to-named-resources"></a>任务分派给指定资源
如果使用基础任务实体，则版本 2 和版本 1 中的任务允许团队成员扮演非默认为其定义的角色。 例如，为康辉默认分派的角色为项目经理，但可以将她分派给需要开发人员角色的任务。 在版本 3 中，指定团队成员的角色始终为默认角色，所以为康辉分派的所有角色都使用她的默认角色，即项目经理。

如果已经在版本 2 和版本 1 中将资源分派给了需要非其默认角色的任务，在您升级时，将为该指定资源分派所有任务分派的默认角色，无论版本 2 中的角色分派是怎样的。 此分配会导致计算出的估算在版本 2 或版本 1 与版本 3 之间存在差异，因为计算估算时基于资源的角色，而不是基于明细任务分派。 例如，在版本 2 中，为候婵分派了两个任务。 任务 1 的明细任务的角色为开发人员，任务 2 的角色为项目经理。 候婵的默认角色为项目经理。

![为一项资源分派了多个角色](media/upgrade-multiple-roles-02.png)

因为开发人员角色和项目经理角色不同，所以成本和销售额估算计算方法如下：

![资源角色的成本估算](media/upggrade-cost-estimates-03.png)

![资源角色的销售额估算](media/upgrade-sales-estimates-04.png)

升级到版本 3 时，明细任务替换为可预订资源团队成员的任务资源分派。 此分派使用可预订资源的默认角色。 下图中，资源是角色为项目经理的候婵。

![资源分派](media/resource-assignment-v2-05.png)

因为估算基于资源的默认角色，所以销售额和成本估算可能改变。 下图中不再能看到 **开发人员** 角色，因为该角色现在取自可预订资源的默认角色。

![默认角色的成本估算](media/resource-assignment-cost-estimate-06.png)
![默认数据的销售额估算](media/resource-assignment-sales-estimate-07.png)

升级完成后，可以将团队成员的角色编辑为非默认分派的角色。 但是，如果更改某个团队成员角色，为其分配的所有任务的角色也会改变，因为版本 3 中无法为团队成员分配多个角色。

![更新资源角色](media/resource-role-assignment-08.png)

将资源的部门从默认部门更改为另一个部门时，这一条对分派给指定资源的明细任务也成立。 版本 3 升级完成后，分派将使用资源的默认部门，而不是明细任务中设置的部门。

### <a name="tasks-assigned-to-generic-resources"></a>任务分派给通用资源
在版本 2 和版本 1 中，可以为任务设置角色和部门，然后使用 **生成团队** 功能基于为任务设置的属性生成通用资源。 在版本 3 中，将创建具有角色和部门的通用团队成员，然后将团队分派给任务。

在版本 2 和版本 1 中，采用通用资源的项目可以为两种状态，或者两种状态均在任务级别。 例如，可以采用以下方案：

- 设置具有角色和部门的任务，但是未生成附属资源分派。
- 具有使用 **生成团队** 功能通过创建通用资源分派的通用团队成员资源分派的任务。

开始升级之前，建议您为满足以下条件的每个项目重新生成团队：将任务分配给了通用资源，或必须运行生成团队流程。

对于分派给使用 **生成团队** 生成的通用团队成员的任务，升级将保留团队的通用资源，并且保留该通用团队成员的分派。 建议仅在升级后，但预订或提交资源请求之前为通用团队成员生成资源要求。 这将保留通用团队成员的所有与项目合同签订部门不同的部门分派。

例如，在 Project Z 项目中，合同签订部门为 Contoso 美国。 在项目计划中，已经为实施阶段的测试任务分派了技术顾问角色，而分派的部门则为 Contoso 印度。

![实施阶段部门分派](media/org-unit-assignment-09.png)

实施阶段后，为技术顾问角色分派了集成测试任务，但是部门设置为 Contoso 美国。  

![集成测试任务部门分派](media/org-unit-generate-team-10.png)

为项目生成团队时，由于任务的部门不同，所以将创建两个通用团队成员。 将为技术顾问 1 分派 Contoso 印度任务，为技术顾问 2 分派 Contoso 美国任务。  

![生成的通用团队成员](media/org-unit-assignments-multiple-resources-11.png)

> [!NOTE]
> 在 Project Service Automation 版本 2 和版本 1 中，团队成员不存储部门，部门在明细任务中维护。

![Project Service Automation 中的版本 2 和版本 1 明细任务](media/line-tasks-12.png)

可以在估算视图中查看部门。 

![部门估算](media/org-unit-estimates-view-13.png)
 
升级完成后时，将把与通用团队成员对应的明细任务中的部门添加到通用团队成员，并删除明细任务。 因此，建议您在升级前为包含通用资源的每个项目生成团队。

对于分派给部门与合同签订项目部门不同的角色，并且尚未生成团队的任务，升级将为该角色创建一个通用团队成员，但是对该团队成员的部门使用项目的合同签订部门。 请回去参考 Project Z 的示例，已经为合同签订部门 Contoso 美国和实施阶段内的项目计划测试任务分配了技术顾问角色，并且采用了分配给 Contoso 印度的部门。 已经为实施阶段后完成的集成测试任务分派了技术顾问角色。 部门为 Contoso 美国，未生成团队。 升级将创建一个通用团队成员（这是分派有所有三个任务的工时的技术顾问），以及部门 Contoso 美国（这是项目的合同签订部门）。   
 
更改不生成的团队成员中不同资源部门的默认设置是我们之所以建议您在升级之前为包含通用资源的每个项目生成或重新生成团队，以便不丢失部门分配的原因。



[!INCLUDE[footer-include](../includes/footer-banner.md)]