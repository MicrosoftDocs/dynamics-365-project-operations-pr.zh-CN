---
title: 定价维度概述
description: 本主题提供有关 Dynamics 365 Project Operations 中定价维度的信息。
author: rumant
ms.date: 11/30/2020
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 01ba11e34e7d8a59716fa9d8c8be3389ab380048
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/10/2021
ms.locfileid: "6004970"
---
# <a name="pricing-dimensions-overview"></a><span data-ttu-id="9847f-103">定价维度概述</span><span class="sxs-lookup"><span data-stu-id="9847f-103">Pricing dimensions overview</span></span>

<span data-ttu-id="9847f-104">_**适用于：** 基于资源/非库存场景的 Project Operations，精简部署 - 估价开票交易_</span><span class="sxs-lookup"><span data-stu-id="9847f-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="9847f-105">人力资源中用于设置定价和成本的维度分为两种类别：</span><span class="sxs-lookup"><span data-stu-id="9847f-105">The dimensions that are used in human resources to set up pricing and costs fall into two categories:</span></span>

- <span data-ttu-id="9847f-106">人员</span><span class="sxs-lookup"><span data-stu-id="9847f-106">People</span></span>
- <span data-ttu-id="9847f-107">计划的工作</span><span class="sxs-lookup"><span data-stu-id="9847f-107">Planned work</span></span>

<span data-ttu-id="9847f-108">因此，定价维度值有两种：</span><span class="sxs-lookup"><span data-stu-id="9847f-108">Because of this, there are two types of pricing dimension values available:</span></span>

- <span data-ttu-id="9847f-109">**选项集**：这种维度是一组值的固定枚举。</span><span class="sxs-lookup"><span data-stu-id="9847f-109">**Option sets**: Dimensions that are fixed enumerations for a set of values.</span></span>
- <span data-ttu-id="9847f-110">**基于实体的值**：这种维度可以是一组可变值。</span><span class="sxs-lookup"><span data-stu-id="9847f-110">**Entity-based values**: Dimensions that can be a varied set of values.</span></span>

## <a name="pricing-dimensions"></a><span data-ttu-id="9847f-111">定价维度</span><span class="sxs-lookup"><span data-stu-id="9847f-111">Pricing dimensions</span></span>

<span data-ttu-id="9847f-112">Dynamics 365 Project Operations 随附了一组默认定价维度。</span><span class="sxs-lookup"><span data-stu-id="9847f-112">Dynamics 365 Project Operations ships with a default set of pricing dimensions.</span></span> <span data-ttu-id="9847f-113">可通过转到 **Project Operations** > **参数** 查看这些定价维度。</span><span class="sxs-lookup"><span data-stu-id="9847f-113">You can view these pricing dimensions by going to **Project Operations** > **Parameters**.</span></span> <span data-ttu-id="9847f-114">在参数记录中 **基于金额的定价维度** 选项卡上，验证角色 **msdyn_resourcecategory** 和资源部门 **msdyn_organizationalunit** 的字段 **适用于销售** 和 **适用于成本** 是否设置为 **是**。</span><span class="sxs-lookup"><span data-stu-id="9847f-114">In the parameter record, on the **Amount-based pricing dimensions** tab, verify that the role, **msdyn_resourcecategory** and resourcing organizational unit, **msdyn_organizationalunit** have the fields **Applicable to sales** and **Applicable to cost** set to **Yes**.</span></span> <span data-ttu-id="9847f-115">启用这些字段后，您可以为每个角色与部门的组合设置价格和成本。</span><span class="sxs-lookup"><span data-stu-id="9847f-115">With these fields enabled, you can set up the price and cost for each role and organizational unit combination.</span></span>

![“适用于销售”已突出显示的 Project Service 参数的屏幕截图](media/PS-OOB-parameters.png)

<span data-ttu-id="9847f-117">如果需要使用更多属性制订资源的价格或成本，可以创建自定义的字段、实体和维度。</span><span class="sxs-lookup"><span data-stu-id="9847f-117">If you need to price or cost for your resources using additional attributes, you can create customized fields, entities, and dimensions.</span></span> <span data-ttu-id="9847f-118">有关详细信息，请参阅以下文主题。</span><span class="sxs-lookup"><span data-stu-id="9847f-118">For more information, see the following topics.</span></span> 
  
  > [!NOTE]
  > <span data-ttu-id="9847f-119">必须按列出的顺序完成这些步骤。</span><span class="sxs-lookup"><span data-stu-id="9847f-119">The procedures must be completed in the order they are listed.</span></span>

