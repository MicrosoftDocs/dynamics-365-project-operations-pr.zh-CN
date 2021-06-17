---
title: 查看建议资源
description: 此主题介绍如何建议任务资源。
author: ruhercul
ms.date: 11/05/2020
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 987ea08c77c1824182856c0d52ee0cd15e7029b9
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/10/2021
ms.locfileid: "6000740"
---
# <a name="review-proposed-resources"></a><span data-ttu-id="48ad0-103">查看建议资源</span><span class="sxs-lookup"><span data-stu-id="48ad0-103">Review proposed resources</span></span>

<span data-ttu-id="48ad0-104">_**适用于：** 基于资源/非库存场景的 Project Operations，精简部署 - 估价开票交易_</span><span class="sxs-lookup"><span data-stu-id="48ad0-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="48ad0-105">资源经理可使用资源请求为项目经理建议资源。</span><span class="sxs-lookup"><span data-stu-id="48ad0-105">Resource managers can propose a resource to the project manager by using a resource request.</span></span>

1. <span data-ttu-id="48ad0-106">从请求网格或请求本身选择 **查找资源**。</span><span class="sxs-lookup"><span data-stu-id="48ad0-106">From the request grid or the request itself, select **Find Resources**.</span></span>
2. <span data-ttu-id="48ad0-107">在 **日程安排助理** 页中，选择资源，然后在 **创建资源预订** 窗格的 **预订状态** 字段中，选择 **预订**。</span><span class="sxs-lookup"><span data-stu-id="48ad0-107">On the **Schedule Assistant** page, select the resource, and then, in the **Create Resource Booking** pane, in the **Booking Status** field, select **Book**.</span></span>

<span data-ttu-id="48ad0-108">将进行以下状态更新：</span><span class="sxs-lookup"><span data-stu-id="48ad0-108">The following status updates occur:</span></span>

- <span data-ttu-id="48ad0-109">在 **日程安排助理** 页中，将更新状态指示器，以便指示预订是建议的，而不是硬预订的。</span><span class="sxs-lookup"><span data-stu-id="48ad0-109">On the **Schedule Assistant** page, the status indicators are updated to indicate that the booking is proposed, not hard-booked.</span></span>
- <span data-ttu-id="48ad0-110">在资源请求中，状态更改为 **需要审阅**。</span><span class="sxs-lookup"><span data-stu-id="48ad0-110">On the resource request, the status is changed to **Needs Review**.</span></span>
- <span data-ttu-id="48ad0-111">在项目的 **团队** 选项卡上，通用团队成员的 **请求状态** 值更改为 **需要审阅**。</span><span class="sxs-lookup"><span data-stu-id="48ad0-111">On the **Team** tab of the project, the generic team member's **Request Status** value is changed to **Needs Review**.</span></span>

<span data-ttu-id="48ad0-112">项目经理可接受或拒绝建议。</span><span class="sxs-lookup"><span data-stu-id="48ad0-112">The project manager can either accept or reject the proposal.</span></span>

<span data-ttu-id="48ad0-113">当资源经理处理资源请求时，可以使用下面的任何方法：</span><span class="sxs-lookup"><span data-stu-id="48ad0-113">When resource managers process resource requests, they can use any of the following approaches:</span></span>

- <span data-ttu-id="48ad0-114">如果一项资源不能满足所需工时，建议多项资源以满足需求。</span><span class="sxs-lookup"><span data-stu-id="48ad0-114">Propose multiple resources to satisfy the demand if no single resource is available to fulfill the required hours.</span></span> <span data-ttu-id="48ad0-115">然后在可满足所需工时的多项资源之间拆分建议的工时。</span><span class="sxs-lookup"><span data-stu-id="48ad0-115">Proposed hours are then split among multiple resources that can satisfy the required hours.</span></span> <span data-ttu-id="48ad0-116">在此方案中，工时不能重合。</span><span class="sxs-lookup"><span data-stu-id="48ad0-116">In this scenario, the hours can't overlap.</span></span>
- <span data-ttu-id="48ad0-117">建议比所需资源更少的资源。</span><span class="sxs-lookup"><span data-stu-id="48ad0-117">Propose fewer resources than are required.</span></span> <span data-ttu-id="48ad0-118">在此方案中，建议的资源产能比请求者指定所需工时少。</span><span class="sxs-lookup"><span data-stu-id="48ad0-118">In this scenario, the proposed resource capacity is less than the required hours that the requestor specified.</span></span> <span data-ttu-id="48ad0-119">因此，当请求者接受建议的资源时，将创建未满足资源要求以捕获剩余需求。</span><span class="sxs-lookup"><span data-stu-id="48ad0-119">Therefore, when the requestor accepts the proposed resources, an unfulfilled resource requirement is created to capture the remaining demand.</span></span>
- <span data-ttu-id="48ad0-120">如果没有哪一项资源可以单独完成工作，则预订多项资源以满足需求。</span><span class="sxs-lookup"><span data-stu-id="48ad0-120">Book multiple resources to satisfy the demand if no single resource is available to complete the work.</span></span>
- <span data-ttu-id="48ad0-121">预订比所需资源更少的资源。</span><span class="sxs-lookup"><span data-stu-id="48ad0-121">Book fewer resources than are required.</span></span> <span data-ttu-id="48ad0-122">在此方案中，预订的工时比所需工时少。</span><span class="sxs-lookup"><span data-stu-id="48ad0-122">In this scenario, the booked hours are fewer than the required hours.</span></span> <span data-ttu-id="48ad0-123">系统将引导您建议资源，而不是建议预订，这样请求者就可以验证和跟踪剩余需求。</span><span class="sxs-lookup"><span data-stu-id="48ad0-123">The system guides you to propose resources instead of bookings, so that the requestor can verify and keep track of remaining demand.</span></span>

