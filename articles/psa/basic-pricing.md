---
title: 项目定价
description: 此主题介绍 Dynamics 365 Project Service Automation 中的定价工作原理。
author: rumant
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/11/2019
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: b319f9be9fd72ac99ce6012b6baffde812e3077d
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/16/2020
ms.locfileid: "4072801"
---
# <a name="project-pricing"></a><span data-ttu-id="3899d-103">项目定价</span><span class="sxs-lookup"><span data-stu-id="3899d-103">Project pricing</span></span> 

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="3899d-104">Dynamics 365 Project Service Automation 扩展了 Dynamics 365 Sales 中的价目表实体。</span><span class="sxs-lookup"><span data-stu-id="3899d-104">Dynamics 365 Project Service Automation extends the Price list entity in Dynamics 365 Sales.</span></span> 

## <a name="key-entities"></a><span data-ttu-id="3899d-105">关键实体</span><span class="sxs-lookup"><span data-stu-id="3899d-105">Key entities</span></span>

<span data-ttu-id="3899d-106">价目表中包含四个不同实体提供的信息：</span><span class="sxs-lookup"><span data-stu-id="3899d-106">A price list includes information that is provided by four different entities:</span></span>

- <span data-ttu-id="3899d-107">**价目表** - 此实体存储有关定价时间的上下文、货币、时效和时间单位的信息。</span><span class="sxs-lookup"><span data-stu-id="3899d-107">**Price List** - This entity stores information about context, currency, date effectivity, and time unit for pricing time.</span></span> <span data-ttu-id="3899d-108">上下文显示价目表表示成本费率还是销售额费率。</span><span class="sxs-lookup"><span data-stu-id="3899d-108">Context shows whether the price list is expresses cost rates or sales rates.</span></span> 
- <span data-ttu-id="3899d-109">**货币** - 此实体存储价目表的价格货币。</span><span class="sxs-lookup"><span data-stu-id="3899d-109">**Currency** - This entity stores the currency of prices on the price list.</span></span> 
- <span data-ttu-id="3899d-110">**日期** - 系统尝试输入交易的默认价格时，使用此实体。</span><span class="sxs-lookup"><span data-stu-id="3899d-110">**Date** - This entity is used when the system tries to enter a default a price on a transaction.</span></span> <span data-ttu-id="3899d-111">PSA 定价选择其时效包含交易日期的价目表。</span><span class="sxs-lookup"><span data-stu-id="3899d-111">PSA pricing selects the price list that has date effectivity that includes the date of the transaction.</span></span> <span data-ttu-id="3899d-112">如果 PSA 定价找到多个对附加到相关报价单的交易日期有效的价目表，则不设置任何默认价格。</span><span class="sxs-lookup"><span data-stu-id="3899d-112">If PSA pricing finds more than one price list that is effective for the transaction date is attached to the related quote, contract, or organizational unit, then no price is defaulted.</span></span> 
- <span data-ttu-id="3899d-113">**时间** - 此实体存储用于表示价格的时间单位，如天费率或小时费率。</span><span class="sxs-lookup"><span data-stu-id="3899d-113">**Time** - This entity stores the unit of time that prices are expressed for, such as daily or hourly rates.</span></span> 

<span data-ttu-id="3899d-114">价目表实体有三个用于存储价格的相关表：</span><span class="sxs-lookup"><span data-stu-id="3899d-114">The Price list entity has three related tables that store prices:</span></span>

  - <span data-ttu-id="3899d-115">**角色价格** - 此表存储角色与部门值组合的费率，用于为人力资源设置基于角色的价格。</span><span class="sxs-lookup"><span data-stu-id="3899d-115">**Role Price** - This table stores a rate for a combination of role and organizational unit values and is used to set up role-based prices for human resources.</span></span>
  - <span data-ttu-id="3899d-116">**交易类别价格** - 此表按交易类别存储价格，用于设置支出类别价格。</span><span class="sxs-lookup"><span data-stu-id="3899d-116">**Transaction Category Price** - This table stores prices by transaction category and is used to set up expense category prices.</span></span>
  - <span data-ttu-id="3899d-117">**价目表项** - 此表存储目录产品的价格。</span><span class="sxs-lookup"><span data-stu-id="3899d-117">**Price List Items** - This table stores prices for catalog products.</span></span>

