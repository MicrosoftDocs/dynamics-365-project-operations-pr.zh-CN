---
title: 估价发票
description: 此主题提供有关 Project Operations 的估价发票的信息。
author: rumant
ms.date: 04/05/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 3eaf2f19506c5464c302176fc620aad5f29b4ae7
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/10/2021
ms.locfileid: "6000650"
---
# <a name="proforma-invoices"></a><span data-ttu-id="349c2-103">估价发票</span><span class="sxs-lookup"><span data-stu-id="349c2-103">Proforma invoices</span></span>

<span data-ttu-id="349c2-104">_**适用于：** 面向资源/非库存场景的 Project Operations_</span><span class="sxs-lookup"><span data-stu-id="349c2-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="349c2-105">估价开票可以在项目经理为客户创建发票之前为项目经理增加一级审批。</span><span class="sxs-lookup"><span data-stu-id="349c2-105">Proforma invoicing gives project managers a second level of approval before they create invoices for customers.</span></span> <span data-ttu-id="349c2-106">批准了项目团队成员提交的时间、支出和材料条目时，即完成了第一级审批。</span><span class="sxs-lookup"><span data-stu-id="349c2-106">The first level of approval is completed when time, expense, and material entries that project team members submit are approved.</span></span> <span data-ttu-id="349c2-107">已确认估价发票在 Project Operations 的项目会计模块中可用。</span><span class="sxs-lookup"><span data-stu-id="349c2-107">Confirmed proforma invoices are available in the Project Accounting module of Project Operations.</span></span> <span data-ttu-id="349c2-108">项目会计人员可以执行其他更新，例如销售税款、会计和发票布局。</span><span class="sxs-lookup"><span data-stu-id="349c2-108">Project accountants can perform additional updates such as sales tax, accounting, and invoice layout.</span></span>


## <a name="creating-project-invoices"></a><span data-ttu-id="349c2-109">创建项目发票</span><span class="sxs-lookup"><span data-stu-id="349c2-109">Creating project invoices</span></span>

<span data-ttu-id="349c2-110">项目发票可以一次创建一个，也可以批量创建。</span><span class="sxs-lookup"><span data-stu-id="349c2-110">Project invoices can be created one at a time or in bulk.</span></span> <span data-ttu-id="349c2-111">可以手动创建，也可以配置为通过自动运行来生成。</span><span class="sxs-lookup"><span data-stu-id="349c2-111">You can create them manually, or they can be configured so that they are generated in automated runs.</span></span>

### <a name="manually-create-project-invoices"></a><span data-ttu-id="349c2-112">手动创建项目发票</span><span class="sxs-lookup"><span data-stu-id="349c2-112">Manually create project invoices</span></span> 

<span data-ttu-id="349c2-113">从 **项目合同** 列表页，可以为每个项目合同分别创建项目发票，也可以为多个项目合同批量创建发票。</span><span class="sxs-lookup"><span data-stu-id="349c2-113">From the **Project Contracts** list page, you can create project invoices separately for each project contract, or you can create invoices in bulk for multiple project contracts.</span></span>

<span data-ttu-id="349c2-114">请执行以下步骤为特定项目合同创建发票。</span><span class="sxs-lookup"><span data-stu-id="349c2-114">Follow this step to create an invoice for a specific project contract.</span></span>

- <span data-ttu-id="349c2-115">在 **项目合同** 列表页中，打开一个项目合同，然后选择 **创建发票**。</span><span class="sxs-lookup"><span data-stu-id="349c2-115">On the **Project Contracts** list page, open a project contract, and then select **Create Invoice**.</span></span>

    <span data-ttu-id="349c2-116">将为所选项目合同的所有状态为 **已准备好开具发票** 的交易生成发票。</span><span class="sxs-lookup"><span data-stu-id="349c2-116">An invoice is generated for all transactions for the selected project contract that have a status of **Ready to Invoice**.</span></span> <span data-ttu-id="349c2-117">这些交易包括时间、支出、材料、里程碑和其他未记帐的销售日记帐行。</span><span class="sxs-lookup"><span data-stu-id="349c2-117">These transactions include time, expenses, materials, milestones, and other unbilled sales journal lines.</span></span>

<span data-ttu-id="349c2-118">执行以下步骤批量创建发票。</span><span class="sxs-lookup"><span data-stu-id="349c2-118">Follow these steps to create invoices in bulk.</span></span>

