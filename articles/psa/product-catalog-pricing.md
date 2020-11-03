---
title: 产品目录定价
description: 此主题介绍 Dynamics 365 Project Service Automation (PSA) 中的产品目录定价工作原理。
author: rumant
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/07/2019
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
ms.openlocfilehash: e6d9266cfee996b68608c99f77d1b0c053985b3d
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/16/2020
ms.locfileid: "4072635"
---
# <a name="product-catalog-pricing"></a><span data-ttu-id="b110a-103">产品目录定价</span><span class="sxs-lookup"><span data-stu-id="b110a-103">Product catalog pricing</span></span> 

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]


<span data-ttu-id="b110a-104">价目表和价目表明细实体支持产品目录定价。</span><span class="sxs-lookup"><span data-stu-id="b110a-104">Price lists and price list item entities support product catalog pricing.</span></span> <span data-ttu-id="b110a-105">此功能通常用于项目报价单和项目合同中基于目录的明细。</span><span class="sxs-lookup"><span data-stu-id="b110a-105">For the most part, this functionality is used for catalog-based lines on project quotes and project contracts.</span></span>

<span data-ttu-id="b110a-106">对于基于项目的明细，合同在赢单后表示交易。</span><span class="sxs-lookup"><span data-stu-id="b110a-106">For project-based lines, a contract represents the deal after it was won.</span></span> <span data-ttu-id="b110a-107">由于协商流程通常在赢单前，所以始终将附加到报价单的定价照原样复制到新价目表和附加到合同。</span><span class="sxs-lookup"><span data-stu-id="b110a-107">Because the process of negotiation usually precedes the win, the pricing that is attached to the quote is always copied as-is to a new price list and attached to the contract.</span></span> <span data-ttu-id="b110a-108">新价目表的更改不能超出合同的范围。</span><span class="sxs-lookup"><span data-stu-id="b110a-108">This new price list can't be changed outside the scope of the contract.</span></span> <span data-ttu-id="b110a-109">此项限制有助于保护从基础价目表中进行的任何价格更改协商而来的费率卡。</span><span class="sxs-lookup"><span data-stu-id="b110a-109">This limitation helps protect the rate card that was negotiated from any price changes that occur in the master price list.</span></span>

<span data-ttu-id="b110a-110">应该设置产品，以使其在产品目录中具有默认成本和价目表。</span><span class="sxs-lookup"><span data-stu-id="b110a-110">Products should be set up so that they have default cost and price lists in the product catalog.</span></span> <span data-ttu-id="b110a-111">必须使用价目表、标准成本和当前成本来配置默认成本和价目表。</span><span class="sxs-lookup"><span data-stu-id="b110a-111">You must use the list price, standard cost, and current cost to configure default cost and list prices.</span></span> <span data-ttu-id="b110a-112">仅当系统在报价单或项目合同的产品价目表中找不到该产品的价目表明细时，才为报价单明细或项目合同子项使用默认价目表。</span><span class="sxs-lookup"><span data-stu-id="b110a-112">The default list prices are used on a quote line or a project contract line only when the system can't find a price list line for that product in the product price list for the quote or project contract.</span></span>

<span data-ttu-id="b110a-113">报价单之间可以更改产品目录明细的价目表。</span><span class="sxs-lookup"><span data-stu-id="b110a-113">The cost price of product catalog lines can be changed between quotes.</span></span> <span data-ttu-id="b110a-114">这种功能非常重要，因为如果不能准确跟踪成本，则不能确定项目协定的运营利润。</span><span class="sxs-lookup"><span data-stu-id="b110a-114">This capability is important, because if you don't accurately track costs, you can't determine operational profits on project engagements.</span></span> <span data-ttu-id="b110a-115">默认情况下，产品的标准成本用作成本费。</span><span class="sxs-lookup"><span data-stu-id="b110a-115">By default, the standard cost of the product is used as the cost price.</span></span> <span data-ttu-id="b110a-116">但是，如果该报价单有其他成本费，则可以更新报价单明细中的默认成本费。</span><span class="sxs-lookup"><span data-stu-id="b110a-116">However, the default cost price can be updated on the quote line if there's a different cost price for that quote.</span></span>

