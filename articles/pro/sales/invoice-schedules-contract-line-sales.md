---
title: 根据基于项目的合同子项创建发票计划 - 精简
description: 此主题提供有关创建发票计划和里程碑的信息。
author: rumant
manager: Annbe
ms.date: 10/26/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 4706a2a711efa7d176030deaa33b65bca28d8498
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/15/2021
ms.locfileid: "5273367"
---
# <a name="create-invoice-schedules-on-a-project-based-contract-line---lite"></a><span data-ttu-id="09194-103">根据基于项目的合同子项创建发票计划 - 精简</span><span class="sxs-lookup"><span data-stu-id="09194-103">Create invoice schedules on a project-based contract line - lite</span></span>

<span data-ttu-id="09194-104">_**适用于：** 精简部署 - 估价交易开票_</span><span class="sxs-lookup"><span data-stu-id="09194-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="09194-105">您可以在基于项目的合同子项中附加发票计划。</span><span class="sxs-lookup"><span data-stu-id="09194-105">You can attach an invoice schedule on a project-based contract line.</span></span> <span data-ttu-id="09194-106">仅在合同赢单，可以创建项目合同后才允许开票。</span><span class="sxs-lookup"><span data-stu-id="09194-106">Invoicing is only allowed after the contract is won to create a Project contract.</span></span> <span data-ttu-id="09194-107">通过发票计划，可以自动创建基于项目的合同子项的草稿发票。</span><span class="sxs-lookup"><span data-stu-id="09194-107">Invoice schedules allow draft invoices for a project-based contract line to be created automatically.</span></span> <span data-ttu-id="09194-108">如果您计划始终手动创建发票，可以跳过在基于项目的合同子项或合同子项上创建发票计划。</span><span class="sxs-lookup"><span data-stu-id="09194-108">If you plan to always create invoices manually, you can skip creating invoice schedules on a project-based contract line or a contract line.</span></span>

## <a name="create-a-time-and-material-invoice-schedule-for-a-project-based-contract-line"></a><span data-ttu-id="09194-109">为基于项目的合同子项创建时间和材料发票计划</span><span class="sxs-lookup"><span data-stu-id="09194-109">Create a time and material invoice schedule for a project-based contract line</span></span>

<span data-ttu-id="09194-110">当基于项目的合同子项使用时间和材料计费方法时，您可以创建基于日期的发票计划。</span><span class="sxs-lookup"><span data-stu-id="09194-110">When a project-based contract line has a time and material billing method, you can create a date-based invoice schedule.</span></span> <span data-ttu-id="09194-111">若要自动生成基于日期的发票计划，请完成以下步骤。</span><span class="sxs-lookup"><span data-stu-id="09194-111">To automatically generate a date-based invoice schedule, complete the following steps.</span></span>

1. <span data-ttu-id="09194-112">转到 **设置** > **发票频率** 设置发票频率。</span><span class="sxs-lookup"><span data-stu-id="09194-112">Go to **Settings** > **Invoice Frequencies** to set up invoice frequency.</span></span>
2. <span data-ttu-id="09194-113">打开项目合同，在 **摘要** 选项卡上设置要求交货日期。</span><span class="sxs-lookup"><span data-stu-id="09194-113">Open the project contract and on the **Summary** tab, set the requested delivery date.</span></span>
3. <span data-ttu-id="09194-114">打开要为其创建基于日期的发票计划的时间和材料合同子项。</span><span class="sxs-lookup"><span data-stu-id="09194-114">Open the time and material contract line that you want to create a date-based invoice schedule for.</span></span> 
4. <span data-ttu-id="09194-115">在 **发票计划** 选项卡上，选择计费开始日期和发票频率。</span><span class="sxs-lookup"><span data-stu-id="09194-115">On the **Invoice Schedule** tab, select a billing start date and the invoice frequency.</span></span> 
5. <span data-ttu-id="09194-116">在子网格上，选择 **生成发票计划**。</span><span class="sxs-lookup"><span data-stu-id="09194-116">On the subgrid, select **Generate Invoice Schedule**.</span></span>

    <span data-ttu-id="09194-117">系统将使用以下字段信息生成发票计划：</span><span class="sxs-lookup"><span data-stu-id="09194-117">The system generates the invoice schedule with the following field information:</span></span>

    - <span data-ttu-id="09194-118">**发票运行日期** 设置为基于发票频率的日期。</span><span class="sxs-lookup"><span data-stu-id="09194-118">**Invoice Run Date** is set to the date based on the invoice frequency.</span></span>
    - <span data-ttu-id="09194-119">**交易截止日期** 设置为 **发票运行日期** 之前的一天。</span><span class="sxs-lookup"><span data-stu-id="09194-119">**Transaction Cut-off Date** is set to the day before the **Invoice Run Date**.</span></span>
    - <span data-ttu-id="09194-120">**运行状态** 自动设置为 **未运行**。</span><span class="sxs-lookup"><span data-stu-id="09194-120">**Run Status** is automatically set to **Not Run**.</span></span> <span data-ttu-id="09194-121">当自动发票创建作业在某个 **发票运行日期** 运行时，此字段将更新为 **运行成功** 或 **运行失败**。</span><span class="sxs-lookup"><span data-stu-id="09194-121">When the automatic invoice creation job runs for a certain **Invoice Run Date**, this field is updated to **Run Successful** or **Run Failed**.</span></span>

