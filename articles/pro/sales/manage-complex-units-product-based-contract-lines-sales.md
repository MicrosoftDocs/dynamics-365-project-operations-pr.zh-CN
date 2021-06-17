---
title: 管理基于产品的合同子项的复杂单位 - 精简
description: 此主题提供有关支持基于订阅的产品的销售的信息。
author: rumant
ms.date: 10/28/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 86da5a96919438e883b56fc8ecfe765f70a789ff
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/10/2021
ms.locfileid: "6003170"
---
# <a name="manage-complex-units-for-product-based-contract-lines---lite"></a><span data-ttu-id="1d3f4-103">管理基于产品的合同子项的复杂单位 - 精简</span><span class="sxs-lookup"><span data-stu-id="1d3f4-103">Manage complex units for product-based contract lines - lite</span></span>

<span data-ttu-id="1d3f4-104">_**适用于：** 精简部署 - 估价交易开票_</span><span class="sxs-lookup"><span data-stu-id="1d3f4-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="1d3f4-105">Dynamics 365 Project Operations 使用数量因子为基于订阅的产品的销售提供支持。</span><span class="sxs-lookup"><span data-stu-id="1d3f4-105">Dynamics 365 Project Operations uses quantity factors to support the sale of subscription-based products.</span></span> <span data-ttu-id="1d3f4-106">对于基于订阅的产品，合同或项目合同子项中的数量表示为用户的月数。</span><span class="sxs-lookup"><span data-stu-id="1d3f4-106">For subscription-based products, the quantity on the contract or project contract line is expressed as the number of user-months.</span></span>

<span data-ttu-id="1d3f4-107">订阅软件的价格以每用户每月价格的形式存储在目录中。</span><span class="sxs-lookup"><span data-stu-id="1d3f4-107">The price of subscription software is stored in the catalog as the price per-user, per-month.</span></span> <span data-ttu-id="1d3f4-108">在销售流程中，合同子项中的价格通常为与销售代表协商并达成折扣的每用户每月价格。</span><span class="sxs-lookup"><span data-stu-id="1d3f4-108">During the sales process, the price on the contract line is usually the per-user, per-month price that was negotiated and discounted by the sales agent.</span></span> <span data-ttu-id="1d3f4-109">每笔交易的用户数量和订阅月数不同。</span><span class="sxs-lookup"><span data-stu-id="1d3f4-109">Each deal has a different number of users and a different number of subscription months.</span></span> <span data-ttu-id="1d3f4-110">用于计算合同子项金额的数量是用户数与订阅月数的乘积。</span><span class="sxs-lookup"><span data-stu-id="1d3f4-110">The quantity used to calculate the amount of the contract line is a product of the number of users and the number of subscription months.</span></span>

<span data-ttu-id="1d3f4-111">为了支持这种销售，Project Operations 支持 *数量因子* 概念。</span><span class="sxs-lookup"><span data-stu-id="1d3f4-111">To support this type of sale, Project Operations supports the concept of *quantity factors*.</span></span> <span data-ttu-id="1d3f4-112">数量因子依赖于产品属性。</span><span class="sxs-lookup"><span data-stu-id="1d3f4-112">Quantity factors rely on product attributes.</span></span> <span data-ttu-id="1d3f4-113">为产品配置特定属性时，您可以将这些属性中的一小部分或全部标记为数量因子。</span><span class="sxs-lookup"><span data-stu-id="1d3f4-113">When you configure specific properties for a product, you can flag a subset of those properties, or all the properties, as quantity factors.</span></span>

<span data-ttu-id="1d3f4-114">Project Operations 将验证是否只有数值属性或具有数值数据类型的产品属性标记为数量因子。</span><span class="sxs-lookup"><span data-stu-id="1d3f4-114">Project Operations validates that only numeric properties or product properties that have a numeric data type are flagged as quantity factors.</span></span> <span data-ttu-id="1d3f4-115">在将具有配置的数量因子的产品添加到合同子项时，**数量** 字段将变为只读。</span><span class="sxs-lookup"><span data-stu-id="1d3f4-115">When a product with configured quantity factors is added to a contract line, the **Quantity** field  becomes read-only.</span></span> <span data-ttu-id="1d3f4-116">为充当数量因子的产品属性输入值之后，Project Operations 将计算合同子项的数量。</span><span class="sxs-lookup"><span data-stu-id="1d3f4-116">After you enter values for product properties that are quantity factors, Project Operations calculates the quantity of the contract line.</span></span>

