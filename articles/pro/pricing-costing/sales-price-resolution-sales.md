---
title: 处理估算和实际值的售价
description: 此主题提供有关解析估计值和实际值中的售价的信息。
author: rumant
manager: Annbe
ms.date: 10/19/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: c8972bd7710735e9acdbf951079f2da24a00bd7f
ms.sourcegitcommit: f8edff6422b82fdf2cea897faa6abb51e2c0c3c8
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/21/2020
ms.locfileid: "4087827"
---
# <a name="resolving-sales-prices-for-estimates-and-actuals"></a><span data-ttu-id="eab2d-103">处理估算和实际值的售价</span><span class="sxs-lookup"><span data-stu-id="eab2d-103">Resolving sales prices for estimates and actuals</span></span>

<span data-ttu-id="eab2d-104">_**适用于：** 精简部署 - 估价交易开票_</span><span class="sxs-lookup"><span data-stu-id="eab2d-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="eab2d-105">当在 Dynamics 365 Project Operations 中解析估计值和实际值中的售价时，系统首先使用相关项目报价单或合同的日期和货币来解析销售价目表。</span><span class="sxs-lookup"><span data-stu-id="eab2d-105">When sales prices on estimates and actuals are resolved in Dynamics 365 Project Operations, the system first uses the date and currency of the related project quote or contract to resolve the sales price list.</span></span> <span data-ttu-id="eab2d-106">解析销售价目表后，系统将解析销售或记帐费率。</span><span class="sxs-lookup"><span data-stu-id="eab2d-106">After the sales price list is resolved, the system resolves the sales or bill rate.</span></span>

## <a name="resolve-sales-rates-on-actual-and-estimate-lines-for-time"></a><span data-ttu-id="eab2d-107">解析时间的实际值和估计值明细中的销售费率</span><span class="sxs-lookup"><span data-stu-id="eab2d-107">Resolve sales rates on actual and estimate lines for time</span></span>

<span data-ttu-id="eab2d-108">在 Project Operations 中，时间估算明细用于表示时间的报价单明细和合同子项详细信息以及项目上的资源分配。</span><span class="sxs-lookup"><span data-stu-id="eab2d-108">In Project Operations, estimate lines for time are used to denote the quote line and contract line details for time and the resource assignments on the project.</span></span>

<span data-ttu-id="eab2d-109">解析销售价目表后，系统将完成以下步骤来设定默认记帐费率。</span><span class="sxs-lookup"><span data-stu-id="eab2d-109">After a price list for sales is resolved, the system completes the following steps to default the bill rate.</span></span>

1. <span data-ttu-id="eab2d-110">系统使用时间的估算明细中的 **角色** 和 **资源单位** 字段与解析的价目表中的角色价格明细进行匹配。</span><span class="sxs-lookup"><span data-stu-id="eab2d-110">The system uses the **Role** and **Resourcing Unit** fields on the estimate line for time, to match against the role price lines in the resolved price list.</span></span> <span data-ttu-id="eab2d-111">这一匹配假设所使用的是现成的记帐费率定价维度。</span><span class="sxs-lookup"><span data-stu-id="eab2d-111">This matching assumes that out-of-box pricing dimensions for bill rates are being used.</span></span> <span data-ttu-id="eab2d-112">如果您基于任何其他字段配置了定价，而不是基于 **角色** 和 **资源单位** 或同时也基于这两个字段，那么此字段组合将是用来检索匹配的角色价格明细的组合。</span><span class="sxs-lookup"><span data-stu-id="eab2d-112">If you have configured pricing based on any other fields instead of, or in addition to **Role** and **Resourcing Unit** , then that is the combination that will be used to retrieve a matching role price line.</span></span>
2. <span data-ttu-id="eab2d-113">如果系统发现具有 **角色** 和 **资源单位** 字段组合的记帐费率的角色价格明细，该记帐费率将为默认值。</span><span class="sxs-lookup"><span data-stu-id="eab2d-113">If the system finds a role price line that has a bill rate for the **Role** and **Resourcing Unit** field combination, then that bill rate is defaulted.</span></span>
3. <span data-ttu-id="eab2d-114">如果系统无法匹配 **角色** 和 **资源单位** 字段值，它将检索具有匹配角色的角色价格明细，但 **资源单位** 为 null 值。</span><span class="sxs-lookup"><span data-stu-id="eab2d-114">If the system is unable to match the **Role** and **Resourcing Unit** field values, then it retrieves role price lines with a matching role but null values of **Resource Unit**.</span></span> <span data-ttu-id="eab2d-115">在系统找到匹配的角色价格记录后，它会将该记录中的记帐费率设为默认值。</span><span class="sxs-lookup"><span data-stu-id="eab2d-115">After the system finds a matching role price record, it will default the bill rate from that record.</span></span> <span data-ttu-id="eab2d-116">此匹配假设将 **角色** 与 **资源单位** 的相对优先级的现成配置作为销售定价维度。</span><span class="sxs-lookup"><span data-stu-id="eab2d-116">This matching assumes an out-of-the-box configuration for the relative priority of **Role** vs **Resourcing Unit** as a sales pricing dimension.</span></span>

> [!NOTE]
> <span data-ttu-id="eab2d-117">如果您配置了不同的 **角色** 和 **资源单位** 优先级，或者您有优先级更高的其他维度，此行为将相应变更。</span><span class="sxs-lookup"><span data-stu-id="eab2d-117">If you configured a different prioritization of **Role** and **Resourcing Unit** , or if you have other dimensions that have higher priority, this behavior will change accordingly.</span></span> <span data-ttu-id="eab2d-118">系统将按优先级顺序使用每个定价维度的匹配值检索角色价格记录，这些维度为 null 值的行排在最后。</span><span class="sxs-lookup"><span data-stu-id="eab2d-118">The system retrieves the role price records with matching values of each of the pricing dimension values in the order of priority with rows that have null values for those dimensions coming last.</span></span>

