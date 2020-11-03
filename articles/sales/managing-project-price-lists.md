---
title: 项目价目表
description: 此主题提供有关项目价目表实体的信息。
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
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
ms.openlocfilehash: 1a69cf51ca8cde8260f4136cf1b2e936f99b112a
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/16/2020
ms.locfileid: "4072830"
---
# <a name="project-price-lists"></a><span data-ttu-id="21686-103">项目价目表</span><span class="sxs-lookup"><span data-stu-id="21686-103">Project price lists</span></span>

<span data-ttu-id="21686-104">_**适用于：** 基于资源/非库存场景的 Project Operations，精简部署 - 估价开票交易_</span><span class="sxs-lookup"><span data-stu-id="21686-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="21686-105">Dynamics 365 Project Operations 扩展 Dynamics 365 Sales 中的价目表实体。</span><span class="sxs-lookup"><span data-stu-id="21686-105">Dynamics 365 Project Operations extends the Price list entity in Dynamics 365 Sales.</span></span> 

## <a name="key-entities"></a><span data-ttu-id="21686-106">关键实体</span><span class="sxs-lookup"><span data-stu-id="21686-106">Key entities</span></span>

<span data-ttu-id="21686-107">价目表中包含四个不同实体提供的信息：</span><span class="sxs-lookup"><span data-stu-id="21686-107">A price list includes information that is provided by four different entities:</span></span>

- <span data-ttu-id="21686-108">**价目表** ：此实体存储有关定价时间的上下文、货币、时效和时间单位的信息。</span><span class="sxs-lookup"><span data-stu-id="21686-108">**Price List** : This entity stores information about context, currency, date effectivity, and time unit for pricing time.</span></span> <span data-ttu-id="21686-109">上下文显示价目表表示成本费率还是销售额费率。</span><span class="sxs-lookup"><span data-stu-id="21686-109">Context shows whether the price list expresses cost rates or sales rates.</span></span> 
- <span data-ttu-id="21686-110">**货币** ：此实体存储价目表的价格货币。</span><span class="sxs-lookup"><span data-stu-id="21686-110">**Currency** :  This entity stores the currency of prices on the price list.</span></span> 
- <span data-ttu-id="21686-111">**日期** ：系统尝试输入交易的默认价格时，使用此实体。</span><span class="sxs-lookup"><span data-stu-id="21686-111">**Date** : This entity is used when the system tries to enter a default a price on a transaction.</span></span> <span data-ttu-id="21686-112">将选择其时效包含交易日期的价目表。</span><span class="sxs-lookup"><span data-stu-id="21686-112">A price list that has date effectivity that includes the date of the transaction is selected.</span></span> <span data-ttu-id="21686-113">如果找到多个对交易日期有效并且附加到相关报价单、合同或部门的价目表，则不设置任何默认价格。</span><span class="sxs-lookup"><span data-stu-id="21686-113">If  more than one price list is found that is effective for the transaction date and is attached to the related quote, contract, or organizational unit, then no price is defaulted.</span></span> 
- <span data-ttu-id="21686-114">**时间** ：此实体存储用于表示价格的时间单位，如天费率或小时费率。</span><span class="sxs-lookup"><span data-stu-id="21686-114">**Time** : This entity stores the unit of time that prices are expressed for, such as daily or hourly rates.</span></span> 

<span data-ttu-id="21686-115">价目表实体有三个用于存储价格的相关表：</span><span class="sxs-lookup"><span data-stu-id="21686-115">The Price list entity has three related tables that store prices:</span></span>

  - <span data-ttu-id="21686-116">**角色价格** ：此表存储角色与部门值组合的费率，用于为人力资源设置基于角色的价格。</span><span class="sxs-lookup"><span data-stu-id="21686-116">**Role Price** : This table stores a rate for a combination of role and organizational unit values and is used to set up role-based prices for human resources.</span></span>
  - <span data-ttu-id="21686-117">**交易类别价格** ：此表按交易类别存储价格，用于设置支出类别价格。</span><span class="sxs-lookup"><span data-stu-id="21686-117">**Transaction Category Price** : This table stores prices by transaction category and is used to set up expense category prices.</span></span>
  - <span data-ttu-id="21686-118">**价目表项** ：此表存储目录产品的价格。</span><span class="sxs-lookup"><span data-stu-id="21686-118">**Price List Items** : This table stores prices for catalog products.</span></span>
 
