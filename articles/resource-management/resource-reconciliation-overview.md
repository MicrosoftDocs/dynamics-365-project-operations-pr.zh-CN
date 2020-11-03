---
title: 资源协调概述
description: 本主题提供有关确保资源预订和项目分派保持一致的信息。
author: ruhercul
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: ruhercul
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: e2b16a6e1c48769ed4d903e546804ba1c4e1c4fa
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/16/2020
ms.locfileid: "4072546"
---
# <a name="resource-reconciliation-overview"></a><span data-ttu-id="20ebd-103">资源协调概述</span><span class="sxs-lookup"><span data-stu-id="20ebd-103">Resource reconciliation overview</span></span>

<span data-ttu-id="20ebd-104">_**适用于：** 基于资源/非库存场景的 Project Operations，精简部署 - 估价开票交易_</span><span class="sxs-lookup"><span data-stu-id="20ebd-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="20ebd-105">团队成员的预订和分派之间关系不紧密。</span><span class="sxs-lookup"><span data-stu-id="20ebd-105">For team members, bookings and assignments are loosely coupled.</span></span> <span data-ttu-id="20ebd-106">换句话说，资源可以有分派但无预订，也可以有预订但无分派。</span><span class="sxs-lookup"><span data-stu-id="20ebd-106">In other words, resources can have assignments but no bookings, or they can have bookings but no assignments.</span></span> <span data-ttu-id="20ebd-107">理想情况下，预订和分派应一致，这样资源就可以落实产能以执行任务分派。</span><span class="sxs-lookup"><span data-stu-id="20ebd-107">Ideally, bookings and assignments should be aligned, so that resources have committed capacity to perform the task assignments.</span></span> <span data-ttu-id="20ebd-108">但是，预订可能基于可用性，而任务的时间安排可能会随着项目的进行而改变。</span><span class="sxs-lookup"><span data-stu-id="20ebd-108">However, the bookings might be based on availability, and task timings might change as the project continues.</span></span> <span data-ttu-id="20ebd-109">因此，预订和分派之间的这种松散关系可以为您提供灵活的选择。</span><span class="sxs-lookup"><span data-stu-id="20ebd-109">Therefore, the loose coupling of bookings and assignments provides flexibility.</span></span>

<span data-ttu-id="20ebd-110">**项目** 窗体上的 **协调** 选项卡可供项目经理在项目团队中协调项目成员的预订及分派。</span><span class="sxs-lookup"><span data-stu-id="20ebd-110">The **Reconciliation** tab on the **Project** form lets project managers reconcile team members' bookings and their assignments for project teams.</span></span>

<span data-ttu-id="20ebd-111">**协调** 选项卡还显示深入到每个成员的单个任务分派级别的预订和分派。</span><span class="sxs-lookup"><span data-stu-id="20ebd-111">The **Reconciliation** tab also shows bookings and assignments down to the level of the individual task assignment for each team member.</span></span> <span data-ttu-id="20ebd-112">工时在单元格显示，表示从数月到数天的时间段。</span><span class="sxs-lookup"><span data-stu-id="20ebd-112">Hours are displayed in cells that represent time periods from months down to days.</span></span>

<span data-ttu-id="20ebd-113">此选项卡还使用 **总计** 列显示项目的整体净总额。</span><span class="sxs-lookup"><span data-stu-id="20ebd-113">The tab also shows an overall net total for the project, together with a **Total** column.</span></span>

<span data-ttu-id="20ebd-114">对于每个资源，此选项卡计算团队成员的预订与团队成员任务分派汇总之差。</span><span class="sxs-lookup"><span data-stu-id="20ebd-114">For each resource, the tab calculates the difference between the team member's bookings and a rollup of the team member's task assignments.</span></span> <span data-ttu-id="20ebd-115">理想情况下，此差应该为 0（零）。</span><span class="sxs-lookup"><span data-stu-id="20ebd-115">Ideally, this difference should be 0 (zero).</span></span> <span data-ttu-id="20ebd-116">换句话说，预订与分派之间应该无差额。</span><span class="sxs-lookup"><span data-stu-id="20ebd-116">In other words, there should be no difference between bookings and assignments.</span></span> <span data-ttu-id="20ebd-117">将为差额着色并添加阴影，以便您注意以下两种情况：</span><span class="sxs-lookup"><span data-stu-id="20ebd-117">Differences are colored and shaded to draw attention to two conditions:</span></span>

