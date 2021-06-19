---
title: 使用里程费率层级设置里程
description: 本主题提供有关里程费率和里程费率层级的信息。
author: suvaidya
ms.date: 05/20/2021
ms.topic: article
ms.reviewer: kfend
ms.author: suvaidya
ms.openlocfilehash: a44d32358a9e88824efc5452b2b5493ac8b97c7f
ms.sourcegitcommit: 18f99fbceccadd4b3e75875e1c5bcdd3e59ce206
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/20/2021
ms.locfileid: "6083660"
---
# <a name="set-up-mileage-using-mileage-rate-tiers"></a><span data-ttu-id="01b48-103">使用里程费率层级设置里程</span><span class="sxs-lookup"><span data-stu-id="01b48-103">Set up mileage using mileage rate tiers</span></span>

<span data-ttu-id="01b48-104">_**适用于：** 面向资源/非库存场景的 Project Operations_</span><span class="sxs-lookup"><span data-stu-id="01b48-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="01b48-105">当报告支出且所选支出类别为 **里程** 时，将根据 *单位费率* 金额计算该支出行的金额。</span><span class="sxs-lookup"><span data-stu-id="01b48-105">When an expense is reported and the selected expense category is **Mileage**, the amount for that expense line is calculated according to the *rate per mileage* amount.</span></span> <span data-ttu-id="01b48-106">该金额是通过使用定义的里程层级确定的，或者如果没有设置里程费率层级，则按照标准里程费率来确定。</span><span class="sxs-lookup"><span data-stu-id="01b48-106">This amount is determined by using defined mileage tiers or, if no mileage rate tiers are set up, by following a standard rate of mileage.</span></span> 

<span data-ttu-id="01b48-107">通过转到 **支出管理** > **设置** > **常规** > **支出类别** > **里程** > **类别设置**，可以设置里程费率层级。</span><span class="sxs-lookup"><span data-stu-id="01b48-107">Mileage rate tiers can be set up by going to **Expense Management** > **Setup** > **General** > **Expense categories** > **Mileage** > **Category setup**.</span></span>

<span data-ttu-id="01b48-108">升级到 10.0.18 后，如果您的组织使用里程支出类别，请考虑在查看以下设计更改后启用里程功能。</span><span class="sxs-lookup"><span data-stu-id="01b48-108">After you upgrade to 10.0.18, if your organization uses the mileage expense category, consider enabling the mileage feature after reviewing the design changes below.</span></span> 

<span data-ttu-id="01b48-109">里程费率层级的新设计会影响 **数量** 字段中的值的处理方式。</span><span class="sxs-lookup"><span data-stu-id="01b48-109">The new design of mileage rate tiers impacts how the value in the **Quantity** field is processed.</span></span> <span data-ttu-id="01b48-110">在 10.0.18 版本之前，**数量** 字段中的值被认为是下限。</span><span class="sxs-lookup"><span data-stu-id="01b48-110">Prior to the release of 10.0.18, the value in the **Quantity** field was considered to be the lower limit.</span></span> <span data-ttu-id="01b48-111">当累积超过该值时，会使用相应的费率。</span><span class="sxs-lookup"><span data-stu-id="01b48-111">When accumulation crossed that value, the corresponding rate was used.</span></span>  <span data-ttu-id="01b48-112">从 10.0.18 起，**数量** 字段中的值被视为上限。</span><span class="sxs-lookup"><span data-stu-id="01b48-112">As of 10.0.18, the value in the **Quantity** field is considered the upper limit.</span></span> <span data-ttu-id="01b48-113">当里程累积小于 **数量** 字段中的值时，会使用相应的费率。</span><span class="sxs-lookup"><span data-stu-id="01b48-113">The corresponding rate is used when mileage accumulation is less than the value in the **Quantity** field.</span></span>  <span data-ttu-id="01b48-114">里程层级的新模型有助于实现跨里程层级的一致性和更好的可用性。</span><span class="sxs-lookup"><span data-stu-id="01b48-114">The new model for mileage tiers helps with consistency across mileage tiers and better usability.</span></span>   

<span data-ttu-id="01b48-115">所有批准的支出报表将在过帐期间根据新设计重新计算。</span><span class="sxs-lookup"><span data-stu-id="01b48-115">All approved expense reports will be recalculated during posting according to the new design.</span></span>

## <a name="example"></a><span data-ttu-id="01b48-116">示例</span><span class="sxs-lookup"><span data-stu-id="01b48-116">Example</span></span>
 
### <a name="before-version-10018"></a><span data-ttu-id="01b48-117">在版本 10.0.18 之前</span><span class="sxs-lookup"><span data-stu-id="01b48-117">Before version 10.0.18</span></span>
<span data-ttu-id="01b48-118">对于两个里程费率层级，每个层级中的 **数量** 字段都表示里程下限。</span><span class="sxs-lookup"><span data-stu-id="01b48-118">With two mileage rate tiers, the **Quantity** field in each tier represents the lower mileage limit.</span></span> <span data-ttu-id="01b48-119">目前，层级一的值为零 (0)，费率为 0.45，层级二的值为 1000，费率为 0.25。</span><span class="sxs-lookup"><span data-stu-id="01b48-119">Currently, tier one has a value of zero (0) and a rate of 0.45, and tier two has a value of 1000 and a rate of 0.25.</span></span> <span data-ttu-id="01b48-120">如果累计里程数或公里数超过字段中的值，则使用相关费率。</span><span class="sxs-lookup"><span data-stu-id="01b48-120">If the accumulated miles or kilometers crosses the value in the field, the related rate is used.</span></span> <span data-ttu-id="01b48-121">如果没有零数量行，系统将使用支出管理中定义的里程费率。</span><span class="sxs-lookup"><span data-stu-id="01b48-121">If there's no line with zero quantity, the system uses the rate of mileage that is defined in Expense management.</span></span> 
 
