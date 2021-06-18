---
title: 将自定义字段设置为定价维度
description: 此主题介绍如何设置自定义定价维度。
author: Rumant
ms.custom:
- dyn365-projectservice
ms.date: 11/20/2018
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: cce3a3fe6aef247380f6284f58d49337f969c38c
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/10/2021
ms.locfileid: "6008300"
---
# <a name="setting-up-custom-fields-as-pricing-dimensions"></a><span data-ttu-id="cf262-103">将自定义字段设置为定价维度</span><span class="sxs-lookup"><span data-stu-id="cf262-103">Setting up custom fields as pricing dimensions</span></span> 

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="cf262-104">首先，此主题假设您已完成了主题[创建自定义字段和实体](create-custom-fields-entities.md)和[向价格设置和交易实体添加自定义字段](field-references.md)中的过程。</span><span class="sxs-lookup"><span data-stu-id="cf262-104">Before you begin, this topic assumes that you have completed the procedures in the topics, [Create custom fields and entities](create-custom-fields-entities.md) and [Add custom fields to price setup and transactional entities](field-references.md).</span></span> <span data-ttu-id="cf262-105">如果尚未完成这些过程，请回去完成，然后回到此主题。</span><span class="sxs-lookup"><span data-stu-id="cf262-105">If you haven't completed those procedures, go back and complete them and then return to this topic.</span></span> 

<span data-ttu-id="cf262-106">此主题介绍如何设置自定义定价维度。</span><span class="sxs-lookup"><span data-stu-id="cf262-106">This topic provides information about setting up custom pricing dimensions.</span></span> <span data-ttu-id="cf262-107">Project Service Web 界面中 **参数** 页 **基于金额的定价维度** 选项卡显示定价维度实体中的记录。</span><span class="sxs-lookup"><span data-stu-id="cf262-107">In the Project Service web interface, on the **Parameters** page, the **Amount-Based Pricing Dimensions** tab shows the records in the pricing dimension entities.</span></span> <span data-ttu-id="cf262-108">默认情况下，安装 Project Service 将在此选项卡上的网格中创建2 行：</span><span class="sxs-lookup"><span data-stu-id="cf262-108">By default, Project Service installation creates 2 rows in the grid on this tab:</span></span>

- <span data-ttu-id="cf262-109">**msdyn_resourcecategory**（角色）</span><span class="sxs-lookup"><span data-stu-id="cf262-109">**msdyn_resourcecategory** (Role)</span></span>
- <span data-ttu-id="cf262-110">**msdyn_OrganizationalUnit**（部门）</span><span class="sxs-lookup"><span data-stu-id="cf262-110">**msdyn_OrganizationalUnit** (Organizational Unit)</span></span>

> [!IMPORTANT]
> <span data-ttu-id="cf262-111">请勿删除这些行。</span><span class="sxs-lookup"><span data-stu-id="cf262-111">Do not delete these rows.</span></span> <span data-ttu-id="cf262-112">但是如果不需要，可以通过将 **适用于成本**、**适用于销售** 和 **适用于购买** 全部设置为 **否**，使其在特定上下文中不可用。</span><span class="sxs-lookup"><span data-stu-id="cf262-112">However, if you do not need them, you can make them not applicable in a specific context by setting **Applicable to Cost**, **Applicable to Sales**, and **Applicable to Purchase** all to **No**.</span></span> <span data-ttu-id="cf262-113">将这些属性值设置为 **否** 与将该字段设置为定价维度的效果相同。</span><span class="sxs-lookup"><span data-stu-id="cf262-113">Setting these attribute values to **No** has the same effect of not having the field as a pricing dimension.</span></span>

<span data-ttu-id="cf262-114">要使字段成为定价维度，该字段必须：</span><span class="sxs-lookup"><span data-stu-id="cf262-114">For a field to become a pricing dimension, it must be:</span></span>

- <span data-ttu-id="cf262-115">创建为 **角色价格** 和 **角色价格加价** 实体中的字段。</span><span class="sxs-lookup"><span data-stu-id="cf262-115">Created as a field in the **Role Price** and **Role Price markup** entities.</span></span> <span data-ttu-id="cf262-116">有关如何执行此操作的详细信息，请参阅[向价格设置和交易实体添加自定义字段](field-references.md)。</span><span class="sxs-lookup"><span data-stu-id="cf262-116">For more information on how to do this, see [Add custom fields to price setup and transactional entities](field-references.md).</span></span>
- <span data-ttu-id="cf262-117">创建为 **定价维度** 表中的行。</span><span class="sxs-lookup"><span data-stu-id="cf262-117">Created as a row in the **Pricing Dimension** table.</span></span> <span data-ttu-id="cf262-118">例如，添加定价维度行，如下图中所示。</span><span class="sxs-lookup"><span data-stu-id="cf262-118">For example, add pricing dimension rows as shown in the following graphic.</span></span> 

