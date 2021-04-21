---
title: 设置发票自动创建
description: 本主题提供关于设置和配置形式发票的自动创建的信息。
author: rumant
manager: Annbe
ms.date: 04/05/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 359c5902e0b6a08ab7fc982095062e4d1816db6c
ms.sourcegitcommit: ca0fc078d1a12484eca193fe051b8442c0559db8
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/07/2021
ms.locfileid: "5866806"
---
# <a name="set-up-automatic-invoice-creation"></a><span data-ttu-id="677c3-103">设置发票自动创建</span><span class="sxs-lookup"><span data-stu-id="677c3-103">Set up automatic invoice creation</span></span> 
 
<span data-ttu-id="677c3-104">_**适用于：** 精简部署 - 估价交易开单，基于资源/非库存场景的 Project Operations_</span><span class="sxs-lookup"><span data-stu-id="677c3-104">_**Applies To:** Lite deployment - deal to proforma invoicing, Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="677c3-105">您可以在 Dynamics 365 Project Operations 中配置自动创建发票。</span><span class="sxs-lookup"><span data-stu-id="677c3-105">You can configure automatic invoice creation in Dynamics 365 Project Operations.</span></span> <span data-ttu-id="677c3-106">系统基于每个项目合同和合同子项的发票计划创建草稿估价发票。</span><span class="sxs-lookup"><span data-stu-id="677c3-106">The system creates a draft proforma invoice based on the invoice schedule for each project contract and contract line.</span></span> <span data-ttu-id="677c3-107">发票计划在合同子项级别配置。</span><span class="sxs-lookup"><span data-stu-id="677c3-107">Invoice schedules are configured at the contract line level.</span></span> <span data-ttu-id="677c3-108">合同中的每一行可以有不同的发票计划，也可以在合同的每一行中包含相同的发票计划。</span><span class="sxs-lookup"><span data-stu-id="677c3-108">Each line on a contract can have a distinct invoice schedule, or the same invoice schedule can be included on every line of the contract.</span></span>

<span data-ttu-id="677c3-109">在您创建发票时，系统始终会为每个项目合同创建至少一个发票。</span><span class="sxs-lookup"><span data-stu-id="677c3-109">When you create an invoice, the system always creates at least one invoice per project contract.</span></span> <span data-ttu-id="677c3-110">在某些情况下，可能创建多个发票。</span><span class="sxs-lookup"><span data-stu-id="677c3-110">In some cases, there may be multiple invoices created.</span></span> <span data-ttu-id="677c3-111">例如，如果合同有多个客户，则将创建与该项目合同中具有可计费交易需要开票的客户数量相同的发票数量。</span><span class="sxs-lookup"><span data-stu-id="677c3-111">For example, if the contract has multiple customers, the same number of invoices will be created as the number of customers that have billable transactions to invoice on that project contract.</span></span>

## <a name="understand-how-transactions-are-included-on-an-invoice"></a><span data-ttu-id="677c3-112">了解发票上如何包含交易</span><span class="sxs-lookup"><span data-stu-id="677c3-112">Understand how transactions are included on an invoice</span></span> 

<span data-ttu-id="677c3-113">在某些情况下，每个基于项目的合同子项会指定单独的发票计划。</span><span class="sxs-lookup"><span data-stu-id="677c3-113">Sometimes, each project-based contract line specifies a separate invoice schedule.</span></span> <span data-ttu-id="677c3-114">例如，Adatum 合同的实施服务具有以下合同子项：</span><span class="sxs-lookup"><span data-stu-id="677c3-114">For example, implementation services for the Adatum contract have the following contract lines:</span></span>

- <span data-ttu-id="677c3-115">具有两个手动创建的里程碑的固定价格的原型工作。</span><span class="sxs-lookup"><span data-stu-id="677c3-115">Prototype work that is a fixed price with two manually created milestones.</span></span>
- <span data-ttu-id="677c3-116">将在星期一每两周计费一次的包括时间的实施服务。</span><span class="sxs-lookup"><span data-stu-id="677c3-116">Implementation work that includes Time and will be billed bi-weekly on Mondays.</span></span>
- <span data-ttu-id="677c3-117">产生的需要在每月的第一个星期一按月计费的支出。</span><span class="sxs-lookup"><span data-stu-id="677c3-117">Expenses incurred that need to be billed monthly on the first Monday of each month.</span></span>