## <a name="resource-availability"></a><span data-ttu-id="48ad0-124">资源可用性</span><span class="sxs-lookup"><span data-stu-id="48ad0-124">Resource availability</span></span>

<span data-ttu-id="48ad0-125">资源经理是可查看资源的可用性和更新预订至关重要。</span><span class="sxs-lookup"><span data-stu-id="48ad0-125">It's critical that resource managers be able to view the availability of resources and update bookings.</span></span> <span data-ttu-id="48ad0-126">在某些情况下，不存在正式需求（资源请求），但是资源经理必须响应来自渠道（如电子邮件、电话联络或即时消息）的意外需求。</span><span class="sxs-lookup"><span data-stu-id="48ad0-126">In some cases, there is no formal demand (resource request), but a resource manager must respond to an unplanned demand that comes through channels such as an email, phone call, or instant message.</span></span> <span data-ttu-id="48ad0-127">资源经理可使用日程安排板更新资源和预订。</span><span class="sxs-lookup"><span data-stu-id="48ad0-127">Resource managers use the Schedule Board to update resources and bookings.</span></span>

<span data-ttu-id="48ad0-128">资源工作时间是计算资源可用性的基础。</span><span class="sxs-lookup"><span data-stu-id="48ad0-128">Resource work hours are used as the basis for calculating the availability of a resource.</span></span> <span data-ttu-id="48ad0-129">资源预订会占用资源的产能。</span><span class="sxs-lookup"><span data-stu-id="48ad0-129">Resource bookings consume the capacity of the resources.</span></span>

<span data-ttu-id="48ad0-130">日程安排板使用颜色和阴影显示预订、可用性、超额预订和预订状态。</span><span class="sxs-lookup"><span data-stu-id="48ad0-130">The Schedule Board uses colors and shading to show bookings, availability, and overbookings, and also the status of bookings.</span></span> <span data-ttu-id="48ad0-131">可使用日程安排板设置中的一项设置来显示图例。</span><span class="sxs-lookup"><span data-stu-id="48ad0-131">A setting in the Schedule Board settings lets you show a legend.</span></span>

<span data-ttu-id="48ad0-132">如果日程安排板中单项可预订资源旁边显示向右箭头，说明可以展开该资源以显示为预订该资源的工作的详细信息。</span><span class="sxs-lookup"><span data-stu-id="48ad0-132">If a right-pointing arrow appears next to an individual bookable resource on the Schedule Board, the resource can be expanded to show details of the work that the resource is booked on.</span></span>

<span data-ttu-id="48ad0-133">因为 Dynamics 365 Project Operations 使用 Universal Resource Scheduling 引擎，所以如果也安装了 Dynamics 365 Field Service，则可查看项目、工作订单和您已将计划扩展到的其他任何实体的资源预订。</span><span class="sxs-lookup"><span data-stu-id="48ad0-133">Because Dynamics 365 Project Operations uses the Universal Resource Scheduling engine, if you also have Dynamics 365 Field Service installed, you can view the details of resource bookings for projects, work orders, and any other entities that you've extended scheduling to.</span></span>

<span data-ttu-id="48ad0-134">若要查看单项资源的更多详细信息，请右键单击该资源打开资源卡。</span><span class="sxs-lookup"><span data-stu-id="48ad0-134">To view more details about an individual resource, right-click it to open the resource card.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]