<span data-ttu-id="1d3f4-117">例如，Dynamics 365 Sales 可能具有以下属性：</span><span class="sxs-lookup"><span data-stu-id="1d3f4-117">For example, Dynamics 365 Sales might have the following properties:</span></span>

- <span data-ttu-id="1d3f4-118">**用户数**：用户的数量。</span><span class="sxs-lookup"><span data-stu-id="1d3f4-118">**No of users**: The number of users.</span></span>
- <span data-ttu-id="1d3f4-119">**月数**：订阅的月数。</span><span class="sxs-lookup"><span data-stu-id="1d3f4-119">**No of Months**: The number of subscription months.</span></span>
- <span data-ttu-id="1d3f4-120">**产品 SKU**：产品的库存单位 (SKU)。</span><span class="sxs-lookup"><span data-stu-id="1d3f4-120">**Product SKU**: The stock keeping unit (SKU) for the product.</span></span>

<span data-ttu-id="1d3f4-121">可以通过编辑产品明细的属性，将 **用户数** 和 **月数** 属性标记为数量因子。</span><span class="sxs-lookup"><span data-stu-id="1d3f4-121">The **No of Users** and **No of Months** properties can be flagged as quantity factors by editing the properties of the product line.</span></span>

<span data-ttu-id="1d3f4-122">若要从产品属性创建数量因子，请完成以下步骤。</span><span class="sxs-lookup"><span data-stu-id="1d3f4-122">To create quantity factors from product properties, complete the following steps.</span></span>

1. <span data-ttu-id="1d3f4-123">在 **Project Operations** 中，选择 **销售-产品**。</span><span class="sxs-lookup"><span data-stu-id="1d3f4-123">On the **Project Operations**, select **Sales-Products**.</span></span>
2. <span data-ttu-id="1d3f4-124">打开需要设置数量因子的产品。</span><span class="sxs-lookup"><span data-stu-id="1d3f4-124">Open the product for which you need to set up quantity factors.</span></span> <span data-ttu-id="1d3f4-125">确保该产品已设置属性。</span><span class="sxs-lookup"><span data-stu-id="1d3f4-125">Make sure that the product has properties already set up.</span></span>
3. <span data-ttu-id="1d3f4-126">在 **项目信息** 页面上，选择 **数量因子** 选项卡。</span><span class="sxs-lookup"><span data-stu-id="1d3f4-126">On the **Project Information** page, select the **Quantity Factors** tab.</span></span>
4. <span data-ttu-id="1d3f4-127">在子网格中，选择 **+ 新建字段计算**。</span><span class="sxs-lookup"><span data-stu-id="1d3f4-127">In the subgrid, select **+ New field computation**.</span></span>
5. <span data-ttu-id="1d3f4-128">输入 **数量因子** 的名称，然后选择要映射到字段计算的属性值。</span><span class="sxs-lookup"><span data-stu-id="1d3f4-128">Enter the name of the **Quantity Factor** and select the property value that maps to the field computation.</span></span>
6. <span data-ttu-id="1d3f4-129">保存并关闭窗体。</span><span class="sxs-lookup"><span data-stu-id="1d3f4-129">Save and close the form.</span></span>
7. <span data-ttu-id="1d3f4-130">对将共同构成基于产品的合同子项的数量的所有属性重复步骤 2-6。</span><span class="sxs-lookup"><span data-stu-id="1d3f4-130">Repeat steps 2-6 for all the properties that together will make up the quantity for the product-based contract line.</span></span>

<span data-ttu-id="1d3f4-131">数量因子设置后，当用户为此产品创建合同子项时，合同子项的数量将锁定。</span><span class="sxs-lookup"><span data-stu-id="1d3f4-131">With quantity factors set up, when the user creates a contract line for this product, the quantity of the contract line is locked.</span></span> <span data-ttu-id="1d3f4-132">然后，会将此数量作为该合同子项的属性值的产品进行计算。</span><span class="sxs-lookup"><span data-stu-id="1d3f4-132">The quantity is then calculated as a product of the property values for that contract line.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]