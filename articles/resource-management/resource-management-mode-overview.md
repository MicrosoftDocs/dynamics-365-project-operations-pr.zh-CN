---
title: 资源管理模式概述
description: 本主题提供有关 Dynamics 365 Project Operations 中的资源管理功能的信息。
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 73ba6190e2e366f22372102d14d26f6d71ba0bc1
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/28/2020
ms.locfileid: "4118507"
---
# <a name="resource-management-modes-overview"></a><span data-ttu-id="b3e23-103">资源管理模式概述</span><span class="sxs-lookup"><span data-stu-id="b3e23-103">Resource management modes overview</span></span>

<span data-ttu-id="b3e23-104">_**适用于：** 基于资源/非库存场景的 Project Operations，精简部署 - 估价开票交易_</span><span class="sxs-lookup"><span data-stu-id="b3e23-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="b3e23-105">Dynamics 365 Project Operations 支持两种模式，以便您执行整个预订流。</span><span class="sxs-lookup"><span data-stu-id="b3e23-105">Dynamics 365 Project Operations supports two modes in order for you to execute the overall booking flow.</span></span> <span data-ttu-id="b3e23-106">管理模式定义为项目参数，如果您的业务需求发生变化，可以进行修改。</span><span class="sxs-lookup"><span data-stu-id="b3e23-106">The mode of management is defined as a project parameter and can be modified if your business needs change.</span></span>    

## <a name="central-mode"></a><span data-ttu-id="b3e23-107">集中模式</span><span class="sxs-lookup"><span data-stu-id="b3e23-107">Central mode</span></span>
<span data-ttu-id="b3e23-108">对于将资源集中分配到项目的组织，集中模式提供了一种确保项目经理可以在项目级别定义资源要求的方法。</span><span class="sxs-lookup"><span data-stu-id="b3e23-108">For organizations who centralize the allocation for resources to projects, the Central mode provides a way to ensure Project managers can define resource requirements at the project level.</span></span> <span data-ttu-id="b3e23-109">资源要求的完成将委派给资源经理。</span><span class="sxs-lookup"><span data-stu-id="b3e23-109">Fulfillment of the resource requirements is delegated to a Resource manager.</span></span> <span data-ttu-id="b3e23-110">项目经理可以接受或拒绝资源经理建议的资源。</span><span class="sxs-lookup"><span data-stu-id="b3e23-110">Project managers can accept or reject resources that are proposed by the Resource manager.</span></span>

![集中模式](./media/resource-management-central.png)

<span data-ttu-id="b3e23-112">若要使用集中模式管理资源，请参阅：</span><span class="sxs-lookup"><span data-stu-id="b3e23-112">To manage resources with the Central mode, see:</span></span>

- [<span data-ttu-id="b3e23-113">为任务分配通用可预订资源，并生成资源要求</span><span class="sxs-lookup"><span data-stu-id="b3e23-113">Assign generic bookable resources to a task and generate resource requirements</span></span>](https://docs.microsoft.com/dynamics365/project-service/assign-generic-bookable-resource)
- [<span data-ttu-id="b3e23-114">根据资源要求预订指定资源</span><span class="sxs-lookup"><span data-stu-id="b3e23-114">Book named resources from resource requirements</span></span>](https://docs.microsoft.com/dynamics365/project-service/book-named-resource)
- [<span data-ttu-id="b3e23-115">提交资源请求</span><span class="sxs-lookup"><span data-stu-id="b3e23-115">Submit a resource request</span></span>](https://docs.microsoft.com/dynamics365/project-service/submit-resource-request)
- [<span data-ttu-id="b3e23-116">实施资源请求</span><span class="sxs-lookup"><span data-stu-id="b3e23-116">Fulfill a resource request</span></span>](https://docs.microsoft.com/dynamics365/project-service/resource-management-fulfill-requests)
- [<span data-ttu-id="b3e23-117">接受或拒绝资源请求的建议项目资源</span><span class="sxs-lookup"><span data-stu-id="b3e23-117">Accept or reject a proposed project resource from a resource request</span></span>](https://docs.microsoft.com/dynamics365/project-service/accept-reject-proposed-resource)

## <a name="hybrid-mode"></a><span data-ttu-id="b3e23-118">混合模式</span><span class="sxs-lookup"><span data-stu-id="b3e23-118">Hybrid mode</span></span>
<span data-ttu-id="b3e23-119">对于需要灵活分配资源的组织，混合模式让项目经理和资源经理都可以预订资源。</span><span class="sxs-lookup"><span data-stu-id="b3e23-119">For organizations who require flexibility in the allocation of resources, the hybrid mode enables both Project managers and Resource managers the ability to book resources.</span></span>

![混合模式](./media/resource-management-hybrid.png)

<span data-ttu-id="b3e23-121">除了受支持的集中模式流程之外，另请参阅以下主题来在混合模式下管理所有其他支持的预订流：</span><span class="sxs-lookup"><span data-stu-id="b3e23-121">In addition to the supported Central mode process, see the following topics to manage all other supported booking flows in the Hybrid mode:</span></span>

<span data-ttu-id="b3e23-122">将资源直接预订到项目：</span><span class="sxs-lookup"><span data-stu-id="b3e23-122">Book a resource directly to a project:</span></span>
- [<span data-ttu-id="b3e23-123">为项目团队预订指定的可预订资源和分派任务</span><span class="sxs-lookup"><span data-stu-id="b3e23-123">Book named bookable resources to a project team and assign tasks</span></span>](https://docs.microsoft.com/dynamics365/project-service/assign-named-bookable-resource)

<span data-ttu-id="b3e23-124">从资源要求预订资源：</span><span class="sxs-lookup"><span data-stu-id="b3e23-124">Book a resource from a resource requirement:</span></span>
- [<span data-ttu-id="b3e23-125">为任务分配通用可预订资源，并生成资源要求</span><span class="sxs-lookup"><span data-stu-id="b3e23-125">Assign generic bookable resources to a task and generate resource requirements</span></span>](https://docs.microsoft.com/dynamics365/project-service/assign-generic-bookable-resource)
- [<span data-ttu-id="b3e23-126">根据资源要求预订指定资源</span><span class="sxs-lookup"><span data-stu-id="b3e23-126">Book named resources from resource requirements</span></span>](https://docs.microsoft.com/dynamics365/project-service/book-named-resource)