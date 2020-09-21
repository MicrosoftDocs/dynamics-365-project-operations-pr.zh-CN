---
title: 软预订资源
description: 此主题介绍如何暂时计划或软预订项目团队成员。
author: ruhercul
manager: kfend
ms.service: business-applications
ms.custom:
- dyn365-projectservice
ms.date: 9/25/2019
ms.topic: article
ms.prod: Applies to Project Service version 3.x
ms.technology: ''
ms.assetid: 04e02ff7-1024-4b65-a281-6f149921b63d
ms.author: ruhercul
audience: Admin
ms.openlocfilehash: 07e768d756732e31df82a9865b957dae09c60821
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/24/2020
ms.locfileid: "3749671"
---
# <a name="soft-book-a-resource"></a><span data-ttu-id="27d62-103">软预订资源</span><span class="sxs-lookup"><span data-stu-id="27d62-103">Soft book a resource</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="27d62-104">您可以暂时计划或将资源“软预订”到项目团队来显示您将资源分派到项目的计划。</span><span class="sxs-lookup"><span data-stu-id="27d62-104">You can tentatively schedule or "soft book" a resource onto a project team to show that you plan to assign the resource to the project.</span></span> <span data-ttu-id="27d62-105">软预订不使用资源的可用产能，您可以将软预订的团队成员分派到项目任务。</span><span class="sxs-lookup"><span data-stu-id="27d62-105">Soft bookings don’t consume a resource’s available capacity, and you can assign soft-booked team members to project tasks.</span></span> <span data-ttu-id="27d62-106">但是，由于软预订不使用资源的产能，您仍可以在同一期间内为其他任务“硬预订”该资源。</span><span class="sxs-lookup"><span data-stu-id="27d62-106">However, because soft booking doesn’t consume a resource’s capacity, you can still "hard book" the resource for other tasks within the same period.</span></span> <span data-ttu-id="27d62-107">通用资源无法软预订，软预订也不能满足对通用资源的请求。</span><span class="sxs-lookup"><span data-stu-id="27d62-107">Generic resources can’t be soft booked, nor can a soft booking fulfill a request for a generic resource.</span></span>

<span data-ttu-id="27d62-108">软预订的项目团队成员在**项目**页的**团队**选项卡上列出，其软预订工时显示在**指定团队成员**视图的**软预订时数**列中。</span><span class="sxs-lookup"><span data-stu-id="27d62-108">Soft-booked project team members are listed on the **Team** tab of the **Project** page, with their soft-booked hours shown in the **Soft Booked Hours** column in the **Named Team Members** view.</span></span> <span data-ttu-id="27d62-109">软预订的团队成员同时在日程安排板上列出。</span><span class="sxs-lookup"><span data-stu-id="27d62-109">Soft-booked team members are also listed on the Schedule board.</span></span> <span data-ttu-id="27d62-110">因为它们都属于软预订，日程安排板不显示这些资源的任何产能的使用。</span><span class="sxs-lookup"><span data-stu-id="27d62-110">Because they are soft booked, the Schedule board doesn't show any consumption of capacity for these resources.</span></span> <span data-ttu-id="27d62-111">软预订的时间不显示在**协调**选项卡上，也不显示在日程安排板**协调**选项卡的**扩展预订**字段中。</span><span class="sxs-lookup"><span data-stu-id="27d62-111">Soft-booked time doesn’t show up on the **Reconciliation** tab, nor is it shown in the **Extend Bookings** field in the **Reconciliation** tab of the Schedule board.</span></span> 

<span data-ttu-id="27d62-112">可通过两种方法为项目软预订团队成员：直接从日程安排板，或通过在**团队**选项卡上添加团队成员。</span><span class="sxs-lookup"><span data-stu-id="27d62-112">There are two ways to soft book a team member onto a project: directly from the Schedule board, or by adding the team member on the **Team** tab.</span></span> 

## <a name="soft-book-from-the-schedule-board"></a><span data-ttu-id="27d62-113">从日程安排板进行软预订</span><span class="sxs-lookup"><span data-stu-id="27d62-113">Soft book from the Schedule board</span></span>
<span data-ttu-id="27d62-114">完成以下步骤从日程安排板软预订资源。</span><span class="sxs-lookup"><span data-stu-id="27d62-114">Complete the following steps to soft book a resource from the Schedule board.</span></span> 

