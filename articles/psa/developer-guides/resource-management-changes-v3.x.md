---
title: 资源管理更改 (Project Service Automation 3.x)
description: 此主题介绍对资源管理区域的更改。
author: makk
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 03/18/2019
ms.topic: article
ms.service: business-applications
ms.author: makk
audience: admin
search.audienceType:
- admin
- customizer
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: 5f88d7309a5e1171629a72e749bfc01abb64c62a
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/15/2021
ms.locfileid: "5284752"
---
# <a name="resource-management-changes-project-service-automation-3x"></a>资源管理更改 (Project Service Automation 3.x)

[!include [banner](../../includes/psa-now-project-operations.md)]

此主题介绍已经对 Dynamics 365 Project Service Automation 版本 3.x 的“资源管理”区域进行的更改。

## <a name="project-estimates"></a>项目估算

项目估算基于 **msdyn\_resourceassignment** 实体（**资源分派**），而不是基于 **msdyn\_projecttask** 实体（**项目任务**）。 资源分派已成为任务计划和定价的“事实来源”。

## <a name="line-tasks"></a>明细任务

在 PSA 3.x 中，明细任务已过时（已弃用）。 分派现在指向整个任务，而不是明细任务。

以下示例显示在 PSA 早期版本中和 PSA 3.x 中如何为团队成员 A 和 B 分派名称为“测试任务”的任务。

- **PSA 3.x 之前版本：**

    - 测试任务

        - 测试任务 – 明细任务 1

            - A 的分派

        - 测试任务 – 明细任务 2

            - B 的分派

- **PSA 3.x：**

    - 测试任务

        - A 的分派
        - B 的分派

## <a name="unassigned-assignment"></a>未分派的分派

在 PSA 3.x 中，未分派的分派是分派给 **空** 团队成员和 **空** 资源的分派。 下面的两种方案中可能出现未分派的分派：

- 如果已创建任务，但是尚未将其分派给任何团队成员，则始终创建未分派的分派。 
- 如果删除了任务的所有被分派人，则为该任务重新创建未分派的分派。

## <a name="scheduling-fields-on-the-project-task-entity"></a>项目任务实体中的计划字段

**msdyn\_projecttask** 实体中的字段已弃用或移到 **msdyn\_resourceassignment** 实体，或者现在从 **msdyn\_projectteam** 实体（**项目团队成员**）引用。

| msdyn\_projecttask（项目任务）中已弃用的字段 | msdyn\_resourceassignment（资源分派）中的新字段 | 注释 |
|---|---|---|
| msdyn\_assignedresources | 无 | |
| msdyn\_assignedteammembers | 无 | |
| msdyn\_numberofresources | 无 | |
| msdyn\_scheduledhours | 无 | |
| msdyn\_effortcontour | msdyn\_plannedwork | 已更改了字段中存储的 JavaScript 对象表示法 (JSON) 数据结构格式。 |

## <a name="schedule-contour"></a>计划分布

计划分布存储在每个 **资源分派** 实体 (**msdyn\_resourceassignment**) 的 **计划的工作** 字段 (**msdyn\_plannedwork**) 中。

### <a name="structure"></a>结构

新的计划分布结构由为计划的每一天定义的灵活时间片段构成。 每个时间片段具有以下属性：

- **开始** – 根据项目日历，工作日的开始工作时间。
- **结束** – 根据项目日历，工作日的结束工作时间。
- **工时** – 为当天分派的工时数量。

**示例**

在此示例使用的项目日历中，工作日为 UTC-8 时区上午 9 点到下午 5 点。

```json
[{"End":"\/Date(1543885200000)\/","Start":"\/Date(1543856400000)\/","Hours":8},{"End":"\/Date(1543971600000)\/","Start":"\/Date(1543942800000)\/","Hours":8},{"End":"\/Date(1544058000000)\/","Start":"\/Date(1544029200000)\/","Hours":2}]
```

### <a name="auto-scheduling-and-manual-scheduling"></a>自动计划和手动计划

