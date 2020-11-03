---
title: 从日程安排板创建项目预订
description: 此主题介绍如何从日程安排板创建项目预订。
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 9/26/2019
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
ms.openlocfilehash: 57fbc71681015fca73cdda4bc7d392f6be4289f3
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/16/2020
ms.locfileid: "4072621"
---
# <a name="create-a-project-booking-from-the-schedule-board"></a><span data-ttu-id="c67fd-103">从日程安排板创建项目预订</span><span class="sxs-lookup"><span data-stu-id="c67fd-103">Create a project booking from the Schedule board</span></span>

<span data-ttu-id="c67fd-104">您可以直接在项目的 **团队** 选项卡上，或通过从通用团队成员分派生成资源要求，然后使用项目团队成员来满足生成的要求，来将资源预订到项目。</span><span class="sxs-lookup"><span data-stu-id="c67fd-104">You can book a resource onto a project directly from the **Team** tab of the project or by generating a resource requirement from a generic team member assignment and then fulfilling the generated requirement with a project team member.</span></span>

<span data-ttu-id="c67fd-105">您还可以直接从日程安排板将资源预订到项目。</span><span class="sxs-lookup"><span data-stu-id="c67fd-105">You can also book a resource onto a project directly from the Schedule board.</span></span> <span data-ttu-id="c67fd-106">可通过三种方法执行此操作：</span><span class="sxs-lookup"><span data-stu-id="c67fd-106">There are three ways to do this:</span></span>

- <span data-ttu-id="c67fd-107">**从已生成的资源要求预订：** 可以在创建通用资源并在项目内分派任务之后生成资源要求。</span><span class="sxs-lookup"><span data-stu-id="c67fd-107">**Book from a generated resource requirement:** You can generate a resource requirement after you create a generic resource and assign tasks within a project.</span></span>

- <span data-ttu-id="c67fd-108">**从主要要求预订：** 主要要求在日程安排板的 **项目** 选项卡中显示。</span><span class="sxs-lookup"><span data-stu-id="c67fd-108">**Book from the primary requirement:** The primary requirements show up on the Schedule board on the **Project** tab.</span></span> 

- <span data-ttu-id="c67fd-109">**从新资源要求预订：** 可以从头开始创建资源要求并将其与项目关联。</span><span class="sxs-lookup"><span data-stu-id="c67fd-109">**Book from a new resource requirement:** You can create a resource requirement from scratch and associate it with a project.</span></span> <span data-ttu-id="c67fd-110">在日程安排板上，此资源要求显示在 **未解决的要求** 选项卡上。</span><span class="sxs-lookup"><span data-stu-id="c67fd-110">On the Schedule board, the resource requirement shows up on the **Open Requirements** tab.</span></span>

## <a name="book-from-a-generated-resource-requirement"></a><span data-ttu-id="c67fd-111">从已生成的资源要求预订</span><span class="sxs-lookup"><span data-stu-id="c67fd-111">Book from a generated resource requirement</span></span>

<span data-ttu-id="c67fd-112">您可以在项目内创建通用资源并向其分派一项或多项任务。</span><span class="sxs-lookup"><span data-stu-id="c67fd-112">You can create a generic resource and assign it one or more tasks within a project.</span></span> <span data-ttu-id="c67fd-113">然后，您可以从通用团队成员生成资源要求。</span><span class="sxs-lookup"><span data-stu-id="c67fd-113">Then you can generate a resource requirement from the generic team member.</span></span> 

1.  <span data-ttu-id="c67fd-114">在日程安排板上，此资源将显示在 **未解决的要求** 选项卡上。如果您有很多未解决的要求，您可能需要在网格上使用列筛选器。</span><span class="sxs-lookup"><span data-stu-id="c67fd-114">On the Schedule board, this resource will show up on the **Open Requirements** tab. You might need to use column filters on the grid if you have many open requirements.</span></span> 

    <span data-ttu-id="c67fd-115">![日程安排板上的“未解决的要求”选项卡](media/FAQ-Project-Booking-Schedule-Board-1.png "预订和分派表的屏幕截图")</span><span class="sxs-lookup"><span data-stu-id="c67fd-115">![Open Requirements tab on the Schedule board](media/FAQ-Project-Booking-Schedule-Board-1.png "Screenshot of bookings and assignments table")</span></span>

