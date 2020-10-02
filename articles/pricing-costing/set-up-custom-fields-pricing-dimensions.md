---
title: 将自定义字段设置为定价维度
description: 此主题提供有关如何使用自定义字段设置定价维度的信息。
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: rumant
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 3a2a3b48df02853e519a45dc1d37052c8ba2529d
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/28/2020
ms.locfileid: "3896585"
---
# <a name="set-up-custom-fields-as-pricing-dimensions"></a><span data-ttu-id="e0c5f-103">将自定义字段设置为定价维度</span><span class="sxs-lookup"><span data-stu-id="e0c5f-103">Set up custom fields as pricing dimensions</span></span>

<span data-ttu-id="e0c5f-104">_**适用于：** 基于资源/非库存场景的 Project Operations，精简部署 - 估价开票交易_</span><span class="sxs-lookup"><span data-stu-id="e0c5f-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="e0c5f-105">首先，此主题假设您已完成了主题[创建自定义字段和实体](create-custom-fields-entities-pricing-dimensions.md)和[向价格设置和交易实体添加所需自定义字段](add-custom-fields-price-setup-transactional-entities.md)中的过程。</span><span class="sxs-lookup"><span data-stu-id="e0c5f-105">Before you begin, this topic assumes that you have completed the procedures in the topics, [Create custom fields and entities](create-custom-fields-entities-pricing-dimensions.md) and [Add required custom fields to price setup and transactional entities](add-custom-fields-price-setup-transactional-entities.md).</span></span> <span data-ttu-id="e0c5f-106">如果尚未完成这些过程，请回去完成，然后回到此主题。</span><span class="sxs-lookup"><span data-stu-id="e0c5f-106">If you haven't completed those procedures, go back and complete them and then return to this topic.</span></span> 

<span data-ttu-id="e0c5f-107">此主题介绍如何设置自定义定价维度。</span><span class="sxs-lookup"><span data-stu-id="e0c5f-107">This topic provides information about setting up custom pricing dimensions.</span></span> <span data-ttu-id="e0c5f-108">在**参数**页上，**基于金额的定价维度**选项卡显示定价维度实体中的记录。</span><span class="sxs-lookup"><span data-stu-id="e0c5f-108">On the **Parameters** page, the **Amount-Based Pricing Dimensions** tab shows the records in the pricing dimension entities.</span></span> <span data-ttu-id="e0c5f-109">默认情况下，此选项卡上的网格中有两行：</span><span class="sxs-lookup"><span data-stu-id="e0c5f-109">By default, there are two rows in the grid on this tab:</span></span>

- <span data-ttu-id="e0c5f-110">**msdyn_resourcecategory**（角色）</span><span class="sxs-lookup"><span data-stu-id="e0c5f-110">**msdyn_resourcecategory** (Role)</span></span>
- <span data-ttu-id="e0c5f-111">**msdyn_OrganizationalUnit**（部门）</span><span class="sxs-lookup"><span data-stu-id="e0c5f-111">**msdyn_OrganizationalUnit** (Organizational Unit)</span></span>

> [!IMPORTANT]
> <span data-ttu-id="e0c5f-112">请勿删除这些行。</span><span class="sxs-lookup"><span data-stu-id="e0c5f-112">Do not delete these rows.</span></span> <span data-ttu-id="e0c5f-113">但是如果不需要，可以通过将**适用于成本**、**适用于销售**和**适用于购买**全部设置为**否**，使其在特定上下文中不可用。</span><span class="sxs-lookup"><span data-stu-id="e0c5f-113">However, if you do not need them, you can make them not applicable in a specific context by setting **Applicable to Cost**, **Applicable to Sales**, and **Applicable to Purchase** all to **No**.</span></span> <span data-ttu-id="e0c5f-114">将这些属性值设置为**否**与将该字段设置为定价维度的效果相同。</span><span class="sxs-lookup"><span data-stu-id="e0c5f-114">Setting these attribute values to **No** has the same effect of not having the field as a pricing dimension.</span></span>

<span data-ttu-id="e0c5f-115">要使字段成为定价维度，该字段必须：</span><span class="sxs-lookup"><span data-stu-id="e0c5f-115">For a field to become a pricing dimension, it must be:</span></span>