<span data-ttu-id="01b48-122">如果员工提交的支出报表包含 1,500 英里，则已过帐支出报表上的两条里程行将是：1000（费率 0.45）+ 500（费率 0.25）= 575.00。</span><span class="sxs-lookup"><span data-stu-id="01b48-122">If an employee submits an expense report with 1,500 miles, the two mileage lines on the posted expense report would be: 1000 (rate 0.45) +  500 (rate 0.25) = 575.00.</span></span>

### <a name="after-version-10018"></a><span data-ttu-id="01b48-123">在版本 10.0.18 之后</span><span class="sxs-lookup"><span data-stu-id="01b48-123">After version 10.0.18</span></span>
<span data-ttu-id="01b48-124">在 10.0.18 中，每个层级中的 **数量** 字段都表示该层级的上限。</span><span class="sxs-lookup"><span data-stu-id="01b48-124">In 10.0.18, the **Quantity** field in each tier represents the upper limit of the tier.</span></span> <span data-ttu-id="01b48-125">目前，层级一的值为 999，费率为 0.45，层级二的值为 999,999,999.00，费率为 0.25。</span><span class="sxs-lookup"><span data-stu-id="01b48-125">Currently, tier one has a value of 999 and a rate of 0.45, and tier two has a value of 999,999,999.00 and a rate of 0.25.</span></span> <span data-ttu-id="01b48-126">如果累计里程数或公里数超过 **数量** 字段中的值，则使用相关费率。</span><span class="sxs-lookup"><span data-stu-id="01b48-126">If the accumulated miles or kilometers crosses the value in the **Quantity** field, the related rate is used.</span></span> <span data-ttu-id="01b48-127">如果超出所有上限，则系统将使用支出管理中定义的里程费率。</span><span class="sxs-lookup"><span data-stu-id="01b48-127">If all upper limits are exceeded, the system uses the rate of mileage that is defined in Expense management.</span></span> 
 
<span data-ttu-id="01b48-128">要正确计算相同的方案，必须更改层级设置。</span><span class="sxs-lookup"><span data-stu-id="01b48-128">To correctly calculate the same scenario, the tier set up must be changed.</span></span> <span data-ttu-id="01b48-129">层级一中的 **数量** 字段的值为 999.00，层级二中的值为 999,999,999.00。</span><span class="sxs-lookup"><span data-stu-id="01b48-129">The **Quantity** field in tier one has a value of 999.00 and a value of 999,999,999.00 in tier two.</span></span> <span data-ttu-id="01b48-130">如果员工超过层级一的总英里数或公里数，系统将使用支出管理中定义的里程费率。</span><span class="sxs-lookup"><span data-stu-id="01b48-130">If an employee exceeds the total quantity of miles or kilometers in tier one, the system uses the rate of mileage that is defined in Expense management.</span></span> 
  
<span data-ttu-id="01b48-131">如果员工提交的支出报表包含 1,500 英里，则已过帐支出报表上的两条里程行将是：1000（费率 0.45）+ 500（费率 0.25）= 575</span><span class="sxs-lookup"><span data-stu-id="01b48-131">If an employee submits an expense report with 1,500 miles, the two mileage lines on the posted expense report would be: 1000 (rate 0.45) +  500 (rate 0.25) = 575</span></span>

## <a name="enable-the-mileage-amount-calculation-for-multiple-mileage-tiers-with-same-rate-feature"></a><span data-ttu-id="01b48-132">启用具有相同费率功能的多个里程层级的里程金额计算</span><span class="sxs-lookup"><span data-stu-id="01b48-132">Enable the Mileage amount calculation for multiple mileage tiers with same rate feature</span></span>

<span data-ttu-id="01b48-133"> **具有相同费率的多个里程层级的里程金额计算** 功能改进了里程费率计算。</span><span class="sxs-lookup"><span data-stu-id="01b48-133">The **Mileage amount calculation for multiple mileage tiers with same rate** feature improves mileage rate calculation.</span></span> <span data-ttu-id="01b48-134">完成以下步骤以启用此功能。</span><span class="sxs-lookup"><span data-stu-id="01b48-134">Complete the following steps to enable this feature.</span></span>

1. <span data-ttu-id="01b48-135">转到 **工作区** > **功能管理**。</span><span class="sxs-lookup"><span data-stu-id="01b48-135">Go to **Workspaces** > **Feature Management**.</span></span> 
2. <span data-ttu-id="01b48-136">在此列表中，找到并选择 **具有相同费率的多个里程层级的里程金额计算**，然后选择 **立即启用**。</span><span class="sxs-lookup"><span data-stu-id="01b48-136">In the list, locate and select **Mileage amount calculation for multiple mileage tiers with same rate**, and then select **Enable now**.</span></span>

<span data-ttu-id="01b48-137">启用该功能后，重置里程层级以正确反映 **数量** 字段的值。</span><span class="sxs-lookup"><span data-stu-id="01b48-137">After you enable the feature, reset the mileage tiers to correctly reflect the value of the **Quantity** field.</span></span> 


[!INCLUDE[footer-include](../includes/footer-banner.md)]
