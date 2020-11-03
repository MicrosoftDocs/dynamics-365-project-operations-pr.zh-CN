---
title: 查看建议资源
description: 此主题介绍如何建议任务资源。
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
ms.openlocfilehash: ad5cbdeb5fe05e6115eb024833a8d58b626ea4c9
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/16/2020
ms.locfileid: "4072571"
---
# <a name="review-proposed-resources"></a><span data-ttu-id="a2d33-103">查看建议资源</span><span class="sxs-lookup"><span data-stu-id="a2d33-103">Review proposed resources</span></span>

<span data-ttu-id="a2d33-104">_**适用于：** 基于资源/非库存场景的 Project Operations，精简部署 - 估价开票交易_</span><span class="sxs-lookup"><span data-stu-id="a2d33-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="a2d33-105">资源经理可使用资源请求为项目经理建议资源。</span><span class="sxs-lookup"><span data-stu-id="a2d33-105">Resource managers can propose a resource to the project manager by using a resource request.</span></span>

1. <span data-ttu-id="a2d33-106">从请求网格或请求本身选择 **查找资源** 。</span><span class="sxs-lookup"><span data-stu-id="a2d33-106">From the request grid or the request itself, select **Find Resources**.</span></span>
2. <span data-ttu-id="a2d33-107">在 **日程安排助理** 页中，选择资源，然后在 **创建资源预订** 窗格的 **预订状态** 字段中，选择 **预订** 。</span><span class="sxs-lookup"><span data-stu-id="a2d33-107">On the **Schedule Assistant** page, select the resource, and then, in the **Create Resource Booking** pane, in the **Booking Status** field, select **Book**.</span></span>

<span data-ttu-id="a2d33-108">将进行以下状态更新：</span><span class="sxs-lookup"><span data-stu-id="a2d33-108">The following status updates occur:</span></span>

- <span data-ttu-id="a2d33-109">在 **日程安排助理** 页中，将更新状态指示器，以便指示预订是建议的，而不是硬预订的。</span><span class="sxs-lookup"><span data-stu-id="a2d33-109">On the **Schedule Assistant** page, the status indicators are updated to indicate that the booking is proposed, not hard-booked.</span></span>
- <span data-ttu-id="a2d33-110">在资源请求中，状态更改为 **需要审阅** 。</span><span class="sxs-lookup"><span data-stu-id="a2d33-110">On the resource request, the status is changed to **Needs Review**.</span></span>
- <span data-ttu-id="a2d33-111">在项目的 **团队** 选项卡上，通用团队成员的 **请求状态** 值更改为 **需要审阅** 。</span><span class="sxs-lookup"><span data-stu-id="a2d33-111">On the **Team** tab of the project, the generic team member's **Request Status** value is changed to **Needs Review**.</span></span>

<span data-ttu-id="a2d33-112">项目经理可接受或拒绝建议。</span><span class="sxs-lookup"><span data-stu-id="a2d33-112">The project manager can either accept or reject the proposal.</span></span>

<span data-ttu-id="a2d33-113">当资源经理处理资源请求时，可以使用下面的任何方法：</span><span class="sxs-lookup"><span data-stu-id="a2d33-113">When resource managers process resource requests, they can use any of the following approaches:</span></span>

