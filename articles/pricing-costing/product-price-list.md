---
title: 产品价目表
description: 此主题提供有关用于项目报价单和合同的目录定价中的价目表的信息。
author: rumant
ms.date: 04/05/2021
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: rumant
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 02d274725983e50adc35a4cae1ac60c35be346a4
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/10/2021
ms.locfileid: "6004925"
---
# <a name="product-price-lists"></a><span data-ttu-id="b6b7d-103">产品价目表</span><span class="sxs-lookup"><span data-stu-id="b6b7d-103">Product price lists</span></span>

<span data-ttu-id="b6b7d-104">_**适用于：** 精简部署 - 估价交易开票_</span><span class="sxs-lookup"><span data-stu-id="b6b7d-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

 <span data-ttu-id="b6b7d-105">在 Project Operations 中，**产品价目表** 和相关价目表项支持基于产品的报价单和合同子项中的产品定价功能。</span><span class="sxs-lookup"><span data-stu-id="b6b7d-105">In Project Operations, **Product price lists** and related price list item entities support functionality for pricing products on product-based quote and contract lines.</span></span> <span data-ttu-id="b6b7d-106">对于项目中使用的产品，使用了项目价目表的价目表项记录。</span><span class="sxs-lookup"><span data-stu-id="b6b7d-106">For products used on projects, the price list item records for project price lists are used.</span></span> 

<span data-ttu-id="b6b7d-107">应该设置产品，以使其在产品目录中具有默认成本和价目表。</span><span class="sxs-lookup"><span data-stu-id="b6b7d-107">Products should be set up so that they have default cost and price lists in the product catalog.</span></span> <span data-ttu-id="b6b7d-108">使用价目表、标准成本和当前成本来配置默认成本和价目表。</span><span class="sxs-lookup"><span data-stu-id="b6b7d-108">Use the list price, standard cost, and current cost to configure default cost and list prices.</span></span> <span data-ttu-id="b6b7d-109">仅当系统在报价单或项目合同的产品价目表中找不到该产品的价目表明细时，才为报价单明细或项目合同子项使用默认价目表。</span><span class="sxs-lookup"><span data-stu-id="b6b7d-109">The default list prices are used on a quote line or a project contract line only when the system can't find a price list line for that product in the product price list for the quote or project contract.</span></span>

<span data-ttu-id="b6b7d-110">报价单之间可以更改产品目录明细的价目表。</span><span class="sxs-lookup"><span data-stu-id="b6b7d-110">The cost price of product catalog lines can be changed between quotes.</span></span> <span data-ttu-id="b6b7d-111">这种功能非常重要，因为如果不能准确跟踪成本，则不能确定项目协定的运营利润。</span><span class="sxs-lookup"><span data-stu-id="b6b7d-111">This capability is important, because if you don't accurately track costs, you can't determine operational profits on project engagements.</span></span> <span data-ttu-id="b6b7d-112">默认情况下，产品的标准成本用作成本费。</span><span class="sxs-lookup"><span data-stu-id="b6b7d-112">By default, the standard cost of the product is used as the cost price.</span></span> <span data-ttu-id="b6b7d-113">但是，如果该报价单有其他成本费，则可以更新报价单明细中的默认成本费。</span><span class="sxs-lookup"><span data-stu-id="b6b7d-113">However, the default cost price can be updated on the quote line if there's a different cost price for that quote.</span></span>

## <a name="price-list-items"></a><span data-ttu-id="b6b7d-114">价目表项</span><span class="sxs-lookup"><span data-stu-id="b6b7d-114">Price list items</span></span>

<span data-ttu-id="b6b7d-115">可将产品目录中的产品添加到不同价目表中。</span><span class="sxs-lookup"><span data-stu-id="b6b7d-115">You can add products from a product catalog to different price lists.</span></span> <span data-ttu-id="b6b7d-116">产品的价目表明细始终引用特定单位。</span><span class="sxs-lookup"><span data-stu-id="b6b7d-116">Price list lines for products always reference a specific unit.</span></span> <span data-ttu-id="b6b7d-117">可以将价目表项中的产品的定价配置为货币金额。</span><span class="sxs-lookup"><span data-stu-id="b6b7d-117">Pricing for a product on price list items can be configured as a currency amount.</span></span> <span data-ttu-id="b6b7d-118">也可以将其配置为定价、当前成本或标准成本的函数。</span><span class="sxs-lookup"><span data-stu-id="b6b7d-118">Alternatively, it can be configured as a function of the list price, current cost, or standard cost.</span></span>

