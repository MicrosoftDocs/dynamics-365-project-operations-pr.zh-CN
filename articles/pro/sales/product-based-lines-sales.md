---
title: 基于产品的商机明细
description: 此主题提供有关 Project Operations 中基于产品的商机明细项目的信息。
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 17ffcf8dc94d42102115281d281d6b553cf1fa17
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/28/2020
ms.locfileid: "3896225"
---
# <a name="product-based-opportunity-lines"></a><span data-ttu-id="16b8f-103">基于产品的商机明细</span><span class="sxs-lookup"><span data-stu-id="16b8f-103">Product-based opportunity lines</span></span>

<span data-ttu-id="16b8f-104">_**适用于：** 精简部署 - 估价交易开票_</span><span class="sxs-lookup"><span data-stu-id="16b8f-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="16b8f-105">基于产品的商机明细是商机中的明细项目。</span><span class="sxs-lookup"><span data-stu-id="16b8f-105">Product-based opportunity lines are line items on the Opportunity.</span></span> <span data-ttu-id="16b8f-106">这些明细将在最终发票上作为不同明细项目交付给客户，没有任何其他增值服务。</span><span class="sxs-lookup"><span data-stu-id="16b8f-106">These lines are delivered to the customer as distinct line items on the eventual invoice without any other value-added services.</span></span> <span data-ttu-id="16b8f-107">不会在任何相关项目的任务中跟踪相关的花费和使用。</span><span class="sxs-lookup"><span data-stu-id="16b8f-107">The associated spend and consumption isn't tracked on tasks of any related projects.</span></span>

<span data-ttu-id="16b8f-108">基于产品的明细可以是目录项或目录外产品。</span><span class="sxs-lookup"><span data-stu-id="16b8f-108">Product-based lines can be catalog items or write-in products.</span></span> <span data-ttu-id="16b8f-109">商机的基于产品的明细中的大多数功能都与 Dynamics 365 Sales 应用程序提供的功能相同。</span><span class="sxs-lookup"><span data-stu-id="16b8f-109">Most of the functionality on an Opportunity's product-based lines follows the functionality provided by the Dynamics 365 Sales application.</span></span> <span data-ttu-id="16b8f-110">有关基于产品的商机明细的详细信息，请参阅[为商机添加产品](https://docs.microsoft.com/dynamics365/sales-enterprise/add-products-opportunity)。</span><span class="sxs-lookup"><span data-stu-id="16b8f-110">For more information about product-based opportunity lines, see [Add products to an opportunity](https://docs.microsoft.com/dynamics365/sales-enterprise/add-products-opportunity).</span></span>

<span data-ttu-id="16b8f-111">有关特定于基于项目的商机的基于产品的商机明细的一个概念是**客户预算**。</span><span class="sxs-lookup"><span data-stu-id="16b8f-111">One concept about product-based opportunity lines that is specific to project-based opportunities is **Customer Budget**.</span></span> <span data-ttu-id="16b8f-112">使用此字段可以跟踪客户愿意为此明细项目支付的金额。</span><span class="sxs-lookup"><span data-stu-id="16b8f-112">Use this field to track the amount the customer is willing to pay for the line item.</span></span>

<span data-ttu-id="16b8f-113">如果商机摘要的收入方法设置为**系统计算**，基于产品和基于项目的明细中的客户预算值将被汇总以计算预计收入。</span><span class="sxs-lookup"><span data-stu-id="16b8f-113">If the revenue method of the Opportunity summary is set to **System Calculated**, the customer budget values across product- and project-based lines are summarized to calculate the estimated revenue.</span></span>
