---
title: 如何在应用程序版本 2.x 中“软预订”资源？
description: 本文介绍如何使用 Project Service 软预订项目团队成员。
author: JohnPBurrows
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 8/21/2018
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: a35799b422fa338c2666e1b2aa11bc2a54f5cce3
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/28/2020
ms.locfileid: "4122242"
---
# <a name="how-do-i-soft-book-resources-in-the-web-app-project-service-app-v2x"></a><span data-ttu-id="7e7f3-103">如何在 Web 应用程序（Project Service 应用程序 v2.x）中“软预订”资源？</span><span class="sxs-lookup"><span data-stu-id="7e7f3-103">How do I "soft book" resources in the web app (Project Service app v2.x)?</span></span>

[!INCLUDE[cc-applies-to-psa-app-1.x-2.x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="7e7f3-104">您可以暂时计划或将资源“软预订”到项目团队来显示您将资源分派到项目的计划。</span><span class="sxs-lookup"><span data-stu-id="7e7f3-104">You can tentatively schedule or "soft book" a resource onto a project team to show you plan to assign the resource to a project.</span></span> <span data-ttu-id="7e7f3-105">软预订不使用资源的可用产能。</span><span class="sxs-lookup"><span data-stu-id="7e7f3-105">Soft bookings don’t consume a resource’s available capacity.</span></span> <span data-ttu-id="7e7f3-106">软预订的团队成员不能被分派到项目任务。</span><span class="sxs-lookup"><span data-stu-id="7e7f3-106">Soft-booked team members can’t be assigned to project tasks.</span></span> <span data-ttu-id="7e7f3-107">仅具有“已硬预订状态”和“已提交提交类型”的资源可以被分派到任务（假设他们具有可以覆盖分派工作量的足够的硬预订时数）。</span><span class="sxs-lookup"><span data-stu-id="7e7f3-107">Only resources with the Status Hard Booked and Commit Type Committed can be assigned to tasks (assuming they have enough hard booking hours to cover the assignment effort).</span></span>

<span data-ttu-id="7e7f3-108">软预订的项目团队成员显示在“团队成员”网格中，其软预订时数显示在“软预订”列中。</span><span class="sxs-lookup"><span data-stu-id="7e7f3-108">Soft-booked project team members show up in the Team Member grid with their soft-booked hours shown in the Soft Book column.</span></span> <span data-ttu-id="7e7f3-109">它们还显示在日程安排板上。</span><span class="sxs-lookup"><span data-stu-id="7e7f3-109">They also show up on the schedule board.</span></span> <span data-ttu-id="7e7f3-110">同样，它们不显示任何产能使用，因为软预订不使用资源的产能。</span><span class="sxs-lookup"><span data-stu-id="7e7f3-110">Again, they don’t indicate any consumption of capacity as soft-booking doesn’t consume capacity of a resource.</span></span>

<span data-ttu-id="7e7f3-111">使用 Project Service 版本 2.x 有三种将团队成员软预订到项目的方法。</span><span class="sxs-lookup"><span data-stu-id="7e7f3-111">There are three ways to soft-book a team member onto a project with Project Service version 2.x.</span></span> <span data-ttu-id="7e7f3-112">您可以通过日程安排板，使用“维护预订”功能，或创建通用资源来进行软预订。</span><span class="sxs-lookup"><span data-stu-id="7e7f3-112">You can soft-book with the schedule board, use the Maintain Bookings feature, or by creating a generic resource.</span></span> <span data-ttu-id="7e7f3-113">将在下面介绍这些方法。</span><span class="sxs-lookup"><span data-stu-id="7e7f3-113">These methods are described below.</span></span>

## <a name="soft-book-with-the-schedule-board"></a><span data-ttu-id="7e7f3-114">使用日程安排板进行软预订</span><span class="sxs-lookup"><span data-stu-id="7e7f3-114">Soft-book with the schedule board</span></span>

<span data-ttu-id="7e7f3-115">若要使用日程安排板进行软预订，请按照此过程：</span><span class="sxs-lookup"><span data-stu-id="7e7f3-115">To soft-book with the schedule board, follow this procedure:</span></span> 
1. <span data-ttu-id="7e7f3-116">打开日程安排板。</span><span class="sxs-lookup"><span data-stu-id="7e7f3-116">Open the schedule board.</span></span>
2. <span data-ttu-id="7e7f3-117">在日程安排板的底部“预订要求”面板上选择“项目”选项卡。</span><span class="sxs-lookup"><span data-stu-id="7e7f3-117">Select the Project tab on the bottom Booking Requirements panel of the schedule board.</span></span>
3. <span data-ttu-id="7e7f3-118">查找您希望在其中软预订资源的项目。</span><span class="sxs-lookup"><span data-stu-id="7e7f3-118">Find the project you wish to soft-book a resource on.</span></span> <span data-ttu-id="7e7f3-119">如果您有很多项目，请单击“项目”列标题，然后使用筛选器来查找项目。</span><span class="sxs-lookup"><span data-stu-id="7e7f3-119">If you have many projects, click on the Project column header and then use the filter to find your project.</span></span>
4. <span data-ttu-id="7e7f3-120">单击项目，然后将它拖放到资源的时间网格中。</span><span class="sxs-lookup"><span data-stu-id="7e7f3-120">Click on the project, then drag and drop it on the resource’s time grid.</span></span>
5. <span data-ttu-id="7e7f3-121">这将在右侧打开“创建资源预订”面板。</span><span class="sxs-lookup"><span data-stu-id="7e7f3-121">This opens the Create Resource Booking panel on the right.</span></span> <span data-ttu-id="7e7f3-122">调整开始日期和结束日期，选择“预订状态为软 (Booking Status as Soft)”并设置时数。</span><span class="sxs-lookup"><span data-stu-id="7e7f3-122">Adjust the start and end date, select the Booking Status as Soft and set the hours.</span></span> 
6. <span data-ttu-id="7e7f3-123">单击“预订”。</span><span class="sxs-lookup"><span data-stu-id="7e7f3-123">Click Book.</span></span>
7. <span data-ttu-id="7e7f3-124">返回项目，资源现在将显示为团队成员，软预订的时数显示在“软预订”列中。</span><span class="sxs-lookup"><span data-stu-id="7e7f3-124">Back on the project, the resource will now show as a team member with the soft booked hours in the Soft Book column.</span></span>

<span data-ttu-id="7e7f3-125">请注意，您无法在工作分解结构 (WBS) 中将资源分派到任务，因为资源必须在团队中硬预订才能分派。</span><span class="sxs-lookup"><span data-stu-id="7e7f3-125">Note that you can’t assign them to tasks on the work breakdown structure (WBS) as resources must be hard booked on the team to be assigned.</span></span>

## <a name="soft-book-using-the-maintain-bookings-feature"></a><span data-ttu-id="7e7f3-126">使用“维护预订”功能进行软预订</span><span class="sxs-lookup"><span data-stu-id="7e7f3-126">Soft-book using the Maintain Bookings feature</span></span>

<span data-ttu-id="7e7f3-127">若要使用“维护预订”进行软预订，请按照此过程：</span><span class="sxs-lookup"><span data-stu-id="7e7f3-127">To soft-book with Maintain Bookings follow this procedure:</span></span>
1. <span data-ttu-id="7e7f3-128">从团队成员网格，单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="7e7f3-128">From the team member grid, Click New.</span></span>
2. <span data-ttu-id="7e7f3-129">选择可预订资源、角色、起始日期/截止日期。</span><span class="sxs-lookup"><span data-stu-id="7e7f3-129">Select the bookable resource, role, from/to.</span></span>
3. <span data-ttu-id="7e7f3-130">选择“无”以外的分配方法：</span><span class="sxs-lookup"><span data-stu-id="7e7f3-130">Select an allocation method other than None:</span></span>
- <span data-ttu-id="7e7f3-131">完全产能</span><span class="sxs-lookup"><span data-stu-id="7e7f3-131">Full Capacity</span></span>
- <span data-ttu-id="7e7f3-132">产能百分比</span><span class="sxs-lookup"><span data-stu-id="7e7f3-132">Percentage Capacity</span></span>
- <span data-ttu-id="7e7f3-133">按时数平均分配</span><span class="sxs-lookup"><span data-stu-id="7e7f3-133">By Hours Distribute Evenly</span></span>
- <span data-ttu-id="7e7f3-134">按时数前期负荷</span><span class="sxs-lookup"><span data-stu-id="7e7f3-134">By Hours Front Load</span></span>
4. <span data-ttu-id="7e7f3-135">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="7e7f3-135">Click Save.</span></span> <span data-ttu-id="7e7f3-136">您将会在团队网格上看到资源，其时数指示为“硬”。</span><span class="sxs-lookup"><span data-stu-id="7e7f3-136">You’ll see the resource on the team grid and their hours indicated as Hard.</span></span>
5. <span data-ttu-id="7e7f3-137">通过单击“维护预订”维护资源的预订。</span><span class="sxs-lookup"><span data-stu-id="7e7f3-137">Maintain the resource’s bookings by clicking Maintain Bookings.</span></span>
6. <span data-ttu-id="7e7f3-138">在日程安排板打开时，展开资源以显示其预订。</span><span class="sxs-lookup"><span data-stu-id="7e7f3-138">When the schedule board opens, expand the resource to show their bookings.</span></span> <span data-ttu-id="7e7f3-139">您将看到预订指示为“硬”。</span><span class="sxs-lookup"><span data-stu-id="7e7f3-139">You will see the booking indicated as Hard.</span></span>
7. <span data-ttu-id="7e7f3-140">右键单击预订，在“更改状态”下，选择“软预订”，然后选择“软”。</span><span class="sxs-lookup"><span data-stu-id="7e7f3-140">Right-click the booking, under Change Status, select Soft Book and then Soft.</span></span> <span data-ttu-id="7e7f3-141">预订状态现在为“软”。</span><span class="sxs-lookup"><span data-stu-id="7e7f3-141">The booking status is now Soft.</span></span>
8. <span data-ttu-id="7e7f3-142">在关闭日程安排板后，您将在团队成员网格中看到资源的时数从“硬”改为“软”。</span><span class="sxs-lookup"><span data-stu-id="7e7f3-142">After closing the schedule board, you’ll see that the hours for the resource have changed from Hard to Soft on the team member grid.</span></span>
<span data-ttu-id="7e7f3-143">请注意，如果您将资源硬预订到团队，然后在 WBS 中向其分派任务，当您使用维护预订将“硬”状态更改为“软”时，这将从该资源的任务中删除分派，因为仅硬预订的资源可以被分派到任务。</span><span class="sxs-lookup"><span data-stu-id="7e7f3-143">Note that if you hard book a resource onto the team and then assign them tasks in the WBS, when you use maintain bookings to change the status of Hard to Soft, it will remove the assignments from the tasks for that resource, as only hard booked resources can be assigned to tasks.</span></span>

## <a name="soft-book-by-creating-a-generic-resource"></a><span data-ttu-id="7e7f3-144">通过创建通用资源进行软预订</span><span class="sxs-lookup"><span data-stu-id="7e7f3-144">Soft-book by creating a generic resource</span></span>

<span data-ttu-id="7e7f3-145">您可以通过生成通过资源团队成员，使用日程安排板或资源请求执行并在预订期间更改类型来创建软预订。</span><span class="sxs-lookup"><span data-stu-id="7e7f3-145">You can create a soft-booking by generating a generic resource team member, fulfilling with schedule board or Resource Request and changing the type during the booking.</span></span>
<span data-ttu-id="7e7f3-146">若要执行此操作，请使用以下过程：</span><span class="sxs-lookup"><span data-stu-id="7e7f3-146">To do this, use the following procedure:</span></span>

1. <span data-ttu-id="7e7f3-147">在项目 WBS 上，向您要为其生成通用团队成员的任务分派角色。</span><span class="sxs-lookup"><span data-stu-id="7e7f3-147">On the project WBS, assign roles to the tasks you wish to generate generic team members for.</span></span>
2. <span data-ttu-id="7e7f3-148">单击“生成项目团队”。</span><span class="sxs-lookup"><span data-stu-id="7e7f3-148">Click Generate Project Team.</span></span>
3. <span data-ttu-id="7e7f3-149">在项目团队成员网格中，选择通用资源并单击“预订”。</span><span class="sxs-lookup"><span data-stu-id="7e7f3-149">On the project team member grid, select the generic resource and click Book.</span></span>
4. <span data-ttu-id="7e7f3-150">在日程安排板上，选择您要预订的资源。</span><span class="sxs-lookup"><span data-stu-id="7e7f3-150">On the schedule board, select the resource that you wish to book.</span></span>
5. <span data-ttu-id="7e7f3-151">在日程安排板的“创建资源预订”面板上，将“预订状态”更改为“软”。</span><span class="sxs-lookup"><span data-stu-id="7e7f3-151">On the schedule board’s Create Resource Booking panel, change the Booking Status to Soft.</span></span>
6. <span data-ttu-id="7e7f3-152">单击“预订”或“预订并退出”。</span><span class="sxs-lookup"><span data-stu-id="7e7f3-152">Click Book or Book and Exit.</span></span>

<span data-ttu-id="7e7f3-153">在关闭日程安排板后，您将看到添加到团队的所选资源和软预订的时数以及分派的时数。</span><span class="sxs-lookup"><span data-stu-id="7e7f3-153">After closing the schedule board, you’ll see the selected resource added to the team with Soft booked hours as well as assigned hours.</span></span> <span data-ttu-id="7e7f3-154">您还将看到通用资源仍在团队上，指示任务已被分派给一个软预订的团队成员。</span><span class="sxs-lookup"><span data-stu-id="7e7f3-154">You’ll also see that the generic resource remains on the team as an indicator that the tasks are assigned to a soft-booked team member.</span></span>

<span data-ttu-id="7e7f3-155">在您准备好可以将软预订的团队成员资源更改为硬预订的团队成员以便您可以将他们分派到任务时，请执行以下操作：</span><span class="sxs-lookup"><span data-stu-id="7e7f3-155">When you’re ready to change a soft-booked team member resource to a hard-booked team member so that you can assign them to tasks, do the following:</span></span>

1. <span data-ttu-id="7e7f3-156">选择该资源，并单击“维护预订”。</span><span class="sxs-lookup"><span data-stu-id="7e7f3-156">Select that resource and click Maintain Bookings.</span></span>
2. <span data-ttu-id="7e7f3-157">在日程安排板打开时，展开资源以显示其预订。</span><span class="sxs-lookup"><span data-stu-id="7e7f3-157">When the schedule board opens, expand the resource to show their bookings.</span></span> <span data-ttu-id="7e7f3-158">您会看到标记为“软”的预订。</span><span class="sxs-lookup"><span data-stu-id="7e7f3-158">You’ll see the booking marked as Soft.</span></span>
3. <span data-ttu-id="7e7f3-159">右键单击预订，在“更改状态”下，选择“硬预订”，然后选择“硬”。</span><span class="sxs-lookup"><span data-stu-id="7e7f3-159">Right-click the booking, under Change Status, select Hard Book and then Hard.</span></span> <span data-ttu-id="7e7f3-160">预订状态现在为“硬”。</span><span class="sxs-lookup"><span data-stu-id="7e7f3-160">The booking status is now Hard.</span></span>
4. <span data-ttu-id="7e7f3-161">在关闭日程安排板后，您将在团队成员网格中看到资源的时数从“软”改为“硬”。</span><span class="sxs-lookup"><span data-stu-id="7e7f3-161">After closing the schedule board, you’ll see that the hours for the resource have changed from Soft to Hard on the team member grid.</span></span> <span data-ttu-id="7e7f3-162">您现在可以将资源分派到任务了（前提是硬预订的时数与要分派的任务的时数一致）。</span><span class="sxs-lookup"><span data-stu-id="7e7f3-162">You may now assign the resource to tasks (provided there is alignment between the hard-booked hours and the effort hours of the task for assignment).</span></span> <span data-ttu-id="7e7f3-163">请注意，如果您按照上面的项目 #3 中的通用资源执行步骤操作，在将软预订的可预订资源的状态更改为硬时，通用团队成员将被从团队中删除。</span><span class="sxs-lookup"><span data-stu-id="7e7f3-163">Note that if you followed the generic resource fulfilment steps in item #3 above, when you change the status of the soft-booked bookable resource to hard, the generic team member is removed from the team.</span></span>