> ![使用价目表配置价格](media/basic-guide-12.png)
 
<span data-ttu-id="3899d-119">价目表是费率卡。</span><span class="sxs-lookup"><span data-stu-id="3899d-119">The price list is a rate card.</span></span> <span data-ttu-id="3899d-120">费率卡是价目表实体与角色价格、交易类别价格和价目表项表中的相关行的组合。</span><span class="sxs-lookup"><span data-stu-id="3899d-120">A rate card is a combination of the Price List entity and related rows in the Role Price, Transaction Category Price, and Price List Items tables.</span></span>

## <a name="resource-roles"></a><span data-ttu-id="3899d-121">资源角色</span><span class="sxs-lookup"><span data-stu-id="3899d-121">Resource roles</span></span>

<span data-ttu-id="3899d-122">术语 *资源角色* 指的是要对项目执行一组特定任务的人员必须拥有的一组技能、资格和认证。</span><span class="sxs-lookup"><span data-stu-id="3899d-122">The term *resource role* refers to a set of skills, competencies, and certifications that a person must have to perform a specific set of tasks on a project.</span></span>

<span data-ttu-id="3899d-123">人力资源时间的报价通常基于资源在特定项目中的角色。</span><span class="sxs-lookup"><span data-stu-id="3899d-123">Human resources time is usually quoted based on the role that a resource fills on a specific project.</span></span> <span data-ttu-id="3899d-124">对于人力资源时间，PSA 支持基于资源角色定成本和记帐。</span><span class="sxs-lookup"><span data-stu-id="3899d-124">For human resource time, PSA supports costing and billing that are based on resource role.</span></span> <span data-ttu-id="3899d-125">可以使用 **时间** 计价单位组中的任何计价单位为时间定价。</span><span class="sxs-lookup"><span data-stu-id="3899d-125">Time can be priced in any unit in the **Time** unit group.</span></span>

<span data-ttu-id="3899d-126">**时间** 计价单位组是在安装 PSA 时创建的。</span><span class="sxs-lookup"><span data-stu-id="3899d-126">The **Time** unit group is crated when PSA is installed.</span></span> <span data-ttu-id="3899d-127">其默认计价单位为 **小时** 。</span><span class="sxs-lookup"><span data-stu-id="3899d-127">It has a default unit of **Hour**.</span></span> <span data-ttu-id="3899d-128">不能删除、重命名或编辑 **时间** 计价单位组或 **时间** 计价单位的属性。</span><span class="sxs-lookup"><span data-stu-id="3899d-128">You can't delete, rename, or edit the attributes fo teh **Time** unit group or the **Hour** unit.</span></span> <span data-ttu-id="3899d-129">但是，可以向 **时间** 计价单位组添加其他计价单位。</span><span class="sxs-lookup"><span data-stu-id="3899d-129">However, you can add other units to the **Time** unit group.</span></span> <span data-ttu-id="3899d-130">如果尝试删除 **时间** 计价单位组或 **小时** 计价单位，可能会导致 PSA 业务逻辑出错。</span><span class="sxs-lookup"><span data-stu-id="3899d-130">If you try to delete either the **Time** unit group or the **Hour** unit, you might cause failures in the PSA business logic.</span></span>

> ![按角色配置价格](media/basic-guide-13.png)
 
## <a name="transaction-categories-and-expense-categories"></a><span data-ttu-id="3899d-132">交易类别和支出类别</span><span class="sxs-lookup"><span data-stu-id="3899d-132">Transaction categories and expense categories</span></span>

