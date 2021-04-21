---
title: 解析估计值和实际值的成本费
description: 此主题提供有关如何解析估计值和实际值的成本费的信息。
author: rumant
manager: Annbe
ms.date: 04/09/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 13903acc22e765ddc5bc1b87428ef3565f2b0a44
ms.sourcegitcommit: ac90be6106592f883a0de39a75836fb40255d65a
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/09/2021
ms.locfileid: "5877301"
---
# <a name="resolving-cost-prices-for-estimates-and-actuals"></a><span data-ttu-id="4b949-103">解析估计值和实际值的成本费</span><span class="sxs-lookup"><span data-stu-id="4b949-103">Resolving cost prices for estimates and actuals</span></span>

<span data-ttu-id="4b949-104">_**适用于：** 面向资源/非库存场景的 Project Operations_</span><span class="sxs-lookup"><span data-stu-id="4b949-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="4b949-105">为了解析估计值和实际值的成本费和成本价目表，系统使用相关项目的 **日期**、**货币** 和 **合同签订部门** 字段中的信息。</span><span class="sxs-lookup"><span data-stu-id="4b949-105">To resolve cost prices and the cost price list for estimates and actuals, the system uses the information in the **Date**, **Currency**, and **Contracting Unit** fields of the related project.</span></span> <span data-ttu-id="4b949-106">解析成本价目表后，应用程序将解析成本费率。</span><span class="sxs-lookup"><span data-stu-id="4b949-106">After the cost price list is resolved, the application resolves the cost rate.</span></span>

## <a name="resolving-cost-rates-on-actual-and-estimate-lines-for-time"></a><span data-ttu-id="4b949-107">解析“时间”的实际值和估计值明细中的成本费率</span><span class="sxs-lookup"><span data-stu-id="4b949-107">Resolving cost rates on actual and estimate lines for Time</span></span>

<span data-ttu-id="4b949-108">“时间”的估计值明细引用项目中时间和资源分配的报价单和合同子项详细信息。</span><span class="sxs-lookup"><span data-stu-id="4b949-108">Estimate lines for Time refer to the quote and contract line details for time and resource assignments on a project.</span></span>

<span data-ttu-id="4b949-109">解析成本价目表后，系统将使用“时间”的估计值明细中的 **角色**、**资源供给公司** 和 **资源单位** 字段与价目表中的角色价格明细进行匹配。</span><span class="sxs-lookup"><span data-stu-id="4b949-109">After a cost price list is resolved, the system uses the **Role**, **Resourcing Company**, and **Resourcing Unit** fields on the estimate line for Time to match against the role price lines in the price list.</span></span> <span data-ttu-id="4b949-110">这一匹配假设您使用的是现成的人工成本定价维度。</span><span class="sxs-lookup"><span data-stu-id="4b949-110">This match assumes that you are using out-of-the-box pricing dimensions for labor cost.</span></span> <span data-ttu-id="4b949-111">如果您将系统配置为匹配代替 **角色**、**资源供给公司** 和 **资源单位** 的字段或除这几个字段外还匹配其他字段，将使用不同的组合来检索匹配的角色价格明细。</span><span class="sxs-lookup"><span data-stu-id="4b949-111">If you configured the system to match fields instead of, or in addition to **Role**, **Resourcing Company**, and **Resourcing Unit**, then a different combination will be used to retrieve a matching role price line.</span></span> <span data-ttu-id="4b949-112">如果应用程序发现具有 **角色**、**资源供给公司** 和 **资源单位** 组合的成本费率的角色价格明细，那就是默认成本费率。</span><span class="sxs-lookup"><span data-stu-id="4b949-112">If the application finds a role price line that has a cost rate for the **Role**, **Resourcing Company**, and **Resourcing Unit** combination, that is the default cost rate.</span></span> <span data-ttu-id="4b949-113">如果应用程序无法完全匹配 **角色**、**资源供给公司** 和 **资源单位** 值的组合，则它将检索具有匹配角色值的角色价格行，但是它的 **资源单位** 和 **资源供给公司** 为 NULL 值。</span><span class="sxs-lookup"><span data-stu-id="4b949-113">If the application can't exactly match the combination of **Role**, **Resourcing Company**, and **Resourcing Unit** values, it will retrieve role price lines with a matching role value, but have null values for **Resourcing Unit** and **Resourcing Company**.</span></span> <span data-ttu-id="4b949-114">在找到具有匹配的角色价格值的匹配角色价格记录后，成本率将默认自该记录。</span><span class="sxs-lookup"><span data-stu-id="4b949-114">After a matching role price record with matching role price value is found, the cost rate defaults from that record.</span></span> 

