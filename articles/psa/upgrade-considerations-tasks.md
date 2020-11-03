---
title: 工作分解结构的升级注意事项
description: 此主题介绍如何将工作分解结构从 Project Service Automation 2.x 升级到 3.x。
manager: kfend
ms.service: dynamics-365-customerservice
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
ms.openlocfilehash: 169dc24f0d1ae151ea5927123fb738221de88250
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/16/2020
ms.locfileid: "4072686"
---
# <a name="upgrade-considerations-for-the-work-breakdown-structure"></a>工作分解结构的升级注意事项
此主题介绍如何将工作分解结构从 Project Service Automation 2.x 升级到 3.x。 此主题定义 Project Service Automation (PSA) 中要成功升级需要的项目健康状态。 以及有关将导致升级失败的一般阻碍情况的信息。 有关在项目计划内定义项目任务及其职能的详细信息，请参阅[项目计划](project-creating.md)。

## <a name="key-entities"></a>关键实体
对于已经使用资源加载的准确工作分解结构，需要以下实体：

- [项目](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_project)
- [项目团队](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projectteam)
- [项目任务](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projecttask)
- [资源分派](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_resourceassignment)
- [项目任务依赖关系](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projecttaskdependency)
- [可预订资源](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/bookableresource)

若要定义已加载资源的工作分解结构，必须完成以下步骤：

1. 创建新项目。 有关如何创建新项目的详细信息，请参阅 [msdyn_project](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_project)。
2. 创建一个或多个任务。 有关如何创建任务的详细信息，请参阅 [msdyn_projecttask](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projecttask)。
3. 定义任务依赖项。 有关详细信息，请参阅[项目任务依赖关系](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projecttaskdependency)。
4. 为项目分派项目团队成员。 有关详细信息，请参阅 [msdyn_projectteam](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projectteam)。
5. 为任务分派项目团队成员。 有关详细信息，请参阅 [msdyn_resourceassignment](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_resourceassignment)。

## <a name="project-team-relationships"></a>项目团队关系

若要确保升级成功，必须正确维护以下关系：
- 所有项目团队成员必须与一项可预订资源关联。
- 所有项目团队成员必须与同一个项目关联。 

## <a name="project-task-relationships"></a>项目任务关系
若要确保升级成功，必须正确维护以下关系：

- 所有相关任务必须与同一个项目关联。
- 每个明细任务必须有一个父任务。
- 每个任务必须有一个父项目。

### <a name="valid-conditions"></a>有效条件

- 所有任务持续时间必须大于或等于 (>=) 一个小时，并小于 1,800,000 分钟（1,250 天）。*
- 所有任务的开始日期不得早于 2000/01/01。*
- 所有任务的开始日期不得晚于当天后的 17 年。*
- 所有任务的开始日期必须早于或等于其完成日期。
- 分类（支出、材料、税和时间）的所有交易类型必须有 **默认计价单位** 和 **计价单位组** 值。
- 应该避免日期格式带字母。

### <a name="potential-mitigation-steps"></a>可能的缓解步骤
- 使用“高级查找”可确定不包含项目 ID 的项目任务。
- 使用“高级查找”可确定计划持续时间大于 1,800,000 的项目任务。
- 在进行任何数据更改之前，您应调查与实体相关联的任何自定义项，它们可能会导致数据进入错误状态。 这些自定义项问题应该首先解决，然后才能继续进行与数据相关的任何更新。
- 对于所标识的孤立任务，如果不需要它们，或者如果应该将它们与正确的父项目相关联，请考虑删除这些任务。
- 对于持续时间超过 1,250 天的任何任务，请考虑添加多个任务以表示总持续时间（如果可行）。

> [!NOTE]
> 带有星号 (\*) 标记的项之所以有限制，是因为客户关系管理 (CRM) 仅支持 7,320 个重复扩展。 必须低于此限制。

## <a name="resource-assignment-relationships"></a>资源分派关系
若要确保升级成功，必须正确维护以下关系：

- 必须将同一个工作分解结构中的所有资源分派与同一个项目关联。
- 必须将同一个工作分解结构中的所有资源分派与同一个项目中的项目团队成员关联。

### <a name="potential-mitigation-steps"></a>可能的缓解步骤
- 确定属于上述情况之外的所有任务。  
- 应删除任何不再有效的资源分派。

## <a name="project-task-dependency-relationships"></a>项目任务依赖项关系
若要确保升级成功，必须正确维护以下关系：

- 所有项目任务依赖项必须与同一个项目关联。
- 一个任务不能多次引用同一个依赖项。
