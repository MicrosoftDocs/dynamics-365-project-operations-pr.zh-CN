---
title: 将项目和任务映射到基于项目的报价单明细
description: 此主题提供有关如何将项目和任务映射到基于项目的任务明细的信息。
author: rumant
manager: Annbe
ms.date: 10/05/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: d714304f408050babae1a6ba74268979e0b6ea4b
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/15/2021
ms.locfileid: "5272737"
---
# <a name="map-projects-and-tasks-to-a-project-based-quote-line"></a><span data-ttu-id="6d31c-103">将项目和任务映射到基于项目的报价单明细</span><span class="sxs-lookup"><span data-stu-id="6d31c-103">Map projects and tasks to a project-based quote line</span></span>

<span data-ttu-id="6d31c-104">_**适用于：** 基于资源/非库存场景的 Project Operations，精简部署 - 估价开票交易_</span><span class="sxs-lookup"><span data-stu-id="6d31c-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="6d31c-105">在基于项目的报价单明细上，可以映射已经与报价单明细关联的项目的特定任务。</span><span class="sxs-lookup"><span data-stu-id="6d31c-105">On project-based quote lines, you can map the specific tasks of a project that is already associated to a quote line.</span></span>

<span data-ttu-id="6d31c-106">当您将任务映射到报价单明细时，您在报价单明细上定义的以下项目将仅应用于这些任务：</span><span class="sxs-lookup"><span data-stu-id="6d31c-106">When you map tasks to a quote line, the following items you defined on the quote line will only apply to those tasks:</span></span>

- <span data-ttu-id="6d31c-107">计费方法</span><span class="sxs-lookup"><span data-stu-id="6d31c-107">Billing method</span></span>
- <span data-ttu-id="6d31c-108">应计费选项</span><span class="sxs-lookup"><span data-stu-id="6d31c-108">Chargeability options</span></span>
- <span data-ttu-id="6d31c-109">上限</span><span class="sxs-lookup"><span data-stu-id="6d31c-109">Not-to-exceed limits</span></span>
- <span data-ttu-id="6d31c-110">客户</span><span class="sxs-lookup"><span data-stu-id="6d31c-110">Customers</span></span>

<span data-ttu-id="6d31c-111">例如，您可能有一个项目，其中一个阶段是固定价格，所有其他阶段是时间和材料。</span><span class="sxs-lookup"><span data-stu-id="6d31c-111">For example, you might have a project where one phase is fixed price and all the other phases are time and materials.</span></span> <span data-ttu-id="6d31c-112">在这种情况下，您可以使用固定价格计费方法将第一阶段及其所有子任务与该阶段的报价单明细相关联。</span><span class="sxs-lookup"><span data-stu-id="6d31c-112">In this case, you can associate the first phase, and all of its child tasks, to the quote line for that phase with a fixed price billing method.</span></span> <span data-ttu-id="6d31c-113">然后，您可以将所有其他阶段与基于时间和材料的报价单明细关联起来。</span><span class="sxs-lookup"><span data-stu-id="6d31c-113">You can then associate all the other phases to the time and materials-based quote line.</span></span>

## <a name="associate-tasks-to-project-based-quote-lines"></a><span data-ttu-id="6d31c-114">将任务与基于项目的报价单明细相关联</span><span class="sxs-lookup"><span data-stu-id="6d31c-114">Associate tasks to project-based quote lines</span></span>

<span data-ttu-id="6d31c-115">您可以从以下位置将任务与报价单明细相关联：</span><span class="sxs-lookup"><span data-stu-id="6d31c-115">You can associate tasks with quote lines from the following locations:</span></span>

- <span data-ttu-id="6d31c-116">**项目** 页 > **任务记帐** 选项卡（最佳）</span><span class="sxs-lookup"><span data-stu-id="6d31c-116">**Project** page > **Task billing** tab (optimal)</span></span>
- <span data-ttu-id="6d31c-117">**报价单明细** 页 > **应计费任务** 选项卡</span><span class="sxs-lookup"><span data-stu-id="6d31c-117">**Quote Line** page > **Chargeable tasks** tab</span></span> 

### <a name="from-the-project-page"></a><span data-ttu-id="6d31c-118">从“项目”页</span><span class="sxs-lookup"><span data-stu-id="6d31c-118">From the Project page</span></span>