1. <span data-ttu-id="349c2-119">在 **项目合同** 列表页，选择必须为其创建发票的一个或多个项目合同，然后选择 **创建项目合同**。</span><span class="sxs-lookup"><span data-stu-id="349c2-119">On the **Project Contracts** list page, select one or more project contracts that you must create an invoice for, and then select **Create Project Invoices**.</span></span>

    <span data-ttu-id="349c2-120">将显示警告消息，说明可能会经过一段延迟才会创建发票。</span><span class="sxs-lookup"><span data-stu-id="349c2-120">A warning message informs you that there might be a delay before invoices are created.</span></span> <span data-ttu-id="349c2-121">还将显示进度。</span><span class="sxs-lookup"><span data-stu-id="349c2-121">The process is also shown.</span></span>

2. <span data-ttu-id="349c2-122">选择 **确定** 关闭消息框。</span><span class="sxs-lookup"><span data-stu-id="349c2-122">Select **OK** to close the message box.</span></span>

    <span data-ttu-id="349c2-123">将为合同子项中所有状态为 **已准备好开具发票** 的交易生成发票。</span><span class="sxs-lookup"><span data-stu-id="349c2-123">An invoice is generated for all transactions on a contract line that have a status of **Ready to Invoice**.</span></span> <span data-ttu-id="349c2-124">这些交易包括时间、支出、材料、里程碑和其他未记帐的销售日记帐行。</span><span class="sxs-lookup"><span data-stu-id="349c2-124">These transactions include time, expenses, materials, milestones, and other unbilled sales journal lines.</span></span>

3. <span data-ttu-id="349c2-125">若要查看生成的发票，请转到 **Sales** \> **记帐** \> **发票**。</span><span class="sxs-lookup"><span data-stu-id="349c2-125">To view the invoices that are generated, go to **Sales** \> **Billing** \> **Invoices**.</span></span> <span data-ttu-id="349c2-126">您将看到每个项目合同的一张发票。</span><span class="sxs-lookup"><span data-stu-id="349c2-126">You will see one invoice for each project contract.</span></span>

### <a name="set-up-automated-creation-of-project-invoices"></a><span data-ttu-id="349c2-127">设置项目发票自动创建</span><span class="sxs-lookup"><span data-stu-id="349c2-127">Set up automated creation of project invoices</span></span> 

<span data-ttu-id="349c2-128">执行以下步骤以配置自动化发票运行。</span><span class="sxs-lookup"><span data-stu-id="349c2-128">Follow these steps to configure an automated invoice run.</span></span>

1. <span data-ttu-id="349c2-129">转至 **设置** \> **批处理作业**。</span><span class="sxs-lookup"><span data-stu-id="349c2-129">Go to **Settings** \> **Batch jobs**.</span></span>
2. <span data-ttu-id="349c2-130">创建一个批处理作业，将其命名为 **Project Operations 创建发票**。</span><span class="sxs-lookup"><span data-stu-id="349c2-130">Create a batch job, and name it **Project Operations Create Invoices**.</span></span> <span data-ttu-id="349c2-131">此批处理作业的名称中必须包含术语“创建发票”。</span><span class="sxs-lookup"><span data-stu-id="349c2-131">The name of the batch job must include the term "Create Invoices."</span></span>
3. <span data-ttu-id="349c2-132">在 **作业类型** 字段中，选择 **无**。</span><span class="sxs-lookup"><span data-stu-id="349c2-132">In the **Job type** field, select **None**.</span></span> <span data-ttu-id="349c2-133">默认情况下，**每天频率** 和 **可用** 选项设置为 **是**。</span><span class="sxs-lookup"><span data-stu-id="349c2-133">By default, the **Frequency Daily** and **Is Active** options are set to **Yes**.</span></span>
4. <span data-ttu-id="349c2-134">选择 **运行工作流**。</span><span class="sxs-lookup"><span data-stu-id="349c2-134">Select **Run Workflow**.</span></span> <span data-ttu-id="349c2-135">在 **查找记录** 对话框中，您将看到三个工作流：</span><span class="sxs-lookup"><span data-stu-id="349c2-135">In the **Look Up Record** dialog box, you will see three workflows:</span></span>

    - <span data-ttu-id="349c2-136">ProcessRunCaller</span><span class="sxs-lookup"><span data-stu-id="349c2-136">ProcessRunCaller</span></span>
    - <span data-ttu-id="349c2-137">ProcessRunner</span><span class="sxs-lookup"><span data-stu-id="349c2-137">ProcessRunner</span></span>
    - <span data-ttu-id="349c2-138">UpdateRoleUtilization</span><span class="sxs-lookup"><span data-stu-id="349c2-138">UpdateRoleUtilization</span></span>

