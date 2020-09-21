---
title: 项目阶段
description: 本主题提供有关项目阶段的信息。
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: 983c25a0-ed21-4151-a109-b385a88285fa
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 70aa057e127df7ba925e84f5d056a06a4cc8833e
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/24/2020
ms.locfileid: "3749679"
---
# <a name="project-stages"></a><span data-ttu-id="7ca16-103">项目阶段</span><span class="sxs-lookup"><span data-stu-id="7ca16-103">Project stages</span></span> 

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="7ca16-104">项目进行中，将更新项目阶段以体现项目的状态。</span><span class="sxs-lookup"><span data-stu-id="7ca16-104">Project stages are updated to reflect the state of the project as it progresses.</span></span> <span data-ttu-id="7ca16-105">默认业务流程将自动更新项目的某些阶段，而其他阶段则由项目经理手动更新。</span><span class="sxs-lookup"><span data-stu-id="7ca16-105">The default business process flow automatically updates some stages of the project while others are manually updated by the project manager.</span></span> 

<span data-ttu-id="7ca16-106">默认 BPF 中定义了以下阶段：</span><span class="sxs-lookup"><span data-stu-id="7ca16-106">The following stages are defined in the default BPF:</span></span>

- <span data-ttu-id="7ca16-107">新建</span><span class="sxs-lookup"><span data-stu-id="7ca16-107">New</span></span>
- <span data-ttu-id="7ca16-108">报价单</span><span class="sxs-lookup"><span data-stu-id="7ca16-108">Quote</span></span>
- <span data-ttu-id="7ca16-109">规划</span><span class="sxs-lookup"><span data-stu-id="7ca16-109">Plan</span></span>
- <span data-ttu-id="7ca16-110">交付</span><span class="sxs-lookup"><span data-stu-id="7ca16-110">Deliver</span></span>
- <span data-ttu-id="7ca16-111">完成</span><span class="sxs-lookup"><span data-stu-id="7ca16-111">Complete</span></span>
- <span data-ttu-id="7ca16-112">结束</span><span class="sxs-lookup"><span data-stu-id="7ca16-112">Close</span></span> 

## <a name="new"></a><span data-ttu-id="7ca16-113">新建</span><span class="sxs-lookup"><span data-stu-id="7ca16-113">New</span></span>

<span data-ttu-id="7ca16-114">创建项目时，项目阶段设置为**新建**。</span><span class="sxs-lookup"><span data-stu-id="7ca16-114">When you create a project, the project stage is set to **New**.</span></span> <span data-ttu-id="7ca16-115">如果项目是从模板创建的，则项目中可能包含计划、估算和团队数据。</span><span class="sxs-lookup"><span data-stu-id="7ca16-115">If the project was created from a template, it might have schedule, estimate, and team data.</span></span> <span data-ttu-id="7ca16-116">否则，只是项目的轮廓，并且必须输入其余组成部分。</span><span class="sxs-lookup"><span data-stu-id="7ca16-116">Otherwise, it's just an outline of the project, and the remaining components must be entered.</span></span>

## <a name="quote"></a><span data-ttu-id="7ca16-117">报价单</span><span class="sxs-lookup"><span data-stu-id="7ca16-117">Quote</span></span>

<span data-ttu-id="7ca16-118">当您将项目与报价单关联或从报价单创建项目时，项目阶段设置为**报价单**，并且估算的开始和结束日期也会更新。</span><span class="sxs-lookup"><span data-stu-id="7ca16-118">When you associate a project with a quote, or when you create a project from a quote, the project stage is set to **Quote**, and the estimated start and end dates are updated.</span></span> <span data-ttu-id="7ca16-119">当项目处于**报价单**阶段时，**项目实体**页的**销售**选项卡显示报价单的详细信息。</span><span class="sxs-lookup"><span data-stu-id="7ca16-119">While the project is in the **Quote** stage, the **Sales** tab on the **Project Entity** page shows details of the quote.</span></span>

## <a name="plan"></a><span data-ttu-id="7ca16-120">规划</span><span class="sxs-lookup"><span data-stu-id="7ca16-120">Plan</span></span>

<span data-ttu-id="7ca16-121">当您获得与项目相关的报价单时，并且当项目转到**合同**阶段时，项目阶段将更新为**规划**。</span><span class="sxs-lookup"><span data-stu-id="7ca16-121">When you win a quote that is associated with a project, and the project is moved to the **Contract** phase, the project stage is updated to **Plan**.</span></span> <span data-ttu-id="7ca16-122">当项目处于**规划**阶段时，**项目实体**页显示合同的详细信息。</span><span class="sxs-lookup"><span data-stu-id="7ca16-122">While the project is in the **Plan** stage, the **Project Entity** page shows details of the contract.</span></span>

## <a name="deliver"></a><span data-ttu-id="7ca16-123">交付</span><span class="sxs-lookup"><span data-stu-id="7ca16-123">Deliver</span></span>

<span data-ttu-id="7ca16-124">昂项目规划完成，并且您已准备好启动项目时，项目经理应该将项目阶段更新为**交付**以表示项目已启动。</span><span class="sxs-lookup"><span data-stu-id="7ca16-124">When the project plan is completed, and you're ready to start the project, the project manager should update the project stage to **Deliver** to show that the project has started.</span></span>

## <a name="complete"></a><span data-ttu-id="7ca16-125">完成</span><span class="sxs-lookup"><span data-stu-id="7ca16-125">Complete</span></span> 

<span data-ttu-id="7ca16-126">当项目的工作已完成时，项目经理可以将阶段更新为**完成**。</span><span class="sxs-lookup"><span data-stu-id="7ca16-126">When the work for the project is completed, the project manager can update the stage to **Complete**.</span></span> <span data-ttu-id="7ca16-127">项目经理可以通过将项目阶段更新为**完成**来指示项目已 100% 完成，但是项目仍然保持打开，以便记录任何待定时间或支出条目。</span><span class="sxs-lookup"><span data-stu-id="7ca16-127">By updating the project stage to **Complete**, the project manager indicates that the work is 100-percent completed, but that the project is being kept open so that any pending time or expense entries can be recorded.</span></span>

## <a name="close"></a><span data-ttu-id="7ca16-128">结束</span><span class="sxs-lookup"><span data-stu-id="7ca16-128">Close</span></span>

<span data-ttu-id="7ca16-129">当记录了项目的所有交易时，项目经理可以将阶段更新为**结束**。</span><span class="sxs-lookup"><span data-stu-id="7ca16-129">When all transactions are recorded for the project, the project manager can update the stage to **Close**.</span></span> <span data-ttu-id="7ca16-130">此时不能记录任何交易，并且项目设置为只读。</span><span class="sxs-lookup"><span data-stu-id="7ca16-130">At that point, no transactions can be recorded, and the project is set to read-only.</span></span>
