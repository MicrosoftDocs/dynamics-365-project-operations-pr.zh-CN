---
title: 复制项目
description: 本主题提供有关在 Dynamics 365 Project Operations 中复制项目的信息。
author: ruhercul
ms.date: 05/21/2021
ms.topic: article
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: c3055ab5b8c07faa2bc9167956d283e2a66029dd
ms.sourcegitcommit: 173f2b1f4e063c440a5f78d76d456c62aadbd89e
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/24/2021
ms.locfileid: "6091243"
---
# <a name="copy-a-project"></a><span data-ttu-id="64bf3-103">复制项目</span><span class="sxs-lookup"><span data-stu-id="64bf3-103">Copy a project</span></span>

<span data-ttu-id="64bf3-104">_**适用于：** 基于资源/非库存场景的 Project Operations，精简部署 - 估价开票交易_</span><span class="sxs-lookup"><span data-stu-id="64bf3-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="64bf3-105">使用 Dynamics 365 Project Operations，可以通过选择 **项目** 窗体上的 **复制项目** 快速生成新项目。</span><span class="sxs-lookup"><span data-stu-id="64bf3-105">With Dynamics 365 Project Operations, you can quickly build new projects by selecting **Copy Project** on the **Projects** form.</span></span> <span data-ttu-id="64bf3-106">若要复制项目，请打开要复制的项目，然后选择 **复制项目**。</span><span class="sxs-lookup"><span data-stu-id="64bf3-106">To copy a project, open the project you want to copy, and then select **Copy project**.</span></span> <span data-ttu-id="64bf3-107">该操作将复制以下内容：</span><span class="sxs-lookup"><span data-stu-id="64bf3-107">The action will copy the following:</span></span>

- <span data-ttu-id="64bf3-108">项目属性</span><span class="sxs-lookup"><span data-stu-id="64bf3-108">Project properties</span></span> 
- <span data-ttu-id="64bf3-109">工作分解结构</span><span class="sxs-lookup"><span data-stu-id="64bf3-109">Work breakdown structure</span></span>
- <span data-ttu-id="64bf3-110">项目团队成员</span><span class="sxs-lookup"><span data-stu-id="64bf3-110">Project team members</span></span>
- <span data-ttu-id="64bf3-111">项目估算</span><span class="sxs-lookup"><span data-stu-id="64bf3-111">Project estimates</span></span>
- <span data-ttu-id="64bf3-112">项目支出估计值</span><span class="sxs-lookup"><span data-stu-id="64bf3-112">Project expense estimates</span></span>
- <span data-ttu-id="64bf3-113">项目材料估算</span><span class="sxs-lookup"><span data-stu-id="64bf3-113">Project material estimates</span></span>

## <a name="project-properties"></a><span data-ttu-id="64bf3-114">项目属性</span><span class="sxs-lookup"><span data-stu-id="64bf3-114">Project properties</span></span>

<span data-ttu-id="64bf3-115">在复制项目时，会复制以下字段中的值：</span><span class="sxs-lookup"><span data-stu-id="64bf3-115">When the project is copied, the values in the following fields are copied:</span></span>

- <span data-ttu-id="64bf3-116">客户</span><span class="sxs-lookup"><span data-stu-id="64bf3-116">Name</span></span>
- <span data-ttu-id="64bf3-117">描述</span><span class="sxs-lookup"><span data-stu-id="64bf3-117">Description</span></span>
- <span data-ttu-id="64bf3-118">客户</span><span class="sxs-lookup"><span data-stu-id="64bf3-118">Customer</span></span>
- <span data-ttu-id="64bf3-119">日历模板</span><span class="sxs-lookup"><span data-stu-id="64bf3-119">Calendar Template</span></span>
- <span data-ttu-id="64bf3-120">货币</span><span class="sxs-lookup"><span data-stu-id="64bf3-120">Currency</span></span>
- <span data-ttu-id="64bf3-121">合同签订部门</span><span class="sxs-lookup"><span data-stu-id="64bf3-121">Contracting Unit</span></span>
- <span data-ttu-id="64bf3-122">项目经理</span><span class="sxs-lookup"><span data-stu-id="64bf3-122">Project Manager</span></span>
- <span data-ttu-id="64bf3-123">状态 </span><span class="sxs-lookup"><span data-stu-id="64bf3-123">Status</span></span>
- <span data-ttu-id="64bf3-124">总体项目状态</span><span class="sxs-lookup"><span data-stu-id="64bf3-124">Overall Project Status</span></span>
- <span data-ttu-id="64bf3-125">注释 </span><span class="sxs-lookup"><span data-stu-id="64bf3-125">Comments</span></span>
- <span data-ttu-id="64bf3-126">估计值</span><span class="sxs-lookup"><span data-stu-id="64bf3-126">Estimates</span></span>
- <span data-ttu-id="64bf3-127">预计开始日期：这是利用副本创建项目的日期。</span><span class="sxs-lookup"><span data-stu-id="64bf3-127">Estimated Start Date: This is the date that the project is created from the copy.</span></span>
- <span data-ttu-id="64bf3-128">预计完成日期：此日期根据从副本制作的新项目的开始日期进行调整。</span><span class="sxs-lookup"><span data-stu-id="64bf3-128">Estimated Finish Date: This date is adjusted based on the start date of the new project that was made from the copy.</span></span>
- <span data-ttu-id="64bf3-129">工作量(小时)</span><span class="sxs-lookup"><span data-stu-id="64bf3-129">Effort (Hours)</span></span>
- <span data-ttu-id="64bf3-130">估算人工成本</span><span class="sxs-lookup"><span data-stu-id="64bf3-130">Estimated Labor Cost</span></span>
- <span data-ttu-id="64bf3-131">估算支出成本</span><span class="sxs-lookup"><span data-stu-id="64bf3-131">Estimated Expense Cost</span></span>
- <span data-ttu-id="64bf3-132">估算材料成本</span><span class="sxs-lookup"><span data-stu-id="64bf3-132">Estimated Material Cost</span></span>