> [!NOTE]
> <span data-ttu-id="4b949-115">如果您配置不同的 **角色**、**资源供给公司** 和 **资源单位** 优先级，或者您有优先级更高的其他维度，此行为将相应变更。</span><span class="sxs-lookup"><span data-stu-id="4b949-115">If you configure a different prioritization of **Role**, **Resourcing Company**, and **Resourcing Unit**, or if you have other dimensions that have higher priority, this behavior will change accordingly.</span></span> <span data-ttu-id="4b949-116">系统将检索角色价格记录，这些记录的值按优先级顺序将每个定价维度值与行进行匹配，行中按优先级顺序最后出现的那些维度具有 NULL 值。</span><span class="sxs-lookup"><span data-stu-id="4b949-116">The system retrieves role price records with values that match each of the pricing dimension values in order of priority with rows that have null values for those dimensions coming last in the priority order.</span></span>

## <a name="resolving-cost-rates-on-actual-and-estimate-lines-for-expense"></a><span data-ttu-id="4b949-117">解析“支出”的实际值和估计值明细中的成本费率</span><span class="sxs-lookup"><span data-stu-id="4b949-117">Resolving cost rates on actual and estimate lines for Expense</span></span>

<span data-ttu-id="4b949-118">“支出”的估计值明细引用项目中支出和支出估计值明细的报价单和合同子项详细信息。</span><span class="sxs-lookup"><span data-stu-id="4b949-118">Estimate lines for Expense refer to the quote and contract line details for expenses and the expense estimate lines on a project.</span></span>

<span data-ttu-id="4b949-119">解析成本价目表后，系统将使用支出的估计值明细中的 **类别** 和 **单位** 字段的组合与解析的价目表中的 **类别价格** 明细进行匹配。</span><span class="sxs-lookup"><span data-stu-id="4b949-119">After a cost price list is resolved, the system uses a combination of the **Category** and **Unit** fields on the estimate line for an expense to match against the **Category Price** lines on the resolved price list.</span></span> <span data-ttu-id="4b949-120">如果系统发现具有 **类别** 和 **单位** 字段组合的成本费率的类别价格明细，此成本费率将为默认值。</span><span class="sxs-lookup"><span data-stu-id="4b949-120">If the system finds a category price line that has a cost rate for the **Category** and **Unit** field combination, the cost rate is defaulted.</span></span> <span data-ttu-id="4b949-121">如果系统无法匹配 **类别** 和 **单位** 值，或者能够找到匹配的类别价格明细，但定价方式不是 **单价**，成本费率默认为零 (0)。</span><span class="sxs-lookup"><span data-stu-id="4b949-121">If the system can't match the **Category** and **Unit** values, or if it is able to find a matching category price line but the pricing method is not **Price Per Unit**, the cost rate is defaulted to zero(0).</span></span>

## <a name="resolving-cost-rates-on-actual-and-estimate-lines-for-material"></a><span data-ttu-id="4b949-122">解析材料的实际明细和估算明细中中成本费率</span><span class="sxs-lookup"><span data-stu-id="4b949-122">Resolving cost rates on actual and estimate lines for material</span></span>

<span data-ttu-id="4b949-123">材料的估算行会引用项目上材料和材料估算行的报价单和合同子项明细。</span><span class="sxs-lookup"><span data-stu-id="4b949-123">Estimate lines for material refer to the quote and contract line details for materials and the material estimate lines on a project.</span></span>

<span data-ttu-id="4b949-124">解析成本价目表后，系统将使用材料估算的估算明细中的 **产品** 和 **单位** 字段组合，以根据已解析价目表中的 **价目表项** 行进行匹配。</span><span class="sxs-lookup"><span data-stu-id="4b949-124">After a cost price list is resolved, the system uses a combination of the **Product** and **Unit** fields on the estimate line for a material estimate to match against the **Price List Items** lines on the resolved price list.</span></span> <span data-ttu-id="4b949-125">如果系统找到具有 **产品** 和 **单位** 字段组合成本费率的产品价格行，则会默认成本费率。</span><span class="sxs-lookup"><span data-stu-id="4b949-125">If the system finds a product price line that has a cost rate for the **Product** and **Unit** field combination, the cost rate is defaulted.</span></span> <span data-ttu-id="4b949-126">如果系统无法匹配 **产品** 和 **单位** 值，则单位成本将默认为零。</span><span class="sxs-lookup"><span data-stu-id="4b949-126">If the system can't match the **Product** and **Unit** values, the unit cost defaults to zero.</span></span> <span data-ttu-id="4b949-127">如果存在匹配的价目表项行，也将发生此默认行为，但是定价方式基于未在产品中定义的标准成本或当前成本。</span><span class="sxs-lookup"><span data-stu-id="4b949-127">This default will also happen if there is a matching price list item line, but the pricing method is based on a standard cost or current cost that isn't defined in the product.</span></span>

[!INCLUDE[footer-include](../includes/footer-banner.md)]
