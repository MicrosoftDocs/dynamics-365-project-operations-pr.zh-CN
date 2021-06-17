---
title: 创建自定义字段和实体，作为定价维度
description: 此主题提供有关如何创建自定义选项集或实体的信息。
author: rumant
ms.date: 11/18/2020
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 41c57690fecbc3bee2a1eb5d26f8a6aa56d8bea9
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/10/2021
ms.locfileid: "6000515"
---
# <a name="create-custom-fields-and-entities-as-pricing-dimensions"></a><span data-ttu-id="c5776-103">创建自定义字段和实体，作为定价维度</span><span class="sxs-lookup"><span data-stu-id="c5776-103">Create custom fields and entities as pricing dimensions</span></span>

<span data-ttu-id="c5776-104">_**适用于：** 基于资源/非库存场景的 Project Operations，精简部署 - 估价开票交易_</span><span class="sxs-lookup"><span data-stu-id="c5776-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="c5776-105">要创建自定义选项集或实体以将其用作定价维度时，请完成以下步骤。</span><span class="sxs-lookup"><span data-stu-id="c5776-105">Complete the following steps when you want to create a custom option set or entity for using it as a pricing dimension.</span></span> <span data-ttu-id="c5776-106">有关详细信息，请参阅[定价维度概述](pricing-dimensions-overview.md)。</span><span class="sxs-lookup"><span data-stu-id="c5776-106">For more information, see [Pricing dimensions overview](pricing-dimensions-overview.md).</span></span>  

> [!IMPORTANT]
> <span data-ttu-id="c5776-107">建议在单独的解决方案中进行所有自定义定价维度更改。</span><span class="sxs-lookup"><span data-stu-id="c5776-107">We recommend that you make all custom pricing dimension changes in a separate solution.</span></span> <span data-ttu-id="c5776-108">此重要的最佳实践为将来根据需要更新或删除更改提供了灵活性。</span><span class="sxs-lookup"><span data-stu-id="c5776-108">This important best practice provides flexibility in the future to update or remove changes as needed.</span></span> <span data-ttu-id="c5776-109">这还将有助于重复使用您的工作，并且在完成所有必需的更改后更便于将这些更改加载到其他实例中，请将此解决方案导出为 **托管解决方案**，并将其导入到其他实例中，以重复使用定价设置。</span><span class="sxs-lookup"><span data-stu-id="c5776-109">This will also help with re-use of your work and make it easier to port these changes to another instance After you have made all of the required changes, export this solution as a **Managed solution** and import it into other instances to reuse your pricing setup.</span></span>

  
## <a name="create-custom-fields-and-option-sets-in-the-pricing-dimension-solution"></a><span data-ttu-id="c5776-110">在定价维度解决方案中创建自定义字段和选项集</span><span class="sxs-lookup"><span data-stu-id="c5776-110">Create custom fields and option sets in the pricing dimension solution</span></span>

<span data-ttu-id="c5776-111">定价维度可以是选项集或实体。</span><span class="sxs-lookup"><span data-stu-id="c5776-111">A pricing dimension can be an option set or an entity.</span></span> <span data-ttu-id="c5776-112">两种都必须在定价解决方案中创建。</span><span class="sxs-lookup"><span data-stu-id="c5776-112">Both must be created in your pricing solution.</span></span> <span data-ttu-id="c5776-113">此过程中的步骤介绍如何创建基于实体的维度和基于选项集的维度。</span><span class="sxs-lookup"><span data-stu-id="c5776-113">The steps in this procedure explain how to create entity-based dimensions and option set-based dimensions.</span></span>

### <a name="entity-based-dimensions"></a><span data-ttu-id="c5776-114">基于实体的维度</span><span class="sxs-lookup"><span data-stu-id="c5776-114">Entity-based dimensions</span></span>
<span data-ttu-id="c5776-115">若要创建基于实体的维度，请执行以下步骤：</span><span class="sxs-lookup"><span data-stu-id="c5776-115">To create entity-based dimensions, follow these steps:</span></span>

1. <span data-ttu-id="c5776-116">转到 **设置** > **解决方案**，然后双击 **\<your organization name> 定价维度**。</span><span class="sxs-lookup"><span data-stu-id="c5776-116">Go to **Settings** > **Solutions**, and then double-click **\<your organization name> pricing dimensions**.</span></span>
2. <span data-ttu-id="c5776-117">在解决方案资源管理器内的左侧导航窗格中，选择 **实体**。</span><span class="sxs-lookup"><span data-stu-id="c5776-117">In Solution Explorer, in the left navigation pane, select **Entities**.</span></span>
3. <span data-ttu-id="c5776-118">选择 **新建** 创建一个IE名称为 **标准标题** 的新实体。</span><span class="sxs-lookup"><span data-stu-id="c5776-118">Select **New** to create a new entity called **Standard Title**.</span></span> 
4. <span data-ttu-id="c5776-119">输入其余所需信息，然后选择 **保存**。</span><span class="sxs-lookup"><span data-stu-id="c5776-119">Enter the remaining required information, and then select **Save**.</span></span>

> ![标准标题实体定义](media/Standard-Title-entity-definition.png)

