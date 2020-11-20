---
title: 创建自定义字段和实体，作为定价维度
description: 此主题提供有关如何创建自定义选项集或实体的信息。
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
ms.openlocfilehash: 616bcd5758b434b45bd06aa1a026f32efc8b7f99
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/28/2020
ms.locfileid: "4130882"
---
# <a name="create-custom-fields-and-entities-as-pricing-dimensions"></a><span data-ttu-id="c0495-103">创建自定义字段和实体，作为定价维度</span><span class="sxs-lookup"><span data-stu-id="c0495-103">Create custom fields and entities as pricing dimensions</span></span>

<span data-ttu-id="c0495-104">_**适用于：** 基于资源/非库存场景的 Project Operations，精简部署 - 估价开票交易_</span><span class="sxs-lookup"><span data-stu-id="c0495-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="c0495-105">任何时候要创建自定义选项集或实体，请完成以下步骤。</span><span class="sxs-lookup"><span data-stu-id="c0495-105">Complete the following steps any time that you want to create a custom option set or entity.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="c0495-106">建议在单独的解决方案中进行所有自定义定价维度更改。</span><span class="sxs-lookup"><span data-stu-id="c0495-106">We recommend that you make all custom pricing dimension changes in a separate solution.</span></span> <span data-ttu-id="c0495-107">这项重要的最佳实践让您可以在将来灵活地根据需要更新或删除更改，从而可以帮助您重复利用您的工作，并更轻松地将这些更改移植到其他实例中。</span><span class="sxs-lookup"><span data-stu-id="c0495-107">This important best practice provides flexibility in the future to update or remove changes as needed, will help with re-use of your work, and makes it easier to port these changes to another instance.</span></span> <span data-ttu-id="c0495-108">进行了所有必需更改之后，将此解决方案作为 **托管解决方案** 导出，然后导入到其他实例中，以便重复利用您的定价设置。</span><span class="sxs-lookup"><span data-stu-id="c0495-108">After you have made all of the required changes, export this solution as a **Managed solution** and import it into other instances to reuse your pricing setup.</span></span>


## <a name="create-a-custom-solution-for-pricing-dimensions"></a><span data-ttu-id="c0495-109">为定价维度创建自定义解决方案</span><span class="sxs-lookup"><span data-stu-id="c0495-109">Create a custom solution for pricing dimensions</span></span>
1. <span data-ttu-id="c0495-110">转到 **设置** > **解决方案**，然后选择 **新建** 创建新的解决方案。</span><span class="sxs-lookup"><span data-stu-id="c0495-110">Go to **Settings** > **Solutions**, and then select **New** to create a new solution.</span></span> 
2. <span data-ttu-id="c0495-111">将该解决方案命名为 **\<your organization name> 定价维度**，输入其余必需信息，然后选择 **保存**。</span><span class="sxs-lookup"><span data-stu-id="c0495-111">Name the solution, **\<your organization name> pricing dimensions**, enter the remaining required information, and then select **Save**.</span></span>
  
## <a name="create-custom-fields-and-option-sets-in-the-pricing-dimension-solution"></a><span data-ttu-id="c0495-112">在定价维度解决方案中创建自定义字段和选项集</span><span class="sxs-lookup"><span data-stu-id="c0495-112">Create custom fields and option sets in the pricing dimension solution</span></span>

<span data-ttu-id="c0495-113">定价维度可以是选项集或实体。</span><span class="sxs-lookup"><span data-stu-id="c0495-113">A pricing dimension can be an option set or an entity.</span></span> <span data-ttu-id="c0495-114">两种都必须在定价解决方案中创建。</span><span class="sxs-lookup"><span data-stu-id="c0495-114">Both must be created in your pricing solution.</span></span> <span data-ttu-id="c0495-115">此过程中的步骤介绍如何创建基于实体的维度和基于选项集的维度。</span><span class="sxs-lookup"><span data-stu-id="c0495-115">The steps in this procedure explain how to create entity-based dimensions and option set-based dimensions.</span></span>

### <a name="entity-based-dimensions"></a><span data-ttu-id="c0495-116">基于实体的维度</span><span class="sxs-lookup"><span data-stu-id="c0495-116">Entity-based dimensions</span></span>

