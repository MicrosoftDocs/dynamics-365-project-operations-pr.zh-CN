---
title: 创建自定义字段和实体
description: 此主题介绍在 Power Apps 平台中如何在自己的解决方案内创建选项集和实体。
author: Rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 10/01/2020
ms.topic: article
ms.service: business-applications
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: b9e32c8871a8986ba827f742baf4e4d5cd9dd235
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/10/2021
ms.locfileid: "5144852"
---
# <a name="create-custom-fields-and-entities"></a><span data-ttu-id="7d307-103">创建自定义字段和实体</span><span class="sxs-lookup"><span data-stu-id="7d307-103">Create custom fields and entities</span></span> 

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="7d307-104">如果要在 Power Apps 平台中创建自定义选项集或实体，随时可完成以下步骤。</span><span class="sxs-lookup"><span data-stu-id="7d307-104">Complete the following steps any time that you want to create a custom option set or entity on the Power Apps platform.</span></span>  
<span data-ttu-id="7d307-105">此主题中的过程应使用 Project Service Automation (PSA) 的 Web 界面完成。</span><span class="sxs-lookup"><span data-stu-id="7d307-105">The procedures in this topic should be completed using the web interface of Project Service Automation (PSA).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="7d307-106">建议在单独的解决方案中进行所有自定义定价维度更改。</span><span class="sxs-lookup"><span data-stu-id="7d307-106">We recommend that you make all custom pricing dimension changes in a separate solution.</span></span> <span data-ttu-id="7d307-107">这项重要的最佳实践让您可以在将来灵活地根据需要更新或删除更改，从而可以帮助您重复利用您的工作，并更轻松地将这些更改移植到其他实例中。</span><span class="sxs-lookup"><span data-stu-id="7d307-107">This important best practice provides flexibility in the future to update or remove changes as needed, will help with re-use of your work, and makes it easier to port these changes to another instance.</span></span> <span data-ttu-id="7d307-108">进行了所有必需更改之后，将此解决方案作为 **托管解决方案** 导出，然后导入到其他实例中，以便重复利用您的定价设置。</span><span class="sxs-lookup"><span data-stu-id="7d307-108">After you have made all of the required changes, export this solution as a **Managed solution** and import it into other instances to reuse your pricing setup.</span></span>

  
## <a name="create-custom-fields-and-option-sets-in-the-pricing-dimension-solution"></a><span data-ttu-id="7d307-109">在定价维度解决方案中创建自定义字段和选项集</span><span class="sxs-lookup"><span data-stu-id="7d307-109">Create custom fields and option sets in the pricing dimension solution</span></span>

<span data-ttu-id="7d307-110">定价维度可以是选项集或实体。</span><span class="sxs-lookup"><span data-stu-id="7d307-110">A pricing dimension can be an option set or an entity.</span></span> <span data-ttu-id="7d307-111">两种都必须在定价解决方案中创建。</span><span class="sxs-lookup"><span data-stu-id="7d307-111">Both must be created in your pricing solution.</span></span> <span data-ttu-id="7d307-112">此过程中的步骤介绍如何创建基于实体的维度和基于选项集的维度。</span><span class="sxs-lookup"><span data-stu-id="7d307-112">The steps in this procedure explain how to create entity-based dimensions and option set-based dimensions.</span></span>

### <a name="entity-based-dimensions"></a><span data-ttu-id="7d307-113">基于实体的维度</span><span class="sxs-lookup"><span data-stu-id="7d307-113">Entity-based dimensions</span></span>

1. <span data-ttu-id="7d307-114">在 PSA 中，单击 **设置** > **解决方案**，然后双击 **\<your organization name> 定价维度**。</span><span class="sxs-lookup"><span data-stu-id="7d307-114">In PSA, click **Settings** > **Solutions**, and then double-click **\<your organization name> pricing dimensions**.</span></span>
2. <span data-ttu-id="7d307-115">在解决方案资源管理器中左侧导航窗格上，选择 **实体**。</span><span class="sxs-lookup"><span data-stu-id="7d307-115">In Solution Explorer, on the left navigation pane, select **Entities**.</span></span>
3. <span data-ttu-id="7d307-116">单击 **新建** 创建一个IE名称为 **标准标题** 的新实体。</span><span class="sxs-lookup"><span data-stu-id="7d307-116">Click **New** to create a new entity called **Standard Title**.</span></span> <span data-ttu-id="7d307-117">输入其余所需信息，然后单击 **保存**。</span><span class="sxs-lookup"><span data-stu-id="7d307-117">Enter the remaining required information, and then click **Save**.</span></span>

> ![标准标题实体定义](media/Standard-Title-entity-definition.png)


