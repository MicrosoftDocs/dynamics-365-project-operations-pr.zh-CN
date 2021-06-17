---
title: 基于产品的报价单明细
description: 此主题介绍基于产品的报价单明细。
author: rumant
ms.custom:
- dyn365-projectservice
ms.date: 03/06/2019
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
ms.openlocfilehash: 1bd789f4ee4d5b4603093be24aa25addafa9e8e8
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/10/2021
ms.locfileid: "5998490"
---
# <a name="product-based-quote-lines"></a><span data-ttu-id="4d8c7-103">基于产品的报价单明细</span><span class="sxs-lookup"><span data-stu-id="4d8c7-103">Product-based quote lines</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]


<span data-ttu-id="4d8c7-104">可在 Dynamics 365 Project Service Automation 中创建基于产品的报价单明细。</span><span class="sxs-lookup"><span data-stu-id="4d8c7-104">You can create product-based quote lines in Dynamics 365 Project Service Automation.</span></span> <span data-ttu-id="4d8c7-105">基于产品的报价单明细可以是“目录外”明细，也可以是产品目录中的项。</span><span class="sxs-lookup"><span data-stu-id="4d8c7-105">Product-based quote lines can be "write-in" lines, or they can be items from the product catalog.</span></span>

## <a name="product-catalog"></a><span data-ttu-id="4d8c7-106">产品目录</span><span class="sxs-lookup"><span data-stu-id="4d8c7-106">Product catalog</span></span>

<span data-ttu-id="4d8c7-107">Dynamics 365 产品目录中的产品具有默认计价单位和计价单位组。</span><span class="sxs-lookup"><span data-stu-id="4d8c7-107">The products in a Dynamics 365 product catalog have a default unit and unit group.</span></span> <span data-ttu-id="4d8c7-108">如果多个产品共享同一组属性，可以创建也具有这些属性的产品系列。</span><span class="sxs-lookup"><span data-stu-id="4d8c7-108">If several products share the same set of attributes, you can create a product family that also has those attributes.</span></span> <span data-ttu-id="4d8c7-109">同一个产品系列中的所有产品继承同一组属性。</span><span class="sxs-lookup"><span data-stu-id="4d8c7-109">All the products in one product family inherit the same set of attributes.</span></span>

<span data-ttu-id="4d8c7-110">例如，一家公司销售大量软件的订阅许可证。</span><span class="sxs-lookup"><span data-stu-id="4d8c7-110">For example, a company sells subscription licenses for a variety of software.</span></span> <span data-ttu-id="4d8c7-111">所有订阅软件都有下面的两个属性：</span><span class="sxs-lookup"><span data-stu-id="4d8c7-111">All subscription software has the following two attributes:</span></span>

- <span data-ttu-id="4d8c7-112">用户数目</span><span class="sxs-lookup"><span data-stu-id="4d8c7-112">Number of users</span></span> 
- <span data-ttu-id="4d8c7-113">订阅持续时间（以月为单位）</span><span class="sxs-lookup"><span data-stu-id="4d8c7-113">Subscription duration (in months)</span></span>

<span data-ttu-id="4d8c7-114">维护这种目录的一个好办法是创建一个名称为 **订阅软件** 的产品系列，并且该产品系列的属性为 **用户数目** 和 **订阅持续时间**。</span><span class="sxs-lookup"><span data-stu-id="4d8c7-114">A good way to maintain this type of catalog is to create a product family that is named **Subscription Software**, and that has **Number of users** and **Subscription duration** as attributes.</span></span> <span data-ttu-id="4d8c7-115">然后可以向 **订阅软件** 产品系列添加单个产品，如 **Dynamics 365 Sales** 或 **Dynamics 365 Field Service**。</span><span class="sxs-lookup"><span data-stu-id="4d8c7-115">You can then add individual products, such as **Dynamics 365 Sales** or **Dynamics 365 Field Service** to the **Subscription Software** product family.</span></span>

## <a name="adding-product-catalog-items-to-a-project-quote"></a><span data-ttu-id="4d8c7-116">向项目报价单添加产品目录项</span><span class="sxs-lookup"><span data-stu-id="4d8c7-116">Adding product catalog items to a project quote</span></span>

