---
title: 软预订要求
description: 本主题提供有关如何软预订要求的信息。
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 03/28/2019
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
ms.openlocfilehash: e753dd2f5635d1e9d0d6a02ea5d1d537879dd3a5
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/28/2020
ms.locfileid: "4124087"
---
# <a name="soft-book-requirements"></a>软预订要求

资源要求可以是硬预订的。 硬预订会创建占用资源产能的建议。 然后会将该建议发回给请求者进行审批。 软预订将资源暂时添加到项目团队，并且在日程安排板中具有不同状态，但是不会占用该资源的产能。 若要从日程安排板软预订资源，请将 **预订状态** 字段设置为 **软性**。

![预订状态设置为“软性”](media/Resource-Management-image77.png)

当 **团队** 选项卡位于 **指定的团队成员** 视图中时，将在此处显示该资源。 将在 **软预订工时数** 列中显示软预订的工时数。

![“指定的团队成员”视图中的“软预订工时数”](media/Resource-Management-image78.png)

软预订的团队成员可以分派给任务。

![软预订的团队成员已分派给任务](media/Resource-Management-image79.png)

在 **协调** 选项卡上，不显示软预订资源的预订，因为 **协调** 选项卡仅考虑硬预订。

![“协调”选项卡上无预订的软预订资源](media/Resource-Management-image80.png)

> [!NOTE]
> 不能从基于通用团队成员生成的要求软预订资源。

在日程安排板中，将为资源的软预订使用其他颜色。

![日程安排板中的软预订](media/Resource-Management-image81.png)

若要将软预订转换为硬预订，请在日程安排板中右键单击软预订，然后选择 **更改状态** \> **硬预订** \> **硬性**。

![将预订状态更改为“硬性”](media/Resource-Management-image82.png)

将更改预订，并且更改日程安排板中的状态。 因为预订状态现在为 **硬性**，所以资源显示为已预订，并且已调整了其产能和可用性。

可使用相同的方法从日程安排板取消硬预订或软预订。

若要在项目的 **团队** 选项卡上将软预订资源转换为硬预订，请选择该资源，然后选择 **确认**。

![确认命令](media/Resource-Management-image83.png)
