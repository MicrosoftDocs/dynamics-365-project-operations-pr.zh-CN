---
title: 定义项目日历
description: 本主题提供有关如何将日历模板应用于项目以跟踪项目计划的信息。
author: ruhercul
ms.date: 02/05/2021
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 0d1a2c4bd2d4022bbf79afcef79170eb482e6418
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/10/2021
ms.locfileid: "5998985"
---
# <a name="define-project-calendars"></a><span data-ttu-id="b27fc-103">定义项目日历</span><span class="sxs-lookup"><span data-stu-id="b27fc-103">Define project calendars</span></span>

<span data-ttu-id="b27fc-104">_**适用于：** 基于资源/非库存场景的 Project Operations，精简部署 - 估价开票交易_</span><span class="sxs-lookup"><span data-stu-id="b27fc-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="b27fc-105">若要创建和管理项目，必须将日历模板应用于该项目。</span><span class="sxs-lookup"><span data-stu-id="b27fc-105">To create and manage a project, you must apply a calendar template to the project.</span></span> <span data-ttu-id="b27fc-106">日历模板定义以下项目属性：</span><span class="sxs-lookup"><span data-stu-id="b27fc-106">The calendar template defines the following project attributes:</span></span>

- <span data-ttu-id="b27fc-107">工作时数，包括开始和结束时间</span><span class="sxs-lookup"><span data-stu-id="b27fc-107">Working hours, including start and end time</span></span>
- <span data-ttu-id="b27fc-108">工作天数</span><span class="sxs-lookup"><span data-stu-id="b27fc-108">Working days</span></span>
- <span data-ttu-id="b27fc-109">日历例外（如非工作日）</span><span class="sxs-lookup"><span data-stu-id="b27fc-109">Calendar exceptions such as non-working days</span></span>

<span data-ttu-id="b27fc-110">应用于项目的日历模板是组织设置中定义的日历模板的副本。</span><span class="sxs-lookup"><span data-stu-id="b27fc-110">The calendar template that's applied to a project is a copy of the calendar template defined in your organization’s settings.</span></span>

> [!NOTE]
> <span data-ttu-id="b27fc-111">如果更改日历模板，这些更改不会传播到项目的工作时间。</span><span class="sxs-lookup"><span data-stu-id="b27fc-111">If you change the calendar template, those changes don't propagate to the working hours of the project.</span></span> <span data-ttu-id="b27fc-112">要更改项目的工作时间，必须应用新的模板。</span><span class="sxs-lookup"><span data-stu-id="b27fc-112">To change the working hours of the project, a new template must be applied.</span></span>

<span data-ttu-id="b27fc-113">要为您的组织创建日历模板，有两个关键要求：</span><span class="sxs-lookup"><span data-stu-id="b27fc-113">To create a calendar template for your organization, there are two key requirements:</span></span>

- <span data-ttu-id="b27fc-114">使用新的或现有的可预订资源定义模板的所需工作时间。</span><span class="sxs-lookup"><span data-stu-id="b27fc-114">Define the desired working hours of the template using a new or existing bookable resource.</span></span>
- <span data-ttu-id="b27fc-115">创建一个新的日历模板，将该模板与可预订资源相关联。</span><span class="sxs-lookup"><span data-stu-id="b27fc-115">Create a new calendar template and associate the template with the bookable resource.</span></span>

<span data-ttu-id="b27fc-116">**定义模板的工作时间**</span><span class="sxs-lookup"><span data-stu-id="b27fc-116">**Define the working hours of the template**</span></span>

1. <span data-ttu-id="b27fc-117">转到 **资源**\>**资源**。</span><span class="sxs-lookup"><span data-stu-id="b27fc-117">Go to **Resources** \> **Resources**.</span></span>
2. <span data-ttu-id="b27fc-118">创建要在日历模板中引用的新资源，或选择一个现有资源。</span><span class="sxs-lookup"><span data-stu-id="b27fc-118">Create a new resource to reference in the calendar template, or select an existing resource.</span></span>
3. <span data-ttu-id="b27fc-119">选择资源的 **工作时间** 选项卡，完成[为资源设置工作时间](/dynamics365/field-service/set-work-hours-resource.md)中的说明配置日历规则。</span><span class="sxs-lookup"><span data-stu-id="b27fc-119">Select the **Work Hours** tab of the resource and complete the instructions in [Set work hours for a resource](/dynamics365/field-service/set-work-hours-resource.md) to configure the calendar rules.</span></span>

<span data-ttu-id="b27fc-120">**创建新的日历模板**</span><span class="sxs-lookup"><span data-stu-id="b27fc-120">**Create a new calendar template**</span></span>

1. <span data-ttu-id="b27fc-121">转到 **设置** \> **日历模板**。</span><span class="sxs-lookup"><span data-stu-id="b27fc-121">Go to **Settings** \> **Calendar Template**.</span></span>
2. <span data-ttu-id="b27fc-122">选择 **新建**，输入名称、说明和模板资源。</span><span class="sxs-lookup"><span data-stu-id="b27fc-122">Select **New**, and enter a name, description, and template resource.</span></span>

> [!NOTE]
> <span data-ttu-id="b27fc-123">在日历模板中引用资源时，该资源的日历的副本将与日历模板相关联。</span><span class="sxs-lookup"><span data-stu-id="b27fc-123">When a resource is referenced in a calendar template, a copy of the resource’s calendar is associated with the calendar template.</span></span> <span data-ttu-id="b27fc-124">如果所复制模板的工作时间发生更改，这些更改不会传播到日历模板。</span><span class="sxs-lookup"><span data-stu-id="b27fc-124">If the working hours of the copied template change, those changes will not propagate to the calendar template.</span></span>

<span data-ttu-id="b27fc-125">现在可将此工作模板与项目日历模板关联。</span><span class="sxs-lookup"><span data-stu-id="b27fc-125">You can now associate the work template with a project calendar template.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]

