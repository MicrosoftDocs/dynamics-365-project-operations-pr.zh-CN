---
title: 为自定义定价维度创建解决方案
description: 本主题提供了有关如何为自定义定价维度创建解决方案的信息。
author: Rumant
manager: tfehr
ms.date: 11/09/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 441501dff23d16960381b3f9fb4b2cceba2b3ba5
ms.sourcegitcommit: 869bde007805ef255f61b03937e4a44aeef61df9
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/12/2020
ms.locfileid: "4513963"
---
# <a name="create-a-solution-for-custom-pricing-dimensions"></a><span data-ttu-id="f5e72-103">为自定义定价维度创建解决方案</span><span class="sxs-lookup"><span data-stu-id="f5e72-103">Create a solution for custom pricing dimensions</span></span>

 <span data-ttu-id="f5e72-104">_**适用于：** 基于资源/非库存场景的 Project Operations，精简部署 - 估价开票交易_</span><span class="sxs-lookup"><span data-stu-id="f5e72-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span> 

>[!IMPORTANT]
><span data-ttu-id="f5e72-105">所有自定义定价维度的更改都应在单独的解决方案中进行。</span><span class="sxs-lookup"><span data-stu-id="f5e72-105">All custom pricing dimension changes should be in a separate solution.</span></span> <span data-ttu-id="f5e72-106">这项重要的最佳实践让您可以灵活地根据需要更新或删除更改，从而可以帮助您重复利用您的工作，并更轻松地将这些更改移植到其他实例中。</span><span class="sxs-lookup"><span data-stu-id="f5e72-106">This important best practice allows the flexibility to update or remove changes as needed, helps with re-use of your work, and makes it easier to port changes to other instances.</span></span> <span data-ttu-id="f5e72-107">进行了所有必需更改之后，将此解决方案作为 **托管** 解决方案导出，然后导入到其他实例中，以便重复利用。</span><span class="sxs-lookup"><span data-stu-id="f5e72-107">After you make the required changes, export this solution as a **Managed** solution, and then import into other instances for reuse.</span></span>

## <a name="create-a-solution-for-custom-pricing-dimensions"></a><span data-ttu-id="f5e72-108">为自定义定价维度创建解决方案</span><span class="sxs-lookup"><span data-stu-id="f5e72-108">Create a solution for custom pricing dimensions</span></span>

1.  <span data-ttu-id="f5e72-109">选择 **设置** > **解决方案**，然后选择 **新建**。</span><span class="sxs-lookup"><span data-stu-id="f5e72-109">Select **Settings** > **Solutions**, and then select **New**.</span></span>
2.  <span data-ttu-id="f5e72-110">将此解决方案命名为 *<your organization name> 定价维度*。</span><span class="sxs-lookup"><span data-stu-id="f5e72-110">Name the solution, *<your organization name> pricing dimensions*.</span></span>
3. <span data-ttu-id="f5e72-111">输入其余所需信息，然后选择 **保存**。</span><span class="sxs-lookup"><span data-stu-id="f5e72-111">Enter the remaining required information, and then select **Save**.</span></span>

  ![创建自定义定价维度解决方案](./media/Creation-of-custom-pricing-dimension-solution.png)
 
## <a name="add-all-required-entities-and-related-components-to-the-pricing-dimension-solution"></a><span data-ttu-id="f5e72-113">向定价维度解决方案添加所有必需实体和相关组件</span><span class="sxs-lookup"><span data-stu-id="f5e72-113">Add all required entities and related components to the Pricing dimension solution</span></span>

<span data-ttu-id="f5e72-114">将以下 Project Service 实体添加到定价解决方案中，以在定价解决方案中进行重要的架构更改。</span><span class="sxs-lookup"><span data-stu-id="f5e72-114">Add the following Project Service entities to your pricing solution to make important schema changes in the pricing solution.</span></span> <span data-ttu-id="f5e72-115">完成此过程后，实体将识别新的定价维度。</span><span class="sxs-lookup"><span data-stu-id="f5e72-115">After you have completed this procedure, the entities will recognize the new pricing dimensions.</span></span>