5. <span data-ttu-id="349c2-139">选择 **ProcessRunCaller**，然后选择 **添加**。</span><span class="sxs-lookup"><span data-stu-id="349c2-139">Select **ProcessRunCaller**, and then select **Add**.</span></span>
6. <span data-ttu-id="349c2-140">在下一个对话框中，选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="349c2-140">In the next dialog box, select **OK**.</span></span> <span data-ttu-id="349c2-141">**Sleep** 工作流后是 **Process** 工作流。</span><span class="sxs-lookup"><span data-stu-id="349c2-141">A **Sleep** workflow is followed by a **Process** workflow.</span></span>

    <span data-ttu-id="349c2-142">可以选择步骤 5 中的 **ProcessRunner**。</span><span class="sxs-lookup"><span data-stu-id="349c2-142">You can also select **ProcessRunner** in step 5.</span></span> <span data-ttu-id="349c2-143">然后，当您选择 **确定** 时，**Process** 工作流后是 **Sleep** 工作流。</span><span class="sxs-lookup"><span data-stu-id="349c2-143">Then, when you select **OK**, a **Process** workflow is followed by a **Sleep** workflow.</span></span>

<span data-ttu-id="349c2-144">**ProcessRunCaller** 和 **ProcessRunner** 工作流创建发票。</span><span class="sxs-lookup"><span data-stu-id="349c2-144">The **ProcessRunCaller** and **ProcessRunner** workflows create invoices.</span></span> <span data-ttu-id="349c2-145">**ProcessRunCaller** 调用 **ProcessRunner**。</span><span class="sxs-lookup"><span data-stu-id="349c2-145">**ProcessRunCaller** calls **ProcessRunner**.</span></span> <span data-ttu-id="349c2-146">**ProcessRunner** 是真正创建发票的工作流。</span><span class="sxs-lookup"><span data-stu-id="349c2-146">**ProcessRunner** is the workflow that actually creates the invoices.</span></span> <span data-ttu-id="349c2-147">它浏览必须为其创建发票的所有合同子项，然后为这些子项创建发票。</span><span class="sxs-lookup"><span data-stu-id="349c2-147">It goes through all the contract lines that invoices must be created for, and it creates invoices for those lines.</span></span> <span data-ttu-id="349c2-148">为了确定必须为其创建发票的合同子项，作业将查看合同子项的发票运行日期。</span><span class="sxs-lookup"><span data-stu-id="349c2-148">To determine the contract lines that invoices must be created for, the job looks at invoice run dates for the contract lines.</span></span> <span data-ttu-id="349c2-149">如果属于一个合同的合同子项具有同一个发票运行日期，将把交易合并到一张具有两项发票明细的发票中。</span><span class="sxs-lookup"><span data-stu-id="349c2-149">If contract lines that belong to one contract have the same invoice run date, the transactions are combined into one invoice that has two invoice lines.</span></span> <span data-ttu-id="349c2-150">如果没有需要为其创建发票的交易，作业将跳过发票创建。</span><span class="sxs-lookup"><span data-stu-id="349c2-150">If there are no transactions to create invoices for, the job skips invoice creation.</span></span>

<span data-ttu-id="349c2-151">**ProcessRunner** 完成运行之后，将调用 **ProcessRunCaller**，提供结束时间，然后关闭。</span><span class="sxs-lookup"><span data-stu-id="349c2-151">After **ProcessRunner** has finished running, it calls **ProcessRunCaller**, provides the end time, and is closed.</span></span> <span data-ttu-id="349c2-152">然后，**ProcessRunCaller** 启动一个从指定结束日期开始运行 24 小时的计时器。</span><span class="sxs-lookup"><span data-stu-id="349c2-152">**ProcessRunCaller** then starts a timer that runs for 24 hours from the specified end time.</span></span> <span data-ttu-id="349c2-153">此计时器结束时，将关闭 **ProcessRunCaller**。</span><span class="sxs-lookup"><span data-stu-id="349c2-153">At the end of the timer, **ProcessRunCaller** is closed.</span></span>

