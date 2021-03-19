---
title: 项目阶段类型
description: 本主题提供有关项目阶段的信息。
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 06/19/2020
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
ms.openlocfilehash: 3503b17e54fc0b321582c30ce534e4cb3f497a5f
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/15/2021
ms.locfileid: "5283672"
---
# <a name="project-stage-types"></a><span data-ttu-id="c7a0b-103">项目阶段类型</span><span class="sxs-lookup"><span data-stu-id="c7a0b-103">Project stage types</span></span> 

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="c7a0b-104">项目阶段旨在反映项目在进行中的状态。</span><span class="sxs-lookup"><span data-stu-id="c7a0b-104">Project stages are designed to reflect the state of the project as it progresses.</span></span> <span data-ttu-id="c7a0b-105">自定义项可用于通过业务流程、Power Automate 或插件扩展自动更新阶段。</span><span class="sxs-lookup"><span data-stu-id="c7a0b-105">Customizations can be used to automatically update the stages with business process flows, Power Automate, or plug-in extensions.</span></span>

<span data-ttu-id="c7a0b-106">默认 BPF 中定义了以下阶段：</span><span class="sxs-lookup"><span data-stu-id="c7a0b-106">The following stages are defined in the default BPF:</span></span>

- <span data-ttu-id="c7a0b-107">新建​​</span><span class="sxs-lookup"><span data-stu-id="c7a0b-107">New</span></span>
- <span data-ttu-id="c7a0b-108">报价单</span><span class="sxs-lookup"><span data-stu-id="c7a0b-108">Quote</span></span>
- <span data-ttu-id="c7a0b-109">规划</span><span class="sxs-lookup"><span data-stu-id="c7a0b-109">Plan</span></span>
- <span data-ttu-id="c7a0b-110">交付</span><span class="sxs-lookup"><span data-stu-id="c7a0b-110">Deliver</span></span>
- <span data-ttu-id="c7a0b-111">完成</span><span class="sxs-lookup"><span data-stu-id="c7a0b-111">Complete</span></span>
- <span data-ttu-id="c7a0b-112">结束</span><span class="sxs-lookup"><span data-stu-id="c7a0b-112">Close</span></span> 

## <a name="new"></a><span data-ttu-id="c7a0b-113">新建</span><span class="sxs-lookup"><span data-stu-id="c7a0b-113">New</span></span>

<span data-ttu-id="c7a0b-114">创建项目时，项目阶段设置为 **新建**。</span><span class="sxs-lookup"><span data-stu-id="c7a0b-114">When you create a project, the project stage is set to **New**.</span></span> <span data-ttu-id="c7a0b-115">如果项目是从模板创建的，则项目中可能包含计划、估算和团队数据。</span><span class="sxs-lookup"><span data-stu-id="c7a0b-115">If the project was created from a template, it might have schedule, estimate, and team data.</span></span> <span data-ttu-id="c7a0b-116">否则，只是项目的轮廓，并且必须输入其余组成部分。</span><span class="sxs-lookup"><span data-stu-id="c7a0b-116">Otherwise, it's just an outline of the project, and the remaining components must be entered.</span></span>

## <a name="quote"></a><span data-ttu-id="c7a0b-117">报价单</span><span class="sxs-lookup"><span data-stu-id="c7a0b-117">Quote</span></span>

<span data-ttu-id="c7a0b-118">当您将项目与报价单关联或从报价单创建项目时，项目阶段设置为 **报价单**，并且估算的开始和结束日期也会更新。</span><span class="sxs-lookup"><span data-stu-id="c7a0b-118">When you associate a project with a quote, or when you create a project from a quote, the project stage is set to **Quote**, and the estimated start and end dates are updated.</span></span> <span data-ttu-id="c7a0b-119">当项目处于 **报价单** 阶段时，**项目实体** 页的 **销售** 选项卡显示报价单的详细信息。</span><span class="sxs-lookup"><span data-stu-id="c7a0b-119">While the project is in the **Quote** stage, the **Sales** tab on the **Project Entity** page shows details of the quote.</span></span>

## <a name="plan"></a><span data-ttu-id="c7a0b-120">规划</span><span class="sxs-lookup"><span data-stu-id="c7a0b-120">Plan</span></span>

<span data-ttu-id="c7a0b-121">当您获得与项目相关的报价单时，并且当项目转到 **合同** 阶段时，项目阶段将更新为 **规划**。</span><span class="sxs-lookup"><span data-stu-id="c7a0b-121">When you win a quote that is associated with a project, and the project is moved to the **Contract** phase, the project stage is updated to **Plan**.</span></span> <span data-ttu-id="c7a0b-122">当项目处于 **规划** 阶段时，**项目实体** 页显示合同的详细信息。</span><span class="sxs-lookup"><span data-stu-id="c7a0b-122">While the project is in the **Plan** stage, the **Project Entity** page shows details of the contract.</span></span>

## <a name="deliver"></a><span data-ttu-id="c7a0b-123">交付</span><span class="sxs-lookup"><span data-stu-id="c7a0b-123">Deliver</span></span>

<span data-ttu-id="c7a0b-124">昂项目规划完成，并且您已准备好启动项目时，项目经理应该将项目阶段更新为 **交付** 以表示项目已启动。</span><span class="sxs-lookup"><span data-stu-id="c7a0b-124">When the project plan is completed, and you're ready to start the project, the project manager should update the project stage to **Deliver** to show that the project has started.</span></span>

## <a name="complete"></a><span data-ttu-id="c7a0b-125">完成</span><span class="sxs-lookup"><span data-stu-id="c7a0b-125">Complete</span></span> 

<span data-ttu-id="c7a0b-126">当项目的工作已完成时，项目经理可以将阶段更新为 **完成**。</span><span class="sxs-lookup"><span data-stu-id="c7a0b-126">When the work for the project is completed, the project manager can update the stage to **Complete**.</span></span> <span data-ttu-id="c7a0b-127">项目经理可以通过将项目阶段更新为 **完成** 来指示项目已 100% 完成，但是项目仍然保持打开，以便记录任何待定时间或支出条目。</span><span class="sxs-lookup"><span data-stu-id="c7a0b-127">By updating the project stage to **Complete**, the project manager indicates that the work is 100-percent completed, but that the project is being kept open so that any pending time or expense entries can be recorded.</span></span>

## <a name="close"></a><span data-ttu-id="c7a0b-128">结束</span><span class="sxs-lookup"><span data-stu-id="c7a0b-128">Close</span></span>

<span data-ttu-id="c7a0b-129">当记录了项目的所有交易时，项目经理可以将阶段更新为 **结束**。</span><span class="sxs-lookup"><span data-stu-id="c7a0b-129">When all transactions are recorded for the project, the project manager can update the stage to **Close**.</span></span> <span data-ttu-id="c7a0b-130">此时不能记录任何交易，并且项目设置为只读。</span><span class="sxs-lookup"><span data-stu-id="c7a0b-130">At that point, no transactions can be recorded, and the project is set to read-only.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]