---
title: 基于产品的合同子项概述
description: 此主题介绍基于产品的合同子项。
author: rumant
manager: Annbe
ms.date: 10/07/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 794a80b0dd6b8717b43e712b96b9ac077517c226
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/16/2020
ms.locfileid: "4072531"
---
# <a name="product-based-contract-lines-overview"></a><span data-ttu-id="77b8d-103">基于产品的合同子项概述</span><span class="sxs-lookup"><span data-stu-id="77b8d-103">Product-based contract lines overview</span></span>

<span data-ttu-id="77b8d-104">_**适用于：** 精简部署 - 估价交易开票_</span><span class="sxs-lookup"><span data-stu-id="77b8d-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="77b8d-105">您可以在 Dynamics 365 Project Operations 中创建基于产品的合同子项。</span><span class="sxs-lookup"><span data-stu-id="77b8d-105">You can create product-based contract lines in Dynamics 365 Project Operations.</span></span> <span data-ttu-id="77b8d-106">基于产品的合同子项可以是手动创建的明细，也可以是产品目录中的项。</span><span class="sxs-lookup"><span data-stu-id="77b8d-106">Product-based contract lines can be manually created lines, or they can be items from the product catalog.</span></span>

## <a name="product-catalog"></a><span data-ttu-id="77b8d-107">产品目录</span><span class="sxs-lookup"><span data-stu-id="77b8d-107">Product catalog</span></span>

<span data-ttu-id="77b8d-108">产品目录中的产品具有默认计价单位和计价单位组。</span><span class="sxs-lookup"><span data-stu-id="77b8d-108">The products in the product catalog have a default unit and unit group.</span></span> <span data-ttu-id="77b8d-109">如果多个产品共享同一组属性，可以创建也具有这些属性的产品系列。</span><span class="sxs-lookup"><span data-stu-id="77b8d-109">If several products share the same set of attributes, you can create a product family that also has those attributes.</span></span> <span data-ttu-id="77b8d-110">同一个产品系列中的所有产品继承同一组属性。</span><span class="sxs-lookup"><span data-stu-id="77b8d-110">All the products in one product family inherit the same set of attributes.</span></span>

<span data-ttu-id="77b8d-111">例如，一家公司销售不同类型软件的订阅许可证。</span><span class="sxs-lookup"><span data-stu-id="77b8d-111">For example, a company sells subscription licenses for different kinds of software.</span></span> <span data-ttu-id="77b8d-112">所有订阅软件都有下面的两个属性：</span><span class="sxs-lookup"><span data-stu-id="77b8d-112">All subscription software has the following two attributes:</span></span>

- <span data-ttu-id="77b8d-113">用户数</span><span class="sxs-lookup"><span data-stu-id="77b8d-113">Number of users</span></span>
- <span data-ttu-id="77b8d-114">订阅持续时间（以月为单位）</span><span class="sxs-lookup"><span data-stu-id="77b8d-114">Subscription duration (in months)</span></span>

<span data-ttu-id="77b8d-115">若要维护此类目录，请创建一个名为 **订阅软件** 的产品系列。</span><span class="sxs-lookup"><span data-stu-id="77b8d-115">To maintain this type of catalog, create a product family that is named **Subscription Software**.</span></span> <span data-ttu-id="77b8d-116">将属性、 **用户数** 和 **订阅持续时间** 添加到产品系列中。</span><span class="sxs-lookup"><span data-stu-id="77b8d-116">Add the attributes, **Number of users** and **Subscription duration** to the product family.</span></span> <span data-ttu-id="77b8d-117">然后，将各个产品添加到 **订阅软件** 产品系列中。</span><span class="sxs-lookup"><span data-stu-id="77b8d-117">Then, add individual products to the **Subscription Software** product family.</span></span>

## <a name="add-product-catalog-items-to-a-project-contract"></a><span data-ttu-id="77b8d-118">向项目合同添加产品目录项</span><span class="sxs-lookup"><span data-stu-id="77b8d-118">Add product catalog items to a project Contract</span></span>

