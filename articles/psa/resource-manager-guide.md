---
title: 资源经理指南
description: Project Service 的资源管理指南
author: JohnPBurrows
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 04ee87e5b1a2cf96434f4862e07d2b85bad9eace
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/28/2020
ms.locfileid: "4123997"
---
# <a name="resource-manager-guide-project-service"></a><span data-ttu-id="32c0f-103">资源经理指南 (Project Service)</span><span class="sxs-lookup"><span data-stu-id="32c0f-103">Resource manager guide (Project Service)</span></span>

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="32c0f-104">[!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] 中的[!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]功能帮助您为项目找到适当时间的适当资源，并确保所有资源均可高效利用。</span><span class="sxs-lookup"><span data-stu-id="32c0f-104">The [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] capabilities in [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] help you find the right resources at the right time for the right project and make sure all resources are utilized efficiently.</span></span>  
  
 <span data-ttu-id="32c0f-105">使用 [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]高效、有效地安排公司的顾问。</span><span class="sxs-lookup"><span data-stu-id="32c0f-105">Deploy your company’s consultants efficiently and effectively with the [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span></span> <span data-ttu-id="32c0f-106">这些基于咨询项目的要求和日程安排，以及顾问的技能和可用性，为您提供安排资源所需的工具。</span><span class="sxs-lookup"><span data-stu-id="32c0f-106">These provide you with the tools you need to schedule resources based on the requirements and schedules of consulting projects and on the skills and availability of your consultants.</span></span> <span data-ttu-id="32c0f-107">您可以迅速找到最适合处理项目的顾问，也可以轻松了解如何在各项目实施期间改善日程安排。</span><span class="sxs-lookup"><span data-stu-id="32c0f-107">You can quickly find the most qualified consultants who are available to work on projects, and you can easily see how to better schedule them during the course of each project.</span></span>  
  
 <span data-ttu-id="32c0f-108">资源日程安排帮助您执行以下操作：</span><span class="sxs-lookup"><span data-stu-id="32c0f-108">Resource scheduling helps you do the following:</span></span>  
  
- <span data-ttu-id="32c0f-109">基于资源的技能和熟练程度级别与项目的资源要求之间的契合程度，将资源与项目配对。</span><span class="sxs-lookup"><span data-stu-id="32c0f-109">Match resources to projects, based on how well their skills and proficiency levels match the project resource requirements.</span></span>  
  
- <span data-ttu-id="32c0f-110">基于资源的可用性和安排的休假，将资源的日程安排与项目日历配对。</span><span class="sxs-lookup"><span data-stu-id="32c0f-110">Match a resource’s schedule to a project calendar, based on their availability and scheduled time off.</span></span> <span data-ttu-id="32c0f-111">颜色编码的日历提供有关资源可用性的视觉提示。</span><span class="sxs-lookup"><span data-stu-id="32c0f-111">The color-coded calendar gives you visual cues about resource availability.</span></span>  
  
- <span data-ttu-id="32c0f-112">查看各个顾问的产能并确定当前如何使用该产能。</span><span class="sxs-lookup"><span data-stu-id="32c0f-112">Review the capacity of each consultant and determine how that capacity is currently used.</span></span> <span data-ttu-id="32c0f-113">这有助您了解顾问在哪些方面利用不充分或利用过度，以及顾问是否发挥了其产能。</span><span class="sxs-lookup"><span data-stu-id="32c0f-113">This can help you find where a consultant might be under- or over-utilized, or if they’re working at capacity.</span></span>  
  
- <span data-ttu-id="32c0f-114">将工作人员的产能百分比或具体的产能时数分派给项目。</span><span class="sxs-lookup"><span data-stu-id="32c0f-114">Assign a percentage or a specific number of hours for a worker’s capacity to a project.</span></span>  
  
- <span data-ttu-id="32c0f-115">进行组资源预订。</span><span class="sxs-lookup"><span data-stu-id="32c0f-115">Make group resource bookings.</span></span>  
  
- <span data-ttu-id="32c0f-116">一步软预订或硬预订资源并将软预订的时数转换为硬预订的时数。</span><span class="sxs-lookup"><span data-stu-id="32c0f-116">Soft book or hard book resources, and convert soft-booked hours into hard-booked hours in one step.</span></span>  
  
- <span data-ttu-id="32c0f-117">基于项目的工作分解结构中定义的资源自动组建项目团队。</span><span class="sxs-lookup"><span data-stu-id="32c0f-117">Automatically form a project team based on resources defined in a work breakdown structure for a project.</span></span>  
  
- <span data-ttu-id="32c0f-118">实施资源请求（预订、建议、查找替补资源）。</span><span class="sxs-lookup"><span data-stu-id="32c0f-118">Fulfill resource requests (book, propose, find substitute resources).</span></span>  
  
- <span data-ttu-id="32c0f-119">根据中央模型分派资源（资源管理员分派）或根据混合模型分派资源（资源管理员和其他管理员可分派）。</span><span class="sxs-lookup"><span data-stu-id="32c0f-119">Assign resources according to a central (resource manager assigns) or hybrid model (resource manager and other managers can assign).</span></span> <span data-ttu-id="32c0f-120">有关设置中央资源管理模型与混合资源管理模型对比的详细信息，请参阅[配置更多参数设置 (Project Service)](../psa/configure-additional-parameters-settings.md)。</span><span class="sxs-lookup"><span data-stu-id="32c0f-120">For more information about setting a central versus hybrid resource management model, see [Configure additional parameters settings (Project Service)](../psa/configure-additional-parameters-settings.md).</span></span>  
  
  <span data-ttu-id="32c0f-121">您可以有效管理多个项目的资源，并确保为项目配备合适的人员。</span><span class="sxs-lookup"><span data-stu-id="32c0f-121">You can manage resources efficiently across projects and ensure that projects are staffed appropriately.</span></span> <span data-ttu-id="32c0f-122">您需要执行下列任务：</span><span class="sxs-lookup"><span data-stu-id="32c0f-122">You’ll need to perform the following tasks:</span></span>  
  
- <span data-ttu-id="32c0f-123">[管理资源请求](../psa/manage-resource-requests.md)。</span><span class="sxs-lookup"><span data-stu-id="32c0f-123">[Manage resource requests](../psa/manage-resource-requests.md).</span></span> <span data-ttu-id="32c0f-124">将顾问的技能和熟练程度与正确的项目配对。</span><span class="sxs-lookup"><span data-stu-id="32c0f-124">Match the skills and proficiencies of your consultants to the right projects.</span></span>  
  
- <span data-ttu-id="32c0f-125">[查看资源可用性](../psa/view-resource-availability.md)。</span><span class="sxs-lookup"><span data-stu-id="32c0f-125">[View resource availability](../psa/view-resource-availability.md).</span></span> <span data-ttu-id="32c0f-126">通过日历视图检查顾问的可用性。</span><span class="sxs-lookup"><span data-stu-id="32c0f-126">Check consultants’ availability in a calendar view.</span></span>  
  
- <span data-ttu-id="32c0f-127">[查看资源利用率](../psa/view-resource-utilization.md)。</span><span class="sxs-lookup"><span data-stu-id="32c0f-127">[View resource utilization](../psa/view-resource-utilization.md).</span></span> <span data-ttu-id="32c0f-128">查看顾问的当前已预订时间百分比。</span><span class="sxs-lookup"><span data-stu-id="32c0f-128">See the percentage of time that your consultants are currently booked.</span></span>  
  
- <span data-ttu-id="32c0f-129">[为项目安排资源](../psa/schedule-resources-project.md)。</span><span class="sxs-lookup"><span data-stu-id="32c0f-129">[Schedule resources for a project](../psa/schedule-resources-project.md).</span></span> <span data-ttu-id="32c0f-130">为项目安排咨询人员的时间表。</span><span class="sxs-lookup"><span data-stu-id="32c0f-130">Schedule consultants for a project.</span></span>  
  
  <span data-ttu-id="32c0f-131">有关提交单个项目的资源请求的详细信息，请参阅[提交资源请求](../psa/submit-resource-requests.md)。</span><span class="sxs-lookup"><span data-stu-id="32c0f-131">For more information about submitting resource requests for individual projects, see [Submit resource requests](../psa/submit-resource-requests.md).</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="32c0f-132">另请参阅</span><span class="sxs-lookup"><span data-stu-id="32c0f-132">See Also</span></span>  
 <span data-ttu-id="32c0f-133">[Project Service 概述](../psa/overview.md) </span><span class="sxs-lookup"><span data-stu-id="32c0f-133">[Overview of Project Service](../psa/overview.md) </span></span>  
 <span data-ttu-id="32c0f-134">[管理员指南](../psa/admin-guide.md) </span><span class="sxs-lookup"><span data-stu-id="32c0f-134">[Administrator Guide](../psa/admin-guide.md) </span></span>  
 <span data-ttu-id="32c0f-135">[客户经理指南](../psa/account-manager-guide.md) </span><span class="sxs-lookup"><span data-stu-id="32c0f-135">[Account Manager Guiden](../psa/account-manager-guide.md) </span></span>  
 <span data-ttu-id="32c0f-136">[项目经理指南](../psa/project-manager-guide.md) </span><span class="sxs-lookup"><span data-stu-id="32c0f-136">[Project Manager Guide](../psa/project-manager-guide.md) </span></span>  
 [<span data-ttu-id="32c0f-137">时间、费用和协作指南</span><span class="sxs-lookup"><span data-stu-id="32c0f-137">Time, Expense, and Collaboration Guide</span></span>](../psa/time-expense-collaboration-guide.md)
