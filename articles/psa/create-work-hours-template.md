---
title: 创建工作时间模板
description: 本主题介绍如何在 Project Service 中创建工作时间模板。
author: ruhercul
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
ms.openlocfilehash: 105e3cb2ef7b904e96dc21013906e0b7444e3b88
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/10/2021
ms.locfileid: "5997185"
---
# <a name="create-a-work-hours-template-project-service"></a><span data-ttu-id="9096b-103">创建工作时间模板 (Project Service)</span><span class="sxs-lookup"><span data-stu-id="9096b-103">Create a work hours template (Project Service)</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="9096b-104">若要创建和管理项目，必须将日历模板应用于该项目。</span><span class="sxs-lookup"><span data-stu-id="9096b-104">To create and manage a project, you must apply a calendar template to the project.</span></span> <span data-ttu-id="9096b-105">日历模板定义以下项目属性：</span><span class="sxs-lookup"><span data-stu-id="9096b-105">The calendar template defines the following project attributes:</span></span>

- <span data-ttu-id="9096b-106">工作时数，包括开始和结束时间</span><span class="sxs-lookup"><span data-stu-id="9096b-106">Working hours, including start and end time</span></span>
- <span data-ttu-id="9096b-107">工作天数</span><span class="sxs-lookup"><span data-stu-id="9096b-107">Working days</span></span>
- <span data-ttu-id="9096b-108">日历例外（如非工作日）</span><span class="sxs-lookup"><span data-stu-id="9096b-108">Calendar exceptions such as non-working days</span></span>

<span data-ttu-id="9096b-109">应用于项目的日历模板是组织设置中定义的日历模板的副本。</span><span class="sxs-lookup"><span data-stu-id="9096b-109">The calendar template that's applied to a project is a copy of the calendar template defined in your organization’s settings.</span></span>

> [!NOTE]
> <span data-ttu-id="9096b-110">如果更改日历模板，这些更改不会传播到项目的工作时间。</span><span class="sxs-lookup"><span data-stu-id="9096b-110">If you change the calendar template, those changes don't propagate to the working hours of the project.</span></span> <span data-ttu-id="9096b-111">要更改项目的工作时间，必须应用新的模板。</span><span class="sxs-lookup"><span data-stu-id="9096b-111">To change the working hours of the project, a new template must be applied.</span></span>

<span data-ttu-id="9096b-112">要为您的组织创建日历模板，有两个关键要求：</span><span class="sxs-lookup"><span data-stu-id="9096b-112">To create a calendar template for your organization, there are two key requirements:</span></span>

- <span data-ttu-id="9096b-113">使用新的或现有的可预订资源定义模板的所需工作时间。</span><span class="sxs-lookup"><span data-stu-id="9096b-113">Define the desired working hours of the template using a new or existing bookable resource.</span></span>
- <span data-ttu-id="9096b-114">创建一个新的日历模板，将该模板与可预订资源相关联。</span><span class="sxs-lookup"><span data-stu-id="9096b-114">Create a new calendar template and associate the template with the bookable resource.</span></span>

<span data-ttu-id="9096b-115">**定义模板的工作时间**</span><span class="sxs-lookup"><span data-stu-id="9096b-115">**Define the working hours of the template**</span></span>

1. <span data-ttu-id="9096b-116">转到 **资源**\>**资源**。</span><span class="sxs-lookup"><span data-stu-id="9096b-116">Go to **Resources** \> **Resources**.</span></span>
2. <span data-ttu-id="9096b-117">创建要在日历模板中引用的新资源，或选择一个现有资源。</span><span class="sxs-lookup"><span data-stu-id="9096b-117">Create a new resource to reference in the calendar template, or select an existing resource.</span></span>
3. <span data-ttu-id="9096b-118">选择资源的 **工作时间** 选项卡，完成[为资源设置工作时间](/dynamics365/field-service/set-work-hours-resource.md)中的说明配置日历规则。</span><span class="sxs-lookup"><span data-stu-id="9096b-118">Select the **Work Hours** tab of the resource and complete the instructions in [Set work hours for a resource](/dynamics365/field-service/set-work-hours-resource.md) to configure the calendar rules.</span></span>

<span data-ttu-id="9096b-119">**创建新的日历模板**</span><span class="sxs-lookup"><span data-stu-id="9096b-119">**Create a new calendar template**</span></span>

1. <span data-ttu-id="9096b-120">转到 **设置** \> **日历模板**。</span><span class="sxs-lookup"><span data-stu-id="9096b-120">Go to **Settings** \> **Calendar Template**.</span></span>
2. <span data-ttu-id="9096b-121">选择 **新建**，输入名称、说明和模板资源。</span><span class="sxs-lookup"><span data-stu-id="9096b-121">Select **New**, and enter a name, description, and template resource.</span></span>


> [!NOTE]
> <span data-ttu-id="9096b-122">在日历模板中引用资源时，该资源的日历的副本将与日历模板相关联。</span><span class="sxs-lookup"><span data-stu-id="9096b-122">When a resource is referenced in a calendar template, a copy of the resource’s calendar is associated with the calendar template.</span></span> <span data-ttu-id="9096b-123">如果所复制模板的工作时间发生更改，这些更改不会传播到日历模板。</span><span class="sxs-lookup"><span data-stu-id="9096b-123">If the working hours of the copied template change, those changes will not propagate to the calendar template.</span></span>


### <a name="see-also"></a><span data-ttu-id="9096b-124">另请参阅</span><span class="sxs-lookup"><span data-stu-id="9096b-124">See Also</span></span>  
 [<span data-ttu-id="9096b-125">设置资源</span><span class="sxs-lookup"><span data-stu-id="9096b-125">Set up resources</span></span>](../psa/set-up-resources.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