- <span data-ttu-id="a2d33-114">如果一项资源不能满足所需工时，建议多项资源以满足需求。</span><span class="sxs-lookup"><span data-stu-id="a2d33-114">Propose multiple resources to satisfy the demand if no single resource is available to fulfill the required hours.</span></span> <span data-ttu-id="a2d33-115">然后在可满足所需工时的多项资源之间拆分建议的工时。</span><span class="sxs-lookup"><span data-stu-id="a2d33-115">Proposed hours are then split among multiple resources that can satisfy the required hours.</span></span> <span data-ttu-id="a2d33-116">在此方案中，工时不能重合。</span><span class="sxs-lookup"><span data-stu-id="a2d33-116">In this scenario, the hours can't overlap.</span></span>
- <span data-ttu-id="a2d33-117">建议比所需资源更少的资源。</span><span class="sxs-lookup"><span data-stu-id="a2d33-117">Propose fewer resources than are required.</span></span> <span data-ttu-id="a2d33-118">在此方案中，建议的资源产能比请求者指定所需工时少。</span><span class="sxs-lookup"><span data-stu-id="a2d33-118">In this scenario, the proposed resource capacity is less than the required hours that the requestor specified.</span></span> <span data-ttu-id="a2d33-119">因此，当请求者接受建议的资源时，将创建未满足资源要求以捕获剩余需求。</span><span class="sxs-lookup"><span data-stu-id="a2d33-119">Therefore, when the requestor accepts the proposed resources, an unfulfilled resource requirement is created to capture the remaining demand.</span></span>
- <span data-ttu-id="a2d33-120">如果没有哪一项资源可以单独完成工作，则预订多项资源以满足需求。</span><span class="sxs-lookup"><span data-stu-id="a2d33-120">Book multiple resources to satisfy the demand if no single resource is available to complete the work.</span></span>
- <span data-ttu-id="a2d33-121">预订比所需资源更少的资源。</span><span class="sxs-lookup"><span data-stu-id="a2d33-121">Book fewer resources than are required.</span></span> <span data-ttu-id="a2d33-122">在此方案中，预订的工时比所需工时少。</span><span class="sxs-lookup"><span data-stu-id="a2d33-122">In this scenario, the booked hours are fewer than the required hours.</span></span> <span data-ttu-id="a2d33-123">系统将引导您建议资源，而不是建议预订，这样请求者就可以验证和跟踪剩余需求。</span><span class="sxs-lookup"><span data-stu-id="a2d33-123">The system guides you to propose resources instead of bookings, so that the requestor can verify and keep track of remaining demand.</span></span>

## <a name="billable-utilization"></a><span data-ttu-id="a2d33-124">可记帐利用率</span><span class="sxs-lookup"><span data-stu-id="a2d33-124">Billable utilization</span></span>

<span data-ttu-id="a2d33-125">资源可以有目标可记帐利用率。</span><span class="sxs-lookup"><span data-stu-id="a2d33-125">Resources can have a target billable utilization.</span></span> <span data-ttu-id="a2d33-126">此目标利用率定义为资源默认角色的一个属性，或在单个可预订资源的记录中设置。</span><span class="sxs-lookup"><span data-stu-id="a2d33-126">This target utilization is either defined as an attribute on a resource's default role or set on the record of the individual bookable resource.</span></span> <span data-ttu-id="a2d33-127">利用率的计算可基于使用批准的时间条目报告的实际工时。</span><span class="sxs-lookup"><span data-stu-id="a2d33-127">Utilization calculations are based on the actual hours that resources have reported by using approved time entries.</span></span>

<span data-ttu-id="a2d33-128">以下公式用于计算利用率：</span><span class="sxs-lookup"><span data-stu-id="a2d33-128">The following formulas are used to calculate utilization:</span></span>

- <span data-ttu-id="a2d33-129">可记帐利用率 = 可记帐实际工时数 ÷ 资源产能</span><span class="sxs-lookup"><span data-stu-id="a2d33-129">Billable utilization = Chargeable actual hours ÷ Resource capacity</span></span>
- <span data-ttu-id="a2d33-130">不可记帐利用率 = 带有记帐类型的 ID 实际时间= 不应计费、补充或不可用 ÷ 资源产能</span><span class="sxs-lookup"><span data-stu-id="a2d33-130">Non-billable utilization = Actual time with billing type ID = Non-chargeable, Complementary, or Not available ÷ Resource capacity</span></span>
- <span data-ttu-id="a2d33-131">内部 = 无销售合同的实际时间 ÷ 资源产能</span><span class="sxs-lookup"><span data-stu-id="a2d33-131">Internal = Actual time with no sales contract ÷ Resource capacity</span></span>
- <span data-ttu-id="a2d33-132">资源产能 = 资源工作时间 – 外出 – 非工作日</span><span class="sxs-lookup"><span data-stu-id="a2d33-132">Resource capacity = Resource work hours – Out-of-office – Non-working days</span></span>