<span data-ttu-id="77b8d-119">项目合同针对两种明细划分部分：基于项目和基于产品。</span><span class="sxs-lookup"><span data-stu-id="77b8d-119">Project contracts have sections for two types of lines, project-based and product-based.</span></span> <span data-ttu-id="77b8d-120">基于产品的明细在合同中包含产品价目表中的所有产品和计价单位。</span><span class="sxs-lookup"><span data-stu-id="77b8d-120">Product-based lines include all of the products and units in the product price list on the contract.</span></span> <span data-ttu-id="77b8d-121">可以添加不属于合同的产品价目表的产品。</span><span class="sxs-lookup"><span data-stu-id="77b8d-121">Products that aren't part of contract's product price list can be added.</span></span>

<span data-ttu-id="77b8d-122">您可以从其他价目表中选择产品，也可以直接从产品目录中选择产品。</span><span class="sxs-lookup"><span data-stu-id="77b8d-122">You can select products from other price lists, or directly from the product catalog.</span></span> <span data-ttu-id="77b8d-123">直接从产品目录选择产品时，该产品的默认价目表将用于产品的售价。</span><span class="sxs-lookup"><span data-stu-id="77b8d-123">When you select products directly from a product catalog, the default price list of that product is used for the product's sales price.</span></span> <span data-ttu-id="77b8d-124">如果未设置默认价目表，则该价格设置为 0（零）。</span><span class="sxs-lookup"><span data-stu-id="77b8d-124">If a default price list isn't set, the price is set to 0 (zero).</span></span>

<span data-ttu-id="77b8d-125">如果合同子项基于产品目录，则可直接在合同子项中替代售价。</span><span class="sxs-lookup"><span data-stu-id="77b8d-125">If a contract line is based on a product catalog, you can override the sales price directly on the line.</span></span> <span data-ttu-id="77b8d-126">合同子项具有 **定价** 字段，此字段有两个值：</span><span class="sxs-lookup"><span data-stu-id="77b8d-126">A contract line has the **Pricing** field with the two values:</span></span>

- <span data-ttu-id="77b8d-127">**替代定价**</span><span class="sxs-lookup"><span data-stu-id="77b8d-127">**Override pricing**</span></span>
- <span data-ttu-id="77b8d-128">**使用默认值**</span><span class="sxs-lookup"><span data-stu-id="77b8d-128">**Use default**</span></span>

<span data-ttu-id="77b8d-129">如果将 **定价** 字段设置为 **替代定价** ，将不设置默认价格。</span><span class="sxs-lookup"><span data-stu-id="77b8d-129">If you set the **Pricing** field to **Override pricing** , the default price isn't set.</span></span> <span data-ttu-id="77b8d-130">为合同子项中的产品输入价格。</span><span class="sxs-lookup"><span data-stu-id="77b8d-130">Enter a price for the product on the contract line.</span></span> <span data-ttu-id="77b8d-131">如果将此字段设置为 **使用默认值** ，将使用默认售价，并且无法编辑此字段。</span><span class="sxs-lookup"><span data-stu-id="77b8d-131">If you set the field to **Use default** , the default sales price is used and the field can't be edited.</span></span>

<span data-ttu-id="77b8d-132">安装 Project Operations 之后，将在合同中基于产品的明细内输入默认售价。</span><span class="sxs-lookup"><span data-stu-id="77b8d-132">After you install Project Operations, default sales prices are entered on the product-based lines on a contract.</span></span> <span data-ttu-id="77b8d-133">**定价** 字段将设置为 **替代定价** ，以便您编辑合同子项中的默认价格。</span><span class="sxs-lookup"><span data-stu-id="77b8d-133">The **Pricing** field is set to **Override pricing** so that you can edit the default price on the contract lines.</span></span> <span data-ttu-id="77b8d-134">这是对 Dynamics 365 Sales 中基于产品的明细行为的 Project Operations 特定替代。</span><span class="sxs-lookup"><span data-stu-id="77b8d-134">This is a Project Operations-specific override to product-based lines behavior in Dynamics 365 Sales.</span></span>