- <span data-ttu-id="e0c5f-116">创建为**角色价格**和**角色价格加价**实体中的字段。</span><span class="sxs-lookup"><span data-stu-id="e0c5f-116">Created as a field in the **Role Price** and **Role Price markup** entities.</span></span> <span data-ttu-id="e0c5f-117">有关如何执行此操作的详细信息，请参阅[向价格设置和交易实体添加自定义字段](add-custom-fields-price-setup-transactional-entities.md)。</span><span class="sxs-lookup"><span data-stu-id="e0c5f-117">For more information on how to do this, see [Add custom fields to price setup and transactional entities](add-custom-fields-price-setup-transactional-entities.md).</span></span>
- <span data-ttu-id="e0c5f-118">创建为**定价维度**表中的行。</span><span class="sxs-lookup"><span data-stu-id="e0c5f-118">Created as a row in the **Pricing Dimension** table.</span></span> <span data-ttu-id="e0c5f-119">例如，添加定价维度行，如下图中所示。</span><span class="sxs-lookup"><span data-stu-id="e0c5f-119">For example, add pricing dimension rows as shown in the following graphic.</span></span> 

<span data-ttu-id="e0c5f-120">资源工作时间 (**msdyn_resourceworkhours**) 已作为基于加价的维度添加，并已添加到**基于加价的定价维度**选项卡上的网格中。</span><span class="sxs-lookup"><span data-stu-id="e0c5f-120">Resource Work hours (**msdyn_resourceworkhours**) is added as a markup-based dimension and has been added to the grid on the **Markup Based Pricing Dimension** tab.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="e0c5f-121">仅当刷新了缓存，才会把对此表中定价维度数据进行的任何更改传播到定价业务逻辑。</span><span class="sxs-lookup"><span data-stu-id="e0c5f-121">Any change to pricing dimension data in this table, existing or new, is propagated to the pricing business logic only after the cache is refreshed.</span></span> <span data-ttu-id="e0c5f-122">缓存刷新时间最多可能需要 10 分钟。</span><span class="sxs-lookup"><span data-stu-id="e0c5f-122">The cache refresh time may take up to 10 minutes.</span></span> <span data-ttu-id="e0c5f-123">留出这样长的时间，以便查看一定会导致定价维度数据更改的价格默认设置逻辑更改。</span><span class="sxs-lookup"><span data-stu-id="e0c5f-123">Allow that length of time to see the changes in price defaulting logic that must result from changes to the Pricing Dimension data.</span></span>


## <a name="attributes-of-the-pricing-dimensions-table"></a><span data-ttu-id="e0c5f-124">“定价维度”表的属性</span><span class="sxs-lookup"><span data-stu-id="e0c5f-124">Attributes of the Pricing Dimensions table</span></span>
<span data-ttu-id="e0c5f-125">以下部分介绍**定价维度**表中的不同属性。</span><span class="sxs-lookup"><span data-stu-id="e0c5f-125">The following sections provide information about the different attributes in the **Pricing Dimensions** table.</span></span>

### <a name="pricing-dimension-name"></a><span data-ttu-id="e0c5f-126">定价维度名称</span><span class="sxs-lookup"><span data-stu-id="e0c5f-126">Pricing Dimension Name</span></span>
<span data-ttu-id="e0c5f-127">此值应该与添加到自定义定价维度的**角色价格**表中的字段的架构名称完全相同。</span><span class="sxs-lookup"><span data-stu-id="e0c5f-127">This value should be the exact same as the schema name of the field that is added to the **Role Price** table for custom pricing dimensions.</span></span> <span data-ttu-id="e0c5f-128">有关将字段添加到**角色价格**表的详细信息，请参阅[向价格设置和交易实体添加自定义字段](add-custom-fields-price-setup-transactional-entities.md)。</span><span class="sxs-lookup"><span data-stu-id="e0c5f-128">For more information about adding fields to the **Role Price** table, see [Add custom fields to price setup and transactional entities](add-custom-fields-price-setup-transactional-entities.md).</span></span>

### <a name="type-of-dimension"></a><span data-ttu-id="e0c5f-129">维度类型</span><span class="sxs-lookup"><span data-stu-id="e0c5f-129">Type of dimension</span></span>
<span data-ttu-id="e0c5f-130">有两种类型的定价维度：</span><span class="sxs-lookup"><span data-stu-id="e0c5f-130">There are two types of pricing dimensions:</span></span>
  
  - <span data-ttu-id="e0c5f-131">**基于金额的维度**：将把来自输入上下文的维度值与**角色价格**明细中的维度值进行匹配，而默认价格/成本则直接从**角色价格**表中提取。</span><span class="sxs-lookup"><span data-stu-id="e0c5f-131">**Amount-based dimensions**: The dimension values from the input context are matched to the dimension values on **Role Price** line and the price/cost is defaulted directly from the **Role Price** table.</span></span>
  - <span data-ttu-id="e0c5f-132">**基于加价的维度**：在这些维度中，使用下面的三步式流程获取价格/成本：</span><span class="sxs-lookup"><span data-stu-id="e0c5f-132">**Markup-based dimensions**: These are dimensions where the following three-step process to get the price/cost is used:</span></span>
 
    1. <span data-ttu-id="e0c5f-133">来自输入上下文的基于非加价的维度值将与角色价格明细进行匹配以获取基础费率。</span><span class="sxs-lookup"><span data-stu-id="e0c5f-133">The non-markup-based dimension values from the input context are matched to the Role Price line to get the base rate.</span></span>
    2. <span data-ttu-id="e0c5f-134">来自输入上下文的维度值将与**角色价格加价**明细进行匹配以获取加价百分比。</span><span class="sxs-lookup"><span data-stu-id="e0c5f-134">The dimension values from the input context are matched to the **Role Price Markup** line to get a markup percentage.</span></span>
    3. <span data-ttu-id="e0c5f-135">第二步的加价百分比将应用于第一步中从**角色价格**表获取的基础费率以获取最终价格/成本。</span><span class="sxs-lookup"><span data-stu-id="e0c5f-135">The markup percentage from the second step is applied to the base rate obtained from the **Role Price** table in the first step to arrive at final price/cost.</span></span>
   
   <span data-ttu-id="e0c5f-136">下表介绍价格加价的计算。</span><span class="sxs-lookup"><span data-stu-id="e0c5f-136">The following table illustrates the calculation of price markups.</span></span>
  
