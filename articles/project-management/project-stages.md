---
title: 项目阶段
description: 此主题提供 Microsoft Dynamics Project Operations 中提供的项目阶段的相关信息。
author: ruhercul
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: a5c695e0cd39f8a222e719cc6c9ffe984fe80b07
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/15/2021
ms.locfileid: "5286777"
---
# <a name="project-stages"></a><span data-ttu-id="64cfa-103">项目阶段</span><span class="sxs-lookup"><span data-stu-id="64cfa-103">Project stages</span></span>

<span data-ttu-id="64cfa-104">_**适用于：** 基于资源/非库存场景的 Project Operations，精简部署 - 估价开票交易_</span><span class="sxs-lookup"><span data-stu-id="64cfa-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="64cfa-105">项目阶段旨在反映项目在进行中的状态。</span><span class="sxs-lookup"><span data-stu-id="64cfa-105">Project stages are designed to reflect the state of the project as it progresses.</span></span> <span data-ttu-id="64cfa-106">自定义项可用于通过业务流程、Power Automate 或插件扩展自动更新阶段。</span><span class="sxs-lookup"><span data-stu-id="64cfa-106">Customizations can be used to automatically update the stages with business process flows, Power Automate, or plug-in extensions.</span></span>

<span data-ttu-id="64cfa-107">默认业务流程流中定义了以下阶段：</span><span class="sxs-lookup"><span data-stu-id="64cfa-107">The following stages are defined in the default business process flow:</span></span>

- <span data-ttu-id="64cfa-108">新建​​</span><span class="sxs-lookup"><span data-stu-id="64cfa-108">New</span></span>
- <span data-ttu-id="64cfa-109">报价单</span><span class="sxs-lookup"><span data-stu-id="64cfa-109">Quote</span></span>
- <span data-ttu-id="64cfa-110">计划</span><span class="sxs-lookup"><span data-stu-id="64cfa-110">Plan</span></span>
- <span data-ttu-id="64cfa-111">交付</span><span class="sxs-lookup"><span data-stu-id="64cfa-111">Deliver</span></span>
- <span data-ttu-id="64cfa-112">完成</span><span class="sxs-lookup"><span data-stu-id="64cfa-112">Complete</span></span>
- <span data-ttu-id="64cfa-113">结束</span><span class="sxs-lookup"><span data-stu-id="64cfa-113">Close</span></span> 

## <a name="new"></a><span data-ttu-id="64cfa-114">新建​​</span><span class="sxs-lookup"><span data-stu-id="64cfa-114">New</span></span>

<span data-ttu-id="64cfa-115">创建项目时，项目阶段设置为 **新建**。</span><span class="sxs-lookup"><span data-stu-id="64cfa-115">When you create a project, the project stage is set to **New**.</span></span> <span data-ttu-id="64cfa-116">如果项目是从模板创建的，则项目中可能包含计划、估算和团队数据。</span><span class="sxs-lookup"><span data-stu-id="64cfa-116">If the project was created from a template, it might have schedule, estimate, and team data.</span></span> <span data-ttu-id="64cfa-117">否则，是项目的轮廓，并且必须输入其余组成部分。</span><span class="sxs-lookup"><span data-stu-id="64cfa-117">Otherwise, it's an outline of the project, and the remaining components must be entered.</span></span>

## <a name="quote"></a><span data-ttu-id="64cfa-118">报价单</span><span class="sxs-lookup"><span data-stu-id="64cfa-118">Quote</span></span>

<span data-ttu-id="64cfa-119">当您将项目与报价单关联或从报价单创建项目时，项目阶段设置为 **报价单**，并且估算的开始和结束日期也会更新。</span><span class="sxs-lookup"><span data-stu-id="64cfa-119">When you associate a project with a quote, or when you create a project from a quote, the project stage is set to **Quote**, and the estimated start and end dates are updated.</span></span> <span data-ttu-id="64cfa-120">当项目处于 **报价单** 阶段时，**项目实体** 页的 **销售** 选项卡显示报价单的详细信息。</span><span class="sxs-lookup"><span data-stu-id="64cfa-120">While the project is in the **Quote** stage, the **Sales** tab on the **Project Entity** page shows details of the quote.</span></span>

## <a name="plan"></a><span data-ttu-id="64cfa-121">规划</span><span class="sxs-lookup"><span data-stu-id="64cfa-121">Plan</span></span>

<span data-ttu-id="64cfa-122">当您获得与项目相关的报价单时，并且当项目转到 **合同** 阶段时，项目阶段将更新为 **规划**。</span><span class="sxs-lookup"><span data-stu-id="64cfa-122">When you win a quote that is associated with a project, and the project is moved to the **Contract** phase, the project stage is updated to **Plan**.</span></span> <span data-ttu-id="64cfa-123">当项目处于 **规划** 阶段时，**项目实体** 页显示合同的详细信息。</span><span class="sxs-lookup"><span data-stu-id="64cfa-123">While the project is in the **Plan** stage, the **Project Entity** page shows details of the contract.</span></span>

## <a name="deliver"></a><span data-ttu-id="64cfa-124">交付</span><span class="sxs-lookup"><span data-stu-id="64cfa-124">Deliver</span></span>

<span data-ttu-id="64cfa-125">昂项目规划完成，并且您已准备好启动项目时，项目经理应该将项目阶段更新为 **交付** 以表示项目已启动。</span><span class="sxs-lookup"><span data-stu-id="64cfa-125">When the project plan is completed, and you're ready to start the project, the project manager should update the project stage to **Deliver** to show that the project has started.</span></span>

## <a name="complete"></a><span data-ttu-id="64cfa-126">完成</span><span class="sxs-lookup"><span data-stu-id="64cfa-126">Complete</span></span> 

<span data-ttu-id="64cfa-127">当项目的工作已完成时，项目经理可以将阶段更新为 **完成**。</span><span class="sxs-lookup"><span data-stu-id="64cfa-127">When the work for the project is completed, the project manager can update the stage to **Complete**.</span></span> <span data-ttu-id="64cfa-128">项目经理可以通过将项目阶段更新为 **完成** 来指示项目已 100% 完成，但是项目仍然保持打开，以便记录任何待定时间或支出条目。</span><span class="sxs-lookup"><span data-stu-id="64cfa-128">By updating the project stage to **Complete**, the project manager indicates that the work is 100-percent completed, but that the project is being kept open so that any pending time or expense entries can be recorded.</span></span>

## <a name="close"></a><span data-ttu-id="64cfa-129">结束</span><span class="sxs-lookup"><span data-stu-id="64cfa-129">Close</span></span>

<span data-ttu-id="64cfa-130">当记录了项目的所有交易时，项目经理可以将阶段更新为 **结束**。</span><span class="sxs-lookup"><span data-stu-id="64cfa-130">When all transactions are recorded for the project, the project manager can update the stage to **Close**.</span></span> <span data-ttu-id="64cfa-131">此时不能记录任何交易，并且项目设置为只读。</span><span class="sxs-lookup"><span data-stu-id="64cfa-131">At that point, no transactions can be recorded, and the project is set to read-only.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]