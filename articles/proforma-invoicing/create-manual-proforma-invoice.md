---
title: 创建手动估价发票
description: 本主题提供有关创建估价发票的信息。
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
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
ms.openlocfilehash: 3289b8bcaddaebe1a3657b5902c1d324f9e0fd53
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/15/2021
ms.locfileid: "5287767"
---
# <a name="create-a-manual-proforma-invoice"></a><span data-ttu-id="bdcdf-103">创建手动估价发票</span><span class="sxs-lookup"><span data-stu-id="bdcdf-103">Create a manual proforma invoice</span></span>

<span data-ttu-id="bdcdf-104">_**适用于：** 面向资源/非库存场景的 Project Operations_</span><span class="sxs-lookup"><span data-stu-id="bdcdf-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="bdcdf-105">开票可以在项目经理为客户创建发票之前为项目经理增加一级审批。</span><span class="sxs-lookup"><span data-stu-id="bdcdf-105">Invoicing gives project managers a second level of approval before they create invoices for customers.</span></span> <span data-ttu-id="bdcdf-106">批准了项目团队成员提交的时间和支出条目时，即完成了第一级审批。</span><span class="sxs-lookup"><span data-stu-id="bdcdf-106">The first level of approval is completed when the time and expense entries that project team members submit are approved.</span></span>

<span data-ttu-id="bdcdf-107">Dynamics 365 Project Operations 不应生成面向客户的发票，原因如下：</span><span class="sxs-lookup"><span data-stu-id="bdcdf-107">Dynamics 365 Project Operations isn't designed to generate customer-facing invoices, for the following reasons:</span></span>

- <span data-ttu-id="bdcdf-108">其中不包含税务信息。</span><span class="sxs-lookup"><span data-stu-id="bdcdf-108">It doesn't contain tax information.</span></span>
- <span data-ttu-id="bdcdf-109">不能使用当前配置的汇率将其他货币转换为开票货币。</span><span class="sxs-lookup"><span data-stu-id="bdcdf-109">It can't convert other currencies to the invoicing currency by using correctly configured exchange rates.</span></span>
- <span data-ttu-id="bdcdf-110">不能正确设置发票格式以打印发票。</span><span class="sxs-lookup"><span data-stu-id="bdcdf-110">It can't correctly format invoices so that they can be printed.</span></span>

<span data-ttu-id="bdcdf-111">但是，您可以使用财务或会计系统创建面向客户的发票以使用生成的发票方案的信息。</span><span class="sxs-lookup"><span data-stu-id="bdcdf-111">Instead, you can use a financial or accounting system to create customer-facing invoices that use the information from generated invoice proposals.</span></span>

## <a name="creating-project-invoices"></a><span data-ttu-id="bdcdf-112">创建项目发票</span><span class="sxs-lookup"><span data-stu-id="bdcdf-112">Creating project invoices</span></span>

<span data-ttu-id="bdcdf-113">项目发票可以一次创建一个，也可以批量创建。</span><span class="sxs-lookup"><span data-stu-id="bdcdf-113">Project invoices can be created one at a time or in bulk.</span></span> <span data-ttu-id="bdcdf-114">可以手动创建，也可以配置为通过自动运行来生成。</span><span class="sxs-lookup"><span data-stu-id="bdcdf-114">You can create them manually, or they can be configured so that they are generated in automated runs.</span></span>

### <a name="manually-create-project-invoices"></a><span data-ttu-id="bdcdf-115">手动创建项目发票</span><span class="sxs-lookup"><span data-stu-id="bdcdf-115">Manually create project invoices</span></span> 

<span data-ttu-id="bdcdf-116">从 **项目合同** 列表页，可以为每个项目合同分别创建项目发票，也可以为多个项目合同批量创建发票。</span><span class="sxs-lookup"><span data-stu-id="bdcdf-116">From the **Project Contracts** list page, you can create project invoices separately for each project contract, or you can create invoices in bulk for multiple project contracts.</span></span>

