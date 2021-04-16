---
title: 为任务分派资源
description: 此主题介绍如何为任务分派资源。
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 9/27/2019
ms.topic: article
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
ms.openlocfilehash: 486371df2de8b400f200dbf38e66cb5e2dec7ae7
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/15/2021
ms.locfileid: "5286237"
---
# <a name="assign-a-resource-to-a-task"></a>为任务分配资源

[!include [banner](../includes/psa-now-project-operations.md)]

在 Microsoft Dynamics 365 Project Service Automation 中可通过三种方法为任务分派资源。

## <a name="book-a-resource-as-a-team-member-and-then-assign-the-resource-to-a-task"></a>作为团队成员预订资源，然后将资源分派给任务。

您可以将资源添加到项目团队，然后在项目计划中将资源分派给任务。

1. 在 **团队成员** 选项卡中，通过选中 **新建** 添加新团队成员。 

2. 将打开 **团队成员快速创建** 面板，在这里您可以选择可预订资源名称并设置角色。 

    为资源的预订选择以下分配方法之一：

    - **完全产能** 为指定的起始日期和截止日期预订资源的完全产能。
    - **产能百分比** 为指定的起始日期和截止日期预订资源产能的百分比。
    - **按时数平均分配** 预订资源指定的小时数，根据指定的起始日期/截止日期按天平均分配时间。
    - **按时数前期负荷** 预订资源指定的小时数，根据指定的起始日期和截止日期前期负荷每天的时间。
    - **无** 将资源添加到团队，但不创建任何分配其产能的预订。

3. 在任务的 **日程安排** 网格上，选择资源单元格中的 **资源** 图标，然后在 **团队成员** 下选择您刚才添加的团队成员。 

> [!NOTE]
> 在 **团队成员** 选项卡和 **协调** 选项卡上，资源均显示已预订工时数和已分派工时数。 这些工时数应该相同，但不必一定如此，因为预订和分派不是紧密结合的。 **协调** 选项卡为您提供它们不同时的详细信息，例如，当您向资源分派的工时数多于已预订工时数时。 如果需要，您可以通过扩展资源的预订或更改分派来更正信息。

## <a name="create-a-generic-team-member-through-task-assignment"></a>通过任务分派创建通用团队成员

通过任务分派创建通用团队成员时，创建描述指定资源（您最终希望处理任务的资源）的特征的占位符或通用资源。 然后，您生成一个用于搜索和预订指定资源的要求（或使用此要求提交请求）。

1. 在任务的 **日程安排** 网格上，选择资源单元格中的 **资源** 图标。

2. 键入名称用作占位符资源的名称。 例如，“项目经理”。

3. 选择 **创建**，然后 **快速创建项目团队成员** 字段中，为通用资源设置角色。

4. 您可以通过在任务的 **资源选择器** 上选择资源来继续将任务分派给此占位符资源。 它们在 **团队成员** 下列出。

5. 在分派通用资源后，在 **团队** 选项卡上选择通用资源，然后选择 **生成要求** 为该通用资源创建资源要求。

6. 为通用资源选择 **预订**。 然后，您可以使用日程安排板查找和预订实际资源。 您还可以提交由资源经理满足的要求。

7. 在通用资源要求由指定资源满足时，通用资源将被从团队中移除，通用资源的任务分派将被分派到满足通用资源的资源要求的指定资源。

## <a name="assign-a-named-resource-from-the-list-of-all-bookable-resources"></a>从所有可预订资源列表分派指定资源

您可以在 **资源选择器** 中使用搜索框来搜索所有可预订资源，然后将其分派给任务。

将把按照这种方法分派的资源添加到无任何预订的团队。 这类似添加团队成员并选择“无”作为分配方法。 资源在 **团队** 和 **协调** 选项卡中显示为资源，仅分派和预订不足。 如果您要使用其可用性，请预订这些资源。

1. 在任务的 **日程安排** 网格上，选择资源单元格中的 **资源** 图标。

2. 开始键入名称。 名称的搜索结果显示在 **资源选择器** 中 **其他资源** 下。

3. 选择要分派给任务的资源。



[!INCLUDE[footer-include](../includes/footer-banner.md)]