| <span data-ttu-id="e0c5f-137">角色</span><span class="sxs-lookup"><span data-stu-id="e0c5f-137">Role</span></span>        | <span data-ttu-id="e0c5f-138">部门</span><span class="sxs-lookup"><span data-stu-id="e0c5f-138">Org Unit</span></span>    |<span data-ttu-id="e0c5f-139">工作位置</span><span class="sxs-lookup"><span data-stu-id="e0c5f-139">Work Location</span></span>      |<span data-ttu-id="e0c5f-140">标准标题</span><span class="sxs-lookup"><span data-stu-id="e0c5f-140">Standard Title</span></span>      |<span data-ttu-id="e0c5f-141">资源工作时间</span><span class="sxs-lookup"><span data-stu-id="e0c5f-141">Resource Work Hours</span></span>      |  <span data-ttu-id="e0c5f-142">加价</span><span class="sxs-lookup"><span data-stu-id="e0c5f-142">Mark Up</span></span>|
| ------------|-------------|-------------------|--------------------|-------------------------|--------:|
|             | <span data-ttu-id="e0c5f-143">Contoso 印度</span><span class="sxs-lookup"><span data-stu-id="e0c5f-143">Contoso India</span></span>|<span data-ttu-id="e0c5f-144">现场</span><span class="sxs-lookup"><span data-stu-id="e0c5f-144">Onsite</span></span>            |                    |<span data-ttu-id="e0c5f-145">加班</span><span class="sxs-lookup"><span data-stu-id="e0c5f-145">Overtime</span></span>                 |<span data-ttu-id="e0c5f-146">15</span><span class="sxs-lookup"><span data-stu-id="e0c5f-146">15</span></span>     |
|             | <span data-ttu-id="e0c5f-147">Contoso 印度</span><span class="sxs-lookup"><span data-stu-id="e0c5f-147">Contoso India</span></span>|<span data-ttu-id="e0c5f-148">本地</span><span class="sxs-lookup"><span data-stu-id="e0c5f-148">Local</span></span>             |                    |<span data-ttu-id="e0c5f-149">加班</span><span class="sxs-lookup"><span data-stu-id="e0c5f-149">Overtime</span></span>                 |<span data-ttu-id="e0c5f-150">10</span><span class="sxs-lookup"><span data-stu-id="e0c5f-150">10</span></span>     |
|             | <span data-ttu-id="e0c5f-151">Contoso US</span><span class="sxs-lookup"><span data-stu-id="e0c5f-151">Contoso US</span></span>   |<span data-ttu-id="e0c5f-152">本地</span><span class="sxs-lookup"><span data-stu-id="e0c5f-152">Local</span></span>             |                    |<span data-ttu-id="e0c5f-153">加班</span><span class="sxs-lookup"><span data-stu-id="e0c5f-153">Overtime</span></span>                 |<span data-ttu-id="e0c5f-154">20</span><span class="sxs-lookup"><span data-stu-id="e0c5f-154">20</span></span>     |


<span data-ttu-id="e0c5f-155">如果 Contoso 印度中一位基础费率为 100 美元的资源在现场工作，并且在时间条目中记录了 8 小时的正常工时和 2 小时的加班，定价引擎将对 8 小时使用基础费率 100，从而记录 800 美元。</span><span class="sxs-lookup"><span data-stu-id="e0c5f-155">If a resource from Contoso India whose base rate is 100 USD is working onsite, and they log 8 hours of Regular time and 2 hours of overtime on the time entry, the pricing engine will use the base rate of 100 for the 8 hours to record 800 USD.</span></span> <span data-ttu-id="e0c5f-156">至于 2 小时的加班，则为基础费率 100 应用 15% 的加价，因此单价为 115 美元，记录的总成本为 230 美元。</span><span class="sxs-lookup"><span data-stu-id="e0c5f-156">For the 2 hours overtime, a markup of 15% will be applied to the base rate of 100 to get a unit price of 115 USD and will record a total cost of 230 USD.</span></span>