<span data-ttu-id="3899d-133">项目顾问产生，并且通常会记帐到客户头上的旅行和其他支出。</span><span class="sxs-lookup"><span data-stu-id="3899d-133">Travel and other expenses that project consultants incur are usually billed to the customer.</span></span> <span data-ttu-id="3899d-134">PSA 支持使用价目表为支出类别定价。</span><span class="sxs-lookup"><span data-stu-id="3899d-134">PSA supports pricing of expense categories by using price lists.</span></span> <span data-ttu-id="3899d-135">例如，机票、酒店和租车就属于支出类别。</span><span class="sxs-lookup"><span data-stu-id="3899d-135">Airfare, hotel, and car rental are examples fo expense categories.</span></span> <span data-ttu-id="3899d-136">支出的每项价目表明细指定特定支出类别的定价。</span><span class="sxs-lookup"><span data-stu-id="3899d-136">Each price list line for expenses specifies pricing for a specific expense category.</span></span> <span data-ttu-id="3899d-137">对于支出类别的定价，PSA 支持以下三种定价方法：</span><span class="sxs-lookup"><span data-stu-id="3899d-137">For pricing of expense categories, PSA supports the following three pricing methods:</span></span>

- <span data-ttu-id="3899d-138">**按成本** - 按支出成本对客户记帐，不加价。</span><span class="sxs-lookup"><span data-stu-id="3899d-138">**At cost** - The expense cost is billed to the customer, and no markup is applied.</span></span>
- <span data-ttu-id="3899d-139">**加价百分比** - 在实际成本的基础上对客户按加价百分比记帐。</span><span class="sxs-lookup"><span data-stu-id="3899d-139">**Markup percentage** - The percentage over the actual cost is billed to the customer.</span></span> 
- <span data-ttu-id="3899d-140">**单价** - 为每个支出类别单位设置记帐价格。</span><span class="sxs-lookup"><span data-stu-id="3899d-140">**Price per unit** - A billing price is set for each unit of the expense category.</span></span> <span data-ttu-id="3899d-141">对客户记帐的金额根据顾问报告的支出单位数量计算。</span><span class="sxs-lookup"><span data-stu-id="3899d-141">The amount that is billed ot the customer is calculated based on the number of expense units that the consultant reports.</span></span> <span data-ttu-id="3899d-142">英里数使用单价定价方法。</span><span class="sxs-lookup"><span data-stu-id="3899d-142">Mileage uses the price-per-unit pricing method.</span></span> <span data-ttu-id="3899d-143">例如，可以将英里数支出类别配置为每天 30 美元 (USD) 或每英里 2 美元。</span><span class="sxs-lookup"><span data-stu-id="3899d-143">For example, the mileage expense category can be configured for 30 US dollars (USD) per day or 2 USD per mile.</span></span> <span data-ttu-id="3899d-144">当顾问为项目报告英里数时，记帐金额基于顾问报告的英里数计算。</span><span class="sxs-lookup"><span data-stu-id="3899d-144">When a consultant reports mileage on a project, the amount to bill is calculated based on the number of miles that the consultant reported.</span></span>

> ![配置支出类别的定价](media/basic-guide-14.png)
 
## <a name="project-sales-pricing-and-overrides"></a><span data-ttu-id="3899d-146">项目销售定价和替代</span><span class="sxs-lookup"><span data-stu-id="3899d-146">Project sales pricing and overrides</span></span>

<span data-ttu-id="3899d-147">对于项目报价单和合同，项目价目表采用的价格替代模式与产品价目表采用的不同。</span><span class="sxs-lookup"><span data-stu-id="3899d-147">For project quotes and contracts, a project price list has a different price override pattern than a product price list.</span></span> <span data-ttu-id="3899d-148">在基于产品目录的报价单明细中，可以直接替代报价单明细中角色和类别的价格，因为每项报价单明细都正好指向一个目录项。</span><span class="sxs-lookup"><span data-stu-id="3899d-148">On a product catalog–based quote line, you can override the price to roles and categories directly on the quote line, because each quote line points to exactly one catalog item.</span></span> <span data-ttu-id="3899d-149">但是，在基于项目的报价单明细中，不能直接替代报价单明细中的角色和类别的价格。</span><span class="sxs-lookup"><span data-stu-id="3899d-149">However, on a project-based quote line, you can't override the price to roles and categories directly on the quote line.</span></span> <span data-ttu-id="3899d-150">为了支持这两种不同的替代模式，PSA 引入了一种新的价目表关联，即项目价目表。</span><span class="sxs-lookup"><span data-stu-id="3899d-150">To support the two distinct override patterns, PSA has introduced a new price list association, the project price list.</span></span>

