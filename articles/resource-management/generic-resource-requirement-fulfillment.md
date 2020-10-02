---
title: 满足通用资源要求
description: 此部分介绍如何为通用资源要求预订指定资源。
author: ruhercul
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.technology: ''
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
ms.openlocfilehash: 76dd47fa2451b5cb61298ff332d77bae646a288a
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/28/2020
ms.locfileid: "3897575"
---
# <a name="generic-resource-requirement-fulfillment"></a><span data-ttu-id="19ac6-103">满足通用资源要求</span><span class="sxs-lookup"><span data-stu-id="19ac6-103">Generic resource requirement fulfillment</span></span>

<span data-ttu-id="19ac6-104">_**适用于：** 基于资源/非库存场景的 Project Operations，精简部署 - 估价开票交易_</span><span class="sxs-lookup"><span data-stu-id="19ac6-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="19ac6-105">可以预订指定资源以替换具有资源要求的通用资源。</span><span class="sxs-lookup"><span data-stu-id="19ac6-105">You can book a named resource to replace generic resource that has a resource requirement.</span></span>

1. <span data-ttu-id="19ac6-106">在**项目**页上，选择**团队**选项卡。</span><span class="sxs-lookup"><span data-stu-id="19ac6-106">On the **Projects** page, select the **Team** tab.</span></span>
2. <span data-ttu-id="19ac6-107">从列表中选择具有资源要求的通用资源，然后选择**预订**。</span><span class="sxs-lookup"><span data-stu-id="19ac6-107">Select the generic resource that has a resource requirement from the list, and then select **Book**.</span></span> <span data-ttu-id="19ac6-108">或者，打开资源要求，然后选择**预订**。</span><span class="sxs-lookup"><span data-stu-id="19ac6-108">Or, open the resource requirement and then select **Book**.</span></span>
3. <span data-ttu-id="19ac6-109">在**日程安排助理**页中，选择要为项目团队预订的指定资源，然后选择**预订**。</span><span class="sxs-lookup"><span data-stu-id="19ac6-109">On the **Schedule Assistant** page, select a named resource to book onto your project team and then select **Book**.</span></span>

<span data-ttu-id="19ac6-110">预订完成并由指定资源满足时，将把通用资源替换为指定资源。</span><span class="sxs-lookup"><span data-stu-id="19ac6-110">When the booking is complete and fulfilled by a named resource, the generic resource is replaced with the named resource.</span></span>

<span data-ttu-id="19ac6-111">也将使用该指定资源更新计划的分派。</span><span class="sxs-lookup"><span data-stu-id="19ac6-111">The assignments on the schedule are updated with the named resource as well.</span></span>

## <a name="fulfill-a-generic-resource-with-multiple-named-resources"></a><span data-ttu-id="19ac6-112">使用多项指定资源替代通用资源</span><span class="sxs-lookup"><span data-stu-id="19ac6-112">Fulfill a generic resource with multiple named resources</span></span>
<span data-ttu-id="19ac6-113">使用多项指定资源满足通用资源的要求类似分派一项指定资源。</span><span class="sxs-lookup"><span data-stu-id="19ac6-113">Fulfilling a requirement for a generic resource with multiple named resources is similar to assigning a single named resource.</span></span> <span data-ttu-id="19ac6-114">例如，有一个持续时间为 5 天，工作量为 120 个小时的任务。</span><span class="sxs-lookup"><span data-stu-id="19ac6-114">For example, there is a task with a duration of five days and 120 hours of effort.</span></span> <span data-ttu-id="19ac6-115">此任务不能由一个每周工作五天，每天通常工作八小时的资源完成。</span><span class="sxs-lookup"><span data-stu-id="19ac6-115">This task can't be completed by one resource that works a typical eight-hour day over a five-day week.</span></span> 

<span data-ttu-id="19ac6-116">此要求适用于五天工作 120 小时的机器人，即每天工作 24 小时。</span><span class="sxs-lookup"><span data-stu-id="19ac6-116">The requirement is for 120 hours of robotics engineering over five days, which is 24 hours per day.</span></span>

<span data-ttu-id="19ac6-117">这个示例是需要多项指定资源来满足一项通用资源请求。</span><span class="sxs-lookup"><span data-stu-id="19ac6-117">This is an example of when multiple named resources are needed to fulfill a generic resource request.</span></span> <span data-ttu-id="19ac6-118">您需要订阅多项资源以满足此要求。</span><span class="sxs-lookup"><span data-stu-id="19ac6-118">You will need to book multiple resources to fulfill the requirement.</span></span>

<span data-ttu-id="19ac6-119">此方案的主要区别是，分派给任务的团队中仍然保留通用资源，并且此位置中不分派预订的指定资源团队成员。</span><span class="sxs-lookup"><span data-stu-id="19ac6-119">The main difference in this scenario is that the generic resource remains on the team assigned to the task, and the booked named resource team members are not assigned as part of the position.</span></span> <span data-ttu-id="19ac6-120">项目经理可以根据需要将工作分派给指定资源。</span><span class="sxs-lookup"><span data-stu-id="19ac6-120">The project manager can assign the work as appropriate to the named resources.</span></span> <span data-ttu-id="19ac6-121">**协调**视图可帮助项目经理将多项资源的预订分解为任务分派。</span><span class="sxs-lookup"><span data-stu-id="19ac6-121">The **Reconciliation** view can assist a project manager in breaking up the bookings across multiple resources to task assignments.</span></span> <span data-ttu-id="19ac6-122">不会自动执行此操作，因为在比上面的简单示例更复杂的方案中（如您有大量任务构成要求或项目经理希望如何分配的意图）需要系统假设。</span><span class="sxs-lookup"><span data-stu-id="19ac6-122">This is not done automatically because in any scenario more complicated than the simple example above, such as where you have a bundle of tasks making up the requirement or the intent of how the project manager wants to assign, needs to be assumed by the system.</span></span> <span data-ttu-id="19ac6-123">因为系统无法理解意图，所以假设可能与意图不同，并且可能会出现错误结果或不可预料的结果。</span><span class="sxs-lookup"><span data-stu-id="19ac6-123">Because the system can't understand intent, it's likely that the assumptions will be different than intended and an incorrect or unpredictable result will occur.</span></span> <span data-ttu-id="19ac6-124">可预测结果是项目经理在**协调**视图的协助下特意创建资源之前，一直使用分派的通用资源。</span><span class="sxs-lookup"><span data-stu-id="19ac6-124">The predictable outcome is that the generic resource remains assigned until the project manager deliberately creates assignments, with the assistance of the **Reconciliation** view.</span></span>


