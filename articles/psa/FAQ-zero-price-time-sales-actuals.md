---
title: 为什么价格在时间销售额实际值中默认为零？
description: 为什么价格在时间销售额实际值中默认为 0 疑难解答。
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
ms.openlocfilehash: c886c4a53b4ba47e381b891fe22a565ad8fd1ac6
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/16/2020
ms.locfileid: "4072728"
---
# <a name="why-is-price-defaulting-to-zero-on-time-sales-actuals"></a><span data-ttu-id="e3916-103">为什么价格在时间销售额实际值中默认为零？</span><span class="sxs-lookup"><span data-stu-id="e3916-103">Why is price defaulting to zero on time sales actuals?</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="e3916-104">此常见问题适用于交易记录类设置为“时间”且交易记录类型为“未记帐销售额”的实际值。</span><span class="sxs-lookup"><span data-stu-id="e3916-104">This FAQ applies to actuals where the transaction class is set to Time and transaction type is Unbilled Sales.</span></span> <span data-ttu-id="e3916-105">以下三项检查有助于您解答时间销售额实际值中的价格（帐单费率）为何默认为 0。</span><span class="sxs-lookup"><span data-stu-id="e3916-105">The following three checks will help you troubleshoot why price (bill rate) is defaulting to 0 on time sales actuals.</span></span>

## <a name="check-1-identify-the-sales-price-list-for-the-project"></a><span data-ttu-id="e3916-106">检查 1：确定项目的销售价目表</span><span class="sxs-lookup"><span data-stu-id="e3916-106">Check 1: Identify the sales price list for the project</span></span>

<span data-ttu-id="e3916-107">从项目的实际值字段查找项目并转至项目页面。</span><span class="sxs-lookup"><span data-stu-id="e3916-107">Find the project from the project field of the actual and go to the project page.</span></span> <span data-ttu-id="e3916-108">然后转到“销售”选项卡，在“项目合同子项”网格上，单击“项目合同”字段中的链接。</span><span class="sxs-lookup"><span data-stu-id="e3916-108">Then go to the Sales tab and on Project Contract lines grid, click on the link in the Project Contract field.</span></span> <span data-ttu-id="e3916-109">“项目合同”页面将打开。</span><span class="sxs-lookup"><span data-stu-id="e3916-109">The project Contract page will open.</span></span> <span data-ttu-id="e3916-110">在“项目合同”页面，转到“项目价目表”选项卡。检查此处是否至少附加了一个价目表。</span><span class="sxs-lookup"><span data-stu-id="e3916-110">On the Project Contract page, go to the Project Price Lists tab. Check if there is at least one price list attached here.</span></span> <span data-ttu-id="e3916-111">如果“项目合同”的“项目价目表”网格中没有附加的价目表，说明您忽略了此问题。</span><span class="sxs-lookup"><span data-stu-id="e3916-111">If there is no price list attached in the Project Price Lists grid of the Project Contract you have isolated the problem.</span></span> <span data-ttu-id="e3916-112">将价目表附加到“项目价目表”网格。</span><span class="sxs-lookup"><span data-stu-id="e3916-112">Attach a price list to the Project Price lists grid.</span></span> <span data-ttu-id="e3916-113">允许在此处附加的价目表应将上下文字段设置为“销售”，且价目表中的货币字段与“项目合同”上的货币字段匹配。</span><span class="sxs-lookup"><span data-stu-id="e3916-113">The price lists allowed to be attached here should have the context field set to Sales and the currency field on the price list should match the currency field on the Project Contract.</span></span> <span data-ttu-id="e3916-114">在您进行必要的修改后，重新创建一个时间条目，批准它，然后确认未记帐的销售额实际值显示有效的价格。</span><span class="sxs-lookup"><span data-stu-id="e3916-114">Once you’ve done made the required fixes, recreate a time entry, approve it, and verify that the unbilled sales actual shows a valid price.</span></span> 

<span data-ttu-id="e3916-115">如果“项目合同”的“项目价目表”网格中有一个或多个附加的价目表，请继续本文中的下一项检查。</span><span class="sxs-lookup"><span data-stu-id="e3916-115">If you have one or more price lists attached in the Project Price Lists grid of the Project Contract, proceed to the next check in the document.</span></span>

## <a name="check-2-are-any-of-the-price-lists-identified-above-valid-for-the-specific-date-of-the-time-sales-actual"></a><span data-ttu-id="e3916-116">检查 2：上方确定的任何价目表是否对时间销售额实际值的特定日期有效？</span><span class="sxs-lookup"><span data-stu-id="e3916-116">Check 2: Are any of the price lists identified above valid for the specific date of the time sales actual?</span></span>