1. <span data-ttu-id="27d62-115">打开日程安排板，然后在**预订要求**面板中选择**项目**选项卡。</span><span class="sxs-lookup"><span data-stu-id="27d62-115">Open the Schedule board, and then in the **Booking Requirements** panel, select the **Project** tab.</span></span>
2. <span data-ttu-id="27d62-116">找到要为其软预订资源的项目。</span><span class="sxs-lookup"><span data-stu-id="27d62-116">Find the project for which you want to soft book a resource.</span></span> <span data-ttu-id="27d62-117">如果列表中有大量项目，请选择**项目**列标题，然后使用筛选器搜索一个或多个项目。</span><span class="sxs-lookup"><span data-stu-id="27d62-117">If there are a large number of projects in the list, select the **Project** column header, and then use the filter to search for one or more projects.</span></span>
3. <span data-ttu-id="27d62-118">搜索项目，然后将其拖放到资源的时间网格中。</span><span class="sxs-lookup"><span data-stu-id="27d62-118">Select the project, and then drag-and-drop it on the resource’s time grid.</span></span>
5. <span data-ttu-id="27d62-119">在**创建资源预订**面板中，调整开始日期和结束日期，将**预订状态**设置为**软性**，然后设置工时。</span><span class="sxs-lookup"><span data-stu-id="27d62-119">In the **Create Resource Booking** panel, adjust the start and end date, set the **Booking Status** to **Soft**, and then set the hours.</span></span> 
6. <span data-ttu-id="27d62-120">单击**预订**。</span><span class="sxs-lookup"><span data-stu-id="27d62-120">Click **Book**.</span></span> <span data-ttu-id="27d62-121">此资源现在作为项目的资源显示在**团队**选项卡上。</span><span class="sxs-lookup"><span data-stu-id="27d62-121">The resource now shows on the **Team** tab as a resource for the project.</span></span> <span data-ttu-id="27d62-122">在**指定团队成员**视图中，您将在**软预订工时数**列中看到软预订的工时数。</span><span class="sxs-lookup"><span data-stu-id="27d62-122">On the **Named Team Member** view you’ll see the soft-booked hours in the **Soft Booked Hours** column.</span></span>

> [!NOTE]
> <span data-ttu-id="27d62-123">您现在可以在**日程安排**选项卡上将软预订的资源分派到任务。在**协调**选项卡上，该资源将显示相对于其任务分派缺少的预订，因为**协调**选项卡只考虑硬预订。</span><span class="sxs-lookup"><span data-stu-id="27d62-123">You can now assign the soft booked to tasks on the **Schedule** tab. On the **Reconciliation** tab, the resource shows a booking deficit relative to the task assignment as the **Reconciliation** tab only considers hard-bookings.</span></span> <span data-ttu-id="27d62-124">您可以使用**扩展预订**功能来硬预订资源以根据资源分派消除硬预订缺少情况。</span><span class="sxs-lookup"><span data-stu-id="27d62-124">You can use the **Extend Bookings** feature to hard-book the resource to eliminate the deficit of hard-bookings against the resources assignments.</span></span> <span data-ttu-id="27d62-125">您必须使用**维护预订**手动取消资源的软预订。</span><span class="sxs-lookup"><span data-stu-id="27d62-125">You’ll have to manually cancel the soft booking for the resource by using **Maintain Bookings**.</span></span>

## <a name="soft-book-on-the-team-tab"></a><span data-ttu-id="27d62-126">“团队”选项卡上的软预订</span><span class="sxs-lookup"><span data-stu-id="27d62-126">Soft book on the Team tab</span></span>

<span data-ttu-id="27d62-127">您可以直接在**团队**选项卡上添加团队成员，然后使用**维护预订**将其预订状态从**硬**更改为**软**。</span><span class="sxs-lookup"><span data-stu-id="27d62-127">You can add team members directly on the **Team** tab, and then change their booking status from **Hard** to **Soft** with **Maintain Bookings**.</span></span> <span data-ttu-id="27d62-128">在通过此方式添加团队成员时，将始终进行硬预订，除非您选择**无**作为分配方法。</span><span class="sxs-lookup"><span data-stu-id="27d62-128">When you add a team member this way, it will always result in a hard-booking unless you select the allocation method as **None**.</span></span>

<span data-ttu-id="27d62-129">若要使用此方法，请完成以下步骤。</span><span class="sxs-lookup"><span data-stu-id="27d62-129">To use this method, complete the following steps.</span></span>