<span data-ttu-id="bdcdf-117">请执行以下步骤为特定项目合同创建发票。</span><span class="sxs-lookup"><span data-stu-id="bdcdf-117">Follow this step to create an invoice for a specific project contract.</span></span>

- <span data-ttu-id="bdcdf-118">在 **项目合同** 列表页中，打开一个项目合同，然后选择 **创建发票**。</span><span class="sxs-lookup"><span data-stu-id="bdcdf-118">On the **Project Contracts** list page, open a project contract, and then select **Create Invoice**.</span></span>

    <span data-ttu-id="bdcdf-119">将为所选项目合同的所有状态为 **已准备好开具发票** 的交易生成发票。</span><span class="sxs-lookup"><span data-stu-id="bdcdf-119">An invoice is generated for all transactions for the selected project contract that have a status of **Ready to Invoice**.</span></span> <span data-ttu-id="bdcdf-120">这些交易包括时间、支出、里程碑和基于产品的合同子项。</span><span class="sxs-lookup"><span data-stu-id="bdcdf-120">These transactions include time, expenses, milestones, and product-based contract lines.</span></span>

<span data-ttu-id="bdcdf-121">执行以下步骤批量创建发票。</span><span class="sxs-lookup"><span data-stu-id="bdcdf-121">Follow these steps to create invoices in bulk.</span></span>

1. <span data-ttu-id="bdcdf-122">在 **项目合同** 列表页，选择必须为其创建发票的一个或多个项目合同，然后选择 **创建项目合同**。</span><span class="sxs-lookup"><span data-stu-id="bdcdf-122">On the **Project Contracts** list page, select one or more project contracts that you must create an invoice for, and then select **Create Project Invoices**.</span></span>

    <span data-ttu-id="bdcdf-123">将显示警告消息，说明可能会经过一段延迟才会创建发票。</span><span class="sxs-lookup"><span data-stu-id="bdcdf-123">A warning message informs you that there might be a delay before invoices are created.</span></span> <span data-ttu-id="bdcdf-124">还将显示进度。</span><span class="sxs-lookup"><span data-stu-id="bdcdf-124">The process is also shown.</span></span>

2. <span data-ttu-id="bdcdf-125">选择 **确定** 关闭消息框。</span><span class="sxs-lookup"><span data-stu-id="bdcdf-125">Select **OK** to close the message box.</span></span>

    <span data-ttu-id="bdcdf-126">将为合同子项中所有状态为 **已准备好开具发票** 的交易生成发票。</span><span class="sxs-lookup"><span data-stu-id="bdcdf-126">An invoice is generated for all transactions on a contract line that have a status of **Ready to Invoice**.</span></span> <span data-ttu-id="bdcdf-127">这些交易包括时间、支出、里程碑和基于产品的合同子项。</span><span class="sxs-lookup"><span data-stu-id="bdcdf-127">These transactions include time, expenses, milestones, and product-based contract lines.</span></span>

3. <span data-ttu-id="bdcdf-128">若要查看生成的发票，请转到 **Sales** \> **记帐** \> **发票**。</span><span class="sxs-lookup"><span data-stu-id="bdcdf-128">To view the invoices that are generated, go to **Sales** \> **Billing** \> **Invoices**.</span></span> <span data-ttu-id="bdcdf-129">您将看到每个项目合同的一张发票。</span><span class="sxs-lookup"><span data-stu-id="bdcdf-129">You will see one invoice for each project contract.</span></span>

### <a name="set-up-automated-creation-of-project-invoices"></a><span data-ttu-id="bdcdf-130">设置项目发票自动创建</span><span class="sxs-lookup"><span data-stu-id="bdcdf-130">Set up automated creation of project invoices</span></span> 

<span data-ttu-id="bdcdf-131">执行以下步骤以配置自动化发票运行。</span><span class="sxs-lookup"><span data-stu-id="bdcdf-131">Follow these steps to configure an automated invoice run.</span></span>

