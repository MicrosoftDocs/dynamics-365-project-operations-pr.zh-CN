---
title: 关闭定价维度
description: 此主题介绍如何关闭定价维度。
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
ms.openlocfilehash: d2e10c9ce782697fa4cbbe6eb63491ebb573a6f6
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/15/2021
ms.locfileid: "5274717"
---
# <a name="turning-off-a-pricing-dimension"></a><span data-ttu-id="b8d8d-103">关闭定价维度</span><span class="sxs-lookup"><span data-stu-id="b8d8d-103">Turning off a pricing dimension</span></span>

<span data-ttu-id="b8d8d-104">_**适用于：** 基于资源/非库存场景的 Project Operations，精简部署 - 估价开票交易_</span><span class="sxs-lookup"><span data-stu-id="b8d8d-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="b8d8d-105">您可能需要每隔数年检查和更新自己的定价策略。</span><span class="sxs-lookup"><span data-stu-id="b8d8d-105">You may need to review and update your pricing strategy every few years.</span></span> <span data-ttu-id="b8d8d-106">您进行的任何更新都可能会要求您关闭现有定价维度并创建一个新的。</span><span class="sxs-lookup"><span data-stu-id="b8d8d-106">Any updates you make might require that you turn off an existing pricing dimension and create a new one.</span></span> <span data-ttu-id="b8d8d-107">例如，您可能以前按 **角色** 定价，但现在决定按 **工作经验** 定价。</span><span class="sxs-lookup"><span data-stu-id="b8d8d-107">For example, you may have previously priced by **Role**, but now you have decided to price by **Work Experience**.</span></span> <span data-ttu-id="b8d8d-108">这可能需要您关闭充当定价维度的 **角色**，并创建 **工作经验** 充当新定价维度。</span><span class="sxs-lookup"><span data-stu-id="b8d8d-108">This may require you to turn off **Role** as a pricing dimension and create **Work Experience** as a new pricing dimension.</span></span> 

<span data-ttu-id="b8d8d-109">开通过奖定价维度的 **适用于成本** 和 **适用于销售** 字段设置为 **否** 来关闭定价维度，无论该定价维度是自带的还是自定义的。</span><span class="sxs-lookup"><span data-stu-id="b8d8d-109">Turning off a pricing dimension, regardless if it is out-of-the-box or custom, can be done by setting the **Applicable to Cost** and **Applicable to Sales** fields of the Pricing Dimension to **No**.</span></span>

<span data-ttu-id="b8d8d-110">不过，当您执行此操作时，您可能会收到错误消息 **如果有相关联的价格记录，则无法更新或删除定价维度**。</span><span class="sxs-lookup"><span data-stu-id="b8d8d-110">However, when you do this, you might receive the error message, **Pricing dimension cannot be updated or deleted if there are associated price records.**</span></span>

![关闭定价维度时可能出现的业务流程错误](media/Business-Process-Error.png)

<span data-ttu-id="b8d8d-112">此错误消息说明存在已经为正在关闭的维度设置的定价记录。</span><span class="sxs-lookup"><span data-stu-id="b8d8d-112">This error message indicates that there are price records that were previously set up for the dimension that is being turned off.</span></span> <span data-ttu-id="b8d8d-113">必须先删除引用某个维度的所有 **角色价格** 和 **角色价格加价** 记录，才能将该维度的适用性设置为 **否**。</span><span class="sxs-lookup"><span data-stu-id="b8d8d-113">All **Role Price** and **Role Price Markup** records that refer to a dimension must be deleted before the dimension’s applicability can be to set to **No**.</span></span> <span data-ttu-id="b8d8d-114">此规则同时适用于自带定价维度和您可能已创建的任何自定义定价维度。</span><span class="sxs-lookup"><span data-stu-id="b8d8d-114">This rule applies to both out-of-the-box pricing dimensions and any custom pricing dimensions that you may have created.</span></span> <span data-ttu-id="b8d8d-115">要执行此项验证的原因是每个 **角色价格** 记录都必须有唯一的维度组合。</span><span class="sxs-lookup"><span data-stu-id="b8d8d-115">The reason for this validation is because each **Role Price** record must have a unique combination of dimensions.</span></span> <span data-ttu-id="b8d8d-116">例如，在名称为 **2018 年美国成本费率** 的价目表中，有以下 **角色价格** 行。</span><span class="sxs-lookup"><span data-stu-id="b8d8d-116">For example, on a price list called **US Cost Rates 2018**, you have the following **Role price** rows.</span></span> 