<span data-ttu-id="677c3-118">在这两个明细项目中定义的发票计划如下表所示：</span><span class="sxs-lookup"><span data-stu-id="677c3-118">Invoice schedules defined on each of these two line items look like the following table:</span></span>

| <span data-ttu-id="677c3-119">合同子项</span><span class="sxs-lookup"><span data-stu-id="677c3-119">Contract line</span></span> | <span data-ttu-id="677c3-120">发票运行日期</span><span class="sxs-lookup"><span data-stu-id="677c3-120">Invoice run date</span></span> | <span data-ttu-id="677c3-121">交易截止日期</span><span class="sxs-lookup"><span data-stu-id="677c3-121">Transaction cut-off date</span></span> | <span data-ttu-id="677c3-122">里程碑日期</span><span class="sxs-lookup"><span data-stu-id="677c3-122">Milestone date</span></span> | <span data-ttu-id="677c3-123">里程碑金额</span><span class="sxs-lookup"><span data-stu-id="677c3-123">Milestone amount</span></span> |
| --- | --- | --- | --- | --- |
| <span data-ttu-id="677c3-124">原型工作</span><span class="sxs-lookup"><span data-stu-id="677c3-124">Prototype work</span></span> | <span data-ttu-id="677c3-125">10 月 5 日，星期一</span><span class="sxs-lookup"><span data-stu-id="677c3-125">October 5, Monday</span></span> | - | <span data-ttu-id="677c3-126">10 月 5 日，星期一</span><span class="sxs-lookup"><span data-stu-id="677c3-126">October 5, Monday</span></span> | <span data-ttu-id="677c3-127">5000 USD</span><span class="sxs-lookup"><span data-stu-id="677c3-127">5000 USD</span></span> |
| - | <span data-ttu-id="677c3-128">11 月 3 日，星期二</span><span class="sxs-lookup"><span data-stu-id="677c3-128">November 3, Tuesday</span></span> | - | <span data-ttu-id="677c3-129">11 月 3 日，星期二</span><span class="sxs-lookup"><span data-stu-id="677c3-129">November 3, Tuesday</span></span> | <span data-ttu-id="677c3-130">12,000 USD</span><span class="sxs-lookup"><span data-stu-id="677c3-130">12,000 USD</span></span> |
| <span data-ttu-id="677c3-131">实施工作</span><span class="sxs-lookup"><span data-stu-id="677c3-131">Implementation work</span></span> | <span data-ttu-id="677c3-132">10 月 5 日，星期一</span><span class="sxs-lookup"><span data-stu-id="677c3-132">October 5, Monday</span></span> | <span data-ttu-id="677c3-133">10 月 4 日，星期日</span><span class="sxs-lookup"><span data-stu-id="677c3-133">October 4, Sunday</span></span> | - | - |
| - | <span data-ttu-id="677c3-134">10 月 19 日，星期一</span><span class="sxs-lookup"><span data-stu-id="677c3-134">October 19, Monday</span></span> | <span data-ttu-id="677c3-135">10 月 18 日，星期日</span><span class="sxs-lookup"><span data-stu-id="677c3-135">October 18, Sunday</span></span> | - | - |
| - | <span data-ttu-id="677c3-136">11 月 2 日，星期一</span><span class="sxs-lookup"><span data-stu-id="677c3-136">November 2, Monday</span></span> | <span data-ttu-id="677c3-137">11 月 1 日，星期日</span><span class="sxs-lookup"><span data-stu-id="677c3-137">November 1, Sunday</span></span> | - | - |
| - | <span data-ttu-id="677c3-138">11 月 16 日，星期一</span><span class="sxs-lookup"><span data-stu-id="677c3-138">November 16, Monday</span></span> | <span data-ttu-id="677c3-139">11 月 15 日，星期日</span><span class="sxs-lookup"><span data-stu-id="677c3-139">November 15, Sunday</span></span> | - | - |
| <span data-ttu-id="677c3-140">产生的支出</span><span class="sxs-lookup"><span data-stu-id="677c3-140">Expenses incurred</span></span> | <span data-ttu-id="677c3-141">10 月 5 日，星期一</span><span class="sxs-lookup"><span data-stu-id="677c3-141">October 5, Monday</span></span> | <span data-ttu-id="677c3-142">10 月 4 日，星期日</span><span class="sxs-lookup"><span data-stu-id="677c3-142">October 4, Sunday</span></span> | - | - |
| - | <span data-ttu-id="677c3-143">11 月 2 日，星期一</span><span class="sxs-lookup"><span data-stu-id="677c3-143">November 2, Monday</span></span> | <span data-ttu-id="677c3-144">11 月 1 日，星期日</span><span class="sxs-lookup"><span data-stu-id="677c3-144">November 1, Sunday</span></span> | - | - |