<span data-ttu-id="b6b7d-119">在将产品价格配置为价目表、标准成本或当前成本功能时，定价功能支持使用各种舍入选项。</span><span class="sxs-lookup"><span data-stu-id="b6b7d-119">Pricing functionality supports various rounding options when product prices are configured as a function of the list price, standard cost, or current cost.</span></span> <span data-ttu-id="b6b7d-120">除了利用多种定价方法和舍入选项，还可以将折扣表与价目表项关联。</span><span class="sxs-lookup"><span data-stu-id="b6b7d-120">In addition to taking advantage of multiple pricing methods and rounding options, you can associate discount lists with price list items.</span></span> 

 
## <a name="default-product-price-list"></a><span data-ttu-id="b6b7d-121">默认产品价目表</span><span class="sxs-lookup"><span data-stu-id="b6b7d-121">Default product price list</span></span>
<span data-ttu-id="b6b7d-122">每个客户记录都有一个 **默认价目表** 字段，可在其中指定与客户的货币匹配的价目表。</span><span class="sxs-lookup"><span data-stu-id="b6b7d-122">Each customer record has a **Default Price List** field, where you can specify a price list that matches the currency of the customer.</span></span> <span data-ttu-id="b6b7d-123">不会在此字段中自动输入默认值。</span><span class="sxs-lookup"><span data-stu-id="b6b7d-123">A default value isn't automatically entered in this field.</span></span> <span data-ttu-id="b6b7d-124">如果有与特定客户达成的自定义定价协议，可使用此字段为该客户关联价目表。</span><span class="sxs-lookup"><span data-stu-id="b6b7d-124">When a custom pricing agreement with a specific customer exists, you can use this field to associate a price list with that customer.</span></span>

<span data-ttu-id="b6b7d-125">商机、报价单和项目合同实体按照以下顺序输入默认产品价目表。</span><span class="sxs-lookup"><span data-stu-id="b6b7d-125">The Opportunity, Quote, and Project Contract entities use the following order to enter default product price lists.</span></span> <span data-ttu-id="b6b7d-126">项目价目表也采用相同的顺序。</span><span class="sxs-lookup"><span data-stu-id="b6b7d-126">The same order is used for project price lists.</span></span>

1.  <span data-ttu-id="b6b7d-127">报价单</span><span class="sxs-lookup"><span data-stu-id="b6b7d-127">Quote</span></span>
2.  <span data-ttu-id="b6b7d-128">商机​​</span><span class="sxs-lookup"><span data-stu-id="b6b7d-128">Opportunity</span></span>
3.  <span data-ttu-id="b6b7d-129">客户</span><span class="sxs-lookup"><span data-stu-id="b6b7d-129">Customer</span></span>
4.  <span data-ttu-id="b6b7d-130">全局设置</span><span class="sxs-lookup"><span data-stu-id="b6b7d-130">Global settings</span></span> 

<span data-ttu-id="b6b7d-131">默认情况下，报价单明细中的 **产品** 字段列出报价单的产品价目表中的所有可用产品。</span><span class="sxs-lookup"><span data-stu-id="b6b7d-131">By default, the **Product** field on the quote line lists all the active products in the product price list of the quote.</span></span> <span data-ttu-id="b6b7d-132">如果已停用某个产品，或者该产品是草稿产品，则不列出该产品，即使价目表中有此产品。</span><span class="sxs-lookup"><span data-stu-id="b6b7d-132">If a product has been inactivated, or if it's a draft product, it isn't listed, even if it's in the price list.</span></span> 

<span data-ttu-id="b6b7d-133">产品目录明细作为发票明细添加到为项目合同创建的第一份发票中。</span><span class="sxs-lookup"><span data-stu-id="b6b7d-133">Product catalog lines are added as invoice lines on the first invoice that is created for a project contract.</span></span> <span data-ttu-id="b6b7d-134">在草稿发票中，可以删除这些发票明细。</span><span class="sxs-lookup"><span data-stu-id="b6b7d-134">On a draft invoice, those invoice lines can be deleted.</span></span> <span data-ttu-id="b6b7d-135">在此情况下想，这些发票将在后续发票中出现，直到为其开票或将发票发给客户。</span><span class="sxs-lookup"><span data-stu-id="b6b7d-135">In that case, the lines will appear on a subsequent invoice until they are invoiced, or until the invoice is sent to the customer.</span></span> <span data-ttu-id="b6b7d-136">不能为产品发票明细的部分数量开票。</span><span class="sxs-lookup"><span data-stu-id="b6b7d-136">You can't invoice a partial quantity of a product invoice line.</span></span> <span data-ttu-id="b6b7d-137">为项目合同中的产品明细开票时，将创建实际值。</span><span class="sxs-lookup"><span data-stu-id="b6b7d-137">When the product lines from the project contract are invoiced, actuals are created.</span></span> <span data-ttu-id="b6b7d-138">但是，不将这些实际值链接到相关项目实体。</span><span class="sxs-lookup"><span data-stu-id="b6b7d-138">However, those actuals aren't linked to the related project entity.</span></span> <span data-ttu-id="b6b7d-139">换句话说，基于产品的项目合同明细独立于任何基于项目的使用。</span><span class="sxs-lookup"><span data-stu-id="b6b7d-139">In other words, product-based project contract lines are independent of any project-based use.</span></span> 


[!INCLUDE[footer-include](../includes/footer-banner.md)]
