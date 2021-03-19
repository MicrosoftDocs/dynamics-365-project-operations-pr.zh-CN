---
title: 默认价目表
description: 此主题提供有关 Project Operations 中的默认销售和成本价目表的信息。
author: rumant
manager: Annbe
ms.date: 10/13/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 04c97429ab8ac769dd22b4127432d80de8fde937
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/15/2021
ms.locfileid: "5275572"
---
# <a name="default-price-lists"></a><span data-ttu-id="2f13f-103">默认价目表</span><span class="sxs-lookup"><span data-stu-id="2f13f-103">Default price lists</span></span>

<span data-ttu-id="2f13f-104">_**适用于：** 基于资源/非库存场景的 Project Operations，精简部署 - 估价开票交易_</span><span class="sxs-lookup"><span data-stu-id="2f13f-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

## <a name="sales-price-lists"></a><span data-ttu-id="2f13f-105">销售价目表</span><span class="sxs-lookup"><span data-stu-id="2f13f-105">Sales price lists</span></span>

<span data-ttu-id="2f13f-106">Dynamics 365 Project Operations 中的每个项目报价单和合同都包含一个默认销售价目表。</span><span class="sxs-lookup"><span data-stu-id="2f13f-106">Every project quote and contract in Dynamics 365 Project Operations contains a default sales price list.</span></span> 

### <a name="price-list-default-on-project-quotes"></a><span data-ttu-id="2f13f-107">项目报价单上的默认价目表</span><span class="sxs-lookup"><span data-stu-id="2f13f-107">Price list default on project quotes</span></span>
<span data-ttu-id="2f13f-108">系统将完成以下过程来确定项目报价单上默认使用哪个价目表：</span><span class="sxs-lookup"><span data-stu-id="2f13f-108">The system completes the following process to determine which price list to default on a project quote:</span></span>

1. <span data-ttu-id="2f13f-109">系统查看附加到客户的项目价目表中的价目表。</span><span class="sxs-lookup"><span data-stu-id="2f13f-109">The system looks at the price lists that are attached to the account's project price lists.</span></span> 
2. <span data-ttu-id="2f13f-110">如果客户记录中附加了项目价目表，系统会查看附加到项目参数与项目报价单的货币相匹配的销售价目表。</span><span class="sxs-lookup"><span data-stu-id="2f13f-110">If there are project price lists attached to the account record, the system looks at the sales price lists attached to the project parameters that match the currency of the project quote.</span></span>
3. <span data-ttu-id="2f13f-111">接下来，系统检查与项目报价单的日期范围匹配的价目表的时效。</span><span class="sxs-lookup"><span data-stu-id="2f13f-111">Next, the system checks the date effectivity of the price lists that match the date range of the project quote.</span></span> <span data-ttu-id="2f13f-112">特别是创建报价单的日期。</span><span class="sxs-lookup"><span data-stu-id="2f13f-112">Specifically, the date the quote was created.</span></span>
4. <span data-ttu-id="2f13f-113">如果有多个价目表对项目报价单的日期有效，项目报价单上将默认显示所有价目表。</span><span class="sxs-lookup"><span data-stu-id="2f13f-113">If there are multiple price lists that are effective for the date of the project quote, all of the price lists default on the project quote.</span></span>
5. <span data-ttu-id="2f13f-114">如果没有对项目报价单的日期有效的价目表，项目报价单上则没有默认项目价目表。</span><span class="sxs-lookup"><span data-stu-id="2f13f-114">If no price lists in effect for the date of the project quote, there's no default project price list on the project quote.</span></span> <span data-ttu-id="2f13f-115">项目报价单上将出现一条警告消息。</span><span class="sxs-lookup"><span data-stu-id="2f13f-115">A warning message will occur on the project quote.</span></span> <span data-ttu-id="2f13f-116">此消息指出，由于没有附加项目价目表，不会对您的项目中的实际值和估计值定价。</span><span class="sxs-lookup"><span data-stu-id="2f13f-116">The message states that actuals and estimates on the project won't be priced because there are no project price lists attached.</span></span>

### <a name="price-list-default-on-project-contracts"></a><span data-ttu-id="2f13f-117">项目合同上的默认价目表</span><span class="sxs-lookup"><span data-stu-id="2f13f-117">Price list default on project contracts</span></span> 
<span data-ttu-id="2f13f-118">系统将完成以下过程来确定项目合同上默认使用哪个价目表：</span><span class="sxs-lookup"><span data-stu-id="2f13f-118">The system completes the following process to determine which price list to default on a project contract:</span></span>

