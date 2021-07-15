---
title: 日程安排助理概述
description: 此主题提供有关使用日程安排助理预订资源的信息。
author: ruhercul
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: kfend
ms.author: ruhercul
ms.custom: intro-internal
ms.openlocfilehash: 83583c97e4ecb5f1fdc0d8d98098afe8e12d27e4
ms.sourcegitcommit: 0fafe022731f0e1e8693382ff906e3f8541d34ca
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 07/07/2021
ms.locfileid: "6368105"
---
# <a name="schedule-assistant-overview"></a><span data-ttu-id="8cddc-103">日程安排助理概述</span><span class="sxs-lookup"><span data-stu-id="8cddc-103">Schedule assistant overview</span></span>

<span data-ttu-id="8cddc-104">_**适用于：** 基于资源/非库存场景的 Project Operations，精简部署 - 估价开票交易_</span><span class="sxs-lookup"><span data-stu-id="8cddc-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="8cddc-105">日程安排助理用于根据项目经理定义的要求来预订资源。</span><span class="sxs-lookup"><span data-stu-id="8cddc-105">The Schedule assistant is used to book resources based on requirements defined by the Project manager.</span></span> <span data-ttu-id="8cddc-106">日程安排助理依赖资源要求中提供的参数来查找资源。</span><span class="sxs-lookup"><span data-stu-id="8cddc-106">The schedule assistant relies on the parameters provided in the resource requirement to find the resource.</span></span> <span data-ttu-id="8cddc-107">日程安排助理建议符合相关要求的资源，如时间窗口或所需的技能。</span><span class="sxs-lookup"><span data-stu-id="8cddc-107">The Schedule assistant recommends resources that match relevant requirements, like time windows or skills needed.</span></span>

<span data-ttu-id="8cddc-108">在确定合适的资源后，资源经理或项目经理可以将资源预订到工作中。</span><span class="sxs-lookup"><span data-stu-id="8cddc-108">After suitable resources are identified, the Resource or Project manager can book the resource to the work.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="8cddc-109">先决条件</span><span class="sxs-lookup"><span data-stu-id="8cddc-109">Prerequisites</span></span>

<span data-ttu-id="8cddc-110">日程安排助理是 Universal Resource Scheduling 解决方案的一部分。</span><span class="sxs-lookup"><span data-stu-id="8cddc-110">The Schedule assistant is a part of the Universal Resource Scheduling solution.</span></span> <span data-ttu-id="8cddc-111">此解决方案随附于 Dynamics 365 Project Operations、Dynamics 365 Field Service 和 Dynamics 365 Customer Service 并与其一起安装。</span><span class="sxs-lookup"><span data-stu-id="8cddc-111">This solution is included and installed with Dynamics 365 Project Operations, Dynamics 365 Field Service, and Dynamics 365 Customer Service.</span></span>

## <a name="matching-requirements-and-resources"></a><span data-ttu-id="8cddc-112">匹配要求与资源</span><span class="sxs-lookup"><span data-stu-id="8cddc-112">Matching requirements and resources</span></span>

<span data-ttu-id="8cddc-113">生成的资源要求基于如下详细信息：</span><span class="sxs-lookup"><span data-stu-id="8cddc-113">A generated resource requirement is based on details such as:</span></span>

-   <span data-ttu-id="8cddc-114">特征</span><span class="sxs-lookup"><span data-stu-id="8cddc-114">Characteristics</span></span>
-   <span data-ttu-id="8cddc-115">角色</span><span class="sxs-lookup"><span data-stu-id="8cddc-115">Roles</span></span>
-   <span data-ttu-id="8cddc-116">业务部门</span><span class="sxs-lookup"><span data-stu-id="8cddc-116">Business units</span></span>
-   <span data-ttu-id="8cddc-117">资源首选项</span><span class="sxs-lookup"><span data-stu-id="8cddc-117">Resource preferences</span></span>
-   <span data-ttu-id="8cddc-118">工作量信息</span><span class="sxs-lookup"><span data-stu-id="8cddc-118">Effort contours</span></span>
-   <span data-ttu-id="8cddc-119">时区</span><span class="sxs-lookup"><span data-stu-id="8cddc-119">Time zone</span></span>

<span data-ttu-id="8cddc-120">日程安排助理使用这些详细信息来筛选资源。</span><span class="sxs-lookup"><span data-stu-id="8cddc-120">The Schedule assistant uses these details to filter resources.</span></span>

## <a name="launch-the-schedule-assistant"></a><span data-ttu-id="8cddc-121">启动日程安排助理</span><span class="sxs-lookup"><span data-stu-id="8cddc-121">Launch the Schedule assistant</span></span>

<span data-ttu-id="8cddc-122">启动日程安排助理有两种方式。</span><span class="sxs-lookup"><span data-stu-id="8cddc-122">There are two ways in which the schedule assistant is launched.</span></span> <span data-ttu-id="8cddc-123">如果您使用的是混合模式，可以在团队成员网格中选择资源要求未满足的任何团队成员，然后选择 **预订**。</span><span class="sxs-lookup"><span data-stu-id="8cddc-123">If you're using the hybrid mode, in the team member grid you can select any team member with an unfulfilled resource requirement, and then select **Book**.</span></span> <span data-ttu-id="8cddc-124">如果您使用的是集中模式，资源经理会查找并选择资源。</span><span class="sxs-lookup"><span data-stu-id="8cddc-124">If you're using the central mode, the Resource manager finds and selects the resource.</span></span>

## <a name="schedule-assistant-filters"></a><span data-ttu-id="8cddc-125">日程安排助理筛选器</span><span class="sxs-lookup"><span data-stu-id="8cddc-125">Schedule assistant filters</span></span>

<span data-ttu-id="8cddc-126">在日程安排助理运行后，资源要求的详细信息将在左侧窗格中显示为筛选值。</span><span class="sxs-lookup"><span data-stu-id="8cddc-126">After the Schedule assistant runs, the details from the resource requirement are displayed as filtered values in the left pane.</span></span> <span data-ttu-id="8cddc-127">资源经理或项目经理可以通过调整筛选器来调整结果以满足计划需求。</span><span class="sxs-lookup"><span data-stu-id="8cddc-127">The Resource manager or the Project manager can fine-tune results by adjusting filters to meet the scheduling needs.</span></span>

<span data-ttu-id="8cddc-128">筛选器窗格显示与工作相关的选项，其中包括：</span><span class="sxs-lookup"><span data-stu-id="8cddc-128">The filter pane shows work-related options, including:</span></span>

-   <span data-ttu-id="8cddc-129">工作开始和结束</span><span class="sxs-lookup"><span data-stu-id="8cddc-129">Work start and end</span></span>
-   <span data-ttu-id="8cddc-130">特征</span><span class="sxs-lookup"><span data-stu-id="8cddc-130">Characteristics</span></span>
-   <span data-ttu-id="8cddc-131">角色</span><span class="sxs-lookup"><span data-stu-id="8cddc-131">Roles</span></span>
-   <span data-ttu-id="8cddc-132">部门</span><span class="sxs-lookup"><span data-stu-id="8cddc-132">Organizational units</span></span>
-   <span data-ttu-id="8cddc-133">资源供给公司</span><span class="sxs-lookup"><span data-stu-id="8cddc-133">Resourcing company</span></span>
-   <span data-ttu-id="8cddc-134">资源类型</span><span class="sxs-lookup"><span data-stu-id="8cddc-134">Resource types</span></span>
-   <span data-ttu-id="8cddc-135">首选资源</span><span class="sxs-lookup"><span data-stu-id="8cddc-135">Preferred resources</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]