---
title: 基于产品的报价单明细概述 - 精简
description: 此主题提供有关处理基于产品的报价单明细的信息。
author: rumant
manager: Annbe
ms.date: 10/30/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: f6aa428c486f149308ad078f9d7a80a0be0f0f04
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/30/2020
ms.locfileid: "4178177"
---
# <a name="product-based-quote-lines-overview---lite"></a><span data-ttu-id="71b54-103">基于产品的报价单明细概述 - 精简</span><span class="sxs-lookup"><span data-stu-id="71b54-103">Product-based quote lines overview - lite</span></span>

<span data-ttu-id="71b54-104">_**适用于：** 精简部署 - 估价交易开票_</span><span class="sxs-lookup"><span data-stu-id="71b54-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="71b54-105">可在 Dynamics 365 Project Operations 中创建基于产品的报价单明细。</span><span class="sxs-lookup"><span data-stu-id="71b54-105">You can create product-based quote lines in Dynamics 365 Project Operations.</span></span> <span data-ttu-id="71b54-106">基于产品的报价单明细可以手动添加，也可以是产品目录中的项。</span><span class="sxs-lookup"><span data-stu-id="71b54-106">Product-based quote lines can be manually added, or they can be items from the product catalog.</span></span>

## <a name="product-catalog"></a><span data-ttu-id="71b54-107">产品目录</span><span class="sxs-lookup"><span data-stu-id="71b54-107">Product catalog</span></span>

<span data-ttu-id="71b54-108">产品目录中的每个产品都有默认计价单位和计价单位组。</span><span class="sxs-lookup"><span data-stu-id="71b54-108">Each product in the product catalog has a default unit and unit group.</span></span> <span data-ttu-id="71b54-109">如果多个产品共享同一组属性，可以创建共享这些属性的产品系列。</span><span class="sxs-lookup"><span data-stu-id="71b54-109">If multiple products share the same set of attributes, you can create a product family that share those attributes.</span></span> 

<span data-ttu-id="71b54-110">例如，一家公司销售不同类型软件的订阅许可证。</span><span class="sxs-lookup"><span data-stu-id="71b54-110">For example, a company sells subscription licenses for different kinds of software.</span></span> <span data-ttu-id="71b54-111">所有订阅软件都有下面的两个属性：</span><span class="sxs-lookup"><span data-stu-id="71b54-111">All subscription software has the following two attributes:</span></span>

- <span data-ttu-id="71b54-112">用户数</span><span class="sxs-lookup"><span data-stu-id="71b54-112">Number of users</span></span>
- <span data-ttu-id="71b54-113">订阅持续时间（以月为单位）</span><span class="sxs-lookup"><span data-stu-id="71b54-113">A subscription duration measured in months</span></span>

<span data-ttu-id="71b54-114">要维护这类目录，创建一个名称为 **订阅软件** 的产品系列，然后将用户数目和订阅持续时间添加为属性。</span><span class="sxs-lookup"><span data-stu-id="71b54-114">To maintain this type of catalog, create a product family named **Subscription Software** and add the number of users and the subscription duration as attributes.</span></span> <span data-ttu-id="71b54-115">接下来，您可以将各个产品添加到 **订阅软件** 产品系列中。</span><span class="sxs-lookup"><span data-stu-id="71b54-115">Next, you can add individual products to the **Subscription Software** product family.</span></span>

## <a name="add-product-catalog-items-to-a-project-quote"></a><span data-ttu-id="71b54-116">向项目报价单添加产品目录项</span><span class="sxs-lookup"><span data-stu-id="71b54-116">Add product catalog items to a project quote</span></span>

<span data-ttu-id="71b54-117">**项目报价单** 和 **项目合同** 页有两个部分：基于项目的明细和基于产品的明细。</span><span class="sxs-lookup"><span data-stu-id="71b54-117">The **Project Quote** and **Project Contract** pages have sections for project-based lines and product-based lines.</span></span> <span data-ttu-id="71b54-118">对于基于产品的明细，报价单明细或项目合同子项的下拉列表中包含产品价目表中的所有产品和单位。</span><span class="sxs-lookup"><span data-stu-id="71b54-118">For product-based lines, the drop-down list on the quote line or project contract line includes all the products and units in the product price list.</span></span> <span data-ttu-id="71b54-119">您还可以添加不属于产品价目表的产品。</span><span class="sxs-lookup"><span data-stu-id="71b54-119">You can also add products that aren't part of the product price list.</span></span>

<span data-ttu-id="71b54-120">此外，还可以从其他价目表或直接从产品目录选择产品。</span><span class="sxs-lookup"><span data-stu-id="71b54-120">Additionally, you can select products from other price lists or directly from the product catalog.</span></span> <span data-ttu-id="71b54-121">直接从产品目录选择产品时，产品的默认价目表用于获取产品的销售价。</span><span class="sxs-lookup"><span data-stu-id="71b54-121">When you select products directly from a product catalog, the default price list of that product is used to get the product's sales price.</span></span> <span data-ttu-id="71b54-122">如果未设置默认价目表，则该价格设置为零 (0)。</span><span class="sxs-lookup"><span data-stu-id="71b54-122">If a default price list isn't set, the price is set to zero (0).</span></span>

<span data-ttu-id="71b54-123">当报价单明细基于产品目录时，可直接在报价单明细中替代售价。</span><span class="sxs-lookup"><span data-stu-id="71b54-123">When a quote line is based on a product catalog, you can override the sales price directly on the quote line.</span></span> <span data-ttu-id="71b54-124">有两个可用值的 **定价** 字段中的报价单明细：</span><span class="sxs-lookup"><span data-stu-id="71b54-124">A quote line in **Pricing** field with two available values:</span></span>

- <span data-ttu-id="71b54-125">**替代定价**</span><span class="sxs-lookup"><span data-stu-id="71b54-125">**Override Pricing**</span></span>
- <span data-ttu-id="71b54-126">**系统价格**</span><span class="sxs-lookup"><span data-stu-id="71b54-126">**Use Default**</span></span>

<span data-ttu-id="71b54-127">如果选择 **替代定价**，将不设置默认价格。</span><span class="sxs-lookup"><span data-stu-id="71b54-127">If you select **Override Pricing**, the default price isn't set.</span></span> <span data-ttu-id="71b54-128">而是必须为报价单中的产品输入价格。</span><span class="sxs-lookup"><span data-stu-id="71b54-128">Instead, you must enter a price for the product on the quote line.</span></span> <span data-ttu-id="71b54-129">如果您选择 **系统价格**，将使用默认售价，此字段将被锁定，无法进行编辑。</span><span class="sxs-lookup"><span data-stu-id="71b54-129">If you select **Use Default**, the default sales price is used and the field is locked for editing.</span></span>

<span data-ttu-id="71b54-130">将在报价单的基于产品的明细中输入默认售价。</span><span class="sxs-lookup"><span data-stu-id="71b54-130">Default sales prices are entered on the product-based lines of a quote.</span></span> <span data-ttu-id="71b54-131">然后将 **定价** 字段设置为 **替代定价**，以便您编辑报价单明细中的默认价格。</span><span class="sxs-lookup"><span data-stu-id="71b54-131">The **Pricing** field is then set to **Override Pricing** so that you can edit the default price on the quote lines.</span></span> <span data-ttu-id="71b54-132">这是对 Dynamics 365 Sales 中基于产品的明细行为的 Project Operations 特定替代。</span><span class="sxs-lookup"><span data-stu-id="71b54-132">This is a Project Operations-specific override to the product-based lines behavior in Dynamics 365 Sales.</span></span>