<span data-ttu-id="21686-119">价目表是费率卡。</span><span class="sxs-lookup"><span data-stu-id="21686-119">The price list is a rate card.</span></span> <span data-ttu-id="21686-120">费率卡是价目表实体与角色价格、交易类别价格和价目表项表中的相关行的组合。</span><span class="sxs-lookup"><span data-stu-id="21686-120">A rate card is a combination of the Price List entity and related rows in the Role Price, Transaction Category Price, and Price List Items tables.</span></span>

## <a name="resource-roles"></a><span data-ttu-id="21686-121">资源角色</span><span class="sxs-lookup"><span data-stu-id="21686-121">Resource roles</span></span>

<span data-ttu-id="21686-122">术语 *资源角色* 指的是要对项目执行一组特定任务的人员必须拥有的一组技能、资格和认证。</span><span class="sxs-lookup"><span data-stu-id="21686-122">The term *resource role* refers to a set of skills, competencies, and certifications that a person must have to perform a specific set of tasks on a project.</span></span>

<span data-ttu-id="21686-123">人力资源时间的报价基于资源在特定项目中的角色。</span><span class="sxs-lookup"><span data-stu-id="21686-123">Human resources time is quoted based on the role that a resource fills on a specific project.</span></span> <span data-ttu-id="21686-124">对于人力资源时间，基于资源角色确定成本和记帐。</span><span class="sxs-lookup"><span data-stu-id="21686-124">For human resource time, costing and billing is based on resource role.</span></span> <span data-ttu-id="21686-125">可以使用 **时间** 计价单位组中的任何计价单位为时间定价。</span><span class="sxs-lookup"><span data-stu-id="21686-125">Time can be priced in any unit in the **Time** unit group.</span></span>

<span data-ttu-id="21686-126">在安装 Project Operations 时，将创建 **时间** 计价单位组。</span><span class="sxs-lookup"><span data-stu-id="21686-126">The **Time** unit group is created when you install Project Operations.</span></span> <span data-ttu-id="21686-127">其默认计价单位为 **小时** 。</span><span class="sxs-lookup"><span data-stu-id="21686-127">It has a default unit of **Hour**.</span></span> <span data-ttu-id="21686-128">不能删除、重命名或编辑 **时间** 计价单位组或 **时间** 计价单位的属性。</span><span class="sxs-lookup"><span data-stu-id="21686-128">You can't delete, rename, or edit the attributes fo the **Time** unit group or the **Hour** unit.</span></span> <span data-ttu-id="21686-129">但是，可以向 **时间** 计价单位组添加其他计价单位。</span><span class="sxs-lookup"><span data-stu-id="21686-129">However, you can add other units to the **Time** unit group.</span></span> <span data-ttu-id="21686-130">如果尝试删除 **时间** 计价单位组或 **小时** 计价单位，可能会导致业务逻辑出错。</span><span class="sxs-lookup"><span data-stu-id="21686-130">If you try to delete either the **Time** unit group or the **Hour** unit, you might cause failures in the business logic.</span></span>
 
## <a name="transaction-categories-and-expense-categories"></a><span data-ttu-id="21686-131">交易类别和支出类别</span><span class="sxs-lookup"><span data-stu-id="21686-131">Transaction categories and expense categories</span></span>

