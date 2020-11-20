---
title: 支出条目（精简）
description: 此主题提供有关如何在精简部署中使用支出条目的信息。
author: stsporen
manager: AnnBe
ms.date: 10/06/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 536c961593599df8e7e2986f92259b0e690eae8b
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/28/2020
ms.locfileid: "4121072"
---
# <a name="expense-entry-lite"></a><span data-ttu-id="976a3-103">支出条目（精简）</span><span class="sxs-lookup"><span data-stu-id="976a3-103">Expense entry (lite)</span></span>

<span data-ttu-id="976a3-104">_**适用于：** 精简部署 - 估价交易开票_</span><span class="sxs-lookup"><span data-stu-id="976a3-104">_**Applies to:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="976a3-105">基本或精简支出管理是一项记录简单支出的功能。</span><span class="sxs-lookup"><span data-stu-id="976a3-105">Basic, or lite, expense management is the capability to record simple expenses.</span></span> <span data-ttu-id="976a3-106">您可以记录一个项目的支出，然后项目审批者将对其进行审核和审批。</span><span class="sxs-lookup"><span data-stu-id="976a3-106">You can record expenses against a project, and then the project approver will review and approve them.</span></span>

<span data-ttu-id="976a3-107">有关 Dynamics 365 Project Operations 中的支出功能的详细信息，请参阅[支出概述](expense-overview.md)。</span><span class="sxs-lookup"><span data-stu-id="976a3-107">For more information about expense capabilities in Dynamics 365 Project Operations, see [Expense overview](expense-overview.md).</span></span>

## <a name="capture-a-basic-expense"></a><span data-ttu-id="976a3-108">捕获基本支出</span><span class="sxs-lookup"><span data-stu-id="976a3-108">Capture a basic expense</span></span>

<span data-ttu-id="976a3-109">您可以捕获支出，以将其提交给审批者。</span><span class="sxs-lookup"><span data-stu-id="976a3-109">You can capture your expenses so that you can submit them to the approver.</span></span>

1. <span data-ttu-id="976a3-110">转到 **支出**，选择 **新建**。</span><span class="sxs-lookup"><span data-stu-id="976a3-110">Go to **Expenses**, and select **New**.</span></span>
2. <span data-ttu-id="976a3-111">在 **新支出** 页上，输入所需的支出信息，然后选择 **保存**。</span><span class="sxs-lookup"><span data-stu-id="976a3-111">On the **New Expense** page, enter the required expense information, and then select **Save**.</span></span>

## <a name="submit-a-basic-expense"></a><span data-ttu-id="976a3-112">提交基本支出</span><span class="sxs-lookup"><span data-stu-id="976a3-112">Submit a basic expense</span></span>

<span data-ttu-id="976a3-113">完成所有支出的捕获并准备好将其进行审批后，必须提交。</span><span class="sxs-lookup"><span data-stu-id="976a3-113">After you've finished capturing all your expenses, and you're ready to have them approved, you must submit them.</span></span>

1. <span data-ttu-id="976a3-114">转到 **支出**，选择一项支出。</span><span class="sxs-lookup"><span data-stu-id="976a3-114">Go to **Expenses**, and select an expense.</span></span> <span data-ttu-id="976a3-115">或者，使用标题上的复选框选择所有支出。</span><span class="sxs-lookup"><span data-stu-id="976a3-115">Or, select all the expenses by using the check box on the header.</span></span>
2. <span data-ttu-id="976a3-116">选择 **提交**。</span><span class="sxs-lookup"><span data-stu-id="976a3-116">Select **Submit**.</span></span> <span data-ttu-id="976a3-117">系统将处理选定的条目，然后创建支出审批请求。</span><span class="sxs-lookup"><span data-stu-id="976a3-117">The system processes the selected entries and then creates expense approval requests.</span></span>

## <a name="recall-a-basic-expense"></a><span data-ttu-id="976a3-118">撤消基本支出</span><span class="sxs-lookup"><span data-stu-id="976a3-118">Recall a basic expense</span></span>

<span data-ttu-id="976a3-119">当您误提交支出时，可以撤消。</span><span class="sxs-lookup"><span data-stu-id="976a3-119">When you submit an expense by mistake, you can recall it.</span></span> <span data-ttu-id="976a3-120">撤消支出条目所需的时间取决于其审批阶段。</span><span class="sxs-lookup"><span data-stu-id="976a3-120">The time that is required to recall an expense entry depends on its approval stage.</span></span>  <span data-ttu-id="976a3-121">如果审批者尚未审批条目，可以立即撤消。</span><span class="sxs-lookup"><span data-stu-id="976a3-121">If the approver hasn't yet approved the entry, the recall can occur immediately.</span></span> <span data-ttu-id="976a3-122">但是，如果条目已经完成审批，则会要求审批者批准撤消，从而撤消交易。</span><span class="sxs-lookup"><span data-stu-id="976a3-122">However, if the entry has already been approved, the approver is asked to approve the recall and reverse the transactions.</span></span>

1. <span data-ttu-id="976a3-123">转到 **支出**，然后在支出列表中，选择要撤消的支出。</span><span class="sxs-lookup"><span data-stu-id="976a3-123">Go to **Expenses**, and then, in the list of expenses, select the expense to recall.</span></span>
2. <span data-ttu-id="976a3-124">选择 **撤消**。</span><span class="sxs-lookup"><span data-stu-id="976a3-124">Select **Recall**.</span></span> <span data-ttu-id="976a3-125">如果支出条目尚未审批，系统会立即将其撤消。</span><span class="sxs-lookup"><span data-stu-id="976a3-125">If the expense entry hasn't yet been approved, the system immediately recalls it.</span></span> <span data-ttu-id="976a3-126">如果支出条目已完成审批，将创建一个撤消请求，通知审批者您要撤消支出。</span><span class="sxs-lookup"><span data-stu-id="976a3-126">If the expense entry has already been approved, a recall request is created to notify the approver that you want to reverse the expense.</span></span> <span data-ttu-id="976a3-127">然后，审批者将确认可以撤消，条目将退回。</span><span class="sxs-lookup"><span data-stu-id="976a3-127">The approver will then confirm that the reversal can be done, and the entry will be returned.</span></span>

## <a name="delete-a-basic-expense"></a><span data-ttu-id="976a3-128">刪除基本支出</span><span class="sxs-lookup"><span data-stu-id="976a3-128">Delete a basic expense</span></span>

<span data-ttu-id="976a3-129">尚未提交的支出可以删除。</span><span class="sxs-lookup"><span data-stu-id="976a3-129">Expenses that haven't yet been submitted can be deleted.</span></span> <span data-ttu-id="976a3-130">若要删除已提交的支出，必须先将其撤消。</span><span class="sxs-lookup"><span data-stu-id="976a3-130">To delete an expense that has already been submitted, you must first recall it.</span></span>

## <a name="see-also"></a><span data-ttu-id="976a3-131">另请参阅</span><span class="sxs-lookup"><span data-stu-id="976a3-131">See also</span></span>

- [<span data-ttu-id="976a3-132">审批概述</span><span class="sxs-lookup"><span data-stu-id="976a3-132">Approvals overview</span></span>](../approvals/approvals-overview.md)