## <a name="create-a-fixed-price-invoice-schedule-for-a-project-based-contract-line"></a><span data-ttu-id="09194-122">为基于项目的合同子项创建固定价格发票计划</span><span class="sxs-lookup"><span data-stu-id="09194-122">Create a fixed price invoice schedule for a project-based contract line</span></span>

<span data-ttu-id="09194-123">当基于项目的合同子项具有固定价格计费方法时，您可以创建基于里程碑的发票计划。</span><span class="sxs-lookup"><span data-stu-id="09194-123">When a project-based contract line has a fixed price billing method, you can create a milestone-based invoice schedule.</span></span> <span data-ttu-id="09194-124">完成以下步骤，为在日历期间内平均分配的一组固定里程碑自动生成基于里程碑的发票计划。</span><span class="sxs-lookup"><span data-stu-id="09194-124">Complete the following steps to automatically generate a milestone-based invoice schedule for a fixed set of milestones that distribute equally for the calendar period.</span></span>

1. <span data-ttu-id="09194-125">转到 **设置** > **发票频率** 设置发票频率。</span><span class="sxs-lookup"><span data-stu-id="09194-125">Go to **Settings** > **Invoice Frequencies** to set up invoice frequency.</span></span>
2. <span data-ttu-id="09194-126">打开项目合同，在 **摘要** 选项卡上设置要求交货日期。</span><span class="sxs-lookup"><span data-stu-id="09194-126">Open the project contract and on the **Summary** tab, set the requested delivery date.</span></span>
3. <span data-ttu-id="09194-127">打开需要创建里程碑计划的固定价格合同子项。</span><span class="sxs-lookup"><span data-stu-id="09194-127">Open the fixed price contract line on which you need to create a milestone schedule.</span></span> 
4. <span data-ttu-id="09194-128">在 **发票计划(计费里程碑)** 选项卡上，选择计费开始日期和发票频率。</span><span class="sxs-lookup"><span data-stu-id="09194-128">On the **Invoice Schedule (Billing Milestones)** tab, select the billing start date and the invoice frequency.</span></span> 
5. <span data-ttu-id="09194-129">在子网格上，选择 **生成定期里程碑**。</span><span class="sxs-lookup"><span data-stu-id="09194-129">On the subgrid, select **Generate Periodic Milestones**.</span></span>

    <span data-ttu-id="09194-130">系统将使用以下里程碑信息生成发票计划。</span><span class="sxs-lookup"><span data-stu-id="09194-130">The system generates the invoice schedule with the following milestone information.</span></span>

    - <span data-ttu-id="09194-131">**里程碑名称** 设置为根据发票频率指示的日期。</span><span class="sxs-lookup"><span data-stu-id="09194-131">**Milestone Name** is set to the date that is dictated based on the invoice frequency.</span></span>
    - <span data-ttu-id="09194-132">**里程碑日期** 设置为根据发票频率指示的日期。</span><span class="sxs-lookup"><span data-stu-id="09194-132">**Milestone Date** is set to the date that is dictated based on the invoice frequency.</span></span>
    - <span data-ttu-id="09194-133">**里程碑金额** 计算为将基于项目的合同子项上的合同金额除以频率、计费开始日期和要求交货日期指示的里程碑数。</span><span class="sxs-lookup"><span data-stu-id="09194-133">**Milestone Amount** is calculated by dividing the contract amount on the project-based contract line by the number of milestones as dictated by the frequency, billing start, and requested delivery dates.</span></span>
    - <span data-ttu-id="09194-134">如果合同子项在 **估算税额** 字段中有值，此字段在生成定期里程碑时，也会平均分配到每个里程碑。</span><span class="sxs-lookup"><span data-stu-id="09194-134">If the contract line has a value in the **Estimated Tax Amount** field, this field is also apportioned to each milestone equally when generating periodic milestones.</span></span>