<span data-ttu-id="21686-132">项目顾问产生，并且会记帐到客户头上的旅行和其他支出。</span><span class="sxs-lookup"><span data-stu-id="21686-132">Travel and other expenses that project consultants incur are billed to the customer.</span></span> <span data-ttu-id="21686-133">支出类别的定价使用价目表完成。</span><span class="sxs-lookup"><span data-stu-id="21686-133">Pricing of expense categories is completed by using price lists.</span></span> <span data-ttu-id="21686-134">例如，机票、酒店和租车就属于支出类别。</span><span class="sxs-lookup"><span data-stu-id="21686-134">Airfare, hotel, and car rental are examples fo expense categories.</span></span> <span data-ttu-id="21686-135">支出的每项价目表明细指定特定支出类别的定价。</span><span class="sxs-lookup"><span data-stu-id="21686-135">Each price list line for expenses specifies pricing for a specific expense category.</span></span> <span data-ttu-id="21686-136">以下三种方法用于价格支出类别：</span><span class="sxs-lookup"><span data-stu-id="21686-136">The following three methods are used to price expense categories:</span></span>

- <span data-ttu-id="21686-137">**按成本** ：按支出成本对客户记帐，不加价。</span><span class="sxs-lookup"><span data-stu-id="21686-137">**At cost** : The expense cost is billed to the customer, and no markup is applied.</span></span>
- <span data-ttu-id="21686-138">**加价百分比** ：在实际成本的基础上对客户按加价百分比记帐。</span><span class="sxs-lookup"><span data-stu-id="21686-138">**Markup percentage** : The percentage over the actual cost is billed to the customer.</span></span> 
- <span data-ttu-id="21686-139">**单价** ：为每个支出类别单位设置记帐价格。</span><span class="sxs-lookup"><span data-stu-id="21686-139">**Price per unit** : A billing price is set for each unit of the expense category.</span></span> <span data-ttu-id="21686-140">对客户记帐的金额根据顾问报告的支出单位数量计算。</span><span class="sxs-lookup"><span data-stu-id="21686-140">The amount that is billed ot the customer is calculated based on the number of expense units that the consultant reports.</span></span> <span data-ttu-id="21686-141">英里数使用单价定价方法。</span><span class="sxs-lookup"><span data-stu-id="21686-141">Mileage uses the price-per-unit pricing method.</span></span> <span data-ttu-id="21686-142">例如，可以将英里数支出类别配置为每天 30 美元 (USD) 或每英里 2 美元。</span><span class="sxs-lookup"><span data-stu-id="21686-142">For example, the mileage expense category can be configured for 30 US dollars (USD) per day or 2 USD per mile.</span></span> <span data-ttu-id="21686-143">当顾问为项目报告英里数时，记帐金额基于顾问报告的英里数计算。</span><span class="sxs-lookup"><span data-stu-id="21686-143">When a consultant reports mileage on a project, the amount to bill is calculated based on the number of miles that the consultant reported.</span></span>
 
## <a name="project-sales-pricing-and-overrides"></a><span data-ttu-id="21686-144">项目销售定价和替代</span><span class="sxs-lookup"><span data-stu-id="21686-144">Project sales pricing and overrides</span></span>

<span data-ttu-id="21686-145">对于项目报价单和合同，项目价目表采用的价格替代模式与产品价目表采用的不同。</span><span class="sxs-lookup"><span data-stu-id="21686-145">For project quotes and contracts, a project price list has a different price override pattern than a product price list.</span></span> <span data-ttu-id="21686-146">在基于产品目录的报价单明细中，可以直接替代报价单明细中角色和类别的价格，因为每项报价单明细都正好指向一个目录项。</span><span class="sxs-lookup"><span data-stu-id="21686-146">On a product catalog–based quote line, you can override the price to roles and categories directly on the quote line, because each quote line points to exactly one catalog item.</span></span> <span data-ttu-id="21686-147">但是，在基于项目的报价单明细中，不能直接替代报价单明细中的角色和类别的价格。</span><span class="sxs-lookup"><span data-stu-id="21686-147">However, on a project-based quote line, you can't override the price to roles and categories directly on the quote line.</span></span> <span data-ttu-id="21686-148">使用项目价目表支持两种不同的替代模式。</span><span class="sxs-lookup"><span data-stu-id="21686-148">Use the project price list to support the two distinct override patterns.</span></span>

