---
title: 为任务和项目团队分派通用可预订资源
description: 本文提供有关为任务和项目团队预订通用资源的信息。
author: JohnPBurrows
ms.custom:
- dyn365-projectservice
ms.date: 12/11/2018
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
ms.openlocfilehash: 9f67ab7381747e5d780f8b0024dd98ae8420d05f
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8923545"
---
# <a name="assign-generic-bookable-resources-to-a-task-and-generate-resource-requirements"></a>为任务分派通用可预订资源和生成资源要求 

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

除了为项目预订和分派指定资源或实际资源，还可以为项目任务分派通用资源。 在您准备好使用指定资源为项目安排人员之前，这些资源可充当指定资源的替身。 

1. 在 Project Service Automation (PSA) 中，打开 **项目** 页面，然后在 **计划** 选项卡上计划的 **资源** 单元格中，输入通用资源的位置名称。 或单击单元格中的 **资源** 图标打开资源选取器，然后输入要创建的通用资源的名称。

![创建和分派通用团队成员。](media/RM-how-to-9.png)

这将打开 **快速创建: 项目团队成员** 面板。 

2. 输入通用资源团队成员的角色和部门，然后单击 **保存**。

![快速创建通用团队成员。](media/RM-how-to-10.png)

3. 创建新的通用资源团队成员之后，将把其分派给任务。 您可以继续把该通用资源分派给任务计划中的其他任务。

![将现有通用团队成员分派给任务。](media/RM-how-to-11.png)

4. 分派通用资源之后，可以通过直接预订或向资源经理提交资源请求来生成资源要求并满足。

![为通用团队成员生成要求。](media/RM-how-to-12.png)

在团队成员网格中，除了可以按照上面的介绍使用资源选取器，还可以直接生成通用资源。 将添加资源和基于 **快速创建: 项目团队成员** 面板中指定的开始/结束日期和分配方法的资源要求。

如果您直接添加通用团队成员，然后向通用资源添加比它们要求工时内所需更多的任务，可能会发现差异。 请单击 **生成要求** 再次生成要求以平衡所需工时与分派。

还可以单击团队网格中的 **资源要求** 链接打开要求并添加技能、首选资源等。

![资源要求。](media/RM-how-to-13.png)



[!INCLUDE[footer-include](../includes/footer-banner.md)]
