---
title: 为什么价格在支出销售额实际值中默认为零？
description: 以下三项检查有助于您解答支出销售额实际值中的价格为何默认为 0。
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
ms.openlocfilehash: 5840bda4f74c720bfcdc7f4e84c8f22e0c6163ec
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/16/2020
ms.locfileid: "4072624"
---
# <a name="why-is-the-price-defaulting-to-zero-on-expense-sales-actuals"></a><span data-ttu-id="6ac95-103">为什么价格在支出销售额实际值中默认为零？</span><span class="sxs-lookup"><span data-stu-id="6ac95-103">Why is the price defaulting to zero on expense sales actuals?</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="6ac95-104">此常见问题适用于交易记录类设置为“支出”且交易记录类型为“未记帐销售额”的支出实际值。</span><span class="sxs-lookup"><span data-stu-id="6ac95-104">This FAQ applies to expense actuals where the transaction class is set to Expense and transaction type is Unbilled Sales.</span></span> <span data-ttu-id="6ac95-105">以下三项检查有助于您解答支出销售额实际值中的价格（帐单费率）为何默认为 0。</span><span class="sxs-lookup"><span data-stu-id="6ac95-105">The following three checks will help you troubleshoot why price (bill rate) is defaulting to 0 on expense sales actuals.</span></span>

## <a name="check-1-identify-the-sales-price-list-for-project"></a><span data-ttu-id="6ac95-106">检查 1：确定项目的销售价目表</span><span class="sxs-lookup"><span data-stu-id="6ac95-106">Check 1: Identify the sales price list for project</span></span>

<span data-ttu-id="6ac95-107">从项目的实际值字段查找项目并转至项目页面。</span><span class="sxs-lookup"><span data-stu-id="6ac95-107">Find the project from the project field of the actual and go to the project page.</span></span> <span data-ttu-id="6ac95-108">然后转到“销售”选项卡。在“项目合同子项”网格上，单击“项目合同”字段中的链接。</span><span class="sxs-lookup"><span data-stu-id="6ac95-108">Then go to the Sales tab. On the Project Contract lines grid, click on the link in the Project Contract field.</span></span> <span data-ttu-id="6ac95-109">“项目合同”页面将打开。</span><span class="sxs-lookup"><span data-stu-id="6ac95-109">The Project Contract page will open.</span></span> <span data-ttu-id="6ac95-110">在“项目合同”页面，转到“项目价目表”选项卡。检查此处是否至少附加了一个价目表。</span><span class="sxs-lookup"><span data-stu-id="6ac95-110">On the Project Contract page, go to the Project Price Lists tab. Check if there is at least one price list attached here.</span></span>

<span data-ttu-id="6ac95-111">如果“项目合同”的“项目价目表”网格中没有附加的价目表，请执行以下操作：</span><span class="sxs-lookup"><span data-stu-id="6ac95-111">If there is no price list attached in the Project Price Lists grid of the Project Contract do the following:</span></span>

- <span data-ttu-id="6ac95-112">将价目表附加到“项目价目表”网格。</span><span class="sxs-lookup"><span data-stu-id="6ac95-112">Attach a price list to the Project Price lists grid.</span></span> <span data-ttu-id="6ac95-113">允许在此处附加的价目表应将上下文字段设置为“销售”，且价目表中的货币字段与“项目合同”上的货币字段匹配。</span><span class="sxs-lookup"><span data-stu-id="6ac95-113">The price lists allowed to be attached here should have the context field set to Sales and the currency field on the price list should match the currency field on the Project Contract.</span></span> <span data-ttu-id="6ac95-114">在您进行必要的修改后，重新创建一个支出条目，批准它，然后确认未记帐的销售额实际值显示有效的价格。</span><span class="sxs-lookup"><span data-stu-id="6ac95-114">Once you’ve made the required fixes, recreate an expense entry, approve it, and verify that the unbilled sales actual shows a valid price.</span></span>
- <span data-ttu-id="6ac95-115">如果“项目合同”的“项目价目表”网格中有一个或多个附加的价目表，请转到检查 2。</span><span class="sxs-lookup"><span data-stu-id="6ac95-115">If you have one or more price lists attached in the Project Price Lists grid of the Project Contract, go to Check 2.</span></span>

## <a name="check-2-are-any-of-the-price-lists-identified-above-valid-for-the-specific-date-of-the-expense-actual"></a><span data-ttu-id="6ac95-116">检查 2：上方确定的任何价目表是否对支出实际值的特定日期有效？</span><span class="sxs-lookup"><span data-stu-id="6ac95-116">Check 2: Are any of the price lists identified above valid for the specific date of the expense actual?</span></span>