如果任务是自动计划的，则工时是前载型，可能会缩短任务持续时间。

**示例**

以下任务自动计划为三天内 18 个工时（2018 年 12 月 3 日到 2018 年 12 月 5 日）。

```json
[{"End":"\/Date(1543885200000)\/","Start":"\/Date(1543856400000)\/","Hours":8},{"End":"\/Date(1543971600000)\/","Start":"\/Date(1543942800000)\/","Hours":8},{"End":"\/Date(1544058000000)\/","Start":"\/Date(1544029200000)\/","Hours":2}]
```

如果任务是手动计划的，则将工时平均分配给所有日期。

**示例**

以下任务手动计划为三天内 18 个工时（2018 年 12 月 3 日到 2018 年 12 月 5 日）。

```json
[{"End":"\/Date(1543885200000)\/","Start":"\/Date(1543856400000)\/","Hours":6},{"End":"\/Date(1543971600000)\/","Start":"\/Date(1543942800000)\/","Hours":6},{"End":"\/Date(1544058000000)\/","Start":"\/Date(1544029200000)\/","Hours":6}]
```

### <a name="assignment-unit"></a>分派单位

PSA 3.x 中已弃用分派单位。 现在按天为所有分派的资源平均分配任务工作量小时数。

**示例**

在此示例中，任务分派给两项资源，并自动计划为三天内 36 个工时（2018 年 12 月 3 日到 2018 年 12 月 5 日）

- 分派 1：

    ```json
    [{"End":"\/Date(1543885200000)\/","Start":"\/Date(1543856400000)\/","Hours":8},{"End":"\/Date(1543971600000)\/","Start":"\/Date(1543942800000)\/","Hours":8},{"End":"\/Date(1544058000000)\/","Start":"\/Date(1544029200000)\/","Hours":2}]
    ```

- 分派 2：

    ```json
    [{"End":"\/Date(1543885200000)\/","Start":"\/Date(1543856400000)\/","Hours":8},{"End":"\/Date(1543971600000)\/","Start":"\/Date(1543942800000)\/","Hours":8},{"End":"\/Date(1544058000000)\/","Start":"\/Date(1544029200000)\/","Hours":2}]
    ```

## <a name="pricing-dimensions"></a>定价维度

在 PSA 3.x 中，已从 **msdyn\_projecttask** 实体删除了资源特定的定价维度字段（如 **角色** 和 **部门**）。 现在可以在生成项目估算时，从资源分派 (**msdyn\_resourceassignment**) 的相应项目团队成员 (**msdyn\_projectteam**) 检索这些字段。 已经为 **msdyn\_projectteam** 实体新增了字段 **msdyn\_organizationalunit**。

| msdyn\_projecttask（项目任务）中已弃用的字段 | 改用了来自 msdyn\_projectteam（项目团队成员）的字段 |
|---|---|
| msdyn\_resourcecategory | msdyn\_resourcecategory |
| msdyn\_organizationalunit | msdyn\_organizationalunit |

## <a name="contours"></a>分布

**msdyn\_projecttask** 实体中已弃用了定价和估算分布字段。 已将其移到 **msdyn\_resourceassignment** 实体。

| msdyn\_projecttask（项目任务）中已弃用的字段 | msdyn\_resourceassignment（资源分派）中的新字段 |
|---|---|
| msdyn\_costestimatecontour | msdyn\_plannedcostcontour |
| msdyn\_salesestimatecontour | msdyn\_plannedsalescontour |

已为 **msdyn\_resourceassignment** 实体增加了以下字段：

* msdyn\_plannedcost
* msdyn\_plannedsales

**msdyn\_projecttask** 实体中计划的成本、实际成本和剩余成本的以下字段未变：

* msdyn\_plannedcost
* msdyn\_plannedsales
* msdyn\_actualcost
* msdyn\_actualsales
* msdyn\_remainingcost
* msdyn\_remainingsales


[!INCLUDE[footer-include](../../includes/footer-banner.md)]