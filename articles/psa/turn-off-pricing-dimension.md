---
title: 关闭定价维度
description: 本主题介绍如何在 Project Service 解决方案中设置定价维度。
author: Rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 11/06/2018
ms.topic: article
ms.service: business-applications
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: 6e4b80b9c4b1b0f57d04079c9d2f84051b451d29
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/15/2021
ms.locfileid: "5281827"
---
# <a name="turn-off-a-pricing-dimension"></a><span data-ttu-id="64e92-103">关闭定价维度</span><span class="sxs-lookup"><span data-stu-id="64e92-103">Turn off a pricing dimension</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="64e92-104">您可能需要每隔数年检查和更新自己的定价策略。</span><span class="sxs-lookup"><span data-stu-id="64e92-104">You may need to review and update your pricing strategy every few years.</span></span> <span data-ttu-id="64e92-105">您进行的任何更新都可能会要求您关闭现有定价维度并创建一个新的。</span><span class="sxs-lookup"><span data-stu-id="64e92-105">Any updates you make might require that you turn off an existing pricing dimension and create a new one.</span></span> <span data-ttu-id="64e92-106">例如，您可能以前按 **角色** 定价，但现在决定按 **工作经验** 定价。</span><span class="sxs-lookup"><span data-stu-id="64e92-106">For example, you may have previously priced by **Role**, but now you have decided to price by **Work Experience**.</span></span> <span data-ttu-id="64e92-107">这可能需要您关闭充当定价维度的 **角色**，并创建 **工作经验** 充当新定价维度。</span><span class="sxs-lookup"><span data-stu-id="64e92-107">This may require you to turn off **Role** as a pricing dimension and create **Work Expereince** as a new pricing dimension.</span></span> 

<span data-ttu-id="64e92-108">开通过奖定价维度的 **适用于成本** 和 **适用于销售** 字段设置为 **否** 来关闭定价维度，无论该定价维度是自带的还是自定义的。</span><span class="sxs-lookup"><span data-stu-id="64e92-108">Turning off a pricing dimension, regardless if it is out-of-the-box or custom, can be done by setting the **Applicable to Cost** and **Applicable to Sales** fields of the Pricing Dimension to **No**.</span></span>

<span data-ttu-id="64e92-109">但是，如果这样做，可能会收到以下错误消息。</span><span class="sxs-lookup"><span data-stu-id="64e92-109">However, when you do this, you might receive the following error message.</span></span>

![关闭定价维度时可能出现的业务流程错误](media/Business-Process-Error.png)


<span data-ttu-id="64e92-111">此错误消息说明存在已经为正在关闭的维度设置的定价记录。</span><span class="sxs-lookup"><span data-stu-id="64e92-111">This error message indicates that there are price records that were previously set up for the dimension that is being turned off.</span></span> <span data-ttu-id="64e92-112">必须先删除引用某个维度的所有 **角色价格** 和 **角色价格加价** 记录，才能将该维度的适用性设置为 **否**。</span><span class="sxs-lookup"><span data-stu-id="64e92-112">All **Role Price** and **Role Price Markup** records that refer to a dimension must be deleted before the dimension’s applicability can be to set to **No**.</span></span> <span data-ttu-id="64e92-113">此规则同时适用于自带定价维度和您可能已创建的任何自定义定价维度。</span><span class="sxs-lookup"><span data-stu-id="64e92-113">This rule applies to both out-of-the-box pricing dimensions and any custom pricing dimensions that you may have created.</span></span> <span data-ttu-id="64e92-114">要执行此项验证的原因是，Project Service 的一项约束要求每个 **角色价格** 记录都必须有唯一的维度组合。</span><span class="sxs-lookup"><span data-stu-id="64e92-114">The reason for this validation is because Project Service has a constraint that each **Role Price** record must have a unique combination of dimensions.</span></span> <span data-ttu-id="64e92-115">例如，在名称为 **2018 年美国成本费率** 的价目表中，有以下 **角色价格** 行。</span><span class="sxs-lookup"><span data-stu-id="64e92-115">For example, on a price list called **US Cost Rates 2018**, you have the following **Role price** rows.</span></span> 

