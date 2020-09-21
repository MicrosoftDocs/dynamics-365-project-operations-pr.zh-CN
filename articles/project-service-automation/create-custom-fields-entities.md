---
title: 创建自定义字段和实体
description: 此主题介绍在 Power Apps 平台中如何在自己的解决方案内创建选项集和实体。
author: Rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 11/26/2018
ms.topic: article
ms.prod: Project Service
ms.service: business-applications
ms.assetid: fb160bfd-e037-4a21-a968-3ff2e6e16481
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
ms.openlocfilehash: 7ee30e3bb6b8034ef226e2e9181195685355011f
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/24/2020
ms.locfileid: "3749770"
---
# <a name="create-custom-fields-and-entities"></a><span data-ttu-id="eaa4f-103">创建自定义字段和实体</span><span class="sxs-lookup"><span data-stu-id="eaa4f-103">Create custom fields and entities</span></span> 

<span data-ttu-id="eaa4f-104">如果要在 Power Apps 平台中创建自定义选项集或实体，随时可完成以下步骤。</span><span class="sxs-lookup"><span data-stu-id="eaa4f-104">Complete the following steps any time that you want to create a custom option set or entity on the Power Apps platform.</span></span>  
<span data-ttu-id="eaa4f-105">此主题中的过程应使用 Project Service Automation (PSA) 的 Web 界面完成。</span><span class="sxs-lookup"><span data-stu-id="eaa4f-105">The procedures in this topic should be completed using the web interface of Project Service Automation (PSA).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="eaa4f-106">建议在单独的解决方案中进行所有自定义定价维度更改。</span><span class="sxs-lookup"><span data-stu-id="eaa4f-106">We recommend that you make all custom pricing dimension changes in a separate solution.</span></span> <span data-ttu-id="eaa4f-107">这项重要的最佳实践让您可以在将来灵活地根据需要更新或删除更改，从而可以帮助您重复利用您的工作，并更轻松地将这些更改移植到其他实例中。</span><span class="sxs-lookup"><span data-stu-id="eaa4f-107">This important best practice provides flexibility in the future to update or remove changes as needed, will help with re-use of your work, and makes it easier to port these changes to another instance.</span></span> <span data-ttu-id="eaa4f-108">进行了所有必需更改之后，将此解决方案作为**托管解决方案**导出，然后导入到其他实例中，以便重复利用您的定价设置。</span><span class="sxs-lookup"><span data-stu-id="eaa4f-108">After you have made all of the required changes, export this solution as a **Managed solution** and import it into other instances to reuse your pricing setup.</span></span>


## <a name="create-a-custom-solution-for-pricing-dimensions"></a><span data-ttu-id="eaa4f-109">为定价维度创建自定义解决方案</span><span class="sxs-lookup"><span data-stu-id="eaa4f-109">Create a custom solution for pricing dimensions</span></span>
1. <span data-ttu-id="eaa4f-110">在 PSA 中，单击**设置** > **解决方案**，然后单击**新建**创建新的解决方案。</span><span class="sxs-lookup"><span data-stu-id="eaa4f-110">In PSA, click **Settings** > **Solutions**, and then click **New** to create a new solution.</span></span> 
2. <span data-ttu-id="eaa4f-111">将该解决方案命名为 **\<您的组织名称> 定价维度**，输入其余必需信息，然后单击**保存**。</span><span class="sxs-lookup"><span data-stu-id="eaa4f-111">Name the solution, **\<your organization name> pricing dimensions**, enter the remaining required information, and then click **Save**.</span></span>

> ![为定价维度创建自定义解决方案](media/Creation-of-custom-pricing-dimension-solution.PNG)
  
## <a name="create-custom-fields-and-option-sets-in-the-pricing-dimension-solution"></a><span data-ttu-id="eaa4f-113">在定价维度解决方案中创建自定义字段和选项集</span><span class="sxs-lookup"><span data-stu-id="eaa4f-113">Create custom fields and option sets in the pricing dimension solution</span></span>