![基于金额的定价维度行](media/Amt-based-PD.png)

<span data-ttu-id="cf262-120">请注意，资源工作时间 (**msdyn_resourceworkhours**) 已作为基于加价的维度添加，并已添加到 **基于加价的定价维度** 选项卡上的网格中。</span><span class="sxs-lookup"><span data-stu-id="cf262-120">Notice that Resource Work hours (**msdyn_resourceworkhours**) has been added as a markup-based dimension and has been added to the grid on the **Markup Based Pricing Dimension** tab.</span></span>

![基于加价的定价维度行](media/Markup-based-PD.png)

> [!IMPORTANT]
> <span data-ttu-id="cf262-122">仅当刷新了缓存，才会把对此表中定价维度数据进行的任何更改传播到 Project Service 定价逻辑。</span><span class="sxs-lookup"><span data-stu-id="cf262-122">Any change to pricing dimension data in this table, existing or new, is propagated to the Project Service pricing business logic only after the cache is refreshed.</span></span> <span data-ttu-id="cf262-123">缓存刷新时间最多可能需要 10 分钟。</span><span class="sxs-lookup"><span data-stu-id="cf262-123">The cache refresh time may take up to 10 minutes.</span></span> <span data-ttu-id="cf262-124">留出这样长的时间，以便查看一定会导致定价维度数据更改的价格默认设置逻辑更改。</span><span class="sxs-lookup"><span data-stu-id="cf262-124">Allow that length of time to see the changes in price defaulting logic that must result from changes to the Pricing Dimension data.</span></span>


## <a name="attributes-of-the-pricing-dimensions-table"></a><span data-ttu-id="cf262-125">“定价维度”表的属性</span><span class="sxs-lookup"><span data-stu-id="cf262-125">Attributes of the Pricing Dimensions table</span></span>
<span data-ttu-id="cf262-126">以下部分介绍 **定价维度** 表中的不同属性。</span><span class="sxs-lookup"><span data-stu-id="cf262-126">The following sections provide information about the different attributes in the **Pricing Dimensions** table.</span></span>

### <a name="pricing-dimension-name"></a><span data-ttu-id="cf262-127">定价维度名称</span><span class="sxs-lookup"><span data-stu-id="cf262-127">Pricing Dimension Name</span></span>
<span data-ttu-id="cf262-128">此值应该与添加到自定义定价维度的 **角色价格** 表中的字段的架构名称完全相同。</span><span class="sxs-lookup"><span data-stu-id="cf262-128">This value should be the exact same as the schema name of the field that is added to the **Role Price** table for custom pricing dimensions.</span></span> <span data-ttu-id="cf262-129">有关将字段添加到 **角色价格** 表的详细信息，请参阅[向价格设置和交易实体添加自定义字段](field-references.md)。</span><span class="sxs-lookup"><span data-stu-id="cf262-129">For more information about adding fields to the **Role Price** table, see [Add custom fields to price setup and transactional entities](field-references.md).</span></span>

### <a name="type-of-dimension"></a><span data-ttu-id="cf262-130">维度类型</span><span class="sxs-lookup"><span data-stu-id="cf262-130">Type of dimension</span></span>
<span data-ttu-id="cf262-131">有两种类型的定价维度：</span><span class="sxs-lookup"><span data-stu-id="cf262-131">There are two types of pricing dimensions:</span></span>
  
  - <span data-ttu-id="cf262-132">**基于金额的维度**：将把来自输入上下文的维度值与 **角色价格** 明细中的维度值进行匹配，而默认价格/成本则直接从 **角色价格** 表中提取。</span><span class="sxs-lookup"><span data-stu-id="cf262-132">**Amount-based dimensions**: The dimension values from the input context are matched to the dimension values on **Role Price** line and the price/cost is defaulted directly from the **Role Price** table.</span></span>
  - <span data-ttu-id="cf262-133">**基于加价的维度**：在这些维度中，Project Service 采用下面的三步式流程获取价格/成本。</span><span class="sxs-lookup"><span data-stu-id="cf262-133">**Markup-based dimensions**: These are dimensions where Project Service will adopt the following 3-step process to get the price/cost</span></span>
 
    1. <span data-ttu-id="cf262-134">Project Service 将来自输入上下文的，基于非加价的维度值与角色价格明细进行匹配以获取基础费率。</span><span class="sxs-lookup"><span data-stu-id="cf262-134">Project Service matches the non-markup-based dimension values from the input context to the Role Price line to get the base rate.</span></span>
    2. <span data-ttu-id="cf262-135">Project Service 将来自输入上下文的所有的维度值与 **角色价格加价** 明细进行匹配以获取加价百分比。</span><span class="sxs-lookup"><span data-stu-id="cf262-135">Project Service matches all of the dimension values from the input context to the **Role Price Markup** line to get a markup percentage.</span></span>
    3. <span data-ttu-id="cf262-136">Project Service 将第二步的加价百分比应用于第一步中从 **角色价格** 表获取的基础费率以获取最终价格/成本。</span><span class="sxs-lookup"><span data-stu-id="cf262-136">Project Service applies the markup percentage from the second step to the base rate obtained from the **Role Price** table in the first step to arrive at final price/cost.</span></span>
   
   <span data-ttu-id="cf262-137">下表介绍价格加价的计算。</span><span class="sxs-lookup"><span data-stu-id="cf262-137">The following table illustrates the calculation of price markups.</span></span>
  