1. <span data-ttu-id="2f13f-119">如果合同是从报价单创建的，将会单独复制报价单上的项目价目表，并附加到项目合同中。</span><span class="sxs-lookup"><span data-stu-id="2f13f-119">If the contract is created from a quote, the project price lists on the quote are copied over separately and attached to the project contract.</span></span>
2. <span data-ttu-id="2f13f-120">如果合同是从头创建的，系统将查看附加到客户的项目价目表的价目表。</span><span class="sxs-lookup"><span data-stu-id="2f13f-120">If the contract is created from scratch, the system looks at the price lists that are attached to the project price lists of the account.</span></span> <span data-ttu-id="2f13f-121">如果客户记录中未附加项目价目表，系统会查找附加到项目参数与项目合同的货币相匹配的销售价目表。</span><span class="sxs-lookup"><span data-stu-id="2f13f-121">If there aren't project price lists attached to the account record, the system looks for sales price lists attached to the project parameters that match the currency of the project contract.</span></span>
4. <span data-ttu-id="2f13f-122">接下来，系统检查与项目合同的日期范围匹配的价目表的时效。</span><span class="sxs-lookup"><span data-stu-id="2f13f-122">Next, the system checks the date effectivity of the price lists that match the date range of the project contract.</span></span> <span data-ttu-id="2f13f-123">特别是创建合同的日期。</span><span class="sxs-lookup"><span data-stu-id="2f13f-123">Specifically, the date the contract was created.</span></span>
5. <span data-ttu-id="2f13f-124">如果有多个价目表对项目合同的日期有效，项目合同上将默认显示所有价目表。</span><span class="sxs-lookup"><span data-stu-id="2f13f-124">If there are multiple price lists that are effective for the date of the contract, all of the price lists default on the contract.</span></span>
6. <span data-ttu-id="2f13f-125">如果没有对合同的日期有效的价目表，则不会有项目价目表在合同上默认显示。</span><span class="sxs-lookup"><span data-stu-id="2f13f-125">If there are no price lists in effect for the date of the contract, no project price lists default to the contract.</span></span> <span data-ttu-id="2f13f-126">项目合同上将出现一条警告消息。</span><span class="sxs-lookup"><span data-stu-id="2f13f-126">A warning message will occur on the project contract.</span></span> <span data-ttu-id="2f13f-127">此消息指出，由于没有附加项目价目表，不会对您的项目中的实际值和估计值定价。</span><span class="sxs-lookup"><span data-stu-id="2f13f-127">The message states that actuals and estimates on the project won't be priced because there are no project price lists attached.</span></span>

## <a name="cost-price-lists"></a><span data-ttu-id="2f13f-128">成本价目表</span><span class="sxs-lookup"><span data-stu-id="2f13f-128">Cost price lists</span></span>

<span data-ttu-id="2f13f-129">在 Project Operations 中，成本价目表不会默认显示在任何实体中。</span><span class="sxs-lookup"><span data-stu-id="2f13f-129">Cost price lists don't default to any entity in Project Operations.</span></span> <span data-ttu-id="2f13f-130">确定用于项目成本的成本价目表始终在当下完成。</span><span class="sxs-lookup"><span data-stu-id="2f13f-130">Determining the cost price list to use for project costs is always done in the moment.</span></span> <span data-ttu-id="2f13f-131">系统将完成以下过程来确定哪个价目表用于项目成本：</span><span class="sxs-lookup"><span data-stu-id="2f13f-131">The system completes the following process to determine which price list to use for project costs:</span></span>

1. <span data-ttu-id="2f13f-132">系统首先查看附加到项目的合同签订部门的价目表。</span><span class="sxs-lookup"><span data-stu-id="2f13f-132">The system first looks at the price lists that are attached to the contracting organization unit of the project.</span></span>
2. <span data-ttu-id="2f13f-133">然后，系统查看与传入的估计值或实际值明细匹配的价目表的时效。</span><span class="sxs-lookup"><span data-stu-id="2f13f-133">The system then looks at the date effectivity of the price lists that match the date of the incoming estimate or actual line.</span></span> <span data-ttu-id="2f13f-134">在此情况下，*估计值明细* 引用 Project Operations 中的全部三个估计上下文：</span><span class="sxs-lookup"><span data-stu-id="2f13f-134">In this situation, *estimate line* refers to all three contexts of estimation in Project Operations:</span></span>

    - <span data-ttu-id="2f13f-135">项目估计值明细</span><span class="sxs-lookup"><span data-stu-id="2f13f-135">Project estimate line</span></span>
    - <span data-ttu-id="2f13f-136">报价单明细详细信息</span><span class="sxs-lookup"><span data-stu-id="2f13f-136">Quote line detail</span></span>
    - <span data-ttu-id="2f13f-137">合同子项详细信息</span><span class="sxs-lookup"><span data-stu-id="2f13f-137">Contract line detail</span></span>
  
3. <span data-ttu-id="2f13f-138">如果有多个价目表对于传入估计值或实际值中的日期有效，将选择最近创建的价目表。</span><span class="sxs-lookup"><span data-stu-id="2f13f-138">If there are multiple price lists that are effective for the date on the incoming estimate or actual, the price list created most recently is selected.</span></span>
4. <span data-ttu-id="2f13f-139">如果项目的合同签订部门没有附加价目表，系统会查看附加到项目参数与项目的货币相匹配的成本价目表。</span><span class="sxs-lookup"><span data-stu-id="2f13f-139">If there no price lists attached to the contracting organization unit of the project, the system looks at cost price lists attached to project parameters that match the currency of the project.</span></span>
5. <span data-ttu-id="2f13f-140">接下来，系统查看与传入的估计值或实际值明细匹配的价目表的时效。</span><span class="sxs-lookup"><span data-stu-id="2f13f-140">Next the system looks at the date effectivity of the price lists that match the date of the incoming estimate or actual line.</span></span> 
6. <span data-ttu-id="2f13f-141">如果有多个价目表对于传入估计值或实际值中的日期有效，将选择最近创建的价目表。</span><span class="sxs-lookup"><span data-stu-id="2f13f-141">If there are multiple price lists that are effective for the date on the incoming estimate or actual, the price list created most recently is selected.</span></span>
7. <span data-ttu-id="2f13f-142">如果没有附加到项目参数与货币和生效日期匹配的成本价目表，系统会在传入的估计值或实际值明细中将成本费率默认为零 (0)。</span><span class="sxs-lookup"><span data-stu-id="2f13f-142">If there are no cost price lists attached to the project parameters that match the currency and effective date, the system defaults the cost rate to zero (0) on the incoming estimate or actual line.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]