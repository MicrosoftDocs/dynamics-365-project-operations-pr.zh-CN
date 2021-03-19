---
title: 作为定价维度的 Project Operations 字段
description: 本主题提供有关在 Dynamics 365 Project Operations 中使用字段作为定价维度的信息。
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
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
ms.openlocfilehash: 04b823e8237590a294ed0706e64d0ecb9d2cf56f
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/15/2021
ms.locfileid: "5274627"
---
# <a name="project-operations-fields-as-pricing-dimensions"></a><span data-ttu-id="28490-103">作为定价维度的 Project Operations 字段</span><span class="sxs-lookup"><span data-stu-id="28490-103">Project Operations fields as pricing dimensions</span></span>

<span data-ttu-id="28490-104">_**适用于：** 基于资源/非库存场景的 Project Operations，精简部署 - 估价开票交易_</span><span class="sxs-lookup"><span data-stu-id="28490-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="28490-105">**实际值** 实体有很多字段可以用作基于资源的定价的定价维度。</span><span class="sxs-lookup"><span data-stu-id="28490-105">The **Actuals** entity has many fields that can be used as pricing dimensions for resource-based pricing.</span></span> <span data-ttu-id="28490-106">例如，一个常用字段为 **可预订资源**。</span><span class="sxs-lookup"><span data-stu-id="28490-106">For example, one common field is **Bookable Resource**.</span></span> <span data-ttu-id="28490-107">可记帐资源少于 20-30 个的小型公司可能会发现采用特定于每个资源的记帐费率和成本费率这种方法更简单。</span><span class="sxs-lookup"><span data-stu-id="28490-107">Smaller companies that have fewer than 20-30 billable resources may find that having bill and cost rates specific to each resource is a simpler approach.</span></span> <span data-ttu-id="28490-108">不过，随着可记帐员工数量增多，维护资源特定费率可能不切实际。</span><span class="sxs-lookup"><span data-stu-id="28490-108">However, as the billable workforce grows, resource-secific rates could become unrealistic to maintain.</span></span> <span data-ttu-id="28490-109">资源成本和记帐费率随着资源升职、获得更多经验或掌握其他技能而开始发生变化。</span><span class="sxs-lookup"><span data-stu-id="28490-109">Resource cost and bill rates begin to vary as resources get promoted, gain more experience, or acquire a different set of skills.</span></span> 

<span data-ttu-id="28490-110">另一个示例是交易类别的。</span><span class="sxs-lookup"><span data-stu-id="28490-110">Another example is that of transaction category.</span></span> <span data-ttu-id="28490-111">客户和实施者已使用交易类别为工作分类和使用此字段根据工作类别定价和设置成本。</span><span class="sxs-lookup"><span data-stu-id="28490-111">Customers and Implementers have used the transaction category to classify work and use the field to price and cost based on the category of work.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]