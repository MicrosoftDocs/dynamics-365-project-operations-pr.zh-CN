---
title: 日程安排助理概述
description: 此主题提供有关使用日程安排助理预订资源的信息。
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: da551e805f395e466952df1dbb7d193bdddba358
ms.sourcegitcommit: 56c42d7f5995a674426a1c2a81bae897dceb391c
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/01/2020
ms.locfileid: "3907914"
---
# <a name="schedule-assistant-overview"></a>日程安排助理概述

_**适用于：** 基于资源/非库存场景的 Project Operations，精简部署 - 估价开票交易_

日程安排助理用于根据项目经理定义的要求来预订资源。 日程安排助理依赖资源要求中提供的参数来查找资源。 日程安排助理建议符合相关要求的资源，如时间窗口或所需的技能。

在确定合适的资源后，资源经理或项目经理可以将资源预订到工作中。

## <a name="prerequisites"></a>先决条件

日程安排助理是 Universal Resource Scheduling 解决方案的一部分。 此解决方案通过 Dynamics 365 Project Operations、Dynamics 365 Field Service 和 Dynamics 365 Customer Service 提供和安装。

## <a name="matching-requirements-and-resources"></a>匹配要求与资源

生成的资源要求基于如下详细信息：

-   特征
-   角色
-   业务部门
-   资源首选项
-   工作量信息
-   时区

日程安排助理使用这些详细信息来筛选资源。

## <a name="launch-the-schedule-assistant"></a>启动日程安排助理

启动日程安排助理有两种方式。 如果您使用的是混合模式，可以在团队成员网格中选择资源要求未满足的任何团队成员，然后选择**预订**。 如果您使用的是集中模式，资源经理会查找并选择资源。

## <a name="schedule-assistant-filters"></a>日程安排助理筛选器

在日程安排助理运行后，资源要求的详细信息将在左侧窗格中显示为筛选值。 资源经理或项目经理可以通过调整筛选器来调整结果以满足计划需求。

筛选器窗格显示与工作相关的选项，其中包括：

-   工作开始和结束
-   特征
-   角色
-   部门
-   资源供给公司
-   资源类型
-   首选资源