<span data-ttu-id="4d8c7-117">项目报价单和项目合同页有两种明细的部分：基于项目的明细和基于产品的明细。</span><span class="sxs-lookup"><span data-stu-id="4d8c7-117">Project quote and project contract pages have sections for two types of lines: project-based lines and product-based lines.</span></span> <span data-ttu-id="4d8c7-118">对于基于产品的明细，Dynamics 365 用于将产品目录中的项添加到报价单。</span><span class="sxs-lookup"><span data-stu-id="4d8c7-118">For product-based lines, Dynamics 365 is used to add items from a product catalog to a quote.</span></span> <span data-ttu-id="4d8c7-119">报价单明细或项目合同子项的下拉列表中包含附加到该报价单或项目合同的产品价目表中的所有产品和单位。</span><span class="sxs-lookup"><span data-stu-id="4d8c7-119">The drop-down list on the quote line or project contract line includes all the products and units in the product price list that is attached to the quote or project contract.</span></span> <span data-ttu-id="4d8c7-120">也可以添加不属于报价单产品价目表的产品。</span><span class="sxs-lookup"><span data-stu-id="4d8c7-120">You can also add products that aren't part of quote's product price list.</span></span>

<span data-ttu-id="4d8c7-121">此外，还可以从其他价目表选择产品，或者直接从产品目录选择产品。</span><span class="sxs-lookup"><span data-stu-id="4d8c7-121">Additionally, you can select products from other price lists, or you can select products directly from the product catalog.</span></span> <span data-ttu-id="4d8c7-122">直接从产品目录选择产品时，产品的默认价目表用于获取产品的销售价。</span><span class="sxs-lookup"><span data-stu-id="4d8c7-122">When you select products directly from a product catalog, the default price list of that product is used to get the product's sales price.</span></span> <span data-ttu-id="4d8c7-123">如果未设置默认价目表，则该价格设置为 0（零）。</span><span class="sxs-lookup"><span data-stu-id="4d8c7-123">If a default price list isn't set, the price is set to 0 (zero).</span></span>

<span data-ttu-id="4d8c7-124">如果报价单明细基于产品目录，则可直接在报价单明细中替代销售价。</span><span class="sxs-lookup"><span data-stu-id="4d8c7-124">If a quote line is based on a product catalog, you can override the sales price directly on the quote line.</span></span> <span data-ttu-id="4d8c7-125">请注意，Dynamics 365 中的报价单明细有一个 **定价** 字段。</span><span class="sxs-lookup"><span data-stu-id="4d8c7-125">Note that a quote line in Dynamics 365 has a **Pricing** field.</span></span> <span data-ttu-id="4d8c7-126">有两个值：</span><span class="sxs-lookup"><span data-stu-id="4d8c7-126">Two values are available:</span></span>

- <span data-ttu-id="4d8c7-127">替代定价</span><span class="sxs-lookup"><span data-stu-id="4d8c7-127">Override pricing</span></span>  
- <span data-ttu-id="4d8c7-128">使用默认值</span><span class="sxs-lookup"><span data-stu-id="4d8c7-128">Use default</span></span>

<span data-ttu-id="4d8c7-129">如果将此字段设置为 **替代定价**，Dynamics 365 将不设置默认价格。</span><span class="sxs-lookup"><span data-stu-id="4d8c7-129">If you set this field to **Override pricing**, Dynamics 365 doesn't set a default price.</span></span> <span data-ttu-id="4d8c7-130">必须为报价单中的产品输入价格。</span><span class="sxs-lookup"><span data-stu-id="4d8c7-130">You must enter a price for the product on the quote line.</span></span> <span data-ttu-id="4d8c7-131">如果将此字段设置为 **使用默认值**，Dynamics 365 将使用默认销售价，并锁定字段，以免被编辑。</span><span class="sxs-lookup"><span data-stu-id="4d8c7-131">If you set this field to **Use default**, Dynamics 365 uses the default sales price and locks the field to prevent editing.</span></span>

<span data-ttu-id="4d8c7-132">安装 PSA 之后，将在报价单中基于产品的明细内输入默认销售价。</span><span class="sxs-lookup"><span data-stu-id="4d8c7-132">After you install PSA, default sales prices are entered on the product-based lines on a quote.</span></span> <span data-ttu-id="4d8c7-133">然后将 **定价** 字段设置为 **替代定价**，以便您编辑报价单明细中的默认价格。</span><span class="sxs-lookup"><span data-stu-id="4d8c7-133">The **Pricing** field is then set to **Override pricing** so that you can edit the default price on the quote lines.</span></span>

> ![设置替代定价](media/basic-guide-10.png)
 
## <a name="quantity-factors-for-products"></a><span data-ttu-id="4d8c7-135">产品的数量因子</span><span class="sxs-lookup"><span data-stu-id="4d8c7-135">Quantity factors for products</span></span>

<span data-ttu-id="4d8c7-136">PSA 使用数量因子为基于订阅的产品的销售提供支持。</span><span class="sxs-lookup"><span data-stu-id="4d8c7-136">PSA uses quantity factors to support the sale of subscription-based products.</span></span> <span data-ttu-id="4d8c7-137">对于基于订阅的产品，报价单或项目合同子项中的数量表示为用户的月数。</span><span class="sxs-lookup"><span data-stu-id="4d8c7-137">For subscription-based products, the quantity on the quote or project contract line is expressed as the number of user months.</span></span>

