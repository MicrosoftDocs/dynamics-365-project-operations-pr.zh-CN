---
title: 资源预估
description: 此主题提供有关在 Project Operations 中如何计算资源预估的信息。
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 2ebde2b3c5bcfb5faa02ee476065ac34b1953432
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/16/2020
ms.locfileid: "4072524"
---
# <a name="resource-estimates"></a><span data-ttu-id="566b3-103">资源预估</span><span class="sxs-lookup"><span data-stu-id="566b3-103">Resource estimates</span></span>

<span data-ttu-id="566b3-104">_**适用于：** 基于资源/非库存场景的 Project Operations，精简部署 - 估价开票交易_</span><span class="sxs-lookup"><span data-stu-id="566b3-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="566b3-105">资源预估来自工作分解结构中定义的分时段工作量以及适用的定价维度。</span><span class="sxs-lookup"><span data-stu-id="566b3-105">Resource estimates come from time-phased effort that is defined in the work breakdown structure along with applicable pricing dimensions.</span></span> <span data-ttu-id="566b3-106">通常，计算方式是 **每个角色的费率/小时 x 时数** 。</span><span class="sxs-lookup"><span data-stu-id="566b3-106">Typically, the calculation is **rate/hr for each role x hours.**</span></span> <span data-ttu-id="566b3-107">每个资源的分时段工作量存储在资源分配记录中。</span><span class="sxs-lookup"><span data-stu-id="566b3-107">The time-phased effort for each resource is stored in the resource assignment record.</span></span> <span data-ttu-id="566b3-108">定价存储在预定义的价目表中。</span><span class="sxs-lookup"><span data-stu-id="566b3-108">The pricing is stored in a pre-defined price list.</span></span> <span data-ttu-id="566b3-109">单位转换基于适用的价目表应用。</span><span class="sxs-lookup"><span data-stu-id="566b3-109">Unit conversion is applied based on the applicable price list.</span></span>

![资源预估](./media/navigation12.png)

## <a name="default-cost-price-and-cost-currency"></a><span data-ttu-id="566b3-111">默认成本费和成本货币</span><span class="sxs-lookup"><span data-stu-id="566b3-111">Default cost price and cost currency</span></span>

<span data-ttu-id="566b3-112">成本费默认为部门中的值。</span><span class="sxs-lookup"><span data-stu-id="566b3-112">Cost prices are defaulted from the Organizational Unit.</span></span>

## <a name="default-bill-rate-and-sales-currency"></a><span data-ttu-id="566b3-113">默认帐单费率和销售货币</span><span class="sxs-lookup"><span data-stu-id="566b3-113">Default bill rate and sales currency</span></span>

<span data-ttu-id="566b3-114">每笔交易应用一次售价。</span><span class="sxs-lookup"><span data-stu-id="566b3-114">Sales prices are applied once per deal.</span></span> <span data-ttu-id="566b3-115">销售价目表的默认层次结构如下：</span><span class="sxs-lookup"><span data-stu-id="566b3-115">The hierarchy for sale price list defaulting is as follows:</span></span>

1. <span data-ttu-id="566b3-116">组织</span><span class="sxs-lookup"><span data-stu-id="566b3-116">Organization</span></span>
2. <span data-ttu-id="566b3-117">客户</span><span class="sxs-lookup"><span data-stu-id="566b3-117">Customer</span></span>
3. <span data-ttu-id="566b3-118">报价单/合同</span><span class="sxs-lookup"><span data-stu-id="566b3-118">Quote/contract</span></span>
