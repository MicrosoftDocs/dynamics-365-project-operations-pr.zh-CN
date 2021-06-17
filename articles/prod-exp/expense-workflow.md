---
title: 支出管理工作流
description: 此主题介绍如何使用 Microsoft Dynamics 365 Finance 中的工作流系统在支出管理中设置支出报表审核流程。
author: ShylaThompson
ms.date: 09/13/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WorkflowtableListPageRnr
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 51ac2712f62d5c5d85b21c0ea929517ccb893bca
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/10/2021
ms.locfileid: "6005195"
---
# <a name="expense-management-workflow"></a><span data-ttu-id="77fd9-103">支出管理工作流</span><span class="sxs-lookup"><span data-stu-id="77fd9-103">Expense management workflow</span></span>

<span data-ttu-id="77fd9-104">可使用工作流系统设置“支出管理”中支出报表的审核流程。</span><span class="sxs-lookup"><span data-stu-id="77fd9-104">You can use the workflow system to set up a review process for expense reports in Expense management.</span></span> <span data-ttu-id="77fd9-105">您可以设置使用以下条件确定由谁审核支出报表的工作流：</span><span class="sxs-lookup"><span data-stu-id="77fd9-105">You can set up a workflow that uses the following criteria to determine who approves expense reports:</span></span>

- <span data-ttu-id="77fd9-106">员工报告层次结构和预定义的审核限制</span><span class="sxs-lookup"><span data-stu-id="77fd9-106">The employee reporting hierarchy and predefined approval limits</span></span>
- <span data-ttu-id="77fd9-107">支持临时审核人和最终审核人的多级审核</span><span class="sxs-lookup"><span data-stu-id="77fd9-107">Multi-level approval that supports interim approvers and a final approver</span></span>
- <span data-ttu-id="77fd9-108">财务维度和项目责任</span><span class="sxs-lookup"><span data-stu-id="77fd9-108">Financial dimensions and project responsibility</span></span>
- <span data-ttu-id="77fd9-109">给特定用户或用户组的分配</span><span class="sxs-lookup"><span data-stu-id="77fd9-109">Assignment to specific users or user groups</span></span>

<span data-ttu-id="77fd9-110">工作流审核可为支出报表、出差申请、预付现金和增值税 (VAT) 还原而创建。</span><span class="sxs-lookup"><span data-stu-id="77fd9-110">Workflow approvals can be created for expense reports, travel requisitions, cash advances, and value-added tax (VAT) recovery.</span></span>

<span data-ttu-id="77fd9-111">**示例**</span><span class="sxs-lookup"><span data-stu-id="77fd9-111">**Example**</span></span>

<span data-ttu-id="77fd9-112">以下流程是针对某一支出报表的出差支出管理工作流程示例。</span><span class="sxs-lookup"><span data-stu-id="77fd9-112">The following process is an example of the expense management workflow for an expense report.</span></span>

1. <span data-ttu-id="77fd9-113">员工创建和保存支出报表。</span><span class="sxs-lookup"><span data-stu-id="77fd9-113">An employee creates and saves an expense report.</span></span>
2. <span data-ttu-id="77fd9-114">员工提交支出报表以供审核。</span><span class="sxs-lookup"><span data-stu-id="77fd9-114">The employee submits the expense report for approval.</span></span> <span data-ttu-id="77fd9-115">审核人根据工作流设置后定义的规则标识。</span><span class="sxs-lookup"><span data-stu-id="77fd9-115">The approver is identified based on the rules that were defined when the workflow was set up.</span></span>
3. <span data-ttu-id="77fd9-116">审核人接收支出报表可供审核的通知。</span><span class="sxs-lookup"><span data-stu-id="77fd9-116">The approver receives a notification that an expense report is ready for approval.</span></span> <span data-ttu-id="77fd9-117">审核人审核支出报表并验证是否满足以下条件：</span><span class="sxs-lookup"><span data-stu-id="77fd9-117">The approver reviews the expense report and verifies that the following conditions are met:</span></span>

    - <span data-ttu-id="77fd9-118">支出不违反任何支出策略。</span><span class="sxs-lookup"><span data-stu-id="77fd9-118">The expenses don't violate any expense policies.</span></span> <span data-ttu-id="77fd9-119">如果支出违反策略，审核人验证支出报表中是否包括有效的业务理由。</span><span class="sxs-lookup"><span data-stu-id="77fd9-119">If an expense violates a policy, the approver verifies that the expense report includes a valid business justification.</span></span>
    - <span data-ttu-id="77fd9-120">电子收据是否附加到支出报表。</span><span class="sxs-lookup"><span data-stu-id="77fd9-120">Electronic receipts are attached to the expense report.</span></span>

4. <span data-ttu-id="77fd9-121">审核人审核整个支出报表。</span><span class="sxs-lookup"><span data-stu-id="77fd9-121">The approver approves the expense report.</span></span>
5. <span data-ttu-id="77fd9-122">将支出报表分配给应付账款协调员以供过帐。</span><span class="sxs-lookup"><span data-stu-id="77fd9-122">The expense report is assigned to the Accounts payable coordinator for posting.</span></span>
6. <span data-ttu-id="77fd9-123">发生以下步骤之一，具体取决于是否配置自动过帐：</span><span class="sxs-lookup"><span data-stu-id="77fd9-123">One of the following steps occurs, depending on whether automatic posting is configured:</span></span>

    - <span data-ttu-id="77fd9-124">如果配置自动过帐，则对支出报表进行付款处理，并且更新支出报表的状态。</span><span class="sxs-lookup"><span data-stu-id="77fd9-124">If automatic posting is configured, the expense report is processed for payment, and the status of the expense report is updated.</span></span>
    - <span data-ttu-id="77fd9-125">如果没有配置自动过帐，应付账款协调员验证所有原始收据已提交，并且收货与支出报表上的成本相符。</span><span class="sxs-lookup"><span data-stu-id="77fd9-125">If automatic posting isn't configured, the Accounts payable coordinator verifies that all original receipts have been submitted, and that the receipts are aligned with the expenses on the expense report.</span></span> <span data-ttu-id="77fd9-126">还必须验证支出报表上的所有税码是否正确。</span><span class="sxs-lookup"><span data-stu-id="77fd9-126">All tax codes that are entered on the expense report must also be verified as correct.</span></span>

<span data-ttu-id="77fd9-127">在验证这些需求后，将支出报表过帐。</span><span class="sxs-lookup"><span data-stu-id="77fd9-127">After these requirements are verified, the expense report is posted.</span></span>

<span data-ttu-id="77fd9-128">在支出报表过帐后，对支出报表授权付款，并且员工获得补偿。</span><span class="sxs-lookup"><span data-stu-id="77fd9-128">After the expense report is posted, payment is authorized for the expense report, and the employee is reimbursed.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]