1. <span data-ttu-id="c0495-117">转到 **设置** > **解决方案**，然后双击 **\<your organization name> 定价维度**。</span><span class="sxs-lookup"><span data-stu-id="c0495-117">Go to **Settings** > **Solutions**, and then double-click **\<your organization name> pricing dimensions**.</span></span>
2. <span data-ttu-id="c0495-118">在解决方案资源管理器中左侧导航窗格上，选择 **实体**。</span><span class="sxs-lookup"><span data-stu-id="c0495-118">In Solution Explorer, on the left navigation pane, select **Entities**.</span></span>
3. <span data-ttu-id="c0495-119">选择 **新建** 创建一个IE名称为 **标准标题** 的新实体。</span><span class="sxs-lookup"><span data-stu-id="c0495-119">Select **New** to create a new entity called **Standard Title**.</span></span> 
4. <span data-ttu-id="c0495-120">输入其余所需信息，然后选择 **保存**。</span><span class="sxs-lookup"><span data-stu-id="c0495-120">Enter the remaining required information, and then select **Save**.</span></span>


### <a name="option-set-based-dimensions"></a><span data-ttu-id="c0495-121">基于选项集的维度</span><span class="sxs-lookup"><span data-stu-id="c0495-121">Option set-based dimensions</span></span> 
<span data-ttu-id="c0495-122">可创建两个基于选项集的维度。</span><span class="sxs-lookup"><span data-stu-id="c0495-122">You can create two option set-based dimensions.</span></span> <span data-ttu-id="c0495-123">**资源工作位置** 用于跟踪 **当前** 位置工作和 **现场** 工作的价格，值为 **常规** 和 **加班** 的 **资源工作时间** 用于在完成工作时应用加价。</span><span class="sxs-lookup"><span data-stu-id="c0495-123">Use **Resource Work Location** to track the price of **Home** location work and **Onsite** work and use **Resource Work hours** with values **Regular** and **Overtime** to apply a markup when work is completed.</span></span>


1. <span data-ttu-id="c0495-124">转到 **设置** > **解决方案**，双击 **\<your organization name> 定价维度**。</span><span class="sxs-lookup"><span data-stu-id="c0495-124">Go to **Settings** > **Solutions**, and double-click  **\<your organization name> pricing dimensions**.</span></span> 
2. <span data-ttu-id="c0495-125">在解决方案资源管理器中左侧导航窗格上，选择 **选项集**。</span><span class="sxs-lookup"><span data-stu-id="c0495-125">In Solution Explorer, on the left navigation pane, select  **Option Sets**.</span></span> 
3. <span data-ttu-id="c0495-126">选择 **新建** 创建一个新的选项集，输入其余必需信息，然后选择 **保存**。</span><span class="sxs-lookup"><span data-stu-id="c0495-126">Select **New** to create a new option set, enter the remaining required information, and then select **Save**.</span></span>

## <a name="create-data-for-entity-based-dimensions"></a><span data-ttu-id="c0495-127">为基于实体的维度创建数据</span><span class="sxs-lookup"><span data-stu-id="c0495-127">Create data for entity-based dimensions</span></span>

<span data-ttu-id="c0495-128">可手动为基于实体的维度创建数据，也可以使用 Microsoft Excel 导入或服务调用创建。</span><span class="sxs-lookup"><span data-stu-id="c0495-128">You can create data for entity-based dimensions manually, or by using Microsoft Excel import or service calls.</span></span> <span data-ttu-id="c0495-129">使用此过程中的步骤从基于实体的维度 **标准标题** 创建两个标准标题：**系统工程师** 和 **高级系统工程师**。</span><span class="sxs-lookup"><span data-stu-id="c0495-129">Use the steps in this procedure to create two standard titles, **Systems Engineer** and **Senior Systems Engineer** from the entity-based dimension, **Standard Title**.</span></span> <span data-ttu-id="c0495-130">如果要创建的数据很少（如在以下示例中），可以使用标准窗体。</span><span class="sxs-lookup"><span data-stu-id="c0495-130">If the data that you want to create is small, as in the following example, you can use a standard form.</span></span>

1. <span data-ttu-id="c0495-131">选择 **高级查找**，选择实体 **标准标题**，然后选择 **结果**。</span><span class="sxs-lookup"><span data-stu-id="c0495-131">Select **Advanced Find**, select the entity **Standard Title**, and then select **Results**.</span></span> <span data-ttu-id="c0495-132">将显示 **标准标题** 实体中的所有行。</span><span class="sxs-lookup"><span data-stu-id="c0495-132">All of the rows in the **Standard Title** entity will be shown.</span></span>
2. <span data-ttu-id="c0495-133">选择 **新建**，在 **名称** 字段中，输入“系统工程师”，然后选择 **保存**。</span><span class="sxs-lookup"><span data-stu-id="c0495-133">Select **New**, and in the **Name** field, enter "Systems Engineer" and then select **Save**.</span></span>
3. <span data-ttu-id="c0495-134">关闭此窗体。</span><span class="sxs-lookup"><span data-stu-id="c0495-134">Close the form.</span></span> 
4. <span data-ttu-id="c0495-135">重复步骤 1 - 3 再为“高级系统工程师”创建一个标准标题。</span><span class="sxs-lookup"><span data-stu-id="c0495-135">Repeat steps 1 - 3 to create another standard title for "Senior Systems Engineer".</span></span>