<span data-ttu-id="a2d33-133">可以在 **资源** 窗格中找到 **资源利用率** 视图。</span><span class="sxs-lookup"><span data-stu-id="a2d33-133">You can find the **Resource Utilization** view in the **Resources** pane.</span></span>

<span data-ttu-id="a2d33-134">此网格中的每个单元格代表一段时间（如天、周或月）的资源可记帐利用率百分比。</span><span class="sxs-lookup"><span data-stu-id="a2d33-134">Each cell in the grid represents the billable utilization percentage of the resource in a period, such as a day, week, or month.</span></span> <span data-ttu-id="a2d33-135">以下公式用于为单元格设置颜色：</span><span class="sxs-lookup"><span data-stu-id="a2d33-135">The following formulas are used to color the cells:</span></span>

- <span data-ttu-id="a2d33-136">**绿色：** 可记帐利用率 \>= 资源目标利用率</span><span class="sxs-lookup"><span data-stu-id="a2d33-136">**Green:** Billable utilization \>= Resource target utilization</span></span>
- <span data-ttu-id="a2d33-137">**黄色：** 目标利用率 – 20 \<= 可记帐利用率 \< 目标利用率</span><span class="sxs-lookup"><span data-stu-id="a2d33-137">**Yellow:** Target utilization – 20 \<= Billable utilization \< Target utilization</span></span>
- <span data-ttu-id="a2d33-138">**红色：** 可记帐利用率 \< 目标利用率 – 20</span><span class="sxs-lookup"><span data-stu-id="a2d33-138">**Red:** Billable utilization \< Target utilization – 20</span></span>

<span data-ttu-id="a2d33-139">因为 **资源利用率** 视图基于日程安排板，所以可使用日程安排板的功能筛选结果。</span><span class="sxs-lookup"><span data-stu-id="a2d33-139">Because the **Resource Utilization** view is based on the Schedule Board, you can use the filtering capabilities of the Schedule Board to filter your results.</span></span>

<span data-ttu-id="a2d33-140">此网格要求对角色或单个资源设置目标利用率。</span><span class="sxs-lookup"><span data-stu-id="a2d33-140">The grid requires that you set a target utilization on either the role or the individual resource.</span></span> <span data-ttu-id="a2d33-141">若要进行此设置，转到 **资源** \> **资源角色** 。</span><span class="sxs-lookup"><span data-stu-id="a2d33-141">To do this setup, go to **Resources** \> **Resource roles**.</span></span>

<span data-ttu-id="a2d33-142">此外，还必须为每项可预订资源分派默认角色。</span><span class="sxs-lookup"><span data-stu-id="a2d33-142">Additionally, a default role must be assigned to each bookable resource.</span></span> <span data-ttu-id="a2d33-143">转到 **资源**\>**资源** 。</span><span class="sxs-lookup"><span data-stu-id="a2d33-143">Go to **Resources** \> **Resources**.</span></span> <span data-ttu-id="a2d33-144">在 **Project Service** 选项卡上，验证是否定义了资源角色，以及角色的 **为默认** 字段是否设置为 **是** 。</span><span class="sxs-lookup"><span data-stu-id="a2d33-144">On the **Project Service** tab, verify that a resource role is defined, and that the **Is Default** field for it is set to **Yes**.</span></span> <span data-ttu-id="a2d33-145">可以添加更多 **为默认 = 否** 的角色。</span><span class="sxs-lookup"><span data-stu-id="a2d33-145">You can add additional roles where **Is Default = No**.</span></span> <span data-ttu-id="a2d33-146">**为默认 = 是** 的角色用于评估针对该角色的目标的资源利用率。</span><span class="sxs-lookup"><span data-stu-id="a2d33-146">The role where the **Is Default = Yes** is used to evaluate the resource's utilization against the target for that role.</span></span>

