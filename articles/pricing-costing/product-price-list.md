---
title: 产品价目表
description: 此主题提供有关用于项目报价单和合同的目录定价中的价目表的信息。
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.technology: ''
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
ms.openlocfilehash: 3570aeb78804e9b267caa55a27e02d6c8df9a5c6
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/28/2020
ms.locfileid: "3898160"
---
# <a name="product-price-lists"></a><span data-ttu-id="7bdaa-103">产品价目表</span><span class="sxs-lookup"><span data-stu-id="7bdaa-103">Product price lists</span></span>

<span data-ttu-id="7bdaa-104">_**适用于：** 基于资源/非库存场景的 Project Operations，精简部署 - 估价开票交易_</span><span class="sxs-lookup"><span data-stu-id="7bdaa-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="7bdaa-105">价目表和价目表明细实体支持产品目录定价。</span><span class="sxs-lookup"><span data-stu-id="7bdaa-105">Price lists and price list item entities support product catalog pricing.</span></span> <span data-ttu-id="7bdaa-106">此功能通常用于项目报价单和项目合同中基于目录的明细。</span><span class="sxs-lookup"><span data-stu-id="7bdaa-106">For the most part, this functionality is used for catalog-based lines on project quotes and project contracts.</span></span>

<span data-ttu-id="7bdaa-107">对于基于项目的明细，合同在赢单后表示交易。</span><span class="sxs-lookup"><span data-stu-id="7bdaa-107">For project-based lines, a contract represents the deal after it was won.</span></span> <span data-ttu-id="7bdaa-108">由于协商流程通常在赢单前，所以始终将附加到报价单的定价照原样复制到新价目表和附加到合同。</span><span class="sxs-lookup"><span data-stu-id="7bdaa-108">Because the process of negotiation usually precedes the win, the pricing that is attached to the quote is always copied as-is to a new price list and attached to the contract.</span></span> <span data-ttu-id="7bdaa-109">新价目表的更改不能超出合同的范围。</span><span class="sxs-lookup"><span data-stu-id="7bdaa-109">This new price list can't be changed outside the scope of the contract.</span></span> <span data-ttu-id="7bdaa-110">此项限制有助于保护从基础价目表中进行的任何价格更改协商而来的费率卡。</span><span class="sxs-lookup"><span data-stu-id="7bdaa-110">This limitation helps protect the rate card that was negotiated from any price changes that occur in the master price list.</span></span>

<span data-ttu-id="7bdaa-111">应该设置产品，以使其在产品目录中具有默认成本和价目表。</span><span class="sxs-lookup"><span data-stu-id="7bdaa-111">Products should be set up so that they have default cost and price lists in the product catalog.</span></span> <span data-ttu-id="7bdaa-112">使用价目表、标准成本和当前成本来配置默认成本和价目表。</span><span class="sxs-lookup"><span data-stu-id="7bdaa-112">Use the list price, standard cost, and current cost to configure default cost and list prices.</span></span> <span data-ttu-id="7bdaa-113">仅当系统在报价单或项目合同的产品价目表中找不到该产品的价目表明细时，才为报价单明细或项目合同子项使用默认价目表。</span><span class="sxs-lookup"><span data-stu-id="7bdaa-113">The default list prices are used on a quote line or a project contract line only when the system can't find a price list line for that product in the product price list for the quote or project contract.</span></span>

<span data-ttu-id="7bdaa-114">报价单之间可以更改产品目录明细的价目表。</span><span class="sxs-lookup"><span data-stu-id="7bdaa-114">The cost price of product catalog lines can be changed between quotes.</span></span> <span data-ttu-id="7bdaa-115">这种功能非常重要，因为如果不能准确跟踪成本，则不能确定项目协定的运营利润。</span><span class="sxs-lookup"><span data-stu-id="7bdaa-115">This capability is important, because if you don't accurately track costs, you can't determine operational profits on project engagements.</span></span> <span data-ttu-id="7bdaa-116">默认情况下，产品的标准成本用作成本费。</span><span class="sxs-lookup"><span data-stu-id="7bdaa-116">By default, the standard cost of the product is used as the cost price.</span></span> <span data-ttu-id="7bdaa-117">但是，如果该报价单有其他成本费，则可以更新报价单明细中的默认成本费。</span><span class="sxs-lookup"><span data-stu-id="7bdaa-117">However, the default cost price can be updated on the quote line if there's a different cost price for that quote.</span></span>