<span data-ttu-id="eaa4f-114">定价维度可以是选项集或实体。</span><span class="sxs-lookup"><span data-stu-id="eaa4f-114">A pricing dimension can be an option set or an entity.</span></span> <span data-ttu-id="eaa4f-115">两种都必须在定价解决方案中创建。</span><span class="sxs-lookup"><span data-stu-id="eaa4f-115">Both must be created in your pricing solution.</span></span> <span data-ttu-id="eaa4f-116">此过程中的步骤介绍如何创建基于实体的维度和基于选项集的维度。</span><span class="sxs-lookup"><span data-stu-id="eaa4f-116">The steps in this procedure explain how to create entity-based dimensions and option set-based dimensions.</span></span>

### <a name="entity-based-dimensions"></a><span data-ttu-id="eaa4f-117">基于实体的维度</span><span class="sxs-lookup"><span data-stu-id="eaa4f-117">Entity-based dimensions</span></span>

1. <span data-ttu-id="eaa4f-118">在 PSA 中，单击**设置** > **解决方案**，然后双击 **\<您的组织名称> 定价维度**。</span><span class="sxs-lookup"><span data-stu-id="eaa4f-118">In PSA, click **Settings** > **Solutions**, and then double-click **\<your organization name> pricing dimensions**.</span></span>
2. <span data-ttu-id="eaa4f-119">在解决方案资源管理器中左侧导航窗格上，选择**实体**。</span><span class="sxs-lookup"><span data-stu-id="eaa4f-119">In Solution Explorer, on the left navigation pane, select **Entities**.</span></span>
3. <span data-ttu-id="eaa4f-120">单击**新建**创建一个IE名称为**标准标题**的新实体。</span><span class="sxs-lookup"><span data-stu-id="eaa4f-120">Click **New** to create a new entity called **Standard Title**.</span></span> <span data-ttu-id="eaa4f-121">输入其余所需信息，然后单击**保存**。</span><span class="sxs-lookup"><span data-stu-id="eaa4f-121">Enter the remaining required information, and then click **Save**.</span></span>

> ![标准标题实体定义](media/Standard-Title-entity-definition.png)


### <a name="option-set-based-dimensions"></a><span data-ttu-id="eaa4f-123">基于选项集的维度</span><span class="sxs-lookup"><span data-stu-id="eaa4f-123">Option set-based dimensions</span></span> 
<span data-ttu-id="eaa4f-124">可创建两个基于选项集的维度。</span><span class="sxs-lookup"><span data-stu-id="eaa4f-124">You can create two option set-based dimensions.</span></span> <span data-ttu-id="eaa4f-125">**资源工作位置**用于跟踪**当前**位置工作和**现场**工作的价格，值为**常规**和**加班**的**资源工作时间**用于在完成工作时应用加价。</span><span class="sxs-lookup"><span data-stu-id="eaa4f-125">Use **Resource Work Location** to track the price of **Home** location work and **Onsite** work and use **Resource Work hours** with values **Regular** and **Overtime** to apply a markup when work is completed.</span></span>


1. <span data-ttu-id="eaa4f-126">在 PSA 中，单击**设置** > **解决方案**，然后双击 **\<您的组织名称> 定价维度**。</span><span class="sxs-lookup"><span data-stu-id="eaa4f-126">In PSA, click **Settings** > **Solutions**, and then double-click  **\<your organization name> pricing dimensions**.</span></span> 
2. <span data-ttu-id="eaa4f-127">在解决方案资源管理器中左侧导航窗格上，选择**选项集**。</span><span class="sxs-lookup"><span data-stu-id="eaa4f-127">In Solution Explorer, on the left navigation pane, select  **Option Sets**.</span></span> 
3. <span data-ttu-id="eaa4f-128">单击**新建**创建一个新的选项集，输入其余必需信息，然后单击**保存**。</span><span class="sxs-lookup"><span data-stu-id="eaa4f-128">Click **New** to create a new option set, enter the remaining required information, and then click **Save**.</span></span>

> ![<span data-ttu-id="eaa4f-129">称为“资源工作位置”且基于选项集的定价维度</span><span class="sxs-lookup"><span data-stu-id="eaa4f-129">Option set based pricing dimension called Resource Work Location</span></span> ](media/Option-set-PD-called-Resource-Work-Location.png)

