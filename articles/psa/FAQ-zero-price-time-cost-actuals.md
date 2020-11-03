---
title: 为什么价格在时间成本实际值中默认为零？
description: 为什么价格在时间成本实际值中默认为 0 疑难解答。
author: rumant
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 8/21/2018
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 44d4952b77ac0a541cdf8e3e55f202c9209efdf4
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/16/2020
ms.locfileid: "4072623"
---
# <a name="why-is-the-price-defaulting-to-zero-on-time-cost-actuals"></a><span data-ttu-id="088a1-103">为什么价格在时间成本实际值中默认为零？</span><span class="sxs-lookup"><span data-stu-id="088a1-103">Why is the price defaulting to zero on time cost actuals?</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="088a1-104">此常见问题适用于交易记录类设置为“时间”且交易记录类型为“成本”的实际值。</span><span class="sxs-lookup"><span data-stu-id="088a1-104">This FAQ applies to actuals where the transaction class is set to Time and transaction type is Cost.</span></span> <span data-ttu-id="088a1-105">以下三项检查有助于您解答时间成本实际值中的价格为何默认为 0。</span><span class="sxs-lookup"><span data-stu-id="088a1-105">The following three checks will help you troubleshoot why the price is defaulting to 0 on time cost actuals.</span></span>
 
## <a name="check-1-identify-the-cost-price-list-for-the-project"></a><span data-ttu-id="088a1-106">检查 1：确定项目的成本价目表</span><span class="sxs-lookup"><span data-stu-id="088a1-106">Check 1: Identify the cost price list for the project</span></span>

<span data-ttu-id="088a1-107">从项目的实际值字段查找项目，然后转至项目页面。</span><span class="sxs-lookup"><span data-stu-id="088a1-107">Find the project from the project field of the actual and then go to the project page.</span></span> <span data-ttu-id="088a1-108">单击该字段中的合同签订部门链接。</span><span class="sxs-lookup"><span data-stu-id="088a1-108">Click on the contracting unit link in the field.</span></span> <span data-ttu-id="088a1-109">在“合同签订部门”页上，检查合同签订部门在“成本价目表”网格中是否有价目表。</span><span class="sxs-lookup"><span data-stu-id="088a1-109">On the Contracting Unit page, check if the contracting unit has a price list in the Cost Price Lists grid.</span></span>

<span data-ttu-id="088a1-110">如果有多个价目表，说明您忽略了此问题。</span><span class="sxs-lookup"><span data-stu-id="088a1-110">If there is more than one price list, you have isolated the problem.</span></span> <span data-ttu-id="088a1-111">Project Service 只为每个部门支持一个价目表。</span><span class="sxs-lookup"><span data-stu-id="088a1-111">Project Service only supports one price list per organizational unit.</span></span> <span data-ttu-id="088a1-112">删除该实体的所有价目表，直到部门的“成本价目表”网格中只有一个附加的价目表。</span><span class="sxs-lookup"><span data-stu-id="088a1-112">Remove all prices lists from this entity until there is only one price list attached in the Cost Price Lists grid of the Organizational Unit.</span></span>

<span data-ttu-id="088a1-113">如果没有价目表附加到部门，记下部门的货币。</span><span class="sxs-lookup"><span data-stu-id="088a1-113">If there are no price lists attached to the Organizational Unit, make a note of the currency of the Organizational unit.</span></span> <span data-ttu-id="088a1-114">转至 Project Service，然后转到“参数”，打开“价目表”选项卡。检查是否有任何价目表的上下文设置为“成本”以及与部门的货币匹配的货币。</span><span class="sxs-lookup"><span data-stu-id="088a1-114">Go to the Project Service and then Parameters and open the Price Lists tab. Check if there are any price lists with context set to Cost and currency that matches the currency of the Organizational Unit.</span></span>
 
<span data-ttu-id="088a1-115">如果没有与该条件匹配的价目表，说明您忽略了此问题。</span><span class="sxs-lookup"><span data-stu-id="088a1-115">If there are no price lists that match that criteria, you have isolated the problem.</span></span> <span data-ttu-id="088a1-116">请确保至少有一个价目表的上下文设置为“成本”且货币与部门的货币匹配。</span><span class="sxs-lookup"><span data-stu-id="088a1-116">Make sure to have at least one price list whose context is set to Cost and whose currency matches the currency of the Organizational Unit.</span></span>

<span data-ttu-id="088a1-117">如果有多个价目表与该条件匹配，请继续阅读本文档以进行更多检查。</span><span class="sxs-lookup"><span data-stu-id="088a1-117">If there is more than one price list that match that criteria, continue reading this document to make more checks.</span></span>

## <a name="check-2-are-any-of-the-price-lists-identified-above-valid-for-the-specific-date-of-the-time-cost-actual"></a><span data-ttu-id="088a1-118">检查 2：上方确定的任何价目表是否对时间成本实际值的特定日期有效？</span><span class="sxs-lookup"><span data-stu-id="088a1-118">Check 2: Are any of the price lists identified above valid for the specific date of the time cost actual?</span></span>

<span data-ttu-id="088a1-119">为了 Project Service 能够在确定默认价格时考虑价目表，该价目表应适用于时间成本实际值中的日期。</span><span class="sxs-lookup"><span data-stu-id="088a1-119">For Project Service to consider a price list for defaulting price, that price list should be applicable for the date on the time cost actual.</span></span> <span data-ttu-id="088a1-120">请检查以下内容查看上面确定的价目表是否适用：</span><span class="sxs-lookup"><span data-stu-id="088a1-120">Check the following to see if the price list(s) identified above are applicable:</span></span>