## <a name="price-list-items"></a><span data-ttu-id="7bdaa-118">价目表项</span><span class="sxs-lookup"><span data-stu-id="7bdaa-118">Price list items</span></span>

<span data-ttu-id="7bdaa-119">可将产品目录中的产品添加到不同价目表中。</span><span class="sxs-lookup"><span data-stu-id="7bdaa-119">You can add products from a product catalog to different price lists.</span></span> <span data-ttu-id="7bdaa-120">产品的价目表明细始终引用特定单位。</span><span class="sxs-lookup"><span data-stu-id="7bdaa-120">Price list lines for products always reference a specific unit.</span></span> <span data-ttu-id="7bdaa-121">可以将价目表项中的产品的定价配置为货币金额。</span><span class="sxs-lookup"><span data-stu-id="7bdaa-121">Pricing for a product on price list items can be configured as a currency amount.</span></span> <span data-ttu-id="7bdaa-122">也可以将其配置为定价、当前成本或标准成本的函数。</span><span class="sxs-lookup"><span data-stu-id="7bdaa-122">Alternatively, it can be configured as a function of the list price, current cost, or standard cost.</span></span>

<span data-ttu-id="7bdaa-123">PSA 支持在将价格配置为定价、标准成本或当前成本时使用各种舍入选项。</span><span class="sxs-lookup"><span data-stu-id="7bdaa-123">PSA supports various rounding options when prices are configured as a function of the list price, standard cost, or current cost.</span></span> <span data-ttu-id="7bdaa-124">除了利用多种定价方法和舍入选项，还可以将折扣表与价目表项关联。</span><span class="sxs-lookup"><span data-stu-id="7bdaa-124">In addition to taking advantage of multiple pricing methods and rounding options, you can associate discount lists with price list items.</span></span> 

<span data-ttu-id="7bdaa-125">通过选择**项目报价单**页中的**创建自定义报价**为报价单创建新的自定义价目表时，将创建该价目表的备份，并将新价目表标头中的**实体**字段设置为**销售实体**。</span><span class="sxs-lookup"><span data-stu-id="7bdaa-125">When you create a new custom price list for a quote by selecting **Create Custom Pricing** on the **Project Quote** page, a copy of the price list is made, and the **Entity** field on the header of the new price list is set to **Sales Entity**.</span></span> <span data-ttu-id="7bdaa-126">将为新价目表的名称追加报价单名称和时间戳。</span><span class="sxs-lookup"><span data-stu-id="7bdaa-126">The name of the new price list is appended with the name of the quote and a timestamp.</span></span> <span data-ttu-id="7bdaa-127">也可以在自定义工作流中使用新价目表的名称和报价单的名称对使用自定义定价的报价单触发额外审阅和审批。</span><span class="sxs-lookup"><span data-stu-id="7bdaa-127">You also can use the name of the new price list and the name of the quote in custom workflows to trigger additional review and approvals for quotes that use custom pricing.</span></span>

 
## <a name="default-product-price-list"></a><span data-ttu-id="7bdaa-128">默认产品价目表</span><span class="sxs-lookup"><span data-stu-id="7bdaa-128">Default product price list</span></span>
<span data-ttu-id="7bdaa-129">每个客户记录都有一个**默认价目表**字段，可在其中指定与客户的货币匹配的价目表。</span><span class="sxs-lookup"><span data-stu-id="7bdaa-129">Each customer record has a **Default Price List** field, where you can specify a price list that matches the currency of the customer.</span></span> <span data-ttu-id="7bdaa-130">不会在此字段中自动输入默认值。</span><span class="sxs-lookup"><span data-stu-id="7bdaa-130">A default value isn't automatically entered in this field.</span></span> <span data-ttu-id="7bdaa-131">如果有与特定客户达成的自定义定价协议，可使用此字段为该客户关联价目表。</span><span class="sxs-lookup"><span data-stu-id="7bdaa-131">When a custom pricing agreement with a specific customer exists, you can use this field to associate a price list with that customer.</span></span>

