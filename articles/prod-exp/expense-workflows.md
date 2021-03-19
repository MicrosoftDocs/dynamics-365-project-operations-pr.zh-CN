---
title: 设置支出管理工作流
description: 您可以设置用来审核和审批出差和支出文档的工作流程。
author: ShylaThompson
manager: AnnBe
ms.date: 09/13/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WorkflowtableListPageRnr
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 36ab1edc4769013684fa9248e6c5eac025637bbd
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/15/2021
ms.locfileid: "5271612"
---
# <a name="set-up-expense-management-workflows"></a><span data-ttu-id="1986e-103">设置支出管理工作流</span><span class="sxs-lookup"><span data-stu-id="1986e-103">Set up Expense management workflows</span></span>

<span data-ttu-id="1986e-104">您可以设置用于审核和审批出差和支出文档的工作流程。</span><span class="sxs-lookup"><span data-stu-id="1986e-104">You can set up a workflow process that is used to review and approve travel and expense documents.</span></span> <span data-ttu-id="1986e-105">工作流可以定义的单据包括支出报表、出差申请和预付现金请求。</span><span class="sxs-lookup"><span data-stu-id="1986e-105">The documents for which workflows can be defined include expense reports, travel requisitions, and cash advance requests.</span></span>

<span data-ttu-id="1986e-106">“工作流”代表业务流程。</span><span class="sxs-lookup"><span data-stu-id="1986e-106">A workflow represents a business process.</span></span> <span data-ttu-id="1986e-107">它定义单据如何在系统中流动并指示必须由谁完成任务或审核单据。</span><span class="sxs-lookup"><span data-stu-id="1986e-107">It defines how a document flows through the system and indicates who must complete a task or approve a document.</span></span> <span data-ttu-id="1986e-108">在组织中使用工作流系统具有以下几项好处：</span><span class="sxs-lookup"><span data-stu-id="1986e-108">There are several benefits of using the workflow system in your organization:</span></span>

-   <span data-ttu-id="1986e-109">**一致的流程**— 您可定义特定单据（如采购申请和支出报表）的审核流程。</span><span class="sxs-lookup"><span data-stu-id="1986e-109">**Consistent processes** — You can define the approval process for specific documents, such as purchase requisitions and expense reports.</span></span> <span data-ttu-id="1986e-110">使用工作流系统有助于确保以一致且有效的方式来处理和审核单据。</span><span class="sxs-lookup"><span data-stu-id="1986e-110">Using the workflow system helps to ensure that documents are processed and approved in a consistent and efficient manner.</span></span>

-   <span data-ttu-id="1986e-111">“流程可见性”— 您可跟踪特定工作流实例的状态、历史记录和绩效指标。</span><span class="sxs-lookup"><span data-stu-id="1986e-111">Process visibility — You can track the status, history, and performance metrics of a specific workflow instance.</span></span> <span data-ttu-id="1986e-112">这可以帮助您确定是否应对工作流进行更改以提高效率。</span><span class="sxs-lookup"><span data-stu-id="1986e-112">This helps you determine whether changes should be made to the workflow to improve efficiency.</span></span>

-   <span data-ttu-id="1986e-113">“集中的工作列表”— 用户可以查看集中化的工作列表，以查看分配给他们的工作流任务和审核任务。</span><span class="sxs-lookup"><span data-stu-id="1986e-113">Centralized work list — Users can view a centralized work list to view the workflow tasks and approvals assigned to them.</span></span> 

<span data-ttu-id="1986e-114">**您可以创建工作流类型**</span><span class="sxs-lookup"><span data-stu-id="1986e-114">**The types of workflows you can create**</span></span>

<span data-ttu-id="1986e-115">下表列出了您可以在 **支出** 过程中创建的工作流类型。</span><span class="sxs-lookup"><span data-stu-id="1986e-115">The following table lists the types of workflows that you can create in **Expense**.</span></span>


|              <span data-ttu-id="1986e-116"><strong>类型</strong></span><span class="sxs-lookup"><span data-stu-id="1986e-116"><strong>Type</strong></span></span>              |                   <span data-ttu-id="1986e-117"><strong>使用此类型可以</strong></span><span class="sxs-lookup"><span data-stu-id="1986e-117"><strong>Use this type to</strong></span></span>                   |
|-------------------------------------------------|-----------------------------------------------------------------------|
|         <span data-ttu-id="1986e-118"><strong>支出报表</strong></span><span class="sxs-lookup"><span data-stu-id="1986e-118"><strong>Expense report</strong></span></span>         |            <span data-ttu-id="1986e-119">为支出报表创建审批工作流。</span><span class="sxs-lookup"><span data-stu-id="1986e-119">Create approval workflows for expense reports.</span></span>             |
|  <span data-ttu-id="1986e-120"><strong>支出报表自动发布</strong></span><span class="sxs-lookup"><span data-stu-id="1986e-120"><strong>Expense report auto posting</strong></span></span>   |        <span data-ttu-id="1986e-121">为支出报表创建自动发布工作流。</span><span class="sxs-lookup"><span data-stu-id="1986e-121">Create automatic posting workflows for expense reports.</span></span>        |
|       <span data-ttu-id="1986e-122"><strong>支出明细项目</strong></span><span class="sxs-lookup"><span data-stu-id="1986e-122"><strong>Expense line item</strong></span></span>        |     <span data-ttu-id="1986e-123">为支出报表中的明细项目创建审批工作流。</span><span class="sxs-lookup"><span data-stu-id="1986e-123">Create approval workflows for line items on expense reports.</span></span>      |
| <span data-ttu-id="1986e-124"><strong>支出明细项目自动发布</strong></span><span class="sxs-lookup"><span data-stu-id="1986e-124"><strong>Expense line item auto posting</strong></span></span> | <span data-ttu-id="1986e-125">为支出报表中的明细项目创建自动发布工作流。</span><span class="sxs-lookup"><span data-stu-id="1986e-125">Create automatic posting workflows for line items on expense reports.</span></span> |
|       <span data-ttu-id="1986e-126"><strong>出差申请</strong></span><span class="sxs-lookup"><span data-stu-id="1986e-126"><strong>Travel requisition</strong></span></span>       |          <span data-ttu-id="1986e-127">为出差申请创建审批工作流。</span><span class="sxs-lookup"><span data-stu-id="1986e-127">Create approval workflows for travel requisitions.</span></span>           |
|      <span data-ttu-id="1986e-128"><strong>预付现金请求</strong></span><span class="sxs-lookup"><span data-stu-id="1986e-128"><strong>Cash advance request</strong></span></span>      |         <span data-ttu-id="1986e-129">为预付现金请求创建审批工作流。</span><span class="sxs-lookup"><span data-stu-id="1986e-129">Create approval workflows for cash advance requests.</span></span>          |
|        <span data-ttu-id="1986e-130"><strong>增值税退税</strong></span><span class="sxs-lookup"><span data-stu-id="1986e-130"><strong>VAT tax recovery</strong></span></span>        | <span data-ttu-id="1986e-131">为增值税 (VAT) 退税创建审批工作流。</span><span class="sxs-lookup"><span data-stu-id="1986e-131">Create approval workflows for the recovery of value-added tax (VAT).</span></span>  |



[!INCLUDE[footer-include](../includes/footer-banner.md)]