2. <span data-ttu-id="c67fd-116">选择此要求。</span><span class="sxs-lookup"><span data-stu-id="c67fd-116">Select the requirement.</span></span> <span data-ttu-id="c67fd-117">**查找可用性** 选项卡将显示在所选行的顶部。</span><span class="sxs-lookup"><span data-stu-id="c67fd-117">The **Find Availability** tab will appear at the top of the selected row.</span></span>
 
3. <span data-ttu-id="c67fd-118">选择此选项卡时，将打开日程安排板的日程安排助理模式，然后筛选满足资源要求的可用资源。</span><span class="sxs-lookup"><span data-stu-id="c67fd-118">When you select the tab, the Schedule Assistant mode of the Schedule board opens and then filters the available resources that meet the resource requirement.</span></span> <span data-ttu-id="c67fd-119">之后，可以预订资源。</span><span class="sxs-lookup"><span data-stu-id="c67fd-119">After that, you can book a resource.</span></span>

4. <span data-ttu-id="c67fd-120">您还可以将选定行从日程安排的底部拖放到上面网格中的资源单元格中。</span><span class="sxs-lookup"><span data-stu-id="c67fd-120">You can also drag and drop the selected row from the bottom of the Schedule board to a resource cell in the grid above.</span></span> <span data-ttu-id="c67fd-121">当您放下要求时，它将在右侧打开 **创建资源预订** 面板。</span><span class="sxs-lookup"><span data-stu-id="c67fd-121">When you drop it, it opens the **Create Resource Booking** panel on the right.</span></span>

    <span data-ttu-id="c67fd-122">选择 **预订** 将资源预订到项目团队中。</span><span class="sxs-lookup"><span data-stu-id="c67fd-122">Selecting **Book** books the resource onto the project team.</span></span>

![“创建资源预订”面板](media/FAQ-Project-Booking-Schedule-Board-6.png "")
 

## <a name="book-from-the-primary-requirement"></a><span data-ttu-id="c67fd-124">从主要要求预订</span><span class="sxs-lookup"><span data-stu-id="c67fd-124">Book from the Primary Requirement</span></span>

<span data-ttu-id="c67fd-125">在 Project Service 中创建项目将自动创建名为“主要要求”的资源要求。</span><span class="sxs-lookup"><span data-stu-id="c67fd-125">Creating a project in Project Service automatically creates a resource requirement called the Primary Requirement.</span></span> <span data-ttu-id="c67fd-126">这是用于通过日程安排板快速预订资源的空要求，既不生成要求，也不从头创建要求。</span><span class="sxs-lookup"><span data-stu-id="c67fd-126">This is an empty requirement that is used to quickly book a resource with the Schedule board without generating a requirement or creating one from scratch.</span></span> <span data-ttu-id="c67fd-127">由于要求是空的，您将需要指定日期以及分配方法和时数（如果适用）。</span><span class="sxs-lookup"><span data-stu-id="c67fd-127">Because the requirement is empty, you’ll need to specify dates as well as the allocation method and hours, if applicable.</span></span> 

1. <span data-ttu-id="c67fd-128">若要使用“主要要求”预订资源，在日程安排板上选择 **项目** 选项卡。如果您有很多项目，您可能需要使用 **项目** 列的列筛选器。</span><span class="sxs-lookup"><span data-stu-id="c67fd-128">To book a resource with the Primary Requirement, on the Schedule board, select the **Project** tab. You might need to use the column filter on the **Project** column if you have many projects.</span></span>

   <span data-ttu-id="c67fd-129">![日程安排板上的列筛选器](media/FAQ-Project-Booking-Schedule-Board-2.png "预订和分派表的屏幕截图")</span><span class="sxs-lookup"><span data-stu-id="c67fd-129">![Column filters on the Schedule board](media/FAQ-Project-Booking-Schedule-Board-2.png "Screenshot of bookings and assignments table")</span></span>

