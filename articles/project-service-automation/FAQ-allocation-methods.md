---
title: 预订分配方法
description: 此主题介绍分配的不同预订方法。
author: ruhercul
manager: kfend
ms.service: business-applications
ms.custom:
- dyn365-projectservice
ms.date: 9/26/2019
ms.topic: article
ms.prod: ''
ms.technology: Microsoft Dynamics 365 Project Service Automation 2.x and 3.x
ms.assetid: 5bb0fdbc-88fe-43eb-8abf-4af9c2352a57
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 030d4fc3bb64fcc67b4a5e51016a8b3a028f3ca8
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/24/2020
ms.locfileid: "3749654"
---
# <a name="booking-allocation-methods"></a><span data-ttu-id="a6bbd-103">预订分配方法</span><span class="sxs-lookup"><span data-stu-id="a6bbd-103">Booking allocation methods</span></span>

<span data-ttu-id="a6bbd-104">不论您是在**团队**选项卡上将团队成员直接添加到项目，还是从日程安排板为项目或要求预订资源，都有一些不同的预订分配方法可供您使用。</span><span class="sxs-lookup"><span data-stu-id="a6bbd-104">Whether you add a team member directly to a project on the **Team** tab, or book a resource to a project or requirement from the Schedule board, there are a few different booking allocation methods you can use.</span></span> <span data-ttu-id="a6bbd-105">此主题说明每个方法如何工作，以及哪些方法可能导致超额预订资源。</span><span class="sxs-lookup"><span data-stu-id="a6bbd-105">This topic explains how each method works, and which methods could lead to overbooking resources.</span></span>

## <a name="booking-allocation-methods"></a><span data-ttu-id="a6bbd-106">预订分配方法</span><span class="sxs-lookup"><span data-stu-id="a6bbd-106">Booking allocation methods</span></span>

### <a name="full-capacity"></a><span data-ttu-id="a6bbd-107">完全产能</span><span class="sxs-lookup"><span data-stu-id="a6bbd-107">Full Capacity</span></span> 
<span data-ttu-id="a6bbd-108">完全产能方法为指定的起始日期和截止日期预订资源的完全产能。</span><span class="sxs-lookup"><span data-stu-id="a6bbd-108">The Full Capacity method books the resource’s full capacity for the specified from and to dates.</span></span> <span data-ttu-id="a6bbd-109">例如，如果资源将日历设置为每天八小时，每周五天，设置五个工作日的开始日期和结束日期将预订资源 40 小时。</span><span class="sxs-lookup"><span data-stu-id="a6bbd-109">For example, if a resource has a calendar set to work eight hours per day, five days a week, setting a start and end date that covers five working days will book the resource for 40 hours.</span></span> <span data-ttu-id="a6bbd-110">预订不会考虑资源的剩余产能。</span><span class="sxs-lookup"><span data-stu-id="a6bbd-110">The booking is done without regard to the resource's remaining capacity.</span></span> <span data-ttu-id="a6bbd-111">如果资源在其他项目的同一期间被预订，40 小时将预订为额外时间，这有可能导致超额预订。</span><span class="sxs-lookup"><span data-stu-id="a6bbd-111">If a resource is already booked on other projects during that period, the 40 hours is booked as additional hours, which potentially leads to overbookings.</span></span>

### <a name="remaining-capacity"></a><span data-ttu-id="a6bbd-112">剩余产能</span><span class="sxs-lookup"><span data-stu-id="a6bbd-112">Remaining Capacity</span></span>
<span data-ttu-id="a6bbd-113">仅当您使用日程安排板直接对项目预订时，剩余产能方法才可用。</span><span class="sxs-lookup"><span data-stu-id="a6bbd-113">The Remaining Capacity method is only available when you book directly to a project using the Schedule board.</span></span> <span data-ttu-id="a6bbd-114">此方法预订指定日期范围内资源的可用产能。</span><span class="sxs-lookup"><span data-stu-id="a6bbd-114">This method books the resource’s available capacity within the specified date range.</span></span> <span data-ttu-id="a6bbd-115">例如，如果资源每周有 40 小时的产能，而且已经预订了 10 小时，在同一周的预订将导致预订该周 30 小时的剩余产能。</span><span class="sxs-lookup"><span data-stu-id="a6bbd-115">For example, if a resource has a capacity of 40 hours per week and has already been booked 10 hours, booking for the same week results in booking the remaining 30 hours of capacity for that week.</span></span>

