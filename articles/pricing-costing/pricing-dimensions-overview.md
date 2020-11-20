---
title: 定价维度概述
description: 本主题提供有关 Dynamics 365 Project Operations 中的定价维度的信息。
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
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
ms.openlocfilehash: ec2e350e0e4c28ea1c9540d70c83fdf0a75dc408
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/28/2020
ms.locfileid: "4128452"
---
# <a name="pricing-dimensions-overview"></a><span data-ttu-id="840ef-103">定价维度概述</span><span class="sxs-lookup"><span data-stu-id="840ef-103">Pricing dimensions overview</span></span>

<span data-ttu-id="840ef-104">_**适用于：** 基于资源/非库存场景的 Project Operations，精简部署 - 估价开票交易_</span><span class="sxs-lookup"><span data-stu-id="840ef-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="840ef-105">人力资源中用于设置定价和成本的维度分为两种类别：</span><span class="sxs-lookup"><span data-stu-id="840ef-105">The dimensions that are used in human resources to set up pricing and costs fall into two categories:</span></span>

- <span data-ttu-id="840ef-106">人员</span><span class="sxs-lookup"><span data-stu-id="840ef-106">People</span></span>
- <span data-ttu-id="840ef-107">计划的工作</span><span class="sxs-lookup"><span data-stu-id="840ef-107">Planned work</span></span>

<span data-ttu-id="840ef-108">因此，定价维度值有两种：</span><span class="sxs-lookup"><span data-stu-id="840ef-108">Because of this, there are two types of pricing dimension values available:</span></span>

- <span data-ttu-id="840ef-109">**选项集**：这种维度是一组值的固定枚举。</span><span class="sxs-lookup"><span data-stu-id="840ef-109">**Option sets**: Dimensions that are fixed enumerations for a set of values.</span></span>
- <span data-ttu-id="840ef-110">**基于实体的值**：这种维度可以是一组可变值。</span><span class="sxs-lookup"><span data-stu-id="840ef-110">**Entity-based values**: Dimensions that can be a varied set of values.</span></span>

## <a name="pricing-dimensions"></a><span data-ttu-id="840ef-111">定价维度</span><span class="sxs-lookup"><span data-stu-id="840ef-111">Pricing dimensions</span></span>

<span data-ttu-id="840ef-112">Dynamics 365 Project Operations 附带一组默认的定价维度。</span><span class="sxs-lookup"><span data-stu-id="840ef-112">Dynamics 365 Project Operations ships with a default set of pricing dimensions.</span></span> <span data-ttu-id="840ef-113">可通过转到 **Project Operations** > **参数** 查看这些定价维度。</span><span class="sxs-lookup"><span data-stu-id="840ef-113">You can view these pricing dimensions by going to **Project Operations** > **Parameters**.</span></span> <span data-ttu-id="840ef-114">在参数记录中 **基于金额的定价维度** 选项卡上，验证角色 **msdyn_resourcecategory** 和资源部门 **msdyn_organizationalunit** 的字段 **适用于销售** 和 **适用于成本** 是否设置为 **是**。</span><span class="sxs-lookup"><span data-stu-id="840ef-114">In the parameter record, on the **Amount-based pricing dimensions** tab, verify that the role, **msdyn_resourcecategory** and resourcing organizational unit, **msdyn_organizationalunit** have the fields **Applicable to sales** and **Applicable to cost** set to **Yes**.</span></span> <span data-ttu-id="840ef-115">启用这些字段后，您可以为每个角色与部门的组合设置价格和成本。</span><span class="sxs-lookup"><span data-stu-id="840ef-115">With these fields enabled, you can set up the price and cost for each role and organizational unit combination.</span></span>

<span data-ttu-id="840ef-116">如果需要使用更多属性制订资源的价格或成本，可以创建自定义的字段、实体和维度。</span><span class="sxs-lookup"><span data-stu-id="840ef-116">If you need to price or cost for your resources using additional attributes, you can create customized fields, entities, and dimensions.</span></span>