2. <span data-ttu-id="c67fd-130">选择仅将项目名称作为其名称且持续时间为零 (0) 的要求。</span><span class="sxs-lookup"><span data-stu-id="c67fd-130">Select the requirement that only has the project name as its name and has a duration of zero (0).</span></span>

3. <span data-ttu-id="c67fd-131">选择行上显示的 **查找可用性** 选项卡。</span><span class="sxs-lookup"><span data-stu-id="c67fd-131">Select the **Find Availability** tab that appears on the row.</span></span> <span data-ttu-id="c67fd-132">这会让日程安排板进入“日程安排助理模式”，并显示可以预订到项目的可用资源。</span><span class="sxs-lookup"><span data-stu-id="c67fd-132">This puts the Schedule board in Schedule Assistant mode and shows the available resources that can be booked onto the project.</span></span>

4. <span data-ttu-id="c67fd-133">由于 **主要要求** 是持续时间为零 (0) 的空要求，您需要在选择和预订资源时在 **创建资源预订** 面板上设置持续时间。</span><span class="sxs-lookup"><span data-stu-id="c67fd-133">Because a **Primary Requirement** is an empty requirement with zero (0) duration, you’ll need to set the duration on the **Create Resource Booking** panel when selecting and booking a resource.</span></span>

5. <span data-ttu-id="c67fd-134">您还可以在日程安排板底部选择 **项目主要要求** ，并将其拖放到资源上以进行预订。</span><span class="sxs-lookup"><span data-stu-id="c67fd-134">You can also select the **Project Primary Requirement** at the bottom of the Schedule board and drag and drop it on a resource to book it.</span></span>
 
    <span data-ttu-id="c67fd-135">由于 **主要要求** 是持续时间为零 (0) 的空要求，所以您需要在选择和预订资源时在 **创建资源预订** 面板上设置持续时间。</span><span class="sxs-lookup"><span data-stu-id="c67fd-135">Because the **Primary Requirement** is an empty requirement that has zero (0) duration, you’ll need to set the duration on the **Create Resource Booking** panel when you select and book a resource.</span></span>
 
    <span data-ttu-id="c67fd-136">在通过日程安排板上的 **主要要求** 预订资源时，您将其添加到项目团队，而无需进行任何分派。</span><span class="sxs-lookup"><span data-stu-id="c67fd-136">When you book a resource through the **Primary Requirement** on the Schedule board, you add it to the project team without any assignments.</span></span>
 
## <a name="book-from-a-new-resource-requirement"></a><span data-ttu-id="c67fd-137">从新资源要求预订</span><span class="sxs-lookup"><span data-stu-id="c67fd-137">Book from a new resource requirement</span></span>
<span data-ttu-id="c67fd-138">完成以下步骤从新资源要求预订。</span><span class="sxs-lookup"><span data-stu-id="c67fd-138">Complete the following steps to book from a new resource requirement.</span></span> 

1. <span data-ttu-id="c67fd-139">转到 **资源要求** ，然后选择 **新建** 创建新的资源要求。</span><span class="sxs-lookup"><span data-stu-id="c67fd-139">Go to **Resource Requirements** , and then select **New** to create a new resource requirement.</span></span>

2. <span data-ttu-id="c67fd-140">在 **项目** 选项卡上，选择一个项目以关联该项目的要求。</span><span class="sxs-lookup"><span data-stu-id="c67fd-140">On the **Project** tab, select a project to associate the requirement to the project.</span></span>
 
    <span data-ttu-id="c67fd-141">在日程安排上，这个新要求显示为您可以满足的 **未解决的要求** 。</span><span class="sxs-lookup"><span data-stu-id="c67fd-141">On the Schedule board, this new requirement shows as an **Open Requirement** that you can fulfill.</span></span>

3. <span data-ttu-id="c67fd-142">预订资源以将其添加到项目团队。</span><span class="sxs-lookup"><span data-stu-id="c67fd-142">Book the resource to add it to the project team.</span></span>

4. <span data-ttu-id="c67fd-143">现在资源已经预订，您必须手动分派任务。</span><span class="sxs-lookup"><span data-stu-id="c67fd-143">Now that the resource is booked, you must assign tasks manually.</span></span>