### <a name="percentage-capacity"></a><span data-ttu-id="a6bbd-116">产能百分比</span><span class="sxs-lookup"><span data-stu-id="a6bbd-116">Percentage Capacity</span></span>
<span data-ttu-id="a6bbd-117">产能百分比方法针对指定的起始日期和截止日期预订产能百分比所需的资源。</span><span class="sxs-lookup"><span data-stu-id="a6bbd-117">The Percentage Capacity method books the resource for a percentage of capacity for the specified from and to dates.</span></span> <span data-ttu-id="a6bbd-118">例如，如果资源将日历设置为每天八小时，每周五天，设置五个工作日 50% 产能的开始日期和结束日期将预订资源 20 小时。</span><span class="sxs-lookup"><span data-stu-id="a6bbd-118">For example, if a resource's calendar is set to work eight hours per day, five days a week, setting a start and end date that covers five working days at 50% capacity would book the resource for 20 hours.</span></span> <span data-ttu-id="a6bbd-119">每天的各个预订跨期间平均分布，本示例中每天为四小时。</span><span class="sxs-lookup"><span data-stu-id="a6bbd-119">The individual bookings per day are spread equally across the period, four hours per day in this example.</span></span> <span data-ttu-id="a6bbd-120">预订不会考虑资源的剩余产能。</span><span class="sxs-lookup"><span data-stu-id="a6bbd-120">The booking is done without regard to the resource’s remaining capacity.</span></span> <span data-ttu-id="a6bbd-121">如果资源在其他项目的同一期间被预订，20 小时将预订为额外时间，这有可能导致超额预订。</span><span class="sxs-lookup"><span data-stu-id="a6bbd-121">If the resource is already booked during that period on other projects, the 20 hours is booked as additional hours, which potentially leads to overbookings.</span></span>

### <a name="evenly-distribute-hours"></a><span data-ttu-id="a6bbd-122">平均分发小时</span><span class="sxs-lookup"><span data-stu-id="a6bbd-122">Evenly Distribute Hours</span></span>
<span data-ttu-id="a6bbd-123">平均分发小时方法预订资源指定的小时数，根据指定的起始日期/截止日期按天平均分配时间。</span><span class="sxs-lookup"><span data-stu-id="a6bbd-123">The Evenly Distribute Hours method books the resource for a specified number of hours, distributing the time evenly per day over the specified from and to dates.</span></span> <span data-ttu-id="a6bbd-124">例如，如果您预订资源五天期间的 20 小时，此方法将平均分配 20 小时，即每天四小时。</span><span class="sxs-lookup"><span data-stu-id="a6bbd-124">For example, if you book a resource for 20 hours over a five day period, this method distributes the 20 hours evenly at four hours per day.</span></span> <span data-ttu-id="a6bbd-125">预订不会考虑资源的剩余产能。</span><span class="sxs-lookup"><span data-stu-id="a6bbd-125">The booking is done without regard to the resource's remaining capacity.</span></span> <span data-ttu-id="a6bbd-126">如果资源在其他项目的同一期间被预订，20 小时将预订为额外时间，这有可能导致超额预订。</span><span class="sxs-lookup"><span data-stu-id="a6bbd-126">If the resource is already booked during that period on other projects, the 20 hours is booked as additional hours, which potentially leads to overbookings.</span></span>