> [!NOTE]
> <span data-ttu-id="21686-149">建议您为项目资源和目录项设置单独的价目表，因为在您替代定价时，这两者的行为不同。</span><span class="sxs-lookup"><span data-stu-id="21686-149">We recommend that you have a separate price list for your project resources and your catalog items, because of the behavior differences between the two when you override pricing.</span></span>

<span data-ttu-id="21686-150">对于项目定价，下面的每个实体可以有一个或多个关联的销售价目表：</span><span class="sxs-lookup"><span data-stu-id="21686-150">Each of the following entities can have one or more associated sales price lists for project pricing:</span></span>

- <span data-ttu-id="21686-151">客户（帐户）</span><span class="sxs-lookup"><span data-stu-id="21686-151">Customer (account)</span></span> 
- <span data-ttu-id="21686-152">商机</span><span class="sxs-lookup"><span data-stu-id="21686-152">Opportunity</span></span> 
- <span data-ttu-id="21686-153">报价单</span><span class="sxs-lookup"><span data-stu-id="21686-153">Quote</span></span> 
- <span data-ttu-id="21686-154">项目合同</span><span class="sxs-lookup"><span data-stu-id="21686-154">Project Contract</span></span>

<span data-ttu-id="21686-155">这些实体与价目表之间的关联通过项目价目表指示。</span><span class="sxs-lookup"><span data-stu-id="21686-155">The association of these entities with a price list is indicated by the project price lists.</span></span> <span data-ttu-id="21686-156">可以将一个或多个价目表与客户、商机、报价单和项目合同销售实体关联。</span><span class="sxs-lookup"><span data-stu-id="21686-156">You can associate one or more price lists with the Customer, Opportunity, Quote, and Project Contract sales entities.</span></span>

<span data-ttu-id="21686-157">不会在客户记录中自动输入默认项目价目表。</span><span class="sxs-lookup"><span data-stu-id="21686-157">A default project price list isn't automatically entered on a customer record.</span></span> <span data-ttu-id="21686-158">但是，可以手动向客户记录附加项目价目表。</span><span class="sxs-lookup"><span data-stu-id="21686-158">However, you can manually attach a project price list to the customer record.</span></span> <span data-ttu-id="21686-159">尽管如此，还是仅当与客户之间存在自定义定价协议时，才应手动附加项目价目表。</span><span class="sxs-lookup"><span data-stu-id="21686-159">Nevertheless, you should manually attach a project price list only when you have a custom pricing agreement with the customer.</span></span> 

<span data-ttu-id="21686-160">如果向销售实体附加项目价目表，将验证以下信息：</span><span class="sxs-lookup"><span data-stu-id="21686-160">When a project price list is attached to a sales entity, the following information is validated:</span></span>

- <span data-ttu-id="21686-161">价目表有 **销售** 上下文。</span><span class="sxs-lookup"><span data-stu-id="21686-161">The price list has a context of **Sales**.</span></span> 
- <span data-ttu-id="21686-162">价目表货币与客户货币匹配。</span><span class="sxs-lookup"><span data-stu-id="21686-162">The price list currency matches the customer currency.</span></span> 

<span data-ttu-id="21686-163">在项目合同中，使用以下优先顺序自动设置相关项目价目表：</span><span class="sxs-lookup"><span data-stu-id="21686-163">On a project contract, the following order of precedence to automatically set related project price lists:</span></span>

1. <span data-ttu-id="21686-164">报价单</span><span class="sxs-lookup"><span data-stu-id="21686-164">Quote</span></span>
2. <span data-ttu-id="21686-165">商机​​</span><span class="sxs-lookup"><span data-stu-id="21686-165">Opportunity</span></span>
3. <span data-ttu-id="21686-166">客户</span><span class="sxs-lookup"><span data-stu-id="21686-166">Customer</span></span> 
4. <span data-ttu-id="21686-167">全局设置</span><span class="sxs-lookup"><span data-stu-id="21686-167">Global settings</span></span> 

