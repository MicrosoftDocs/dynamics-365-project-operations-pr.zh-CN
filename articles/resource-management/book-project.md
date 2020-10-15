---
title: 项目预订
description: 本主题提供有关为项目预订资源的信息。
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 19128264ed3db7efeeba948155f0ddbdc806c2a0
ms.sourcegitcommit: 56c42d7f5995a674426a1c2a81bae897dceb391c
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/01/2020
ms.locfileid: "3907931"
---
# <a name="book-to-a-project"></a><span data-ttu-id="94321-103">项目预订</span><span class="sxs-lookup"><span data-stu-id="94321-103">Book to a project</span></span>

<span data-ttu-id="94321-104">_**适用于：** 基于资源/非库存场景的 Project Operations，精简部署 - 估价开票交易_</span><span class="sxs-lookup"><span data-stu-id="94321-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="94321-105">有时，项目经理或资源经理需要在没有为通用团队成员定义特定要求的情况下为项目分配资源。</span><span class="sxs-lookup"><span data-stu-id="94321-105">There are times where a Project manager or Resource manager will need to allocate a resource to project without a specific requirement being defined from a generic team member.</span></span> <span data-ttu-id="94321-106">这可以通过以下三种方式之一来实现。</span><span class="sxs-lookup"><span data-stu-id="94321-106">This can be achieved in one of three ways.</span></span>

- <span data-ttu-id="94321-107">从团队成员网格预订</span><span class="sxs-lookup"><span data-stu-id="94321-107">Book from the team member grid</span></span>
- <span data-ttu-id="94321-108">从日程安排板预订</span><span class="sxs-lookup"><span data-stu-id="94321-108">Book from the schedule board</span></span>
- <span data-ttu-id="94321-109">从**项目**窗体预订</span><span class="sxs-lookup"><span data-stu-id="94321-109">Book from the **Project** form</span></span>

## <a name="book-from-the-team-member-grid"></a><span data-ttu-id="94321-110">从团队成员网格预订</span><span class="sxs-lookup"><span data-stu-id="94321-110">Book from the team member grid</span></span>

<span data-ttu-id="94321-111">如果您的组织在混合资源分配模式下运行，项目经理可以通过完成以下步骤将资源直接预订到项目。</span><span class="sxs-lookup"><span data-stu-id="94321-111">If your organization is operating in hybrid Resource allocation mode, the Project manager can book a resource directly to the project by completing the following steps.</span></span>

1. <span data-ttu-id="94321-112">在项目中，转到团队成员网格，选择**新建**。</span><span class="sxs-lookup"><span data-stu-id="94321-112">From the project, go to the team member grid and select **New**.</span></span>
2. <span data-ttu-id="94321-113">定义资源的职位名称和角色。</span><span class="sxs-lookup"><span data-stu-id="94321-113">Define the position name and the role of the resource.</span></span>
3. <span data-ttu-id="94321-114">从可用查找中选择可预订资源。</span><span class="sxs-lookup"><span data-stu-id="94321-114">Select the bookable resource from the available lookup.</span></span>
4. <span data-ttu-id="94321-115">选择资源后，定义以下字段信息来预订资源：</span><span class="sxs-lookup"><span data-stu-id="94321-115">After you select the resource, define the following field information to book the resource:</span></span>

    - <span data-ttu-id="94321-116">开始日期</span><span class="sxs-lookup"><span data-stu-id="94321-116">Start date</span></span>
    - <span data-ttu-id="94321-117">完成日期</span><span class="sxs-lookup"><span data-stu-id="94321-117">Finish date</span></span>
    - <span data-ttu-id="94321-118">分派方法</span><span class="sxs-lookup"><span data-stu-id="94321-118">Allocation method</span></span>
    - <span data-ttu-id="94321-119">工时（如果适用）</span><span class="sxs-lookup"><span data-stu-id="94321-119">Hours, if applicable</span></span>
    - <span data-ttu-id="94321-120">项目审批者</span><span class="sxs-lookup"><span data-stu-id="94321-120">Project approver</span></span>

6. <span data-ttu-id="94321-121">选择**保存并关闭**</span><span class="sxs-lookup"><span data-stu-id="94321-121">Select **Save and Close**</span></span>

## <a name="book-from-the-schedule-board"></a><span data-ttu-id="94321-122">从日程安排板预订</span><span class="sxs-lookup"><span data-stu-id="94321-122">Book from the schedule board</span></span>

