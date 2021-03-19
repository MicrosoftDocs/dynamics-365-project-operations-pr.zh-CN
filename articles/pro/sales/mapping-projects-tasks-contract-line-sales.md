---
title: 将项目和任务映射到基于项目的合同子项 - 精简
description: 此主题提供有关在合同子项中添加和删除项目与任务的信息。
author: rumant
manager: Annbe
ms.date: 10/27/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: c5c29872ef3d62780eea3c0eda48c8fd2a9af4b1
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/15/2021
ms.locfileid: "5272782"
---
# <a name="map-projects-and-tasks-to-a-project-based-contract-line---lite"></a><span data-ttu-id="6b1aa-103">将项目和任务映射到基于项目的合同子项 - 精简</span><span class="sxs-lookup"><span data-stu-id="6b1aa-103">Map projects and tasks to a project-based contract line - lite</span></span>

<span data-ttu-id="6b1aa-104">_**适用于：** 精简部署 - 估价交易开票_</span><span class="sxs-lookup"><span data-stu-id="6b1aa-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="6b1aa-105">在基于项目的合同子项上，您可以将项目中的特定任务映射到合同子项。</span><span class="sxs-lookup"><span data-stu-id="6b1aa-105">On project-based contract lines, you can map specific tasks in a project to the contract line.</span></span>

<span data-ttu-id="6b1aa-106">当您将特定任务映射到合同子项时，合同子项中定义的计费方法、应计费选项、上限以及客户仅适用于这些特定任务。</span><span class="sxs-lookup"><span data-stu-id="6b1aa-106">When you map specific tasks to a contract line, the billing method, chargeability options, Not-to-exceed limits, and the customers defined on the contract line will be applicable to those specific tasks only.</span></span>

<span data-ttu-id="6b1aa-107">如果您遇到项目的一个阶段（例如，原型阶段）是固定价格，所有其他阶段都是时间和材料的情形，您可以将原型阶段和所有关联的子任务与具有固定价格计费方法的那个阶段的合同子项相关联。</span><span class="sxs-lookup"><span data-stu-id="6b1aa-107">If you have a scenario where one phase of a project, for example the Prototype Phase, is fixed price and all the other phases are time and material, you will be able to associate the Prototype phase and all the associated child tasks to the contract line for that phase with a fixed price billing method.</span></span>

<span data-ttu-id="6b1aa-108">您的项目工作分解结构 (WBS) 中的所有其他阶段都可以与基于时间和材料的合同子项相关联。</span><span class="sxs-lookup"><span data-stu-id="6b1aa-108">All the other phases in your project work breakdown structure (WBS) can be associated to the time and material-based contract line.</span></span>

## <a name="associate-tasks-to-project-based-contract-lines"></a><span data-ttu-id="6b1aa-109">将任务与基于项目的合同子项关联</span><span class="sxs-lookup"><span data-stu-id="6b1aa-109">Associate tasks to project-based contract lines</span></span>

<span data-ttu-id="6b1aa-110">任务可以从 **合同子项** 页上的 **应计费任务** 选项卡或 **项目** 页上的 **任务计费** 选项卡与合同子项关联。</span><span class="sxs-lookup"><span data-stu-id="6b1aa-110">Tasks can be associated to contract lines from the **Chargeable Tasks** tab on the **Contract Line** page or from the **Task Billing** tab on the **Project** page.</span></span>

### <a name="from-the-contract-line-page"></a><span data-ttu-id="6b1aa-111">从“合同子项”页</span><span class="sxs-lookup"><span data-stu-id="6b1aa-111">From the Contract line page</span></span>

<span data-ttu-id="6b1aa-112">完成以下步骤，从 **合同子项** 页的 **应计费任务** 选项卡将项目任务与合同子项关联。</span><span class="sxs-lookup"><span data-stu-id="6b1aa-112">Complete the following steps to associate project tasks to the contract line from the **Chargeable Tasks** tab of the **Contract Line** page.</span></span>

