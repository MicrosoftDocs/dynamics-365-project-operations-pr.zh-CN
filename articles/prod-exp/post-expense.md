---
title: 过帐支出报表
description: 本主题说明如何将支出报表过帐到总帐。
author: saraschi2
manager: AnnBe
ms.date: 02/26/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TrvPerDiems
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 36be76c0c9f25cb93921acee36a820e276cad625
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/15/2021
ms.locfileid: "5271297"
---
# <a name="post-an-expense-report"></a><span data-ttu-id="3d542-103">过帐支出报表</span><span class="sxs-lookup"><span data-stu-id="3d542-103">Post an expense report</span></span>

<span data-ttu-id="3d542-104">在支出报表已审核和转移到总帐后，可以将其过帐到总帐。</span><span class="sxs-lookup"><span data-stu-id="3d542-104">After an expense report has been approved and transferred to the general journal, it can be posted to the general ledger.</span></span> <span data-ttu-id="3d542-105">在您过帐支出报表时，将标识符合增值税 (VAT) 退税条件的支出。</span><span class="sxs-lookup"><span data-stu-id="3d542-105">When you post an expense report, expenses that are eligible for recovery of value-added tax (VAT) are identified.</span></span> <span data-ttu-id="3d542-106">验证和退回增值税付款的任务将分配给负责验证支出报表的员工。</span><span class="sxs-lookup"><span data-stu-id="3d542-106">The task of verifying and recovering VAT payments is assigned to the employee who is responsible for verifying the expense report.</span></span>

<span data-ttu-id="3d542-107">如果应向雇佣该员工的公司以外的其它公司收取支出报表中的支出， 您必须验证是哪个公司欠这笔支出，以及这笔支出应付给哪个公司。</span><span class="sxs-lookup"><span data-stu-id="3d542-107">If expenses on an expense report are charged to a company other than the company that employs the employee, you must verify the company that those expenses are owed to and the company that the expenses are owed from.</span></span> <span data-ttu-id="3d542-108">例如，提交支出报表的员工为 DAT 公司工作，但向 DIR 公司收取费用。</span><span class="sxs-lookup"><span data-stu-id="3d542-108">For example, the employee who submitted an expense report works for the DAT company but charged an expense to the DIR company.</span></span> <span data-ttu-id="3d542-109">在这种情况下，DAT 是支出被欠公司，DIR 是欠款公司。</span><span class="sxs-lookup"><span data-stu-id="3d542-109">In this case, DAT is the company that the expense is owed to, and DIR is the company that the expense is owed from.</span></span> <span data-ttu-id="3d542-110">验证这些日记帐行后，您可以将支出明细过帐到总帐。</span><span class="sxs-lookup"><span data-stu-id="3d542-110">After you verify these journal lines, you can post the expense lines to the general ledger.</span></span>

<span data-ttu-id="3d542-111">若要过帐支出报表，在 **批准的支出报表** 页上，选择支出报表，然后在操作窗格上选择 **过帐**。</span><span class="sxs-lookup"><span data-stu-id="3d542-111">To post an expense report, on the **Approved expense reports** page, select the expense report, and then, on the Action Pane, select **Post**.</span></span>

<span data-ttu-id="3d542-112">您也可以同时在列表中过帐所有支出报表。</span><span class="sxs-lookup"><span data-stu-id="3d542-112">You can also post all the expense reports in the list at the same time.</span></span> <span data-ttu-id="3d542-113">选择所有支出报表，然后选择 **过帐**。</span><span class="sxs-lookup"><span data-stu-id="3d542-113">Select all the expense reports, and then select **Post**.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]