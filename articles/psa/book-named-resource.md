---
title: 根据资源要求预订指定资源
description: 此部分介绍如何为通用资源要求预订指定资源。
author: JohnPBurrows
manager: kfend
ms.service: project-operations
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
ms.openlocfilehash: d7ff58ec08661adc702867c6c26805a74a3637c9
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/28/2020
ms.locfileid: "4125887"
---
# <a name="book-named-resources-from-resource-requirements"></a>根据资源要求预订指定资源

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

可以预订指定资源以替换具有资源要求的通用资源。

1. 在 Project Service Automation (PSA) 中的 **项目** 页中，单击 **团队** 选项卡。
2. 从列表中选择具有资源要求的通用资源，然后单击 **预订**。 或者，打开资源要求，然后单击 **预订**。


![预订通用团队成员](media/RM-how-to-14.png)


3. 在 **日程安排助理** 页中，选择要为项目团队预订的指定资源，然后单击 **预订**。

![使用日程安排助理预订通用团队成员](media/RM-how-to-15.png)

预订完成并由指定资源满足时，将把通用资源替换为指定资源。

![指定团队成员替换通用团队成员](media/RM-how-to-16.png)

也将使用该指定资源更新计划的分派。

![分派给项目任务的指定团队成员](media/RM-how-to-17.png)

## <a name="fulfill-a-generic-resource-with-multiple-named-resources"></a>使用多项指定资源替代通用资源
使用多项指定资源满足通用资源的要求类似分派一项指定资源。 例如，有一个持续时间为 5 天，工作量为 120 个小时的任务。 此任务不能由一个每周工作五天，每天通常工作八小时的资源完成。 

![一个需要为期五天的 120 小时工作量的任务](media/RM-how-to-21.png)

此要求适用于五天工作 120 小时的机器人，即每天工作 24 小时。

![按天要求](media/RM-how-to-22.png)

这个示例是需要多项指定资源来满足一项通用资源请求。 您需要订阅多项资源以满足此要求。

![订阅多项资源以满足要求](media/RM-how-to-23.png)

此方案的主要区别是，分派给任务的团队中仍然保留通用资源，并且此位置中不分派预订的指定资源团队成员。 项目经理可以根据需要将工作分派给指定资源。 **协调** 视图可帮助项目经理将多项资源的预订分解为任务分派。 不会自动执行此操作，因为比上面的简单示例更复杂的方案中（如您有大量任务构成要求），需要系统假设项目经理的分派方法意图。 因为系统无法理解意图，所以假设可能与意图不同，并且可能会发生错误结果或不可预料的结果。 可预测结果是项目经理在 **协调** 视图的协助下特意创建资源之前，一直使用分派的通用资源。


