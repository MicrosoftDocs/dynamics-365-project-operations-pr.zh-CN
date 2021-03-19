---
title: 设置目录产品的成本和销售费率 - 精简
description: 此主题提供有关如何设置产品目录中各项的成本和销售费率的信息。
author: rumant
manager: Annbe
ms.date: 10/09/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: f0941c549cc38f0938a5819e8cb6ca9912f14790
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/15/2021
ms.locfileid: "5274447"
---
# <a name="set-up-cost-and-sales-rates-for-catalog-products---lite"></a><span data-ttu-id="3a63f-103">设置目录产品的成本和销售费率 - 精简</span><span class="sxs-lookup"><span data-stu-id="3a63f-103">Set up cost and sales rates for catalog products - lite</span></span>

<span data-ttu-id="3a63f-104">_**适用于：** 精简部署 - 估价交易开票_</span><span class="sxs-lookup"><span data-stu-id="3a63f-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="3a63f-105">在 Dynamics 365 Project Operations 中设置产品目录项目的定价与 Dynamics 365 Sales 中相同。</span><span class="sxs-lookup"><span data-stu-id="3a63f-105">Setting up pricing for product catalog items in Dynamics 365 Project Operations is the same as in Dynamics 365 Sales.</span></span>

<span data-ttu-id="3a63f-106">在 Project Operations 中，无法在项目中估计或使用产品，因此无需在项目价目表上为报价单和合同设置产品目录价格。</span><span class="sxs-lookup"><span data-stu-id="3a63f-106">In Project Operations, products can't be estimated or used on projects, so product catalog prices don't need to be set on project price lists for quotes and contracts.</span></span>

<span data-ttu-id="3a63f-107">使用报价单、合同或客户的 **产品价格** 字段设置产品目录价格。</span><span class="sxs-lookup"><span data-stu-id="3a63f-107">Use the **Product Price** field of a quote, contract, or account to set up product catalog prices.</span></span> <span data-ttu-id="3a63f-108">不要在项目价目表中设置产品目录价格。</span><span class="sxs-lookup"><span data-stu-id="3a63f-108">Don't set up product catalog prices in the project price lists.</span></span> <span data-ttu-id="3a63f-109">项目价目表是 Project Operations 独有的。</span><span class="sxs-lookup"><span data-stu-id="3a63f-109">Project price lists are exclusive to Project Operations.</span></span> <span data-ttu-id="3a63f-110">特定于应用程序的业务逻辑将价目表从报价单复制到合同。</span><span class="sxs-lookup"><span data-stu-id="3a63f-110">Application-specific business logic copies the price lists from a quote to a contract.</span></span> <span data-ttu-id="3a63f-111">因此会生成特定于合同的项目价目表。</span><span class="sxs-lookup"><span data-stu-id="3a63f-111">The result is a contract-specific project price list.</span></span> <span data-ttu-id="3a63f-112">如果报价单上的项目价目表太大，复制操作可能会延迟报价单赢单流程。</span><span class="sxs-lookup"><span data-stu-id="3a63f-112">The copy operation can delay the quote win process if the project price list on the quote gets too large.</span></span> <span data-ttu-id="3a63f-113">不会复制产品价目表来在合同上创建自定义价目表。</span><span class="sxs-lookup"><span data-stu-id="3a63f-113">Product price lists aren't copied to create custom price lists on contracts.</span></span> <span data-ttu-id="3a63f-114">因为不涉及复制，所以报价单流程的性能不会受到影响。</span><span class="sxs-lookup"><span data-stu-id="3a63f-114">Because there's no copying involved, the performance of the quote process isn't affected.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]