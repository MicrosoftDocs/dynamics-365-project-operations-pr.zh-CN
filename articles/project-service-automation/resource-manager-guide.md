---
title: 资源经理指南
description: Project Service 的资源管理指南
author: JohnPBurrows
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: 4a3f3fa7-ae1a-4139-974b-f61cc8a8bda7
ms.author: jburrows
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 67b400fe3e6bb60775ee144c1d3720a311204d7d
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/24/2020
ms.locfileid: "3749780"
---
# <a name="resource-manager-guide-project-service"></a><span data-ttu-id="f236b-103">资源经理指南 (Project Service)</span><span class="sxs-lookup"><span data-stu-id="f236b-103">Resource manager guide (Project Service)</span></span>

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="f236b-104">[!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] 中的[!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]功能帮助您为项目找到适当时间的适当资源，并确保所有资源均可高效利用。</span><span class="sxs-lookup"><span data-stu-id="f236b-104">The [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] capabilities in [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] help you find the right resources at the right time for the right project and make sure all resources are utilized efficiently.</span></span>  
  
 <span data-ttu-id="f236b-105">使用 [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]高效、有效地安排公司的顾问。</span><span class="sxs-lookup"><span data-stu-id="f236b-105">Deploy your company’s consultants efficiently and effectively with the [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span></span> <span data-ttu-id="f236b-106">这些基于咨询项目的要求和日程安排，以及顾问的技能和可用性，为您提供安排资源所需的工具。</span><span class="sxs-lookup"><span data-stu-id="f236b-106">These provide you with the tools you need to schedule resources based on the requirements and schedules of consulting projects and on the skills and availability of your consultants.</span></span> <span data-ttu-id="f236b-107">您可以迅速找到最适合处理项目的顾问，也可以轻松了解如何在各项目实施期间改善日程安排。</span><span class="sxs-lookup"><span data-stu-id="f236b-107">You can quickly find the most qualified consultants who are available to work on projects, and you can easily see how to better schedule them during the course of each project.</span></span>  
  
 <span data-ttu-id="f236b-108">资源日程安排帮助您执行以下操作：</span><span class="sxs-lookup"><span data-stu-id="f236b-108">Resource scheduling helps you do the following:</span></span>  
  
- <span data-ttu-id="f236b-109">基于资源的技能和熟练程度级别与项目的资源要求之间的契合程度，将资源与项目配对。</span><span class="sxs-lookup"><span data-stu-id="f236b-109">Match resources to projects, based on how well their skills and proficiency levels match the project resource requirements.</span></span>  
  
- <span data-ttu-id="f236b-110">基于资源的可用性和安排的休假，将资源的日程安排与项目日历配对。</span><span class="sxs-lookup"><span data-stu-id="f236b-110">Match a resource’s schedule to a project calendar, based on their availability and scheduled time off.</span></span> <span data-ttu-id="f236b-111">颜色编码的日历提供有关资源可用性的视觉提示。</span><span class="sxs-lookup"><span data-stu-id="f236b-111">The color-coded calendar gives you visual cues about resource availability.</span></span>  
  
- <span data-ttu-id="f236b-112">查看各个顾问的产能并确定当前如何使用该产能。</span><span class="sxs-lookup"><span data-stu-id="f236b-112">Review the capacity of each consultant and determine how that capacity is currently used.</span></span> <span data-ttu-id="f236b-113">这有助您了解顾问在哪些方面利用不充分或利用过度，以及顾问是否发挥了其产能。</span><span class="sxs-lookup"><span data-stu-id="f236b-113">This can help you find where a consultant might be under- or over-utilized, or if they’re working at capacity.</span></span>  
  
- <span data-ttu-id="f236b-114">将工作人员的产能百分比或具体的产能时数分派给项目。</span><span class="sxs-lookup"><span data-stu-id="f236b-114">Assign a percentage or a specific number of hours for a worker’s capacity to a project.</span></span>  
  
- <span data-ttu-id="f236b-115">进行组资源预订。</span><span class="sxs-lookup"><span data-stu-id="f236b-115">Make group resource bookings.</span></span>  
  
- <span data-ttu-id="f236b-116">一步软预订或硬预订资源并将软预订的时数转换为硬预订的时数。</span><span class="sxs-lookup"><span data-stu-id="f236b-116">Soft book or hard book resources, and convert soft-booked hours into hard-booked hours in one step.</span></span>  
  
- <span data-ttu-id="f236b-117">基于项目的工作分解结构中定义的资源自动组建项目团队。</span><span class="sxs-lookup"><span data-stu-id="f236b-117">Automatically form a project team based on resources defined in a work breakdown structure for a project.</span></span>  
  
- <span data-ttu-id="f236b-118">实施资源请求（预订、建议、查找替补资源）。</span><span class="sxs-lookup"><span data-stu-id="f236b-118">Fulfill resource requests (book, propose, find substitute resources).</span></span>  
  
- <span data-ttu-id="f236b-119">根据中央模型分派资源（资源管理员分派）或根据混合模型分派资源（资源管理员和其他管理员可分派）。</span><span class="sxs-lookup"><span data-stu-id="f236b-119">Assign resources according to a central (resource manager assigns) or hybrid model (resource manager and other managers can assign).</span></span> <span data-ttu-id="f236b-120">有关设置中央资源管理模型与混合资源管理模型对比的详细信息，请参阅[配置更多参数设置 (Project Service)](../project-service/configure-additional-parameters-settings.md)。</span><span class="sxs-lookup"><span data-stu-id="f236b-120">For more information about setting a central versus hybrid resource management model, see [Configure additional parameters settings (Project Service)](../project-service/configure-additional-parameters-settings.md).</span></span>  
  
  <span data-ttu-id="f236b-121">您可以有效管理多个项目的资源，并确保为项目配备合适的人员。</span><span class="sxs-lookup"><span data-stu-id="f236b-121">You can manage resources efficiently across projects and ensure that projects are staffed appropriately.</span></span> <span data-ttu-id="f236b-122">您需要执行下列任务：</span><span class="sxs-lookup"><span data-stu-id="f236b-122">You’ll need to perform the following tasks:</span></span>  
  
- <span data-ttu-id="f236b-123">[管理资源请求](../project-service/manage-resource-requests.md)。</span><span class="sxs-lookup"><span data-stu-id="f236b-123">[Manage resource requests](../project-service/manage-resource-requests.md).</span></span> <span data-ttu-id="f236b-124">将顾问的技能和熟练程度与正确的项目配对。</span><span class="sxs-lookup"><span data-stu-id="f236b-124">Match the skills and proficiencies of your consultants to the right projects.</span></span>  
  
- <span data-ttu-id="f236b-125">[查看资源可用性](../project-service/view-resource-availability.md)。</span><span class="sxs-lookup"><span data-stu-id="f236b-125">[View resource availability](../project-service/view-resource-availability.md).</span></span> <span data-ttu-id="f236b-126">通过日历视图检查顾问的可用性。</span><span class="sxs-lookup"><span data-stu-id="f236b-126">Check consultants’ availability in a calendar view.</span></span>  
  
- <span data-ttu-id="f236b-127">[查看资源利用率](../project-service/view-resource-utilization.md)。</span><span class="sxs-lookup"><span data-stu-id="f236b-127">[View resource utilization](../project-service/view-resource-utilization.md).</span></span> <span data-ttu-id="f236b-128">查看顾问的当前已预订时间百分比。</span><span class="sxs-lookup"><span data-stu-id="f236b-128">See the percentage of time that your consultants are currently booked.</span></span>  
  
- <span data-ttu-id="f236b-129">[为项目安排资源](../project-service/schedule-resources-project.md)。</span><span class="sxs-lookup"><span data-stu-id="f236b-129">[Schedule resources for a project](../project-service/schedule-resources-project.md).</span></span> <span data-ttu-id="f236b-130">为项目安排咨询人员的时间表。</span><span class="sxs-lookup"><span data-stu-id="f236b-130">Schedule consultants for a project.</span></span>  
  
  <span data-ttu-id="f236b-131">有关提交单个项目的资源请求的详细信息，请参阅[提交资源请求](../project-service/submit-resource-requests.md)。</span><span class="sxs-lookup"><span data-stu-id="f236b-131">For more information about submitting resource requests for individual projects, see [Submit resource requests](../project-service/submit-resource-requests.md).</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="f236b-132">另请参阅</span><span class="sxs-lookup"><span data-stu-id="f236b-132">See Also</span></span>  
 <span data-ttu-id="f236b-133">[Project Service 概述](../project-service/overview.md) </span><span class="sxs-lookup"><span data-stu-id="f236b-133">[Overview of Project Service](../project-service/overview.md) </span></span>  
 <span data-ttu-id="f236b-134">[管理员指南](../project-service/admin-guide.md) </span><span class="sxs-lookup"><span data-stu-id="f236b-134">[Administrator Guide](../project-service/admin-guide.md) </span></span>  
 <span data-ttu-id="f236b-135">[客户经理指南](../project-service/account-manager-guide.md) </span><span class="sxs-lookup"><span data-stu-id="f236b-135">[Account Manager Guiden](../project-service/account-manager-guide.md) </span></span>  
 <span data-ttu-id="f236b-136">[项目经理指南](../project-service/project-manager-guide.md) </span><span class="sxs-lookup"><span data-stu-id="f236b-136">[Project Manager Guide](../project-service/project-manager-guide.md) </span></span>  
 [<span data-ttu-id="f236b-137">时间、费用和协作指南</span><span class="sxs-lookup"><span data-stu-id="f236b-137">Time, Expense, and Collaboration Guide</span></span>](../project-service/time-expense-collaboration-guide.md)