<span data-ttu-id="677c3-145">在此示例中，当自动开票在以下时间运行时：</span><span class="sxs-lookup"><span data-stu-id="677c3-145">In this example when the automatic invoicing runs on:</span></span>

- <span data-ttu-id="677c3-146">**10 月 4 日或之前的任何日期**：不会为此合同生成发票，因为这些合同子项中每个合同子项的 **发票计划** 表都不会调出“10 月 4 日，星期日”作为发票运行日期。</span><span class="sxs-lookup"><span data-stu-id="677c3-146">**October 4 or any date before**: No invoice is generated for this contract because the **Invoice Schedule** table for each of these contract lines doesn't call out October 4, Sunday as an invoice run date.</span></span>
- <span data-ttu-id="677c3-147">**10 月 5 日，星期一**：为以下各项生成一个发票：</span><span class="sxs-lookup"><span data-stu-id="677c3-147">**October 5 Monday**: One invoice is generated for:</span></span>

    - <span data-ttu-id="677c3-148">包括里程碑的原型工作（如果其标记为 **可开票**）。</span><span class="sxs-lookup"><span data-stu-id="677c3-148">Prototype work that includes the milestone, if it is marked as **Ready to Invoice**.</span></span>
    - <span data-ttu-id="677c3-149">包括在交易截止日期“10 月 4 日，星期日”之前创建的所有时间交易且标记为 **可开票** 的实施工作。</span><span class="sxs-lookup"><span data-stu-id="677c3-149">Implementation work that includes all Time transactions created before the transaction cut-off date of October 4, Sunday, that is marked as **Ready to Invoice**.</span></span>
    - <span data-ttu-id="677c3-150">包括在交易截止日期“10 月 4 日，星期日”之前创建的所有支出交易且标记为 **可开票** 的产生的支出。</span><span class="sxs-lookup"><span data-stu-id="677c3-150">Expense incurred that includes all Expense transactions created before the transaction cut-off date of October 4, Sunday, that is marked as **Ready to Invoice**.</span></span>
  
- <span data-ttu-id="677c3-151">**10 月 6 日或 10 月 19 日之前的任何日期**：不会为此合同生成发票，因为这些合同子项中每个合同子项的 **发票计划** 表都不会调出“10 月 6 日或 10 月 19 日之前的任何日期”作为发票运行日期。</span><span class="sxs-lookup"><span data-stu-id="677c3-151">**On October 6 or any date before October 19**: No invoice is generated for this contract since the **Invoice Schedule** table for each of these contract lines does not call out October 6 or any date before October 19 as an invoice run date.</span></span>
- <span data-ttu-id="677c3-152">**10 月 19 日，星期一**：将为包括在交易截止日期“10 月 18 日，星期日”之前创建的所有时间交易且标记为 **可开票** 的实施工作生成一个发票。</span><span class="sxs-lookup"><span data-stu-id="677c3-152">**October 19, Monday**: One invoice is generated for implementation work that includes all Time transactions created before the transaction cut-off date of October 18, Sunday, that is marked as **Ready to Invoice**.</span></span>
- <span data-ttu-id="677c3-153">**11 月 2 日，星期一**：为以下各项生成一个发票：</span><span class="sxs-lookup"><span data-stu-id="677c3-153">**November 2 Monday**: One invoice is generated for:</span></span>

    - <span data-ttu-id="677c3-154">包括在交易截止日期“11 月 1 日，星期日”之前创建的所有时间交易且标记为 **可开票** 的实施工作。</span><span class="sxs-lookup"><span data-stu-id="677c3-154">Implementation work that includes all Time transactions created before the transaction cut-off date of November 1, Sunday, that is marked as **Ready to Invoice**.</span></span>
    - <span data-ttu-id="677c3-155">包括在交易截止日期“11 月 1 日，星期日”之前创建的所有支出交易且标记为 **可开票** 的产生的支出。</span><span class="sxs-lookup"><span data-stu-id="677c3-155">Expense incurred that includes all Expense transactions created before the transaction cut-off date of November 1, Sunday, that is marked as **Ready to Invoice**.</span></span>