<span data-ttu-id="09194-135">计费里程碑应该等于基于项目的合同子项的合同值。</span><span class="sxs-lookup"><span data-stu-id="09194-135">Billing milestones should equal the contracted value of the project-based contract line.</span></span> <span data-ttu-id="09194-136">如果不相等，将出现错误。</span><span class="sxs-lookup"><span data-stu-id="09194-136">If they aren't equal, an error occurs.</span></span> <span data-ttu-id="09194-137">您可以通过创建、编辑或删除里程碑来验证计费里程碑是否是该明细的合同值的总计来解决错误。</span><span class="sxs-lookup"><span data-stu-id="09194-137">You can fix that error by verifying that the billing milestones total the contracted value of the line by either creating, editing, or deleting milestones.</span></span> <span data-ttu-id="09194-138">进行更改后，刷新页面。</span><span class="sxs-lookup"><span data-stu-id="09194-138">After the changes are made, refresh the page.</span></span>

### <a name="manually-create-milestones"></a><span data-ttu-id="09194-139">手动创建里程碑</span><span class="sxs-lookup"><span data-stu-id="09194-139">Manually create milestones</span></span>

<span data-ttu-id="09194-140">固定价格里程碑在不定期拆分时可以手动生成。</span><span class="sxs-lookup"><span data-stu-id="09194-140">Fixed price milestones can be generated manually when they aren't periodically split.</span></span> <span data-ttu-id="09194-141">要手动创建里程碑，请完成以下步骤。</span><span class="sxs-lookup"><span data-stu-id="09194-141">To create a milestone manually, complete the following steps.</span></span>

1. <span data-ttu-id="09194-142">打开要创建里程碑的固定价格合同子项。</span><span class="sxs-lookup"><span data-stu-id="09194-142">Open the fixed price contract line on which you want to create a milestone.</span></span> 
2. <span data-ttu-id="09194-143">在 **发票计划** 选项卡上的子网格中，选择 **+ 创建新合同子项里程碑**。</span><span class="sxs-lookup"><span data-stu-id="09194-143">On the **Invoice Schedule** tab, on the subgrid, select **+ Create new Contract line milestone**.</span></span>
3. <span data-ttu-id="09194-144">在 **里程碑创建** 窗体上，根据下表输入所需信息。</span><span class="sxs-lookup"><span data-stu-id="09194-144">On the **Milestone Creation** form, enter the required information based on the following table.</span></span> 