### <a name="front-load-hours"></a><span data-ttu-id="a6bbd-127">前期负荷小时</span><span class="sxs-lookup"><span data-stu-id="a6bbd-127">Front Load Hours</span></span>
<span data-ttu-id="a6bbd-128">前期负荷小时方法预订资源指定的小时数，根据指定的起始日期和截止日期前期负荷每天的时间。</span><span class="sxs-lookup"><span data-stu-id="a6bbd-128">The Front Load Hours method books the resource for a specified number of hours, front-loading the per-day hours over the specified from and to dates.</span></span> <span data-ttu-id="a6bbd-129">前期负荷按照“先到先用”的顺序使用资源的可用产能。</span><span class="sxs-lookup"><span data-stu-id="a6bbd-129">Front-loading consumes the resource's available capacity in a “first-in-first-consumed” order.</span></span> <span data-ttu-id="a6bbd-130">例如，如果资源的工作计划是每天八小时，每周五天，并且他们当前没有预订，预订资源五个工作日期间的 20 小时将导致以下每日预订模式：</span><span class="sxs-lookup"><span data-stu-id="a6bbd-130">For example, if a resource’s work schedule is eight hours per day, five days per week, and they have no current bookings, booking the resource for 20 hours over a five working day period results in the following daily booking pattern:</span></span> 

|                           |    <span data-ttu-id="a6bbd-131">第 1 天</span><span class="sxs-lookup"><span data-stu-id="a6bbd-131">Day 1</span></span>    |    <span data-ttu-id="a6bbd-132">第 2 天</span><span class="sxs-lookup"><span data-stu-id="a6bbd-132">Day 2</span></span>    |    <span data-ttu-id="a6bbd-133">第 3 天</span><span class="sxs-lookup"><span data-stu-id="a6bbd-133">Day 3</span></span>    |    <span data-ttu-id="a6bbd-134">第 4 天</span><span class="sxs-lookup"><span data-stu-id="a6bbd-134">Day 4</span></span>    |    <span data-ttu-id="a6bbd-135">第 5 天</span><span class="sxs-lookup"><span data-stu-id="a6bbd-135">Day 5</span></span>    |    <span data-ttu-id="a6bbd-136">总计</span><span class="sxs-lookup"><span data-stu-id="a6bbd-136">Total</span></span>    |
|---------------------------|-------------|-------------|-------------|-------------|-------------|-------------|
|    <span data-ttu-id="a6bbd-137">现有预订</span><span class="sxs-lookup"><span data-stu-id="a6bbd-137">Existing   bookings</span></span>    |    <span data-ttu-id="a6bbd-138">0</span><span class="sxs-lookup"><span data-stu-id="a6bbd-138">0</span></span>        |    <span data-ttu-id="a6bbd-139">0</span><span class="sxs-lookup"><span data-stu-id="a6bbd-139">0</span></span>        |    <span data-ttu-id="a6bbd-140">0</span><span class="sxs-lookup"><span data-stu-id="a6bbd-140">0</span></span>        |    <span data-ttu-id="a6bbd-141">0</span><span class="sxs-lookup"><span data-stu-id="a6bbd-141">0</span></span>        |    <span data-ttu-id="a6bbd-142">0</span><span class="sxs-lookup"><span data-stu-id="a6bbd-142">0</span></span>        |    <span data-ttu-id="a6bbd-143">0</span><span class="sxs-lookup"><span data-stu-id="a6bbd-143">0</span></span>        |
|    <span data-ttu-id="a6bbd-144">新预订</span><span class="sxs-lookup"><span data-stu-id="a6bbd-144">New   booking</span></span>          |    <span data-ttu-id="a6bbd-145">8</span><span class="sxs-lookup"><span data-stu-id="a6bbd-145">8</span></span>        |    <span data-ttu-id="a6bbd-146">8</span><span class="sxs-lookup"><span data-stu-id="a6bbd-146">8</span></span>        |    <span data-ttu-id="a6bbd-147">4</span><span class="sxs-lookup"><span data-stu-id="a6bbd-147">4</span></span>        |    <span data-ttu-id="a6bbd-148">0</span><span class="sxs-lookup"><span data-stu-id="a6bbd-148">0</span></span>        |    <span data-ttu-id="a6bbd-149">0</span><span class="sxs-lookup"><span data-stu-id="a6bbd-149">0</span></span>        |    <span data-ttu-id="a6bbd-150">20</span><span class="sxs-lookup"><span data-stu-id="a6bbd-150">20</span></span>       |

