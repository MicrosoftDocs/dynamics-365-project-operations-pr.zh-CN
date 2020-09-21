---
title: 定价和定成本维度主页
description: 此主题概述定价维度。
author: rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 11/19/2018
ms.topic: article
ms.prod: Project Service
ms.service: business-applications
ms.assetid: 425d7bb8-9015-4f67-b9c9-cf3602e9afe8
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
ms.openlocfilehash: 2379d0d2e038f28a1a8df87a851e9bf7db7fe33f
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/24/2020
ms.locfileid: "3749686"
---
# <a name="pricing-and-costing-dimensions-home-page"></a><span data-ttu-id="347f6-103">定价和定成本维度主页</span><span class="sxs-lookup"><span data-stu-id="347f6-103">Pricing and costing dimensions home page</span></span>

<span data-ttu-id="347f6-104">人力资源中用于设置定价和成本的维度分为两种类别：</span><span class="sxs-lookup"><span data-stu-id="347f6-104">The dimensions that are used in human resources to set up pricing and costs fall into two categories:</span></span>

- <span data-ttu-id="347f6-105">人员</span><span class="sxs-lookup"><span data-stu-id="347f6-105">People</span></span>
- <span data-ttu-id="347f6-106">计划的工作</span><span class="sxs-lookup"><span data-stu-id="347f6-106">Planned work</span></span>

<span data-ttu-id="347f6-107">因此， Project Service Automation (PSA) 中的定价维度值有两种：</span><span class="sxs-lookup"><span data-stu-id="347f6-107">Because of this, there are two types of pricing dimension values available in Project Service Automation (PSA):</span></span> 

- <span data-ttu-id="347f6-108">**选项集** - 这种维度是一组值的固定枚举。</span><span class="sxs-lookup"><span data-stu-id="347f6-108">**Option sets** - Dimensions that are fixed enumerations for a set of values.</span></span>
- <span data-ttu-id="347f6-109">**基于实体的值** - 这种维度可以是一组可变值。</span><span class="sxs-lookup"><span data-stu-id="347f6-109">**Entity-based values** - Dimensions that can be a varied set of values.</span></span>

## <a name="pricing-dimensions"></a><span data-ttu-id="347f6-110">定价维度</span><span class="sxs-lookup"><span data-stu-id="347f6-110">Pricing dimensions</span></span>

<span data-ttu-id="347f6-111">PSA 随附了一组默认定价维度。</span><span class="sxs-lookup"><span data-stu-id="347f6-111">PSA ships with a default set of pricing dimensions.</span></span> <span data-ttu-id="347f6-112">可通过转到 **Project Service** > **参数**查看。</span><span class="sxs-lookup"><span data-stu-id="347f6-112">You can view these by going to **Project Service** > **Parameters**.</span></span> <span data-ttu-id="347f6-113">在参数记录中**基于金额的定价维度**选项卡上，验证角色 **msdyn_resourcecategory** 和资源部门 **msdyn_organizationalunit** 的字段**适用于销售**和**适用于成本**是否设置为**是**。</span><span class="sxs-lookup"><span data-stu-id="347f6-113">In the parameter record, on the **Amount-based pricing dimensions** tab, verify that the role, **msdyn_resourcecategory** and resourcing organizational unit, **msdyn_organizationalunit** have the fields **Applicable to sales** and **Applicable to cost** set to **Yes**.</span></span> <span data-ttu-id="347f6-114">这样就可以为每个角色与部门的组合设置价格和成本。</span><span class="sxs-lookup"><span data-stu-id="347f6-114">This will allow you to set up the price and cost for each role and organizational unit combination.</span></span>

![“适用于销售”已突出显示的 Project Service 参数的屏幕截图](media/PS-OOB-parameters.png)

> [!IMPORTANT]
> <span data-ttu-id="347f6-116">如果在 PSA 版本 3 之前已将角色和部门的自带字段用作定价维度，则不存在任何显而易见的更改。</span><span class="sxs-lookup"><span data-stu-id="347f6-116">If you have been the using out-of-the box fields of role and organizational unit as pricing dimensions prior to version 3 of PSA, there will not be any observable change.</span></span> <span data-ttu-id="347f6-117">可以继续正常使用 Project Service。</span><span class="sxs-lookup"><span data-stu-id="347f6-117">You can continue to use Project Service as usual.</span></span> 

<span data-ttu-id="347f6-118">如果需要使用更多属性制订资源的价格或成本，可以创建自定义的字段、实体和维度。</span><span class="sxs-lookup"><span data-stu-id="347f6-118">If you need to price or cost for your resources using additional attributes, you can create customized fields, entities, and dimensions.</span></span> <span data-ttu-id="347f6-119">有关详细信息，请参阅以下主题，但是请注意，必须按照下列顺序完成过程：</span><span class="sxs-lookup"><span data-stu-id="347f6-119">For more information, see the following topics, however note that you must complete the procedures in the order listed below:</span></span>

