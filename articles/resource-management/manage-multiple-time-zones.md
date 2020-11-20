---
title: 管理时区
description: 在创建项目时，其时区基于所应用的工作时间模板中定义的时区。
author: ruhercul
manager: Annbe
ms.date: 10/05/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 278b226c88c2f441262eb5be0504f34a1964848c
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/28/2020
ms.locfileid: "4119812"
---
# <a name="manage-time-zones"></a>管理时区

_**适用于：** 基于资源/非库存场景的 Project Operations，精简部署 - 估价开票交易_


## <a name="projects"></a>项目

在创建项目时，时区基于所应用的工作时间模板中定义的时区。 在 **项目** 上，除 **任务** 选项卡外，日期始终与每个选项卡上登录的用户的时区相关。当您查看工作分解结构时，日期始终会以项目的时区显示。

## <a name="tasks"></a>任务

在创建任务时，开始时间、结束时间和小时/天由项目的工作时间控制。 例如，如果在时区为 -8 PST 且具有以下工作时间的项目中创建任务：星期一至星期五，上午 9:00 至下午 5:00，创建的任何没有分配的任务都将遵循项目日历的开始时间和结束时间。

## <a name="manage-resources-with-time-zones"></a>使用时区管理资源

为了在使用 **扩展预订** 时获得准确且可预测的结果，必须满足两个关键的先决条件：  

- 用户必须配置其设备的时区，使其与系统的 **个性化设置** 中定义的时区匹配。
 
  ![Windows 10 中的时区设置](media/reconcile-assignments-03.png)

  ![个性化设置中的时区设置](media/reconcile-assignments-04.png)
 
- 可预订资源必须至少有一分钟的工作时间与用于定义所请求扩展的分布重叠。 例如，以下资源的工作时间在上午 9:00 到下午 7:00 之间。 

  ![资源分布比较](media/reconcile-assignments-05.png)

下表显示了：

- 项目日历模板
- 资源 A：该资源具有相同的日历，并与项目位于同一时区中。 预订的开始时间将为上午 9:00。
- 资源 B：此资源与项目位于不同时区，从其时区的上午 7:00 开始。 但是，预订将在上午 9:00 开始，因为这是工作分布的最早开始时间。
- 资源 C 和 D：这些资源位于不同时区，彼此之间以及与项目之间都不同，其预订开始时间不早于各自的可用开始时间。

|实体  |日历  |
|-|-|
|项目日历模板   | ![项目日历](media/reconcile-assignments-06.png) |
|资源 A  | ![资源 A 日历](media/reconcile-assignments-06.png) |
|资源 B  |  ![资源 B 日历](media/reconcile-assignments-07.png) |
|资源 C  |  ![资源 C 日历](media/reconcile-assignments-08.png) |
|资源 D  | ![资源 D 日历](media/reconcile-assignments-09.png)  |
 
在导航到 **协调** 视图时，会显示资源分配和关联的预订不足。

![扩展前的协调视图](media/reconcile-assignments-10.png)

在对每个资源使用扩展预订功能之后，由于每个资源的工作时间与预订不足的信息重叠，因此成功为每个资源扩展了预订。

![预订扩展后的协调视图](media/reconcile-assignments-11.png) 

请注意，仔细查看预订的详细信息会发现预订开始时间有所不同。 预订开始时间不早于分配信息的开始时间，也不早于资源的可用开始时间。

![日程安排板中的新资源预订](media/reconcile-assignments-12.png)