| <span data-ttu-id="cf262-138">角色</span><span class="sxs-lookup"><span data-stu-id="cf262-138">Role</span></span>        | <span data-ttu-id="cf262-139">部门</span><span class="sxs-lookup"><span data-stu-id="cf262-139">Org Unit</span></span>    |<span data-ttu-id="cf262-140">工作位置</span><span class="sxs-lookup"><span data-stu-id="cf262-140">Work Location</span></span>      |<span data-ttu-id="cf262-141">标准标题</span><span class="sxs-lookup"><span data-stu-id="cf262-141">Standard Title</span></span>      |<span data-ttu-id="cf262-142">资源工作时间</span><span class="sxs-lookup"><span data-stu-id="cf262-142">Resource Work Hours</span></span>      |  <span data-ttu-id="cf262-143">加价</span><span class="sxs-lookup"><span data-stu-id="cf262-143">Mark Up</span></span>|
| ------------|-------------|-------------------|--------------------|-------------------------|--------:|
|             | <span data-ttu-id="cf262-144">Contoso 印度</span><span class="sxs-lookup"><span data-stu-id="cf262-144">Contoso India</span></span>|<span data-ttu-id="cf262-145">现场</span><span class="sxs-lookup"><span data-stu-id="cf262-145">Onsite</span></span>            |                    |<span data-ttu-id="cf262-146">加班</span><span class="sxs-lookup"><span data-stu-id="cf262-146">Overtime</span></span>                 |<span data-ttu-id="cf262-147">15</span><span class="sxs-lookup"><span data-stu-id="cf262-147">15</span></span>     |
|             | <span data-ttu-id="cf262-148">Contoso 印度</span><span class="sxs-lookup"><span data-stu-id="cf262-148">Contoso India</span></span>|<span data-ttu-id="cf262-149">局部</span><span class="sxs-lookup"><span data-stu-id="cf262-149">Local</span></span>             |                    |<span data-ttu-id="cf262-150">加班</span><span class="sxs-lookup"><span data-stu-id="cf262-150">Overtime</span></span>                 |<span data-ttu-id="cf262-151">10</span><span class="sxs-lookup"><span data-stu-id="cf262-151">10</span></span>     |
|             | <span data-ttu-id="cf262-152">Contoso US</span><span class="sxs-lookup"><span data-stu-id="cf262-152">Contoso US</span></span>   |<span data-ttu-id="cf262-153">局部</span><span class="sxs-lookup"><span data-stu-id="cf262-153">Local</span></span>             |                    |<span data-ttu-id="cf262-154">加班</span><span class="sxs-lookup"><span data-stu-id="cf262-154">Overtime</span></span>                 |<span data-ttu-id="cf262-155">20</span><span class="sxs-lookup"><span data-stu-id="cf262-155">20</span></span>     |


<span data-ttu-id="cf262-156">如果 Contoso 印度中一位基础费率为 100 美元的资源在现场工作，并且在时间条目中记录了 8 小时的正常工时和 2 小时的加班，Project Service 定价引擎将对 8 小时使用基础费率 100，从而记录 800 美元。</span><span class="sxs-lookup"><span data-stu-id="cf262-156">If a resource from Contoso India whose base rate is 100 USD is working onsite, and they log 8 hours of Regular time and 2 hours of overtime on the time entry, the Project Service pricing engine will use the base rate of 100 for the 8 hours to record 800 USD.</span></span> <span data-ttu-id="cf262-157">至于 2 小时的加班，则为基础费率 100 应用 15% 的加价，因此单价为 115 美元，记录的总成本为 230 美元。</span><span class="sxs-lookup"><span data-stu-id="cf262-157">For the 2 hours overtime, a markup of 15% will be applied to the base rate of 100 to get a unit price of 115 USD and will record a total cost of 230 USD.</span></span>