> ![<span data-ttu-id="eaa4f-130">称为“资源工作时间”且基于选项集的定价维度</span><span class="sxs-lookup"><span data-stu-id="eaa4f-130">Option set based pricing dimension called Resource Work Hours</span></span> ](media/Option-set-PD-called-Resource-Work-Hours.PNG)


## <a name="create-data-for-entity-based-dimensions"></a><span data-ttu-id="eaa4f-131">为基于实体的维度创建数据</span><span class="sxs-lookup"><span data-stu-id="eaa4f-131">Create data for entity-based dimensions</span></span>

<span data-ttu-id="eaa4f-132">可手动为基于实体的维度创建数据，也可以使用 Microsoft Excel 导入或服务调用创建。</span><span class="sxs-lookup"><span data-stu-id="eaa4f-132">You can create data for entity-based dimensions manually, or by using Microsoft Excel import or service calls.</span></span> <span data-ttu-id="eaa4f-133">使用此过程中的步骤从基于实体的维度**标准标题**创建两个标准标题：**系统工程师**和**高级系统工程师**。</span><span class="sxs-lookup"><span data-stu-id="eaa4f-133">Use the steps in this procedure to create two standard titles, **Systems Engineer** and **Senior Systems Engineer** from the entity-based dimension, **Standard Title**.</span></span> <span data-ttu-id="eaa4f-134">如果要创建的数据很少（如在以下示例中），可以使用标准窗体。</span><span class="sxs-lookup"><span data-stu-id="eaa4f-134">If the data that you want to create is small, as in the following example, you can use a standard form.</span></span>

1. <span data-ttu-id="eaa4f-135">在 PSA 中，单击**高级查找**。</span><span class="sxs-lookup"><span data-stu-id="eaa4f-135">In PSA, click **Advanced Find**.</span></span> <span data-ttu-id="eaa4f-136">选择实体**标准标题**，然后单击**结果**。</span><span class="sxs-lookup"><span data-stu-id="eaa4f-136">Select the entity **Standard Title** and then click **Results**.</span></span> <span data-ttu-id="eaa4f-137">将显示**标准标题**实体中的所有行。</span><span class="sxs-lookup"><span data-stu-id="eaa4f-137">All of the rows in the **Standard Title** entity will be shown.</span></span>
2. <span data-ttu-id="eaa4f-138">单击**新建**。</span><span class="sxs-lookup"><span data-stu-id="eaa4f-138">Click **New**.</span></span> <span data-ttu-id="eaa4f-139">在**名称**字段中，输入“系统工程师”，然后单击**保存**。</span><span class="sxs-lookup"><span data-stu-id="eaa4f-139">In the **Name** field, enter "Systems Engineer" and then click **Save**.</span></span>
3. <span data-ttu-id="eaa4f-140">关闭窗体。</span><span class="sxs-lookup"><span data-stu-id="eaa4f-140">Close the form.</span></span> 
4. <span data-ttu-id="eaa4f-141">重复步骤 1 - 3 再为“高级系统工程师”创建一个标准标题。</span><span class="sxs-lookup"><span data-stu-id="eaa4f-141">Repeat steps 1 - 3 to create another standard title for "Senior Systems Engineer".</span></span>

> ![<span data-ttu-id="eaa4f-142">标准标题实体的示例数据</span><span class="sxs-lookup"><span data-stu-id="eaa4f-142">Sample Data for Standard Title entity</span></span> ](media/ST-data.png)

## <a name="add-all-required-psa-entities-and-related-components-to-the-pricing-dimension-solution"></a><span data-ttu-id="eaa4f-143">向定价维度解决方案添加所有必需的 PSA 实体和相关组件</span><span class="sxs-lookup"><span data-stu-id="eaa4f-143">Add all required PSA entities and related components to the Pricing Dimension Solution</span></span>
<span data-ttu-id="eaa4f-144">您需要向定价解决方案添加以下 Project Service 实体。</span><span class="sxs-lookup"><span data-stu-id="eaa4f-144">You will need to add the following Project Service entities to your pricing solution.</span></span> <span data-ttu-id="eaa4f-145">请使用此过程中的步骤在定价解决方案中进行一些重要的架构更改，以便实体可以识别新的定价维度。</span><span class="sxs-lookup"><span data-stu-id="eaa4f-145">Use the steps in this procedure to make some important schema changes in the pricing solution so that the entities become aware of the new pricing dimensions.</span></span>