<span data-ttu-id="21686-168">默认输入项目价目表时，系统将验证货币是否匹配客户的货币，以及已输入的默认价目表是否有 **销售** 上下文。</span><span class="sxs-lookup"><span data-stu-id="21686-168">When a project price list is entered by default, the system validates that the currency matches the customer’s currency, and that the default price lists that have been entered have a context of **Sales**.</span></span>

<span data-ttu-id="21686-169">可以将多个项目价目表与客户、商机、报价单和项目合同实体关联。</span><span class="sxs-lookup"><span data-stu-id="21686-169">You can associate multiple project price lists with the Customer, Opportunity, Quote, and Project Contract entities.</span></span> <span data-ttu-id="21686-170">此功能支持为长期开展的项目合同设置特定于日期的默认价格，在此情况下，可能需要多个价目表来纳入通货膨胀导致的价格更新。</span><span class="sxs-lookup"><span data-stu-id="21686-170">This capability supports date-specific default prices for a long-running project contract, where you might require more than one price list to account for price updates that occur because of inflation.</span></span> <span data-ttu-id="21686-171">但是，如果与客户、商机、报价单或项目合同实体关联的价目表存在重合时效，默认价格可能不正确。</span><span class="sxs-lookup"><span data-stu-id="21686-171">However, if the price lists that you associate with the Customer, Opportunity, Quote, or Project Contract entity have overlapping date effectivity, the default prices might be incorrect.</span></span> <span data-ttu-id="21686-172">因此，应确保不将具有重合时效的项目价目表与这些实体关联。</span><span class="sxs-lookup"><span data-stu-id="21686-172">Therefore, you should make sure that project price lists that have overlapping date effectivity aren't associated with those entities.</span></span>

### <a name="deal-specific-price-overrides"></a><span data-ttu-id="21686-173">交易特定的价格替代</span><span class="sxs-lookup"><span data-stu-id="21686-173">Deal-specific price overrides</span></span>

<span data-ttu-id="21686-174">您可为报价单或项目合同中默认输入的项目价目表中所选价格创建交易特定的替代。</span><span class="sxs-lookup"><span data-stu-id="21686-174">You can create deal-specific overrides for selected prices on project price lists that are entered by default on a quote or project contract.</span></span>

<span data-ttu-id="21686-175">默认情况下，项目合同始终会获取基础销售价目表的副本，而不是其直接链接。</span><span class="sxs-lookup"><span data-stu-id="21686-175">By default, a project contract always gets a copy of the master sales price list instead of a direct link to it.</span></span> <span data-ttu-id="21686-176">此行为可以帮助确保在基础价目表改变时，与客户就工作说明书 (SOW) 达成的价格协议不变。</span><span class="sxs-lookup"><span data-stu-id="21686-176">This behavior helps guarantee that price agreements that are made with a customer for a statement of work (SOW) don't change if the master price list is changed.</span></span>

<span data-ttu-id="21686-177">但是，在报价单中，可以使用基础价目表。</span><span class="sxs-lookup"><span data-stu-id="21686-177">However, on a quote, you can use a master price list.</span></span> <span data-ttu-id="21686-178">也可以复制基础价目表并进行编辑，以便创建仅适用于该报价单的自定义价目表。</span><span class="sxs-lookup"><span data-stu-id="21686-178">Alternatively, you can copy a master price list and edit it to create a custom price list that applies only to that quote.</span></span> <span data-ttu-id="21686-179">若要创建特定于某个报价单的新价目表，请在 **报价单** 页中选择 **创建自定义报价** 。</span><span class="sxs-lookup"><span data-stu-id="21686-179">To create a new price list that is specific to a quote, on the **Quote** page, select **Create custom pricing**.</span></span> <span data-ttu-id="21686-180">只能从报价单访问交易特定的项目价目表。</span><span class="sxs-lookup"><span data-stu-id="21686-180">You can access the deal-specific project price list only from the quote.</span></span> 