## <a name="pricing-human-resource-time"></a><span data-ttu-id="840ef-117">为人力资源时间定价</span><span class="sxs-lookup"><span data-stu-id="840ef-117">Pricing human resource time</span></span>
<span data-ttu-id="840ef-118">组织如何为人力资源时间定价通常是直接影响组织利润率的重要战略注意事项。</span><span class="sxs-lookup"><span data-stu-id="840ef-118">How an organization prices human resource time is often an important strategic consideration that directly affects the organization's profitability.</span></span> <span data-ttu-id="840ef-119">当组织准备好确定希望如何设置人力资源时间的记帐费率和成本费率时，请与财务团队和业务主管合作。</span><span class="sxs-lookup"><span data-stu-id="840ef-119">Work with the finance teams and practice heads when your organization is ready to identify how it wants to set up bill and cost rates for human resource time.</span></span>

<span data-ttu-id="840ef-120">有关定价的其他注意事项包括是否重复利用尚不是充当组织的定价维度，但是适合定价维度的字段或实体。</span><span class="sxs-lookup"><span data-stu-id="840ef-120">Other considerations for pricing include whether to re-use fields or entities that are not currently pricing dimensions but apply as a pricing dimension for your organization.</span></span> <span data-ttu-id="840ef-121">**交易类别** (**msdyn_transactioncategory**) 和 **可预订资源** (**bookableresource**) 之类字段就是候选维度。</span><span class="sxs-lookup"><span data-stu-id="840ef-121">Fields like **Transaction Category** (**msdyn_transactioncategory**) and **Bookable Resource** (**bookableresource**) are examples of candidate dimensions.</span></span> 

<span data-ttu-id="840ef-122">应注意定价维度应该是表还是选项集。</span><span class="sxs-lookup"><span data-stu-id="840ef-122">Consider whether your pricing dimension should be a table or an option set.</span></span> <span data-ttu-id="840ef-123">如果您预测维度值将更改为超过 10 或 12，并且您需要这些值的更多属性，可以创建非选项集实体。</span><span class="sxs-lookup"><span data-stu-id="840ef-123">If you foresee changes to the values of a dimension which will exceed 10 or 12 and you need additional attributes on these values, you could create an entity rather than an option set.</span></span> <span data-ttu-id="840ef-124">若要维护选项集（如添加或删除值），需要管理员或开发人员，而大多数用户可以向表添加新行。</span><span class="sxs-lookup"><span data-stu-id="840ef-124">Maintaining an option set, such as adding or removing values, requires an admin or developer whereas adding new rows to a table can be done by most users.</span></span>

<span data-ttu-id="840ef-125">以下示例显示基于资源所属角色和资源部门设置的记帐费率。</span><span class="sxs-lookup"><span data-stu-id="840ef-125">The following example shows bill rates that are set up based on the role and the resourcing org unit to which the resource belongs.</span></span> <span data-ttu-id="840ef-126">成本费率通常基于员工的工资级别和员工所属部门。</span><span class="sxs-lookup"><span data-stu-id="840ef-126">Cost rates are typically based on the salary band of the employee and the org unit that they belong to.</span></span> <span data-ttu-id="840ef-127">在此示例中，记帐费率和成本费率表如下所示。</span><span class="sxs-lookup"><span data-stu-id="840ef-127">In this example, the bill rate and cost rate tables will look like the following.</span></span>

<span data-ttu-id="840ef-128">**示例记帐费率**</span><span class="sxs-lookup"><span data-stu-id="840ef-128">**Sample bill rates**</span></span>