<span data-ttu-id="6d31c-119">**项目** 页提供将任务与报价单明细关联的最佳体验。</span><span class="sxs-lookup"><span data-stu-id="6d31c-119">The **Project** page provides the optimal experience for associating tasks to quote lines.</span></span> <span data-ttu-id="6d31c-120">您可以使用此页面选择多个任务，然后将所有任务及其子任务关联到选定的报价单明细。</span><span class="sxs-lookup"><span data-stu-id="6d31c-120">You can use this page to select multiple tasks and associate all of them, plus their child tasks, to the selected quote line.</span></span>

1. <span data-ttu-id="6d31c-121">在基于项目的报价单明细的 **常规** 选项卡上，确认 **项目** 字段已填写。</span><span class="sxs-lookup"><span data-stu-id="6d31c-121">On the **General** tab of a project–based quote line, verify the **Project** field is filled out.</span></span>
2. <span data-ttu-id="6d31c-122">在 **包含的任务** 字段中，选择 **仅所选任务**。</span><span class="sxs-lookup"><span data-stu-id="6d31c-122">In the **Included tasks** field, select **Selected tasks only**.</span></span>
3. <span data-ttu-id="6d31c-123">保存基于项目的报价单明细。</span><span class="sxs-lookup"><span data-stu-id="6d31c-123">Save the project-based quote line.</span></span> <span data-ttu-id="6d31c-124">当窗体刷新时，**应计费任务** 选项卡将显示。</span><span class="sxs-lookup"><span data-stu-id="6d31c-124">When the form refreshes, the **Chargeable tasks** tab displays.</span></span>
4. <span data-ttu-id="6d31c-125">在 **常规** 选项卡上，从 **项目** 字段中选择项目的链接。</span><span class="sxs-lookup"><span data-stu-id="6d31c-125">On the **General** tab, select the link for the project from the **Project** field.</span></span>
5. <span data-ttu-id="6d31c-126">在 **项目** 页上，选择 **任务记帐** 选项卡。</span><span class="sxs-lookup"><span data-stu-id="6d31c-126">On the **Project** page, select the **Task billing** tab.</span></span>
6. <span data-ttu-id="6d31c-127">在第二个网格（适用于特定于任务的计费设置）中，选择一个或多个任务，然后选择 **关联报价单明细**。</span><span class="sxs-lookup"><span data-stu-id="6d31c-127">In the second grid, which applies to task-specific billing setup, select one or more tasks and then select **Associate quote lines**.</span></span>
7. <span data-ttu-id="6d31c-128">在出现的对话页面中，选择一个在报价单上显示基于项目的报价单明细的报价单明细。</span><span class="sxs-lookup"><span data-stu-id="6d31c-128">In the dialog page that appears, select a quote line that displays project-based quote lines on the quote.</span></span>
8. <span data-ttu-id="6d31c-129">在 **计费类型** 字段中，指明这些任务是应计费还是非应计费。</span><span class="sxs-lookup"><span data-stu-id="6d31c-129">In the **Billing type** field, indicate if these tasks are chargeable or non-chargeable.</span></span>
9. <span data-ttu-id="6d31c-130">选中复选框以指示关联是否应包括所选任务的子任务。</span><span class="sxs-lookup"><span data-stu-id="6d31c-130">Select the check box to indicate if the association should include child tasks of the selected tasks.</span></span> <span data-ttu-id="6d31c-131">选中复选框会将所选任务的子任务与报价单明细相关联。</span><span class="sxs-lookup"><span data-stu-id="6d31c-131">Checking the box will associate the child tasks of the selected tasks to the quote line.</span></span>
10. <span data-ttu-id="6d31c-132">选择 **确定** 以关闭对话框。</span><span class="sxs-lookup"><span data-stu-id="6d31c-132">Select **OK** to close the dialog.</span></span>

### <a name="from-the-quote-line-page"></a><span data-ttu-id="6d31c-133">从“报价单明细”页</span><span class="sxs-lookup"><span data-stu-id="6d31c-133">From the Quote line page</span></span>

