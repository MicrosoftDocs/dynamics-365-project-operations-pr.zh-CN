---
title: 资源利用率概述
description: 此主题介绍 Project Operations 中的资源利用率。
author: ruhercul
ms.date: 11/05/2020
ms.topic: article
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: a683931bcd6a357c5feec9198b190b948ad17a40
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/10/2021
ms.locfileid: "6000785"
---
# <a name="resource-utilization-overview"></a><span data-ttu-id="b50ad-103">资源利用率概述</span><span class="sxs-lookup"><span data-stu-id="b50ad-103">Resource utilization overview</span></span>

<span data-ttu-id="b50ad-104">_**适用于：** 基于资源/非库存场景的 Project Operations，精简部署 - 估价开票交易_</span><span class="sxs-lookup"><span data-stu-id="b50ad-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="b50ad-105">资源可以有目标可记帐利用率。</span><span class="sxs-lookup"><span data-stu-id="b50ad-105">Resources can have a target billable utilization.</span></span> <span data-ttu-id="b50ad-106">此目标利用率定义为资源默认角色的一个属性，或在单个可预订资源的记录中设置。</span><span class="sxs-lookup"><span data-stu-id="b50ad-106">This target utilization is defined as an attribute on a resource's default role or set on the record of the individual bookable resource.</span></span> <span data-ttu-id="b50ad-107">利用率的计算可基于使用批准的时间条目报告的实际工时。</span><span class="sxs-lookup"><span data-stu-id="b50ad-107">Utilization calculations are based on the actual hours that resources have reported by using approved time entries.</span></span>

<span data-ttu-id="b50ad-108">以下公式用于计算利用率：</span><span class="sxs-lookup"><span data-stu-id="b50ad-108">The following formulas are used to calculate utilization:</span></span>

  - <span data-ttu-id="b50ad-109">可记帐利用率 = 可记帐实际工时数 ÷ 资源产能</span><span class="sxs-lookup"><span data-stu-id="b50ad-109">Billable utilization = Chargeable actual hours ÷ Resource capacity</span></span>
  - <span data-ttu-id="b50ad-110">不可记帐利用率 = 带有记帐类型的 ID 实际时间= 不应计费、补充或不可用 ÷ 资源产能</span><span class="sxs-lookup"><span data-stu-id="b50ad-110">Non-billable utilization = Actual time with billing type ID = Non-chargeable, Complementary, or Not available ÷ Resource capacity</span></span>
  - <span data-ttu-id="b50ad-111">内部 = 无销售合同的实际时间 ÷ 资源产能</span><span class="sxs-lookup"><span data-stu-id="b50ad-111">Internal = Actual time with no sales contract ÷ Resource capacity</span></span>
  - <span data-ttu-id="b50ad-112">资源产能 = 资源工作时间 – 外出 – 非工作日</span><span class="sxs-lookup"><span data-stu-id="b50ad-112">Resource capacity = Resource work hours – Out-of-office – Non-working days</span></span>

<span data-ttu-id="b50ad-113">可以在 **资源** 窗格中找到 **资源利用率** 视图。</span><span class="sxs-lookup"><span data-stu-id="b50ad-113">You can find the **Resource Utilization** view in the **Resources** pane.</span></span>

<span data-ttu-id="b50ad-114">此网格中的每个单元格代表一段时间（如天、周或月）的资源可记帐利用率百分比。</span><span class="sxs-lookup"><span data-stu-id="b50ad-114">Each cell in the grid represents the billable utilization percentage of the resource in a period, such as a day, week, or month.</span></span> <span data-ttu-id="b50ad-115">以下公式用于为单元格设置颜色：</span><span class="sxs-lookup"><span data-stu-id="b50ad-115">The following formulas are used to color the cells:</span></span>

  - <span data-ttu-id="b50ad-116">**绿色**：可计费利用率 >= 资源目标利用率</span><span class="sxs-lookup"><span data-stu-id="b50ad-116">**Green**: Billable utilization >= Resource target utilization</span></span>
  - <span data-ttu-id="b50ad-117">**黄色**：目标利用率 – 20 <= 可计费利用率 < 目标利用率</span><span class="sxs-lookup"><span data-stu-id="b50ad-117">**Yellow**: Target utilization – 20 <= Billable utilization < Target utilization</span></span>
  - <span data-ttu-id="b50ad-118">**红色**：可计费利用率 < 目标利用率 – 20</span><span class="sxs-lookup"><span data-stu-id="b50ad-118">**Red**: Billable utilization < Target utilization – 20</span></span>

<span data-ttu-id="b50ad-119">因为 **资源利用率** 视图基于日程安排板，所以可使用日程安排板的功能筛选结果。</span><span class="sxs-lookup"><span data-stu-id="b50ad-119">Because the **Resource Utilization** view is based on the Schedule Board, you can use the filtering capabilities of the Schedule Board to filter your results.</span></span>

<span data-ttu-id="b50ad-120">此网格要求对角色或单个资源设置目标利用率。</span><span class="sxs-lookup"><span data-stu-id="b50ad-120">The grid requires that you set a target utilization on either the role or the individual resource.</span></span> <span data-ttu-id="b50ad-121">若要进行此设置，转到 **资源** > **资源角色**。</span><span class="sxs-lookup"><span data-stu-id="b50ad-121">To do this setup, go to **Resources** > **Resource roles**.</span></span>

<span data-ttu-id="b50ad-122">此外，还必须为每项可预订资源分派默认角色。</span><span class="sxs-lookup"><span data-stu-id="b50ad-122">Additionally, a default role must be assigned to each bookable resource.</span></span> <span data-ttu-id="b50ad-123">转到 **资源** > **资源**。</span><span class="sxs-lookup"><span data-stu-id="b50ad-123">Go to **Resources** > **Resources**.</span></span> <span data-ttu-id="b50ad-124">在 **Project Service** 选项卡上，验证是否定义了资源角色，以及 **为默认** 字段是否设置为 **是**。</span><span class="sxs-lookup"><span data-stu-id="b50ad-124">On the **Project Service** tab, verify that a resource role is defined, and that the **Is Default** field is set to **Yes**.</span></span> <span data-ttu-id="b50ad-125">可以添加更多 **为默认** = **否** 的角色。</span><span class="sxs-lookup"><span data-stu-id="b50ad-125">You can add additional roles where **Is Default** = **No**.</span></span> <span data-ttu-id="b50ad-126">**为默认** = **是** 的角色用于评估针对该角色的目标的资源利用率。</span><span class="sxs-lookup"><span data-stu-id="b50ad-126">The role where the **Is Default** = **Yes** is used to evaluate the resource's utilization against the target for that role.</span></span>

<span data-ttu-id="b50ad-127">在 **Project Service** 选项卡上，也可以为资源设置单个目标利用率。</span><span class="sxs-lookup"><span data-stu-id="b50ad-127">On the **Project Service** tab, you can also set an individual target utilization for the resource.</span></span> <span data-ttu-id="b50ad-128">然后，利用率的计算使用该目标利用率评估资源的目标，而不是资源默认角色的目标。</span><span class="sxs-lookup"><span data-stu-id="b50ad-128">The utilization calculation then uses that target utilization to evaluate the resource's target instead of the target of the resource's default role.</span></span>

<span data-ttu-id="b50ad-129">仅当资源批准了网格中显示的期间内的应计费时间时才显示资源的利用率。</span><span class="sxs-lookup"><span data-stu-id="b50ad-129">Utilization is only shown for a resource if that resource has approved, chargeable time during the period shown in the grid.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]