<span data-ttu-id="6ac95-117">为了 Project Service 能够在确定默认价格时考虑价目表，该价目表应适用于支出销售额实际值中的日期。</span><span class="sxs-lookup"><span data-stu-id="6ac95-117">For Project Service to consider a price list for defaulting price, that price list should be applicable for the date on the expense sales actual.</span></span> <span data-ttu-id="6ac95-118">请检查以下内容查看上面确定的价目表是否适用：</span><span class="sxs-lookup"><span data-stu-id="6ac95-118">Check the following to see if the price list(s) identified above are applicable:</span></span>

- <span data-ttu-id="6ac95-119">首先检查附加的价目表的常规选项卡上的开始日期和结束日期是否不是空的。</span><span class="sxs-lookup"><span data-stu-id="6ac95-119">Start by checking if start and end dates on the general tab for the price lists attached aren’t empty.</span></span> <span data-ttu-id="6ac95-120">如果上面确定的价目表上的开始日期和结束日期是空的，您忽略了此问题。</span><span class="sxs-lookup"><span data-stu-id="6ac95-120">If the start and end dates on the price lists identified above are empty, you have isolated the problem.</span></span> 
- <span data-ttu-id="6ac95-121">记下支出销售额实际值中的开始日期字段，检查确定的任何价目表是否适用于该日期。</span><span class="sxs-lookup"><span data-stu-id="6ac95-121">Make a note of the start date field on your expense sales actual and check if any of the price lists identified is applicable for that date.</span></span> <span data-ttu-id="6ac95-122">例如，支出实际值的日期应在价目表上的开始日期和结束日期之间。</span><span class="sxs-lookup"><span data-stu-id="6ac95-122">For example, the date of the expense actual should fall within the start date and end date on the price list.</span></span> 
    - <span data-ttu-id="6ac95-123">如果没有覆盖支出销售额实际值上该日期的价目表，说明您忽略了此问题。</span><span class="sxs-lookup"><span data-stu-id="6ac95-123">If there is no price list that covers that date on the expense sales actual, you have isolated the problem.</span></span> <span data-ttu-id="6ac95-124">修改价目表的开始日期和结束日期以确保价目表覆盖支出实际值的日期。</span><span class="sxs-lookup"><span data-stu-id="6ac95-124">Modify the start and end dates of the price list to ensure that the price list covers the date of the expense actual.</span></span> 
    - <span data-ttu-id="6ac95-125">如果有多个覆盖支出销售额实际值上该日期的价目表，说明您忽略了此问题。</span><span class="sxs-lookup"><span data-stu-id="6ac95-125">If there is more than one price list that covers the date on the expense sales actual, you have isolated the problem.</span></span> <span data-ttu-id="6ac95-126">您可以解决此问题，方法是编辑价目表的开始日期和结束日期，以只有一个价目表覆盖支出实际值的日期。</span><span class="sxs-lookup"><span data-stu-id="6ac95-126">You can fix this by editing the start and end dates of the price list(s) so that there is only one price list that covers the date of the expense actual.</span></span> 
    - <span data-ttu-id="6ac95-127">如果只有一个价目表覆盖支出实际值的日期，前往检查 3。</span><span class="sxs-lookup"><span data-stu-id="6ac95-127">If there is only one price list that covers that date of the expense actual, move to Check 3.</span></span>
<span data-ttu-id="6ac95-128">在您进行必要的修改后，重新创建一个支出条目，批准它，然后确认未记帐的销售额实际值显示有效的价格。</span><span class="sxs-lookup"><span data-stu-id="6ac95-128">Once you’ve done made the required fixes, recreate an expense entry, approve it, and verify that the unbilled sales actual shows a valid price.</span></span>

## <a name="check-3-is-there-a-valid-price-for-the-expense-category-in-the-applicable-project-price-list"></a><span data-ttu-id="6ac95-129">检查 3：适用的项目价目表中是否有支出类别的有效价格？</span><span class="sxs-lookup"><span data-stu-id="6ac95-129">Check 3: Is there a valid price for the expense category in the applicable project price list?</span></span> 

<span data-ttu-id="6ac95-130">如果成功完成了检查 1 和检查 2，您现在应该只有一个适用于支出销售额实际值的日期的项目价目表。</span><span class="sxs-lookup"><span data-stu-id="6ac95-130">If you have successfully completed Check 1 and Check 2, you should now have only one project price list that is applicable for the date of the expense sales actual.</span></span> <span data-ttu-id="6ac95-131">打开此项目价目表并转到“类别价格”选项卡。确保支出实际值上特定支出类别的网格中有行。</span><span class="sxs-lookup"><span data-stu-id="6ac95-131">Open this Project Price List and go to the Category Prices tab. Make sure that there is a row in the grid for the specific expense category on the Expense actual.</span></span>
 
