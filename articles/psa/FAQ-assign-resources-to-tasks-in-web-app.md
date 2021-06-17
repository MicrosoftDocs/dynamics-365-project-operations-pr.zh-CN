---
title: 如何在 Web 应用程序中将可预订资源分派给任务
description: 可预订资源分派方法的概述。
author: JohnPBurrows
ms.custom:
- dyn365-projectservice
ms.date: 8/21/2018
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 32a04ddef901515cd77262b5ae6be2458cb6b00c
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/10/2021
ms.locfileid: "5993277"
---
# <a name="how-do-i-assign-a-bookable-resource-to-a-task-in-the-web-app-project-service-app-v2x"></a>如何在 Web 应用程序（Project Service 应用程序 v2.x）中将可预订资源分派到任务？

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1.x-2.x](../includes/cc-applies-to-psa-app-1x-2x.md)]

在 Project Service 中可通过两种方法将资源分派到任务。 您可以作为团队成员预订资源，然后将它分派到任务。 或者，可以通过任务的角色分派创建通用团队成员，生成团队，然后通过指定资源满足备份要求。

请注意，如果您要将可预订资源分派到任务，可预订资源团队成员必须有足够的可用预订。 预订的状态必须为“提交类型硬性预订”和“已提交状态”。 如果资源没有足够的预订，Project Service 将删除分派并显示以下错误消息：

*无法将资源分派到任务 - 以下资源没有为项目预订的足够时间*

## <a name="book-a-resource-as-a-team-member-and-then-assign-the-resource-to-a-task"></a>作为团队成员预订资源，然后将资源分派到任务。

使用该方法，您将资源添加到项目团队，然后在项目计划中将任务分派给资源。 以下是如何操作：
1.  在团队成员网格中，通过选中 **新建** 添加新团队成员。
2.  在“团队成员快速创建”屏幕上，选择可预订资源名称并设置角色。
3.  选择 **起始** 和 **截止** 日期。

    > [!div class="mx-imgBorder"] 
    > ![添加团队成员的屏幕截图](media/FAQ-Resources-to-Tasks2-1.png "添加团队成员的屏幕截图")
 
4.  选择以下分配方法之一预订资源：
    - **完全产能** 为指定的起始日期和截止日期预订资源的完全产能。
    - **产能百分比** 为指定的起始日期和截止日期预订资源产能的百分比。
    - **按时数平均分配** 预订资源指定的小时数，根据指定的起始日期和截止日期按天平均分配时间。
    - **按时数前期负荷** 预订资源指定的小时数，根据指定的起始日期和截止日期前期负荷每天的时间。

    请勿选择 **无**，因为这会将资源添加到团队，但不创建任何分配资源产能的预订。
5.  选择 **保存**。

    请注意，预订小时数必须足够覆盖您向其分派此资源的任务的工作时间和日期范围。 如果它们不一致，则无法将资源分派到任务。

6.  在任务的工作分解结构 (WBS) 上，单击资源单元格下拉列表。 然后： 

    1. 选择 **添加**。
    2. 选择 **资源** 下的下拉列表，并选择您上面添加的团队成员。
    3. 选择 **确定**。 团队成员现在分派到了任务。

    > [!div class="mx-imgBorder"] 
    > ![使用 WBS 添加资源的屏幕截图](media/FAQ-Resources-to-Tasks2-2.png "使用 WBS 添加资源的屏幕截图")
 
在团队成员网格上，您将在“分派的时数”下看到资源的已分派时数的总和。 它将小于或等于资源的预订时数。 

> [!div class="mx-imgBorder"] 
> ![资源的已分派时数的屏幕截图](media/FAQ-Resources-to-Tasks2-3.png "资源的已分派时数的屏幕截图")
 
如果您尝试分派到资源的任务在资源预订的结束日期之后开始，此资源将不会显示在下拉列表中。

请注意，如果资源有一些剩余的未分派产能，那么您可以将资源分派给多于其已预订时数的时数。 在这种情况下，资源仅部分分派到其预订。 您可以通过将“未分派时数”列添加到工作分解结构来查看这些剩余的未分派任务时数。

如果资源被分派给他们预订的时数（其已预订时数等于其已分派时数），在您尝试向他们分派其他任务时，您将看到以下错误消息：

*无法将资源分派到任务 - 以下资源没有为项目预订的足够时间。*

此外，在您创建项目时添加到团队的默认项目经理团队成员也将被添加且无任何预订，并且无法被分派到任何任务。 它们不会显示在任务的资源下拉列表中。

如果要分派此资源，您需要从团队中将其删除，然后使用“无”以外的分配方法重新添加它们。 在创建项目时将它们添加到团队的原因是为了项目在默认情况下至少有一个项目审批者。

## <a name="create-a-generic-team-member-through-role-assignment-on-tasks"></a>通过任务上的角色分派创建通用团队成员

此方法将确保资源有足够的任务的预订。 首先，在将角色分派到任务后生成团队，通过此方式创建描述指定资源（您最终希望处理任务的资源）的特征的占位符或通用资源。 以下是如何操作：

1. 在工作分解结构上，选择一项任务。
2. 在资源单元格中选择 **已分派角色** 下拉列表图标。
3. 选择 **角色** 下拉列表并选择通用资源的角色。
4. 选择 **确定**。

    > [!div class="mx-imgBorder"] 
    > ![使用 WBS 添加资源的屏幕截图](media/FAQ-Resources-to-Tasks2-4.png "使用 WBS 添加资源的屏幕截图")
 
在 WBS 中将角色分派到任务后，选择 **生成项目团队**。 Project Service 根据角色、资源部门和项目日历通过聚合任务分派来创建最低数量的通用团队成员。

> [!div class="mx-imgBorder"] 
> ![生成项目团队的屏幕截图](media/FAQ-Resources-to-Tasks2-5.png "生成项目团队的屏幕截图")
 
在团队成员网格中，您将会看到具有此角色和职位名称的通用资源类型的资源。 如果角色需要两个资源来完成工作，“生成团队”功能将创建两个团队成员，并使用职位名称来区分它们。

> [!div class="mx-imgBorder"] 
> ![添加两个通用资源的屏幕截图](media/FAQ-Resources-to-Tasks2-6.png "添加两个通用资源的屏幕截图")
 
您可以通过选择“资源要求”下的链接来打开通用团队成员的支持资源要求。

> [!div class="mx-imgBorder"] 
> ![打开支持资源要求的屏幕截图](media/FAQ-Resources-to-Tasks2-7.png "打开支持资源要求的屏幕截图")

为通用资源选择 **预订**，然后您可以使用日程安排板查找和预订实际资源。 您还可以通过选择 **提交请求** 来提交由资源经理满足的要求。

在通用资源要求由指定资源满足时，通用资源将被从团队中移除，通用资源的任务分派将被分派到满足通用资源的资源要求的指定资源。
 



[!INCLUDE[footer-include](../includes/footer-banner.md)]