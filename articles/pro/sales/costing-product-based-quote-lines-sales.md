---
title: 基于产品的报价单明细成本核算
description: 此主题提供有关将成本费应用于基于产品的报价单明细的信息。
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: d21ab159294cac66ffeb8abcf0943b4babd7b360
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/28/2020
ms.locfileid: "4118912"
---
# <a name="costing-product-based-quote-lines"></a><span data-ttu-id="46fc6-103">基于产品的报价单明细成本核算</span><span class="sxs-lookup"><span data-stu-id="46fc6-103">Costing product-based quote lines</span></span>

<span data-ttu-id="46fc6-104">_**适用于：** 基于资源/非库存场景的 Project Operations，精简部署 - 估价开票交易_</span><span class="sxs-lookup"><span data-stu-id="46fc6-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="46fc6-105">Dynamics 365 Project Operations 中基于产品的报价单明细也包含 **成本费** 字段。</span><span class="sxs-lookup"><span data-stu-id="46fc6-105">Product-based quote lines in Dynamics 365 Project Operations also have a **Cost Price** field.</span></span> <span data-ttu-id="46fc6-106">此字段用于在报价单明细中跟踪产品的成本费，并用于下游利润率的计算。</span><span class="sxs-lookup"><span data-stu-id="46fc6-106">This field is used to track the cost price for the product on the quote line and for downstream profitability calculations.</span></span>

<span data-ttu-id="46fc6-107">为目录产品创建基于产品的报价单明细时，基于产品的报价单明细的成本默认为产品目录中 **标准成本** 字段的值。</span><span class="sxs-lookup"><span data-stu-id="46fc6-107">When a product-based quote line is created for a catalog product, the cost of the product-based quote line is defaulted from the **Standard Cost** field in the product catalog.</span></span> <span data-ttu-id="46fc6-108">产品目录中的“标准成本”字段以组织的基础货币设置。</span><span class="sxs-lookup"><span data-stu-id="46fc6-108">The standard cost field in the product catalog is set up in the Organization's base currency.</span></span> <span data-ttu-id="46fc6-109">基于产品的报价单明细上的默认单位成本将转换为报价单上的销售货币。</span><span class="sxs-lookup"><span data-stu-id="46fc6-109">The default unit cost on the product-based quote line is converted to the sales currency on the quote.</span></span>

## <a name="unit-cost-on-a-product-based-quote-line"></a><span data-ttu-id="46fc6-110">基于产品的报价单明细中的单位成本</span><span class="sxs-lookup"><span data-stu-id="46fc6-110">Unit cost on a product-based quote line</span></span>

<span data-ttu-id="46fc6-111">在基于产品的报价单明细中提供单位成本的目的是为了让每个销售的产品显示不同的成本。</span><span class="sxs-lookup"><span data-stu-id="46fc6-111">The purpose of having a unit cost on a product-based quote line is to allow for different costs for a product for each sale.</span></span> <span data-ttu-id="46fc6-112">这不是一个典型场景，但有时供应商可能根据最终销售的客户为产品成本提供折扣。</span><span class="sxs-lookup"><span data-stu-id="46fc6-112">This is not a typical scenario, but sometimes the cost of the product may be discounted by the supplier depending on the customer of the final sale.</span></span>

<span data-ttu-id="46fc6-113">例如：</span><span class="sxs-lookup"><span data-stu-id="46fc6-113">For example:</span></span>

<span data-ttu-id="46fc6-114">Fabrikam Robotics 正在 A Datum Corporation 的装配线上安装机械臂。</span><span class="sxs-lookup"><span data-stu-id="46fc6-114">Fabrikam Robotics is installing robotic arms at A Datum Corporation's assembly lines.</span></span> <span data-ttu-id="46fc6-115">Fabrikam 提供安装服务，但机械臂需要从 Trey 机器人公司购买。</span><span class="sxs-lookup"><span data-stu-id="46fc6-115">Fabrikam provides installation services but the robotic arms are procured from Trey robotics.</span></span> <span data-ttu-id="46fc6-116">如果在 A Datum Corporation 安装机械臂为 Trey 的机械臂开辟了一个新的行业类别，那么 Trey 可能为这笔交易给予 Fabrikam 特殊折扣。</span><span class="sxs-lookup"><span data-stu-id="46fc6-116">If the installation of robotic arms at A Datum Corporation opens a new industry vertical for Trey's robotic arms, Trey could give a special discount for this deal to Fabrikam.</span></span>

<span data-ttu-id="46fc6-117">在这种情况下，Fabrikam 将为机械臂创建基于产品的报价单明细，并为此报价单输入特殊的每单位成本。</span><span class="sxs-lookup"><span data-stu-id="46fc6-117">In this case, Fabrikam will create product-based quote line for Robotic Arms and input a special per unit cost for this quote.</span></span> <span data-ttu-id="46fc6-118">此成本与 Trey 机械臂的标准成本不同。</span><span class="sxs-lookup"><span data-stu-id="46fc6-118">This cost is different from the standard cost of Trey Robotic Arms.</span></span>