1. <span data-ttu-id="bdcdf-132">转至 **设置** \> **批处理作业**。</span><span class="sxs-lookup"><span data-stu-id="bdcdf-132">Go to **Settings** \> **Batch jobs**.</span></span>
2. <span data-ttu-id="bdcdf-133">创建一个批处理作业，将其命名为 **Project Operations 创建发票**。</span><span class="sxs-lookup"><span data-stu-id="bdcdf-133">Create a batch job, and name it **Project Operations Create Invoices**.</span></span> <span data-ttu-id="bdcdf-134">此批处理作业的名称中必须包含术语“创建发票”。</span><span class="sxs-lookup"><span data-stu-id="bdcdf-134">The name of the batch job must include the term "Create Invoices."</span></span>
3. <span data-ttu-id="bdcdf-135">在 **作业类型** 字段中，选择 **无**。</span><span class="sxs-lookup"><span data-stu-id="bdcdf-135">In the **Job type** field, select **None**.</span></span> <span data-ttu-id="bdcdf-136">默认情况下，**每天频率** 和 **可用** 选项设置为 **是**。</span><span class="sxs-lookup"><span data-stu-id="bdcdf-136">By default, the **Frequency Daily** and **Is Active** options are set to **Yes**.</span></span>
4. <span data-ttu-id="bdcdf-137">选择 **运行工作流**。</span><span class="sxs-lookup"><span data-stu-id="bdcdf-137">Select **Run Workflow**.</span></span> <span data-ttu-id="bdcdf-138">在 **查找记录** 对话框中，您将看到三个工作流：</span><span class="sxs-lookup"><span data-stu-id="bdcdf-138">In the **Look Up Record** dialog box, you will see three workflows:</span></span>

    - <span data-ttu-id="bdcdf-139">ProcessRunCaller</span><span class="sxs-lookup"><span data-stu-id="bdcdf-139">ProcessRunCaller</span></span>
    - <span data-ttu-id="bdcdf-140">ProcessRunner</span><span class="sxs-lookup"><span data-stu-id="bdcdf-140">ProcessRunner</span></span>
    - <span data-ttu-id="bdcdf-141">UpdateRoleUtilization</span><span class="sxs-lookup"><span data-stu-id="bdcdf-141">UpdateRoleUtilization</span></span>

5. <span data-ttu-id="bdcdf-142">选择 **ProcessRunCaller**，然后选择 **添加**。</span><span class="sxs-lookup"><span data-stu-id="bdcdf-142">Select **ProcessRunCaller**, and then select **Add**.</span></span>
6. <span data-ttu-id="bdcdf-143">在下一个对话框中，选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="bdcdf-143">In the next dialog box, select **OK**.</span></span> <span data-ttu-id="bdcdf-144">**Sleep** 工作流后是 **Process** 工作流。</span><span class="sxs-lookup"><span data-stu-id="bdcdf-144">A **Sleep** workflow is followed by a **Process** workflow.</span></span>

    <span data-ttu-id="bdcdf-145">可以选择步骤 5 中的 **ProcessRunner**。</span><span class="sxs-lookup"><span data-stu-id="bdcdf-145">You can also select **ProcessRunner** in step 5.</span></span> <span data-ttu-id="bdcdf-146">然后，当您选择 **确定** 时，**Process** 工作流后是 **Sleep** 工作流。</span><span class="sxs-lookup"><span data-stu-id="bdcdf-146">Then, when you select **OK**, a **Process** workflow is followed by a **Sleep** workflow.</span></span>

