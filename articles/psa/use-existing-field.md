---
title: 将 Project Service 中的现有字段用作定价维度
description: 此主题介绍如何将现有 Project Service 字段用作定价维度。
author: Rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 11/19/2018
ms.topic: article
ms.service: business-applications
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: ad03f5f7c1c9e93ca12a8c8d48ffbd2f80b1511f
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/15/2021
ms.locfileid: "5281557"
---
# <a name="use-an-existing-field-in-project-service-as-a-pricing-dimension"></a><span data-ttu-id="a9a19-103">将 Project Service 中的现有字段用作定价维度</span><span class="sxs-lookup"><span data-stu-id="a9a19-103">Use an existing field in Project Service as a pricing dimension</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="a9a19-104">Project Service Automation (PSA) 在 **实际值** 实体中有大量字段，可在项目组织中用作基于资源的定价的定价维度。</span><span class="sxs-lookup"><span data-stu-id="a9a19-104">Project Service Automation (PSA) has many fields on the **Actuals** entity that can be used as pricing dimensions for resource-based pricing in project organizations.</span></span> <span data-ttu-id="a9a19-105">例如，一个常用字段为 **可预订资源**。</span><span class="sxs-lookup"><span data-stu-id="a9a19-105">For example, one common field is **Bookable Resource**.</span></span> <span data-ttu-id="a9a19-106">可记帐资源少于 20-30 个的小型公司可能会发现采用特定于每个资源的记帐费率和成本费率这种方法更简单。</span><span class="sxs-lookup"><span data-stu-id="a9a19-106">Smaller companies that have fewer than 20-30 billable resources may find that having bill and cost rates specific to each resource is a simpler approach.</span></span> <span data-ttu-id="a9a19-107">但是，随着可记帐员工数量增多，特定费率可能变得不现实，因为随着资源升级，经验增多或获得其他技能集，资源成本和记帐费率会开始变化。</span><span class="sxs-lookup"><span data-stu-id="a9a19-107">However, as the billable workforce grows, specific rates could become unrealistic to maintain as resource cost and bill rates begin to vary as resources get promoted, gain more experience, or acquire a different skill set.</span></span> <span data-ttu-id="a9a19-108">因为这种方法仍然适用于一定规模的公司，所以请参阅[将可预订资源用作定价维度](bookable-resource-pricing-dimension.md)了解如何将现有 Project Service 字段用作定价维度。</span><span class="sxs-lookup"><span data-stu-id="a9a19-108">Because this approach still works for companies of a certain size, see [Use a bookable resource as a pricing dimension](bookable-resource-pricing-dimension.md) to understand how an existing Project Service field can be used as a pricing dimension.</span></span>

<span data-ttu-id="a9a19-109">另一个示例是交易类别的。</span><span class="sxs-lookup"><span data-stu-id="a9a19-109">Another example is that of transaction category.</span></span> <span data-ttu-id="a9a19-110">客户和实施者已在 PSA 中使用交易类别为工作分类和使用此字段根据工作类别定价和设置成本。</span><span class="sxs-lookup"><span data-stu-id="a9a19-110">Customers and Implementers have used the transaction category in PSA to classify work and use the field to price and cost based on the category of work.</span></span> <span data-ttu-id="a9a19-111">有关详细信息，请参阅[将交易类别用作定价维度](transaction-category-pricing-dimension.md)。</span><span class="sxs-lookup"><span data-stu-id="a9a19-111">For more information, see [Use transaction category as a pricing dimension](transaction-category-pricing-dimension.md).</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]