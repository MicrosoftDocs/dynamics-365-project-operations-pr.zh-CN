---
title: 内部公司支出
description: 本主题提供有关如何使用内部公司支出将工作人员的支出分配给为其执行工作的法人的信息。
author: ShylaThompson
manager: AnnBe
ms.date: 05/20/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TrvParameters
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d908a1c062f5b7f01cf340dcd6f7f24714a992bf
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/15/2021
ms.locfileid: "5271522"
---
# <a name="intercompany-expenses"></a><span data-ttu-id="50fe4-103">内部公司支出</span><span class="sxs-lookup"><span data-stu-id="50fe4-103">Intercompany expenses</span></span>

<span data-ttu-id="50fe4-104">由在组织中的一个法人雇佣的工作人员可能在同一组织执行其他法人的工作。</span><span class="sxs-lookup"><span data-stu-id="50fe4-104">A worker who is employed by one legal entity in an organization might perform work for another legal entity in the same organization.</span></span> <span data-ttu-id="50fe4-105">您可以使用内部公司支出将工作人员的支出分配给为其执行工作的法人。</span><span class="sxs-lookup"><span data-stu-id="50fe4-105">You can use intercompany expenses to assign the worker’s expenses to the legal entity for which the  work was performed.</span></span> <span data-ttu-id="50fe4-106">雇用该工作人员的法人称为借出方法人。</span><span class="sxs-lookup"><span data-stu-id="50fe4-106">The legal entity that employs the worker is called the loaning legal entity.</span></span> <span data-ttu-id="50fe4-107">工作人员产生支出的法人称为“借款法人”。</span><span class="sxs-lookup"><span data-stu-id="50fe4-107">The legal entity for which the worker incurs expenses is called the borrowing legal entity.</span></span> 

<span data-ttu-id="50fe4-108">您必须先启用内部公司支出行，工作人员才能够创建和提交内部公司支出。</span><span class="sxs-lookup"><span data-stu-id="50fe4-108">Before a worker can create and submit intercompany expenses, you must enable intercompany expense lines.</span></span> <span data-ttu-id="50fe4-109">在借出法人中，在 **支出管理参数** 页上，选择 **允许内部公司支出行**。</span><span class="sxs-lookup"><span data-stu-id="50fe4-109">In the loaning legal entity, on the **Expense management parameters** page, select **Allow intercompany expense lines**.</span></span> 

## <a name="tax-posting-for-intercompany-expenses"></a><span data-ttu-id="50fe4-110">内部公司支出的税金过帐</span><span class="sxs-lookup"><span data-stu-id="50fe4-110">Tax posting for intercompany expenses</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="50fe4-111">您必须先在“总帐销售税”设置中启用此功能，然后才可以在支出报表中使用与借出（来源）法人关联的税组，而不是借款（目标）法人。</span><span class="sxs-lookup"><span data-stu-id="50fe4-111">Before you can use tax groups that are associated with the loaning (source) legal entity instead of the borrowing (destination) legal entity in your expense report, you must enable the functionality in the General ledger sales tax setup.</span></span> <span data-ttu-id="50fe4-112">当 **内部公司税款过帐法人** 参数设置为 **来源**，**应用销售税税收规则** 设置为 **否** 时，将使用借出法人的税收组合。</span><span class="sxs-lookup"><span data-stu-id="50fe4-112">When the **Legal entity for intercompany tax posting** parameter is set to **Source** and **Apply sales tax taxation rules** is set to **No**, the tax combination for the loaning legal entity is used.</span></span> <span data-ttu-id="50fe4-113">如果同一个参数设置为 **目标**，将使用借入方法人的税务组合。</span><span class="sxs-lookup"><span data-stu-id="50fe4-113">When the same parameter is set to **Destination**, the tax combination for borrowing legal entity will be used.</span></span> <span data-ttu-id="50fe4-114">对于美国的法人来说，如果此参数设置为 **源**，则还必须在新的 **分类帐过帐组** 页中配置 **应收销售税** 字段。</span><span class="sxs-lookup"><span data-stu-id="50fe4-114">For legal entities in the United States, when the parameter is set to **Source**, the **Sales tax receivable** field must also be configured on the new **Ledger posting groups** page.</span></span> <span data-ttu-id="50fe4-115">成本核算引擎将把此字段中的信息用于与税务有关的成本核算条目。</span><span class="sxs-lookup"><span data-stu-id="50fe4-115">The accounting engine will use the information from this field for tax-related accounting entry.</span></span>   
<span data-ttu-id="50fe4-116">无论是否有项目，此行为对过帐的支出行都一致。</span><span class="sxs-lookup"><span data-stu-id="50fe4-116">The behavior is consistent for expense lines posted with or without a project.</span></span>  


[!INCLUDE[footer-include](../includes/footer-banner.md)]