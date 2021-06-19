---
title: 管理收入估算
description: 本主题提供有关如何使用项目收入估算的信息。
author: sigitac
ms.date: 11/04/2020
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: e3cbaff18d8bd4d6f6a7577bba25b3e843b1757e
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/10/2021
ms.locfileid: "6013836"
---
# <a name="manage-revenue-estimates"></a><span data-ttu-id="ca298-103">管理收入估算</span><span class="sxs-lookup"><span data-stu-id="ca298-103">Manage revenue estimates</span></span>

<span data-ttu-id="ca298-104">_**适用于：** 面向资源/非库存场景的 Project Operations_</span><span class="sxs-lookup"><span data-stu-id="ca298-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="ca298-105">您可以创建、计算、过帐、冲销或消除收入估算。</span><span class="sxs-lookup"><span data-stu-id="ca298-105">You can create, calculate, post, reverse, or eliminate revenue estimates.</span></span> <span data-ttu-id="ca298-106">您可以手动或使用定期流程来执行此操作。</span><span class="sxs-lookup"><span data-stu-id="ca298-106">You can do this either manually or by using a periodic process.</span></span> <span data-ttu-id="ca298-107">本主题提供有关如何使用项目收入估算的信息。</span><span class="sxs-lookup"><span data-stu-id="ca298-107">This topic provides information about how to work with revenue estimates for projects.</span></span>

### <a name="manage-revenue-estimates-manually"></a><span data-ttu-id="ca298-108">手动管理收入估算</span><span class="sxs-lookup"><span data-stu-id="ca298-108">Manage revenue estimates manually</span></span>

<span data-ttu-id="ca298-109">在固定价格收入估算项目或 **估算查询** 页（**项目管理和会计** > **报告和查询** > **估计查询和报告**）上，选择 **估算**。</span><span class="sxs-lookup"><span data-stu-id="ca298-109">On the fixed price revenue estimate project or the **Estimate inquiry** page (**Project management and accounting** > **Reports and inquiries** > **Estimates inquiries and reports**), select **Estimates**.</span></span>

### <a name="manage-revenue-estimates-using-a-periodic-process"></a><span data-ttu-id="ca298-110">使用定期流程管理收入估算</span><span class="sxs-lookup"><span data-stu-id="ca298-110">Manage revenue estimates using a periodic process</span></span>

<span data-ttu-id="ca298-111">转到 **项目管理和会计** > **定期** > **估算**，并选择相应的流程。</span><span class="sxs-lookup"><span data-stu-id="ca298-111">Go to **Project management and accounting** > **Periodic** > **Estimates** and select the corresponding process.</span></span>

## <a name="create-a-revenue-estimate"></a><span data-ttu-id="ca298-112">创建收入估算</span><span class="sxs-lookup"><span data-stu-id="ca298-112">Create a revenue estimate</span></span>

<span data-ttu-id="ca298-113">完成以下步骤以创建收入估算。</span><span class="sxs-lookup"><span data-stu-id="ca298-113">Complete the following steps to create a revenue estimate.</span></span> 

