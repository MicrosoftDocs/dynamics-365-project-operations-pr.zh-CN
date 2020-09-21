---
title: 关键概念
description: 此主题介绍 Project Service Automation 中的关键资源管理概念。
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/28/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: f5f96f65-c191-493a-aef7-df7deb52a9cb
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 4a839b828d5e1da1e5a8d8a378197b3d4932e529
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/24/2020
ms.locfileid: "3749760"
---
# <a name="key-concepts"></a><span data-ttu-id="9ed55-103">关键概念</span><span class="sxs-lookup"><span data-stu-id="9ed55-103">Key concepts</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="9ed55-104">下表定义 Dynamics 365 Project Service Automation 应用程序中使用的关键概念。</span><span class="sxs-lookup"><span data-stu-id="9ed55-104">The following table defines key concepts that are used in the Dynamics 365 Project Service Automation app.</span></span>

| <span data-ttu-id="9ed55-105">概念</span><span class="sxs-lookup"><span data-stu-id="9ed55-105">Concept</span></span>                    | <span data-ttu-id="9ed55-106">定义</span><span class="sxs-lookup"><span data-stu-id="9ed55-106">Definition</span></span> |
|----------------------------|------------|
| <span data-ttu-id="9ed55-107">项目团队成员</span><span class="sxs-lookup"><span data-stu-id="9ed55-107">Project team member</span></span>        | <span data-ttu-id="9ed55-108">在项目团队中，一个项目团队成员可以是拥有预订的指定资源，没有预订的指定资源，或通用资源。</span><span class="sxs-lookup"><span data-stu-id="9ed55-108">As part of the project team, a project team member can be a named resource that has bookings, a named resource that doesn't have bookings, or a generic resource.</span></span> <span data-ttu-id="9ed55-109">通用资源没有预订，位于项目本地，并且在项目中没有产能约束。</span><span class="sxs-lookup"><span data-stu-id="9ed55-109">Generic resources don't have bookings, are local to the project, and don't have capacity constraints across projects.</span></span> |
| <span data-ttu-id="9ed55-110">项目通用资源</span><span class="sxs-lookup"><span data-stu-id="9ed55-110">Project generic resource</span></span>   | <span data-ttu-id="9ed55-111">资源占位符，用于在不必知道指定资源的情况下组建团队和为项目安排人员。</span><span class="sxs-lookup"><span data-stu-id="9ed55-111">A resource placeholder that lets you form a team and staff a project plan without having to know the named resource.</span></span> <span data-ttu-id="9ed55-112">项目日历用作通用资源的日历。</span><span class="sxs-lookup"><span data-stu-id="9ed55-112">The project calendar is used as the generic resource's calendar.</span></span> <span data-ttu-id="9ed55-113">可将通用资源添加到项目团队并分派给任务。</span><span class="sxs-lookup"><span data-stu-id="9ed55-113">Generic resources can be added to a project team and assigned to tasks.</span></span> |
| <span data-ttu-id="9ed55-114">预订的工时数</span><span class="sxs-lookup"><span data-stu-id="9ed55-114">Booked hours</span></span>               | <span data-ttu-id="9ed55-115">资源工时数是为项目硬预订来帮助确保完成项目工作。</span><span class="sxs-lookup"><span data-stu-id="9ed55-115">Resource hours are hard-booked against a project to help guarantee that the project work is completed.</span></span> <span data-ttu-id="9ed55-116">预订的工时数占用资源的总产能。</span><span class="sxs-lookup"><span data-stu-id="9ed55-116">Booked hours are consumed from the resource's overall capacity.</span></span> <span data-ttu-id="9ed55-117">预订仅针对指定资源，不针对通用资源。</span><span class="sxs-lookup"><span data-stu-id="9ed55-117">Bookings are against named resources only, not against generic resources.</span></span> |
| <span data-ttu-id="9ed55-118">分派的工时数</span><span class="sxs-lookup"><span data-stu-id="9ed55-118">Assigned hours</span></span>             | <span data-ttu-id="9ed55-119">资源工时数分派给项目计划中的任务。</span><span class="sxs-lookup"><span data-stu-id="9ed55-119">Resource hours are assigned to tasks in the project schedule.</span></span> <span data-ttu-id="9ed55-120">分派可以针对指定资源或通用资源。</span><span class="sxs-lookup"><span data-stu-id="9ed55-120">Assignments can be against either named resources or generic resources.</span></span> <span data-ttu-id="9ed55-121">分派可以独立于预订。</span><span class="sxs-lookup"><span data-stu-id="9ed55-121">Assignments can be independent of bookings.</span></span> |
| <span data-ttu-id="9ed55-122">所需工时数</span><span class="sxs-lookup"><span data-stu-id="9ed55-122">Required hours</span></span>             | <span data-ttu-id="9ed55-123">需要，但是尚未由指定资源实施的产能。</span><span class="sxs-lookup"><span data-stu-id="9ed55-123">The capacity that is required, but that isn't yet fulfilled by a named resource.</span></span> <span data-ttu-id="9ed55-124">所需工时数仅与已生成了资源要求的通用团队成员有关。</span><span class="sxs-lookup"><span data-stu-id="9ed55-124">Required hours are relevant only for generic team members that have generated resource requirements.</span></span> |
| <span data-ttu-id="9ed55-125">需求</span><span class="sxs-lookup"><span data-stu-id="9ed55-125">Demand</span></span>                     | <span data-ttu-id="9ed55-126">当前和近期工作负荷。</span><span class="sxs-lookup"><span data-stu-id="9ed55-126">The current and incoming workload.</span></span> <span data-ttu-id="9ed55-127">在 Project Service Automation 中，需求显示为资源要求或资源请求。</span><span class="sxs-lookup"><span data-stu-id="9ed55-127">In Project Service Automation, demand is shown as resource requirements or resource requests.</span></span> |
| <span data-ttu-id="9ed55-128">资源要求</span><span class="sxs-lookup"><span data-stu-id="9ed55-128">Resource requirement</span></span>       | <span data-ttu-id="9ed55-129">一种实体，用于捕获所需资源的所需工时数、开始和结束日期、技能、地域和其他定价维度。</span><span class="sxs-lookup"><span data-stu-id="9ed55-129">An entity that is used to capture required hours, start and end dates, skills, geography, and other pricing dimensions for the required resources.</span></span> <span data-ttu-id="9ed55-130">资源要求从项目团队成员生成或单独创建。</span><span class="sxs-lookup"><span data-stu-id="9ed55-130">Resource requirements are either generated from project team members or individually created.</span></span> |
| <span data-ttu-id="9ed55-131">资源请求</span><span class="sxs-lookup"><span data-stu-id="9ed55-131">Resource request</span></span>           | <span data-ttu-id="9ed55-132">一种实体，用作“信封”来传递资源经理必须满足的资源要求。</span><span class="sxs-lookup"><span data-stu-id="9ed55-132">An entity that is used as an "envelope" to carry the resource requirement that must be fulfilled by a resource manager.</span></span> |
| <span data-ttu-id="9ed55-133">资源默认角色</span><span class="sxs-lookup"><span data-stu-id="9ed55-133">Resource default role</span></span>      | <span data-ttu-id="9ed55-134">为计算利用率将资源归入的角色。</span><span class="sxs-lookup"><span data-stu-id="9ed55-134">The role that a resource is grouped under for utilization calculation.</span></span> <span data-ttu-id="9ed55-135">假设资源拥有角色所需技能和满足该角色的目标利用率。</span><span class="sxs-lookup"><span data-stu-id="9ed55-135">The resource is assumed to have the required skills for the role and to meet the target utilization for that role.</span></span> |
| <span data-ttu-id="9ed55-136">资源部门</span><span class="sxs-lookup"><span data-stu-id="9ed55-136">Resource organization unit</span></span> | <span data-ttu-id="9ed55-137">将资源分派给的部门。</span><span class="sxs-lookup"><span data-stu-id="9ed55-137">The organizational unit that a resource is assigned to.</span></span> |
| <span data-ttu-id="9ed55-138">分布</span><span class="sxs-lookup"><span data-stu-id="9ed55-138">Contour</span></span>                    | <span data-ttu-id="9ed55-139">按天分解的任务、要求或分派工时数。</span><span class="sxs-lookup"><span data-stu-id="9ed55-139">Task, requirement, or assignment hours as they are broken down into a daily distribution.</span></span> <span data-ttu-id="9ed55-140">例如，可以将一个为期五天的 40 小时任务分布在五天，每天八小时。</span><span class="sxs-lookup"><span data-stu-id="9ed55-140">For example, a five-day, 40-hour task can be contoured into eight hours per day over five days.</span></span> |
| <span data-ttu-id="9ed55-141">协调视图</span><span class="sxs-lookup"><span data-stu-id="9ed55-141">Reconciliation view</span></span>        | <span data-ttu-id="9ed55-142">一个视图，其中显示每个项目团队成员的预订和分派。</span><span class="sxs-lookup"><span data-stu-id="9ed55-142">A view that shows the bookings and assignments for each project team member.</span></span> <span data-ttu-id="9ed55-143">项目经理可使用此视图查找预订与分派之间的不匹配，并在出现了任何不匹配时采取纠正措施。</span><span class="sxs-lookup"><span data-stu-id="9ed55-143">This view lets the project manager look for any mismatch between bookings and assignments, and to take corrective action if any mismatch occurs.</span></span> |
| <span data-ttu-id="9ed55-144">工作时间</span><span class="sxs-lookup"><span data-stu-id="9ed55-144">Work hours</span></span>                 | <span data-ttu-id="9ed55-145">一种实体，用于识别资源产能、工作时间和非工作时间。</span><span class="sxs-lookup"><span data-stu-id="9ed55-145">An entity that is used to identify resource capacity, and working and non-working hours.</span></span> <span data-ttu-id="9ed55-146">此实体也称为资源日历。</span><span class="sxs-lookup"><span data-stu-id="9ed55-146">This entity is also referred to as the resource calendar.</span></span> |
