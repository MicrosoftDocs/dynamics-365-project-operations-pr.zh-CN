---
title: 满足通用资源要求
description: 此主题介绍如何为通用资源要求预订指定资源。
author: ruhercul
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: fef896ae12c196d5566ad54f3e15373020e4e28a
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/15/2021
ms.locfileid: "5279577"
---
# <a name="generic-resource-requirement-fulfillment"></a>满足通用资源要求

_**适用于：** 基于资源/非库存场景的 Project Operations，精简部署 - 估价开票交易_

可以预订指定资源以替换具有资源要求的通用资源。

1. 在 **项目** 页上，选择 **团队** 选项卡。
2. 从列表中选择具有资源要求的通用资源，然后选择 **预订**。 或者，打开资源要求，然后选择 **预订**。
3. 在 **日程安排助理** 页中，选择要为项目团队预订的指定资源，然后选择 **预订**。

预订完成并由指定资源满足时，将把通用资源替换为指定资源。

也将使用该指定资源更新计划的分派。

## <a name="fulfill-a-generic-resource-with-multiple-named-resources"></a>使用多项指定资源替代通用资源
使用多项指定资源满足通用资源的要求类似分派一项指定资源。 例如，有一个持续时间为 5 天，工作量为 120 个小时的任务。 此任务不能由一个每周工作五天，每天通常工作八小时的资源完成。 

此要求适用于五天工作 120 小时的机器人，即每天工作 24 小时。

这个示例是需要多项指定资源来满足一项通用资源请求。 您需要订阅多项资源以满足此要求。

此方案的主要区别是，分派给任务的团队中仍然保留通用资源，并且此位置中不分派预订的指定资源团队成员。 项目经理可以根据需要将工作分派给指定资源。 **协调** 视图可帮助项目经理将多项资源的预订分解为任务分派。 不会自动执行此操作，因为在比上面的简单示例更复杂的方案中（如您有大量任务构成要求或项目经理希望如何分配的意图）需要系统假设。 因为系统无法理解意图，所以假设可能与意图不同，并且可能会出现错误结果或不可预料的结果。 可预测结果是项目经理在 **协调** 视图的协助下特意创建资源之前，一直使用分派的通用资源。




[!INCLUDE[footer-include](../includes/footer-banner.md)]