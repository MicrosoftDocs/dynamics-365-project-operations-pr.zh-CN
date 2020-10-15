---
title: 预订与分配
description: 此主题提供有关资源预订和资源分配之间的区别的信息。
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: fa99783e52dbcdeaf80bbfd03df0f458f86b5e99
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/28/2020
ms.locfileid: "3896000"
---
# <a name="bookings-vs-assignments"></a><span data-ttu-id="31017-103">预订与分配</span><span class="sxs-lookup"><span data-stu-id="31017-103">Bookings vs assignments</span></span>

<span data-ttu-id="31017-104">_**适用于：** 基于资源/非库存场景的 Project Operations，精简部署 - 估价开票交易_</span><span class="sxs-lookup"><span data-stu-id="31017-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="31017-105">预订是将资源硬性或软性分配给项目。</span><span class="sxs-lookup"><span data-stu-id="31017-105">Bookings are the hard or soft allocation of resources to a project.</span></span> <span data-ttu-id="31017-106">硬预订占用资源的产能。</span><span class="sxs-lookup"><span data-stu-id="31017-106">Hard bookings consume a resource's capacity.</span></span> 

<span data-ttu-id="31017-107">分派是将资源分派给项目计划中的项目任务。</span><span class="sxs-lookup"><span data-stu-id="31017-107">Assignments are the assignment of resources to project tasks in the project schedule.</span></span> <span data-ttu-id="31017-108">资源可以是实际资源或通用资源。</span><span class="sxs-lookup"><span data-stu-id="31017-108">The resources can be real or generic.</span></span> 

<span data-ttu-id="31017-109">理想情况下，实际资源、预订和分派应一致，因为它们没有区别。</span><span class="sxs-lookup"><span data-stu-id="31017-109">Ideally, for real resources, the bookings and assignments should agree, because they don't differ.</span></span> <span data-ttu-id="31017-110">但是，Microsoft Dynamics Project Operations 不强制执行此共识。</span><span class="sxs-lookup"><span data-stu-id="31017-110">However, Microsoft Dynamics Project Operations doesn't enforce this agreement.</span></span> <span data-ttu-id="31017-111">**协调**视图为项目经理显示资源的预订和分派不一致的位置。</span><span class="sxs-lookup"><span data-stu-id="31017-111">The **Reconciliation** view shows a project manager places where a resource's bookings and assignments don't agree.</span></span>