1. [<span data-ttu-id="9847f-120">为自定义定价维度创建解决方案</span><span class="sxs-lookup"><span data-stu-id="9847f-120">Create a solution for custom pricing dimensions</span></span>](../sales/create-solution-custompd.md)
2. [<span data-ttu-id="9847f-121">创建自定义字段和实体</span><span class="sxs-lookup"><span data-stu-id="9847f-121">Create custom fields and entities</span></span>](create-custom-fields-entities-pricing-dimensions.md)
3. [<span data-ttu-id="9847f-122">为价格设置和交易实体添加自定义字段</span><span class="sxs-lookup"><span data-stu-id="9847f-122">Add custom fields to price setup and transactional entities</span></span>](add-custom-fields-price-setup-transactional-entities.md)
4. [<span data-ttu-id="9847f-123">将自定义字段设置为定价维度</span><span class="sxs-lookup"><span data-stu-id="9847f-123">Set up custom fields as pricing dimensions</span></span>](set-up-custom-fields-pricing-dimensions.md)
5. [<span data-ttu-id="9847f-124">更新插件属性以包括新定价维度</span><span class="sxs-lookup"><span data-stu-id="9847f-124">Update plug-in attributes to include new pricing dimensions</span></span>](update-plugin-attributes-pd.md)


## <a name="pricing-human-resource-time"></a><span data-ttu-id="9847f-125">为人力资源时间定价</span><span class="sxs-lookup"><span data-stu-id="9847f-125">Pricing human resource time</span></span>
<span data-ttu-id="9847f-126">组织如何为人力资源时间定价通常是直接影响组织利润率的重要战略注意事项。</span><span class="sxs-lookup"><span data-stu-id="9847f-126">How an organization prices human resource time is often an important strategic consideration that directly affects the organization's profitability.</span></span> <span data-ttu-id="9847f-127">当组织准备好确定希望如何设置人力资源时间的记帐费率和成本费率时，请与财务团队和业务主管合作。</span><span class="sxs-lookup"><span data-stu-id="9847f-127">Work with the finance teams and practice heads when your organization is ready to identify how it wants to set up bill and cost rates for human resource time.</span></span>

<span data-ttu-id="9847f-128">有关定价的其他注意事项包括是否重复利用尚不是充当组织的定价维度，但是适合定价维度的字段或实体。</span><span class="sxs-lookup"><span data-stu-id="9847f-128">Other considerations for pricing include whether to re-use fields or entities that are not currently pricing dimensions but apply as a pricing dimension for your organization.</span></span> <span data-ttu-id="9847f-129">**交易类别** (**msdyn_transactioncategory**) 和 **可预订资源** (**bookableresource**) 之类字段就是候选维度。</span><span class="sxs-lookup"><span data-stu-id="9847f-129">Fields like **Transaction Category** (**msdyn_transactioncategory**) and **Bookable Resource** (**bookableresource**) are examples of candidate dimensions.</span></span> 

<span data-ttu-id="9847f-130">应注意定价维度应该是表还是选项集。</span><span class="sxs-lookup"><span data-stu-id="9847f-130">Consider whether your pricing dimension should be a table or an option set.</span></span> <span data-ttu-id="9847f-131">如果您预测维度值将更改为超过 10 或 12，并且您需要这些值的更多属性，可以创建非选项集实体。</span><span class="sxs-lookup"><span data-stu-id="9847f-131">If you foresee changes to the values of a dimension which will exceed 10 or 12 and you need additional attributes on these values, you could create an entity rather than an option set.</span></span> <span data-ttu-id="9847f-132">若要维护选项集（如添加或删除值），需要管理员或开发人员，而大多数用户可以向表添加新行。</span><span class="sxs-lookup"><span data-stu-id="9847f-132">Maintaining an option set, such as adding or removing values, requires an admin or developer whereas adding new rows to a table can be done by most users.</span></span>

<span data-ttu-id="9847f-133">以下示例显示基于资源所属角色和资源部门设置的记帐费率。</span><span class="sxs-lookup"><span data-stu-id="9847f-133">The following example shows bill rates that are set up based on the role and the resourcing org unit to which the resource belongs.</span></span> <span data-ttu-id="9847f-134">成本费率通常基于员工的工资级别和员工所属部门。</span><span class="sxs-lookup"><span data-stu-id="9847f-134">Cost rates are typically based on the salary band of the employee and the org unit that they belong to.</span></span> <span data-ttu-id="9847f-135">在此示例中，记帐费率和成本费率表如下所示。</span><span class="sxs-lookup"><span data-stu-id="9847f-135">In this example, the bill rate and cost rate tables will look like the following.</span></span>

<span data-ttu-id="9847f-136">**示例记帐费率**</span><span class="sxs-lookup"><span data-stu-id="9847f-136">**Sample bill rates**</span></span>

