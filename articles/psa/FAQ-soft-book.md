---
title: 软预订资源
description: 此主题介绍如何暂时计划或软预订项目团队成员。
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 9/25/2019
ms.topic: article
ms.author: ruhercul
audience: Admin
search.app:
- ProjectOperations
ms.openlocfilehash: 1d2044692d1c6d694a1365be76dd8e7ddafd376d
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/15/2021
ms.locfileid: "5285967"
---
# <a name="soft-book-a-resource"></a>软预订资源

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

您可以暂时计划或将资源“软预订”到项目团队来显示您将资源分派到项目的计划。 软预订不使用资源的可用产能，您可以将软预订的团队成员分派到项目任务。 但是，由于软预订不使用资源的产能，您仍可以在同一期间内为其他任务“硬预订”该资源。 通用资源无法软预订，软预订也不能满足对通用资源的请求。

软预订的项目团队成员在 **项目** 页的 **团队** 选项卡上列出，其软预订工时显示在 **指定团队成员** 视图的 **软预订时数** 列中。 软预订的团队成员同时在日程安排板上列出。 因为它们都属于软预订，日程安排板不显示这些资源的任何产能的使用。 软预订的时间不显示在 **协调** 选项卡上，也不显示在日程安排板 **协调** 选项卡的 **扩展预订** 字段中。 

可通过两种方法为项目软预订团队成员：直接从日程安排板，或通过在 **团队** 选项卡上添加团队成员。 

## <a name="soft-book-from-the-schedule-board"></a>从日程安排板进行软预订
完成以下步骤从日程安排板软预订资源。 

1. 打开日程安排板，然后在 **预订要求** 面板中选择 **项目** 选项卡。
2. 找到要为其软预订资源的项目。 如果列表中有大量项目，请选择 **项目** 列标题，然后使用筛选器搜索一个或多个项目。
3. 搜索项目，然后将其拖放到资源的时间网格中。
5. 在 **创建资源预订** 面板中，调整开始日期和结束日期，将 **预订状态** 设置为 **软性**，然后设置工时。 
6. 单击 **预订**。 此资源现在作为项目的资源显示在 **团队** 选项卡上。 在 **指定团队成员** 视图中，您将在 **软预订工时数** 列中看到软预订的工时数。

> [!NOTE]
> 您现在可以在 **日程安排** 选项卡上将软预订的资源分派到任务。在 **协调** 选项卡上，该资源将显示相对于其任务分派缺少的预订，因为 **协调** 选项卡只考虑硬预订。 您可以使用 **扩展预订** 功能来硬预订资源以根据资源分派消除硬预订缺少情况。 您必须使用 **维护预订** 手动取消资源的软预订。

## <a name="soft-book-on-the-team-tab"></a>“团队”选项卡上的软预订

您可以直接在 **团队** 选项卡上添加团队成员，然后使用 **维护预订** 将其预订状态从 **硬** 更改为 **软**。 在通过此方式添加团队成员时，将始终进行硬预订，除非您选择 **无** 作为分配方法。

若要使用此方法，请完成以下步骤。

1. 在 **项目** 页的 **团队** 选项卡上，单击 **新建**。
2. 选择可预订资源、角色、起始日期和截止日期。
3. 选择 **无** 以外的分配方法：
4. 选择 **保存**。 您将会在网格上看到资源，其时数显示在 **硬预订时数** 列中。
5. 通过选择 **维护预订** 维护资源的预订。
6. 在日程安排板打开时，展开资源以显示其预订。 您将看到预订显示为 **硬**。
7. 右键单击预订，在 **更改状态** 下，选择 **软预订** \> **软**。 预订状态现在为 **软**。
8. 在关闭日程安排板后，当查看 **指定团队成员** 视图时，您将看到资源的时数已从 **团队** 选项卡网格的 **硬预订时数** 列移至 **软预订时数**。

> [!NOTE]
> 在使用 **维护预订** 将状态从 **硬** 更改为 **软** 时，如果您将资源硬预订给团队，然后为该资源分派任务，将保留该资源的任务分派。 但是，在 **协调** 选项卡上，资源将缺少预订，因为在协调预订与分派时将仅考虑硬预订。 您可以使用 **协调** 选项卡上的 **扩展预订** 功能来硬预订资源以根据资源分派消除硬预订缺少情况。 您必须使用 **维护预订** 取消资源的软预订。

在您准备好可以将软预订的团队成员资源更改为硬预订的团队成员时，请执行以下操作：

1. 在日程安排板上，展开资源以显示其预订。 您会看到显示为 **软** 的预订。
2. 右键单击预订，在 **更改状态** 下，选择 **硬预订** \> **硬**。 预订状态现在为 **硬**。
3. 在关闭日程安排板、返回项目，然后打开 **团队** 选项卡后，当进入 **指定团队成员** 视图时，您将看到资源的时数已从 **团队** 选项卡的 **软预订时数** 列移至 **硬预订时数** 列。 如果资源被分派到任务，他们将不再显示 **协调** 选项卡上缺少的预订，因为其预订现在是硬预订。



[!INCLUDE[footer-include](../includes/footer-banner.md)]