## <a name="add-all-required-entities-and-related-components-to-the-pricing-dimension-solution"></a><span data-ttu-id="c0495-136">向定价维度解决方案添加所有必需实体和相关组件</span><span class="sxs-lookup"><span data-stu-id="c0495-136">Add all required entities and related components to the Pricing Dimension Solution</span></span>
<span data-ttu-id="c0495-137">您需要向定价解决方案添加以下实体。</span><span class="sxs-lookup"><span data-stu-id="c0495-137">You will need to add the following entities to your pricing solution.</span></span> <span data-ttu-id="c0495-138">请使用此过程中的步骤在定价解决方案中进行一些重要的架构更改，以便实体可以识别新的定价维度。</span><span class="sxs-lookup"><span data-stu-id="c0495-138">Use the steps in this procedure to make some important schema changes in the pricing solution so that the entities become aware of the new pricing dimensions.</span></span>

1. <span data-ttu-id="c0495-139">选择 **设置** > **解决方案**，双击 **\<your organization name> 定价维度**。</span><span class="sxs-lookup"><span data-stu-id="c0495-139">Select **Settings** > **Solutions**, and double-click **\<your organization name> pricing dimensions**.</span></span> 
2. <span data-ttu-id="c0495-140">在解决方案资源管理器中左侧导航窗格上，选择 **添加现有** > **实体**。</span><span class="sxs-lookup"><span data-stu-id="c0495-140">In Solution Explorer, on the left navigation pane, select **Add Existing** > **Entities**.</span></span>
3. <span data-ttu-id="c0495-141">在 **解决方案组件** 对话框中，选择以下实体：</span><span class="sxs-lookup"><span data-stu-id="c0495-141">In the **Solution Components** dialog box, select the following entities:</span></span>

  - <span data-ttu-id="c0495-142">实际值</span><span class="sxs-lookup"><span data-stu-id="c0495-142">Actual</span></span>
  - <span data-ttu-id="c0495-143">可预订的资源</span><span class="sxs-lookup"><span data-stu-id="c0495-143">Bookable Resource</span></span>
  - <span data-ttu-id="c0495-144">估算明细</span><span class="sxs-lookup"><span data-stu-id="c0495-144">Estimate Line</span></span>
  - <span data-ttu-id="c0495-145">发票明细详细信息</span><span class="sxs-lookup"><span data-stu-id="c0495-145">Invoice Line Detail</span></span>
  - <span data-ttu-id="c0495-146">日记帐行</span><span class="sxs-lookup"><span data-stu-id="c0495-146">Journal Line</span></span>
  - <span data-ttu-id="c0495-147">项目合同子项详细信息</span><span class="sxs-lookup"><span data-stu-id="c0495-147">Project Contract Line Detail</span></span>
  - <span data-ttu-id="c0495-148">项目团队成员</span><span class="sxs-lookup"><span data-stu-id="c0495-148">Project Team Member</span></span>
  - <span data-ttu-id="c0495-149">报价单明细详细信息</span><span class="sxs-lookup"><span data-stu-id="c0495-149">Quote Line Detail</span></span>
  - <span data-ttu-id="c0495-150">角色价格加价</span><span class="sxs-lookup"><span data-stu-id="c0495-150">Role Price Markup</span></span>
  - <span data-ttu-id="c0495-151">角色价格</span><span class="sxs-lookup"><span data-stu-id="c0495-151">Role Price</span></span> 
  - <span data-ttu-id="c0495-152">时间条目</span><span class="sxs-lookup"><span data-stu-id="c0495-152">Time Entry</span></span> 


> [!NOTE]
> <span data-ttu-id="c0495-153">务必包括所选每个实体的所有窗体和视图。</span><span class="sxs-lookup"><span data-stu-id="c0495-153">Make sure to include all forms and views for each of the entities selected.</span></span>

4. <span data-ttu-id="c0495-154">当系统提示包括上面所选实体的任何依赖实体时，选择 **否**。</span><span class="sxs-lookup"><span data-stu-id="c0495-154">When prompted to include any dependent entities for the entities selected above, select **No**.</span></span>

