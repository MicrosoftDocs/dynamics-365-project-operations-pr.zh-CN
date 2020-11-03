---
title: 管理时区
description: 在创建项目时，其时区基于所应用的工作时间模板中定义的时区。
author: ruhercul
manager: Annbe
ms.date: 10/05/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 27f58f0dacc3404119a719547ad374629c740740
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/16/2020
ms.locfileid: "4072542"
---
# <a name="manage-time-zones"></a><span data-ttu-id="95ec8-103">管理时区</span><span class="sxs-lookup"><span data-stu-id="95ec8-103">Manage time zones</span></span>

<span data-ttu-id="95ec8-104">_**适用于：** 基于资源/非库存场景的 Project Operations，精简部署 - 估价开票交易_</span><span class="sxs-lookup"><span data-stu-id="95ec8-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>


## <a name="projects"></a><span data-ttu-id="95ec8-105">项目</span><span class="sxs-lookup"><span data-stu-id="95ec8-105">Projects</span></span>

<span data-ttu-id="95ec8-106">在创建项目时，时区基于所应用的工作时间模板中定义的时区。</span><span class="sxs-lookup"><span data-stu-id="95ec8-106">When a project is created, the time zone is based on the time zone defined in the applied work hour template.</span></span> <span data-ttu-id="95ec8-107">在 **项目** 上，除 **任务** 选项卡外，日期始终与每个选项卡上登录的用户的时区相关。当您查看工作分解结构时，日期始终会以项目的时区显示。</span><span class="sxs-lookup"><span data-stu-id="95ec8-107">On the **Project** for, the dates are always relative to the time zone of the user that is logged in on each tab, except the **Task** tab. When you view the work breakdown structure, the dates will always be displayed in the project’s time zone.</span></span>

## <a name="tasks"></a><span data-ttu-id="95ec8-108">任务</span><span class="sxs-lookup"><span data-stu-id="95ec8-108">Tasks</span></span>

<span data-ttu-id="95ec8-109">在创建任务时，开始时间、结束时间和小时/天由项目的工作时间控制。</span><span class="sxs-lookup"><span data-stu-id="95ec8-109">When a task is created, the start time, end time, and hours/day is controlled by the working hours of the project.</span></span> <span data-ttu-id="95ec8-110">例如，如果在时区为 -8 PST 且具有以下工作时间的项目中创建任务：星期一至星期五，上午 9:00 至下午 5:00，创建的任何没有分配的任务都将遵循项目日历的开始时间和结束时间。</span><span class="sxs-lookup"><span data-stu-id="95ec8-110">For example, if a task is created with a project whose time zone is -8 PST and has the following working hours: 9:00 AM to 5:00 PM Monday to Friday, any task created without an assignment will respect the start time and end time of the project calendar.</span></span>

## <a name="manage-resources-with-time-zones"></a><span data-ttu-id="95ec8-111">使用时区管理资源</span><span class="sxs-lookup"><span data-stu-id="95ec8-111">Manage resources with time zones</span></span>

<span data-ttu-id="95ec8-112">为了在使用 **扩展预订** 时获得准确且可预测的结果，必须满足两个关键的先决条件：</span><span class="sxs-lookup"><span data-stu-id="95ec8-112">For accurate and predictable results when using **Extend Booking** , there are two key prerequisites that must be met:</span></span>  

- <span data-ttu-id="95ec8-113">用户必须配置其设备的时区，使其与系统的 **个性化设置** 中定义的时区匹配。</span><span class="sxs-lookup"><span data-stu-id="95ec8-113">The user must configure their device's time zone to match the time zone defined in the system's **Personalization Settings**.</span></span>
 
  ![Windows 10 中的时区设置](media/reconcile-assignments-03.png)

  ![个性化设置中的时区设置](media/reconcile-assignments-04.png)
 
- <span data-ttu-id="95ec8-116">可预订资源必须至少有一分钟的工作时间与用于定义所请求扩展的分布重叠。</span><span class="sxs-lookup"><span data-stu-id="95ec8-116">The bookable resource must have at least one minute of working time that overlaps with the contours that are used to define the requested extension.</span></span> <span data-ttu-id="95ec8-117">例如，以下资源的工作时间在上午 9:00 到下午 7:00 之间。</span><span class="sxs-lookup"><span data-stu-id="95ec8-117">For example, the following resources with working hours that fall between 9:00 AM and 7:00 PM.</span></span> 

  ![资源分布比较](media/reconcile-assignments-05.png)

<span data-ttu-id="95ec8-119">下表显示了：</span><span class="sxs-lookup"><span data-stu-id="95ec8-119">The following table shows:</span></span>