1. <span data-ttu-id="ca298-114">转到 **项目管理和会计** > **定期** > **估算**。</span><span class="sxs-lookup"><span data-stu-id="ca298-114">Go to **Project management and accounting** > **Periodic** > **Estimates**.</span></span>
2. <span data-ttu-id="ca298-115">选择 **新建**。</span><span class="sxs-lookup"><span data-stu-id="ca298-115">Select **New**.</span></span> <span data-ttu-id="ca298-116">在 **估算创建** 页上，选择以下参数：</span><span class="sxs-lookup"><span data-stu-id="ca298-116">On the **Estimate creation** page, select the following parameters:</span></span>

   - <span data-ttu-id="ca298-117">**期间代码**：此代码确定估算的过帐频率。</span><span class="sxs-lookup"><span data-stu-id="ca298-117">**Period code**: This code determines how frequently estimates are posted.</span></span>
   - <span data-ttu-id="ca298-118">**估算日期**：处理估算的日期。</span><span class="sxs-lookup"><span data-stu-id="ca298-118">**Estimate date**: The date the estimate is processed.</span></span>
   - <span data-ttu-id="ca298-119">**连续**：选中此复选框，以仅在上一期间过帐估算后或估算是已创建的第一个估算时才创建估算。</span><span class="sxs-lookup"><span data-stu-id="ca298-119">**Continuous**: Select this check box to create estimates only if estimates were posted in the previous period, or if the estimate is the first estimate that has been created.</span></span> <span data-ttu-id="ca298-120">如果未选中此复选框，即使上一期间未过帐估算，也会创建估算。</span><span class="sxs-lookup"><span data-stu-id="ca298-120">If this is not selected, estimates are created even if estimates were not posted in the previous period.</span></span>
   - <span data-ttu-id="ca298-121">**完成成本计算方法**：定义如何估算剩余的项目工作。</span><span class="sxs-lookup"><span data-stu-id="ca298-121">**Cost to complete method**: Define how to estimate the remaining project work.</span></span> <span data-ttu-id="ca298-122">有关详细信息，请参阅[完成成本计算方法](cost-complete-methods.md)。</span><span class="sxs-lookup"><span data-stu-id="ca298-122">For more information, see [Cost to complete methods](cost-complete-methods.md).</span></span>
   - <span data-ttu-id="ca298-123">**完成方法**：从以下选项中选择完成方法：</span><span class="sxs-lookup"><span data-stu-id="ca298-123">**Completion method**: Select a completion method from the following options:</span></span>
     - <span data-ttu-id="ca298-124">**自动**：完成百分比被自动计算，并基于计算中包含的成本行。</span><span class="sxs-lookup"><span data-stu-id="ca298-124">**Automatic**: The completion percentage is calculated automatically and based on the cost lines included in the calculation.</span></span> <span data-ttu-id="ca298-125">成本模板定义包含的成本行。</span><span class="sxs-lookup"><span data-stu-id="ca298-125">The cost template defines the cost lines that are included.</span></span>
     - <span data-ttu-id="ca298-126">**手动**：完成百分比等于上次估算的完成百分比。</span><span class="sxs-lookup"><span data-stu-id="ca298-126">**Manual**: The completion percentage equals the completion percentage of the last estimate.</span></span> <span data-ttu-id="ca298-127">创建估算后，可以更改 **估算** 页上的 **手动计算**。</span><span class="sxs-lookup"><span data-stu-id="ca298-127">After the estimate is created, you can change the **Manual calculation** on the **Estimates** page.</span></span>
     - <span data-ttu-id="ca298-128">**从成本模板**：自动和手动方法相结合。</span><span class="sxs-lookup"><span data-stu-id="ca298-128">**From cost template**: A combination of the automatic and manual methods.</span></span> <span data-ttu-id="ca298-129">根据成本模板中的默认值，自动或手动设置此选项。</span><span class="sxs-lookup"><span data-stu-id="ca298-129">This option is set automatically or manually, depending on the default value in the cost template.</span></span>
   - <span data-ttu-id="ca298-130">**预测模型**：为估算选择预测模型。</span><span class="sxs-lookup"><span data-stu-id="ca298-130">**Forecast model**: Select a forecast model for the estimate.</span></span>
   - <span data-ttu-id="ca298-131">**打印估算列表**：创建并显示估算列表。</span><span class="sxs-lookup"><span data-stu-id="ca298-131">**Print estimate list**: Create and show an estimate list.</span></span> <span data-ttu-id="ca298-132">该列表包含当前函数的状态。</span><span class="sxs-lookup"><span data-stu-id="ca298-132">The list contains the status of the current function.</span></span> <span data-ttu-id="ca298-133">您可以在报表上打印有关估算的任何警告。</span><span class="sxs-lookup"><span data-stu-id="ca298-133">You can print any warnings about the estimate on the report.</span></span> <span data-ttu-id="ca298-134">以下情况会导致估算列表中出现警告：</span><span class="sxs-lookup"><span data-stu-id="ca298-134">The following conditions cause warnings to appear in the estimate list:</span></span>
     - <span data-ttu-id="ca298-135">完成百分比超过 100%。</span><span class="sxs-lookup"><span data-stu-id="ca298-135">A completion percentage of more than 100 percent.</span></span>
     - <span data-ttu-id="ca298-136">完成百分比小于 0%。</span><span class="sxs-lookup"><span data-stu-id="ca298-136">A completion percentage less than zero percent.</span></span>
     - <span data-ttu-id="ca298-137">**待完成** 列中为负金额。</span><span class="sxs-lookup"><span data-stu-id="ca298-137">A negative amount in the **To complete** column.</span></span>
     - <span data-ttu-id="ca298-138">估算没有对应的合同金额。</span><span class="sxs-lookup"><span data-stu-id="ca298-138">An estimate with no corresponding contract amount.</span></span>
     - <span data-ttu-id="ca298-139">估算没有附加的成本估算。</span><span class="sxs-lookup"><span data-stu-id="ca298-139">An estimate with no attached cost estimate.</span></span>
   - <span data-ttu-id="ca298-140">**显示信息日志**：选择此选项可接收一条消息，此消息包含有关运行作业时处理的估算项目的信息。</span><span class="sxs-lookup"><span data-stu-id="ca298-140">**Show Infolog**: Select this option to receive a message that contains information about the estimate projects that were processed when the job was run.</span></span>