<span data-ttu-id="e3916-117">为了 Project Service 能够在确定默认价格时考虑价目表，该价目表应适用于时间销售额实际值中的日期。</span><span class="sxs-lookup"><span data-stu-id="e3916-117">For Project Service to consider a price list for defaulting price, that price list should be applicable for the date on the time sales actual.</span></span> <span data-ttu-id="e3916-118">请检查以下内容查看上面确定的价目表是否适用：</span><span class="sxs-lookup"><span data-stu-id="e3916-118">Check the following to see if the price list(s) identified above are applicable:</span></span>
- <span data-ttu-id="e3916-119">检查附加的价目表的常规选项卡上的开始日期和结束日期是否不是空的。</span><span class="sxs-lookup"><span data-stu-id="e3916-119">Check if the start and end dates on the general tab for the price lists attached aren’t empty.</span></span> <span data-ttu-id="e3916-120">如果上面确定的价目表上的开始日期和结束日期是空的，说明您忽略了此问题。</span><span class="sxs-lookup"><span data-stu-id="e3916-120">If the start and end dates on price lists identified above are empty, you have isolated the problem.</span></span> 
- <span data-ttu-id="e3916-121">记下时间销售额实际值中的开始日期字段，检查确定的任何价目表是否适用于该日期。</span><span class="sxs-lookup"><span data-stu-id="e3916-121">Make a note of the start date field on your time sales actual and check if any of the price lists identified is applicable for that date.</span></span> <span data-ttu-id="e3916-122">例如，时间销售额实际值的日期应在价目表上的开始日期和结束日期之间。</span><span class="sxs-lookup"><span data-stu-id="e3916-122">For example, the date of the time sales actual should fall within the start date and end date on the price list.</span></span> 
    - <span data-ttu-id="e3916-123">如果没有覆盖时间销售额实际值上该日期的价目表，说明您忽略了此问题。</span><span class="sxs-lookup"><span data-stu-id="e3916-123">If there is no price list that covers that date on the time sales actual, you have isolated the problem.</span></span> <span data-ttu-id="e3916-124">修改价目表的开始日期和结束日期以确保价目表覆盖时间销售额实际值的日期。</span><span class="sxs-lookup"><span data-stu-id="e3916-124">Modify the start and end dates of the price list to ensure that the price list covers the date of the time sales actual.</span></span> 
    - <span data-ttu-id="e3916-125">如果有多个覆盖时间销售额实际值上该日期的价目表，说明您忽略了此问题。</span><span class="sxs-lookup"><span data-stu-id="e3916-125">If there is more than one price list that covers the date on the time sales actual, you have isolated the problem.</span></span> <span data-ttu-id="e3916-126">您可以解决此问题，方法是编辑价目表的开始日期和结束日期，以只有一个价目表覆盖时间销售额实际值的日期。</span><span class="sxs-lookup"><span data-stu-id="e3916-126">You can fix this by editing the start and end dates of the price list(s) so that there is only one price list that covers the date of the time sales actual.</span></span> 
    - <span data-ttu-id="e3916-127">如果只有一个价目表覆盖时间销售额实际值的日期，转到检查 3。</span><span class="sxs-lookup"><span data-stu-id="e3916-127">If there is only one price list that covers that date of the time sales actual, go to Check 3.</span></span>
<span data-ttu-id="e3916-128">在您进行必要的修改后，重新创建一个时间条目，批准它，然后确认时间销售额实际值显示有效的价格。</span><span class="sxs-lookup"><span data-stu-id="e3916-128">Once you’ve done made the required fixes, recreate a time entry, approve it, and verify that the time sales actual shows a valid price.</span></span>

## <a name="check-3-is-there-a-price-in-the-price-list-for-the-pricing-dimensions-on-the-time-sales-actual"></a><span data-ttu-id="e3916-129">检查 3：价目表中是否有价格用于时间销售额实际值中的定价维度？</span><span class="sxs-lookup"><span data-stu-id="e3916-129">Check 3: Is there a price in the price list for the pricing dimensions on the time sales actual?</span></span>

<span data-ttu-id="e3916-130">如果成功完成了检查 1 和检查 2，您现在应该只有一个适用于时间销售额实际值的日期的价目表。</span><span class="sxs-lookup"><span data-stu-id="e3916-130">If you have successfully completed Check 1 and Check 2, you should now have only one price list that is applicable for the date of the time sales actual.</span></span> <span data-ttu-id="e3916-131">打开此价目表并导航到“角色价格”选项卡。确保时间销售额实际值上定价维度的网格中有行。</span><span class="sxs-lookup"><span data-stu-id="e3916-131">Open this Price List and navigate to the Role Prices tab. Make sure that there is a row in the grid for the pricing dimensions on the Time sales actual.</span></span>

<span data-ttu-id="e3916-132">如果时间销售额实际值中的定价维度的角色价格网格中没有行，则说明您忽略了此问题。</span><span class="sxs-lookup"><span data-stu-id="e3916-132">If there is no row in the role price grid for the pricing dimensions on the time sales actual, then you have isolated the problem.</span></span> <span data-ttu-id="e3916-133">在时间销售额实际值中定价维度的“角色价格”网格中创建行。</span><span class="sxs-lookup"><span data-stu-id="e3916-133">Create a row in the Role prices grid for the pricing dimensions on your time sales actual.</span></span> <span data-ttu-id="e3916-134">完成后，重新创建时间条目，批准它，然后确认时间销售额实际值显示有效的价格。</span><span class="sxs-lookup"><span data-stu-id="e3916-134">Once this is done, recreate time entry, approve it, and verify that the time sales actual shows a valid price.</span></span>

<span data-ttu-id="e3916-135">如果在完成上述三项检查后您仍然无法在时间销售额实际值中看到有效价格，请提交支持票证。</span><span class="sxs-lookup"><span data-stu-id="e3916-135">If you still don't see a valid price on your time sales actual after following the three checks above, please log a support ticket.</span></span> 

