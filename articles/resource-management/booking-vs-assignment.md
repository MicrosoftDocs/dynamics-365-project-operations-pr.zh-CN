---
title: 预订与分配
description: 此主题提供有关资源预订和资源分配之间的区别的信息。
author: ruhercul
manager: Annbe
ms.date: 01/08/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 9e346766e6ccbb3dff59ef12072a1cd63f1e4231
ms.sourcegitcommit: 260ce052fed760bb44c514517806049ca13a5459
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/08/2021
ms.locfileid: "4841161"
---
# <a name="bookings-vs-assignments"></a><span data-ttu-id="62cfb-103">预订与分配</span><span class="sxs-lookup"><span data-stu-id="62cfb-103">Bookings vs assignments</span></span>

<span data-ttu-id="62cfb-104">_**适用于：** 基于资源/非库存场景的 Project Operations，精简部署 - 估价开票交易_</span><span class="sxs-lookup"><span data-stu-id="62cfb-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="62cfb-105">预订是将资源硬性或软性分配给项目。</span><span class="sxs-lookup"><span data-stu-id="62cfb-105">Bookings are the hard or soft allocation of resources to a project.</span></span> <span data-ttu-id="62cfb-106">硬预订占用资源的产能。</span><span class="sxs-lookup"><span data-stu-id="62cfb-106">Hard bookings consume a resource's capacity.</span></span> <span data-ttu-id="62cfb-107">预订表示团队的组织概念，让他们可以了解如何在各个项目中投放资源。</span><span class="sxs-lookup"><span data-stu-id="62cfb-107">Bookings represent organizational concepts for teams so that they can understand how resources will be engaged across various projects.</span></span> <span data-ttu-id="62cfb-108">Dynamics 365 Project Operations 将预订视为项目级概念。</span><span class="sxs-lookup"><span data-stu-id="62cfb-108">Dynamics 365 Project Operations considers bookings a project-level concept.</span></span> 

<span data-ttu-id="62cfb-109">与预订不同，分配是资源对项目计划中的项目任务的承诺。</span><span class="sxs-lookup"><span data-stu-id="62cfb-109">Unlike bookings, assignments are the commitment of resources to project tasks in the project schedule.</span></span> <span data-ttu-id="62cfb-110">资源可以是指定的或通用的。</span><span class="sxs-lookup"><span data-stu-id="62cfb-110">The resources can be named or generic.</span></span>  <span data-ttu-id="62cfb-111">从项目任务分配获取资源要求时，Project Operations 使用资源分配的工作量信息来构建资源要求详细信息的信息。</span><span class="sxs-lookup"><span data-stu-id="62cfb-111">When a resource requirement is derived from the project task assignments, Project Operations uses the effort contours of the resources assignment to build the contours of the resource requirement details.</span></span> <span data-ttu-id="62cfb-112">但是，不会保留对资源分配的引用。</span><span class="sxs-lookup"><span data-stu-id="62cfb-112">However, a refence to the resource assignments isn't maintained.</span></span> <span data-ttu-id="62cfb-113">对从资源要求派生的预订的更新不会更新任何资源分配。</span><span class="sxs-lookup"><span data-stu-id="62cfb-113">Updates to the bookings derived from the resource requirement don't update any resource assignments.</span></span>

<span data-ttu-id="62cfb-114">通常，资源的预订总和等于一项或多项任务中资源分配的总和。</span><span class="sxs-lookup"><span data-stu-id="62cfb-114">Typically, the sum of the bookings for a resource will equal the sum of the resource's assignments across one or many tasks.</span></span> <span data-ttu-id="62cfb-115">但是，Project Operations 不强制执行此共识。</span><span class="sxs-lookup"><span data-stu-id="62cfb-115">However, Project Operations doesn't enforce this agreement.</span></span> <span data-ttu-id="62cfb-116">**协调** 视图为项目经理显示资源的预订和分配不一致的位置。</span><span class="sxs-lookup"><span data-stu-id="62cfb-116">The **Reconciliation** view shows the Project manager places where a resource's bookings and assignments don't agree.</span></span>