<span data-ttu-id="6d31c-134">您可以从 **报价单明细** 页的 **应计费任务** 选项卡将项目任务与报价单明细相关联。</span><span class="sxs-lookup"><span data-stu-id="6d31c-134">You can associate project tasks to quote lines from the **Chargeable tasks** tab on **Quote line** page.</span></span>

>[!NOTE]
><span data-ttu-id="6d31c-135">将项目任务与报价单明细相关联的最佳位置是在 **项目** 页的 **任务记帐** 选项卡上。</span><span class="sxs-lookup"><span data-stu-id="6d31c-135">The optimal place to associate project tasks to quote lines is on the **Task billing** tab on the **Project** page.</span></span> <span data-ttu-id="6d31c-136">如果您从 **报价单明细** 页的 **应计费任务** 选项卡关联任务，则必须手动关联每个项目。</span><span class="sxs-lookup"><span data-stu-id="6d31c-136">If you associate tasks from the **Chargeable tasks** tab on **Quote line** page, you must manually associate each project.</span></span>

1. <span data-ttu-id="6d31c-137">在基于项目的报价单明细的 **常规** 选项卡上，确认在 **项目** 字段中选择了一个项目。</span><span class="sxs-lookup"><span data-stu-id="6d31c-137">On the **General** tab of a project–based quote line, verify that there is a project selected in the **Project** field.</span></span>
2. <span data-ttu-id="6d31c-138">在 **包含的任务** 字段中，选择 **仅所选任务**。</span><span class="sxs-lookup"><span data-stu-id="6d31c-138">In the **Included tasks** field, select **Selected tasks only**.</span></span>
3. <span data-ttu-id="6d31c-139">保存基于项目的报价单明细。</span><span class="sxs-lookup"><span data-stu-id="6d31c-139">Save the project-based quote line.</span></span> <span data-ttu-id="6d31c-140">当窗体刷新时，**应计费任务** 选项卡将显示。</span><span class="sxs-lookup"><span data-stu-id="6d31c-140">When the form refreshes, the **Chargeable tasks** tab displays.</span></span>
4. <span data-ttu-id="6d31c-141">在 **应计费任务** 选项卡上，选择 **添加报价单明细任务**。</span><span class="sxs-lookup"><span data-stu-id="6d31c-141">On the **Chargeable tasks** tab, select **Add a quote line task**.</span></span>
5. <span data-ttu-id="6d31c-142">在 **报价单明细任务** 页上的 **任务** 字段中，选择任务，然后在 **计费类型** 字段中选择 **保存**。</span><span class="sxs-lookup"><span data-stu-id="6d31c-142">On the **Quote line task** page, in the **Tasks** field, select the task and in the **Billing type** field, select **Save**.</span></span> 
6. <span data-ttu-id="6d31c-143">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="6d31c-143">Close the page.</span></span> <span data-ttu-id="6d31c-144">所选任务现已与报价单明细关联。</span><span class="sxs-lookup"><span data-stu-id="6d31c-144">The selected task is now associated to the quote line.</span></span>

## <a name="disassociate-tasks-from-projectbased-quote-lines"></a><span data-ttu-id="6d31c-145">取消任务与基于项目的报价单明细的关联</span><span class="sxs-lookup"><span data-stu-id="6d31c-145">Disassociate tasks from project–based quote lines</span></span>

### <a name="from-the-project-page"></a><span data-ttu-id="6d31c-146">从“项目”页</span><span class="sxs-lookup"><span data-stu-id="6d31c-146">From the Project page</span></span>

<span data-ttu-id="6d31c-147">此方法提供取消任务与报价单明细的关联的最佳体验。</span><span class="sxs-lookup"><span data-stu-id="6d31c-147">This method provides the most optimal experience for disassociating tasks from quote lines.</span></span> <span data-ttu-id="6d31c-148">您可以选择多个任务，然后取消所有任务及其子任务与选定的报价单明细的关联。</span><span class="sxs-lookup"><span data-stu-id="6d31c-148">You can select multiple tasks and disassociate all of the them, plus their child tasks, from the selected quote line.</span></span>

