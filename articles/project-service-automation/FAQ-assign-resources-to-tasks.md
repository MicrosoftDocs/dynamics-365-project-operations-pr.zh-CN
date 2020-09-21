---
title: 为任务分派资源
description: 此主题介绍如何为任务分派资源。
author: ruhercul
manager: kfend
ms.service: business-applications
ms.custom:
- dyn365-projectservice
ms.date: 9/27/2019
ms.topic: article
ms.prod: Project Service
ms.technology: Dynamics 365 Project Service Automation 3.x
ms.assetid: 3ea9516c-0276-4e30-b308-f792f64d608b
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 509f7a4464b2e810900b31a78219ba696192a18b
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/24/2020
ms.locfileid: "3749806"
---
# <a name="assign-a-resource-to-a-task"></a><span data-ttu-id="cdc65-103">为任务分派资源</span><span class="sxs-lookup"><span data-stu-id="cdc65-103">Assign a resource to a task</span></span>

<span data-ttu-id="cdc65-104">在 Microsoft Dynamics 365 Project Service Automation 中可通过三种方法为任务分派资源。</span><span class="sxs-lookup"><span data-stu-id="cdc65-104">There are three ways to assign a resource to a task in Microsoft Dynamics 365 Project Service Automation.</span></span>

## <a name="book-a-resource-as-a-team-member-and-then-assign-the-resource-to-a-task"></a><span data-ttu-id="cdc65-105">作为团队成员预订资源，然后将资源分派给任务。</span><span class="sxs-lookup"><span data-stu-id="cdc65-105">Book a resource as a team member, and then assign the resource to a task</span></span>

<span data-ttu-id="cdc65-106">您可以将资源添加到项目团队，然后在项目计划中将资源分派给任务。</span><span class="sxs-lookup"><span data-stu-id="cdc65-106">You can add a resource to the project team, and then assign the resource to tasks in the project schedule.</span></span>

1. <span data-ttu-id="cdc65-107">在**团队成员**选项卡中，通过选中**新建**添加新团队成员。</span><span class="sxs-lookup"><span data-stu-id="cdc65-107">On the **Team Member** tab, add a new team member by selecting **New**.</span></span> 

2. <span data-ttu-id="cdc65-108">将打开**团队成员快速创建**面板，在这里您可以选择可预订资源名称并设置角色。</span><span class="sxs-lookup"><span data-stu-id="cdc65-108">The **Team Member Quick Create** panel opens, where you can select the bookable resource name and set a role.</span></span> 

    <span data-ttu-id="cdc65-109">为资源的预订选择以下分配方法之一：</span><span class="sxs-lookup"><span data-stu-id="cdc65-109">Select one of the following allocation methods for the resource’s booking:</span></span>

    - <span data-ttu-id="cdc65-110">**完全产能**为指定的起始日期和截止日期预订资源的完全产能。</span><span class="sxs-lookup"><span data-stu-id="cdc65-110">**Full Capacity** books the resource’s full capacity for the specified from and to dates.</span></span>
    - <span data-ttu-id="cdc65-111">**产能百分比**为指定的起始日期和截止日期预订资源产能的百分比。</span><span class="sxs-lookup"><span data-stu-id="cdc65-111">**Percentage Capacity** books the resource for a percentage of the resource's capacity for the specified from and to dates.</span></span>
    - <span data-ttu-id="cdc65-112">**按时数平均分配**预订资源指定的小时数，根据指定的起始日期/截止日期按天平均分配时间。</span><span class="sxs-lookup"><span data-stu-id="cdc65-112">**By Hours Distribute Evenly** books the resource for a specified number of hours, distributing them evenly per day over the specified from and to dates.</span></span>
    - <span data-ttu-id="cdc65-113">**按时数前期负荷**预订资源指定的小时数，根据指定的起始日期和截止日期前期负荷每天的时间。</span><span class="sxs-lookup"><span data-stu-id="cdc65-113">**By Hours Front Load** books the resource for a specified number of hours, front-loading the per-day hours over the specified from and to dates.</span></span>
    - <span data-ttu-id="cdc65-114">**无**将资源添加到团队，但不创建任何分配其产能的预订。</span><span class="sxs-lookup"><span data-stu-id="cdc65-114">**None** adds the resource to the team but doesn’t create any bookings that absorb their capacity.</span></span>

