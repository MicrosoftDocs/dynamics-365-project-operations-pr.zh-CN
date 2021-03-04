---
title: 为项目团队预订指定的可预订资源和分派任务
description: 本主题介绍如何为项目团队预订指定资源和将其分派给任务。
author: JohnPBurrows
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 11/28/2018
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
ms.openlocfilehash: d8a49b6ae8423cb99c710e40704475b4a71d3724
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/10/2021
ms.locfileid: "5145347"
---
# <a name="book-named-bookable-resources-to-a-project-team-and-assign-tasks"></a>为项目团队预订指定的可预订资源和分派任务 

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

可向项目添加指定资源，方法是直接为团队预订这些资源。 为此，请完成以下步骤：

1. 在 Project Service Automation 中，转到 **项目**，然后选择并打开要为其预订的项目。
2. 在 **项目** 页的 **团队** 选项卡上，单击 **新建**。 

![从“团队”选项卡添加团队成员](media/RM-how-to-1.png)

3. 在 **快速创建项目团队成员** 对话框中，选择可预订资源。 如果为资源分派了默认角色，将使用该角色填充 **角色** 字段。 可以根据需要更改此角色。 
4. 选择将需要资源的开始日期和结束日期，然后选择资源产能的分配方法。 
5. 如果希望该团队成员担任项目审批者，请在 **项目审批者** 字段中选择 **是**。 这意味着该团队成员可以审批为此项目提交的时间和支出条目。 
6. 单击 **保存**。

![在快速创建窗体中添加团队成员](media/RM-how-to-2.png)


可以将预订的资源分派给项目中的任务。 在 **项目** 页中，单击 **计划** 选项卡将任务分派给新资源。 从任务网格中的 **资源** 字段启动的资源选取器将显示可选团队成员。

![在计划选项卡上为任务分派团队成员](media/RM-how-to-3.png)

在 Project Service Automation (PSA) 版本 3 中，资源预订与任务分派之间的关系不紧密。 这意味着当您在计划中使用资源选取器时，可以为团队成员分派比其在项目中的工时更多的任务工时。
可以在 **团队** 选项卡或 **资源协调** 选项卡中查看团队成员预订与分派之间的差异。也可以在更详细的级别协调资源的预订与分派之间的差异。

![“资源协调”选项卡](media/RM-how-to-4.png)

也可以使用 **计划** 选项卡上的资源选取器搜索和选择尚不属于项目团队的可预订资源。 这些在资源选取器中显示为 **其他资源**。

![为任务分派非团队成员资源](media/RM-how-to-5.png)

执行此操作时，将把资源添加到项目团队，并分派给任务，而不会生成任何预订。

![有分派，但无预订的团队成员](media/RM-how-to-6.png)

可使用 **协调** 选项卡的扩展预订功能或 **日程安排板** 为项目预订资源产能。

![在资源协调选项卡上扩展团队成员的预订](media/RM-how-to-7.png)

为项目预订团队成员之后，您可以使用维护预订或直接使用日程安排板来管理其预订。


[!INCLUDE[footer-include](../includes/footer-banner.md)]