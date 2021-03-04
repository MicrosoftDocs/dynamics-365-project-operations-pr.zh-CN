---
title: 基于产品的商机明细 - 精简
description: 此主题提供有关 Project Operations 中基于产品的商机明细项目的信息。
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: b826bf3a1320eee2758af7a094e9f1c2eac6a119
ms.sourcegitcommit: 2b74edd31f38410024a01124c9202a4d94464d04
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/17/2020
ms.locfileid: "4764943"
---
# <a name="product-based-opportunity-lines---lite"></a><span data-ttu-id="7769e-103">基于产品的商机明细 - 精简</span><span class="sxs-lookup"><span data-stu-id="7769e-103">Product-based opportunity lines - lite</span></span>

<span data-ttu-id="7769e-104">_**适用于：** 精简部署 - 估价交易开票_</span><span class="sxs-lookup"><span data-stu-id="7769e-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="7769e-105">基于产品的商机明细是商机中的明细项目。</span><span class="sxs-lookup"><span data-stu-id="7769e-105">Product-based opportunity lines are line items on the Opportunity.</span></span> <span data-ttu-id="7769e-106">这些不同的明细项目位于提供给客户的最终发票上。</span><span class="sxs-lookup"><span data-stu-id="7769e-106">These distinct line items are on the eventual invoice that is provided to the customer.</span></span> <span data-ttu-id="7769e-107">此发票不包含任何其他服务。</span><span class="sxs-lookup"><span data-stu-id="7769e-107">The invoice doesn't include any other additional services.</span></span> <span data-ttu-id="7769e-108">不会在任何相关项目的任务中跟踪相关的花费和使用。</span><span class="sxs-lookup"><span data-stu-id="7769e-108">The associated spend and consumption isn't tracked on tasks of any related projects.</span></span>

<span data-ttu-id="7769e-109">基于产品的明细可以是目录项或目录外产品。</span><span class="sxs-lookup"><span data-stu-id="7769e-109">Product-based lines can be catalog items or write-in products.</span></span> <span data-ttu-id="7769e-110">商机的基于产品的明细中的大多数功能都与 Dynamics 365 Sales 应用程序提供的功能相同。</span><span class="sxs-lookup"><span data-stu-id="7769e-110">Most of the functionality on an Opportunity's product-based lines follows the functionality provided by the Dynamics 365 Sales application.</span></span> <span data-ttu-id="7769e-111">有关基于产品的商机明细的详细信息，请参阅[为商机添加产品](https://docs.microsoft.com/dynamics365/sales-enterprise/add-products-opportunity)。</span><span class="sxs-lookup"><span data-stu-id="7769e-111">For more information about product-based opportunity lines, see [Add products to an opportunity](https://docs.microsoft.com/dynamics365/sales-enterprise/add-products-opportunity).</span></span>

<span data-ttu-id="7769e-112">**客户预算** 是一个特定于基于项目的商机明细的概念。</span><span class="sxs-lookup"><span data-stu-id="7769e-112">**Customer budget** is a concept that is specific to project-based opportunity lines.</span></span> <span data-ttu-id="7769e-113">**客户预算** 字段跟踪客户要为项目支付的金额。</span><span class="sxs-lookup"><span data-stu-id="7769e-113">The **Customer budget** field tracks the amount the customer is willing to pay for the item.</span></span>

<span data-ttu-id="7769e-114">当商机摘要的收入方法为 **系统计算** 时，将汇总商机明细中的客户预算值来计算估计收入。</span><span class="sxs-lookup"><span data-stu-id="7769e-114">When the revenue method of the Opportunity summary is **System Calculated**, the customer budget values across the opportunity lines are summarized to calculate the estimated revenue.</span></span> 

