---
title: 管理基于产品的报价单明细的复杂单位（如每用户、每月）- 精简
description: 此主题提供有关管理基于产品的报价单明细的复杂单位的信息。
author: rumant
manager: Annbe
ms.date: 10/06/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 2ee46da2f663ef4f5f8fc7f9f89b6fcfd09a1798
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/30/2020
ms.locfileid: "4175565"
---
# <a name="managing-complex-units-such-as-per-user-per-month-for-product-based-quote-lines---lite"></a><span data-ttu-id="6c455-103">管理基于产品的报价单明细的复杂单位（如每用户、每月）- 精简</span><span class="sxs-lookup"><span data-stu-id="6c455-103">Managing complex units such as per-user, per-month for product-based quote lines - lite</span></span>

<span data-ttu-id="6c455-104">_**适用于：** 精简部署 - 估价交易开票_</span><span class="sxs-lookup"><span data-stu-id="6c455-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="6c455-105">Dynamics 365 Project Operations 使用数量因子为基于订阅的产品的销售提供支持。</span><span class="sxs-lookup"><span data-stu-id="6c455-105">Dynamics 365 Project Operations uses quantity factors to support the sale of subscription-based products.</span></span> <span data-ttu-id="6c455-106">对于基于订阅的产品，报价单或项目合同子项中的数量表示为用户的月数。</span><span class="sxs-lookup"><span data-stu-id="6c455-106">For subscription-based products, the quantity on the quote or project contract line is expressed as the number of user-months.</span></span>

<span data-ttu-id="6c455-107">通常，订阅软件的价格以每用户每月价格的形式存储在目录中。</span><span class="sxs-lookup"><span data-stu-id="6c455-107">Usually, the price of subscription software is stored in the catalog as the price per user per month.</span></span> <span data-ttu-id="6c455-108">销售阶段中，报价单明细中的价格通常为与 IT 销售代表协商并达成折扣的每用户每月价格。</span><span class="sxs-lookup"><span data-stu-id="6c455-108">During the sales process, the price on the quote line is usually the per-user, per-month price that was negotiated and discounted by the IT sales agent.</span></span> <span data-ttu-id="6c455-109">每笔交易的用户数量和订阅月数不同。</span><span class="sxs-lookup"><span data-stu-id="6c455-109">Each deal has a different number of users and a different number of subscription months.</span></span> <span data-ttu-id="6c455-110">用于计算报价单明细的数量是用户数与订阅月数的乘积。</span><span class="sxs-lookup"><span data-stu-id="6c455-110">The quantity used to compute the quote line is a product of the number of users and the number of subscription months.</span></span>

<span data-ttu-id="6c455-111">为了支持这种销售，Project Operations 引入了数量因子这一概念。</span><span class="sxs-lookup"><span data-stu-id="6c455-111">To support this type of sale, Project Operations introduced the concept of quantity factors.</span></span> <span data-ttu-id="6c455-112">在 Dynamics 365 中，数量因子依赖于产品属性。</span><span class="sxs-lookup"><span data-stu-id="6c455-112">Quantity factors rely on the product attributes in Dynamics 365.</span></span> <span data-ttu-id="6c455-113">为产品配置特定属性时，Project Operations 会让您将部分或全部属性标记为数量因子。</span><span class="sxs-lookup"><span data-stu-id="6c455-113">When you configure specific properties for a product, Project Operations lets you flag a subset, or all of the properties, as quantity factors.</span></span>

<span data-ttu-id="6c455-114">Project Operations 将验证是否只有数值属性或具有数值数据类型的产品属性标记为数量因子。</span><span class="sxs-lookup"><span data-stu-id="6c455-114">Project Operations validates that only numeric properties or product properties that have a numeric data type are flagged as quantity factors.</span></span> <span data-ttu-id="6c455-115">当您将具有数量因子的产品添加到报价单明细时，**数量** 字段将变为只读。</span><span class="sxs-lookup"><span data-stu-id="6c455-115">When you add a product with quantity factors to a quote line, the **Quantity** field becomes read-only.</span></span> <span data-ttu-id="6c455-116">为充当数量因子的产品属性输入值之后，Project Operations 将计算报价单明细的数量。</span><span class="sxs-lookup"><span data-stu-id="6c455-116">After you enter values for product properties that are quantity factors, Project Operations calculates the quantity of the quote line.</span></span>