<span data-ttu-id="bdcdf-147">**ProcessRunCaller** 和 **ProcessRunner** 工作流创建发票。</span><span class="sxs-lookup"><span data-stu-id="bdcdf-147">The **ProcessRunCaller** and **ProcessRunner** workflows create invoices.</span></span> <span data-ttu-id="bdcdf-148">**ProcessRunCaller** 调用 **ProcessRunner**。</span><span class="sxs-lookup"><span data-stu-id="bdcdf-148">**ProcessRunCaller** calls **ProcessRunner**.</span></span> <span data-ttu-id="bdcdf-149">**ProcessRunner** 是真正创建发票的工作流。</span><span class="sxs-lookup"><span data-stu-id="bdcdf-149">**ProcessRunner** is the workflow that actually creates the invoices.</span></span> <span data-ttu-id="bdcdf-150">它浏览必须为其创建发票的所有合同子项，然后为这些子项创建发票。</span><span class="sxs-lookup"><span data-stu-id="bdcdf-150">It goes through all the contract lines that invoices must be created for, and it creates invoices for those lines.</span></span> <span data-ttu-id="bdcdf-151">为了确定必须为其创建发票的合同子项，作业将查看合同子项的发票运行日期。</span><span class="sxs-lookup"><span data-stu-id="bdcdf-151">To determine the contract lines that invoices must be created for, the job looks at invoice run dates for the contract lines.</span></span> <span data-ttu-id="bdcdf-152">如果属于一个合同的合同子项具有同一个发票运行日期，将把交易合并到一张具有两项发票明细的发票中。</span><span class="sxs-lookup"><span data-stu-id="bdcdf-152">If contract lines that belong to one contract have the same invoice run date, the transactions are combined into one invoice that has two invoice lines.</span></span> <span data-ttu-id="bdcdf-153">如果没有需要为其创建发票的交易，作业将跳过发票创建。</span><span class="sxs-lookup"><span data-stu-id="bdcdf-153">If there are no transactions to create invoices for, the job skips invoice creation.</span></span>

<span data-ttu-id="bdcdf-154">**ProcessRunner** 完成运行之后，将调用 **ProcessRunCaller**，提供结束时间，然后关闭。</span><span class="sxs-lookup"><span data-stu-id="bdcdf-154">After **ProcessRunner** has finished running, it calls **ProcessRunCaller**, provides the end time, and is closed.</span></span> <span data-ttu-id="bdcdf-155">然后，**ProcessRunCaller** 启动一个从指定结束日期开始运行 24 小时的计时器。</span><span class="sxs-lookup"><span data-stu-id="bdcdf-155">**ProcessRunCaller** then starts a timer that runs for 24 hours from the specified end time.</span></span> <span data-ttu-id="bdcdf-156">此计时器结束时，将关闭 **ProcessRunCaller**。</span><span class="sxs-lookup"><span data-stu-id="bdcdf-156">At the end of the timer, **ProcessRunCaller** is closed.</span></span>

<span data-ttu-id="bdcdf-157">用于创建发票的批处理作业是周期性作业。</span><span class="sxs-lookup"><span data-stu-id="bdcdf-157">The batch process job for creating invoices is a recurrent job.</span></span> <span data-ttu-id="bdcdf-158">如果多次运行此批处理流程，将创建多个作业实例，并导致出错。</span><span class="sxs-lookup"><span data-stu-id="bdcdf-158">If this batch process is run many times, multiple instances of the job are created and cause errors.</span></span> <span data-ttu-id="bdcdf-159">因此，仅应启动此批处理流程一次，并且仅当其停止运行时才应重新启动它。</span><span class="sxs-lookup"><span data-stu-id="bdcdf-159">Therefore, you should start the batch process only one time, and you should restart it only if it stops running.</span></span>

> [!NOTE]
> <span data-ttu-id="bdcdf-160">仅为按发票计划配置的项目合同子项运行批处理开票。</span><span class="sxs-lookup"><span data-stu-id="bdcdf-160">Batch invoicing only runs for project contract lines that are configured by invoice schedules.</span></span> <span data-ttu-id="bdcdf-161">必须为采用固定价格记帐方法的合同子项配置里程碑。</span><span class="sxs-lookup"><span data-stu-id="bdcdf-161">A contract line with a fixed price billing method must have milestones configured.</span></span> <span data-ttu-id="bdcdf-162">将需要为采用时间和材料记帐方法的项目合同子项设置基于日期的发票计划。</span><span class="sxs-lookup"><span data-stu-id="bdcdf-162">A project contract line with a time and material billing method will need a date-based invoice schedule set up.</span></span> <span data-ttu-id="bdcdf-163">这同样适用于基于项目的合同子项。</span><span class="sxs-lookup"><span data-stu-id="bdcdf-163">The same applies to a project-based contract line.</span></span>      
 
