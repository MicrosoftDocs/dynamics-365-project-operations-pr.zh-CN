---
title: 更正发票
description: 本主题提供有关更正发票的信息。
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 1ebfec053a59bbadd261d4333f6737cf16292e81
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/28/2020
ms.locfileid: "4122377"
---
# <a name="corrected-invoices"></a><span data-ttu-id="beec1-103">更正发票</span><span class="sxs-lookup"><span data-stu-id="beec1-103">Corrected invoices</span></span>

<span data-ttu-id="beec1-104">_**适用于：** 面向资源/非库存场景的 Project Operations_</span><span class="sxs-lookup"><span data-stu-id="beec1-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="beec1-105">可以编辑已确认的发票。</span><span class="sxs-lookup"><span data-stu-id="beec1-105">Confirmed invoices can be edited.</span></span> <span data-ttu-id="beec1-106">编辑已确认的发票时，将创建更正发票的草稿。</span><span class="sxs-lookup"><span data-stu-id="beec1-106">When you edit a confirmed invoice, a draft of the corrected invoice is created.</span></span> <span data-ttu-id="beec1-107">因为假设您希望冲销原始发票中的所有交易和数量，所以此更正发票中包含原始发票中的所有交易，并且其中的所有数量均为零 (0)。</span><span class="sxs-lookup"><span data-stu-id="beec1-107">Because the assumption is that you want to reverse all the transactions and quantities from the original invoice, the corrected invoice includes all the transactions from the original invoice, and all the quantities on it are zero (0).</span></span>

<span data-ttu-id="beec1-108">当交易不需要更正时，可以将其从草稿纠正发票中删除。</span><span class="sxs-lookup"><span data-stu-id="beec1-108">When transactions don't require correction, you can remove them from the draft corrective invoice.</span></span> <span data-ttu-id="beec1-109">若要仅冲销或返回部分数量，可以编辑明细详细信息中的“数量”字段。</span><span class="sxs-lookup"><span data-stu-id="beec1-109">To reverse or return only a partial quantity, you can edit the Quantity field on the line detail.</span></span> <span data-ttu-id="beec1-110">如果打开发票明细详细信息，可以看到原始发票数量。</span><span class="sxs-lookup"><span data-stu-id="beec1-110">If you open the invoice line detail, you can see the original invoice quantity.</span></span> <span data-ttu-id="beec1-111">然后可以编辑当前发票数量，使其比原始发票数量少或多。</span><span class="sxs-lookup"><span data-stu-id="beec1-111">You can then edit the current invoice quantity so that it's less than or more than the original invoice quantity.</span></span>

<span data-ttu-id="beec1-112">确认纠正发票时，将撤消原始已记帐实际销售额，并创建新的已记帐实际销售额。</span><span class="sxs-lookup"><span data-stu-id="beec1-112">When you confirm a corrective invoice, the original billed sales actual is reversed, and a new billed sales actual is created.</span></span> <span data-ttu-id="beec1-113">如果减少了数量，差额将导致也创建一项新的未记帐实际销售额。</span><span class="sxs-lookup"><span data-stu-id="beec1-113">If the quantity was reduced, the difference will cause a new unbilled sales actual to be created too.</span></span> <span data-ttu-id="beec1-114">例如，如果原始已记帐销售额是八小时的，并且更正发票明细详细信息的减少后数量为六小时，将冲销原始已记帐销售明细，并创建两项新的实际值：</span><span class="sxs-lookup"><span data-stu-id="beec1-114">For example, if the original billed sale was for eight hours, and the corrected invoice line detail has a reduced quantity of six hours, the original billed sales line is revered and two new actuals are created:</span></span>

- <span data-ttu-id="beec1-115">六小时的已记帐实际销售额。</span><span class="sxs-lookup"><span data-stu-id="beec1-115">A billed sales actual for six hours.</span></span>
- <span data-ttu-id="beec1-116">其余两小时的未记帐实际销售额。</span><span class="sxs-lookup"><span data-stu-id="beec1-116">An unbilled sales actual for the remaining two hours.</span></span> <span data-ttu-id="beec1-117">以后可为此交易记帐或标记为非应计费，具体取决于与客户的协商结果。</span><span class="sxs-lookup"><span data-stu-id="beec1-117">This transaction can either be billed later or marked as non-chargeable, depending on the negotiations with the customer.</span></span>
