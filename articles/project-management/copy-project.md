---
title: 复制项目
description: 本主题提供有关在 Dynamics 365 Project Operations 中复制项目的信息。
author: ruhercul
manager: AnnBe
ms.date: 02/22/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: af1942e81691d9e13fdcbbf68599c1a8a4004582
ms.sourcegitcommit: 24528bb9c0ef8898077cb3bc672daa211c0e73aa
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/04/2021
ms.locfileid: "5479508"
---
# <a name="copy-a-project"></a><span data-ttu-id="caa80-103">复制项目</span><span class="sxs-lookup"><span data-stu-id="caa80-103">Copy a project</span></span>

<span data-ttu-id="caa80-104">_**适用于：** 基于资源/非库存场景的 Project Operations，精简部署 - 估价开票交易_</span><span class="sxs-lookup"><span data-stu-id="caa80-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="caa80-105">使用 Dynamics 365 Project Operations，可以通过选择 **项目** 窗体上的 **复制项目** 快速生成新项目。</span><span class="sxs-lookup"><span data-stu-id="caa80-105">With Dynamics 365 Project Operations, you can quickly build new projects by selecting **Copy Project** on the **Projects** form.</span></span> <span data-ttu-id="caa80-106">若要复制项目，请打开要复制的项目，然后选择 **复制项目**。</span><span class="sxs-lookup"><span data-stu-id="caa80-106">To copy a project, open the project you want to copy, and then select **Copy project**.</span></span> <span data-ttu-id="caa80-107">此操作将复制：</span><span class="sxs-lookup"><span data-stu-id="caa80-107">The action will copy:</span></span>

- <span data-ttu-id="caa80-108">项目属性（从源项目复制了估计的开始日期）</span><span class="sxs-lookup"><span data-stu-id="caa80-108">Project properties (The estimated start date is copied from the source project)</span></span>
- <span data-ttu-id="caa80-109">工作分解结构</span><span class="sxs-lookup"><span data-stu-id="caa80-109">The Work breakdown structure</span></span>
- <span data-ttu-id="caa80-110">项目团队成员</span><span class="sxs-lookup"><span data-stu-id="caa80-110">Project team members</span></span>
- <span data-ttu-id="caa80-111">项目估算</span><span class="sxs-lookup"><span data-stu-id="caa80-111">Project estimates</span></span>
- <span data-ttu-id="caa80-112">项目支出估计值</span><span class="sxs-lookup"><span data-stu-id="caa80-112">Project expense estimates</span></span>

## <a name="project-properties"></a><span data-ttu-id="caa80-113">项目属性</span><span class="sxs-lookup"><span data-stu-id="caa80-113">Project properties</span></span>

<span data-ttu-id="caa80-114">在复制项目时，会复制以下字段中的值：</span><span class="sxs-lookup"><span data-stu-id="caa80-114">When the project is copied, the values in the following fields are copied:</span></span>