- <span data-ttu-id="20ebd-118">**预订不足** - 资源的分派比预订的多时，发生预订不足。</span><span class="sxs-lookup"><span data-stu-id="20ebd-118">**Booking shortage** – A booking shortage occurs when a resource has more assignments than bookings.</span></span> <span data-ttu-id="20ebd-119">因为尚未保留此产能，所以项目经理可能希望解决这个问题，方法是扩展资源的预订以弥补不足额。</span><span class="sxs-lookup"><span data-stu-id="20ebd-119">Because this capacity hasn't been reserved, a project manager might want to correct this condition by extending the resource's bookings to cover the deficit.</span></span>
- <span data-ttu-id="20ebd-120">**超出预订** – 当已经将某个资源预订给项目，但是尚未将其分派给任务时，发生超出预订。</span><span class="sxs-lookup"><span data-stu-id="20ebd-120">**Excess bookings** – Excess bookings occur when a resource has been booked to the project but hasn't been assigned to tasks.</span></span> <span data-ttu-id="20ebd-121">如果资源是在进行任务分派之前为项目预订的，则可以接受这种情况。</span><span class="sxs-lookup"><span data-stu-id="20ebd-121">This condition might be acceptable in the cases where the resource was booked to the project before task assignment occurred.</span></span> <span data-ttu-id="20ebd-122">但是，如果是其他情况，则不会计划把资源分派给任务。</span><span class="sxs-lookup"><span data-stu-id="20ebd-122">However, in other cases, the resource isn't planned to be assigned to tasks.</span></span> <span data-ttu-id="20ebd-123">在这些情况下，项目经理应该考虑取消资源的预订，以便将产能用于其他项目。</span><span class="sxs-lookup"><span data-stu-id="20ebd-123">In these cases, the project manager should consider canceling the resource's bookings, so that the capacity can be used for another project.</span></span>

<span data-ttu-id="20ebd-124">在某些情况下，在高于天的级别（如月级别）查看时间时，可能会发现资源的净差额为零（换句话说，预订 = 分派）。</span><span class="sxs-lookup"><span data-stu-id="20ebd-124">In some cases, when you view time at a higher level than the day level (for example, the month level), you might see a net difference of zero for a resource (in other words, bookings = assignments).</span></span> <span data-ttu-id="20ebd-125">但是，如果在周级别查看时间，可能会发现第一周的分派为零小时，预订为 40 小时，但是第二周的分派为 40 小时，预订为零小时。</span><span class="sxs-lookup"><span data-stu-id="20ebd-125">However, if you view time at the week level, you might see that there are assignments of zero hours and bookings of 40 hours in the first week, but assignments of 40 hours and bookings of zero hours in the second week.</span></span> <span data-ttu-id="20ebd-126">总体而言，已协调预订和分派，但是一周与下一周不同。</span><span class="sxs-lookup"><span data-stu-id="20ebd-126">Overall, the bookings and assignments are reconciled, but they differ from one week to the next.</span></span>

<span data-ttu-id="20ebd-127">在更高级别查看时间时， **协调** 选项卡中的单元格有一个指示器，用于说明较低级别存在差额。</span><span class="sxs-lookup"><span data-stu-id="20ebd-127">When you view time at higher levels, cells in the **Reconciliation** tab have an indicator to inform you that there are differences at lower levels.</span></span> <span data-ttu-id="20ebd-128">可通过在单元格中双击进行放大来查看差额。</span><span class="sxs-lookup"><span data-stu-id="20ebd-128">By double-clicking in a cell, you can zoom in to view the difference.</span></span> <span data-ttu-id="20ebd-129">然后可以右键单击进行缩小。通过选择资源，然后使用网格工具栏上的 **下一个差异** 控件，可以转到该资源的订阅与分派之间的下一个差额。</span><span class="sxs-lookup"><span data-stu-id="20ebd-129">You can then right-click to zoom out. By selecting a resource and then using the **Next difference** control on the grid toolbar, you can go to the next difference between bookings and assignments for that resource.</span></span> <span data-ttu-id="20ebd-130">然后可以使用 **上一个差异** 控件后退。</span><span class="sxs-lookup"><span data-stu-id="20ebd-130">You can then use the **Previous difference** control to go back.</span></span> <span data-ttu-id="20ebd-131">也可以在 **设置** 下关闭差额指示器和导航行为。</span><span class="sxs-lookup"><span data-stu-id="20ebd-131">You can also turn off the difference indicator and navigation behavior under **Settings**.</span></span>


<span data-ttu-id="20ebd-132">如果某个资源有任务分派，但是无预订，请在 **项目** 页的 **协调** 选项卡上选择预订不足，然后选择 **扩展预订** 。</span><span class="sxs-lookup"><span data-stu-id="20ebd-132">If you have task assignments for a resource but no bookings, on the **Projects** page, on the **Reconciliation** tab, select the booking shortage, and then select **Extend Booking**.</span></span> <span data-ttu-id="20ebd-133">将显示 **扩展预订** 对话框，其中显示需要来解决资源不足的预订。</span><span class="sxs-lookup"><span data-stu-id="20ebd-133">The **Extend Booking** dialog box appears and shows the booking that is needed to address the resource's shortage.</span></span> <span data-ttu-id="20ebd-134">还显示该资源在所有项目或其他可计划实体中的现有预订。</span><span class="sxs-lookup"><span data-stu-id="20ebd-134">It also shows the resource's existing bookings across all projects or other schedulable entities.</span></span> <span data-ttu-id="20ebd-135">如果选择 **确定** 为资源创建预订，无论该资源是否可用，都可能导致超额预订。</span><span class="sxs-lookup"><span data-stu-id="20ebd-135">If you select **OK** to create the booking for the resource, regardless of that resource's availability, you might cause overbooking.</span></span>

<span data-ttu-id="20ebd-136">然后，项目经理或资源经理可使用日程安排板管理资源超额预订超过其产能的任何情况。</span><span class="sxs-lookup"><span data-stu-id="20ebd-136">The project manager or resource manager can then use the Schedule Board to manage any situations where a resource is overbooked beyond its capacity.</span></span>

