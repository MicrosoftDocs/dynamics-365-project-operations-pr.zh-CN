---
title: 查看建议资源
description: 此主题介绍如何建议任务资源。
author: ruhercul
ms.date: 11/05/2020
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: ruhercul
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 987ea08c77c1824182856c0d52ee0cd15e7029b9
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/10/2021
ms.locfileid: "6000740"
---
# <a name="review-proposed-resources"></a>查看建议资源

_**适用于：** 基于资源/非库存场景的 Project Operations，精简部署 - 估价开票交易_

资源经理可使用资源请求为项目经理建议资源。

1. 从请求网格或请求本身选择 **查找资源**。
2. 在 **日程安排助理** 页中，选择资源，然后在 **创建资源预订** 窗格的 **预订状态** 字段中，选择 **预订**。

将进行以下状态更新：

- 在 **日程安排助理** 页中，将更新状态指示器，以便指示预订是建议的，而不是硬预订的。
- 在资源请求中，状态更改为 **需要审阅**。
- 在项目的 **团队** 选项卡上，通用团队成员的 **请求状态** 值更改为 **需要审阅**。

项目经理可接受或拒绝建议。

当资源经理处理资源请求时，可以使用下面的任何方法：

- 如果一项资源不能满足所需工时，建议多项资源以满足需求。 然后在可满足所需工时的多项资源之间拆分建议的工时。 在此方案中，工时不能重合。
- 建议比所需资源更少的资源。 在此方案中，建议的资源产能比请求者指定所需工时少。 因此，当请求者接受建议的资源时，将创建未满足资源要求以捕获剩余需求。
- 如果没有哪一项资源可以单独完成工作，则预订多项资源以满足需求。
- 预订比所需资源更少的资源。 在此方案中，预订的工时比所需工时少。 系统将引导您建议资源，而不是建议预订，这样请求者就可以验证和跟踪剩余需求。

## <a name="resource-availability"></a>资源可用性

资源经理是可查看资源的可用性和更新预订至关重要。 在某些情况下，不存在正式需求（资源请求），但是资源经理必须响应来自渠道（如电子邮件、电话联络或即时消息）的意外需求。 资源经理可使用日程安排板更新资源和预订。

资源工作时间是计算资源可用性的基础。 资源预订会占用资源的产能。

日程安排板使用颜色和阴影显示预订、可用性、超额预订和预订状态。 可使用日程安排板设置中的一项设置来显示图例。

如果日程安排板中单项可预订资源旁边显示向右箭头，说明可以展开该资源以显示为预订该资源的工作的详细信息。

因为 Dynamics 365 Project Operations 使用 Universal Resource Scheduling 引擎，所以如果也安装了 Dynamics 365 Field Service，则可查看项目、工作订单和您已将计划扩展到的其他任何实体的资源预订。

若要查看单项资源的更多详细信息，请右键单击该资源打开资源卡。



[!INCLUDE[footer-include](../includes/footer-banner.md)]