<span data-ttu-id="21686-181">创建自定义项目价目表时，只会复制价目表的项目组成部分。</span><span class="sxs-lookup"><span data-stu-id="21686-181">When you create a custom project price list, only the project components of the price list are copied.</span></span> <span data-ttu-id="21686-182">换句话说，创建的新价目表是报价单中附加的现有项目价目表的副本，并且这个新价目表只有相关角色价格和交易类别价格。</span><span class="sxs-lookup"><span data-stu-id="21686-182">In other words, a new price list created as a copy of the existing project price list that is attached on the quote, and this new price list has only related role prices and transaction category prices.</span></span>
  
## <a name="tracking-costs"></a><span data-ttu-id="21686-183">跟踪成本</span><span class="sxs-lookup"><span data-stu-id="21686-183">Tracking costs</span></span>

<span data-ttu-id="21686-184">Project Operations 可以跟踪在项目中使用人力资源时间产生的成本。</span><span class="sxs-lookup"><span data-stu-id="21686-184">Project Operations tracks costs for the use of human resource time on projects.</span></span> <span data-ttu-id="21686-185">还可以跟踪项目期间产生的其他支出（如旅行支出）的成本。</span><span class="sxs-lookup"><span data-stu-id="21686-185">It also tracks costs for other expenses that are incurred during the project, such as travel expenses.</span></span>

<span data-ttu-id="21686-186">和记帐费率一样，也使用价目表设置人力资源的成本费率。</span><span class="sxs-lookup"><span data-stu-id="21686-186">Like bill rates, cost rates for human resources are also set up using price lists.</span></span> <span data-ttu-id="21686-187">下面是成本价目表与销售额价目表行为之间的主要差别：</span><span class="sxs-lookup"><span data-stu-id="21686-187">Here are the main differences in the behavior of the cost price list and sales price list:</span></span>

- <span data-ttu-id="21686-188">不能替代特定产品、合同或报价单的资源成本费率。</span><span class="sxs-lookup"><span data-stu-id="21686-188">The cost rate of a resource can’t be overridden on a specific project, contract, or quote.</span></span> <span data-ttu-id="21686-189">但是，如果进行了特定于交易性质的更改，则可以按交易替代记帐费率。</span><span class="sxs-lookup"><span data-stu-id="21686-189">However, bill rates can be overridden on a per-deal basis if changes are made that are specific to the nature of the deal.</span></span> 

- <span data-ttu-id="21686-190">解析成本价目表时采用以下顺序：</span><span class="sxs-lookup"><span data-stu-id="21686-190">The following order is used to resolve a cost price list:</span></span>

    1. <span data-ttu-id="21686-191">附加到部门的成本价目表。</span><span class="sxs-lookup"><span data-stu-id="21686-191">The cost price list that is attached to the organizational unit.</span></span>
    2. <span data-ttu-id="21686-192">附加到 Project Operations 参数的成本价目表。</span><span class="sxs-lookup"><span data-stu-id="21686-192">The cost price list that is attached to the Project Operations parameters.</span></span> <span data-ttu-id="21686-193">因为可以将大量不同货币的成本价目表附加到参数，所以会在项目、合同或报价单的合同签订部门的货币与成本价目表的货币之间完成货币匹配。</span><span class="sxs-lookup"><span data-stu-id="21686-193">Because cost price lists in many different currencies can be attached to the parameters, a currency match is completed between the currency of the contracting organizational unit of the project, contract, or quote, and the currency of the cost price list.</span></span>
    3. <span data-ttu-id="21686-194">对于支出，按成本定价方法和成本加价定价方法不适用于成本价目表。</span><span class="sxs-lookup"><span data-stu-id="21686-194">For expenses, the at-cost and markup-over-cost pricing methods don’t apply to cost price lists.</span></span> <span data-ttu-id="21686-195">即使在成本价目表明细中使用这些定价方法设置交易类别成本，系统也会忽略这些定价方法，并且不输入任何默认成本费。</span><span class="sxs-lookup"><span data-stu-id="21686-195">Even if these pricing methods are used on cost price list lines to set up transaction category costs, the system ignores them, and no default cost price is entered.</span></span>