- <span data-ttu-id="677c3-156">**11 月 3 日，星期二**：将为包括 12000 美元里程碑的原型工作生成一个发票（如果其标记为 **可开票**）。</span><span class="sxs-lookup"><span data-stu-id="677c3-156">**November 3, Tuesday**: One invoice is generated for prototype work that includes the milestone for 12000 USD, if it is marked as **Ready to Invoice**.</span></span>

## <a name="configure-automatic-invoicing"></a><span data-ttu-id="677c3-157">配置自动开票</span><span class="sxs-lookup"><span data-stu-id="677c3-157">Configure automatic invoicing</span></span>

<span data-ttu-id="677c3-158">完成以下步骤配置自动化发票运行。</span><span class="sxs-lookup"><span data-stu-id="677c3-158">Complete the following steps to configure an automated invoice run.</span></span>

1. <span data-ttu-id="677c3-159">在 **Project Operations** 中，转到 **设置** > **定期发票设置**。</span><span class="sxs-lookup"><span data-stu-id="677c3-159">In **Project Operations**, go to **Settings** > **Recurring Invoice Setup**.</span></span>
2. <span data-ttu-id="677c3-160">创建一个批处理作业，将其命名为 **Project Operations 创建发票**。</span><span class="sxs-lookup"><span data-stu-id="677c3-160">Create a batch job, and name it **rPoject Operations Create Invoices**.</span></span> <span data-ttu-id="677c3-161">此批处理作业的名称中必须包含词语“创建发票”。</span><span class="sxs-lookup"><span data-stu-id="677c3-161">The name of the batch job must include the words, "create invoices".</span></span>
3. <span data-ttu-id="677c3-162">在 **作业类型** 字段中，选择 **无**。</span><span class="sxs-lookup"><span data-stu-id="677c3-162">In the **Job Type** field, select **None**.</span></span> <span data-ttu-id="677c3-163">默认情况下，**每天频率** 和 **可用** 字段设置为 **是**。</span><span class="sxs-lookup"><span data-stu-id="677c3-163">By default, the **Frequency Daily** and **Is Active** fields are set to **Yes**.</span></span>
4. <span data-ttu-id="677c3-164">选择 **运行工作流**。</span><span class="sxs-lookup"><span data-stu-id="677c3-164">Select **Run Workflow**.</span></span> <span data-ttu-id="677c3-165">在 **查找记录** 对话框中，您将看到三个工作流：</span><span class="sxs-lookup"><span data-stu-id="677c3-165">In the **Look Up Record** dialog box, you will see three workflows:</span></span>

- <span data-ttu-id="677c3-166">ProcessRunCaller</span><span class="sxs-lookup"><span data-stu-id="677c3-166">ProcessRunCaller</span></span>
- <span data-ttu-id="677c3-167">ProcessRunner</span><span class="sxs-lookup"><span data-stu-id="677c3-167">ProcessRunner</span></span>
- <span data-ttu-id="677c3-168">UpdateRoleUtilization</span><span class="sxs-lookup"><span data-stu-id="677c3-168">UpdateRoleUtilization</span></span>

5. <span data-ttu-id="677c3-169">选择 **ProcessRunCaller**，然后选择 **添加**。</span><span class="sxs-lookup"><span data-stu-id="677c3-169">Select **ProcessRunCaller**, and then select **Add**.</span></span>
6. <span data-ttu-id="677c3-170">在下一个对话框中，选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="677c3-170">In the next dialog box, select **OK**.</span></span> <span data-ttu-id="677c3-171">**Sleep** 工作流后是 **Process** 工作流。</span><span class="sxs-lookup"><span data-stu-id="677c3-171">A **Sleep** workflow is followed by a **Process** workflow.</span></span> 

> [!NOTE]
> <span data-ttu-id="677c3-172">可以选择步骤 5 中的 **ProcessRunner**。</span><span class="sxs-lookup"><span data-stu-id="677c3-172">You can also select **ProcessRunner** in step 5.</span></span> <span data-ttu-id="677c3-173">然后，当您选择 **确定** 时，**Process** 工作流后是 **Sleep** 工作流。</span><span class="sxs-lookup"><span data-stu-id="677c3-173">Then, when you select **OK**, a **Process** workflow is followed by a **Sleep** workflow.</span></span>

