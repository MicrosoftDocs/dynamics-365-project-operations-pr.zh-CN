---
title: Project Service Automation 到 Project Operations 的功能变化
description: 本文概述了 Microsoft Dynamics 365 Project Service Automation 到 Dynamics 365 Project Operations 的功能变化。
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 02/03/2022
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
ms.reviewer: johnmichalak
ms.openlocfilehash: 9869b3ad0fb6429484a26f367e06a0996f110ed8
ms.sourcegitcommit: a2d720ac6d7ddb20a0967fe87992a376b2478208
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/04/2022
ms.locfileid: "9621206"
---
# <a name="feature-changes-for-project-service-automation-to-project-operations"></a>Project Service Automation 到 Project Operations 的功能变化

项目成功从 Microsoft Dynamics 365 Project Service Automation 3.X 升级到 Dynamics 365 Project Operations Lite 后，无法在任务网格工作分解结构 (WBS) 中编辑项目任务。 客户可以查看跟踪网格中的 WBS，其中添加了新字段，以提供与任务相关的所有详细信息。 对于需要对 WBS 进行编辑的项目，您可以有选择地将符合条件的项目转换为新的 Project for the web 计划体验。

## <a name="project-conversion-process"></a>项目转换过程

要转换项目，请执行以下步骤。

1. 打开项目的主页，然后在操作窗格上选择 **转换**。
1. 在确认消息框中，选择 **确定** 开始项目转换。 将出现以下操作：

    1. 出现在项目主页上的消息栏将显示“项目计划正在转换。 在转换完成之前，您无法对项目进行更改。”
    1. 您将被重定向到项目列表。

    项目转换完成后，将执行以下操作：

    1. 分配的项目经理将在应用程序右侧收到通知。
    1. 显示转换正在进行的消息栏将被删除。
    1. **计划** 选项卡将显示 Project for the web 的新计划体验。 任何具有适当许可证和安全角色的用户都可以编辑 WBS。
    1. **计划引擎** 字段将更新为 **Project for the web**。
    1. **转换** 按钮将被从操作窗格中删除。

> [!IMPORTANT]
> 不允许批量转换项目。 任何同时更新大量项目的尝试都将受限。 此限制有助于确保所有客户都有高性能。

## <a name="manual-tasks-vs-automatic-tasks"></a>手动任务与自动任务

当环境从 Project Service Automation 升级到 Project Operations 时，WBS 中的所有任务都将被视为自动计划。 手动计划任务的概念在 Project for The web 中不可用。 但是，您可以在创建新项目时使用[计划模式](/project-management/scheduling-modes.md)设置来定义项目的首选计划行为。

## <a name="restricted-operations-for-pre-conversion-projects"></a>预转换项目的限制操作

本节概述项目未转换时可以预期的功能差异。

### <a name="copy-project"></a>复制项目

仅转换后的项目支持 **复制** 操作。 转换之前无法复制已升级的项目。

### <a name="move-project"></a>移动项目

除非项目已经转换，否则对项目开始日期的更改不会按比例改变任务的开始。

## <a name="frequently-asked-questions"></a>常见问题解答

### <a name="what-are-the-differences-between-converted-projects-and-new-projects-that-are-created-after-the-upgrade-has-been-completed"></a>升级完成后创建的转换项目和新项目之间有什么区别？

对于在环境升级后转换的项目，将设置一个标志，指示计划仅使用项目日历。 此行为与 Project Service Automation 中的行为匹配。 但是，不会为升级后创建的新项目设置标志。 因此，当资源被分配给任务时，计划将使用资源的工作时间。

### <a name="what-should-i-do-if-my-project-fails-to-be-converted"></a>如果我的项目转换失败，我该怎么办？

如果您的项目转换失败，第一步是查看错误日志，确定是否有与 WBS 相关的任何常见问题。 如果日志没有显示您可以采取操作的具体错误，请联系客户支持，以便进一步审查您的案例。

### <a name="how-are-business-closures-handled-in-project-for-the-web"></a>Project for the web 中是如何处理节假日的？

Project for the web 不使用企业在组织级别定义的节假日。 但是，它使用在给定工作时间模板中定义的其他类型的休息日。

### <a name="what-are-the-limitations-of-project-for-the-web"></a>Project for the web 有哪些限制？

请参阅[创建工作分解结构：项目限制](/project-management/create-wbs#project-limitations.md)。

### <a name="can-i-expect-changes-to-my-cost-and-sales-estimates"></a>我的成本和销售估计值会发生变化吗？

在重新计算资源分配信息或者资源分配的日期边界与源项目不同这些很少见的情况下，您可能会看到销售和成本估计值的差异。 作为升级过程的一部分，客户需要测试一组具有代表性的示例项目，以便他们能够了解任何潜在的计划更改。
