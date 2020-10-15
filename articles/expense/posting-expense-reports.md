---
title: 过帐支出报表
description: 此主题介绍如何过帐支出报表。
author: suvaidya
manager: AnnBe
ms.date: 09/09/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: ''
ms.author: shylaw
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: ec897373cd74f7d7f63cd9ca4c46f4245336eb7f
ms.sourcegitcommit: 56c42d7f5995a674426a1c2a81bae897dceb391c
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/01/2020
ms.locfileid: "3907397"
---
# <a name="post-expense-reports"></a><span data-ttu-id="d8b7c-103">过帐支出报表</span><span class="sxs-lookup"><span data-stu-id="d8b7c-103">Post expense reports</span></span>

<span data-ttu-id="d8b7c-104">在支出报表被批准并转移到常规日记帐后，可以将其过帐。</span><span class="sxs-lookup"><span data-stu-id="d8b7c-104">After an expense report has been approved and transferred to the general journal, it can be posted.</span></span> <span data-ttu-id="d8b7c-105">在您过帐支出报表时，将标识符合增值税 (VAT) 退税条件的支出。</span><span class="sxs-lookup"><span data-stu-id="d8b7c-105">When you post an expense report, expenses that are eligible for recovery of value-added tax (VAT) are identified.</span></span> <span data-ttu-id="d8b7c-106">验证和退回增值税付款的任务将分配给负责验证支出报表的员工。</span><span class="sxs-lookup"><span data-stu-id="d8b7c-106">The task of verifying and recovering VAT payments is assigned to the employee who is responsible for verifying the expense report.</span></span>

<span data-ttu-id="d8b7c-107">如果支出报表上的支出是由雇用该员工的公司以外的其他公司收取的，您必须同时验证这些支出所属于的公司和欠款公司。</span><span class="sxs-lookup"><span data-stu-id="d8b7c-107">If expenses on an expense report are charged to a company other than the company that employs the employee, you must verify both the company that those expenses are owed to and the company that they are owed from.</span></span> <span data-ttu-id="d8b7c-108">例如，提交支出报表的员工为 DAT 公司工作，但向 DIR 公司收取费用。</span><span class="sxs-lookup"><span data-stu-id="d8b7c-108">For example, the employee who submitted an expense report works for the DAT company but charged an expense to the DIR company.</span></span> <span data-ttu-id="d8b7c-109">在这种情况下，DAT 是支出被欠公司，DIR 是欠款公司。</span><span class="sxs-lookup"><span data-stu-id="d8b7c-109">In this case, DAT is the company that the expense is owed to, and DIR is the company that the expense is owed from.</span></span> <span data-ttu-id="d8b7c-110">验证这些日记帐行后，您可以将支出明细过帐到总帐。</span><span class="sxs-lookup"><span data-stu-id="d8b7c-110">After you verify these journal lines, you can post the expense lines to the general ledger.</span></span>

<span data-ttu-id="d8b7c-111">若要过帐支出报表，在**批准的支出报表**页上，选择支出报表，然后在操作窗格上选择**过帐**。</span><span class="sxs-lookup"><span data-stu-id="d8b7c-111">To post an expense report, on the **Approved expense reports** page, select the expense report, and then, on the Action Pane, select **Post**.</span></span>

<span data-ttu-id="d8b7c-112">您也可以同时在列表中过帐所有支出报表。</span><span class="sxs-lookup"><span data-stu-id="d8b7c-112">You can also post all the expense reports in the list at the same time.</span></span> <span data-ttu-id="d8b7c-113">选择所有支出报表，然后选择**过帐**。</span><span class="sxs-lookup"><span data-stu-id="d8b7c-113">Select all the expense reports, and then select **Post**.</span></span>
