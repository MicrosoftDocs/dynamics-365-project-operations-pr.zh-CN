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
# <a name="schedule-assistant-overview"></a><span data-ttu-id="2bd7d-103">日程安排助理概述</span><span class="sxs-lookup"><span data-stu-id="2bd7d-103">Schedule assistant overview</span></span>

<span data-ttu-id="2bd7d-104">_**适用于：** 基于资源/非库存场景的 Project Operations，精简部署 - 估价开票交易_</span><span class="sxs-lookup"><span data-stu-id="2bd7d-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="2bd7d-105">日程安排助理用于根据项目经理定义的要求来预订资源。</span><span class="sxs-lookup"><span data-stu-id="2bd7d-105">The Schedule assistant is used to book resources based on requirements defined by the Project manager.</span></span> <span data-ttu-id="2bd7d-106">日程安排助理依赖资源要求中提供的参数来查找资源。</span><span class="sxs-lookup"><span data-stu-id="2bd7d-106">The schedule assistant relies on the parameters provided in the resource requirement to find the resource.</span></span> <span data-ttu-id="2bd7d-107">日程安排助理建议符合相关要求的资源，如时间窗口或所需的技能。</span><span class="sxs-lookup"><span data-stu-id="2bd7d-107">The Schedule assistant recommends resources that match relevant requirements, like time windows or skills needed.</span></span>

<span data-ttu-id="2bd7d-108">在确定合适的资源后，资源经理或项目经理可以将资源预订到工作中。</span><span class="sxs-lookup"><span data-stu-id="2bd7d-108">After suitable resources are identified, the Resource or Project manager can book the resource to the work.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="2bd7d-109">先决条件</span><span class="sxs-lookup"><span data-stu-id="2bd7d-109">Prerequisites</span></span>

<span data-ttu-id="2bd7d-110">日程安排助理是 Universal Resource Scheduling 解决方案的一部分。</span><span class="sxs-lookup"><span data-stu-id="2bd7d-110">The Schedule assistant is a part of the Universal Resource Scheduling solution.</span></span> <span data-ttu-id="2bd7d-111">此解决方案通过 Dynamics 365 Project Operations、Dynamics 365 Field Service 和 Dynamics 365 Customer Service 提供和安装。</span><span class="sxs-lookup"><span data-stu-id="2bd7d-111">This solution is included and installed with Dynamics 365 Project Operations, Dynamics 365 Field Service, and Dynamics 365 Customer Service.</span></span>

## <a name="matching-requirements-and-resources"></a><span data-ttu-id="2bd7d-112">匹配要求与资源</span><span class="sxs-lookup"><span data-stu-id="2bd7d-112">Matching requirements and resources</span></span>

<span data-ttu-id="2bd7d-113">生成的资源要求基于如下详细信息：</span><span class="sxs-lookup"><span data-stu-id="2bd7d-113">A generated resource requirement is based on details such as:</span></span>

-   <span data-ttu-id="2bd7d-114">特征</span><span class="sxs-lookup"><span data-stu-id="2bd7d-114">Characteristics</span></span>
-   <span data-ttu-id="2bd7d-115">角色</span><span class="sxs-lookup"><span data-stu-id="2bd7d-115">Roles</span></span>
-   <span data-ttu-id="2bd7d-116">业务部门</span><span class="sxs-lookup"><span data-stu-id="2bd7d-116">Business units</span></span>
-   <span data-ttu-id="2bd7d-117">资源首选项</span><span class="sxs-lookup"><span data-stu-id="2bd7d-117">Resource preferences</span></span>
-   <span data-ttu-id="2bd7d-118">工作量信息</span><span class="sxs-lookup"><span data-stu-id="2bd7d-118">Effort contours</span></span>
-   <span data-ttu-id="2bd7d-119">时区</span><span class="sxs-lookup"><span data-stu-id="2bd7d-119">Time zone</span></span>

<span data-ttu-id="2bd7d-120">日程安排助理使用这些详细信息来筛选资源。</span><span class="sxs-lookup"><span data-stu-id="2bd7d-120">The Schedule assistant uses these details to filter resources.</span></span>

## <a name="launch-the-schedule-assistant"></a><span data-ttu-id="2bd7d-121">启动日程安排助理</span><span class="sxs-lookup"><span data-stu-id="2bd7d-121">Launch the Schedule assistant</span></span>

<span data-ttu-id="2bd7d-122">启动日程安排助理有两种方式。</span><span class="sxs-lookup"><span data-stu-id="2bd7d-122">There are two ways in which the schedule assistant is launched.</span></span> <span data-ttu-id="2bd7d-123">如果您使用的是混合模式，可以在团队成员网格中选择资源要求未满足的任何团队成员，然后选择**预订**。</span><span class="sxs-lookup"><span data-stu-id="2bd7d-123">If you're using the hybrid mode, in the team member grid you can select any team member with an unfulfilled resource requirement, and then select **Book**.</span></span> <span data-ttu-id="2bd7d-124">如果您使用的是集中模式，资源经理会查找并选择资源。</span><span class="sxs-lookup"><span data-stu-id="2bd7d-124">If you're using the central mode, the Resource manager finds and selects the resource.</span></span>

## <a name="schedule-assistant-filters"></a><span data-ttu-id="2bd7d-125">日程安排助理筛选器</span><span class="sxs-lookup"><span data-stu-id="2bd7d-125">Schedule assistant filters</span></span>

<span data-ttu-id="2bd7d-126">在日程安排助理运行后，资源要求的详细信息将在左侧窗格中显示为筛选值。</span><span class="sxs-lookup"><span data-stu-id="2bd7d-126">After the Schedule assistant runs, the details from the resource requirement are displayed as filtered values in the left pane.</span></span> <span data-ttu-id="2bd7d-127">资源经理或项目经理可以通过调整筛选器来调整结果以满足计划需求。</span><span class="sxs-lookup"><span data-stu-id="2bd7d-127">The Resource manager or the Project manager can fine-tune results by adjusting filters to meet the scheduling needs.</span></span>

<span data-ttu-id="2bd7d-128">筛选器窗格显示与工作相关的选项，其中包括：</span><span class="sxs-lookup"><span data-stu-id="2bd7d-128">The filter pane shows work-related options, including:</span></span>

-   <span data-ttu-id="2bd7d-129">工作开始和结束</span><span class="sxs-lookup"><span data-stu-id="2bd7d-129">Work start and end</span></span>
-   <span data-ttu-id="2bd7d-130">特征</span><span class="sxs-lookup"><span data-stu-id="2bd7d-130">Characteristics</span></span>
-   <span data-ttu-id="2bd7d-131">角色</span><span class="sxs-lookup"><span data-stu-id="2bd7d-131">Roles</span></span>
-   <span data-ttu-id="2bd7d-132">部门</span><span class="sxs-lookup"><span data-stu-id="2bd7d-132">Organizational units</span></span>
-   <span data-ttu-id="2bd7d-133">资源供给公司</span><span class="sxs-lookup"><span data-stu-id="2bd7d-133">Resourcing company</span></span>
-   <span data-ttu-id="2bd7d-134">资源类型</span><span class="sxs-lookup"><span data-stu-id="2bd7d-134">Resource types</span></span>
-   <span data-ttu-id="2bd7d-135">首选资源</span><span class="sxs-lookup"><span data-stu-id="2bd7d-135">Preferred resources</span></span>