1. <span data-ttu-id="27d62-130">在**项目**页的**团队**选项卡上，单击**新建**。</span><span class="sxs-lookup"><span data-stu-id="27d62-130">On the **Project** page, on the **Team** tab, click **New**.</span></span>
2. <span data-ttu-id="27d62-131">选择可预订资源、角色、起始日期和截止日期。</span><span class="sxs-lookup"><span data-stu-id="27d62-131">Select the bookable resource, the role, and the from and to dates.</span></span>
3. <span data-ttu-id="27d62-132">选择**无**以外的分配方法：</span><span class="sxs-lookup"><span data-stu-id="27d62-132">Select an allocation method other than **None**.</span></span>
4. <span data-ttu-id="27d62-133">选择**保存**。</span><span class="sxs-lookup"><span data-stu-id="27d62-133">Select **Save**.</span></span> <span data-ttu-id="27d62-134">您将会在网格上看到资源，其时数显示在**硬预订时数**列中。</span><span class="sxs-lookup"><span data-stu-id="27d62-134">You’ll see the resource on the grid and their hours in the **Hard Booked Hours** column.</span></span>
5. <span data-ttu-id="27d62-135">通过选择**维护预订**维护资源的预订。</span><span class="sxs-lookup"><span data-stu-id="27d62-135">Maintain the resource’s bookings by selecting **Maintain Bookings**.</span></span>
6. <span data-ttu-id="27d62-136">在日程安排板打开时，展开资源以显示其预订。</span><span class="sxs-lookup"><span data-stu-id="27d62-136">When the Schedule board opens, expand the resource to show their bookings.</span></span> <span data-ttu-id="27d62-137">您将看到预订显示为**硬**。</span><span class="sxs-lookup"><span data-stu-id="27d62-137">You will see the booking shown as **Hard**.</span></span>
7. <span data-ttu-id="27d62-138">右键单击预订，在**更改状态**下，选择**软预订** \> **软**。</span><span class="sxs-lookup"><span data-stu-id="27d62-138">Right-click the booking, and under **Change Status**, select **Soft Book** \> **Soft**.</span></span> <span data-ttu-id="27d62-139">预订状态现在为**软**。</span><span class="sxs-lookup"><span data-stu-id="27d62-139">The booking status is now **Soft**.</span></span>
8. <span data-ttu-id="27d62-140">在关闭日程安排板后，当查看**指定团队成员**视图时，您将看到资源的时数已从**团队**选项卡网格的**硬预订时数**列移至**软预订时数**。</span><span class="sxs-lookup"><span data-stu-id="27d62-140">After you close the Schedule board, you’ll see that the hours for the resource have moved from the **Hard Booked Hours** column to the **Soft Booked Hours** on the **Team** tab grid, when looking at the **Named Team Members** view.</span></span>

> [!NOTE]
> <span data-ttu-id="27d62-141">在使用**维护预订**将状态从**硬**更改为**软**时，如果您将资源硬预订给团队，然后为该资源分派任务，将保留该资源的任务分派。</span><span class="sxs-lookup"><span data-stu-id="27d62-141">When you use **Maintain Bookings** to change the status from **Hard** to **Soft**, if you hard-book a resource onto the team and then assign tasks to the resource, the task assignments for the resource are retained.</span></span> <span data-ttu-id="27d62-142">但是，在**协调**选项卡上，资源将缺少预订，因为在协调预订与分派时将仅考虑硬预订。</span><span class="sxs-lookup"><span data-stu-id="27d62-142">However, on the **Reconciliation** tab, the resource will have a booking deficiency because only hard-bookings are considered when reconciling bookings versus assignments.</span></span> <span data-ttu-id="27d62-143">您可以使用**协调**选项卡上的**扩展预订**功能来硬预订资源以根据资源分派消除硬预订缺少情况。</span><span class="sxs-lookup"><span data-stu-id="27d62-143">You can use the **Extend Bookings** feature on the **Reconciliation** tab to hard-book the resource to eliminate the deficit of hard bookings against the resources assignments.</span></span> <span data-ttu-id="27d62-144">您必须使用**维护预订**取消资源的软预订。</span><span class="sxs-lookup"><span data-stu-id="27d62-144">You’ll have to cancel the soft booking for the resource by using **Maintain Bookings**.</span></span>

<span data-ttu-id="27d62-145">在您准备好可以将软预订的团队成员资源更改为硬预订的团队成员时，请执行以下操作：</span><span class="sxs-lookup"><span data-stu-id="27d62-145">When you’re ready to change a soft-booked team member resource to a hard-booked team member, do the following:</span></span>

1. <span data-ttu-id="27d62-146">在日程安排板上，展开资源以显示其预订。</span><span class="sxs-lookup"><span data-stu-id="27d62-146">On the Schedule board, expand the resource to show their bookings.</span></span> <span data-ttu-id="27d62-147">您会看到显示为**软**的预订。</span><span class="sxs-lookup"><span data-stu-id="27d62-147">You’ll see the booking shown as **Soft**.</span></span>
2. <span data-ttu-id="27d62-148">右键单击预订，在**更改状态**下，选择**硬预订** \> **硬**。</span><span class="sxs-lookup"><span data-stu-id="27d62-148">Right-click the booking, and under **Change Status**, select **Hard Book** \> **Hard**.</span></span> <span data-ttu-id="27d62-149">预订状态现在为**硬**。</span><span class="sxs-lookup"><span data-stu-id="27d62-149">The booking status is now **Hard**.</span></span>
3. <span data-ttu-id="27d62-150">在关闭日程安排板、返回项目，然后打开**团队**选项卡后，当进入**指定团队成员**视图时，您将看到资源的时数已从**团队**选项卡的**软预订时数**列移至**硬预订时数**列。</span><span class="sxs-lookup"><span data-stu-id="27d62-150">After you close the Schedule board, return to the project, and open the **Team** tab, you’ll see that the hours for the resource have moved from the **Soft Booked Hours** column to the **Hard Booked Hours** column on the **Team** tab when in the **Named Team Members** view.</span></span> <span data-ttu-id="27d62-151">如果资源被分派到任务，他们将不再显示**协调**选项卡上缺少的预订，因为其预订现在是硬预订。</span><span class="sxs-lookup"><span data-stu-id="27d62-151">If the resource was assigned to tasks, they’ll no longer show a booking deficit on the **Reconciliation** tab as their bookings are now hard.</span></span>