### <a name="applicable-to-cost"></a><span data-ttu-id="cf262-158">适用于成本</span><span class="sxs-lookup"><span data-stu-id="cf262-158">Applicable to Cost</span></span> 
<span data-ttu-id="cf262-159">如果此项设置为 **是**，则指示在检索成本和加价费率时，应将来自输入上下文的维度值用于匹配 **角色价格** 和 **角色价格加价**。</span><span class="sxs-lookup"><span data-stu-id="cf262-159">If this is set to **Yes**, it indicates that the dimension value from the input context should be used to match to the **Role Price** and **Role Price Markup** when retrieving the cost and markup rates.</span></span>

### <a name="applicable-to-sales"></a><span data-ttu-id="cf262-160">适用于销售</span><span class="sxs-lookup"><span data-stu-id="cf262-160">Applicable to Sales</span></span>
<span data-ttu-id="cf262-161">如果此项设置为 **是**，则指示在检索记帐和加价费率时，应将来自输入上下文的维度值用于匹配 **角色价格** 和 **角色价格加价**。</span><span class="sxs-lookup"><span data-stu-id="cf262-161">If this is set to **Yes**, it indicates that the dimension value from the input context should be used to match to the **Role Price** and **Role Price Markup** when retrieving the bill and markup rates.</span></span>

### <a name="applicable-to-purchase"></a><span data-ttu-id="cf262-162">适用于购买</span><span class="sxs-lookup"><span data-stu-id="cf262-162">Applicable to Purchase</span></span>
<span data-ttu-id="cf262-163">如果此项设置为 **是**，则指示在检索购买价格时，应将来自输入上下文的维度值用于匹配 **角色价格** 和 **角色价格加价**。</span><span class="sxs-lookup"><span data-stu-id="cf262-163">If this is set to **Yes**, it indicates that the dimension value from the input context should be used to match to the **Role Price** and **Role Price Markup** when retrieving the purchase price.</span></span> <span data-ttu-id="cf262-164">Project Service 目前不支持分包方案，因此不使用此字段。</span><span class="sxs-lookup"><span data-stu-id="cf262-164">Currently Project Service does not support subcontracting scenarios, so this field is not used.</span></span> 

### <a name="priority"></a><span data-ttu-id="cf262-165">优先级</span><span class="sxs-lookup"><span data-stu-id="cf262-165">Priority</span></span>
<span data-ttu-id="cf262-166">设置维度优先级有助于 Project Service 定价生成价格，即使无法找到输入维度值与 **角色价格** 或 **角色价格加价** 表中的值之间的精确匹配项也不例外。</span><span class="sxs-lookup"><span data-stu-id="cf262-166">Setting the dimension priority helps Project Service pricing produce a price even when it can't find an exact match between the input dimension values and the values from the **Role Price** or **Role Price Markup** tables.</span></span> <span data-ttu-id="cf262-167">在此方案中，Project Service 通过按照维度的优先级为维度加权，对不匹配维度值使用空值。</span><span class="sxs-lookup"><span data-stu-id="cf262-167">In this scenario, Project Service will use null values for unmatched dimension values by weighing the dimensions in order of their priority.</span></span>

- <span data-ttu-id="cf262-168">**成本优先级**：维度的成本优先级值指示与成本价格设置进行匹配时，该维度的权重。</span><span class="sxs-lookup"><span data-stu-id="cf262-168">**Cost Priority**: The value of a dimension's cost priority will indicate the weight of that dimension when matching against the setup of cost prices.</span></span> <span data-ttu-id="cf262-169">**成本优先级** 的值在 **适用于成本** 的维度之间必须唯一。</span><span class="sxs-lookup"><span data-stu-id="cf262-169">The value of **Cost Priority** must be unique across dimensions that are **Applicable to Cost**.</span></span>
- <span data-ttu-id="cf262-170">**销售优先级**：维度的销售优先级值指示与销售价格设置进行匹配时，该维度的权重。</span><span class="sxs-lookup"><span data-stu-id="cf262-170">**Sales Priority**: The value of dimension's sales priority will indicate the weight of that dimension when matching against the setup of sales prices or bill rates.</span></span> <span data-ttu-id="cf262-171">**销售优先级** 的值在 **适用于销售** 的维度之间必须唯一。</span><span class="sxs-lookup"><span data-stu-id="cf262-171">The value of **Sales Priority** must be unique across dimensions that are **Applicable to Sales**.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]