## <a name="resolve-sales-rates-on-actual-and-estimate-lines-for-expense"></a><span data-ttu-id="eab2d-119">解析支出的实际值和估计值明细中的销售费率</span><span class="sxs-lookup"><span data-stu-id="eab2d-119">Resolve sales rates on actual and estimate lines for expense</span></span>

<span data-ttu-id="eab2d-120">在 Project Operations 中，支出估算明细用于表示支出的报价单明细和合同子项详细信息以及项目上的支出估算明细。</span><span class="sxs-lookup"><span data-stu-id="eab2d-120">In Project Operations, estimate lines for expense are used to denote the quote line and contract line details for expenses and the expense estimate lines on the project.</span></span>

<span data-ttu-id="eab2d-121">解析销售价目表后，系统将完成以下步骤来设定默认销售单价。</span><span class="sxs-lookup"><span data-stu-id="eab2d-121">After a price list for sales is resolved, the system completes the following steps to default the unit sales price.</span></span>

1. <span data-ttu-id="eab2d-122">系统使用支出的估计值明细中的 **类别** 和 **单位** 字段组合与解析的价目表中的类别价格明细进行匹配。</span><span class="sxs-lookup"><span data-stu-id="eab2d-122">The system uses the **Category** and **Unit** field combination on the estimate line for expense to match against the category price lines in the price list that was resolved.</span></span>
2. <span data-ttu-id="eab2d-123">如果系统发现具有 **类别** 和 **单位** 字段组合的销售费率的类别价格明细，该销售费率将为默认值。</span><span class="sxs-lookup"><span data-stu-id="eab2d-123">If the system finds a category price line that has a sales rate for the **Category** and **Unit** field combination, then that sales rate is defaulted.</span></span>
3. <span data-ttu-id="eab2d-124">如果系统找到匹配的类别价格明细，此定价方式可能用于设定默认售价。</span><span class="sxs-lookup"><span data-stu-id="eab2d-124">If the system finds a matching category price line, the pricing method may be used to default the sales price.</span></span> <span data-ttu-id="eab2d-125">下表显示了 Project Operations 中的设定默认支出价格行为。</span><span class="sxs-lookup"><span data-stu-id="eab2d-125">The following table below shows the expense price defaulting behavior in Project Operations.</span></span>

    | <span data-ttu-id="eab2d-126">背景</span><span class="sxs-lookup"><span data-stu-id="eab2d-126">Context</span></span> | <span data-ttu-id="eab2d-127">定价方式</span><span class="sxs-lookup"><span data-stu-id="eab2d-127">Pricing method</span></span> | <span data-ttu-id="eab2d-128">已设定默认价格</span><span class="sxs-lookup"><span data-stu-id="eab2d-128">Price defaulted</span></span> |
    | --- | --- | --- |
    | <span data-ttu-id="eab2d-129">估计</span><span class="sxs-lookup"><span data-stu-id="eab2d-129">Estimate</span></span> | <span data-ttu-id="eab2d-130">单价</span><span class="sxs-lookup"><span data-stu-id="eab2d-130">Price per unit</span></span> | <span data-ttu-id="eab2d-131">基于类别价格明细</span><span class="sxs-lookup"><span data-stu-id="eab2d-131">Based on the category price line</span></span> |
    | &nbsp; | <span data-ttu-id="eab2d-132">按成本</span><span class="sxs-lookup"><span data-stu-id="eab2d-132">At cost</span></span> | <span data-ttu-id="eab2d-133">0.00</span><span class="sxs-lookup"><span data-stu-id="eab2d-133">0.00</span></span> |
    | &nbsp; | <span data-ttu-id="eab2d-134">成本加价</span><span class="sxs-lookup"><span data-stu-id="eab2d-134">Markup over cost</span></span> | <span data-ttu-id="eab2d-135">0.00</span><span class="sxs-lookup"><span data-stu-id="eab2d-135">0.00</span></span> |
    | <span data-ttu-id="eab2d-136">实际</span><span class="sxs-lookup"><span data-stu-id="eab2d-136">Actual</span></span> | <span data-ttu-id="eab2d-137">单价</span><span class="sxs-lookup"><span data-stu-id="eab2d-137">Price per unit</span></span> | <span data-ttu-id="eab2d-138">基于类别价格明细</span><span class="sxs-lookup"><span data-stu-id="eab2d-138">Based on the category price line</span></span> |
    | &nbsp; | <span data-ttu-id="eab2d-139">按成本</span><span class="sxs-lookup"><span data-stu-id="eab2d-139">At cost</span></span> | <span data-ttu-id="eab2d-140">基于相关成本实际值</span><span class="sxs-lookup"><span data-stu-id="eab2d-140">Based on the related cost actual</span></span> |
    | &nbsp; | <span data-ttu-id="eab2d-141">成本加价</span><span class="sxs-lookup"><span data-stu-id="eab2d-141">Markup over cost</span></span> | <span data-ttu-id="eab2d-142">在相关成本实际值的单位成本费率中应用类别价格明细定义的加价</span><span class="sxs-lookup"><span data-stu-id="eab2d-142">Apply a markup as defined by the category price line on the unit cost rate of the related cost actual</span></span> |

4. <span data-ttu-id="eab2d-143">如果系统无法匹配 **类别** 和 **单位** 字段值，销售费率将默认为零 (0)。</span><span class="sxs-lookup"><span data-stu-id="eab2d-143">If the system is unable to match the **Category** and **Unit** field values, the sales rate defaults to zero(0).</span></span>