1. <span data-ttu-id="6b1aa-113">在基于项目的合同子项的 **常规** 选项卡上，验证 **项目** 字段是否填充。</span><span class="sxs-lookup"><span data-stu-id="6b1aa-113">On the **General** tab of a project-based contract line, verify that the **Project** field is filled out.</span></span>
2. <span data-ttu-id="6b1aa-114">在 **包含的任务** 字段中，选择 **仅所选任务**。</span><span class="sxs-lookup"><span data-stu-id="6b1aa-114">In the **Included Tasks** field, select the **Selected Tasks Only**.</span></span>
3. <span data-ttu-id="6b1aa-115">保存您的更改。</span><span class="sxs-lookup"><span data-stu-id="6b1aa-115">Save your changes.</span></span> <span data-ttu-id="6b1aa-116">窗体将刷新，**应计费任务** 选项卡将显示。</span><span class="sxs-lookup"><span data-stu-id="6b1aa-116">The form will refresh and the **Chargeable Tasks** tab will be visible.</span></span>
4. <span data-ttu-id="6b1aa-117">选择 **应计费任务** 选项卡，在子网格中选择 **添加合同子项任务**。</span><span class="sxs-lookup"><span data-stu-id="6b1aa-117">Select the **Chargeable Tasks** tab, and in the subgrid, select **Add a Contract Line Task**.</span></span>
5. <span data-ttu-id="6b1aa-118">在 **合同子项任务** 页上的 **任务** 下拉列表中，选择任务。</span><span class="sxs-lookup"><span data-stu-id="6b1aa-118">On the **Contract Line Tasks** page, in the **Tasks** drop-down, select the task.</span></span> 
6. <span data-ttu-id="6b1aa-119">在 **计费类型** 字段中输入信息，然后选择 **保存并关闭**。</span><span class="sxs-lookup"><span data-stu-id="6b1aa-119">Enter information in the **Billing Type** field, and then select **Save and Close**.</span></span> <span data-ttu-id="6b1aa-120">所选任务已与合同子项关联。</span><span class="sxs-lookup"><span data-stu-id="6b1aa-120">The selected task is associated to the contract line.</span></span>

> [!NOTE]
> <span data-ttu-id="6b1aa-121">这不是将项目任务关联到合同子项的最佳体验。</span><span class="sxs-lookup"><span data-stu-id="6b1aa-121">This is not the most optimal experience for associating project tasks to contract lines.</span></span> <span data-ttu-id="6b1aa-122">在此体验中，每个项目都必须手动关联。</span><span class="sxs-lookup"><span data-stu-id="6b1aa-122">Each project will have to be manually associated in this experience.</span></span> <span data-ttu-id="6b1aa-123">首选方法是使用 **项目** 页上的 **任务计费** 选项卡。</span><span class="sxs-lookup"><span data-stu-id="6b1aa-123">The preferred way is from the **Task Billing** tab on the **Project** page.</span></span>

### <a name="from-the-project-page"></a><span data-ttu-id="6b1aa-124">从“项目”页</span><span class="sxs-lookup"><span data-stu-id="6b1aa-124">From the project page</span></span>

<span data-ttu-id="6b1aa-125">这是将任务关联到合同子项的最佳方法。</span><span class="sxs-lookup"><span data-stu-id="6b1aa-125">This is the optimal method to associate tasks to contract lines.</span></span> <span data-ttu-id="6b1aa-126">您可以选择多个任务，然后将它们及子任务关联到所选合同子项。</span><span class="sxs-lookup"><span data-stu-id="6b1aa-126">You can select multiple tasks and associate all of the them and their child tasks to the selected contract line.</span></span> <span data-ttu-id="6b1aa-127">完成以下步骤，从 **项目** 页将任务与合同子项关联。</span><span class="sxs-lookup"><span data-stu-id="6b1aa-127">Complete the following steps to associate tasks to the contract line from the **Project** page.</span></span>