### <a name="applicable-to-cost"></a><span data-ttu-id="e0c5f-157">适用于成本</span><span class="sxs-lookup"><span data-stu-id="e0c5f-157">Applicable to Cost</span></span> 
<span data-ttu-id="e0c5f-158">如果此项设置为**是**，则指示在检索成本和加价费率时，应将来自输入上下文的维度值用于匹配**角色价格**和**角色价格加价**。</span><span class="sxs-lookup"><span data-stu-id="e0c5f-158">If this is set to **Yes**, it indicates that the dimension value from the input context should be used to match to the **Role Price** and **Role Price Markup** when retrieving the cost and markup rates.</span></span>

### <a name="applicable-to-sales"></a><span data-ttu-id="e0c5f-159">适用于销售</span><span class="sxs-lookup"><span data-stu-id="e0c5f-159">Applicable to Sales</span></span>
<span data-ttu-id="e0c5f-160">如果此项设置为**是**，则指示在检索记帐和加价费率时，应将来自输入上下文的维度值用于匹配**角色价格**和**角色价格加价**。</span><span class="sxs-lookup"><span data-stu-id="e0c5f-160">If this is set to **Yes**, it indicates that the dimension value from the input context should be used to match to the **Role Price** and **Role Price Markup** when retrieving the bill and markup rates.</span></span>

### <a name="applicable-to-purchase"></a><span data-ttu-id="e0c5f-161">适用于购买</span><span class="sxs-lookup"><span data-stu-id="e0c5f-161">Applicable to Purchase</span></span>
<span data-ttu-id="e0c5f-162">如果此项设置为**是**，则指示在检索购买价格时，应将来自输入上下文的维度值用于匹配**角色价格**和**角色价格加价**。</span><span class="sxs-lookup"><span data-stu-id="e0c5f-162">If this is set to **Yes**, it indicates that the dimension value from the input context should be used to match to the **Role Price** and **Role Price Markup** when retrieving the purchase price.</span></span> <span data-ttu-id="e0c5f-163">不支持分包方案，因此不使用此字段。</span><span class="sxs-lookup"><span data-stu-id="e0c5f-163">Subcontracting scenarios are not supported, so this field is not used.</span></span> 

### <a name="priority"></a><span data-ttu-id="e0c5f-164">优先级</span><span class="sxs-lookup"><span data-stu-id="e0c5f-164">Priority</span></span>
<span data-ttu-id="e0c5f-165">设置维度优先级有助于定价生成价格，即使无法找到输入维度值与**角色价格**或**角色价格加价**表中的值之间的精确匹配项也不例外。</span><span class="sxs-lookup"><span data-stu-id="e0c5f-165">Setting the dimension priority helps pricing produce a price even when it can't find an exact match between the input dimension values and the values from the **Role Price** or **Role Price Markup** tables.</span></span> <span data-ttu-id="e0c5f-166">在此方案中，将通过按照维度的优先级为维度加权，对不匹配维度值使用空值。</span><span class="sxs-lookup"><span data-stu-id="e0c5f-166">In this scenario, null values are used for unmatched dimension values by weighing the dimensions in order of their priority.</span></span>

- <span data-ttu-id="e0c5f-167">**成本优先级**：维度的成本优先级值指示与成本价格设置进行匹配时，该维度的权重。</span><span class="sxs-lookup"><span data-stu-id="e0c5f-167">**Cost Priority**: The value of a dimension's cost priority will indicate the weight of that dimension when matching against the setup of cost prices.</span></span> <span data-ttu-id="e0c5f-168">**成本优先级**的值在**适用于成本**的维度之间必须唯一。</span><span class="sxs-lookup"><span data-stu-id="e0c5f-168">The value of **Cost Priority** must be unique across dimensions that are **Applicable to Cost**.</span></span>
- <span data-ttu-id="e0c5f-169">**销售优先级**：维度的销售优先级值指示与销售价格设置进行匹配时，该维度的权重。</span><span class="sxs-lookup"><span data-stu-id="e0c5f-169">**Sales Priority**: The value of dimension's sales priority will indicate the weight of that dimension when matching against the setup of sales prices or bill rates.</span></span> <span data-ttu-id="e0c5f-170">**销售优先级**的值在**适用于销售**的维度之间必须唯一。</span><span class="sxs-lookup"><span data-stu-id="e0c5f-170">The value of **Sales Priority** must be unique across dimensions that are **Applicable to Sales**.</span></span>