> [!NOTE]
> <span data-ttu-id="3899d-151">建议您为项目资源和目录项设置单独的价目表，因为在您替代定价时，这两者的行为不同。</span><span class="sxs-lookup"><span data-stu-id="3899d-151">We recommend that you have a separate price list for your project resources and your catalog items, because of the behavior differences between the two when you override pricing.</span></span>

<span data-ttu-id="3899d-152">对于项目定价，下面的每个实体可以有一个或多个关联的销售价目表：</span><span class="sxs-lookup"><span data-stu-id="3899d-152">Each of the following entities can have one or more associated sales price lists for project pricing:</span></span>

- <span data-ttu-id="3899d-153">客户（帐户）</span><span class="sxs-lookup"><span data-stu-id="3899d-153">Customer (account)</span></span> 
- <span data-ttu-id="3899d-154">商机</span><span class="sxs-lookup"><span data-stu-id="3899d-154">Opportunity</span></span> 
- <span data-ttu-id="3899d-155">报价单</span><span class="sxs-lookup"><span data-stu-id="3899d-155">Quote</span></span> 
- <span data-ttu-id="3899d-156">项目合同</span><span class="sxs-lookup"><span data-stu-id="3899d-156">Project Contract</span></span>

<span data-ttu-id="3899d-157">这些实体与价目表之间的关联通过项目价目表指示。</span><span class="sxs-lookup"><span data-stu-id="3899d-157">The association of these entities with a price list is indicated by the project price lists.</span></span> <span data-ttu-id="3899d-158">可以将一个或多个价目表与客户、商机、报价单和项目合同销售实体关联。</span><span class="sxs-lookup"><span data-stu-id="3899d-158">You can associate one or more price lists with the Customer, Opportunity, Quote, and Project Contract sales entities.</span></span>

<span data-ttu-id="3899d-159">不会在客户记录中自动输入默认项目价目表。</span><span class="sxs-lookup"><span data-stu-id="3899d-159">A default project price list isn't automatically entered on a customer record.</span></span> <span data-ttu-id="3899d-160">但是，可以手动向客户记录附加项目价目表。</span><span class="sxs-lookup"><span data-stu-id="3899d-160">However, you can manually attach a project price list to the customer record.</span></span> <span data-ttu-id="3899d-161">尽管如此，还是仅当与客户之间存在自定义定价协议时，才应手动附加项目价目表。</span><span class="sxs-lookup"><span data-stu-id="3899d-161">Nevertheless, you should manually attach a project price list only when you have a custom pricing agreement with the customer.</span></span> 

<span data-ttu-id="3899d-162">如果向销售实体附加项目价目表，PSA 将验证以下信息：</span><span class="sxs-lookup"><span data-stu-id="3899d-162">When a project price list is attached to a sales entity, PSA validates the following information:</span></span>

- <span data-ttu-id="3899d-163">价目表有 **销售** 上下文。</span><span class="sxs-lookup"><span data-stu-id="3899d-163">The price list las a context of **Sales**.</span></span> 
- <span data-ttu-id="3899d-164">价目表货币与客户货币匹配。</span><span class="sxs-lookup"><span data-stu-id="3899d-164">The price list currency matches the customer currency.</span></span> 

<span data-ttu-id="3899d-165">在项目合同中，PSA 使用以下优先顺序自动设置相关项目价目表：</span><span class="sxs-lookup"><span data-stu-id="3899d-165">On a project contract, PSA uses the following order of precedence to automatically set related project price lists:</span></span>

1. <span data-ttu-id="3899d-166">报价单</span><span class="sxs-lookup"><span data-stu-id="3899d-166">Quote</span></span>
2. <span data-ttu-id="3899d-167">商机</span><span class="sxs-lookup"><span data-stu-id="3899d-167">Opportunity</span></span>
3. <span data-ttu-id="3899d-168">客户</span><span class="sxs-lookup"><span data-stu-id="3899d-168">Customer</span></span> 
4. <span data-ttu-id="3899d-169">PSA 的全局设置</span><span class="sxs-lookup"><span data-stu-id="3899d-169">Global settings for PSA</span></span>