## <a name="post-wip-or-accruals"></a><span data-ttu-id="ca298-141">过帐 WIP 或应计</span><span class="sxs-lookup"><span data-stu-id="ca298-141">Post WIP or accruals</span></span>

<span data-ttu-id="ca298-142">计算估算后，将维持、减少或增加这些估算。</span><span class="sxs-lookup"><span data-stu-id="ca298-142">After the estimates are evaluated, they are maintained, decreased, or increased.</span></span> <span data-ttu-id="ca298-143">然后，您可以在使用 **已完成合同** 评估原则时过帐 WIP；在使用 **已完成百分比** 评估原则时过帐应计值。</span><span class="sxs-lookup"><span data-stu-id="ca298-143">You can then post the WIP when you work with the **Completed contract** assessment principle, or post the accruals when you work with the **Completed percentage** assessment principle.</span></span>
  
<span data-ttu-id="ca298-144">估算期间状态从 **已创建** 更改为 **已过帐**。</span><span class="sxs-lookup"><span data-stu-id="ca298-144">The estimate period status changes from **Created** to **Posted**.</span></span>

## <a name="reverse-wip-or-accruals"></a><span data-ttu-id="ca298-145">冲销 WIP 或应计值</span><span class="sxs-lookup"><span data-stu-id="ca298-145">Reverse WIP or accruals</span></span>

<span data-ttu-id="ca298-146">使用冲销选项贷记已过帐的 WIP 或应计值，然后创建期间估算。</span><span class="sxs-lookup"><span data-stu-id="ca298-146">Use the reverse option to credit already posted WIP or accruals, and then create estimates for the period.</span></span>

> [!NOTE]
> <span data-ttu-id="ca298-147">要冲销其他期间之间的期间，请冲销必要的估算期间，然后重新过帐它们。</span><span class="sxs-lookup"><span data-stu-id="ca298-147">To reverse a period that is in between other periods, reverse the necessary estimate periods and then repost them.</span></span> <span data-ttu-id="ca298-148">由于所有后续期间都取决于上一期间的估算，因此不要跳过任何期间。</span><span class="sxs-lookup"><span data-stu-id="ca298-148">Because all subsequent periods depend on the estimates from the previous period, don't skip any periods.</span></span>

## <a name="eliminate-the-estimate-project-and-finish-the-project"></a><span data-ttu-id="ca298-149">消除估算项目并完成项目</span><span class="sxs-lookup"><span data-stu-id="ca298-149">Eliminate the estimate project and finish the project</span></span>

