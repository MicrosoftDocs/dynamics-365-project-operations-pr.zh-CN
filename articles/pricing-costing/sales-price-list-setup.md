---
title: 设置销售价目表
description: 此主题提供用于项目定价的销售价目表的信息。
author: rumant
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 712dedb6766ff36181e261a66f3af99469449574
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/10/2021
ms.locfileid: "6004880"
---
# <a name="set-up-a-sales-price-list"></a><span data-ttu-id="1886d-103">设置销售价目表</span><span class="sxs-lookup"><span data-stu-id="1886d-103">Set up a sales price list</span></span>

<span data-ttu-id="1886d-104">_**适用于：** 基于资源/非库存场景的 Project Operations，精简部署 - 估价开票交易_</span><span class="sxs-lookup"><span data-stu-id="1886d-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="1886d-105">对于项目报价单和合同，项目价目表采用的价格替代模式与产品价目表采用的不同。</span><span class="sxs-lookup"><span data-stu-id="1886d-105">For project quotes and contracts, a project price list has a different price override pattern than a product price list.</span></span> <span data-ttu-id="1886d-106">在基于产品目录的报价单明细中，可以直接替代报价单明细中角色和类别的价格，因为每项报价单明细都正好指向一个目录项。</span><span class="sxs-lookup"><span data-stu-id="1886d-106">On a product catalog–based quote line, you can override the price to roles and categories directly on the quote line, because each quote line points to exactly one catalog item.</span></span> <span data-ttu-id="1886d-107">但是，在基于项目的报价单明细中，不能直接替代报价单明细中的角色和类别的价格。</span><span class="sxs-lookup"><span data-stu-id="1886d-107">However, on a project-based quote line, you can't override the price to roles and categories directly on the quote line.</span></span> <span data-ttu-id="1886d-108">您可以使用项目价目表来使用两种不同的替代模式。</span><span class="sxs-lookup"><span data-stu-id="1886d-108">You can use the project price list to work with the two distinct override patterns.</span></span>

> [!NOTE]
> <span data-ttu-id="1886d-109">建议您为项目资源和目录项设置单独的价目表，因为在您替代定价时，这两者的行为不同。</span><span class="sxs-lookup"><span data-stu-id="1886d-109">We recommend that you have a separate price list for your project resources and your catalog items, because of the behavior differences between the two when you override pricing.</span></span>

<span data-ttu-id="1886d-110">对于项目定价，下面的每个实体可以有一个或多个关联的销售价目表：</span><span class="sxs-lookup"><span data-stu-id="1886d-110">Each of the following entities can have one or more associated sales price lists for project pricing:</span></span>

- <span data-ttu-id="1886d-111">客户（帐户）</span><span class="sxs-lookup"><span data-stu-id="1886d-111">Customer (account)</span></span> 
- <span data-ttu-id="1886d-112">商机</span><span class="sxs-lookup"><span data-stu-id="1886d-112">Opportunity</span></span> 
- <span data-ttu-id="1886d-113">报价单</span><span class="sxs-lookup"><span data-stu-id="1886d-113">Quote</span></span> 
- <span data-ttu-id="1886d-114">项目合同</span><span class="sxs-lookup"><span data-stu-id="1886d-114">Project Contract</span></span>

<span data-ttu-id="1886d-115">这些实体与价目表之间的关联通过项目价目表指示。</span><span class="sxs-lookup"><span data-stu-id="1886d-115">The association of these entities with a price list is indicated by the project price lists.</span></span> <span data-ttu-id="1886d-116">可以将一个或多个价目表与客户、商机、报价单和项目合同销售实体关联。</span><span class="sxs-lookup"><span data-stu-id="1886d-116">You can associate one or more price lists with the Customer, Opportunity, Quote, and Project Contract sales entities.</span></span>