## <a name="price-list-items"></a><span data-ttu-id="b110a-117">价目表项</span><span class="sxs-lookup"><span data-stu-id="b110a-117">Price list items</span></span>

<span data-ttu-id="b110a-118">可将产品目录中的产品添加到不同价目表中。</span><span class="sxs-lookup"><span data-stu-id="b110a-118">You can add products from a product catalog to different price lists.</span></span> <span data-ttu-id="b110a-119">产品的价目表明细始终引用特定单位。</span><span class="sxs-lookup"><span data-stu-id="b110a-119">Price list lines for products always reference a specific unit.</span></span> <span data-ttu-id="b110a-120">可以将价目表项中的产品的定价配置为货币金额。</span><span class="sxs-lookup"><span data-stu-id="b110a-120">Pricing for a product on price list items can be configured as a currency amount.</span></span> <span data-ttu-id="b110a-121">也可以将其配置为定价、当前成本或标准成本的函数。</span><span class="sxs-lookup"><span data-stu-id="b110a-121">Alternatively, it can be configured as a function of the list price, current cost, or standard cost.</span></span>

<span data-ttu-id="b110a-122">PSA 支持在将价格配置为定价、标准成本或当前成本时使用各种舍入选项。</span><span class="sxs-lookup"><span data-stu-id="b110a-122">PSA supports various rounding options when prices are configured as a function of the list price, standard cost, or current cost.</span></span> <span data-ttu-id="b110a-123">除了利用多种定价方法和舍入选项，还可以将折扣表与价目表项关联。</span><span class="sxs-lookup"><span data-stu-id="b110a-123">In addition to taking advantage of multiple pricing methods and rounding options, you can associate discount lists with price list items.</span></span> 

> ![将目录中的产品添加到不同价目表中](media/basic-guide-16.png)

<span data-ttu-id="b110a-125">通过选择 **项目报价单** 页中的 **创建自定义报价** 为报价单创建新的自定义价目表时，PSA 将创建该价目表的备份，并将新价目表标头中的 **实体** 字段设置为 **销售实体** 。</span><span class="sxs-lookup"><span data-stu-id="b110a-125">When you create a new custom price list for a quote by selecting **Create Custom Pricing** on the **Project Quote** page, PSA makes a copy of the price list, and the **Entity** field on the header of the new price list is set to **Sales Entity**.</span></span> <span data-ttu-id="b110a-126">将为新价目表的名称追加报价单名称和时间戳。</span><span class="sxs-lookup"><span data-stu-id="b110a-126">The name of the new price list is appended with the name of the quote and a timestamp.</span></span> <span data-ttu-id="b110a-127">也可以在自定义工作流中使用新价目表的名称和报价单的名称对使用自定义定价的报价单触发额外审阅和审批。</span><span class="sxs-lookup"><span data-stu-id="b110a-127">You also can use the name of the new price list and the name of the quote in custom workflows to trigger additional review and approvals for quotes that use custom pricing.</span></span>

 
## <a name="default-product-price-list"></a><span data-ttu-id="b110a-128">默认产品价目表</span><span class="sxs-lookup"><span data-stu-id="b110a-128">Default product price list</span></span>
<span data-ttu-id="b110a-129">每个客户记录都有一个 **默认价目表** 字段，可在其中指定与客户的货币匹配的价目表。</span><span class="sxs-lookup"><span data-stu-id="b110a-129">Each customer record has a **Default Price List** field, where you can specify a price list that matches the currency of the customer.</span></span> <span data-ttu-id="b110a-130">在 PSA 中，不会在此字段中自动输入默认值。</span><span class="sxs-lookup"><span data-stu-id="b110a-130">In PSA, a default value isn't automatically entered in this field.</span></span> <span data-ttu-id="b110a-131">如果有与特定客户达成的自定义定价协议，可使用此字段为该客户关联价目表。</span><span class="sxs-lookup"><span data-stu-id="b110a-131">When a custom pricing agreement with a specific customer exists, you can use this field to associate a price list with that customer.</span></span>