> [!NOTE]
> <span data-ttu-id="64bf3-133">复制项目是一项长期操作。</span><span class="sxs-lookup"><span data-stu-id="64bf3-133">Copy project is a long running operation.</span></span> <span data-ttu-id="64bf3-134">项目记录、它们的相关属性和许多相关实体也会被复制。</span><span class="sxs-lookup"><span data-stu-id="64bf3-134">Project records, their relevant attributes, and many related entities are also copied.</span></span> <span data-ttu-id="64bf3-135">由于操作的长期性，复制开始后，目标项目页面被锁定以进行编辑，直到复制操作完成为止。</span><span class="sxs-lookup"><span data-stu-id="64bf3-135">Because of the long running nature of the operation, after the copy starts, the target project page is locked for editing until the copy operation is complete.</span></span>

## <a name="work-breakdown-structure"></a><span data-ttu-id="64bf3-136">工作分解结构</span><span class="sxs-lookup"><span data-stu-id="64bf3-136">Work breakdown structure</span></span>

<span data-ttu-id="64bf3-137">复制项目时，会复制整个已加载资源的工作分解结构。</span><span class="sxs-lookup"><span data-stu-id="64bf3-137">When the project is copied, the entire resource-loaded work breakdown structure is copied.</span></span> <span data-ttu-id="64bf3-138">指定资源将替换为通用资源。</span><span class="sxs-lookup"><span data-stu-id="64bf3-138">Named resources are replaced with generic resources.</span></span> <span data-ttu-id="64bf3-139">如果指定资源与通用资源没有相同的工作时间，则将重新计算计划，任务持续时间可能会更改。</span><span class="sxs-lookup"><span data-stu-id="64bf3-139">If the named resources don't have the same working hours as the generic resource, the schedule will be recalculated and task durations may change.</span></span>

## <a name="project-team-members"></a><span data-ttu-id="64bf3-140">项目团队成员</span><span class="sxs-lookup"><span data-stu-id="64bf3-140">Project team members</span></span>

<span data-ttu-id="64bf3-141">从源项目复制项目团队时，将复制通用资源。</span><span class="sxs-lookup"><span data-stu-id="64bf3-141">When a project team is copied from the source project, the generic resources are copied.</span></span> <span data-ttu-id="64bf3-142">通用资源分派也与源项目中一样进行维护。</span><span class="sxs-lookup"><span data-stu-id="64bf3-142">Generic resource assignments are also maintained as they were in the source project.</span></span> <span data-ttu-id="64bf3-143">指定资源将转换为通用团队成员。</span><span class="sxs-lookup"><span data-stu-id="64bf3-143">Named resources will be converted to generic team members.</span></span>

## <a name="estimates"></a><span data-ttu-id="64bf3-144">估计值</span><span class="sxs-lookup"><span data-stu-id="64bf3-144">Estimates</span></span>

<span data-ttu-id="64bf3-145">复制项目时，将从源项目复制资源、支出和材料估算行。</span><span class="sxs-lookup"><span data-stu-id="64bf3-145">When the project is copied, resource, expense and material estimate lines are copied from the source project.</span></span> 

<span data-ttu-id="64bf3-146">有关如何以编程方式访问“复制项目”的信息，请参阅[使用“复制项目”开发项目模板](dev-copy-project.md)。</span><span class="sxs-lookup"><span data-stu-id="64bf3-146">For information on how to programmatically access Copy Project, see [Develop project templates with Copy Project](dev-copy-project.md).</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