<span data-ttu-id="3899d-170">默认输入项目价目表时，PSA 验证货币是否匹配客户的货币，以及已输入的默认价目表是否有 **销售** 上下文。</span><span class="sxs-lookup"><span data-stu-id="3899d-170">When a project price list is entered by default, PSA validates that the currency matches the customer’s currency, and that the default price lists that have been entered have a context of **Sales**.</span></span>

<span data-ttu-id="3899d-171">可以将多个项目价目表与客户、商机、报价单和项目合同实体关联。</span><span class="sxs-lookup"><span data-stu-id="3899d-171">You can associate multiple project price lists with the Customer, Opportunity, Quote, and Project Contract entities.</span></span> <span data-ttu-id="3899d-172">此功能支持为长期开展的项目合同设置特定于日期的默认价格，在此情况下，可能需要多个价目表来纳入通货膨胀导致的价格更新。</span><span class="sxs-lookup"><span data-stu-id="3899d-172">This capability supports date-specific default prices for a long-running project contract, where you might require more than one price list to account for price updates that occur because of inflation.</span></span> <span data-ttu-id="3899d-173">但是，如果与客户、商机、报价单或项目合同实体关联的价目表存在重合时效，默认价格可能不正确。</span><span class="sxs-lookup"><span data-stu-id="3899d-173">However, if the price lists that you associate with the Customer, Opportunity, Quote, or Project Contract entity have overlapping date effectivity, the default prices might be incorrect.</span></span> <span data-ttu-id="3899d-174">因此，应确保不将具有重合时效的项目价目表与这些实体关联。</span><span class="sxs-lookup"><span data-stu-id="3899d-174">Therefore, you should make sure that project price lists that have overlapping date effectivity aren't associated with those entities.</span></span>

### <a name="deal-specific-price-overrides"></a><span data-ttu-id="3899d-175">交易特定的价格替代</span><span class="sxs-lookup"><span data-stu-id="3899d-175">Deal-specific price overrides</span></span>

<span data-ttu-id="3899d-176">在 PSA 中，可为报价单或项目合同中默认输入的项目价目表中所选价格创建交易特定的替代。</span><span class="sxs-lookup"><span data-stu-id="3899d-176">In PSA, you can create deal-specific overrides for selected prices on project price lists that are entered by default on a quote or project contract.</span></span>

<span data-ttu-id="3899d-177">默认情况下，项目合同始终会获取基础销售价目表的副本，而不是其直接链接。</span><span class="sxs-lookup"><span data-stu-id="3899d-177">By default, a project contract always gets a copy of the master sales price list instead of a direct link to it.</span></span> <span data-ttu-id="3899d-178">此行为可以帮助确保在基础价目表改变时，与客户就工作说明书 (SOW) 达成的价格协议不变。</span><span class="sxs-lookup"><span data-stu-id="3899d-178">This behavior helps guarantee that price agreements that are made iwth a customer for a statement of work (SOW) don't change if the master price list is changed.</span></span>

<span data-ttu-id="3899d-179">但是，在报价单中，可以使用基础价目表。</span><span class="sxs-lookup"><span data-stu-id="3899d-179">However, on a quote, you can use a master price list.</span></span> <span data-ttu-id="3899d-180">也可以复制基础价目表并进行编辑，以便创建仅适用于该报价单的自定义价目表。</span><span class="sxs-lookup"><span data-stu-id="3899d-180">Alternatively, you can copy a master price list and edit it to create a custom price list that applies only to that quote.</span></span> <span data-ttu-id="3899d-181">若要创建特定于某个报价单的新价目表，请在 **报价单** 页中选择 **创建自定义报价** 。</span><span class="sxs-lookup"><span data-stu-id="3899d-181">To create a new price list that is specific to a quote, on the **Quote** page, select **Create custom pricing**.</span></span> <span data-ttu-id="3899d-182">只能从报价单访问交易特定的项目价目表。</span><span class="sxs-lookup"><span data-stu-id="3899d-182">You can access the deal-specific project price list only from the quote.</span></span> 