| <span data-ttu-id="09194-145">字段</span><span class="sxs-lookup"><span data-stu-id="09194-145">Field</span></span> | <span data-ttu-id="09194-146">地点</span><span class="sxs-lookup"><span data-stu-id="09194-146">Location</span></span> | <span data-ttu-id="09194-147">描述</span><span class="sxs-lookup"><span data-stu-id="09194-147">Description</span></span> | <span data-ttu-id="09194-148">下游影响</span><span class="sxs-lookup"><span data-stu-id="09194-148">Downstream impact</span></span> |
| --- | --- | --- | --- |
| <span data-ttu-id="09194-149">里程碑名称</span><span class="sxs-lookup"><span data-stu-id="09194-149">Milestone Name</span></span> | <span data-ttu-id="09194-150">快速创建</span><span class="sxs-lookup"><span data-stu-id="09194-150">Quick Create</span></span> | <span data-ttu-id="09194-151">里程碑名称的文本字段。</span><span class="sxs-lookup"><span data-stu-id="09194-151">Text field for the name of the milestone.</span></span> | <span data-ttu-id="09194-152">此字段包含在项目合同子项里程碑和发票上。</span><span class="sxs-lookup"><span data-stu-id="09194-152">This field is included on the project contract line milestone and the invoice.</span></span> |
| <span data-ttu-id="09194-153">项目任务</span><span class="sxs-lookup"><span data-stu-id="09194-153">Project Task</span></span> | <span data-ttu-id="09194-154">快速创建</span><span class="sxs-lookup"><span data-stu-id="09194-154">Quick Create</span></span> | <span data-ttu-id="09194-155">如果里程碑与项目任务关联，请使用此引用添加自定义逻辑，并根据任务状态设置里程碑状态。</span><span class="sxs-lookup"><span data-stu-id="09194-155">If the milestone is tied to a project task, use this reference to add custom logic and set the milestone status based on the task status.</span></span> | <span data-ttu-id="09194-156">此引用对任务没有下游影响。</span><span class="sxs-lookup"><span data-stu-id="09194-156">There is no downstream impact of this reference to a task.</span></span> |
| <span data-ttu-id="09194-157">里程碑日期</span><span class="sxs-lookup"><span data-stu-id="09194-157">Milestone Date</span></span> | <span data-ttu-id="09194-158">快速创建</span><span class="sxs-lookup"><span data-stu-id="09194-158">Quick Create</span></span> | <span data-ttu-id="09194-159">自动发票创建流程应查找此里程碑的状态以在开票时将其作为考虑因素的日期。</span><span class="sxs-lookup"><span data-stu-id="09194-159">The date on which the automatic invoice creation process should look for the status of this milestone to consider it for invoicing.</span></span> | <span data-ttu-id="09194-160">此字段包含在项目合同子项里程碑和发票上。</span><span class="sxs-lookup"><span data-stu-id="09194-160">This is included on the project contract line milestone and the invoice.</span></span> |
| <span data-ttu-id="09194-161">账单状态</span><span class="sxs-lookup"><span data-stu-id="09194-161">Invoice Status</span></span> | <span data-ttu-id="09194-162">快速创建</span><span class="sxs-lookup"><span data-stu-id="09194-162">Quick Create</span></span> | <span data-ttu-id="09194-163">创建里程碑时，此状态始终设置为 **未准备好开票** 或 **未开始**。</span><span class="sxs-lookup"><span data-stu-id="09194-163">When the milestone is created, this status is always set to **Not ready for invoicing** or **Not started**.</span></span> | <span data-ttu-id="09194-164">此字段包含在项目合同子项里程碑和发票上。</span><span class="sxs-lookup"><span data-stu-id="09194-164">This is included on the project contract line milestone and the invoice.</span></span> |
| <span data-ttu-id="09194-165">明细金额</span><span class="sxs-lookup"><span data-stu-id="09194-165">Line Amount</span></span> | <span data-ttu-id="09194-166">快速创建</span><span class="sxs-lookup"><span data-stu-id="09194-166">Quick Create</span></span> | <span data-ttu-id="09194-167">将向客户开发票的里程碑的金额或值。</span><span class="sxs-lookup"><span data-stu-id="09194-167">The amount or value of the milestone that will be invoiced to the customer.</span></span> | <span data-ttu-id="09194-168">此字段包含在项目合同子项里程碑和发票上，</span><span class="sxs-lookup"><span data-stu-id="09194-168">This field is included on the project contract line milestone and the invoice,</span></span> |
| <span data-ttu-id="09194-169">税款</span><span class="sxs-lookup"><span data-stu-id="09194-169">Tax</span></span> | <span data-ttu-id="09194-170">快速创建</span><span class="sxs-lookup"><span data-stu-id="09194-170">Quick Create</span></span> | <span data-ttu-id="09194-171">里程碑上应用的税额。</span><span class="sxs-lookup"><span data-stu-id="09194-171">The tax amount applied on the milestone.</span></span> | <span data-ttu-id="09194-172">此字段包含在项目合同子项里程碑和发票上。</span><span class="sxs-lookup"><span data-stu-id="09194-172">This is included on the project contract line milestone and the invoice.</span></span> |

4. <span data-ttu-id="09194-173">选择 **保存并关闭**。</span><span class="sxs-lookup"><span data-stu-id="09194-173">Select **Save and Close**.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]