<span data-ttu-id="349c2-154">用于创建发票的批处理作业是周期性作业。</span><span class="sxs-lookup"><span data-stu-id="349c2-154">The batch process job for creating invoices is a recurrent job.</span></span> <span data-ttu-id="349c2-155">如果多次运行此批处理流程，将创建多个作业实例，并导致出错。</span><span class="sxs-lookup"><span data-stu-id="349c2-155">If this batch process is run many times, multiple instances of the job are created and cause errors.</span></span> <span data-ttu-id="349c2-156">因此，仅应启动此批处理流程一次，并且仅当其停止运行时才应重新启动它。</span><span class="sxs-lookup"><span data-stu-id="349c2-156">Therefore, you should start the batch process only one time, and you should restart it only if it stops running.</span></span>

> [!NOTE]
> <span data-ttu-id="349c2-157">仅为按发票计划配置的项目合同子项运行批处理开票。</span><span class="sxs-lookup"><span data-stu-id="349c2-157">Batch invoicing only runs for project contract lines that are configured by invoice schedules.</span></span> <span data-ttu-id="349c2-158">必须为采用固定价格记帐方法的合同子项配置里程碑。</span><span class="sxs-lookup"><span data-stu-id="349c2-158">A contract line with a fixed price billing method must have milestones configured.</span></span> <span data-ttu-id="349c2-159">将需要为采用时间和材料记帐方法的项目合同子项设置基于日期的发票计划。</span><span class="sxs-lookup"><span data-stu-id="349c2-159">A project contract line with a time and material billing method will need a date-based invoice schedule set up.</span></span> <span data-ttu-id="349c2-160">这同样适用于基于项目的合同子项。</span><span class="sxs-lookup"><span data-stu-id="349c2-160">The same applies to a project-based contract line.</span></span>      
 
### <a name="edit-a-draft-invoice"></a><span data-ttu-id="349c2-161">编辑草稿发票</span><span class="sxs-lookup"><span data-stu-id="349c2-161">Edit a draft invoice</span></span>

<span data-ttu-id="349c2-162">创建项目草稿发票时，将把批准时间、支出和材料使用条目时创建的所有未记帐销售交易提取到该发票中。</span><span class="sxs-lookup"><span data-stu-id="349c2-162">When you create a draft project invoice, all unbilled sales transactions that were created when the time, expense, and material usage entries were approved are pulled onto the invoice.</span></span> <span data-ttu-id="349c2-163">可以在发票仍然处于草稿阶段时进行以下调整：</span><span class="sxs-lookup"><span data-stu-id="349c2-163">You can make the following adjustments while the invoice is still in a draft stage:</span></span>

- <span data-ttu-id="349c2-164">删除或编辑发票明细详细信息。</span><span class="sxs-lookup"><span data-stu-id="349c2-164">Delete or edit invoice line details.</span></span>
- <span data-ttu-id="349c2-165">编辑和调整数量和记帐类型。</span><span class="sxs-lookup"><span data-stu-id="349c2-165">Edit and adjust the quantity and billing type.</span></span>

<span data-ttu-id="349c2-166">选择 **确认** 以确认发票。</span><span class="sxs-lookup"><span data-stu-id="349c2-166">Select **Confirm** to confirm an invoice.</span></span> <span data-ttu-id="349c2-167">“确认”操作是单向操作。</span><span class="sxs-lookup"><span data-stu-id="349c2-167">The Confirm action is a one-way action.</span></span> <span data-ttu-id="349c2-168">选择 **确认** 时，系统将把发票设置为只读，并根据每项发票明细的每项发票明细详细信息创建已记帐实际销售额。</span><span class="sxs-lookup"><span data-stu-id="349c2-168">When you select **Confirm**, the system makes the invoice read-only and creates billed sales actuals from each invoice line detail for each invoice line.</span></span> <span data-ttu-id="349c2-169">如果发票明细详细信息引用未记帐实际销售额，系统还将冲销这个未记帐实际销售额。</span><span class="sxs-lookup"><span data-stu-id="349c2-169">If the invoice line detail references an unbilled sales actual, the system also reverses the unbilled sales actual.</span></span> <span data-ttu-id="349c2-170">（所有基于时间或支出条目创建的发票明细详细信息都将引用未记帐实际销售额。）总帐集成系统可以使用此项冲销来冲销项目的在制品 (WIP) 以达成会计目的。</span><span class="sxs-lookup"><span data-stu-id="349c2-170">(Any invoice line detail that was created from a time or expense entry will reference an unbilled sales actual.) General ledger integration systems can use this reversal to reverse project work in progress (WIP) for accounting purposes.</span></span>