1. <span data-ttu-id="6d31c-149">在基于项目的报价单明细的 **常规** 选项卡上，在 **项目** 字段中，选择项目链接。</span><span class="sxs-lookup"><span data-stu-id="6d31c-149">On the **General** tab of a project–based quote line, in the **Project** field, select the project link.</span></span>
2. <span data-ttu-id="6d31c-150">在 **项目** 页上，选择 **任务记帐** 选项卡。</span><span class="sxs-lookup"><span data-stu-id="6d31c-150">On the **Project** page, select the **Task billing** tab.</span></span>
3. <span data-ttu-id="6d31c-151">在第二个网格（适用于特定于任务的计费设置）中，选择一个或多个任务，然后选择 **取消关联报价单明细**。</span><span class="sxs-lookup"><span data-stu-id="6d31c-151">In the second grid, which applies to task-specific billing setup, select one or more tasks, and then select **Disassociate quote lines**.</span></span>
4. <span data-ttu-id="6d31c-152">在显示的对话页面中，选择报价单明细。</span><span class="sxs-lookup"><span data-stu-id="6d31c-152">In the dialog page that appears, select a quote line.</span></span>
5. <span data-ttu-id="6d31c-153">选中复选框以指示是否还应从所选任务的子任务中删除此关联。</span><span class="sxs-lookup"><span data-stu-id="6d31c-153">Select the check box to indicate whether the association should also be removed from child tasks of the selected tasks.</span></span> <span data-ttu-id="6d31c-154">选中复选框还将取消所选任务的子任务与报价单明细的关联。</span><span class="sxs-lookup"><span data-stu-id="6d31c-154">Checking the box will also disassociate the child tasks of the selected tasks to the quote line.</span></span>
6. <span data-ttu-id="6d31c-155">选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="6d31c-155">Select **OK**.</span></span> <span data-ttu-id="6d31c-156">警告消息将通知您，如果删除此关联，以前记录在任务中的所有实际值都可能取消。</span><span class="sxs-lookup"><span data-stu-id="6d31c-156">A warning message informs you that if you remove this association, any actuals previously recorded on the task could be reversed.</span></span> 
7. <span data-ttu-id="6d31c-157">选择 **确定** 继续删除任务与基于项目的报价单明细之间的关联。</span><span class="sxs-lookup"><span data-stu-id="6d31c-157">Select **OK** to continue and remove the association between the task and the project-based quote line.</span></span>

### <a name="from-the-quote-line-page"></a><span data-ttu-id="6d31c-158">从“报价单明细”页</span><span class="sxs-lookup"><span data-stu-id="6d31c-158">From the Quote line page</span></span>

<span data-ttu-id="6d31c-159">您还可以从 **报价单明细** 页的 **应计费任务** 选项卡取消项目任务与报价单明细的关联。</span><span class="sxs-lookup"><span data-stu-id="6d31c-159">You can also disassociate project tasks to quote lines from the **Chargeable tasks** tab on **Quote line** page.</span></span>

1. <span data-ttu-id="6d31c-160">在 **应计费任务** 选项卡上，选择 **删除报价单明细任务**。</span><span class="sxs-lookup"><span data-stu-id="6d31c-160">On the **Chargeable tasks** tab, select **Delete a quote line task**.</span></span>
2. <span data-ttu-id="6d31c-161">选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="6d31c-161">Select **OK**.</span></span> <span data-ttu-id="6d31c-162">警告消息将通知您，如果删除此关联，以前记录在任务中的所有实际值都可能取消。</span><span class="sxs-lookup"><span data-stu-id="6d31c-162">A warning message informs you that if you remove this association, any actuals previously recorded on the task could be reversed.</span></span> 
3. <span data-ttu-id="6d31c-163">选择 **确定** 继续删除任务与基于项目的报价单明细之间的关联。</span><span class="sxs-lookup"><span data-stu-id="6d31c-163">Select **OK** to continue and remove the association between the task and the project-based quote line.</span></span>

>[!NOTE]
> <span data-ttu-id="6d31c-164">此过程不会从项目中删除任务。</span><span class="sxs-lookup"><span data-stu-id="6d31c-164">This procedure doesn't delete the task from the project.</span></span> <span data-ttu-id="6d31c-165">只是从基于项目的报价单明细中删除任务关联。</span><span class="sxs-lookup"><span data-stu-id="6d31c-165">It only removes the task association from the project-based quote line.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]