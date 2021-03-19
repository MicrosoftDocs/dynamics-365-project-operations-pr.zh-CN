---
title: 为定价维度创建自定义解决方案
description: 此主题说明如何在创建自定义定价维度时创建自定义解决方案。
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
ms.openlocfilehash: 1d8117d6f6bcedc97264401fc941470f34efb1ae
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/15/2021
ms.locfileid: "5284977"
---
# <a name="create-custom-solutions-for-pricing-dimensions"></a><span data-ttu-id="e640d-103">为定价维度创建自定义解决方案</span><span class="sxs-lookup"><span data-stu-id="e640d-103">Create custom solutions for pricing dimensions</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

> [!IMPORTANT]
> <span data-ttu-id="e640d-104">所有自定义定价维度的更改都应在单独的解决方案中进行。</span><span class="sxs-lookup"><span data-stu-id="e640d-104">All custom pricing dimension changes should be in a separate solution.</span></span> <span data-ttu-id="e640d-105">这项重要的最佳实践让您可以在将来灵活地根据需要更新或删除更改，从而可以帮助您重复利用您的工作，并更轻松地将这些更改移植到其他实例中。</span><span class="sxs-lookup"><span data-stu-id="e640d-105">This important best practice provides flexibility in the future to update or remove changes as needed, will help with re-use of your work, and makes it easier to port these changes to another instance.</span></span> <span data-ttu-id="e640d-106">进行所有必需更改之后，将此解决方案作为 **托管解决方案** 导出，然后导入到其他实例中，以便重复利用您的定价设置。</span><span class="sxs-lookup"><span data-stu-id="e640d-106">After you make the required changes, export this solution as a **Managed solution**, and import it into other instances to reuse your pricing setup.</span></span>

1. <span data-ttu-id="e640d-107">选择 **设置** > **解决方案**，然后选择 **新建**。</span><span class="sxs-lookup"><span data-stu-id="e640d-107">Select **Settings** > **Solutions**, and then select **New**.</span></span> 
2. <span data-ttu-id="e640d-108">将该解决方案命名为 **\<your organization name> 定价维度**，输入其余必需信息，然后选择 **保存**。</span><span class="sxs-lookup"><span data-stu-id="e640d-108">Name the solution, **\<your organization name> pricing dimensions**, enter the remaining required information, and then select **Save**.</span></span>

> ![为定价维度创建自定义解决方案](media/Creation-of-custom-pricing-dimension-solution.PNG)
  
## <a name="add-all-required-entities-and-related-components-to-the-pricing-dimension-solution"></a><span data-ttu-id="e640d-110">向定价维度解决方案添加所有必需实体和相关组件</span><span class="sxs-lookup"><span data-stu-id="e640d-110">Add all required entities and related components to the Pricing dimension solution</span></span>
<span data-ttu-id="e640d-111">您需要向定价解决方案添加以下 Project Service 实体。</span><span class="sxs-lookup"><span data-stu-id="e640d-111">You will need to add the following Project Service entities to your pricing solution.</span></span> <span data-ttu-id="e640d-112">完成此过程中的步骤在定价解决方案中进行一些重要的架构更改，以便实体可以识别新的定价维度。</span><span class="sxs-lookup"><span data-stu-id="e640d-112">Complete the steps in this procedure to make some important schema changes in the pricing solution so that the entities become aware of the new pricing dimensions.</span></span>

1. <span data-ttu-id="e640d-113">选择 **设置** > **解决方案**，然后双击 **\<your organization name> 定价维度**。</span><span class="sxs-lookup"><span data-stu-id="e640d-113">Select **Settings** > **Solutions**, and then double-click **\<your organization name> pricing dimensions**.</span></span> 
2. <span data-ttu-id="e640d-114">在解决方案资源管理器中左侧导航窗格上，选择 **添加现有** > **实体**。</span><span class="sxs-lookup"><span data-stu-id="e640d-114">In Solution Explorer, on the left navigation pane, select **Add Existing** > **Entities**.</span></span>
3. <span data-ttu-id="e640d-115">在 **解决方案组件** 对话框中，选择以下实体：</span><span class="sxs-lookup"><span data-stu-id="e640d-115">In the **Solution Components** dialog box, select the following entities:</span></span>

- <span data-ttu-id="e640d-116">实际</span><span class="sxs-lookup"><span data-stu-id="e640d-116">Actual</span></span>
- <span data-ttu-id="e640d-117">可预订资源</span><span class="sxs-lookup"><span data-stu-id="e640d-117">Bookable Resource</span></span>
- <span data-ttu-id="e640d-118">估计值明细</span><span class="sxs-lookup"><span data-stu-id="e640d-118">Estimate Line</span></span>
- <span data-ttu-id="e640d-119">项目任务</span><span class="sxs-lookup"><span data-stu-id="e640d-119">Project Task</span></span>
- <span data-ttu-id="e640d-120">发票明细详细信息</span><span class="sxs-lookup"><span data-stu-id="e640d-120">Invoice Line Detail</span></span>
- <span data-ttu-id="e640d-121">日记帐行</span><span class="sxs-lookup"><span data-stu-id="e640d-121">Journal Line</span></span>
- <span data-ttu-id="e640d-122">项目合同子项详细信息</span><span class="sxs-lookup"><span data-stu-id="e640d-122">Project Contract Line Detail</span></span>
- <span data-ttu-id="e640d-123">项目团队成员</span><span class="sxs-lookup"><span data-stu-id="e640d-123">Project Team Member</span></span>
- <span data-ttu-id="e640d-124">报价单行明细</span><span class="sxs-lookup"><span data-stu-id="e640d-124">Quote Line Detail</span></span>
- <span data-ttu-id="e640d-125">角色价格加价</span><span class="sxs-lookup"><span data-stu-id="e640d-125">Role Price Markup</span></span>
- <span data-ttu-id="e640d-126">角色价格</span><span class="sxs-lookup"><span data-stu-id="e640d-126">Role Price</span></span> 
- <span data-ttu-id="e640d-127">时间条目</span><span class="sxs-lookup"><span data-stu-id="e640d-127">Time Entry</span></span> 

> ![向定价维度解决方案添加现有实体](media/Existing-entities-to-PD-solution.png)

> ![选择解决方案组件](media/Dimension-Components.png)

> [!NOTE]
> <span data-ttu-id="e640d-130">务必包括所选每个实体的所有窗体和视图。</span><span class="sxs-lookup"><span data-stu-id="e640d-130">Make sure to include all forms and views for each of the entities selected.</span></span>

4. <span data-ttu-id="e640d-131">当系统提示包括所选实体的任何依赖实体时，选择 **否**。</span><span class="sxs-lookup"><span data-stu-id="e640d-131">When prompted to include any dependent entities for the selected entities, select **No**.</span></span>

> ![请勿包含全部相关组件](media/Do-not-include-required.png)




[!INCLUDE[footer-include](../includes/footer-banner.md)]