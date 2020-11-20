---
title: 更新项目
description: 此主题提供有关在 Project Operations 中更新项目的信息。
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 8bcbc6c5a62d252398d541649647fbad49006a0c
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/28/2020
ms.locfileid: "4131422"
---
# <a name="update-a-project"></a><span data-ttu-id="0de39-103">更新项目</span><span class="sxs-lookup"><span data-stu-id="0de39-103">Update a project</span></span>

<span data-ttu-id="0de39-104">_**适用于：** 基于资源/非库存场景的 Project Operations，精简部署 - 估价开票交易_</span><span class="sxs-lookup"><span data-stu-id="0de39-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="0de39-105">以下是创建项目后可以在项目中更新的字段的摘要，以及更新的所有适用含义。</span><span class="sxs-lookup"><span data-stu-id="0de39-105">Below is a summary of the fields that can be updated on a project after it has been created and any applicable implications of the updates.</span></span>

## <a name="project-detail-fields"></a><span data-ttu-id="0de39-106">项目详细信息字段</span><span class="sxs-lookup"><span data-stu-id="0de39-106">Project detail fields</span></span>

- <span data-ttu-id="0de39-107">**名称**：项目的标题。</span><span class="sxs-lookup"><span data-stu-id="0de39-107">**Name**: The title of the project.</span></span>
- <span data-ttu-id="0de39-108">**说明**：项目的概述。</span><span class="sxs-lookup"><span data-stu-id="0de39-108">**Description**: An overview of the project.</span></span>
- <span data-ttu-id="0de39-109">**客户**：要向其交付项目的公司。</span><span class="sxs-lookup"><span data-stu-id="0de39-109">**Customer**: The company the project will be delivered to.</span></span>
- <span data-ttu-id="0de39-110">**日历模板**：项目的工作时间。</span><span class="sxs-lookup"><span data-stu-id="0de39-110">**Calendar template**: The working hours of the project.</span></span> <span data-ttu-id="0de39-111">当字段更改时，将重新计算整个计划。</span><span class="sxs-lookup"><span data-stu-id="0de39-111">When the field is changed, the entire schedule is recalculated.</span></span>
- <span data-ttu-id="0de39-112">**货币**：项目的货币。</span><span class="sxs-lookup"><span data-stu-id="0de39-112">**Currency**: The currency for the project.</span></span> <span data-ttu-id="0de39-113">此字段的默认值基于在合同签订部门定义的货币。</span><span class="sxs-lookup"><span data-stu-id="0de39-113">This field defaults based on the currency defined in the contracting unit.</span></span> <span data-ttu-id="0de39-114">当合同签订部门更新时，此字段也会更新。</span><span class="sxs-lookup"><span data-stu-id="0de39-114">When the contracting unit is updated, the field is also updated.</span></span>
- <span data-ttu-id="0de39-115">**合同签订部门**：代表主要负责赢得销售和管理对客户的工作和服务交付的公司组或部门的部门。</span><span class="sxs-lookup"><span data-stu-id="0de39-115">**Contracting Unit**: The organizational unit that represents the company group or division that is primarily responsible for winning the sale and managing the delivery of work and services to the customer.</span></span> 
- <span data-ttu-id="0de39-116">**项目经理**：有权审阅和审批时间条目和支出的项目团队成员。</span><span class="sxs-lookup"><span data-stu-id="0de39-116">**Project Manager**: The project team member who has the authority to review and approve time entries and expenses.</span></span>

## <a name="estimate-fields"></a><span data-ttu-id="0de39-117">预估字段</span><span class="sxs-lookup"><span data-stu-id="0de39-117">Estimate fields</span></span>

- <span data-ttu-id="0de39-118">**预估开始日期**：项目将开始的日期。</span><span class="sxs-lookup"><span data-stu-id="0de39-118">**Estimated Start Date**: The date that the project will begin.</span></span> <span data-ttu-id="0de39-119">更新此字段后，项目上的所有任务都会按新的开始日期按比例移动。</span><span class="sxs-lookup"><span data-stu-id="0de39-119">When this field is updated, any tasks on the project will move proportionately with the start new start date.</span></span>
- <span data-ttu-id="0de39-120">**完成日期**：项目计划结束的日期。</span><span class="sxs-lookup"><span data-stu-id="0de39-120">**Finish Date**: The date that the project is scheduled to end.</span></span>
- <span data-ttu-id="0de39-121">**工作量**：项目的预估工作量。</span><span class="sxs-lookup"><span data-stu-id="0de39-121">**Effort**: The estimated effort of the project.</span></span> <span data-ttu-id="0de39-122">在项目中添加任务后，此字段不能再进行编辑。</span><span class="sxs-lookup"><span data-stu-id="0de39-122">When tasks are added to the project, this field is no longer editable.</span></span>
- <span data-ttu-id="0de39-123">**预估人工成本**：项目的估计人工成本。</span><span class="sxs-lookup"><span data-stu-id="0de39-123">**Estimated Labor Cost**: The estimated labor cost of the project.</span></span> <span data-ttu-id="0de39-124">在项目中添加人工成本后，此字段不能再进行编辑。</span><span class="sxs-lookup"><span data-stu-id="0de39-124">When labor costs are added to the project, this field is no longer editable.</span></span>
- <span data-ttu-id="0de39-125">**预估支出**：项目的估计支出。</span><span class="sxs-lookup"><span data-stu-id="0de39-125">**Estimated Expenses**: The estimated expenses of the project.</span></span> <span data-ttu-id="0de39-126">在项目中添加支出后，此字段不能再进行编辑。</span><span class="sxs-lookup"><span data-stu-id="0de39-126">When expenses are added to the project, this field is no longer editable.</span></span>

## <a name="project-actual-fields"></a><span data-ttu-id="0de39-127">项目实际值字段</span><span class="sxs-lookup"><span data-stu-id="0de39-127">Project actual fields</span></span>
- <span data-ttu-id="0de39-128">**实际开始时间**：项目开始的日期。</span><span class="sxs-lookup"><span data-stu-id="0de39-128">**Actual Start**: The date that the project started.</span></span>
- <span data-ttu-id="0de39-129">**实际完成时间**：在项目完成时更新。</span><span class="sxs-lookup"><span data-stu-id="0de39-129">**Actual Finish**: To be updated when a project has been completed.</span></span>

## <a name="project-status-fields"></a><span data-ttu-id="0de39-130">项目状态字段</span><span class="sxs-lookup"><span data-stu-id="0de39-130">Project status fields</span></span>

- <span data-ttu-id="0de39-131">**总体项目状态**：项目经理提供的总体项目运行状况。</span><span class="sxs-lookup"><span data-stu-id="0de39-131">**Overall Project Status**: The overall project health provided by the Project manager.</span></span>
- <span data-ttu-id="0de39-132">**注释**：项目经理提供的有关当前项目运行状况的叙述。</span><span class="sxs-lookup"><span data-stu-id="0de39-132">**Comments**: A narrative regarding the current health of the project provided by the Project manager.</span></span>