### <a name="option-set-based-dimensions"></a><span data-ttu-id="7d307-119">基于选项集的维度</span><span class="sxs-lookup"><span data-stu-id="7d307-119">Option set-based dimensions</span></span> 
<span data-ttu-id="7d307-120">可创建两个基于选项集的维度。</span><span class="sxs-lookup"><span data-stu-id="7d307-120">You can create two option set-based dimensions.</span></span> <span data-ttu-id="7d307-121">**资源工作位置** 用于跟踪 **当前** 位置工作和 **现场** 工作的价格，值为 **常规** 和 **加班** 的 **资源工作时间** 用于在完成工作时应用加价。</span><span class="sxs-lookup"><span data-stu-id="7d307-121">Use **Resource Work Location** to track the price of **Home** location work and **Onsite** work and use **Resource Work hours** with values **Regular** and **Overtime** to apply a markup when work is completed.</span></span>


1. <span data-ttu-id="7d307-122">在 PSA 中，单击 **设置** > **解决方案**，然后双击 **\<your organization name> 定价维度**。</span><span class="sxs-lookup"><span data-stu-id="7d307-122">In PSA, click **Settings** > **Solutions**, and then double-click  **\<your organization name> pricing dimensions**.</span></span> 
2. <span data-ttu-id="7d307-123">在解决方案资源管理器中左侧导航窗格上，选择 **选项集**。</span><span class="sxs-lookup"><span data-stu-id="7d307-123">In Solution Explorer, on the left navigation pane, select  **Option Sets**.</span></span> 
3. <span data-ttu-id="7d307-124">单击 **新建** 创建一个新的选项集，输入其余必需信息，然后单击 **保存**。</span><span class="sxs-lookup"><span data-stu-id="7d307-124">Click **New** to create a new option set, enter the remaining required information, and then click **Save**.</span></span>

> ![<span data-ttu-id="7d307-125">称为“资源工作位置”且基于选项集的定价维度</span><span class="sxs-lookup"><span data-stu-id="7d307-125">Option set based pricing dimension called Resource Work Location</span></span> ](media/Option-set-PD-called-Resource-Work-Location.png)

> ![<span data-ttu-id="7d307-126">称为“资源工作时间”且基于选项集的定价维度</span><span class="sxs-lookup"><span data-stu-id="7d307-126">Option set based pricing dimension called Resource Work Hours</span></span> ](media/Option-set-PD-called-Resource-Work-Hours.PNG)


## <a name="create-data-for-entity-based-dimensions"></a><span data-ttu-id="7d307-127">为基于实体的维度创建数据</span><span class="sxs-lookup"><span data-stu-id="7d307-127">Create data for entity-based dimensions</span></span>

<span data-ttu-id="7d307-128">可手动为基于实体的维度创建数据，也可以使用 Microsoft Excel 导入或服务调用创建。</span><span class="sxs-lookup"><span data-stu-id="7d307-128">You can create data for entity-based dimensions manually, or by using Microsoft Excel import or service calls.</span></span> <span data-ttu-id="7d307-129">使用此过程中的步骤从基于实体的维度 **标准标题** 创建两个标准标题：**系统工程师** 和 **高级系统工程师**。</span><span class="sxs-lookup"><span data-stu-id="7d307-129">Use the steps in this procedure to create two standard titles, **Systems Engineer** and **Senior Systems Engineer** from the entity-based dimension, **Standard Title**.</span></span> <span data-ttu-id="7d307-130">如果要创建的数据很少（如在以下示例中），可以使用标准窗体。</span><span class="sxs-lookup"><span data-stu-id="7d307-130">If the data that you want to create is small, as in the following example, you can use a standard form.</span></span>

1. <span data-ttu-id="7d307-131">在 PSA 中，单击 **高级查找**。</span><span class="sxs-lookup"><span data-stu-id="7d307-131">In PSA, click **Advanced Find**.</span></span> <span data-ttu-id="7d307-132">选择实体 **标准标题**，然后单击 **结果**。</span><span class="sxs-lookup"><span data-stu-id="7d307-132">Select the entity **Standard Title** and then click **Results**.</span></span> <span data-ttu-id="7d307-133">将显示 **标准标题** 实体中的所有行。</span><span class="sxs-lookup"><span data-stu-id="7d307-133">All of the rows in the **Standard Title** entity will be shown.</span></span>
2. <span data-ttu-id="7d307-134">单击 **新建**。</span><span class="sxs-lookup"><span data-stu-id="7d307-134">Click **New**.</span></span> <span data-ttu-id="7d307-135">在 **名称** 字段中，输入“系统工程师”，然后单击 **保存**。</span><span class="sxs-lookup"><span data-stu-id="7d307-135">In the **Name** field, enter "Systems Engineer" and then click **Save**.</span></span>
3. <span data-ttu-id="7d307-136">关闭窗体。</span><span class="sxs-lookup"><span data-stu-id="7d307-136">Close the form.</span></span> 
4. <span data-ttu-id="7d307-137">重复步骤 1 - 3 再为“高级系统工程师”创建一个标准标题。</span><span class="sxs-lookup"><span data-stu-id="7d307-137">Repeat steps 1 - 3 to create another standard title for "Senior Systems Engineer".</span></span>

> ![<span data-ttu-id="7d307-138">标准标题实体的示例数据</span><span class="sxs-lookup"><span data-stu-id="7d307-138">Sample Data for Standard Title entity</span></span> ](media/ST-data.png)


