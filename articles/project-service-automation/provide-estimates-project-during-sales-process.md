---
title: 在销售流程中提供项目的工作估计
description: 如何在 Project Service 中的销售流程中提供项目的工作估计
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: 8e6fbba8-2908-4555-9470-43c37e66efea
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 8edb91010dd1227bc7947b59664d08430c219638
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/24/2020
ms.locfileid: "3749762"
---
# <a name="provide-work-estimates-for-a-project-during-the-sales-process-project-service"></a><span data-ttu-id="c9357-103">在销售流程中提供项目的工作估计 (Project Service)</span><span class="sxs-lookup"><span data-stu-id="c9357-103">Provide work estimates for a project during the sales process (Project Service)</span></span>

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="c9357-104">在销售流程期间，您可以使用报价单明细从新执行销售估计。</span><span class="sxs-lookup"><span data-stu-id="c9357-104">During the sales process, you can work out sales estimates from the ground up with quote lines.</span></span> [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] <span data-ttu-id="c9357-105">中的[!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]功能提供更科学、更确定性的进行销售估计的方法，此方法是通过划分工作项，并关联参与工作分解结构中项目的估计的相关属性来执行。</span><span class="sxs-lookup"><span data-stu-id="c9357-105">capabilities in [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] provide a more scientific and deterministic way of coming up with sales estimates by breaking down work items and associating relevant attributes that contribute toward the estimates for the project in the work breakdown structure.</span></span>  
  
 <span data-ttu-id="c9357-106">一旦您赢得销售，您可以在项目计划中使用关联的工作分解结构，并根据项目成功完成的需要进行调整。</span><span class="sxs-lookup"><span data-stu-id="c9357-106">Once you win the sale, you can use the associated work breakdown structure in your project plan, refining it as necessary for successful completion of your project.</span></span>  
  
## <a name="link-a-project-to-a-quote-line"></a><span data-ttu-id="c9357-107">链接项目到报价单明细</span><span class="sxs-lookup"><span data-stu-id="c9357-107">Link a project to a quote line</span></span>  
 <span data-ttu-id="c9357-108">如果创建基于项目的报价单明细，您可以从报价单明细创建一个新项目。</span><span class="sxs-lookup"><span data-stu-id="c9357-108">When creating a project-based quote line, you can create a new project from the quote line.</span></span> <span data-ttu-id="c9357-109">然后可以使用项目模板，其可以是您的组织常用的预配置的标准项目计划和财务估计，也可以是过去项目的项目计划副本和估计。</span><span class="sxs-lookup"><span data-stu-id="c9357-109">You can then use project templates, which are either pre-configured standard project plans and financial estimates common to your organization, or a copy of a project plan and estimates from a past project.</span></span> <span data-ttu-id="c9357-110">在创建项目时，选择项目模板将提供调整项目计划、估计和角色要求的基础。</span><span class="sxs-lookup"><span data-stu-id="c9357-110">When you create a project, choosing a project template provides a basis to refine the project plan, estimates, and role requirements.</span></span> <span data-ttu-id="c9357-111">通过从报价单创建项目，项目将自动与报价单明细关联。</span><span class="sxs-lookup"><span data-stu-id="c9357-111">By creating your project from the quote, the project is automatically associated with the quote line.</span></span>  
  
## <a name="project-estimate-components"></a><span data-ttu-id="c9357-112">项目估计组件</span><span class="sxs-lookup"><span data-stu-id="c9357-112">Project estimate components</span></span>  
 <span data-ttu-id="c9357-113">项目的工作分解结构提供将工作分解到任务，维护任务层次结构，以及分派完成每项任务所需的工作估计的方法。</span><span class="sxs-lookup"><span data-stu-id="c9357-113">The work breakdown structure in a project provides a way to break down work into tasks, maintain a hierarchy of tasks, and assign an estimate of effort required to complete each task.</span></span> <span data-ttu-id="c9357-114">您还可以将角色分派到任务以指示完成任务和计划所需的资源类型的估计。</span><span class="sxs-lookup"><span data-stu-id="c9357-114">You can also associate roles to a task to indicate an estimate of the type of resource required to complete a task and a schedule.</span></span>  
  
 <span data-ttu-id="c9357-115">工作分解结构帮助您确定工作任务和计划估计。</span><span class="sxs-lookup"><span data-stu-id="c9357-115">The work breakdown structure helps you determine work effort and schedule estimates.</span></span> <span data-ttu-id="c9357-116">默认情况下，项目使用您之前定义的默认价目表。</span><span class="sxs-lookup"><span data-stu-id="c9357-116">By default, the project uses default price lists that you defined earlier.</span></span> <span data-ttu-id="c9357-117">在价目表中定义的成本和销售价格帮助确定项目的工作分解的财务估计。</span><span class="sxs-lookup"><span data-stu-id="c9357-117">The cost and sales prices defined in the price lists help determine financial estimates for the project’s work breakdown.</span></span>  
  
 <span data-ttu-id="c9357-118">如果项目与报价单关联，报价单将具有不同的默认价目表，报价单的价目表将用于财务估计。</span><span class="sxs-lookup"><span data-stu-id="c9357-118">If your project is associated with a quote, and the quote has a different price list from the default, the quote’s price list is used for financial estimates.</span></span>  
  
## <a name="import-estimates-from-a-project-into-a-quote"></a><span data-ttu-id="c9357-119">将估计从项目导入到报价单</span><span class="sxs-lookup"><span data-stu-id="c9357-119">Import estimates from a project into a quote</span></span>  
 <span data-ttu-id="c9357-120">当您的项目中有项目估计后，您可以将这些估计导入到报价单明细：</span><span class="sxs-lookup"><span data-stu-id="c9357-120">Once you have project estimates in the project, you can import these estimates into the quote line:</span></span>  
  
-   <span data-ttu-id="c9357-121">在**报价单明细详细信息**中，单击**从估计导入**。</span><span class="sxs-lookup"><span data-stu-id="c9357-121">In **Quote Line Details**, click **Import from estimates**.</span></span> 

-   <span data-ttu-id="c9357-122">选择是否导入按交易类型、角色或工作分解结构节点级别汇总的项目估计。</span><span class="sxs-lookup"><span data-stu-id="c9357-122">Select whether to import project estimates summarized by transaction type, role, or work breakdown structure node level.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="c9357-123">另请参阅</span><span class="sxs-lookup"><span data-stu-id="c9357-123">See Also</span></span>  
 [<span data-ttu-id="c9357-124">项目经理指南</span><span class="sxs-lookup"><span data-stu-id="c9357-124">Project Manager Guide</span></span>](../project-service/project-manager-guide.md)