<span data-ttu-id="a6bbd-151">前期负荷方法考虑现有预订和可用产能。</span><span class="sxs-lookup"><span data-stu-id="a6bbd-151">The front load method takes into consideration existing bookings and available capacity.</span></span> <span data-ttu-id="a6bbd-152">例如，如果同一个资源已在工作周内有 20 小时的预订，新预订将使用剩余产能，如下所示：</span><span class="sxs-lookup"><span data-stu-id="a6bbd-152">For example, if the same resource already has 20 hours of bookings in the work week, the new bookings consume the remaining capacity as follows:</span></span>

|                     | <span data-ttu-id="a6bbd-153">第 1 天</span><span class="sxs-lookup"><span data-stu-id="a6bbd-153">Day 1</span></span> | <span data-ttu-id="a6bbd-154">第 2 天</span><span class="sxs-lookup"><span data-stu-id="a6bbd-154">Day 2</span></span> | <span data-ttu-id="a6bbd-155">第 3 天</span><span class="sxs-lookup"><span data-stu-id="a6bbd-155">Day 3</span></span> | <span data-ttu-id="a6bbd-156">第 4 天</span><span class="sxs-lookup"><span data-stu-id="a6bbd-156">Day 4</span></span> | <span data-ttu-id="a6bbd-157">第 5 天</span><span class="sxs-lookup"><span data-stu-id="a6bbd-157">Day 5</span></span> | <span data-ttu-id="a6bbd-158">总计</span><span class="sxs-lookup"><span data-stu-id="a6bbd-158">Total</span></span> |
|---------------------|-------|-------|-------|-------|-------|-------|
| <span data-ttu-id="a6bbd-159">现有预订</span><span class="sxs-lookup"><span data-stu-id="a6bbd-159">Existing   bookings</span></span> | <span data-ttu-id="a6bbd-160">8</span><span class="sxs-lookup"><span data-stu-id="a6bbd-160">8</span></span>     | <span data-ttu-id="a6bbd-161">8</span><span class="sxs-lookup"><span data-stu-id="a6bbd-161">8</span></span>     | <span data-ttu-id="a6bbd-162">4</span><span class="sxs-lookup"><span data-stu-id="a6bbd-162">4</span></span>     | <span data-ttu-id="a6bbd-163">0</span><span class="sxs-lookup"><span data-stu-id="a6bbd-163">0</span></span>     | <span data-ttu-id="a6bbd-164">0</span><span class="sxs-lookup"><span data-stu-id="a6bbd-164">0</span></span>     | <span data-ttu-id="a6bbd-165">20</span><span class="sxs-lookup"><span data-stu-id="a6bbd-165">20</span></span>    |
| <span data-ttu-id="a6bbd-166">新预订</span><span class="sxs-lookup"><span data-stu-id="a6bbd-166">New   booking</span></span>       | <span data-ttu-id="a6bbd-167">0</span><span class="sxs-lookup"><span data-stu-id="a6bbd-167">0</span></span>     | <span data-ttu-id="a6bbd-168">0</span><span class="sxs-lookup"><span data-stu-id="a6bbd-168">0</span></span>     | <span data-ttu-id="a6bbd-169">4</span><span class="sxs-lookup"><span data-stu-id="a6bbd-169">4</span></span>     | <span data-ttu-id="a6bbd-170">8</span><span class="sxs-lookup"><span data-stu-id="a6bbd-170">8</span></span>     | <span data-ttu-id="a6bbd-171">8</span><span class="sxs-lookup"><span data-stu-id="a6bbd-171">8</span></span>     | <span data-ttu-id="a6bbd-172">20</span><span class="sxs-lookup"><span data-stu-id="a6bbd-172">20</span></span>    |