| <span data-ttu-id="b8d8d-117">标准标题</span><span class="sxs-lookup"><span data-stu-id="b8d8d-117">Standard Title</span></span>         | <span data-ttu-id="b8d8d-118">部门</span><span class="sxs-lookup"><span data-stu-id="b8d8d-118">Org Unit</span></span>    |<span data-ttu-id="b8d8d-119">单位</span><span class="sxs-lookup"><span data-stu-id="b8d8d-119">Unit</span></span>   |<span data-ttu-id="b8d8d-120">价格</span><span class="sxs-lookup"><span data-stu-id="b8d8d-120">Price</span></span>  |<span data-ttu-id="b8d8d-121">货币</span><span class="sxs-lookup"><span data-stu-id="b8d8d-121">Currency</span></span>  |
| -----------------------|-------------|-------|-------|----------|
| <span data-ttu-id="b8d8d-122">系统工程师</span><span class="sxs-lookup"><span data-stu-id="b8d8d-122">Systems Engineer</span></span>|<span data-ttu-id="b8d8d-123">Contoso US</span><span class="sxs-lookup"><span data-stu-id="b8d8d-123">Contoso US</span></span>|<span data-ttu-id="b8d8d-124">Hour</span><span class="sxs-lookup"><span data-stu-id="b8d8d-124">Hour</span></span>| <span data-ttu-id="b8d8d-125">100</span><span class="sxs-lookup"><span data-stu-id="b8d8d-125">100</span></span>|<span data-ttu-id="b8d8d-126">USD</span><span class="sxs-lookup"><span data-stu-id="b8d8d-126">USD</span></span>|
| <span data-ttu-id="b8d8d-127">高级系统工程师</span><span class="sxs-lookup"><span data-stu-id="b8d8d-127">Senior Systems Engineer</span></span>|<span data-ttu-id="b8d8d-128">Contoso US</span><span class="sxs-lookup"><span data-stu-id="b8d8d-128">Contoso US</span></span>|<span data-ttu-id="b8d8d-129">Hour</span><span class="sxs-lookup"><span data-stu-id="b8d8d-129">Hour</span></span>| <span data-ttu-id="b8d8d-130">150</span><span class="sxs-lookup"><span data-stu-id="b8d8d-130">150</span></span>| <span data-ttu-id="b8d8d-131">USD</span><span class="sxs-lookup"><span data-stu-id="b8d8d-131">USD</span></span>|


<span data-ttu-id="b8d8d-132">关闭充当定价维度的 **标准标题**，并且定价引擎搜索价格时，将仅使用输入上下文中的 **部门** 值。</span><span class="sxs-lookup"><span data-stu-id="b8d8d-132">When you turn off **Standard Title** as the pricing dimension, and the pricing engine searches for a price, it will only use the **Org Unit** value from the input context.</span></span> <span data-ttu-id="b8d8d-133">如果输入上下文的 **部门** 为“Contoso US”，结果将不确定，因为两个行都将匹配。</span><span class="sxs-lookup"><span data-stu-id="b8d8d-133">If the **Org Unit** of the input context is “Contoso US”, the result will be non-deterministic because both the rows will match.</span></span> <span data-ttu-id="b8d8d-134">为了避免出现这样的情况，在您创建 **角色价格** 记录时，系统会验证维度组合是否唯一。</span><span class="sxs-lookup"><span data-stu-id="b8d8d-134">To avoid this scenario, when you create **Role Price** records, the system validates that the combination of dimensions is unique.</span></span> <span data-ttu-id="b8d8d-135">如果在创建 **角色价格** 记录后关闭了维度，可能会违反此项约束。</span><span class="sxs-lookup"><span data-stu-id="b8d8d-135">If the dimension is turned off after the **Role Price** records are created, this constraint can be violated.</span></span> <span data-ttu-id="b8d8d-136">因此，您需要在关闭维度之前删除已填充了维度值的所有 **角色价格** 和 **角色价格加价** 行。</span><span class="sxs-lookup"><span data-stu-id="b8d8d-136">Therefore, it is required that before you turn off a dimension, you delete all **Role Price** and **Role Price Markup** rows that have that dimension value populated.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]