<span data-ttu-id="1886d-117">不会在客户记录中自动输入默认项目价目表。</span><span class="sxs-lookup"><span data-stu-id="1886d-117">A default project price list isn't automatically entered on a customer record.</span></span> <span data-ttu-id="1886d-118">但是，可以手动向客户记录附加项目价目表。</span><span class="sxs-lookup"><span data-stu-id="1886d-118">However, you can manually attach a project price list to the customer record.</span></span> <span data-ttu-id="1886d-119">尽管如此，还是仅当与客户之间存在自定义定价协议时，才应手动附加项目价目表。</span><span class="sxs-lookup"><span data-stu-id="1886d-119">Nevertheless, you should manually attach a project price list only when you have a custom pricing agreement with the customer.</span></span> 

<span data-ttu-id="1886d-120">如果向销售实体附加项目价目表，将验证以下信息：</span><span class="sxs-lookup"><span data-stu-id="1886d-120">When a project price list is attached to a sales entity, the following information is validated:</span></span>

- <span data-ttu-id="1886d-121">价目表有 **销售** 上下文。</span><span class="sxs-lookup"><span data-stu-id="1886d-121">The price list has a context of **Sales**.</span></span> 
- <span data-ttu-id="1886d-122">价目表货币与客户货币匹配。</span><span class="sxs-lookup"><span data-stu-id="1886d-122">The price list currency matches the customer currency.</span></span> 

<span data-ttu-id="1886d-123">在项目合同中，以下优先顺序用于自动设置相关项目价目表：</span><span class="sxs-lookup"><span data-stu-id="1886d-123">On a project contract, the following order of precedence is used to automatically set related project price lists:</span></span>

1. <span data-ttu-id="1886d-124">报价单</span><span class="sxs-lookup"><span data-stu-id="1886d-124">Quote</span></span>
2. <span data-ttu-id="1886d-125">商机​​</span><span class="sxs-lookup"><span data-stu-id="1886d-125">Opportunity</span></span>
3. <span data-ttu-id="1886d-126">客户</span><span class="sxs-lookup"><span data-stu-id="1886d-126">Customer</span></span> 
4. <span data-ttu-id="1886d-127">全局设置</span><span class="sxs-lookup"><span data-stu-id="1886d-127">Global settings</span></span> 

<span data-ttu-id="1886d-128">默认输入项目价目表时，系统将验证货币是否匹配客户的货币，以及已输入的默认价目表是否有 **销售** 上下文。</span><span class="sxs-lookup"><span data-stu-id="1886d-128">When a project price list is entered by default, the system validates that the currency matches the customer’s currency, and that the default price lists that have been entered have a context of **Sales**.</span></span>

<span data-ttu-id="1886d-129">可以将多个项目价目表与客户、商机、报价单和项目合同实体关联。</span><span class="sxs-lookup"><span data-stu-id="1886d-129">You can associate multiple project price lists with the Customer, Opportunity, Quote, and Project Contract entities.</span></span> <span data-ttu-id="1886d-130">此功能支持为长期开展的项目合同设置特定于日期的默认价格，在此情况下，可能需要多个价目表来纳入通货膨胀导致的价格更新。</span><span class="sxs-lookup"><span data-stu-id="1886d-130">This capability supports date-specific default prices for a long-running project contract, where you might require more than one price list to account for price updates that occur because of inflation.</span></span> <span data-ttu-id="1886d-131">但是，如果与客户、商机、报价单或项目合同实体关联的价目表存在重合时效，默认价格可能不正确。</span><span class="sxs-lookup"><span data-stu-id="1886d-131">However, if the price lists that you associate with the Customer, Opportunity, Quote, or Project Contract entity have overlapping date effectivity, the default prices might be incorrect.</span></span> <span data-ttu-id="1886d-132">因此，应确保不将具有重合时效的项目价目表与这些实体关联。</span><span class="sxs-lookup"><span data-stu-id="1886d-132">Therefore, you should make sure that project price lists that have overlapping date effectivity aren't associated with those entities.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]