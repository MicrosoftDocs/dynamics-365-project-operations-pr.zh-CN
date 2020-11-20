---
title: 设置支出管理工作流
description: 您可以设置用于审核和审批出差和支出文档的工作流程。
author: suvaidya
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: ''
ms.author: shylaw
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: af6463b07e282ae1ff6aa7dc1a540ff7c8cc318a
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/28/2020
ms.locfileid: "4127687"
---
# <a name="set-up-workflows-for-expense-management"></a><span data-ttu-id="00537-103">设置支出管理工作流</span><span class="sxs-lookup"><span data-stu-id="00537-103">Set up workflows for Expense management</span></span>

<span data-ttu-id="00537-104">_**适用于：** 基于资源/非库存场景的 Project Operations，精简部署 - 估价开票交易_</span><span class="sxs-lookup"><span data-stu-id="00537-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="00537-105">您可以设置用来审核和审批出差和支出文档的工作流程。</span><span class="sxs-lookup"><span data-stu-id="00537-105">You can set up a workflow process to review and approve travel and expense documents.</span></span> <span data-ttu-id="00537-106">您可以为支出报表、出差申请和预付现金请求定义工作流。</span><span class="sxs-lookup"><span data-stu-id="00537-106">You can define workflows for expense reports, travel requisitions, and cash advance requests.</span></span>

<span data-ttu-id="00537-107">工作流表示一个业务流程，定义文档在系统中的流动方式。</span><span class="sxs-lookup"><span data-stu-id="00537-107">A workflow represents a business process and defines how a document flows through the system.</span></span> <span data-ttu-id="00537-108">工作流还指示必须完成任务或审批文档的人员。</span><span class="sxs-lookup"><span data-stu-id="00537-108">The workflow also indicates who must complete a task or approve a document.</span></span> <span data-ttu-id="00537-109">在组织中使用工作流系统具有以下几项好处：</span><span class="sxs-lookup"><span data-stu-id="00537-109">There are several benefits of using the workflow system in your organization:</span></span>

- <span data-ttu-id="00537-110">**一致的流程**：您可以为特定文档（如采购申请和支出报表）定义审批流程。</span><span class="sxs-lookup"><span data-stu-id="00537-110">**Consistent processes**: You can define the approval process for specific documents, such as purchase requisitions and expense reports.</span></span> <span data-ttu-id="00537-111">使用工作流系统有助于确保以一致且有效的方式处理和审批文档。</span><span class="sxs-lookup"><span data-stu-id="00537-111">Using the workflow system helps ensure that documents are processed and approved in a consistent and efficient manner.</span></span>
- <span data-ttu-id="00537-112">**流程可见**：可以跟踪特定工作流实例的状态、历史记录和性能指标。</span><span class="sxs-lookup"><span data-stu-id="00537-112">**Process visibility**: You can track the status, history, and performance metrics of a specific workflow instance.</span></span> <span data-ttu-id="00537-113">这可以帮助您确定是否应对工作流进行更改以提高效率。</span><span class="sxs-lookup"><span data-stu-id="00537-113">This helps you determine whether changes should be made to the workflow to improve efficiency.</span></span>
- <span data-ttu-id="00537-114">**集中式工作列表**：用户可以查看集中式工作列表，来查看分配给他们的工作流任务和审批。</span><span class="sxs-lookup"><span data-stu-id="00537-114">**Centralized work list**: Users can view a centralized work list to view the workflow tasks and approvals assigned to them.</span></span> 

## <a name="workflow-types"></a><span data-ttu-id="00537-115">工作流类型</span><span class="sxs-lookup"><span data-stu-id="00537-115">Workflow types</span></span>

<span data-ttu-id="00537-116">下表列出了您可以在 **支出管理** 中创建的工作流的类型。</span><span class="sxs-lookup"><span data-stu-id="00537-116">The following table lists the types of workflows that you can create in **Expense Management**.</span></span>


|              <span data-ttu-id="00537-117"><strong>类型</strong></span><span class="sxs-lookup"><span data-stu-id="00537-117"><strong>Type</strong></span></span>              |                   <span data-ttu-id="00537-118"><strong>使用此类型可以</strong></span><span class="sxs-lookup"><span data-stu-id="00537-118"><strong>Use this type to</strong></span></span>                   |
|-------------------------------------------------|-----------------------------------------------------------------------|
|   <span data-ttu-id="00537-119"><strong>支出报表自动审批</strong></span><span class="sxs-lookup"><span data-stu-id="00537-119"><strong>Expense report auto approval</strong></span></span> |            <span data-ttu-id="00537-120">为支出报表创建审批工作流。</span><span class="sxs-lookup"><span data-stu-id="00537-120">Create approval workflows for expense reports.</span></span>             |
|  <span data-ttu-id="00537-121"><strong>支出报表自动发布</strong></span><span class="sxs-lookup"><span data-stu-id="00537-121"><strong>Expense report auto posting</strong></span></span>   |        <span data-ttu-id="00537-122">为支出报表创建自动发布工作流。</span><span class="sxs-lookup"><span data-stu-id="00537-122">Create automatic posting workflows for expense reports.</span></span>        |
|       <span data-ttu-id="00537-123"><strong>支出明细项目</strong></span><span class="sxs-lookup"><span data-stu-id="00537-123"><strong>Expense line item</strong></span></span>        |     <span data-ttu-id="00537-124">为支出报表中的明细项目创建审批工作流。</span><span class="sxs-lookup"><span data-stu-id="00537-124">Create approval workflows for line items on expense reports.</span></span>      |
| <span data-ttu-id="00537-125"><strong>支出明细项目自动发布</strong></span><span class="sxs-lookup"><span data-stu-id="00537-125"><strong>Expense line item auto posting</strong></span></span> | <span data-ttu-id="00537-126">为支出报表中的明细项目创建自动发布工作流。</span><span class="sxs-lookup"><span data-stu-id="00537-126">Create automatic posting workflows for line items on expense reports.</span></span> |
|       <span data-ttu-id="00537-127"><strong>出差申请</strong></span><span class="sxs-lookup"><span data-stu-id="00537-127"><strong>Travel requisition</strong></span></span>       |          <span data-ttu-id="00537-128">为出差申请创建审批工作流。</span><span class="sxs-lookup"><span data-stu-id="00537-128">Create approval workflows for travel requisitions.</span></span>           |
|      <span data-ttu-id="00537-129"><strong>预付现金请求</strong></span><span class="sxs-lookup"><span data-stu-id="00537-129"><strong>Cash advance request</strong></span></span>      |         <span data-ttu-id="00537-130">为预付现金请求创建审批工作流。</span><span class="sxs-lookup"><span data-stu-id="00537-130">Create approval workflows for cash advance requests.</span></span>          |
|        <span data-ttu-id="00537-131"><strong>增值税退税</strong></span><span class="sxs-lookup"><span data-stu-id="00537-131"><strong>VAT tax recovery</strong></span></span>        | <span data-ttu-id="00537-132">为增值税 (VAT) 退税创建审批工作流。</span><span class="sxs-lookup"><span data-stu-id="00537-132">Create approval workflows for the recovery of value-added tax (VAT).</span></span>  |
