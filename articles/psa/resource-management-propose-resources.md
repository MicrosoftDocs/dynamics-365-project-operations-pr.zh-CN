---
title: 建议项目资源
description: 此主题介绍如何推荐项目资源。
author: ruhercul
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
ms.openlocfilehash: 9fe63f424735f22dc6b525631287e7ff36db17f37aad8e14e926f5cc9be39136
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/06/2021
ms.locfileid: "6995030"
---
# <a name="propose-project-resources"></a>建议项目资源

[!include [banner](../includes/psa-now-project-operations.md)]

资源经理可使用资源请求为项目经理建议资源。

1. 从请求网格或请求本身选择 **查找资源**。
2. 在 **日程安排助理** 页中，选择资源，然后在 **创建资源预订** 窗格的 **预订状态** 字段中，选择 **预订**。

    ![已选择建议的资源。](media/Resource-Management-image62.png)

将进行以下状态更新：

- 在 **日程安排助理** 页中，将更新状态指示器，以便指示预订是建议的，而不是硬预订的。

    ![“日程安排助理”页中建议的预订的状态指示器。](media/Resource-Management-image63.png)

- 在资源请求中，状态更改为 **需要审阅**。

    ![资源请求状态已更改为“需要审阅”。](media/Resource-Management-image64.png)

- 在项目的 **团队** 选项卡上，通用团队成员的 **请求状态** 值更改为 **需要审阅**。

    ![“团队”选项卡上通用团队成员的请求状态更改为“需要审阅”。](media/Resource-Management-image48.png)

项目经理可接受或拒绝建议。

当资源经理处理资源请求时，可以使用下面的任何方法：

- 如果一项资源不能满足所需工时，建议多项资源以满足需求。 然后在可满足所需工时的多项资源之间拆分建议的工时。 在此方案中，工时不能重合。
- 建议比所需资源更少的资源。 在此方案中，建议的资源产能比请求者指定所需工时少。 因此，当请求者接受建议的资源时，将创建未满足资源要求以捕获剩余需求。
- 如果没有哪一项资源可以单独完成工作，则预订多项资源以满足需求。
- 预订比所需资源更少的资源。 在此方案中，预订的工时比所需工时少。 系统将引导您建议资源，而不是建议预订，这样请求者就可以验证和跟踪剩余需求。

## <a name="billable-utilization"></a>可记帐利用率

资源可以有目标可记帐利用率。 此目标利用率定义为资源默认角色的一个属性，或在单个可预订资源的记录中设置。 利用率的计算可基于使用批准的时间条目报告的实际工时。

以下公式用于计算利用率：

- 可记帐利用率 = 可记帐实际工时数 ÷ 资源产能
- 不可记帐利用率 = 带有记帐类型的 ID 实际时间= 不应计费、补充或不可用 ÷ 资源产能
- 内部 = 无销售合同的实际时间 ÷ 资源产能
- 资源产能 = 资源工作时间 – 外出 – 非工作日

可以在 **资源** 窗格中找到 **资源利用率** 视图。

![资源利用率视图。](media/Resource-Management-image65.png)

此网格中的每个单元格代表一段时间（如天、周或月）的资源可记帐利用率百分比。 以下公式用于为单元格设置颜色：

- **绿色：** 可记帐利用率 \>= 资源目标利用率
- **黄色：** 目标利用率 – 20 \<= 可记帐利用率 \< 目标利用率
- **红色：** 可记帐利用率 \< 目标利用率 – 20

因为 **资源利用率** 视图基于日程安排板，所以可使用日程安排板的功能筛选结果。

此网格要求对角色或单个资源设置目标利用率。 若要进行此设置，转到 **资源** \> **资源角色**。

此外，还必须为每项可预订资源分派默认角色。 转到 **资源**\>**资源**。 在 **Project Service** 选项卡上，验证是否定义了资源角色，以及角色的 **为默认** 字段是否设置为 **是**。 可以添加更多 **为默认 = 否** 的角色。 **为默认 = 是** 的角色用于评估针对该角色的目标的资源利用率。

![默认角色集。](media/Resource-Management-image67.png)

在 **Project Service** 选项卡上，也可以为资源设置单个目标利用率。 然后，利用率的计算使用该目标利用率评估资源的目标，而不是资源默认角色的目标。

仅当资源批准了网格中显示的期间内的应计费时间时才显示该资源的利用率。

## <a name="resource-availability"></a>资源可用性

资源经理是可查看资源的可用性和更新预订至关重要。 在某些情况下，不存在正式需求（资源请求），但是资源经理必须响应来自渠道（如电子邮件、电话联络或即时消息）的意外需求。 资源经理可使用日程安排板更新资源和预订。

资源工作时间是计算资源可用性的基础。 资源预订会占用资源的产能。

![日程安排板。](media/Resource-Management-image68.png)

日程安排板使用颜色和阴影显示预订、可用性、超额预订和预订状态。 可使用日程安排板设置中的一项设置来显示图例。

如果日程安排板中单项可预订资源旁边显示向右箭头，说明可以展开该资源以显示为预订该资源的工作的详细信息。

![日程安排板中已展开可预订资源。](media/Resource-Management-image69.png)

因为 Dynamics 365 Project Service Automation 使用 Universal Resource Scheduling 引擎，所以如果也安装了 Dynamics 365 Field Service，则可查看项目、工作订单和您已将计划扩展到的其他任何实体的资源预订。

![项目和工作订单的资源预订详细信息。](media/Resource-Management-image70.png)

若要查看单项资源的更多详细信息，请右键单击该资源打开资源卡。

![资源卡。](media/Resource-Management-image71.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]