<span data-ttu-id="ca298-150">估算过程的最后一步是消除估算项目，并在完成百分比达到 100% 时结束固定价格项目。</span><span class="sxs-lookup"><span data-stu-id="ca298-150">The final step in the estimate process is to eliminate the estimate project and end the fixed price project when the percentage of completion reaches 100 percent.</span></span>

<span data-ttu-id="ca298-151">运行消除时将发生以下情况：</span><span class="sxs-lookup"><span data-stu-id="ca298-151">The following occurs when you run the elimination:</span></span>

- <span data-ttu-id="ca298-152">对于具有已完成合同的固定价格项目，WIP 值会从余额帐户中清除并过帐到损益帐户。</span><span class="sxs-lookup"><span data-stu-id="ca298-152">For a fixed price project with a completed contract, the WIP values clear from the balance accounts and post to the profit and loss accounts.</span></span>
- <span data-ttu-id="ca298-153">对于具有已完成百分比的固定价格项目，应计值将从损益帐户中删除。</span><span class="sxs-lookup"><span data-stu-id="ca298-153">For a fixed-price project with a completed percentage, the accruals are removed from the profit and loss accounts.</span></span>

<span data-ttu-id="ca298-154">估算会将状态更改为 **已消除**。</span><span class="sxs-lookup"><span data-stu-id="ca298-154">The estimate changes the status to **Eliminated**.</span></span>

> [!NOTE]
> <span data-ttu-id="ca298-155">在特殊情况下，百分比可以超过 100%。</span><span class="sxs-lookup"><span data-stu-id="ca298-155">In special cases, the percentage can extend beyond 100 percent.</span></span> <span data-ttu-id="ca298-156">发生这种情况时，请使用 **“将完成成本设置为零”方法** 将完成百分比降低到 100%。</span><span class="sxs-lookup"><span data-stu-id="ca298-156">When this happens, reduce the percentage of completion by using the **Set cost to complete to zero method** to reach 100 percent.</span></span>

## <a name="reverse-elimination"></a><span data-ttu-id="ca298-157">冲销消除</span><span class="sxs-lookup"><span data-stu-id="ca298-157">Reverse elimination</span></span>

1. <span data-ttu-id="ca298-158">转到 **项目管理和会计** > **定期** > **估算** > **冲销消除**。</span><span class="sxs-lookup"><span data-stu-id="ca298-158">Go to **Project management and accounting** > **Periodic** > **Estimates** > **Reverse elimination**.</span></span> 
2. <span data-ttu-id="ca298-159">在操作窗格 **流程** 选项卡上的 **维护** 组中，选择 **估算**。</span><span class="sxs-lookup"><span data-stu-id="ca298-159">On the Action Pane, on the **Process** tab, in the **Maintain** group, select **Estimate**.</span></span> 
3. <span data-ttu-id="ca298-160">选择 **冲销消除**。</span><span class="sxs-lookup"><span data-stu-id="ca298-160">Select **Reverse elimination**.</span></span>

<span data-ttu-id="ca298-161">使用此页面可以冲销具有指定估算日期且估算状态为 **已消除** 的所有消除。</span><span class="sxs-lookup"><span data-stu-id="ca298-161">Use this page to reverse all eliminations with a specified estimate date and with an estimate status of **Eliminated**.</span></span> <span data-ttu-id="ca298-162">选择相应的字段后，交易状态将更改。</span><span class="sxs-lookup"><span data-stu-id="ca298-162">The transaction status changes after you select the appropriate fields.</span></span>

<span data-ttu-id="ca298-163">如果项目阶段设置为已完成，这也会自动将项目状态更改为 **正在处理**。</span><span class="sxs-lookup"><span data-stu-id="ca298-163">This also automatically changes the project status to **In process** if the project stage is set to finished.</span></span> <span data-ttu-id="ca298-164">项目期间的估算状态将重新更改为 **已过帐**。</span><span class="sxs-lookup"><span data-stu-id="ca298-164">The estimate status of the project period changes back to **Posted**.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]