| <span data-ttu-id="9847f-137">角色</span><span class="sxs-lookup"><span data-stu-id="9847f-137">Role</span></span>        | <span data-ttu-id="9847f-138">部门</span><span class="sxs-lookup"><span data-stu-id="9847f-138">Org Unit</span></span>    |<span data-ttu-id="9847f-139">计价单位</span><span class="sxs-lookup"><span data-stu-id="9847f-139">Unit</span></span>      |<span data-ttu-id="9847f-140">单价</span><span class="sxs-lookup"><span data-stu-id="9847f-140">Price</span></span>      |<span data-ttu-id="9847f-141">货币</span><span class="sxs-lookup"><span data-stu-id="9847f-141">Currency</span></span>  |
| ------------|-------------|----------|----------:|----------|
| <span data-ttu-id="9847f-142">开发人员</span><span class="sxs-lookup"><span data-stu-id="9847f-142">Developer</span></span>   | <span data-ttu-id="9847f-143">Contoso US</span><span class="sxs-lookup"><span data-stu-id="9847f-143">Contoso US</span></span>  |<span data-ttu-id="9847f-144">小时</span><span class="sxs-lookup"><span data-stu-id="9847f-144">Hour</span></span> | <span data-ttu-id="9847f-145">200</span><span class="sxs-lookup"><span data-stu-id="9847f-145">200</span></span>|<span data-ttu-id="9847f-146">USD</span><span class="sxs-lookup"><span data-stu-id="9847f-146">USD</span></span>     |
| <span data-ttu-id="9847f-147">开发人员</span><span class="sxs-lookup"><span data-stu-id="9847f-147">Developer</span></span>   | <span data-ttu-id="9847f-148">Contoso 印度</span><span class="sxs-lookup"><span data-stu-id="9847f-148">Contoso India</span></span> |<span data-ttu-id="9847f-149">小时</span><span class="sxs-lookup"><span data-stu-id="9847f-149">Hour</span></span>|   <span data-ttu-id="9847f-150">112</span><span class="sxs-lookup"><span data-stu-id="9847f-150">112</span></span>|<span data-ttu-id="9847f-151">USD</span><span class="sxs-lookup"><span data-stu-id="9847f-151">USD</span></span>     |


<span data-ttu-id="9847f-152">**示例成本费率**</span><span class="sxs-lookup"><span data-stu-id="9847f-152">**Sample cost rates**</span></span>

| <span data-ttu-id="9847f-153">工资级别</span><span class="sxs-lookup"><span data-stu-id="9847f-153">Salary Band</span></span>     | <span data-ttu-id="9847f-154">部门</span><span class="sxs-lookup"><span data-stu-id="9847f-154">Org Unit</span></span>    |<span data-ttu-id="9847f-155">计价单位</span><span class="sxs-lookup"><span data-stu-id="9847f-155">Unit</span></span>      |<span data-ttu-id="9847f-156">单价</span><span class="sxs-lookup"><span data-stu-id="9847f-156">Price</span></span>      |<span data-ttu-id="9847f-157">货币</span><span class="sxs-lookup"><span data-stu-id="9847f-157">Currency</span></span>  |
| ----------------|-------------|----------|----------:|----------|
| <span data-ttu-id="9847f-158">My company_Band1</span><span class="sxs-lookup"><span data-stu-id="9847f-158">My company_Band1</span></span> | <span data-ttu-id="9847f-159">Contoso US</span><span class="sxs-lookup"><span data-stu-id="9847f-159">Contoso US</span></span>  |<span data-ttu-id="9847f-160">小时</span><span class="sxs-lookup"><span data-stu-id="9847f-160">Hour</span></span> | <span data-ttu-id="9847f-161">145</span><span class="sxs-lookup"><span data-stu-id="9847f-161">145</span></span>|<span data-ttu-id="9847f-162">USD</span><span class="sxs-lookup"><span data-stu-id="9847f-162">USD</span></span>     |
| <span data-ttu-id="9847f-163">My company_Band2</span><span class="sxs-lookup"><span data-stu-id="9847f-163">My company_Band2</span></span> | <span data-ttu-id="9847f-164">Contoso 印度</span><span class="sxs-lookup"><span data-stu-id="9847f-164">Contoso India</span></span> |<span data-ttu-id="9847f-165">小时</span><span class="sxs-lookup"><span data-stu-id="9847f-165">Hour</span></span>|   <span data-ttu-id="9847f-166">67</span><span class="sxs-lookup"><span data-stu-id="9847f-166">67</span></span>|<span data-ttu-id="9847f-167">USD</span><span class="sxs-lookup"><span data-stu-id="9847f-167">USD</span></span>     |


[!INCLUDE[footer-include](../includes/footer-banner.md)]