---
title: 设置目录产品的成本和销售费率
description: 此主题提供有关如何设置产品目录中各项的成本和销售费率的信息。
author: rumant
manager: Annbe
ms.date: 10/09/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: d5178a9143536bf4b2573403125325017861cdd5
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/16/2020
ms.locfileid: "4072671"
---
# <a name="set-up-cost-and-sales-rates-for-catalog-products"></a><span data-ttu-id="0a305-103">设置目录产品的成本和销售费率</span><span class="sxs-lookup"><span data-stu-id="0a305-103">Set up cost and sales rates for catalog products</span></span>

<span data-ttu-id="0a305-104">_**适用于：** 精简部署 - 估价交易开票_</span><span class="sxs-lookup"><span data-stu-id="0a305-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="0a305-105">在 Dynamics 365 Project Operations 中为产品目录项设置定价与在 Dynamics 365 Sales 中相同。</span><span class="sxs-lookup"><span data-stu-id="0a305-105">Setting up pricing for product catalog items in Dynamics 365 Project Operations is the same as in Dynamics 365 Sales.</span></span>

<span data-ttu-id="0a305-106">由于无法在 Project Operations 中的项目中估算或使用产品，因此无需在报价单和合同的项目价目表中设置产品目录价格。</span><span class="sxs-lookup"><span data-stu-id="0a305-106">Because products can't be estimated or used on projects in Project Operations, there is no need to set product catalog prices on project price lists for quotes and contracts.</span></span>

<span data-ttu-id="0a305-107">应在报价单、合同或客户的 **产品价格** 字段中设置产品目录价格。</span><span class="sxs-lookup"><span data-stu-id="0a305-107">Product catalog prices should be set up in the **Product Price** field of a quote, contract, or account.</span></span> <span data-ttu-id="0a305-108">不要在这些实体的项目价目表中设置产品目录价格。</span><span class="sxs-lookup"><span data-stu-id="0a305-108">Don't set up product catalog prices in the project price lists for these entities.</span></span> <span data-ttu-id="0a305-109">项目价目表是 Project Operations 独有的。</span><span class="sxs-lookup"><span data-stu-id="0a305-109">Project price lists are exclusive to Project Operations.</span></span> <span data-ttu-id="0a305-110">存在将价目表从报价单复制到合同的特定于应用程序的业务逻辑。</span><span class="sxs-lookup"><span data-stu-id="0a305-110">There is application-specific business logic that copies the price lists from a quote to a contract.</span></span> <span data-ttu-id="0a305-111">因此会生成特定于合同的项目价目表。</span><span class="sxs-lookup"><span data-stu-id="0a305-111">The result is a contract-specific project price list.</span></span> <span data-ttu-id="0a305-112">如果报价单上的项目价目表太大，复制操作可能会延迟报价单赢单流程。</span><span class="sxs-lookup"><span data-stu-id="0a305-112">The copy operation can delay the quote win process if the project price list on the quote gets too large.</span></span> <span data-ttu-id="0a305-113">不会复制产品价目表来在合同上创建自定义价目表。</span><span class="sxs-lookup"><span data-stu-id="0a305-113">Product price lists aren't copied to create custom price lists on contracts.</span></span> <span data-ttu-id="0a305-114">这意味着产品价目表不会影响报价单赢单流程的性能。</span><span class="sxs-lookup"><span data-stu-id="0a305-114">This means that product price lists don't impact the performance of the quote win process.</span></span>