<span data-ttu-id="3899d-183">创建自定义项目价目表时，只会复制价目表的项目组成部分。</span><span class="sxs-lookup"><span data-stu-id="3899d-183">When you create a custom project price list, only the project components of the price list are copied.</span></span> <span data-ttu-id="3899d-184">换句话说，创建的新价目表是报价单中附加的现有项目价目表的副本，并且这个新价目表只有相关角色价格和交易类别价格。</span><span class="sxs-lookup"><span data-stu-id="3899d-184">In other words, a new price list created as a copy of the existing project price list that is attached on the quote, and this new price list has only related role prices and transaction category prices.</span></span>

> ![查看和配置项目合同的自定义定价](media/basic-guide-15.png)
  
## <a name="tracking-costs"></a><span data-ttu-id="3899d-186">跟踪成本</span><span class="sxs-lookup"><span data-stu-id="3899d-186">Tracking costs</span></span>

<span data-ttu-id="3899d-187">PSA 可以跟踪在项目中使用人力资源时间产生的成本。</span><span class="sxs-lookup"><span data-stu-id="3899d-187">PSA tracks costs for the use of human resource time on projects.</span></span> <span data-ttu-id="3899d-188">还可以跟踪项目期间产生的其他支出（如旅行支出）的成本。</span><span class="sxs-lookup"><span data-stu-id="3899d-188">It also tracks costs for other expenses that are incurrred during hte project, such as travel expenses.</span></span>

<span data-ttu-id="3899d-189">和记帐费率一样，也使用价目表设置人力资源的成本费率。</span><span class="sxs-lookup"><span data-stu-id="3899d-189">Like bill rates, cost rates for human resources are also set up using price lists.</span></span> <span data-ttu-id="3899d-190">下面是成本价目表与销售额价目表行为之间的主要差别：</span><span class="sxs-lookup"><span data-stu-id="3899d-190">Here are the main differences in the behavior of the cost price list and sales price list:</span></span>

- <span data-ttu-id="3899d-191">不能替代特定产品、合同或报价单的资源成本费率。</span><span class="sxs-lookup"><span data-stu-id="3899d-191">The cost rate of a resource can’t be overridden on a specific project, contract, or quote.</span></span> <span data-ttu-id="3899d-192">但是，如果进行了特定于交易性质的更改，则可以按交易替代记帐费率。</span><span class="sxs-lookup"><span data-stu-id="3899d-192">However, bill rates can be overridden on a per-deal basis if changes are made that are specific to the nature of the deal.</span></span> 

- <span data-ttu-id="3899d-193">解析成本价目表时采用以下顺序：</span><span class="sxs-lookup"><span data-stu-id="3899d-193">The following order is used to resolve a cost price list:</span></span>

    1. <span data-ttu-id="3899d-194">附加到部门的成本价目表。</span><span class="sxs-lookup"><span data-stu-id="3899d-194">The cost price list that is attached to the organizational unit.</span></span>
    2. <span data-ttu-id="3899d-195">附加到 Project Service 参数的成本价目表。</span><span class="sxs-lookup"><span data-stu-id="3899d-195">The cost price list that is attached to the project service parameters.</span></span> <span data-ttu-id="3899d-196">因为可以将大量不同货币的成本价目表附加到 Project Service 参数，所以 PSA 会在项目、合同或报价单的货币与成本价目表的货币之间进行匹配。</span><span class="sxs-lookup"><span data-stu-id="3899d-196">Because cost price lists in many different currencies can be attached to project service parameters, PSA does a currency match between the currency of the contracting organizational unit of the project, contract, or quote, and the currency of the cost price list.</span></span>
    3. <span data-ttu-id="3899d-197">对于支出，按成本定价方法和成本加价定价方法不适用于成本价目表。</span><span class="sxs-lookup"><span data-stu-id="3899d-197">For expenses, the at-cost and markup-over-cost pricing methods don’t apply to cost price lists.</span></span> <span data-ttu-id="3899d-198">即使在成本价目表明细中使用这些定价方法设置交易类别成本，系统也会忽略这些定价方法，并且不输入任何默认成本费。</span><span class="sxs-lookup"><span data-stu-id="3899d-198">Even if these pricing methods are used on cost price list lines to set up transaction category costs, the system ignores them, and no default cost price is entered.</span></span>