- [<span data-ttu-id="347f6-120">创建自定义字段和实体</span><span class="sxs-lookup"><span data-stu-id="347f6-120">Create custom fields and entities</span></span>](create-custom-fields-entities.md)
- [<span data-ttu-id="347f6-121">向价格设置和交易实体添加自定义字段</span><span class="sxs-lookup"><span data-stu-id="347f6-121">Add custom fields to price setup and transactional entities</span></span>](field-references.md)
- [<span data-ttu-id="347f6-122">将自定义字段设置为定价维度</span><span class="sxs-lookup"><span data-stu-id="347f6-122">Set up custom fields as pricing dimensions</span></span>](set-up-pricing-dimensions.md)
- [<span data-ttu-id="347f6-123">更新插件属性以包括新定价维度</span><span class="sxs-lookup"><span data-stu-id="347f6-123">Update plug-in attributes to include new pricing dimensions</span></span>](update-plug-in-attributes.md)

## <a name="pricing-human-resource-time"></a><span data-ttu-id="347f6-124">为人力资源时间定价</span><span class="sxs-lookup"><span data-stu-id="347f6-124">Pricing human resource time</span></span>
<span data-ttu-id="347f6-125">组织如何为人力资源时间定价通常是直接影响组织利润率的重要战略注意事项。</span><span class="sxs-lookup"><span data-stu-id="347f6-125">How an organization prices human resource time is often an important strategic consideration that directly affects the organization's profitability.</span></span> <span data-ttu-id="347f6-126">当组织准备好确定希望如何设置人力资源时间的记帐费率和成本费率时，请与财务团队和业务主管合作。</span><span class="sxs-lookup"><span data-stu-id="347f6-126">Work with the finance teams and practice heads when your organization is ready to identify how it wants to set up bill and cost rates for human resource time.</span></span>

<span data-ttu-id="347f6-127">有关定价的其他注意事项包括是否重复利用尚不是充当组织的定价维度，但是适合定价维度的字段或实体。</span><span class="sxs-lookup"><span data-stu-id="347f6-127">Other considerations for pricing include whether to re-use fields or entities that are not currently pricing dimensions but apply as a pricing dimension for your organization.</span></span> <span data-ttu-id="347f6-128">**交易类别** (**msdyn_transactioncategory**) 和**可预订资源** (**bookableresource**) 之类字段就是候选维度。</span><span class="sxs-lookup"><span data-stu-id="347f6-128">Fields like **Transaction Category** (**msdyn_transactioncategory**) and **Bookable Resource** (**bookableresource**) are examples of candidate dimensions.</span></span> 

<span data-ttu-id="347f6-129">还应注意定价维度应该是表还是选项集。</span><span class="sxs-lookup"><span data-stu-id="347f6-129">You should also consider whether your pricing dimension should be a table or an option set.</span></span> <span data-ttu-id="347f6-130">如果您预测维度值将更改为超过 10 或 12，并且您需要这些值的更多属性，可以创建非选项集实体。</span><span class="sxs-lookup"><span data-stu-id="347f6-130">If you foresee changes to the values of a dimension which will exceed 10 or 12 and you need additional attributes on these values, you could create an entity rather than an option set.</span></span> <span data-ttu-id="347f6-131">若要维护选项集（如添加或删除值），需要管理员或开发人员，而大多数用户可以向表添加新行。</span><span class="sxs-lookup"><span data-stu-id="347f6-131">Maintaining an option set, such as adding or removing values, requires an admin or developer whereas adding new rows to a table can be done by most users.</span></span>

<span data-ttu-id="347f6-132">以下示例显示基于资源所属角色和资源部门设置的记帐费率。</span><span class="sxs-lookup"><span data-stu-id="347f6-132">The following example shows bill rates that are set up based on the role and the resourcing org unit to which the resource belongs.</span></span> <span data-ttu-id="347f6-133">成本费率通常基于员工的工资级别和员工所属部门。</span><span class="sxs-lookup"><span data-stu-id="347f6-133">Cost rates are typically based on the salary band of the employee and the org unit that they belong to.</span></span> <span data-ttu-id="347f6-134">在此示例中，记帐费率和成本费率表如下所示。</span><span class="sxs-lookup"><span data-stu-id="347f6-134">In this example, the bill rate and cost rate tables will look like the following.</span></span>

<span data-ttu-id="347f6-135">**示例记帐费率**</span><span class="sxs-lookup"><span data-stu-id="347f6-135">**Sample bill rates**</span></span>