### <a name="correct-a-confirmed-invoice"></a><span data-ttu-id="349c2-171">更正已确认的发票</span><span class="sxs-lookup"><span data-stu-id="349c2-171">Correct a confirmed invoice</span></span>

<span data-ttu-id="349c2-172">可以编辑（更正）已确认的发票。</span><span class="sxs-lookup"><span data-stu-id="349c2-172">Confirmed invoices can be edited (corrected).</span></span> <span data-ttu-id="349c2-173">更正已确认的发票时，将创建新的草稿纠正发票。</span><span class="sxs-lookup"><span data-stu-id="349c2-173">When you correct a confirmed invoice, a new draft corrective invoice is created.</span></span> <span data-ttu-id="349c2-174">因为假设您希望冲销原始发票中的所有交易和数量，所以此纠正发票中包含原始发票中的所有交易，并且其中的所有数量均为 0（零）。</span><span class="sxs-lookup"><span data-stu-id="349c2-174">Because the assumption is that you want to reverse all the transactions and quantities from the original invoice, this corrective invoice includes all the transactions from the original invoice, and all the quantities on it are 0 (zero).</span></span>

<span data-ttu-id="349c2-175">如果有任何交易不需要更正，可以将其从草稿纠正发票中删除。</span><span class="sxs-lookup"><span data-stu-id="349c2-175">If any transactions don't require correction, you can remove them from the draft corrective invoice.</span></span> <span data-ttu-id="349c2-176">如果要仅冲销或返回部分数量，可以编辑明细详细信息中的 **数量** 字段。</span><span class="sxs-lookup"><span data-stu-id="349c2-176">If you want to reverse or return only a partial quantity, you can edit the **Quantity** field on the line detail.</span></span> <span data-ttu-id="349c2-177">如果打开发票明细详细信息，可以看到原始发票数量。</span><span class="sxs-lookup"><span data-stu-id="349c2-177">If you open the invoice line detail, you can see the original invoice quantity.</span></span> <span data-ttu-id="349c2-178">然后可以编辑当前发票数量，使其比原始发票数量少或多。</span><span class="sxs-lookup"><span data-stu-id="349c2-178">You can then edit the current invoice quantity so that it's less than or more than the original invoice quantity.</span></span>

<span data-ttu-id="349c2-179">确认纠正发票时，将撤消原始已记帐实际销售额，并创建新的已记帐实际销售额。</span><span class="sxs-lookup"><span data-stu-id="349c2-179">When you confirm a corrective invoice, the original billed sales actual is reversed, and a new billed sales actual is created.</span></span> <span data-ttu-id="349c2-180">如果减少了数量，差额将导致也创建一项新的未记帐实际销售额。</span><span class="sxs-lookup"><span data-stu-id="349c2-180">If the quantity was reduced, the difference will cause a new unbilled sales actual to be created too.</span></span> <span data-ttu-id="349c2-181">例如，如果原始已记帐销售额是八小时的，并且纠正发票明细详细信息的减少后数量为六小时，将冲销原始已记帐销售明细，并创建两项新的实际值：</span><span class="sxs-lookup"><span data-stu-id="349c2-181">For example, if the original billed sale was for eight hours, and the corrective invoice line detail has a reduced quantity of six hours, the original billed sales line is reversed and two new actuals are created:</span></span>

- <span data-ttu-id="349c2-182">六小时的已记帐实际销售额。</span><span class="sxs-lookup"><span data-stu-id="349c2-182">A billed sales actual for six hours.</span></span>
- <span data-ttu-id="349c2-183">其余两小时的未记帐实际销售额。</span><span class="sxs-lookup"><span data-stu-id="349c2-183">An unbilled sales actual for the remaining two hours.</span></span> <span data-ttu-id="349c2-184">以后可为此交易记帐或标记为非应计费，具体取决于与客户的协商结果。</span><span class="sxs-lookup"><span data-stu-id="349c2-184">This transaction can either be billed later or marked as non-chargeable, depending on the negotiations with the customer.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