3. <span data-ttu-id="cdc65-115">在任务的**日程安排**网格上，选择资源单元格中的**资源**图标，然后在**团队成员**下选择您刚才添加的团队成员。</span><span class="sxs-lookup"><span data-stu-id="cdc65-115">On the **Schedule** grid for a task, select the **Resource** icon in the resource cell, and then under **Team Members**, select the team member you just added.</span></span> 

> [!NOTE]
> <span data-ttu-id="cdc65-116">在**团队成员**选项卡和**协调**选项卡上，资源均显示已预订工时数和已分派工时数。</span><span class="sxs-lookup"><span data-stu-id="cdc65-116">On the **Team Member** and **Reconciliation** tabs, the resource shows booked and assigned hours.</span></span> <span data-ttu-id="cdc65-117">这些工时数应该相同，但不必一定如此，因为预订和分派不是紧密结合的。</span><span class="sxs-lookup"><span data-stu-id="cdc65-117">The hours should be the same, but it isn't required as bookings and assignments are not tightly coupled.</span></span> <span data-ttu-id="cdc65-118">**协调**选项卡为您提供它们不同时的详细信息，例如，当您向资源分派的工时数多于已预订工时数时。</span><span class="sxs-lookup"><span data-stu-id="cdc65-118">The **Reconciliation** tab gives you details when they are different, such as when you assign a resource more hours than you have booked.</span></span> <span data-ttu-id="cdc65-119">如果需要，您可以通过扩展资源的预订或更改分派来更正信息。</span><span class="sxs-lookup"><span data-stu-id="cdc65-119">If needed, you can correct the information by extending the resource's bookings or changing the assignment.</span></span>

## <a name="create-a-generic-team-member-through-task-assignment"></a><span data-ttu-id="cdc65-120">通过任务分派创建通用团队成员</span><span class="sxs-lookup"><span data-stu-id="cdc65-120">Create a generic team member through task assignment</span></span>

<span data-ttu-id="cdc65-121">通过任务分派创建通用团队成员时，创建描述指定资源（您最终希望处理任务的资源）的特征的占位符或通用资源。</span><span class="sxs-lookup"><span data-stu-id="cdc65-121">When you create a generic team member through task assignment, you create a placeholder or generic resource that describes the characteristics of the named resource you ultimately want to work on the tasks.</span></span> <span data-ttu-id="cdc65-122">然后，您生成一个用于搜索和预订指定资源的要求（或使用此要求提交请求）。</span><span class="sxs-lookup"><span data-stu-id="cdc65-122">You then generate a requirement (or submit a request using the requirement) that is used to search for and book the named resource.</span></span>

1. <span data-ttu-id="cdc65-123">在任务的**日程安排**网格上，选择资源单元格中的**资源**图标。</span><span class="sxs-lookup"><span data-stu-id="cdc65-123">On the **Schedule** grid for a task, select the **Resource** icon in the resource cell.</span></span>

2. <span data-ttu-id="cdc65-124">键入名称用作占位符资源的名称。</span><span class="sxs-lookup"><span data-stu-id="cdc65-124">Type a name to serve as the placeholder resource’s name.</span></span> <span data-ttu-id="cdc65-125">例如，“项目经理”。</span><span class="sxs-lookup"><span data-stu-id="cdc65-125">For example, Program Manager.</span></span>

3. <span data-ttu-id="cdc65-126">选择**创建**，然后**快速创建项目团队成员**字段中，为通用资源设置角色。</span><span class="sxs-lookup"><span data-stu-id="cdc65-126">Select **Create**, and in the **Quick Create Project Team Member** field, set the role for the generic resource.</span></span>

4. <span data-ttu-id="cdc65-127">您可以通过在任务的**资源选择器**上选择资源来继续将任务分派给此占位符资源。</span><span class="sxs-lookup"><span data-stu-id="cdc65-127">You can continue to assign tasks to this placeholder resource by selecting the resource on the **Resource Selector** for the task.</span></span> <span data-ttu-id="cdc65-128">它们在**团队成员**下列出。</span><span class="sxs-lookup"><span data-stu-id="cdc65-128">They’re listed under **Team Members**.</span></span>