<span data-ttu-id="677c3-174">**ProcessRunCaller** 和 **ProcessRunner** 工作流创建发票。</span><span class="sxs-lookup"><span data-stu-id="677c3-174">The **ProcessRunCaller** and **ProcessRunner** workflows create invoices.</span></span> <span data-ttu-id="677c3-175">**ProcessRunCaller** 调用 **ProcessRunner**。</span><span class="sxs-lookup"><span data-stu-id="677c3-175">**ProcessRunCaller** calls **ProcessRunner**.</span></span> <span data-ttu-id="677c3-176">**ProcessRunner** 是真正创建发票的工作流。</span><span class="sxs-lookup"><span data-stu-id="677c3-176">**ProcessRunner** is the workflow that actually creates the invoices.</span></span> <span data-ttu-id="677c3-177">此工作流经过必须为其创建发票的所有合同子项，然后为这些子项创建发票。</span><span class="sxs-lookup"><span data-stu-id="677c3-177">The workflow goes through all the contract lines that invoices must be created for, and creates invoices for those lines.</span></span> <span data-ttu-id="677c3-178">为了确定必须为其创建发票的合同子项，作业将查看合同子项的发票运行日期。</span><span class="sxs-lookup"><span data-stu-id="677c3-178">To determine the contract lines that invoices must be created for, the job looks at invoice run dates for the contract lines.</span></span> <span data-ttu-id="677c3-179">如果属于一个合同的合同子项具有同一个发票运行日期，将把交易合并到一张具有两项发票明细的发票中。</span><span class="sxs-lookup"><span data-stu-id="677c3-179">If contract lines that belong to one contract have the same invoice run date, the transactions are combined into one invoice that has two invoice lines.</span></span> <span data-ttu-id="677c3-180">如果没有需要为其创建发票的交易，作业将跳过发票创建。</span><span class="sxs-lookup"><span data-stu-id="677c3-180">If there are no transactions to create invoices for, the job skips creating an invoice.</span></span>

<span data-ttu-id="677c3-181">**ProcessRunner** 完成运行之后，将调用 **ProcessRunCaller**，提供结束时间，然后关闭。</span><span class="sxs-lookup"><span data-stu-id="677c3-181">After **ProcessRunner** has finished running, it calls **ProcessRunCaller**, provides the end time, and is closed.</span></span> <span data-ttu-id="677c3-182">然后，**ProcessRunCaller** 启动一个从指定结束日期开始运行 24 小时的计时器。</span><span class="sxs-lookup"><span data-stu-id="677c3-182">**ProcessRunCaller** then starts a timer that runs for 24-hours from the specified end time.</span></span> <span data-ttu-id="677c3-183">此计时器结束时，将关闭 **ProcessRunCaller**。</span><span class="sxs-lookup"><span data-stu-id="677c3-183">At the end of the timer, **ProcessRunCaller** is closed.</span></span>

<span data-ttu-id="677c3-184">用于创建发票的批处理作业是周期性作业。</span><span class="sxs-lookup"><span data-stu-id="677c3-184">The batch process job for creating invoices is a recurrent job.</span></span> <span data-ttu-id="677c3-185">如果多次运行此批处理流程，将创建多个作业实例，并导致出错。</span><span class="sxs-lookup"><span data-stu-id="677c3-185">If this batch process is run many times, multiple instances of the job are created and causes errors.</span></span> <span data-ttu-id="677c3-186">因此，仅应启动此批处理流程一次，之后仅在它停止运行时重新启动。</span><span class="sxs-lookup"><span data-stu-id="677c3-186">Therefore, you should start the batch process only one time, and then restart only if it stops running.</span></span>

> [!NOTE]
> <span data-ttu-id="677c3-187">Project Operations 中的批处理开票仅为按发票计划配置的项目合同子项运行。</span><span class="sxs-lookup"><span data-stu-id="677c3-187">Batch invoicing in Project Operations only runs for project contract lines that are configured by invoice schedules.</span></span> <span data-ttu-id="677c3-188">必须为采用固定价格记帐方法的合同子项配置里程碑。</span><span class="sxs-lookup"><span data-stu-id="677c3-188">A contract line with a fixed price billing method must have milestones configured.</span></span> <span data-ttu-id="677c3-189">将需要为采用时间和材料记帐方法的项目合同子项设置基于日期的发票计划。</span><span class="sxs-lookup"><span data-stu-id="677c3-189">A project contract line with a time and material billing method will need a date-based invoice schedule set up.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