### <a name="option-set-based-dimensions"></a><span data-ttu-id="c5776-121">基于选项集的维度</span><span class="sxs-lookup"><span data-stu-id="c5776-121">Option set-based dimensions</span></span> 
<span data-ttu-id="c5776-122">可创建两个基于选项集的维度。</span><span class="sxs-lookup"><span data-stu-id="c5776-122">You can create two option set-based dimensions.</span></span> 

- <span data-ttu-id="c5776-123">**资源工作位置** 用于跟踪 **当前** 位置工作和 **现场** 工作的价格。</span><span class="sxs-lookup"><span data-stu-id="c5776-123">Use **Resource Work Location** to track the price of **Home** location work and **Onsite** work.</span></span> 
- <span data-ttu-id="c5776-124">值为 **常规** 和 **加班** 的 **资源工作时间** 用于在完成工作时应用加价。</span><span class="sxs-lookup"><span data-stu-id="c5776-124">Use **Resource Work hours** with values **Regular** and **Overtime** to apply a markup when the work is complete.</span></span>

<span data-ttu-id="c5776-125">下图提供了 **资源工作位置** 维度的视图。</span><span class="sxs-lookup"><span data-stu-id="c5776-125">The following graphic provides a view of the **Resource Work Location** dimension.</span></span> 

> ![称为“资源工作位置”且基于选项集的定价维度](media/Option-set-PD-called-Resource-Work-Location.png)

<span data-ttu-id="c5776-127">下图提供了 **资源工作时间** 维度的视图。</span><span class="sxs-lookup"><span data-stu-id="c5776-127">The following graphic provides a view of the **Resource Work Hours** dimension.</span></span> 

> ![称为“资源工作时间”且基于选项集的定价维度](media/Option-set-PD-called-Resource-Work-Hours.png)

1. <span data-ttu-id="c5776-129">转到 **设置** > **解决方案**，双击 **\<your organization name> 定价维度**。</span><span class="sxs-lookup"><span data-stu-id="c5776-129">Go to **Settings** > **Solutions**, and double-click  **\<your organization name> pricing dimensions**.</span></span> 
2. <span data-ttu-id="c5776-130">在解决方案资源管理器内的左侧导航窗格中，选择 **选项集**。</span><span class="sxs-lookup"><span data-stu-id="c5776-130">In Solution Explorer, in the left navigation pane, select  **Option Sets**.</span></span> 
3. <span data-ttu-id="c5776-131">选择 **新建** 创建一个新的选项集，输入其余必需信息，然后选择 **保存**。</span><span class="sxs-lookup"><span data-stu-id="c5776-131">Select **New** to create a new option set, enter the remaining required information, and then select **Save**.</span></span>

## <a name="create-data-for-entity-based-dimensions"></a><span data-ttu-id="c5776-132">为基于实体的维度创建数据</span><span class="sxs-lookup"><span data-stu-id="c5776-132">Create data for entity-based dimensions</span></span>

<span data-ttu-id="c5776-133">可手动为基于实体的维度创建数据，也可以使用 Microsoft Excel 导入或服务调用创建。</span><span class="sxs-lookup"><span data-stu-id="c5776-133">You can create data for entity-based dimensions manually, or by using Microsoft Excel import or service calls.</span></span> <span data-ttu-id="c5776-134">使用此过程中的步骤从基于实体的维度 **标准标题** 创建两个标准标题：**系统工程师** 和 **高级系统工程师**。</span><span class="sxs-lookup"><span data-stu-id="c5776-134">Use the steps in this procedure to create two standard titles, **Systems Engineer** and **Senior Systems Engineer** from the entity-based dimension, **Standard Title**.</span></span> <span data-ttu-id="c5776-135">如果要创建的数据很少（如在以下示例中），可以使用标准窗体。</span><span class="sxs-lookup"><span data-stu-id="c5776-135">If the data that you want to create is small, as in the following example, you can use a standard form.</span></span>

1. <span data-ttu-id="c5776-136">选择 **高级查找**。</span><span class="sxs-lookup"><span data-stu-id="c5776-136">Select **Advanced Find**.</span></span>
2. <span data-ttu-id="c5776-137">选择实体 **标准标题**，然后选择 **结果**。</span><span class="sxs-lookup"><span data-stu-id="c5776-137">Select the entity **Standard Title**, and then select **Results**.</span></span> <span data-ttu-id="c5776-138">将显示 **标准标题** 实体中的所有行。</span><span class="sxs-lookup"><span data-stu-id="c5776-138">All of the rows in the **Standard Title** entity will be shown.</span></span>
3. <span data-ttu-id="c5776-139">选择 **新建**，在 **名称** 字段中，输入“系统工程师”，然后选择 **保存**。</span><span class="sxs-lookup"><span data-stu-id="c5776-139">Select **New**, and in the **Name** field, enter "Systems Engineer" and then select **Save**.</span></span>
4. <span data-ttu-id="c5776-140">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="c5776-140">Close the page.</span></span> 
5. <span data-ttu-id="c5776-141">重复步骤 1 - 3 再为“高级系统工程师”创建一个标准标题。</span><span class="sxs-lookup"><span data-stu-id="c5776-141">Repeat steps 1-3 to create another standard title for "Senior Systems Engineer".</span></span>

> ![标准标题实体的示例数据](media/ST-data.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]