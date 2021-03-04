---
title: 基于产品的合同子项成本核算 - 精简
description: 此主题提供有关创建的信息
author: rumant
manager: Annbe
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: a81c972f36179621f0547c24fc53d294485f638c
ms.sourcegitcommit: 2b74edd31f38410024a01124c9202a4d94464d04
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/17/2020
ms.locfileid: "4764448"
---
# <a name="cost-product-based-contract-lines---lite"></a><span data-ttu-id="0efe0-103">基于产品的合同子项成本核算 - 精简</span><span class="sxs-lookup"><span data-stu-id="0efe0-103">Cost product-based contract lines - lite</span></span>

<span data-ttu-id="0efe0-104">_**适用于：** 精简部署 - 估价交易开票_</span><span class="sxs-lookup"><span data-stu-id="0efe0-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="0efe0-105">Dynamics 365 Project Operations 中基于产品的合同子项包括 **成本费** 字段，该字段存储产品的成本费以用于下游利润率计算。</span><span class="sxs-lookup"><span data-stu-id="0efe0-105">Product-based contract lines in Dynamics 365 Project Operations include the **Cost Price** field, which stores the cost price of the product for downstream profitability calculations.</span></span>

<span data-ttu-id="0efe0-106">为目录产品创建基于产品的合同子项时，合同子项的成本默认来自产品目录中的 **标准成本** 字段。</span><span class="sxs-lookup"><span data-stu-id="0efe0-106">When a product-based contract line is created for a catalog product, the cost of the line defaults from the **Standard Cost** field in the product catalog.</span></span> <span data-ttu-id="0efe0-107">产品目录中的 **标准成本** 字段以组织的基础货币设置。</span><span class="sxs-lookup"><span data-stu-id="0efe0-107">The **Standard Cost** field in the product catalog is set up in the Organization's base currency.</span></span> <span data-ttu-id="0efe0-108">当单位成本默认为合同子项上的值时，它将转换为合同中的销售币种。</span><span class="sxs-lookup"><span data-stu-id="0efe0-108">When the unit cost defaults on the contract line, it's converted into the sales currency on the contract.</span></span>

## <a name="unit-cost-on-a-product-based-contract-line"></a><span data-ttu-id="0efe0-109">基于产品的合同子项中的单位成本</span><span class="sxs-lookup"><span data-stu-id="0efe0-109">Unit cost on a product-based contract line</span></span>

<span data-ttu-id="0efe0-110">在基于产品的合同子项中提供单位成本可以让一个单位的每个销售显示不同的产品成本。</span><span class="sxs-lookup"><span data-stu-id="0efe0-110">Having a unit cost on a product-based contract line allows for different product costs for each sale of a unit.</span></span> <span data-ttu-id="0efe0-111">虽然不是总是有必要这样做，但在某些情况下供应商可能会为客户提供打折的产品成本。</span><span class="sxs-lookup"><span data-stu-id="0efe0-111">While not always necessary, there are certain scenarios where the cost of the product may be discounted for the customer by the supplier.</span></span> <span data-ttu-id="0efe0-112">考虑以下情况：</span><span class="sxs-lookup"><span data-stu-id="0efe0-112">Consider the following scenario:</span></span>

<span data-ttu-id="0efe0-113">Fabrikam Robotics 正在 Adatum Corporation 的装配线上安装机械臂。</span><span class="sxs-lookup"><span data-stu-id="0efe0-113">Fabrikam Robotics is installing robotic arms at Adatum Corporation's assembly lines.</span></span> <span data-ttu-id="0efe0-114">Fabrikam 提供安装服务，但机械臂来自 Trey Research。</span><span class="sxs-lookup"><span data-stu-id="0efe0-114">Fabrikam provides installation services but the robotic arms are from Trey Research.</span></span> <span data-ttu-id="0efe0-115">如果在 Adatum Corporation 安装机械臂为 Trey Research 开辟了一个新的行业类别，那么他们可能为这笔交易向 Fabrikam 提供特殊折扣。</span><span class="sxs-lookup"><span data-stu-id="0efe0-115">If the installation of robotic arms at Adatum Corporation opens a new industry vertical for Trey Research, they could offer a special discount for this deal to Fabrikam.</span></span> <span data-ttu-id="0efe0-116">在这种情况下，Fabrikam 为机械臂创建了基于产品的合同子项。</span><span class="sxs-lookup"><span data-stu-id="0efe0-116">In this case, Fabrikam creates a product-based contract line for Robotic Arms.</span></span> <span data-ttu-id="0efe0-117">然后为此合同输入了单位成本。</span><span class="sxs-lookup"><span data-stu-id="0efe0-117">A per unit cost is entered for this contract.</span></span> <span data-ttu-id="0efe0-118">此成本与 Trey Research 机械臂的成本不同。</span><span class="sxs-lookup"><span data-stu-id="0efe0-118">The cost is different from the cost of robotic arms from Trey Research.</span></span>
