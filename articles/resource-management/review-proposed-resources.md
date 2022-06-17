---
title: 查看建议资源
description: 本文介绍如何建议任务资源。
author: ruhercul
ms.date: 08/18/2021
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: ruhercul
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 3f20dda2b7b384608b8f4b548c18ac21d07fee07
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8924833"
---
# <a name="review-proposed-resources"></a>查看建议资源

_**适用于：** 基于资源/非库存场景的 Project Operations，精简部署 - 估价开票交易_

资源经理可使用资源请求为项目经理建议资源。

若要查看建议的资源，请执行以下步骤：

1. 从 **请求** 网格或请求本身选择 **查找资源**。
2. 在 **日程安排助理** 页面中，选择资源，然后确认建议的预订中包含建议的所有工时。
3. 在 **创建资源预订** 窗格中，将 **预订状态** 字段设置为 **已拟定**，然后选择 **预订**。

    > [!NOTE]
    > 将 **预订状态** 设置为 **已拟定** 不会硬预订资源，也不会将通用资源替换为指定的团队成员。

    将进行以下状态更新：

    - 在 **日程安排助理** 页中，将更新状态指示器，以便指示预订是建议的，而不是硬预订的。
    - 在资源请求中，状态更改为 **需要审阅**。
    - 在项目的 **团队** 选项卡上，通用团队成员的 **请求状态** 值更改为 **需要审阅**。

项目经理可接受或拒绝建议。

当资源经理处理资源请求时，可以使用下面的任何方法：

- 如果一项资源不能满足所需工时，建议多项资源以满足需求。 然后在可满足所需工时的多项资源之间拆分建议的工时。 在此方案中，工时不能重合。
- 建议比所需资源更少的资源。 在此方案中，建议的资源产能比请求者指定所需工时少。 当请求者接受建议的资源时，将创建未满足资源要求以捕获剩余需求。
- 如果没有哪一项资源可以单独完成工作，则预订多项资源以满足需求。
- 预订比所需资源更少的资源。 在此方案中，预订的工时比所需工时少。 系统将引导您建议资源，而不是建议预订，这样请求者就可以验证和跟踪剩余需求。

## <a name="resource-availability"></a>资源可用性

资源经理必须可以查看资源的可用性和更新预订。 在某些情况下，不存在正式需求（资源请求）。 但是资源经理必须响应来自其他渠道（如电子邮件、电话联络或即时消息）的意外需求。 资源经理可使用 **日程安排板** 更新资源和预订。

资源工作时间是计算资源可用性的基础。 资源预订会占用资源的产能。

**日程安排板** 使用颜色和阴影显示预订、可用性、超额预订和预订状态。 **日程安排板** 中的设可用于显示图例。

如果 **日程安排板** 中单项可预订资源旁边显示向右箭头，说明可以展开该资源以显示为预订该资源的工作的详细信息。

因为 Dynamics 365 Project Operations 使用 Universal Resource Scheduling 引擎，所以如果也安装了 Dynamics 365 Field Service，则可查看项目、工作订单和您已将计划扩展到的其他任何实体的资源预订。

若要查看单项资源的更多详细信息，请右键单击该资源打开资源卡。



[!INCLUDE[footer-include](../includes/footer-banner.md)]