| <span data-ttu-id="64e92-116">标准标题</span><span class="sxs-lookup"><span data-stu-id="64e92-116">Standard Title</span></span>         | <span data-ttu-id="64e92-117">部门</span><span class="sxs-lookup"><span data-stu-id="64e92-117">Org Unit</span></span>    |<span data-ttu-id="64e92-118">单位</span><span class="sxs-lookup"><span data-stu-id="64e92-118">Unit</span></span>   |<span data-ttu-id="64e92-119">价格</span><span class="sxs-lookup"><span data-stu-id="64e92-119">Price</span></span>  |<span data-ttu-id="64e92-120">货币</span><span class="sxs-lookup"><span data-stu-id="64e92-120">Currency</span></span>  |
| -----------------------|-------------|-------|-------|----------|
| <span data-ttu-id="64e92-121">系统工程师</span><span class="sxs-lookup"><span data-stu-id="64e92-121">Systems Engineer</span></span>|<span data-ttu-id="64e92-122">Contoso US</span><span class="sxs-lookup"><span data-stu-id="64e92-122">Contoso US</span></span>|<span data-ttu-id="64e92-123">Hour</span><span class="sxs-lookup"><span data-stu-id="64e92-123">Hour</span></span>| <span data-ttu-id="64e92-124">100</span><span class="sxs-lookup"><span data-stu-id="64e92-124">100</span></span>|<span data-ttu-id="64e92-125">USD</span><span class="sxs-lookup"><span data-stu-id="64e92-125">USD</span></span>|
| <span data-ttu-id="64e92-126">高级系统工程师</span><span class="sxs-lookup"><span data-stu-id="64e92-126">Senior Systems Engineer</span></span>|<span data-ttu-id="64e92-127">Contoso US</span><span class="sxs-lookup"><span data-stu-id="64e92-127">Contoso US</span></span>|<span data-ttu-id="64e92-128">Hour</span><span class="sxs-lookup"><span data-stu-id="64e92-128">Hour</span></span>| <span data-ttu-id="64e92-129">150</span><span class="sxs-lookup"><span data-stu-id="64e92-129">150</span></span>| <span data-ttu-id="64e92-130">USD</span><span class="sxs-lookup"><span data-stu-id="64e92-130">USD</span></span>|


<span data-ttu-id="64e92-131">关闭充当定价维度的 **标准标题**，并且 Project Service 定价引擎搜索价格时，将仅使用输入上下文中的 **部门** 值。</span><span class="sxs-lookup"><span data-stu-id="64e92-131">When you turn off **Standard Title** as the pricing dimension, and the Project Service pricing engine searches for a price, it will only use the **Org Unit** value from the input context.</span></span> <span data-ttu-id="64e92-132">如果输入上下文的 **部门** 为“Contoso US”，结果将不确定，因为两个行都将匹配。</span><span class="sxs-lookup"><span data-stu-id="64e92-132">If the **Org Unit** of the input context is “Contoso US”, the result will be non-deterministic because both the rows will match.</span></span> <span data-ttu-id="64e92-133">为了避免出现这样的情况，在您创建 **角色价格** 记录时，Project Service 会验证维度组合是否唯一。</span><span class="sxs-lookup"><span data-stu-id="64e92-133">To avoid this scenario, when you create **Role Price** records, Project Service validates that the combination of dimensions is unique.</span></span> <span data-ttu-id="64e92-134">如果在创建 **角色价格** 记录后关闭了维度，可能会违反此项约束。</span><span class="sxs-lookup"><span data-stu-id="64e92-134">If the dimension is turned off after the **Role Price** records are created, this constraint can be violated.</span></span> <span data-ttu-id="64e92-135">因此，您需要在关闭维度之前删除已填充了维度值的所有 **角色价格** 和 **角色价格加价** 行。</span><span class="sxs-lookup"><span data-stu-id="64e92-135">Therefore, it is required that before you turn off a dimension, you delete all **Role Price** and **Role Price Markup** rows that have that dimension value populated.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]