<span data-ttu-id="a2d33-147">在 **Project Service** 选项卡上，也可以为资源设置单个目标利用率。</span><span class="sxs-lookup"><span data-stu-id="a2d33-147">On the **Project Service** tab, you can also set an individual target utilization for the resource.</span></span> <span data-ttu-id="a2d33-148">然后，利用率的计算使用该目标利用率评估资源的目标，而不是资源默认角色的目标。</span><span class="sxs-lookup"><span data-stu-id="a2d33-148">The utilization calculation then uses that target utilization to evaluate the resource's target instead of the target of the resource's default role.</span></span>

<span data-ttu-id="a2d33-149">仅当资源批准了网格中显示的期间内的应计费时间时才显示该资源的利用率。</span><span class="sxs-lookup"><span data-stu-id="a2d33-149">Utilization is shown for a resource only if that resource has approved, chargeable time during the period that is shown in the grid.</span></span>

## <a name="resource-availability"></a><span data-ttu-id="a2d33-150">资源可用性</span><span class="sxs-lookup"><span data-stu-id="a2d33-150">Resource availability</span></span>

<span data-ttu-id="a2d33-151">资源经理是可查看资源的可用性和更新预订至关重要。</span><span class="sxs-lookup"><span data-stu-id="a2d33-151">It's critical that resource managers be able to view the availability of resources and update bookings.</span></span> <span data-ttu-id="a2d33-152">在某些情况下，不存在正式需求（资源请求），但是资源经理必须响应来自渠道（如电子邮件、电话联络或即时消息）的意外需求。</span><span class="sxs-lookup"><span data-stu-id="a2d33-152">In some cases, there is no formal demand (resource request), but a resource manager must respond to an unplanned demand that comes through channels such as an email, phone call, or instant message.</span></span> <span data-ttu-id="a2d33-153">资源经理可使用日程安排板更新资源和预订。</span><span class="sxs-lookup"><span data-stu-id="a2d33-153">Resource managers use the Schedule Board to update resources and bookings.</span></span>

<span data-ttu-id="a2d33-154">资源工作时间是计算资源可用性的基础。</span><span class="sxs-lookup"><span data-stu-id="a2d33-154">Resource work hours are used as the basis for calculating the availability of a resource.</span></span> <span data-ttu-id="a2d33-155">资源预订会占用资源的产能。</span><span class="sxs-lookup"><span data-stu-id="a2d33-155">Resource bookings consume the capacity of the resources.</span></span>

<span data-ttu-id="a2d33-156">日程安排板使用颜色和阴影显示预订、可用性、超额预订和预订状态。</span><span class="sxs-lookup"><span data-stu-id="a2d33-156">The Schedule Board uses colors and shading to show bookings, availability, and overbookings, and also the status of bookings.</span></span> <span data-ttu-id="a2d33-157">可使用日程安排板设置中的一项设置来显示图例。</span><span class="sxs-lookup"><span data-stu-id="a2d33-157">A setting in the Schedule Board settings lets you show a legend.</span></span>

<span data-ttu-id="a2d33-158">如果日程安排板中单项可预订资源旁边显示向右箭头，说明可以展开该资源以显示为预订该资源的工作的详细信息。</span><span class="sxs-lookup"><span data-stu-id="a2d33-158">If a right-pointing arrow appears next to an individual bookable resource on the Schedule Board, the resource can be expanded to show details of the work that the resource is booked on.</span></span>

<span data-ttu-id="a2d33-159">因为 Dynamics 365 Project Operations 使用 Universal Resource Scheduling 引擎，所以如果也安装了 Dynamics 365 Field Service，则可查看项目、工作订单和您已将计划扩展到的其他任何实体的资源预订。</span><span class="sxs-lookup"><span data-stu-id="a2d33-159">Because Dynamics 365 Project Operations uses the Universal Resource Scheduling engine, if you also have Dynamics 365 Field Service installed, you can view the details of resource bookings for projects, work orders, and any other entities that you've extended scheduling to.</span></span>

<span data-ttu-id="a2d33-160">若要查看单项资源的更多详细信息，请右键单击该资源打开资源卡。</span><span class="sxs-lookup"><span data-stu-id="a2d33-160">To view more details about an individual resource, right-click it to open the resource card.</span></span>