<span data-ttu-id="6c455-117">例如，Dynamics 365 Sales 可能具有以下属性：</span><span class="sxs-lookup"><span data-stu-id="6c455-117">For example, Dynamics 365 Sales might have the following properties:</span></span>

- <span data-ttu-id="6c455-118">**用户数**：用户的数量</span><span class="sxs-lookup"><span data-stu-id="6c455-118">**No of users**: The number of users</span></span>
- <span data-ttu-id="6c455-119">**月数**：订阅的月数</span><span class="sxs-lookup"><span data-stu-id="6c455-119">**No of Months**: The number of subscription months</span></span>
- <span data-ttu-id="6c455-120">**产品 SKU**</span><span class="sxs-lookup"><span data-stu-id="6c455-120">**Product SKU**</span></span>

<span data-ttu-id="6c455-121">您可以通过编辑产品明细的属性，将 **用户数** 和 **月数** 属性标记为数量因子。</span><span class="sxs-lookup"><span data-stu-id="6c455-121">You can flag the **No of Users** and **No of Months** properties as quantity factors by editing the properties of the product line.</span></span>

<span data-ttu-id="6c455-122">若要从产品属性创建数量因子，请执行以下步骤：</span><span class="sxs-lookup"><span data-stu-id="6c455-122">To create Quantity factors from Product properties, follow these steps:</span></span>

1. <span data-ttu-id="6c455-123">在 Project Operations 的左侧导航窗格中，转到 **销售** > **产品**。</span><span class="sxs-lookup"><span data-stu-id="6c455-123">On the Project Operations left navigation pane, go to **Sales** > **Products**.</span></span>
2. <span data-ttu-id="6c455-124">打开需要为其配置数量因子的产品。</span><span class="sxs-lookup"><span data-stu-id="6c455-124">Open the product for which you need to configure quantity factors.</span></span> <span data-ttu-id="6c455-125">确保产品已配置属性。</span><span class="sxs-lookup"><span data-stu-id="6c455-125">Make sure the product has properties already configured.</span></span>
3. <span data-ttu-id="6c455-126">在产品的 **项目信息** 页上，选择 **数量因子** 选项卡。</span><span class="sxs-lookup"><span data-stu-id="6c455-126">On the **Project Information** page for the Product, select the **Quantity Factors** tab.</span></span>
4. <span data-ttu-id="6c455-127">在子网格中，选择 **+ 新建字段计算**。</span><span class="sxs-lookup"><span data-stu-id="6c455-127">In the subgrid, select **+ New field computation**.</span></span>
5. <span data-ttu-id="6c455-128">输入数量因子的名称，然后选择要映射到字段计算的属性值。</span><span class="sxs-lookup"><span data-stu-id="6c455-128">Enter the name of the Quantity factor and select the property value that maps to the field computation.</span></span>
6. <span data-ttu-id="6c455-129">保存并关闭窗体。</span><span class="sxs-lookup"><span data-stu-id="6c455-129">Save and close the form.</span></span> <span data-ttu-id="6c455-130">对所有用于计算基于产品的报价单明细的数量的属性重复这些步骤。</span><span class="sxs-lookup"><span data-stu-id="6c455-130">Repeat these steps for all properties to use for computing the quantity for the product-based quote line.</span></span>

<span data-ttu-id="6c455-131">在您为产品创建基于产品的报价单明细时，报价单明细的数量将被锁定。</span><span class="sxs-lookup"><span data-stu-id="6c455-131">When you create a product-based quote line for a product, the quantity of the quote line will be locked.</span></span> <span data-ttu-id="6c455-132">此数量将计算为您为该报价单明细输入的属性值的乘积。</span><span class="sxs-lookup"><span data-stu-id="6c455-132">The quantity will be computed as a product of the property values that you input for that quote line.</span></span>