<span data-ttu-id="4d8c7-138">通常，订阅软件的价格以每用户每月价格的形式存储在目录中。</span><span class="sxs-lookup"><span data-stu-id="4d8c7-138">Usually, the price of subscription software is stored in the catalog as the price per user per month.</span></span> <span data-ttu-id="4d8c7-139">但是，可改用其他时间描述。</span><span class="sxs-lookup"><span data-stu-id="4d8c7-139">However, you can use other time descriptions instead.</span></span> <span data-ttu-id="4d8c7-140">销售阶段中，报价单明细中的价格通常为与 IT 销售代表协商并达成折扣的每用户每月价格。</span><span class="sxs-lookup"><span data-stu-id="4d8c7-140">During the sales process, the price on the quote line is usually the per-user, per-month price that was negotiated and discounted by the IT sales agent.</span></span> <span data-ttu-id="4d8c7-141">每笔交易的用户数量和订阅月数不同。</span><span class="sxs-lookup"><span data-stu-id="4d8c7-141">Each deal has a different number of users and a different number of subscription months.</span></span> <span data-ttu-id="4d8c7-142">用于计算报价单明细金额的数量是用户数与订阅月数的乘积。</span><span class="sxs-lookup"><span data-stu-id="4d8c7-142">The quantity that is used to compute the amount of the quote line is a product of the number of users and the number of subscription months.</span></span>

<span data-ttu-id="4d8c7-143">为了支持这种销售，PSA 引入了数量因子这一概念。</span><span class="sxs-lookup"><span data-stu-id="4d8c7-143">To support this type of sale, PSA introduced the concept of quantity factors.</span></span> <span data-ttu-id="4d8c7-144">在 Dynamics 365 中，数量因子依赖于产品属性。</span><span class="sxs-lookup"><span data-stu-id="4d8c7-144">Quantity factors rely on the product attributes in Dynamics 365.</span></span> <span data-ttu-id="4d8c7-145">为产品配置特定属性时，PSA 将请您把这些属性中的一小部分或全部标记为数量因子。</span><span class="sxs-lookup"><span data-stu-id="4d8c7-145">When you configure specific properties for a product, PSA lets you flag a subset of those properties, or all the properties, as quantity factors.</span></span>

<span data-ttu-id="4d8c7-146">PSA 将验证是否只有数值属性或具有数值数据类型的产品属性标记为数量因子。</span><span class="sxs-lookup"><span data-stu-id="4d8c7-146">PSA validates that only numeric properties or product properties that have a numeric data type are flagged as quantity factors.</span></span> <span data-ttu-id="4d8c7-147">将为其配置了数量因子的产品添加到报价单明细时，报价单明细中的 **数量** 字段将成为只读字段。</span><span class="sxs-lookup"><span data-stu-id="4d8c7-147">When a product that quantity factors are configured for is added to a quote line, the **Quantity** field on the quote line becomes a read-only field.</span></span> <span data-ttu-id="4d8c7-148">为充当数量因子的产品属性输入值之后，PSA 将计算报价单明细的数量。</span><span class="sxs-lookup"><span data-stu-id="4d8c7-148">After you enter values for product properties that are quantity factors, PSA computes the quantity of the quote line.</span></span>

<span data-ttu-id="4d8c7-149">例如，Dynamics 365 可能具有以下属性：</span><span class="sxs-lookup"><span data-stu-id="4d8c7-149">For example, Dynamics 365 might have the following properties:</span></span> 

- <span data-ttu-id="4d8c7-150">**用户数目** - 用户的数量</span><span class="sxs-lookup"><span data-stu-id="4d8c7-150">**No of users** - The number of users</span></span> 
- <span data-ttu-id="4d8c7-151">**月数** - 订阅的月数</span><span class="sxs-lookup"><span data-stu-id="4d8c7-151">**No of Months** - The number of subscription months</span></span>
- <span data-ttu-id="4d8c7-152">**产品 SKU**</span><span class="sxs-lookup"><span data-stu-id="4d8c7-152">**Product SKU**</span></span> 

<span data-ttu-id="4d8c7-153">可以通过编辑产品明细的属性，将 **用户数目** 和 **月数** 属性标记为数量因子。</span><span class="sxs-lookup"><span data-stu-id="4d8c7-153">Tne **No of Users** and **No of Months** properties can be flagged as quantity factors by editing the properties of the product line.</span></span> 

> ![将“用户数目”和“月数”标记为数量因子](media/basic-guide-11.png)
 


[!INCLUDE[footer-include](../includes/footer-banner.md)]