5. <span data-ttu-id="cdc65-129">在分派通用资源后，在**团队**选项卡上选择通用资源，然后选择**生成要求**为该通用资源创建资源要求。</span><span class="sxs-lookup"><span data-stu-id="cdc65-129">When you’re done assigning the generic resource, select the generic resource on the **Team** tab, and then select **Generate Requirement** to create a resource requirement for the generic resource.</span></span>

6. <span data-ttu-id="cdc65-130">为通用资源选择**预订**。</span><span class="sxs-lookup"><span data-stu-id="cdc65-130">Select **Book** for the generic resource.</span></span> <span data-ttu-id="cdc65-131">然后，您可以使用日程安排板查找和预订实际资源。</span><span class="sxs-lookup"><span data-stu-id="cdc65-131">You can then use the Schedule board to find and book a real resource.</span></span> <span data-ttu-id="cdc65-132">您还可以提交由资源经理满足的要求。</span><span class="sxs-lookup"><span data-stu-id="cdc65-132">You can also submit the requirement for fulfillment by a resource manager.</span></span>

7. <span data-ttu-id="cdc65-133">在通用资源要求由指定资源满足时，通用资源将被从团队中移除，通用资源的任务分派将被分派到满足通用资源的资源要求的指定资源。</span><span class="sxs-lookup"><span data-stu-id="cdc65-133">When the generic resource is fulfilled with a named resource, the generic resource is removed from the team and the task assignments for the generic resource are assigned to the named resource that fulfilled the generic resource’s resource requirement.</span></span>

## <a name="assign-a-named-resource-from-the-list-of-all-bookable-resources"></a><span data-ttu-id="cdc65-134">从所有可预订资源列表分派指定资源</span><span class="sxs-lookup"><span data-stu-id="cdc65-134">Assign a named resource from the list of all bookable resources</span></span>

<span data-ttu-id="cdc65-135">您可以在**资源选择器**中使用搜索框来搜索所有可预订资源，然后将其分派给任务。</span><span class="sxs-lookup"><span data-stu-id="cdc65-135">You can use the search box in the **Resource Selector** to search all bookable resources and assign them to a task.</span></span>

<span data-ttu-id="cdc65-136">将把按照这种方法分派的资源添加到无任何预订的团队。</span><span class="sxs-lookup"><span data-stu-id="cdc65-136">Resources assigned this way are added to the team without any bookings.</span></span> <span data-ttu-id="cdc65-137">这类似添加团队成员并选择“无”作为分配方法。</span><span class="sxs-lookup"><span data-stu-id="cdc65-137">This is similar to adding a team member and selecting None as the allocation method.</span></span> <span data-ttu-id="cdc65-138">资源在**团队**和**协调**选项卡中显示为资源，仅分派和预订不足。</span><span class="sxs-lookup"><span data-stu-id="cdc65-138">The resource is displayed in the **Team** and **Reconciliation** tabs as resources with only assignments and a booking deficit.</span></span> <span data-ttu-id="cdc65-139">如果您要使用其可用性，请预订这些资源。</span><span class="sxs-lookup"><span data-stu-id="cdc65-139">Book them if you want to use their availability.</span></span>

1. <span data-ttu-id="cdc65-140">在任务的**日程安排**网格上，选择资源单元格中的**资源**图标。</span><span class="sxs-lookup"><span data-stu-id="cdc65-140">On the **Schedule** grid for a task, select the **Resource** icon in the resource cell.</span></span>

2. <span data-ttu-id="cdc65-141">开始键入名称。</span><span class="sxs-lookup"><span data-stu-id="cdc65-141">Start typing a name.</span></span> <span data-ttu-id="cdc65-142">名称的搜索结果显示在**资源选择器**中**其他资源**下。</span><span class="sxs-lookup"><span data-stu-id="cdc65-142">The search results for the name are displayed in the **Resource Selector** under **Other Resources**.</span></span>

3. <span data-ttu-id="cdc65-143">选择要分派给任务的资源。</span><span class="sxs-lookup"><span data-stu-id="cdc65-143">Select the resource that you want to assign to the task.</span></span>

