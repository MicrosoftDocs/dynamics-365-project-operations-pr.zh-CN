---
title: 支出报表的多人审批
description: 此主题提供有关需要多人审批的支出报表的信息。
author: saraschi2
manager: AnnBe
ms.date: 02/23/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TrvExpensesReportList
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9b6d07f00fd6c1ba2d860787665d95f95f7b1a89
ms.sourcegitcommit: 9f31b33ed6e7f1b49200a407913201a1337f3401
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/14/2021
ms.locfileid: "4960596"
---
# <a name="multiple-approvers-on-an-expense-report"></a><span data-ttu-id="0dc0d-103">支出报表的多人审批</span><span class="sxs-lookup"><span data-stu-id="0dc0d-103">Multiple approvers on an expense report</span></span>

<span data-ttu-id="0dc0d-104">根据您组织的支出审核策略，可能需要多人审核由员工提交的支出报表。</span><span class="sxs-lookup"><span data-stu-id="0dc0d-104">Depending on your organization's expense approval policies, more than one person might have to approve an expense report that is submitted by an employee.</span></span> <span data-ttu-id="0dc0d-105">在设置支出报表审批的工作流程时，您可以添加包含一个或多个支出报表审批者的任务或步骤的工作流元素。</span><span class="sxs-lookup"><span data-stu-id="0dc0d-105">When you set up the workflow process for expense report approval, you can add workflow elements that include tasks or steps for one or more expense report approvers.</span></span> <span data-ttu-id="0dc0d-106">例如，您可能需要所有支出报表首先由提交报表的员工经理审核，然后由应付帐款协调员进行审核。</span><span class="sxs-lookup"><span data-stu-id="0dc0d-106">For example, you might require that all expense reports be approved first by the manager of the employee who submitted the report and then by the Accounts payable coordinator.</span></span>

<span data-ttu-id="0dc0d-107">如果您决定需要多个支出报表审批者，可以采用以下任一方式添加工作流元素：</span><span class="sxs-lookup"><span data-stu-id="0dc0d-107">If you decide to require multiple expense report approvers, you can add the workflow elements in any of the following ways:</span></span>

- <span data-ttu-id="0dc0d-108">添加一个具有一个步骤的审批元素。</span><span class="sxs-lookup"><span data-stu-id="0dc0d-108">Add one approval element that has one step.</span></span> <span data-ttu-id="0dc0d-109">例如，该步骤可能要求将支出报表分配给某个用户组，并由该用户组成员的 50% 进行审批。</span><span class="sxs-lookup"><span data-stu-id="0dc0d-109">For example, the step might require that an expense report be assigned to a user group, and that it be approved by 50 percent of the user group's members.</span></span>
- <span data-ttu-id="0dc0d-110">添加一个具有多个步骤的审批元素。</span><span class="sxs-lookup"><span data-stu-id="0dc0d-110">Add one approval element that has multiple steps.</span></span> <span data-ttu-id="0dc0d-111">例如，审批元素可能包括以下步骤：</span><span class="sxs-lookup"><span data-stu-id="0dc0d-111">For example, the approval element might have the following steps:</span></span>

    1. <span data-ttu-id="0dc0d-112">提交支出报表的员工的经理审批报表。</span><span class="sxs-lookup"><span data-stu-id="0dc0d-112">The manager of the employee who submitted the expense report approves it.</span></span>
    2. <span data-ttu-id="0dc0d-113">应付帐款职员验证收据和支出报表项。</span><span class="sxs-lookup"><span data-stu-id="0dc0d-113">The Accounts payable clerk verifies the receipts and the expense report items.</span></span>
    3. <span data-ttu-id="0dc0d-114">预算负责人审批支出报表。</span><span class="sxs-lookup"><span data-stu-id="0dc0d-114">The budget owner approves the expense report.</span></span>

- <span data-ttu-id="0dc0d-115">添加多个审批元素，每个元素包含一个步骤。</span><span class="sxs-lookup"><span data-stu-id="0dc0d-115">Add multiple approval elements, each of which has one step.</span></span> <span data-ttu-id="0dc0d-116">例如，您可以为下列每个步骤添加单独的审批元素：</span><span class="sxs-lookup"><span data-stu-id="0dc0d-116">For example, you might add a separate approval element for each of the following steps:</span></span>

    1. <span data-ttu-id="0dc0d-117">员工的经理审批支出报表。</span><span class="sxs-lookup"><span data-stu-id="0dc0d-117">The employee's manager approves the expense report.</span></span>
    2. <span data-ttu-id="0dc0d-118">预算负责人审批支出报表。</span><span class="sxs-lookup"><span data-stu-id="0dc0d-118">The budget owner approves the expense report.</span></span>