| <span data-ttu-id="347f6-136">角色</span><span class="sxs-lookup"><span data-stu-id="347f6-136">Role</span></span>        | <span data-ttu-id="347f6-137">部门</span><span class="sxs-lookup"><span data-stu-id="347f6-137">Org Unit</span></span>    |<span data-ttu-id="347f6-138">单位</span><span class="sxs-lookup"><span data-stu-id="347f6-138">Unit</span></span>      |<span data-ttu-id="347f6-139">价格</span><span class="sxs-lookup"><span data-stu-id="347f6-139">Price</span></span>      |<span data-ttu-id="347f6-140">货币</span><span class="sxs-lookup"><span data-stu-id="347f6-140">Currency</span></span>  |
| ------------|-------------|----------|----------:|----------|
| <span data-ttu-id="347f6-141">开发人员</span><span class="sxs-lookup"><span data-stu-id="347f6-141">Developer</span></span>   | <span data-ttu-id="347f6-142">Contoso US</span><span class="sxs-lookup"><span data-stu-id="347f6-142">Contoso US</span></span>  |<span data-ttu-id="347f6-143">Hour</span><span class="sxs-lookup"><span data-stu-id="347f6-143">Hour</span></span> | <span data-ttu-id="347f6-144">200</span><span class="sxs-lookup"><span data-stu-id="347f6-144">200</span></span>|<span data-ttu-id="347f6-145">USD</span><span class="sxs-lookup"><span data-stu-id="347f6-145">USD</span></span>     |
| <span data-ttu-id="347f6-146">开发人员</span><span class="sxs-lookup"><span data-stu-id="347f6-146">Developer</span></span>   | <span data-ttu-id="347f6-147">Contoso 印度</span><span class="sxs-lookup"><span data-stu-id="347f6-147">Contoso India</span></span> |<span data-ttu-id="347f6-148">Hour</span><span class="sxs-lookup"><span data-stu-id="347f6-148">Hour</span></span>|   <span data-ttu-id="347f6-149">112</span><span class="sxs-lookup"><span data-stu-id="347f6-149">112</span></span>|<span data-ttu-id="347f6-150">USD</span><span class="sxs-lookup"><span data-stu-id="347f6-150">USD</span></span>     |


<span data-ttu-id="347f6-151">**示例成本费率**</span><span class="sxs-lookup"><span data-stu-id="347f6-151">**Sample cost rates**</span></span>

| <span data-ttu-id="347f6-152">工资级别</span><span class="sxs-lookup"><span data-stu-id="347f6-152">Salary Band</span></span>     | <span data-ttu-id="347f6-153">部门</span><span class="sxs-lookup"><span data-stu-id="347f6-153">Org Unit</span></span>    |<span data-ttu-id="347f6-154">单位</span><span class="sxs-lookup"><span data-stu-id="347f6-154">Unit</span></span>      |<span data-ttu-id="347f6-155">价格</span><span class="sxs-lookup"><span data-stu-id="347f6-155">Price</span></span>      |<span data-ttu-id="347f6-156">货币</span><span class="sxs-lookup"><span data-stu-id="347f6-156">Currency</span></span>  |
| ----------------|-------------|----------|----------:|----------|
| <span data-ttu-id="347f6-157">My company_Band1</span><span class="sxs-lookup"><span data-stu-id="347f6-157">My company_Band1</span></span> | <span data-ttu-id="347f6-158">Contoso US</span><span class="sxs-lookup"><span data-stu-id="347f6-158">Contoso US</span></span>  |<span data-ttu-id="347f6-159">Hour</span><span class="sxs-lookup"><span data-stu-id="347f6-159">Hour</span></span> | <span data-ttu-id="347f6-160">145</span><span class="sxs-lookup"><span data-stu-id="347f6-160">145</span></span>|<span data-ttu-id="347f6-161">USD</span><span class="sxs-lookup"><span data-stu-id="347f6-161">USD</span></span>     |
| <span data-ttu-id="347f6-162">My company_Band2</span><span class="sxs-lookup"><span data-stu-id="347f6-162">My company_Band2</span></span> | <span data-ttu-id="347f6-163">Contoso 印度</span><span class="sxs-lookup"><span data-stu-id="347f6-163">Contoso India</span></span> |<span data-ttu-id="347f6-164">Hour</span><span class="sxs-lookup"><span data-stu-id="347f6-164">Hour</span></span>|   <span data-ttu-id="347f6-165">67</span><span class="sxs-lookup"><span data-stu-id="347f6-165">67</span></span>|<span data-ttu-id="347f6-166">USD</span><span class="sxs-lookup"><span data-stu-id="347f6-166">USD</span></span>     |