<span data-ttu-id="94321-123">当资源经理需要直接将资源预订到项目时，他们可以使用日程安排板和项目要求。</span><span class="sxs-lookup"><span data-stu-id="94321-123">When a Resource manager needs to book a resource directly to a project, they can use the schedule board and the project requirement.</span></span> <span data-ttu-id="94321-124">项目要求是一项资源要求，可以一直作为预订依据。</span><span class="sxs-lookup"><span data-stu-id="94321-124">The project requirement is a resource requirement that is always available to be booked against.</span></span> <span data-ttu-id="94321-125">要从日程安排板直接预订到项目，请完成以下步骤。</span><span class="sxs-lookup"><span data-stu-id="94321-125">To book directly to a project form the schedule board, complete the following steps.</span></span>

1. <span data-ttu-id="94321-126">导航到日程安排板，在左侧页面上，筛选您为要求考虑的资源。</span><span class="sxs-lookup"><span data-stu-id="94321-126">Navigate to the schedule board and on the left page, filter for the resources you are considering for the requirement.</span></span>
2. <span data-ttu-id="94321-127">在底部窗格中，选择**项目**选项卡查看项目要求列表。</span><span class="sxs-lookup"><span data-stu-id="94321-127">In the bottom pane, select the **Project** tab to view a list of project requirements.</span></span>
3. <span data-ttu-id="94321-128">将要求拖到资源上并定义下列信息：</span><span class="sxs-lookup"><span data-stu-id="94321-128">Drag the requirement onto a resource and define the following information:</span></span>

    - <span data-ttu-id="94321-129">开始日期</span><span class="sxs-lookup"><span data-stu-id="94321-129">Start date</span></span>
    - <span data-ttu-id="94321-130">完成日期</span><span class="sxs-lookup"><span data-stu-id="94321-130">Finish date</span></span>
    - <span data-ttu-id="94321-131">预订状态</span><span class="sxs-lookup"><span data-stu-id="94321-131">Booking status</span></span>
    - <span data-ttu-id="94321-132">预订方法</span><span class="sxs-lookup"><span data-stu-id="94321-132">Booking method</span></span>
    - <span data-ttu-id="94321-133">持续时间</span><span class="sxs-lookup"><span data-stu-id="94321-133">Duration</span></span>

## <a name="book-from-the-project-form"></a><span data-ttu-id="94321-134">从“项目”窗体预订</span><span class="sxs-lookup"><span data-stu-id="94321-134">Book from the Project form</span></span>

<span data-ttu-id="94321-135">作为项目经理，您可能需要将资源预订到项目，但只知道条件，不知道资源姓名。</span><span class="sxs-lookup"><span data-stu-id="94321-135">As a Project manager, you might need to book a resource to a project, but only know the criteria rather than the name of the resource.</span></span> <span data-ttu-id="94321-136">完成以下步骤来使用日程安排助理根据资源的任何可用属性来查找资源。</span><span class="sxs-lookup"><span data-stu-id="94321-136">Complete the following steps to use the schedule assistant to find a resource based on any available attributes of the resource.</span></span> 

1. <span data-ttu-id="94321-137">导航到项目，选择**预订**打开日程安排助理。</span><span class="sxs-lookup"><span data-stu-id="94321-137">Navigate to the project and select **Book** to open the Schedule Assistant.</span></span>
2. <span data-ttu-id="94321-138">使用日程安排助理左侧的筛选器，精简条件，然后选择**搜索**。</span><span class="sxs-lookup"><span data-stu-id="94321-138">Using the filters on the left side of the Schedule Assistant, narrow the criteria and select **Search.**</span></span>
3. <span data-ttu-id="94321-139">根据结果中返回的资源，您可以预订资源。</span><span class="sxs-lookup"><span data-stu-id="94321-139">Based on resources returned in the results, you can book a resource.</span></span>

> [!NOTE]
> <span data-ttu-id="94321-140">此方法不会为资源创建任何预订。</span><span class="sxs-lookup"><span data-stu-id="94321-140">This method doesn't create any bookings for the resource.</span></span> <span data-ttu-id="94321-141">而是将资源添加到团队。</span><span class="sxs-lookup"><span data-stu-id="94321-141">Instead, it adds the resource to the team.</span></span> <span data-ttu-id="94321-142">在将团队成员添加到项目之后，项目经理可以使用维护预订或扩展预订将所需预订添加到资源。</span><span class="sxs-lookup"><span data-stu-id="94321-142">After the team member has been added to the project, the project manager can use maintain bookings or extend bookings to add the required bookings to the resource.</span></span>
