---
title: 销售额估算和项目
description: 此主题介绍如何在销售流程中利用计划和估算。
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
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
ms.openlocfilehash: d8bb380519759659dc1b4151b62228a626ee7a26
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/28/2020
ms.locfileid: "4120667"
---
# <a name="sales-estimates-and-projects"></a><span data-ttu-id="4f96f-103">销售额估算和项目</span><span class="sxs-lookup"><span data-stu-id="4f96f-103">Sales estimates and projects</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="4f96f-104">销售流程中，可通过将项目链接到销售报价单来创建销售额估算。</span><span class="sxs-lookup"><span data-stu-id="4f96f-104">During the sales process, you can create sales estimates by linking a project to a sales quote.</span></span> <span data-ttu-id="4f96f-105">这样，就可以在销售流程中进行临时估算，以利用项目计划和估算产能。</span><span class="sxs-lookup"><span data-stu-id="4f96f-105">In this way, deterministic estimation can occur during the sales process, to take advantage of project scheduling and estimation capabilities.</span></span> <span data-ttu-id="4f96f-106">如果销售通过，可将用于销售估算目的的计划用作进一步优化项目计划的基础。</span><span class="sxs-lookup"><span data-stu-id="4f96f-106">If the sale goes through, the schedule that was used for sales estimation purposes can be used as the basis for further refinement of the project plan.</span></span>

## <a name="linking-a-project-to-a-quote-line"></a><span data-ttu-id="4f96f-107">将项目链接到报价单明细</span><span class="sxs-lookup"><span data-stu-id="4f96f-107">Linking a project to a quote line</span></span>

<span data-ttu-id="4f96f-108">创建基于项目的报价单明细时，可在 **报价单明细** 页中创建新项目或关联现有项目。</span><span class="sxs-lookup"><span data-stu-id="4f96f-108">When you create a project-based quote line, you can create a new project or associate an existing project pn the **Quote Line** page.</span></span> 

> ![“报价单明细”窗体](media/project-8.png)
 
<span data-ttu-id="4f96f-110">基于报价单明细详细信息创建新项目时，可利用项目模板。</span><span class="sxs-lookup"><span data-stu-id="4f96f-110">When you create a new project from the quote line details, you can take advantage of project templates.</span></span> <span data-ttu-id="4f96f-111">项目模板是用于表示组织中的典型标准项目计划和财务估算的模型项目。</span><span class="sxs-lookup"><span data-stu-id="4f96f-111">Project templates are model projects that represent standard project plans and financial estimates that are typical in an organization.</span></span> <span data-ttu-id="4f96f-112">也可以表示来自过去项目的项目计划和估算的副本。</span><span class="sxs-lookup"><span data-stu-id="4f96f-112">They can also represent copies of project plans and estimates from past projects.</span></span>

> ![报价单明细详细信息](media/project-9.png)
  
<span data-ttu-id="4f96f-114">基于报价单创建项目时，项目将自动与报价单明细关联。</span><span class="sxs-lookup"><span data-stu-id="4f96f-114">When you create the project from the quote, the project is automatically associated with the quote line.</span></span>

## <a name="components-of-estimates-in-a-project"></a><span data-ttu-id="4f96f-115">项目中的估算的组件</span><span class="sxs-lookup"><span data-stu-id="4f96f-115">Components of estimates in a project</span></span>

<span data-ttu-id="4f96f-116">可通过计划将工作拆分为任务，维护任务层次结构，确定需要哪些资源才能完成任务，以及分派完成任务所需工作量的估算。</span><span class="sxs-lookup"><span data-stu-id="4f96f-116">A schedule lets you divide work into tasks, maintain a hierarchy of tasks, determine what resources are required to complete a task, and assign an estimate of the effort that is required to complete a task.</span></span>

<span data-ttu-id="4f96f-117">可通过使用 **项目** 页的 **计划** 选项卡上的字段定义工作量和计划估算。</span><span class="sxs-lookup"><span data-stu-id="4f96f-117">You can define the work effort and schedule estimates by using the fields on the **Schedule** tab of the **Project** page.</span></span> <span data-ttu-id="4f96f-118">因为价目表与项目关联，所以使用在价目表中定义的成本和销售价计算财务估算。</span><span class="sxs-lookup"><span data-stu-id="4f96f-118">Because a price list is associated with the project, financial estimates are calculated by using cost and sales prices that are defined in the price list.</span></span>

## <a name="importing-estimates-from-a-project-into-a-quote"></a><span data-ttu-id="4f96f-119">将估计从项目导入到报价单</span><span class="sxs-lookup"><span data-stu-id="4f96f-119">Importing estimates from a project into a quote</span></span>

<span data-ttu-id="4f96f-120">定义项目估算之后，可将其导入报价单明细中。</span><span class="sxs-lookup"><span data-stu-id="4f96f-120">After you define project estimates, you can import them into the quote line.</span></span> <span data-ttu-id="4f96f-121">在 **报价单明细详细信息** 页中，选择功能区中的 **从估算导入** 以按交易类型、角色或任务级别汇总项目估算。</span><span class="sxs-lookup"><span data-stu-id="4f96f-121">On the **Quote Line Details** page, select **Import from estimates** on the ribbon to summarize project estimates by transaction type, role, or task level.</span></span>
