---
title: 支出报表和多人审批
description: 此主题提供有关需要多人审批的支出报表的信息。
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
ms.openlocfilehash: cfa8677f38e9468aa3236f587d2e9bd5af839054
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/28/2020
ms.locfileid: "4120982"
---
# <a name="expense-reports-and-multiple-approvers"></a><span data-ttu-id="6af78-103">支出报表和多人审批</span><span class="sxs-lookup"><span data-stu-id="6af78-103">Expense reports and multiple approvers</span></span>

<span data-ttu-id="6af78-104">_**适用于：** 基于资源/非库存场景的 Project Operations，精简部署 - 估价开票交易_</span><span class="sxs-lookup"><span data-stu-id="6af78-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="6af78-105">根据您的组织的支出审批政策，可能必须由多个人员审批提交的支出报表。</span><span class="sxs-lookup"><span data-stu-id="6af78-105">Depending on your organization's expense approval policies, more than one person might have to approve a submitted expense report.</span></span> <span data-ttu-id="6af78-106">在设置支出报表审批的工作流程时，您可以添加包含一个或多个支出报表审批者的任务或步骤的工作流元素。</span><span class="sxs-lookup"><span data-stu-id="6af78-106">When you set up the workflow process for expense report approval, you can add workflow elements that include tasks or steps for one or more expense report approvers.</span></span> <span data-ttu-id="6af78-107">例如，您可能需要所有支出报表由两名单独的人员（提交报表的员工的经理和应付帐款协调员）审批。</span><span class="sxs-lookup"><span data-stu-id="6af78-107">For example, you might require that all expense reports be approved by two separate people, the manager of the employee who submitted the report and the Accounts payable coordinator.</span></span>

<span data-ttu-id="6af78-108">如果您决定需要多个支出报表审批者，可以采用以下任一方式添加工作流元素：</span><span class="sxs-lookup"><span data-stu-id="6af78-108">If you decide to require multiple expense report approvers, you can add the workflow elements in any of the following ways:</span></span>

- <span data-ttu-id="6af78-109">添加一个具有一个步骤的审批元素。</span><span class="sxs-lookup"><span data-stu-id="6af78-109">Add one approval element that has one step.</span></span> <span data-ttu-id="6af78-110">例如，该步骤可能要求将支出报表分配给某个用户组，并由该用户组成员的 50% 进行审批。</span><span class="sxs-lookup"><span data-stu-id="6af78-110">For example, the step might require that an expense report be assigned to a user group, and that it be approved by 50 percent of the user group's members.</span></span>
- <span data-ttu-id="6af78-111">添加一个具有多个步骤的审批元素。</span><span class="sxs-lookup"><span data-stu-id="6af78-111">Add one approval element that has multiple steps.</span></span> <span data-ttu-id="6af78-112">例如，审批元素可能包括以下步骤：</span><span class="sxs-lookup"><span data-stu-id="6af78-112">For example, the approval element might have the following steps:</span></span>

    1. <span data-ttu-id="6af78-113">提交支出报表的员工的经理审批报表。</span><span class="sxs-lookup"><span data-stu-id="6af78-113">The manager of the employee who submitted the expense report approves it.</span></span>
    2. <span data-ttu-id="6af78-114">应付帐款职员验证收据和支出报表项。</span><span class="sxs-lookup"><span data-stu-id="6af78-114">The Accounts payable clerk verifies the receipts and the expense report items.</span></span>
    3. <span data-ttu-id="6af78-115">预算负责人审批支出报表。</span><span class="sxs-lookup"><span data-stu-id="6af78-115">The budget owner approves the expense report.</span></span>

- <span data-ttu-id="6af78-116">添加多个审批元素，每个元素包含一个步骤。</span><span class="sxs-lookup"><span data-stu-id="6af78-116">Add multiple approval elements, each of which has one step.</span></span> <span data-ttu-id="6af78-117">例如，您可以为下列每个步骤添加单独的审批元素：</span><span class="sxs-lookup"><span data-stu-id="6af78-117">For example, you might add a separate approval element for each of the following steps:</span></span>

    1. <span data-ttu-id="6af78-118">员工的经理审批支出报表。</span><span class="sxs-lookup"><span data-stu-id="6af78-118">The employee's manager approves the expense report.</span></span>
    2. <span data-ttu-id="6af78-119">预算负责人审批支出报表。</span><span class="sxs-lookup"><span data-stu-id="6af78-119">The budget owner approves the expense report.</span></span>
