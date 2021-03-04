---
title: 根据估算和实际值处理成本费 - 精简
description: 此主题提供有关如何解析估计值和实际值中的成本费的信息。
author: rumant
manager: Annbe
ms.date: 10/13/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: d2afaa2231f4044dbcbfa24b91aec39289275a91
ms.sourcegitcommit: 2b74edd31f38410024a01124c9202a4d94464d04
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/17/2020
ms.locfileid: "4764562"
---
# <a name="resolve-cost-prices-on-estimates-and-actuals---lite"></a><span data-ttu-id="c707c-103">根据估算和实际值处理成本费 - 精简</span><span class="sxs-lookup"><span data-stu-id="c707c-103">Resolve cost prices on estimates and actuals - lite</span></span>

<span data-ttu-id="c707c-104">_**适用于：** 精简部署 - 估价交易开票_</span><span class="sxs-lookup"><span data-stu-id="c707c-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="c707c-105">为了解析估计值和实际值的成本费和成本价目表，系统使用相关项目的 **日期**、**货币** 和 **合同签订部门** 字段中的信息。</span><span class="sxs-lookup"><span data-stu-id="c707c-105">To resolve cost prices and the cost price list for estimates and actuals, the system uses the information in the **Date**, **Currency**, and **Contracting Unit** fields of the related project.</span></span> <span data-ttu-id="c707c-106">解析成本价目表后，应用程序将解析成本费率。</span><span class="sxs-lookup"><span data-stu-id="c707c-106">After the cost price list is resolved, the application resolves the cost rate.</span></span>

## <a name="resolving-cost-rates-on-actual-and-estimate-lines-for-time"></a><span data-ttu-id="c707c-107">解析“时间”的实际值和估计值明细中的成本费率</span><span class="sxs-lookup"><span data-stu-id="c707c-107">Resolving cost rates on actual and estimate lines for Time</span></span>

<span data-ttu-id="c707c-108">“时间”的估计值明细引用项目中时间和资源分配的报价单和合同子项详细信息。</span><span class="sxs-lookup"><span data-stu-id="c707c-108">Estimate lines for Time refer to the quote and contract line details for time and resource assignments on a project.</span></span>

<span data-ttu-id="c707c-109">成本价目表决定后，时间估算明细上的 **角色** 和 **资源单位** 字段将与价目表中的角色价格明细进行匹配。</span><span class="sxs-lookup"><span data-stu-id="c707c-109">After a cost price list is resolved, the **Role** and **Resourcing Unit** fields on the estimate line for Time are matched against the role price lines in the price list.</span></span> <span data-ttu-id="c707c-110">此匹配假设您为人工成本使用的是标准定价维度。</span><span class="sxs-lookup"><span data-stu-id="c707c-110">This match assumes that you're using the standard pricing dimensions for labor cost.</span></span> <span data-ttu-id="c707c-111">如果您将系统配置为匹配代替 **角色** 和 **资源单位** 的字段或除这两个字段外还匹配其他字段，将使用不同的组合来检索匹配的角色价格明细。</span><span class="sxs-lookup"><span data-stu-id="c707c-111">If you configured the system to match fields instead of, or in addition to **Role** and **Resourcing Unit**, then a different combination will be used to retrieve a matching role price line.</span></span> <span data-ttu-id="c707c-112">如果应用程序发现具有 **角色** 和 **资源单位** 组合的成本费率的角色价格明细，那就是默认成本费率。</span><span class="sxs-lookup"><span data-stu-id="c707c-112">If the application finds a role price line that has a cost rate for the **Role** and **Resourcing Unit** combination, that is the default cost rate.</span></span> <span data-ttu-id="c707c-113">如果应用程序无法匹配 **角色** 和 **资源单位** 值，它将检索具有匹配角色的角色价格明细，但 **资源单位** 为 null 值。</span><span class="sxs-lookup"><span data-stu-id="c707c-113">If the application can't match the **Role** and **Resourcing Unit** values, then it retrieves role price lines with a matching role, but null values of the **Resourcing Unit**.</span></span> <span data-ttu-id="c707c-114">在有了匹配的角色价格记录后，成本费率将默认为该记录中的值。</span><span class="sxs-lookup"><span data-stu-id="c707c-114">After it has a matching role price record, the cost rate defaults from that record.</span></span> 

> [!NOTE]
> <span data-ttu-id="c707c-115">如果您配置不同的 **角色** 和 **资源单位** 优先级，或者您有优先级更高的其他维度，此行为将相应变更。</span><span class="sxs-lookup"><span data-stu-id="c707c-115">If you configure a different prioritization of **Role** and **Resourcing Unit**, or if you have other dimensions that have higher priority, this behavior will change accordingly.</span></span> <span data-ttu-id="c707c-116">系统将按优先级顺序使用与每个定价维度值匹配的值检索角色价格记录，这些维度为 null 值的行排在最后。</span><span class="sxs-lookup"><span data-stu-id="c707c-116">The system retrieves role price records with values that match each of the pricing dimension values in order of priority with rows that have null values for those dimensions coming last.</span></span>

## <a name="resolving-cost-rates-on-actual-and-estimate-lines-for-expense"></a><span data-ttu-id="c707c-117">解析“支出”的实际值和估计值明细中的成本费率</span><span class="sxs-lookup"><span data-stu-id="c707c-117">Resolving cost rates on actual and estimate lines for Expense</span></span>

<span data-ttu-id="c707c-118">“支出”的估计值明细引用项目中支出和支出估计值明细的报价单和合同子项详细信息。</span><span class="sxs-lookup"><span data-stu-id="c707c-118">Estimate lines for Expense refer to the quote and contract line details for expenses and the expense estimate lines on a project.</span></span>

<span data-ttu-id="c707c-119">成本价目表决定后，系统将使用支出估算明细上的 **类别** 和 **单位** 字段的组合与已决定的价目表上的 **类别价格** 明细进行匹配。</span><span class="sxs-lookup"><span data-stu-id="c707c-119">After a cost price list is resolved, the system uses a combination of the **Category** and **Unit** fields on the expense estimate line to match against the **Category Price** lines on the resolved price list.</span></span> <span data-ttu-id="c707c-120">如果系统发现具有 **类别** 和 **单位** 字段组合的成本费率的类别价格明细，此成本费率将为默认值。</span><span class="sxs-lookup"><span data-stu-id="c707c-120">If the system finds a category price line that has a cost rate for the **Category** and **Unit** field combination, the cost rate is defaulted.</span></span> <span data-ttu-id="c707c-121">如果系统无法匹配 **类别** 和 **单位** 值，或者系统能够找到匹配的类别价格线，但定价方式不是 **单价**，成本费率将默认为零 (0)。</span><span class="sxs-lookup"><span data-stu-id="c707c-121">If the system can't match the **Category** and **Unit** values, or if it's able to find a matching category price line but the pricing method isn't **Price Per Unit**, the cost rate defaults to zero(0).</span></span>