1. <span data-ttu-id="6b1aa-128">在基于项目的合同子项的 **常规** 选项卡上，验证 **项目** 字段是否填充。</span><span class="sxs-lookup"><span data-stu-id="6b1aa-128">On the **General** tab of a project-based contract line, verify that the **Project** field is filled out.</span></span>
2. <span data-ttu-id="6b1aa-129">在 **包含的任务** 字段中，选择 **仅所选任务**。</span><span class="sxs-lookup"><span data-stu-id="6b1aa-129">On the **Included Tasks** field, select **Selected Tasks Only**.</span></span>
3. <span data-ttu-id="6b1aa-130">保存基于项目的合同子项。</span><span class="sxs-lookup"><span data-stu-id="6b1aa-130">Save the project-based contract line.</span></span> <span data-ttu-id="6b1aa-131">窗体将刷新，**应计费任务** 选项卡将显示。</span><span class="sxs-lookup"><span data-stu-id="6b1aa-131">The form will refresh and the **Chargeable Tasks** tab will be visible.</span></span> <span data-ttu-id="6b1aa-132">这只是进行验证。</span><span class="sxs-lookup"><span data-stu-id="6b1aa-132">This is just for verification purposes only.</span></span>
4. <span data-ttu-id="6b1aa-133">在基于项目的合同子项的 **常规** 选项卡上，在 **项目** 字段中，选择项目链接。</span><span class="sxs-lookup"><span data-stu-id="6b1aa-133">On the **General** tab of the project-based contract line, in the **Project** field, select the project link.</span></span>
5. <span data-ttu-id="6b1aa-134">在 **项目** 页上，选择 **任务计费设置** 选项卡。</span><span class="sxs-lookup"><span data-stu-id="6b1aa-134">On the **Project** page, select the **Task Billing Setup** tab.</span></span>
6. <span data-ttu-id="6b1aa-135">有两个网格。</span><span class="sxs-lookup"><span data-stu-id="6b1aa-135">There are two grids.</span></span> <span data-ttu-id="6b1aa-136">一个网格用于应用于整个项目的合同子项。</span><span class="sxs-lookup"><span data-stu-id="6b1aa-136">One grid is for contract lines that apply to the whole project.</span></span> <span data-ttu-id="6b1aa-137">另一个网格用于特定于任务的计费设置。</span><span class="sxs-lookup"><span data-stu-id="6b1aa-137">The second grid applies to task-specific billing setup.</span></span> <span data-ttu-id="6b1aa-138">在第二个网格中，选择一个或多个任务，然后选择 **关联合同子项**。</span><span class="sxs-lookup"><span data-stu-id="6b1aa-138">In the second grid, select one or more tasks, and then select **Associate Contract Lines**.</span></span>
7. <span data-ttu-id="6b1aa-139">在打开的对话页面中，从下拉列表中选择合同子项。</span><span class="sxs-lookup"><span data-stu-id="6b1aa-139">In the dialog page that opens, select a contract line from the drop-down.</span></span>
8. <span data-ttu-id="6b1aa-140">使用 **计费类型** 下拉列表将任务标记为应计费或非应计费。</span><span class="sxs-lookup"><span data-stu-id="6b1aa-140">Use the **Billing Type** drop-down to mark the tasks as chargeable or non-chargeable.</span></span>
9. <span data-ttu-id="6b1aa-141">选中复选框以指示关联是否还应包括所选任务的子任务。</span><span class="sxs-lookup"><span data-stu-id="6b1aa-141">Select the check box to indicate if the association should also include child tasks of the selected tasks.</span></span> <span data-ttu-id="6b1aa-142">选中复选框还会将所选任务的子任务关联到合同子项。</span><span class="sxs-lookup"><span data-stu-id="6b1aa-142">Checking the box will also associate the child tasks of the selected tasks to the contract line.</span></span>
10. <span data-ttu-id="6b1aa-143">选择 **确定** 以关闭对话框。</span><span class="sxs-lookup"><span data-stu-id="6b1aa-143">Select **OK** to close the dialog.</span></span>

## <a name="unassociate-tasks-from-project-based-contract-lines"></a><span data-ttu-id="6b1aa-144">取消任务与基于项目的合同子项的关联</span><span class="sxs-lookup"><span data-stu-id="6b1aa-144">Unassociate tasks from project-based contract lines</span></span>

### <a name="from-the-contract-line-page"></a><span data-ttu-id="6b1aa-145">从“合同子项”页</span><span class="sxs-lookup"><span data-stu-id="6b1aa-145">From the contract line page</span></span>

<span data-ttu-id="6b1aa-146">完成以下步骤，在 **合同子项** 页的 **应计费任务** 选项卡上，取消项目任务与合同子项的关联。</span><span class="sxs-lookup"><span data-stu-id="6b1aa-146">Complete the following steps to unassociate project tasks from the contract line on the **Chargeable Tasks** tab of the **Contract Line** page.</span></span>

1. <span data-ttu-id="6b1aa-147">在 **应计费任务** 选项卡上，选择 **删除合同子项任务**。</span><span class="sxs-lookup"><span data-stu-id="6b1aa-147">On the **Chargeable Tasks** tab, select **Delete a Contract Line Task**.</span></span>
2. <span data-ttu-id="6b1aa-148">将出现一条警告消息，指示删除此关联可能导致冲销任务中以前记录的所有实际值。</span><span class="sxs-lookup"><span data-stu-id="6b1aa-148">A warning message indicates that removing this association could result in reversal of any actuals previously recorded on the task.</span></span> <span data-ttu-id="6b1aa-149">选择对话中的 **确定** 以删除任务与基于项目的合同子项之间的关联。</span><span class="sxs-lookup"><span data-stu-id="6b1aa-149">Select **OK** on the dialog to remove the association between the task and the project-based contract line.</span></span> 