### <a name="edit-a-draft-invoice"></a><span data-ttu-id="bdcdf-164">编辑草稿发票</span><span class="sxs-lookup"><span data-stu-id="bdcdf-164">Edit a draft invoice</span></span>

<span data-ttu-id="bdcdf-165">创建项目草稿发票时，将把批准时间和支出条目时创建的所有未记帐销售交易提取到该发票中。</span><span class="sxs-lookup"><span data-stu-id="bdcdf-165">When you create a draft project invoice, all unbilled sales transactions that were created when the time and expense entries were approved are pulled onto the invoice.</span></span> <span data-ttu-id="bdcdf-166">可以在发票仍然处于草稿阶段时进行以下调整：</span><span class="sxs-lookup"><span data-stu-id="bdcdf-166">You can make the following adjustments while the invoice is still in a draft stage:</span></span>

- <span data-ttu-id="bdcdf-167">删除或编辑发票明细详细信息。</span><span class="sxs-lookup"><span data-stu-id="bdcdf-167">Delete or edit invoice line details.</span></span>
- <span data-ttu-id="bdcdf-168">编辑和调整数量和记帐类型。</span><span class="sxs-lookup"><span data-stu-id="bdcdf-168">Edit and adjust the quantity and billing type.</span></span>
- <span data-ttu-id="bdcdf-169">直接将时间、支出和费用作为交易添加到发票中。</span><span class="sxs-lookup"><span data-stu-id="bdcdf-169">Directly add time, expense, and fees as transactions on the invoice.</span></span> <span data-ttu-id="bdcdf-170">如果发票明细映射到允许这些交易分类的合同明细，则可使用此功能。</span><span class="sxs-lookup"><span data-stu-id="bdcdf-170">You can use this feature if the invoice line is mapped to a contract line that allows for these transaction classes.</span></span>

<span data-ttu-id="bdcdf-171">选择 **确认** 以确认发票。</span><span class="sxs-lookup"><span data-stu-id="bdcdf-171">Select **Confirm** to confirm an invoice.</span></span> <span data-ttu-id="bdcdf-172">“确认”操作是单向操作。</span><span class="sxs-lookup"><span data-stu-id="bdcdf-172">The Confirm action is a one-way action.</span></span> <span data-ttu-id="bdcdf-173">选择 **确认** 时，系统将把发票设置为只读，并根据每项发票明细的每项发票明细详细信息创建已记帐实际销售额。</span><span class="sxs-lookup"><span data-stu-id="bdcdf-173">When you select **Confirm**, the system makes the invoice read-only and creates billed sales actuals from each invoice line detail for each invoice line.</span></span> <span data-ttu-id="bdcdf-174">如果发票明细详细信息引用未记帐实际销售额，系统还将冲销这个未记帐实际销售额。</span><span class="sxs-lookup"><span data-stu-id="bdcdf-174">If the invoice line detail references an unbilled sales actual, the system also reverses the unbilled sales actual.</span></span> <span data-ttu-id="bdcdf-175">（所有基于时间或支出条目创建的发票明细详细信息都将引用未记帐实际销售额。）总帐集成系统可以使用此项冲销来冲销项目的在制品 (WIP) 以达成会计目的。</span><span class="sxs-lookup"><span data-stu-id="bdcdf-175">(Any invoice line detail that was created from a time or expense entry will reference an unbilled sales actual.) General ledger integration systems can use this reversal to reverse project work in progress (WIP) for accounting purposes.</span></span>

### <a name="correct-a-confirmed-invoice"></a><span data-ttu-id="bdcdf-176">更正已确认的发票</span><span class="sxs-lookup"><span data-stu-id="bdcdf-176">Correct a confirmed invoice</span></span>