<span data-ttu-id="7bdaa-132">商机、报价单和项目合同实体按照以下顺序输入默认产品价目表。</span><span class="sxs-lookup"><span data-stu-id="7bdaa-132">The Opportunity, Quote, and Project Contract entities use the following order to enter default product price lists.</span></span> <span data-ttu-id="7bdaa-133">项目价目表也采用相同的顺序。</span><span class="sxs-lookup"><span data-stu-id="7bdaa-133">The same order is used for project price lists.</span></span>

1.  <span data-ttu-id="7bdaa-134">报价单</span><span class="sxs-lookup"><span data-stu-id="7bdaa-134">Quote</span></span>
2.  <span data-ttu-id="7bdaa-135">商机​​</span><span class="sxs-lookup"><span data-stu-id="7bdaa-135">Opportunity</span></span>
3.  <span data-ttu-id="7bdaa-136">客户</span><span class="sxs-lookup"><span data-stu-id="7bdaa-136">Customer</span></span>
4.  <span data-ttu-id="7bdaa-137">全局设置</span><span class="sxs-lookup"><span data-stu-id="7bdaa-137">Global settings</span></span> 

<span data-ttu-id="7bdaa-138">默认情况下，报价单明细中的**产品**字段列出报价单的产品价目表中的所有可用产品。</span><span class="sxs-lookup"><span data-stu-id="7bdaa-138">By default, the **Product** field on the quote line lists all the active products in the product price list of the quote.</span></span> <span data-ttu-id="7bdaa-139">如果已停用某个产品，或者该产品是草稿产品，则不列出该产品，即使价目表中有此产品。</span><span class="sxs-lookup"><span data-stu-id="7bdaa-139">If a product has been inactivated, or if it's a draft product, it isn't listed, even if it's in the price list.</span></span> 

<span data-ttu-id="7bdaa-140">产品目录明细作为发票明细添加到为项目合同创建的第一份发票中。</span><span class="sxs-lookup"><span data-stu-id="7bdaa-140">Product catalog lines are added as invoice lines on the first invoice that is created for a project contract.</span></span> <span data-ttu-id="7bdaa-141">在草稿发票中，可以删除这些发票明细。</span><span class="sxs-lookup"><span data-stu-id="7bdaa-141">On a draft invoice, those invoice lines can be deleted.</span></span> <span data-ttu-id="7bdaa-142">在此情况下想，这些发票将在后续发票中出现，直到为其开票或将发票发给客户。</span><span class="sxs-lookup"><span data-stu-id="7bdaa-142">In that case, the lines will appear on a subsequent invoice until they are invoiced, or until the invoice is sent to the customer.</span></span> <span data-ttu-id="7bdaa-143">不能为产品发票明细的部分数量开票。</span><span class="sxs-lookup"><span data-stu-id="7bdaa-143">You can't invoice a partial quantity of a product invoice line.</span></span> <span data-ttu-id="7bdaa-144">为项目合同中的产品明细开票时，将创建实际值。</span><span class="sxs-lookup"><span data-stu-id="7bdaa-144">When the product lines from the project contract are invoiced, actuals are created.</span></span> <span data-ttu-id="7bdaa-145">但是，不将这些实际值链接到相关项目实体。</span><span class="sxs-lookup"><span data-stu-id="7bdaa-145">However, those actuals aren't linked to the related project entity.</span></span> <span data-ttu-id="7bdaa-146">换句话说，基于产品的项目合同明细独立于任何基于项目的使用。</span><span class="sxs-lookup"><span data-stu-id="7bdaa-146">In other words, product-based project contract lines are independent of any project-based use.</span></span> <span data-ttu-id="7bdaa-147">不跟踪项目的材料消耗。</span><span class="sxs-lookup"><span data-stu-id="7bdaa-147">Material consumption on projects isn't tracked.</span></span>