- <span data-ttu-id="95ec8-120">项目日历模板</span><span class="sxs-lookup"><span data-stu-id="95ec8-120">A project calendar template</span></span>
- <span data-ttu-id="95ec8-121">资源 A：该资源具有相同的日历，并与项目位于同一时区中。</span><span class="sxs-lookup"><span data-stu-id="95ec8-121">Resource A: This resource has the same calendar and is in the same time zone as the project.</span></span> <span data-ttu-id="95ec8-122">预订的开始时间将为上午 9:00。</span><span class="sxs-lookup"><span data-stu-id="95ec8-122">The start time of the bookings will be 9:00 AM.</span></span>
- <span data-ttu-id="95ec8-123">资源 B：此资源与项目位于不同时区，从其时区的上午 7:00 开始。</span><span class="sxs-lookup"><span data-stu-id="95ec8-123">Resource B: This resource is located in a different time zone than the project and starts at 7:00 AM in their time zone.</span></span> <span data-ttu-id="95ec8-124">但是，预订将在上午 9:00 开始，因为这是工作分布的最早开始时间。</span><span class="sxs-lookup"><span data-stu-id="95ec8-124">However, the bookings will begin at 9:00 AM as that is the earliest start time of the assignment contour.</span></span>
- <span data-ttu-id="95ec8-125">资源 C 和 D：这些资源位于不同时区，彼此之间以及与项目之间都不同，其预订开始时间不早于各自的可用开始时间。</span><span class="sxs-lookup"><span data-stu-id="95ec8-125">Resources C and D: The resources are located in different time zones, both different from each other and the project, and their bookings start no earlier than their respective available start times.</span></span>

|<span data-ttu-id="95ec8-126">实体</span><span class="sxs-lookup"><span data-stu-id="95ec8-126">Entity</span></span>  |<span data-ttu-id="95ec8-127">日历</span><span class="sxs-lookup"><span data-stu-id="95ec8-127">Calendar</span></span>  |
|-|-|
|<span data-ttu-id="95ec8-128">项目日历模板</span><span class="sxs-lookup"><span data-stu-id="95ec8-128">Project calendar template</span></span>   | ![项目日历](media/reconcile-assignments-06.png) |
|<span data-ttu-id="95ec8-130">资源 A</span><span class="sxs-lookup"><span data-stu-id="95ec8-130">Resource A</span></span>  | ![资源 A 日历](media/reconcile-assignments-06.png) |
|<span data-ttu-id="95ec8-132">资源 B</span><span class="sxs-lookup"><span data-stu-id="95ec8-132">Resource B</span></span>  |  ![资源 B 日历](media/reconcile-assignments-07.png) |
|<span data-ttu-id="95ec8-134">资源 C</span><span class="sxs-lookup"><span data-stu-id="95ec8-134">Resource C</span></span>  |  ![资源 C 日历](media/reconcile-assignments-08.png) |
|<span data-ttu-id="95ec8-136">资源 D</span><span class="sxs-lookup"><span data-stu-id="95ec8-136">Resource D</span></span>  | ![资源 D 日历](media/reconcile-assignments-09.png)  |
 
<span data-ttu-id="95ec8-138">在导航到 **协调** 视图时，会显示资源分配和关联的预订不足。</span><span class="sxs-lookup"><span data-stu-id="95ec8-138">When you navigate to the **Reconciliation** view, the resource assignments and the associated booking shortages are displayed.</span></span>

![扩展前的协调视图](media/reconcile-assignments-10.png)

<span data-ttu-id="95ec8-140">在对每个资源使用扩展预订功能之后，由于每个资源的工作时间与预订不足的信息重叠，因此成功为每个资源扩展了预订。</span><span class="sxs-lookup"><span data-stu-id="95ec8-140">After the extend booking functionality has been used for each resource, bookings are successfully extended for each resource because each resource’s working hours overlapped with the contours of the shortage.</span></span>

![预订扩展后的协调视图](media/reconcile-assignments-11.png) 

<span data-ttu-id="95ec8-142">请注意，仔细查看预订的详细信息会发现预订开始时间有所不同。</span><span class="sxs-lookup"><span data-stu-id="95ec8-142">Notice that a closer look at the details of the bookings shows differences in the start time of the bookings.</span></span> <span data-ttu-id="95ec8-143">预订开始时间不早于分配信息的开始时间，也不早于资源的可用开始时间。</span><span class="sxs-lookup"><span data-stu-id="95ec8-143">The bookings start no earlier than the start time of the assignment contour and no earlier than the available start time of the resource.</span></span>

![日程安排板中的新资源预订](media/reconcile-assignments-12.png)
