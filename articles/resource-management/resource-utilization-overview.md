---
title: 资源利用率概述
description: 此主题介绍 Project Operations 中的资源利用率。
author: ruhercul
manager: Annbe
ms.date: 11/05/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 4d66b5fc642ef53adf1169ce891a7a5fa26b07d6
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/15/2021
ms.locfileid: "5279307"
---
# <a name="resource-utilization-overview"></a>资源利用率概述

_**适用于：** 基于资源/非库存场景的 Project Operations，精简部署 - 估价开票交易_

资源可以有目标可记帐利用率。 此目标利用率定义为资源默认角色的一个属性，或在单个可预订资源的记录中设置。 利用率的计算可基于使用批准的时间条目报告的实际工时。

以下公式用于计算利用率：

  - 可记帐利用率 = 可记帐实际工时数 ÷ 资源产能
  - 不可记帐利用率 = 带有记帐类型的 ID 实际时间= 不应计费、补充或不可用 ÷ 资源产能
  - 内部 = 无销售合同的实际时间 ÷ 资源产能
  - 资源产能 = 资源工作时间 – 外出 – 非工作日

可以在 **资源** 窗格中找到 **资源利用率** 视图。

此网格中的每个单元格代表一段时间（如天、周或月）的资源可记帐利用率百分比。 以下公式用于为单元格设置颜色：

  - **绿色**：可计费利用率 >= 资源目标利用率
  - **黄色**：目标利用率 – 20 <= 可计费利用率 < 目标利用率
  - **红色**：可计费利用率 < 目标利用率 – 20

因为 **资源利用率** 视图基于日程安排板，所以可使用日程安排板的功能筛选结果。

此网格要求对角色或单个资源设置目标利用率。 若要进行此设置，转到 **资源** > **资源角色**。

此外，还必须为每项可预订资源分派默认角色。 转到 **资源** > **资源**。 在 **Project Service** 选项卡上，验证是否定义了资源角色，以及 **为默认** 字段是否设置为 **是**。 可以添加更多 **为默认** = **否** 的角色。 **为默认** = **是** 的角色用于评估针对该角色的目标的资源利用率。

在 **Project Service** 选项卡上，也可以为资源设置单个目标利用率。 然后，利用率的计算使用该目标利用率评估资源的目标，而不是资源默认角色的目标。

仅当资源批准了网格中显示的期间内的应计费时间时才显示资源的利用率。


[!INCLUDE[footer-include](../includes/footer-banner.md)]