- <span data-ttu-id="088a1-121">检查附加的价目表的常规选项卡上的开始日期和结束日期是否不是空的。</span><span class="sxs-lookup"><span data-stu-id="088a1-121">Check if the start and end dates on the general tab for the price lists attached aren’t empty.</span></span> <span data-ttu-id="088a1-122">如果上面确定的价目表上的开始日期和结束日期是空的，说明您忽略了此问题。</span><span class="sxs-lookup"><span data-stu-id="088a1-122">If the start and end dates on price lists identified above are empty, you have isolated the problem.</span></span> 
- <span data-ttu-id="088a1-123">记下时间成本实际值中的开始日期字段，检查确定的任何价目表是否适用于该日期。</span><span class="sxs-lookup"><span data-stu-id="088a1-123">Make a note of the start date field on your time cost actual and check if any of the price lists identified is applicable for that date.</span></span> <span data-ttu-id="088a1-124">例如，时间成本实际值的日期应在价目表上的开始日期和结束日期之间。</span><span class="sxs-lookup"><span data-stu-id="088a1-124">For example, the date of the time cost actual should fall within the start date and end date on the price list.</span></span> 
    - <span data-ttu-id="088a1-125">如果没有覆盖时间成本实际值上该日期的价目表，说明您忽略了此问题。</span><span class="sxs-lookup"><span data-stu-id="088a1-125">If there is no price list that covers that date on the time cost actual, you have isolated the problem.</span></span> <span data-ttu-id="088a1-126">修改价目表的开始日期和结束日期以确保价目表覆盖时间成本实际值的日期。</span><span class="sxs-lookup"><span data-stu-id="088a1-126">Modify the start and end dates of the price list to ensure that the price list covers the date of the time cost actual.</span></span> 
    - <span data-ttu-id="088a1-127">如果有多个覆盖时间成本实际值上该日期的价目表，说明您忽略了此问题。</span><span class="sxs-lookup"><span data-stu-id="088a1-127">If there is more than one price list that covers the date on the time cost actual, you have isolated the problem.</span></span> <span data-ttu-id="088a1-128">您可以解决此问题，方法是编辑价目表的开始日期和结束日期，以只有一个价目表覆盖时间成本实际值的日期。</span><span class="sxs-lookup"><span data-stu-id="088a1-128">You can fix this by editing the start and end dates of the price list(s) so that there is only one price list that covers the date of the time cost actual.</span></span> 
    - <span data-ttu-id="088a1-129">如果只有一个价目表覆盖时间成本实际值的日期，移至文档中的下一项检查。</span><span class="sxs-lookup"><span data-stu-id="088a1-129">If there is only one price list that covers that date of the time cost actual, move to the next check in the document.</span></span>
<span data-ttu-id="088a1-130">在您进行必要的修改后，重新创建一个时间条目，批准它，然后确认时间成本实际值显示有效的价格。</span><span class="sxs-lookup"><span data-stu-id="088a1-130">Once you’ve done made the required fixes, recreate a time entry, approve it, and verify that the time cost actual shows a valid price.</span></span>

## <a name="check-3-is-there-a-price-in-the-price-list-for-the-pricing-dimensions-on-the-time-cost-actual"></a><span data-ttu-id="088a1-131">检查 3：价目表中是否有价格用于时间成本实际值中的定价维度？</span><span class="sxs-lookup"><span data-stu-id="088a1-131">Check 3: Is there a price in the price list for the pricing dimensions on the time cost actual?</span></span>

<span data-ttu-id="088a1-132">如果成功完成了检查 1 和检查 2，您现在应该只有一个适用于时间成本实际值的日期的价目表。</span><span class="sxs-lookup"><span data-stu-id="088a1-132">If you have successfully completed Check 1 and Check 2, you should now have only one price list that is applicable for the date of the time cost actual.</span></span> <span data-ttu-id="088a1-133">打开此价目表并转到“角色价格”选项卡。确保时间成本实际值上定价维度的网格中有行。</span><span class="sxs-lookup"><span data-stu-id="088a1-133">Open this Price List and go to the Role Prices tab. Make sure that there is a row in the grid for the pricing dimensions on the time cost actual.</span></span>

<span data-ttu-id="088a1-134">如果时间成本实际值中的定价维度的角色价格网格中没有行，则说明您忽略了此问题。</span><span class="sxs-lookup"><span data-stu-id="088a1-134">If there is no row in the role price grid for the pricing dimensions on the time cost actual, then you have isolated the problem.</span></span> <span data-ttu-id="088a1-135">在时间成本实际值中定价维度的“角色价格”网格中创建行。</span><span class="sxs-lookup"><span data-stu-id="088a1-135">Create a row in the Role prices grid for the pricing dimensions on your time cost actual.</span></span> <span data-ttu-id="088a1-136">完成后，重新创建时间条目，批准它，然后确认时间成本实际值显示有效的价格。</span><span class="sxs-lookup"><span data-stu-id="088a1-136">Once this is done, recreate time entry, approve it, and verify that the time cost actual shows a valid price.</span></span>
 
<span data-ttu-id="088a1-137">如果在完成上述三项检查后您仍然无法在时间成本实际值中看到有效价格，请提交支持票证。</span><span class="sxs-lookup"><span data-stu-id="088a1-137">If you still don't see a valid price on your time cost actual after you’ve done the three checks above, please log a support ticket.</span></span>



