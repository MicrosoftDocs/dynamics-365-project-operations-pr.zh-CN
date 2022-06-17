---
title: 关键概念
description: 本文介绍 Project Service Automation 中的关键资源管理概念。
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
ms.reviewer: johnmichalak
ms.openlocfilehash: 41b13000ca17ec3a5d86fdb17885f09692d6f0c0
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8921705"
---
# <a name="key-concepts"></a>关键概念

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

下表定义 Dynamics 365 Project Service Automation 应用程序中使用的关键概念。

| 概念                    | 定义 |
|----------------------------|------------|
| 项目团队成员        | 在项目团队中，一个项目团队成员可以是拥有预订的指定资源，没有预订的指定资源，或通用资源。 通用资源没有预订，位于项目本地，并且在项目中没有产能约束。 |
| 项目通用资源   | 资源占位符，用于在不必知道指定资源的情况下组建团队和为项目安排人员。 项目日历用作通用资源的日历。 可将通用资源添加到项目团队并分派给任务。 |
| 预订的工时数               | 资源工时数是为项目硬预订来帮助确保完成项目工作。 预订的工时数占用资源的总产能。 预订仅针对指定资源，不针对通用资源。 |
| 分派的工时数             | 资源工时数分派给项目计划中的任务。 分派可以针对指定资源或通用资源。 分派可以独立于预订。 |
| 所需工时数             | 需要，但是尚未由指定资源实施的产能。 所需工时数仅与已生成了资源要求的通用团队成员有关。 |
| 需求                     | 当前和近期工作负荷。 在 Project Service Automation 中，需求显示为资源要求或资源请求。 |
| 资源要求       | 一种实体，用于捕获所需资源的所需工时数、开始和结束日期、技能、地域和其他定价维度。 资源要求从项目团队成员生成或单独创建。 |
| 资源请求           | 一种实体，用作“信封”来传递资源经理必须满足的资源要求。 |
| 资源默认角色      | 为计算利用率将资源归入的角色。 假设资源拥有角色所需技能和满足该角色的目标利用率。 |
| 资源部门 | 将资源分派给的部门。 |
| 分布                    | 按天分解的任务、要求或分派工时数。 例如，可以将一个为期五天的 40 小时任务分布在五天，每天八小时。 |
| 协调视图        | 一个视图，其中显示每个项目团队成员的预订和分派。 项目经理可使用此视图查找预订与分派之间的不匹配，并在出现了任何不匹配时采取纠正措施。 |
| 工作时间                 | 一种实体，用于识别资源产能、工作时间和非工作时间。 此实体也称为资源日历。 |


[!INCLUDE[footer-include](../includes/footer-banner.md)]