<span data-ttu-id="b110a-132">商机、报价单和项目合同实体按照以下顺序输入默认产品价目表。</span><span class="sxs-lookup"><span data-stu-id="b110a-132">The Opportunity, Quote, and Project Contract entities use the following order to enter default product price lists.</span></span> <span data-ttu-id="b110a-133">项目价目表也采用相同的顺序。</span><span class="sxs-lookup"><span data-stu-id="b110a-133">The same order is used for project price lists.</span></span>

1.  <span data-ttu-id="b110a-134">报价单</span><span class="sxs-lookup"><span data-stu-id="b110a-134">Quote</span></span>
2.  <span data-ttu-id="b110a-135">商机</span><span class="sxs-lookup"><span data-stu-id="b110a-135">Opportunity</span></span>
3.  <span data-ttu-id="b110a-136">客户</span><span class="sxs-lookup"><span data-stu-id="b110a-136">Customer</span></span>
4.  <span data-ttu-id="b110a-137">PSA 的全局设置</span><span class="sxs-lookup"><span data-stu-id="b110a-137">Global settings for PSA</span></span>

<span data-ttu-id="b110a-138">默认情况下，报价单明细中的 **产品** 字段列出报价单的产品价目表中的所有可用产品。</span><span class="sxs-lookup"><span data-stu-id="b110a-138">By default, the **Product** field on the quote line lists all the active products in the product price list of the quote.</span></span> <span data-ttu-id="b110a-139">如果已停用某个产品，或者该产品是草稿产品，则不列出该产品，即使价目表中有此产品。</span><span class="sxs-lookup"><span data-stu-id="b110a-139">If a product has been inactivated, or if it's a draft product, it isn't listed, even if it's in the price list.</span></span> 

<span data-ttu-id="b110a-140">产品目录明细作为发票明细添加到为项目合同创建的第一份发票中。</span><span class="sxs-lookup"><span data-stu-id="b110a-140">Product catalog lines are added as invoice lines on the first invoice that is created for a project contract.</span></span> <span data-ttu-id="b110a-141">在草稿发票中，可以删除这些发票明细。</span><span class="sxs-lookup"><span data-stu-id="b110a-141">On a draft invoice, those invoice lines can be deleted.</span></span> <span data-ttu-id="b110a-142">在此情况下想，这些发票将在后续发票中出现，直到为其开票或将发票发给客户。</span><span class="sxs-lookup"><span data-stu-id="b110a-142">In that case, the lines will appear on a subsequent invoice until they are invoiced, or until the invoice is sent to the customer.</span></span> <span data-ttu-id="b110a-143">在 PSA 中，不能为产品发票明细的部分数量开票。</span><span class="sxs-lookup"><span data-stu-id="b110a-143">In PSA, you can't invoice a partial quantity of a product invoice line.</span></span> <span data-ttu-id="b110a-144">为项目合同中的产品明细开票时，将创建实际值。</span><span class="sxs-lookup"><span data-stu-id="b110a-144">When the product lines from the project contract are invoiced, actuals are created.</span></span> <span data-ttu-id="b110a-145">但是，不将这些实际值链接到相关项目实体。</span><span class="sxs-lookup"><span data-stu-id="b110a-145">However, those actuals aren't linked to the related project entity.</span></span> <span data-ttu-id="b110a-146">换句话说，基于产品的项目合同明细独立于任何基于项目的使用。</span><span class="sxs-lookup"><span data-stu-id="b110a-146">In other words, product-based project contract lines are independent of any project-based use.</span></span> <span data-ttu-id="b110a-147">PSA 不跟踪项目的材料消耗。</span><span class="sxs-lookup"><span data-stu-id="b110a-147">PSA doesn't track material consumption on projects.</span></span>