1.  <span data-ttu-id="f5e72-116">选择 **设置** > **解决方案**，然后双击 **<*您的组织名称*> 定价维度**。</span><span class="sxs-lookup"><span data-stu-id="f5e72-116">Select **Settings** > **Solutions**, and then double-click **<*your organization name*> pricing dimensions**.</span></span>
2.  <span data-ttu-id="f5e72-117">在解决方案资源管理器中左侧导航窗格上，选择 **添加现有** > **实体**。</span><span class="sxs-lookup"><span data-stu-id="f5e72-117">In Solution Explorer, on the left navigation pane, select **Add Existing** > **Entities**.</span></span>
3.  <span data-ttu-id="f5e72-118">在 **解决方案组件** 对话框中，选择以下实体：</span><span class="sxs-lookup"><span data-stu-id="f5e72-118">In the **Solution Components** dialog box, select the following entities:</span></span>
 
   - <span data-ttu-id="f5e72-119">**实际**</span><span class="sxs-lookup"><span data-stu-id="f5e72-119">**Actual**</span></span>
   - <span data-ttu-id="f5e72-120">**可预订资源**</span><span class="sxs-lookup"><span data-stu-id="f5e72-120">**Bookable Resource**</span></span>
   - <span data-ttu-id="f5e72-121">**估计值明细**</span><span class="sxs-lookup"><span data-stu-id="f5e72-121">**Estimate Line**</span></span>
   - <span data-ttu-id="f5e72-122">**项目任务**</span><span class="sxs-lookup"><span data-stu-id="f5e72-122">**Project Task**</span></span>
   - <span data-ttu-id="f5e72-123">**发票明细详细信息**</span><span class="sxs-lookup"><span data-stu-id="f5e72-123">**Invoice Line Detail**</span></span>
   - <span data-ttu-id="f5e72-124">**日记帐行**</span><span class="sxs-lookup"><span data-stu-id="f5e72-124">**Journal Line**</span></span>
   - <span data-ttu-id="f5e72-125">**项目合同子项详细信息**</span><span class="sxs-lookup"><span data-stu-id="f5e72-125">**Project Contract Line Detail**</span></span>
   - <span data-ttu-id="f5e72-126">**项目团队成员**</span><span class="sxs-lookup"><span data-stu-id="f5e72-126">**Project Team Member**</span></span>
   - <span data-ttu-id="f5e72-127">**报价单行明细**</span><span class="sxs-lookup"><span data-stu-id="f5e72-127">**Quote Line Detail**</span></span>
   - <span data-ttu-id="f5e72-128">**角色价格加价**</span><span class="sxs-lookup"><span data-stu-id="f5e72-128">**Role Price Markup**</span></span>
   - <span data-ttu-id="f5e72-129">**角色价格**</span><span class="sxs-lookup"><span data-stu-id="f5e72-129">**Role Price**</span></span>
   - <span data-ttu-id="f5e72-130">**时间条目**</span><span class="sxs-lookup"><span data-stu-id="f5e72-130">**Time Entry**</span></span>
 
   ![添加现有实体的自定义定价维度解决方案](./media/Existing-entities-to-PD-solution.png)
 
 4. <span data-ttu-id="f5e72-132">对于每个实体，查看要添加的组件以及每个实体的实体资产最终列表。</span><span class="sxs-lookup"><span data-stu-id="f5e72-132">For each entity, review the components being added and the final list of entity assets for each entity.</span></span> 

   >[!NOTE]
   > <span data-ttu-id="f5e72-133">包括所选每个实体的所有窗体和视图。</span><span class="sxs-lookup"><span data-stu-id="f5e72-133">Include all forms and views for each of the selected entities.</span></span>

  ![已添加实体](./media/solution-component-selection.png)


5.  <span data-ttu-id="f5e72-135">当提示包括所选实体的任何相关实体时，选择 **否，不包含必需组件。**</span><span class="sxs-lookup"><span data-stu-id="f5e72-135">When prompted to include any dependent entities for the selected entities, select **No, do not include required components.**</span></span>

    ![包括相关实体](./media/Do-not-include-required.png)
