---
title: 解析估计值和实际值的成本费
description: 此主题提供有关如何解析估计值和实际值的成本费的信息。
author: rumant
manager: Annbe
ms.date: 10/13/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: d3422ef2eacc1e0617e60d41b7ddbcefe44d5b90
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/16/2020
ms.locfileid: "4072466"
---
# <a name="resolving-cost-prices-for-estimates-and-actuals"></a><span data-ttu-id="c7a0c-103">解析估计值和实际值的成本费</span><span class="sxs-lookup"><span data-stu-id="c7a0c-103">Resolving cost prices for estimates and actuals</span></span>

<span data-ttu-id="c7a0c-104">_**适用于：** 面向资源/非库存场景的 Project Operations_</span><span class="sxs-lookup"><span data-stu-id="c7a0c-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="c7a0c-105">为了解析估计值和实际值的成本费和成本价目表，系统使用相关项目的 **日期** 、 **货币** 和 **合同签订部门** 字段中的信息。</span><span class="sxs-lookup"><span data-stu-id="c7a0c-105">To resolve cost prices and the cost price list for estimates and actuals, the system uses the information in the **Date** , **Currency** , and **Contracting Unit** fields of the related project.</span></span> <span data-ttu-id="c7a0c-106">解析成本价目表后，应用程序将解析成本费率。</span><span class="sxs-lookup"><span data-stu-id="c7a0c-106">After the cost price list is resolved, the application resolves the cost rate.</span></span>

## <a name="resolving-cost-rates-on-actual-and-estimate-lines-for-time"></a><span data-ttu-id="c7a0c-107">解析“时间”的实际值和估计值明细中的成本费率</span><span class="sxs-lookup"><span data-stu-id="c7a0c-107">Resolving cost rates on actual and estimate lines for Time</span></span>

<span data-ttu-id="c7a0c-108">“时间”的估计值明细引用项目中时间和资源分配的报价单和合同子项详细信息。</span><span class="sxs-lookup"><span data-stu-id="c7a0c-108">Estimate lines for Time refer to the quote and contract line details for time and resource assignments on a project.</span></span>

<span data-ttu-id="c7a0c-109">解析成本价目表后，系统将使用“时间”的估计值明细中的 **角色** 、 **资源供给公司** 和 **资源单位** 字段与价目表中的角色价格明细进行匹配。</span><span class="sxs-lookup"><span data-stu-id="c7a0c-109">After a cost price list is resolved, the system uses the **Role** , **Resourcing Company** , and **Resourcing Unit** fields on the estimate line for Time to match against the role price lines in the price list.</span></span> <span data-ttu-id="c7a0c-110">这一匹配假设您使用的是现成的人工成本定价维度。</span><span class="sxs-lookup"><span data-stu-id="c7a0c-110">This match assumes that you are using out-of-the-box pricing dimensions for labor cost.</span></span> <span data-ttu-id="c7a0c-111">如果您将系统配置为匹配代替 **角色** 、 **资源供给公司** 和 **资源单位** 的字段或除这几个字段外还匹配其他字段，将使用不同的组合来检索匹配的角色价格明细。</span><span class="sxs-lookup"><span data-stu-id="c7a0c-111">If you configured the system to match fields instead of, or in addition to **Role** , **Resourcing Company** , and **Resourcing Unit** , then a different combination will be used to retrieve a matching role price line.</span></span> <span data-ttu-id="c7a0c-112">如果应用程序发现具有 **角色** 、 **资源供给公司** 和 **资源单位** 组合的成本费率的角色价格明细，那就是默认成本费率。</span><span class="sxs-lookup"><span data-stu-id="c7a0c-112">If the application finds a role price line that has a cost rate for the **Role** , **Resourcing Company** , and **Resourcing Unit** combination, that is the default cost rate.</span></span> <span data-ttu-id="c7a0c-113">如果应用程序无法匹配 **角色** 、 **资源供给公司** 和 **资源单位** 值，它将检索具有匹配角色的角色价格明细，但 **资源单位** 为 null 值。</span><span class="sxs-lookup"><span data-stu-id="c7a0c-113">If the application can't match the **Role** , **Resourcing Company** , and **Resourcing Unit** values, then it retrieves role price lines with a matching role, but null values of the **Resourcing Unit**.</span></span> <span data-ttu-id="c7a0c-114">在有了匹配的角色价格记录后，成本费率将默认为该记录中的值。</span><span class="sxs-lookup"><span data-stu-id="c7a0c-114">After it has a matching role price record, the cost rate defaults from that record.</span></span> 

> [!NOTE]
> <span data-ttu-id="c7a0c-115">如果您配置不同的 **角色** 、 **资源供给公司** 和 **资源单位** 优先级，或者您有优先级更高的其他维度，此行为将相应变更。</span><span class="sxs-lookup"><span data-stu-id="c7a0c-115">If you configure a different prioritization of **Role** , **Resourcing Company** , and **Resourcing Unit** , or if you have other dimensions that have higher priority, this behavior will change accordingly.</span></span> <span data-ttu-id="c7a0c-116">系统将按优先级顺序使用与每个定价维度值匹配的值检索角色价格记录，这些维度为 null 值的行排在最后。</span><span class="sxs-lookup"><span data-stu-id="c7a0c-116">The system retrieves role price records with values that match each of the pricing dimension values in order of priority with rows that have null values for those dimensions coming last.</span></span>

## <a name="resolving-cost-rates-on-actual-and-estimate-lines-for-expense"></a><span data-ttu-id="c7a0c-117">解析“支出”的实际值和估计值明细中的成本费率</span><span class="sxs-lookup"><span data-stu-id="c7a0c-117">Resolving cost rates on actual and estimate lines for Expense</span></span>

<span data-ttu-id="c7a0c-118">“支出”的估计值明细引用项目中支出和支出估计值明细的报价单和合同子项详细信息。</span><span class="sxs-lookup"><span data-stu-id="c7a0c-118">Estimate lines for Expense refer to the quote and contract line details for expenses and the expense estimate lines on a project.</span></span>

<span data-ttu-id="c7a0c-119">解析成本价目表后，系统将使用支出的估计值明细中的 **类别** 和 **单位** 字段的组合与解析的价目表中的 **类别价格** 明细进行匹配。</span><span class="sxs-lookup"><span data-stu-id="c7a0c-119">After a cost price list is resolved, the system uses a combination of the **Category** and **Unit** fields on the estimate line for an expense to match against the **Category Price** lines on the resolved price list.</span></span> <span data-ttu-id="c7a0c-120">如果系统发现具有 **类别** 和 **单位** 字段组合的成本费率的类别价格明细，此成本费率将为默认值。</span><span class="sxs-lookup"><span data-stu-id="c7a0c-120">If the system finds a category price line that has a cost rate for the **Category** and **Unit** field combination, the cost rate is defaulted.</span></span> <span data-ttu-id="c7a0c-121">如果系统无法匹配 **类别** 和 **单位** 值，或者能够找到匹配的类别价格明细，但定价方式不是 **单价** ，成本费率默认为零 (0)。</span><span class="sxs-lookup"><span data-stu-id="c7a0c-121">If the system can't match the **Category** and **Unit** values, or if it is able to find a matching category price line but the pricing method is not **Price Per Unit** , the cost rate is defaulted to zero(0).</span></span>