- <span data-ttu-id="6ac95-132">如果没有，则说明您忽略了此问题。</span><span class="sxs-lookup"><span data-stu-id="6ac95-132">If there is no row, then you have isolated the problem.</span></span> <span data-ttu-id="6ac95-133">在支出实际值的类别的“类别价格”网格中创建行。</span><span class="sxs-lookup"><span data-stu-id="6ac95-133">Create a row in the Category price grid for the category on your expense actual.</span></span> <span data-ttu-id="6ac95-134">完成后，重新创建一个支出条目，批准它，然后确认未记帐的销售额实际值显示有效的价格。</span><span class="sxs-lookup"><span data-stu-id="6ac95-134">Once this is done, recreate an expense entry, approve it, and verify that the unbilled sales actual shows a valid price.</span></span> 
- <span data-ttu-id="6ac95-135">如果类别价格网格中有支出类别行，请检查其是否有有效价格。</span><span class="sxs-lookup"><span data-stu-id="6ac95-135">If there is a row for the expense category in the category prices grid, check if it has a valid price.</span></span>

<span data-ttu-id="6ac95-136">若要了解有效的价格是什么，请使用以下方法：</span><span class="sxs-lookup"><span data-stu-id="6ac95-136">To understand what a valid price is, use these methods:</span></span>

- <span data-ttu-id="6ac95-137">如果类别价格行上的“定价方式”字段设置为“按成本”，那么支出销售额实际值中的单位价格将默认为“支出”条目中的值。</span><span class="sxs-lookup"><span data-stu-id="6ac95-137">If the Pricing Method field on the Category price line is set to At Cost, then the unit rate on your Expense sales actual will be defaulted to the value in the Expense entry.</span></span>
- <span data-ttu-id="6ac95-138">如果类别价格行上的“定价方式”字段设置为“加价百分比”，则检查“百分比”字段是否设置为有效值。</span><span class="sxs-lookup"><span data-stu-id="6ac95-138">If the Pricing Method field on the Category price line is set to Markup Percentage, then check if the Percent field is set to a valid value.</span></span> <span data-ttu-id="6ac95-139">支出销售额实际值中的单位价格通过将此加价百分比应用到“支出”条目中的价格来确定默认值。</span><span class="sxs-lookup"><span data-stu-id="6ac95-139">The unit rate on your Expense sales actual is defaulted by applying this markup percent to the price in the Expense entry.</span></span>
- <span data-ttu-id="6ac95-140">如果类别价格行上的“定价方式”字段设置为“单价”，则检查“价格”字段是否设置为有效值。</span><span class="sxs-lookup"><span data-stu-id="6ac95-140">If the Pricing Method field on the Category price line is set to Price per Unit, then check if the Price field is set to a valid value.</span></span> <span data-ttu-id="6ac95-141">支出销售额实际值中的单位价格将默认为“价格”字段中指定的货币金额。</span><span class="sxs-lookup"><span data-stu-id="6ac95-141">The unit rate on your Expense sales actual will be defaulted to the currency amount specified in the Price field.</span></span>

<span data-ttu-id="6ac95-142">如果支出类别的价格设置无效，则说明您忽略了此问题。</span><span class="sxs-lookup"><span data-stu-id="6ac95-142">If the price setup for the expense category isn't valid, then you have isolated the problem.</span></span> <span data-ttu-id="6ac95-143">解决方法是根据上述规则编辑包含支出类别的有效价格的类别价格行。</span><span class="sxs-lookup"><span data-stu-id="6ac95-143">The solution is to edit the category price line with a valid price for the expense category in accordance with the rules above.</span></span> <span data-ttu-id="6ac95-144">完成后，重新创建一个支出条目，批准它，然后检查未记帐的销售额实际值是否获取了有效价格。</span><span class="sxs-lookup"><span data-stu-id="6ac95-144">Once you’ve done that, recreate an expense entry, approve it, and then check that the unbilled sales actual gets a valid price.</span></span>

<span data-ttu-id="6ac95-145">如果在完成上述三项检查后您仍然无法在支出销售额实际值中看到有效价格，请提交支持票证。</span><span class="sxs-lookup"><span data-stu-id="6ac95-145">If you still don't see a valid price on your expense sales actual after doing the three checks above, please log a support ticket.</span></span>