- <span data-ttu-id="caa80-115">客户</span><span class="sxs-lookup"><span data-stu-id="caa80-115">Name</span></span>
- <span data-ttu-id="caa80-116">描述</span><span class="sxs-lookup"><span data-stu-id="caa80-116">Description</span></span>
- <span data-ttu-id="caa80-117">客户</span><span class="sxs-lookup"><span data-stu-id="caa80-117">Customer</span></span>
- <span data-ttu-id="caa80-118">日历模板</span><span class="sxs-lookup"><span data-stu-id="caa80-118">Calendar Template</span></span>
- <span data-ttu-id="caa80-119">货币</span><span class="sxs-lookup"><span data-stu-id="caa80-119">Currency</span></span>
- <span data-ttu-id="caa80-120">合同签订部门</span><span class="sxs-lookup"><span data-stu-id="caa80-120">Contracting Unit</span></span>
- <span data-ttu-id="caa80-121">项目经理</span><span class="sxs-lookup"><span data-stu-id="caa80-121">Project Manager</span></span>
- <span data-ttu-id="caa80-122">状态 </span><span class="sxs-lookup"><span data-stu-id="caa80-122">Status</span></span>
- <span data-ttu-id="caa80-123">总体项目状态</span><span class="sxs-lookup"><span data-stu-id="caa80-123">Overall Project Status</span></span>
- <span data-ttu-id="caa80-124">注释 </span><span class="sxs-lookup"><span data-stu-id="caa80-124">Comments</span></span>
- <span data-ttu-id="caa80-125">估算</span><span class="sxs-lookup"><span data-stu-id="caa80-125">Estimates</span></span>
- <span data-ttu-id="caa80-126">预计开始日期</span><span class="sxs-lookup"><span data-stu-id="caa80-126">Estimated Start Date</span></span>
- <span data-ttu-id="caa80-127">完成日期</span><span class="sxs-lookup"><span data-stu-id="caa80-127">Finish Date</span></span>
- <span data-ttu-id="caa80-128">工作量(小时)</span><span class="sxs-lookup"><span data-stu-id="caa80-128">Effort (Hours)</span></span>
- <span data-ttu-id="caa80-129">估算人工成本</span><span class="sxs-lookup"><span data-stu-id="caa80-129">Estimated Labor Cost</span></span>
- <span data-ttu-id="caa80-130">估算支出成本</span><span class="sxs-lookup"><span data-stu-id="caa80-130">Estimated Expense Cost</span></span>

## <a name="work-breakdown-structure"></a><span data-ttu-id="caa80-131">工作分解结构</span><span class="sxs-lookup"><span data-stu-id="caa80-131">Work breakdown structure</span></span>

<span data-ttu-id="caa80-132">复制项目时，会复制整个已加载资源的工作分解结构。</span><span class="sxs-lookup"><span data-stu-id="caa80-132">When the project is copied, the entire resource-loaded work breakdown structure is copied.</span></span> <span data-ttu-id="caa80-133">指定资源将替换为通用资源。</span><span class="sxs-lookup"><span data-stu-id="caa80-133">Named resources are replaced with generic resources.</span></span> <span data-ttu-id="caa80-134">如果指定资源与通用资源没有相同的工作时间，则将重新计算计划，任务持续时间可能会更改。</span><span class="sxs-lookup"><span data-stu-id="caa80-134">If the named resources don't have the same working hours as the generic resource, the schedule will be recalculated and task durations may change.</span></span>

## <a name="project-team-members"></a><span data-ttu-id="caa80-135">项目团队成员</span><span class="sxs-lookup"><span data-stu-id="caa80-135">Project team members</span></span>

<span data-ttu-id="caa80-136">从源项目复制项目团队时，将复制通用资源。</span><span class="sxs-lookup"><span data-stu-id="caa80-136">When a project team is copied from the source project, the generic resources are copied.</span></span> <span data-ttu-id="caa80-137">通用资源分派也与源项目中一样进行维护。</span><span class="sxs-lookup"><span data-stu-id="caa80-137">Generic resource assignments are also maintained as they were in the source project.</span></span> <span data-ttu-id="caa80-138">指定资源将转换为通用团队成员。</span><span class="sxs-lookup"><span data-stu-id="caa80-138">Named resources will be converted to generic team members.</span></span>

## <a name="estimates"></a><span data-ttu-id="caa80-139">估算</span><span class="sxs-lookup"><span data-stu-id="caa80-139">Estimates</span></span>

<span data-ttu-id="caa80-140">复制项目时，将从源项目复制资源和支出估算行。</span><span class="sxs-lookup"><span data-stu-id="caa80-140">When the project is copied, both resource and expense estimate lines are copied from the source project.</span></span> 

<span data-ttu-id="caa80-141">有关如何以编程方式访问“复制项目”的信息，请参阅[使用“复制项目”开发项目模板](dev-copy-project.md)。</span><span class="sxs-lookup"><span data-stu-id="caa80-141">For information on how to programmatically access Copy Project, see [Develop project templates with Copy Project](dev-copy-project.md).</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