| <span data-ttu-id="840ef-129">角色</span><span class="sxs-lookup"><span data-stu-id="840ef-129">Role</span></span>        | <span data-ttu-id="840ef-130">部门</span><span class="sxs-lookup"><span data-stu-id="840ef-130">Org Unit</span></span>    |<span data-ttu-id="840ef-131">单位</span><span class="sxs-lookup"><span data-stu-id="840ef-131">Unit</span></span>      |<span data-ttu-id="840ef-132">价格</span><span class="sxs-lookup"><span data-stu-id="840ef-132">Price</span></span>      |<span data-ttu-id="840ef-133">货币</span><span class="sxs-lookup"><span data-stu-id="840ef-133">Currency</span></span>  |
| ------------|-------------|----------|----------:|----------|
| <span data-ttu-id="840ef-134">开发人员</span><span class="sxs-lookup"><span data-stu-id="840ef-134">Developer</span></span>   | <span data-ttu-id="840ef-135">Contoso US</span><span class="sxs-lookup"><span data-stu-id="840ef-135">Contoso US</span></span>  |<span data-ttu-id="840ef-136">Hour</span><span class="sxs-lookup"><span data-stu-id="840ef-136">Hour</span></span> | <span data-ttu-id="840ef-137">200</span><span class="sxs-lookup"><span data-stu-id="840ef-137">200</span></span>|<span data-ttu-id="840ef-138">USD</span><span class="sxs-lookup"><span data-stu-id="840ef-138">USD</span></span>     |
| <span data-ttu-id="840ef-139">开发人员</span><span class="sxs-lookup"><span data-stu-id="840ef-139">Developer</span></span>   | <span data-ttu-id="840ef-140">Contoso 印度</span><span class="sxs-lookup"><span data-stu-id="840ef-140">Contoso India</span></span> |<span data-ttu-id="840ef-141">Hour</span><span class="sxs-lookup"><span data-stu-id="840ef-141">Hour</span></span>|   <span data-ttu-id="840ef-142">112</span><span class="sxs-lookup"><span data-stu-id="840ef-142">112</span></span>|<span data-ttu-id="840ef-143">USD</span><span class="sxs-lookup"><span data-stu-id="840ef-143">USD</span></span>     |


<span data-ttu-id="840ef-144">**示例成本费率**</span><span class="sxs-lookup"><span data-stu-id="840ef-144">**Sample cost rates**</span></span>

| <span data-ttu-id="840ef-145">工资级别</span><span class="sxs-lookup"><span data-stu-id="840ef-145">Salary Band</span></span>     | <span data-ttu-id="840ef-146">部门</span><span class="sxs-lookup"><span data-stu-id="840ef-146">Org Unit</span></span>    |<span data-ttu-id="840ef-147">单位</span><span class="sxs-lookup"><span data-stu-id="840ef-147">Unit</span></span>      |<span data-ttu-id="840ef-148">价格</span><span class="sxs-lookup"><span data-stu-id="840ef-148">Price</span></span>      |<span data-ttu-id="840ef-149">货币</span><span class="sxs-lookup"><span data-stu-id="840ef-149">Currency</span></span>  |
| ----------------|-------------|----------|----------:|----------|
| <span data-ttu-id="840ef-150">My company_Band1</span><span class="sxs-lookup"><span data-stu-id="840ef-150">My company_Band1</span></span> | <span data-ttu-id="840ef-151">Contoso US</span><span class="sxs-lookup"><span data-stu-id="840ef-151">Contoso US</span></span>  |<span data-ttu-id="840ef-152">Hour</span><span class="sxs-lookup"><span data-stu-id="840ef-152">Hour</span></span> | <span data-ttu-id="840ef-153">145</span><span class="sxs-lookup"><span data-stu-id="840ef-153">145</span></span>|<span data-ttu-id="840ef-154">USD</span><span class="sxs-lookup"><span data-stu-id="840ef-154">USD</span></span>     |
| <span data-ttu-id="840ef-155">My company_Band2</span><span class="sxs-lookup"><span data-stu-id="840ef-155">My company_Band2</span></span> | <span data-ttu-id="840ef-156">Contoso 印度</span><span class="sxs-lookup"><span data-stu-id="840ef-156">Contoso India</span></span> |<span data-ttu-id="840ef-157">Hour</span><span class="sxs-lookup"><span data-stu-id="840ef-157">Hour</span></span>|   <span data-ttu-id="840ef-158">67</span><span class="sxs-lookup"><span data-stu-id="840ef-158">67</span></span>|<span data-ttu-id="840ef-159">USD</span><span class="sxs-lookup"><span data-stu-id="840ef-159">USD</span></span>     |