> [!NOTE]
> <span data-ttu-id="6b1aa-150">这不会从项目中删除任务。</span><span class="sxs-lookup"><span data-stu-id="6b1aa-150">This doesn't delete the task from the project.</span></span> <span data-ttu-id="6b1aa-151">而是将任务关联从基于项目的合同子项中删除。</span><span class="sxs-lookup"><span data-stu-id="6b1aa-151">Instead, it removes the task association from the project-based contract line.</span></span>

### <a name="from-the-project-page"></a><span data-ttu-id="6b1aa-152">从“项目”页</span><span class="sxs-lookup"><span data-stu-id="6b1aa-152">From the project page</span></span>

<span data-ttu-id="6b1aa-153">这不是取消任务与合同子项的关联的更优的体验。</span><span class="sxs-lookup"><span data-stu-id="6b1aa-153">This is the more optimal experience for unassociating tasks from contract lines.</span></span> <span data-ttu-id="6b1aa-154">您可以选择多个任务，然后取消所有任务及其子任务与所选合同子项的关联。</span><span class="sxs-lookup"><span data-stu-id="6b1aa-154">You can select multiple tasks and unassociate all of the them and their child tasks from the selected contract line.</span></span> <span data-ttu-id="6b1aa-155">完成以下步骤，取消任务与合同子项的关联。</span><span class="sxs-lookup"><span data-stu-id="6b1aa-155">Complete the following steps to unassociate tasks from the contract line.</span></span>

1. <span data-ttu-id="6b1aa-156">从基于项目的合同子项的 **常规** 选项卡，在 **项目** 字段中，单击项目的链接。</span><span class="sxs-lookup"><span data-stu-id="6b1aa-156">From **General** tab of the project-based contract line, in the **Project** field, click on the link for project.</span></span>
2. <span data-ttu-id="6b1aa-157">在 **项目** 页上，选择 **任务计费设置** 选项卡。</span><span class="sxs-lookup"><span data-stu-id="6b1aa-157">On the **Project** page, select the **Task Billing Setup** tab.</span></span>
3. <span data-ttu-id="6b1aa-158">页面上有两个网格。</span><span class="sxs-lookup"><span data-stu-id="6b1aa-158">There are two grids on the page.</span></span> <span data-ttu-id="6b1aa-159">一个网格用于应用于整个项目的合同子项，另一个用于特定于任务的计费设置。</span><span class="sxs-lookup"><span data-stu-id="6b1aa-159">One grid is for contract lines that apply to the whole project and the second applies to task-specific billing setup.</span></span> <span data-ttu-id="6b1aa-160">在第二个网格中，选择一个或多个任务，然后选择 **取消关联合同子项**。</span><span class="sxs-lookup"><span data-stu-id="6b1aa-160">In the second grid, select one or more tasks and the select **Disassociate Contract Lines**.</span></span>
4. <span data-ttu-id="6b1aa-161">在打开的对话页面中，从下拉列表中选择合同子项。</span><span class="sxs-lookup"><span data-stu-id="6b1aa-161">In the  dialog page that opens, select a contract line from the drop-down.</span></span>
5. <span data-ttu-id="6b1aa-162">选中复选框以指示是否还应删除所选任务的所有子任务的关联。</span><span class="sxs-lookup"><span data-stu-id="6b1aa-162">Select the check box to indicate if the association should also be removed from any child tasks of the selected tasks.</span></span> <span data-ttu-id="6b1aa-163">选中复选框还会取消所选任务的子任务与合同子项的关联。</span><span class="sxs-lookup"><span data-stu-id="6b1aa-163">Checking the box will also unassociate the child tasks of the selected tasks from the contract line.</span></span>
6. <span data-ttu-id="6b1aa-164">选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="6b1aa-164">Select **OK**.</span></span> <span data-ttu-id="6b1aa-165">将出现一条警告消息，指示删除此关联可能导致冲销任务中以前记录的所有实际值。</span><span class="sxs-lookup"><span data-stu-id="6b1aa-165">A warning message indicates that removing this association could result in reversal of any actuals recorded on the task previously.</span></span> <span data-ttu-id="6b1aa-166">选择警告对话中的 **确定** 以删除任务与基于项目的合同子项之间的关联。</span><span class="sxs-lookup"><span data-stu-id="6b1aa-166">Select **OK** on the warning dialog to remove the association between the task and the project-based contract line.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]