<span data-ttu-id="a6bbd-173">由于考虑了可用产能，如果资源没有可以通过预订分配的剩余产能，您可能收到错误消息。</span><span class="sxs-lookup"><span data-stu-id="a6bbd-173">Because available capacity is considered, you may get an error message if the resource has no remaining capacity that can be absorbed by the booking.</span></span> <span data-ttu-id="a6bbd-174">使用此方法，不能超额预订。</span><span class="sxs-lookup"><span data-stu-id="a6bbd-174">With this method, you can’t overbook.</span></span>

### <a name="none"></a><span data-ttu-id="a6bbd-175">无</span><span class="sxs-lookup"><span data-stu-id="a6bbd-175">None</span></span>
<span data-ttu-id="a6bbd-176">“无”方法仅当您从项目内的**团队**选项卡预订时可用。</span><span class="sxs-lookup"><span data-stu-id="a6bbd-176">The None method is only available when you book from the **Team** tab within a project.</span></span> <span data-ttu-id="a6bbd-177">该方法在项目中作为团队成员添加资源，但不创建任何分配资源产能的预订。</span><span class="sxs-lookup"><span data-stu-id="a6bbd-177">This method adds the resource as a team member on the project, but doesn’t create any bookings that absorb the resource's capacity.</span></span> <span data-ttu-id="a6bbd-178">在创建项目时添加默认项目经理团队成员时使用此方法。</span><span class="sxs-lookup"><span data-stu-id="a6bbd-178">This method is used when the default project manager team member is added when a project is created.</span></span> <span data-ttu-id="a6bbd-179">创建项目的项目经理用户默认添加到项目，以便项目实体记录具有负责人，并且项目上有一个审批者。</span><span class="sxs-lookup"><span data-stu-id="a6bbd-179">The project manager user who created the project is added by default to the project, so that the project entity record has an owner and there is one approver on the project.</span></span> <span data-ttu-id="a6bbd-180">由于该用户没有任何预订，如果您确实要预订资源，您可以将其删除，然后使用其他分配方法重新添加，或将资源添加到任务，然后使用**协调**选项卡上的**扩展预订**创建用于分派的预订。</span><span class="sxs-lookup"><span data-stu-id="a6bbd-180">Because this user doesn't have any bookings, if you do want to book the resource, you can either delete and then re-add them using a different allocation method, or add the resource to tasks and then use **Extend Bookings** on the **Reconciliation** tab to create bookings for the assignments.</span></span>

## <a name="allocation-methods-that-lead-to-overbooking"></a><span data-ttu-id="a6bbd-181">导致超额预订的分配方法</span><span class="sxs-lookup"><span data-stu-id="a6bbd-181">Allocation methods that lead to overbooking</span></span>
<span data-ttu-id="a6bbd-182">简而言之，如果资源已在其他项目（或其他工作订单或可计划实体）中提交，以下分配方法将导致超额预订：</span><span class="sxs-lookup"><span data-stu-id="a6bbd-182">To summarize, the following allocation methods lead to overbooking if the resource is already committed in other projects (or for other work orders or schedulable entities):</span></span>

- <span data-ttu-id="a6bbd-183">完全产能</span><span class="sxs-lookup"><span data-stu-id="a6bbd-183">Full Capacity</span></span>
- <span data-ttu-id="a6bbd-184">产能百分比</span><span class="sxs-lookup"><span data-stu-id="a6bbd-184">Percentage Capacity</span></span>
- <span data-ttu-id="a6bbd-185">平均分发小时</span><span class="sxs-lookup"><span data-stu-id="a6bbd-185">Evenly Distribute Hours</span></span>

<span data-ttu-id="a6bbd-186">在使用这三种分配方法之一时，不会通知您资源被超额预订。</span><span class="sxs-lookup"><span data-stu-id="a6bbd-186">When using one of these three allocation methods, you won’t be notified that the resource is overbooked.</span></span> <span data-ttu-id="a6bbd-187">若要更正超额预订，则需要使用日程安排板。</span><span class="sxs-lookup"><span data-stu-id="a6bbd-187">To correct the overbooking, you’ll need to use the Schedule board.</span></span>