<span data-ttu-id="bdcdf-177">可以编辑（更正）已确认的发票。</span><span class="sxs-lookup"><span data-stu-id="bdcdf-177">Confirmed invoices can be edited (corrected).</span></span> <span data-ttu-id="bdcdf-178">更正已确认的发票时，将创建新的草稿纠正发票。</span><span class="sxs-lookup"><span data-stu-id="bdcdf-178">When you correct a confirmed invoice, a new draft corrective invoice is created.</span></span> <span data-ttu-id="bdcdf-179">因为假设您希望冲销原始发票中的所有交易和数量，所以此纠正发票中包含原始发票中的所有交易，并且其中的所有数量均为 0（零）。</span><span class="sxs-lookup"><span data-stu-id="bdcdf-179">Because the assumption is that you want to reverse all the transactions and quantities from the original invoice, this corrective invoice includes all the transactions from the original invoice, and all the quantities on it are 0 (zero).</span></span>

<span data-ttu-id="bdcdf-180">如果有任何交易不需要更正，可以将其从草稿纠正发票中删除。</span><span class="sxs-lookup"><span data-stu-id="bdcdf-180">If any transactions don't require correction, you can remove them from the draft corrective invoice.</span></span> <span data-ttu-id="bdcdf-181">如果要仅冲销或返回部分数量，可以编辑明细详细信息中的 **数量** 字段。</span><span class="sxs-lookup"><span data-stu-id="bdcdf-181">If you want to reverse or return only a partial quantity, you can edit the **Quantity** field on the line detail.</span></span> <span data-ttu-id="bdcdf-182">如果打开发票明细详细信息，可以看到原始发票数量。</span><span class="sxs-lookup"><span data-stu-id="bdcdf-182">If you open the invoice line detail, you can see the original invoice quantity.</span></span> <span data-ttu-id="bdcdf-183">然后可以编辑当前发票数量，使其比原始发票数量少或多。</span><span class="sxs-lookup"><span data-stu-id="bdcdf-183">You can then edit the current invoice quantity so that it's less than or more than the original invoice quantity.</span></span>

<span data-ttu-id="bdcdf-184">确认纠正发票时，将撤消原始已记帐实际销售额，并创建新的已记帐实际销售额。</span><span class="sxs-lookup"><span data-stu-id="bdcdf-184">When you confirm a corrective invoice, the original billed sales actual is reversed, and a new billed sales actual is created.</span></span> <span data-ttu-id="bdcdf-185">如果减少了数量，差额将导致也创建一项新的未记帐实际销售额。</span><span class="sxs-lookup"><span data-stu-id="bdcdf-185">If the quantity was reduced, the difference will cause a new unbilled sales actual to be created too.</span></span> <span data-ttu-id="bdcdf-186">例如，如果原始已记帐销售额是八小时的，并且纠正发票明细详细信息的减少后数量为六小时，将冲销原始已记帐销售明细，并创建两项新的实际值：</span><span class="sxs-lookup"><span data-stu-id="bdcdf-186">For example, if the original billed sale was for eight hours, and the corrective invoice line detail has a reduced quantity of six hours, the original billed sales line is reversed and two new actuals are created:</span></span>

- <span data-ttu-id="bdcdf-187">六小时的已记帐实际销售额。</span><span class="sxs-lookup"><span data-stu-id="bdcdf-187">A billed sales actual for six hours.</span></span>
- <span data-ttu-id="bdcdf-188">其余两小时的未记帐实际销售额。</span><span class="sxs-lookup"><span data-stu-id="bdcdf-188">An unbilled sales actual for the remaining two hours.</span></span> <span data-ttu-id="bdcdf-189">以后可为此交易记帐或标记为非应计费，具体取决于与客户的协商结果。</span><span class="sxs-lookup"><span data-stu-id="bdcdf-189">This transaction can either be billed later or marked as non-chargeable, depending on the negotiations with the customer.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]