1. <span data-ttu-id="eaa4f-146">在 PSA 中，单击**设置** > **解决方案**，然后双击 **\<您的组织名称> 定价维度**。</span><span class="sxs-lookup"><span data-stu-id="eaa4f-146">In PSA, click **Settings** > **Solutions**, and then double-click **\<your organization name> pricing dimensions**.</span></span> 
2. <span data-ttu-id="eaa4f-147">在解决方案资源管理器中左侧导航窗格上，选择**添加现有** > **实体**。</span><span class="sxs-lookup"><span data-stu-id="eaa4f-147">In Solution Explorer, on the left navigation pane, select **Add Existing** > **Entities**.</span></span>
3. <span data-ttu-id="eaa4f-148">在**解决方案组件**对话框中，选择以下实体：</span><span class="sxs-lookup"><span data-stu-id="eaa4f-148">In the **Solution Components** dialog box, select the following entities:</span></span>

- <span data-ttu-id="eaa4f-149">实际值</span><span class="sxs-lookup"><span data-stu-id="eaa4f-149">Actual</span></span>
- <span data-ttu-id="eaa4f-150">可预订的资源</span><span class="sxs-lookup"><span data-stu-id="eaa4f-150">Bookable Resource</span></span>
- <span data-ttu-id="eaa4f-151">估算明细</span><span class="sxs-lookup"><span data-stu-id="eaa4f-151">Estimate Line</span></span>
- <span data-ttu-id="eaa4f-152">发票明细详细信息</span><span class="sxs-lookup"><span data-stu-id="eaa4f-152">Invoice Line Detail</span></span>
- <span data-ttu-id="eaa4f-153">日记帐行</span><span class="sxs-lookup"><span data-stu-id="eaa4f-153">Journal Line</span></span>
- <span data-ttu-id="eaa4f-154">项目合同子项详细信息</span><span class="sxs-lookup"><span data-stu-id="eaa4f-154">Project Contract Line Detail</span></span>
- <span data-ttu-id="eaa4f-155">项目团队成员</span><span class="sxs-lookup"><span data-stu-id="eaa4f-155">Project Team Member</span></span>
- <span data-ttu-id="eaa4f-156">报价单行明细</span><span class="sxs-lookup"><span data-stu-id="eaa4f-156">Quote Line Detail</span></span>
- <span data-ttu-id="eaa4f-157">角色价格加价</span><span class="sxs-lookup"><span data-stu-id="eaa4f-157">Role Price Markup</span></span>
- <span data-ttu-id="eaa4f-158">角色价格</span><span class="sxs-lookup"><span data-stu-id="eaa4f-158">Role Price</span></span> 
- <span data-ttu-id="eaa4f-159">时间条目</span><span class="sxs-lookup"><span data-stu-id="eaa4f-159">Time Entry</span></span> 

> ![向定价维度解决方案添加现有实体](media/Existing-entities-to-PD-solution.png)

> ![选择解决方案组件](media/Dimension-Components.png)

> [!NOTE]
> <span data-ttu-id="eaa4f-162">务必包括所选每个实体的所有窗体和视图。</span><span class="sxs-lookup"><span data-stu-id="eaa4f-162">Make sure to include all forms and views for each of the entities selected.</span></span>

4. <span data-ttu-id="eaa4f-163">当系统提示包括上面所选实体的任何依赖实体时，单击**否**。</span><span class="sxs-lookup"><span data-stu-id="eaa4f-163">When prompted to include any dependent entities for the entities selected above, click **No**.</span></span>

> ![请勿包含全部相关组件](media/Do-not-include-required.png)


