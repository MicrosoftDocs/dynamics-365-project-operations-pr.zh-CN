---
title: 实际值概述
description: 本主题提供有关项目实际值的信息。
author: rumant
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 08/03/2020
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 63ad6544f0ec0a893aebd8d81f3ee895e51c294e
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/10/2021
ms.locfileid: "5146112"
---
# <a name="actuals-overview"></a><span data-ttu-id="c2bcc-103">实际值概述</span><span class="sxs-lookup"><span data-stu-id="c2bcc-103">Actuals overview</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="c2bcc-104">实际值是已完成的项目工作量。</span><span class="sxs-lookup"><span data-stu-id="c2bcc-104">Actuals are the amount of work that has been completed on a project.</span></span> <span data-ttu-id="c2bcc-105">可将项目实际值回溯到其源文档。</span><span class="sxs-lookup"><span data-stu-id="c2bcc-105">Project actuals can be traced back to their source documents.</span></span> <span data-ttu-id="c2bcc-106">这些源文档包括时间、支出和日记帐条目，以及发票。</span><span class="sxs-lookup"><span data-stu-id="c2bcc-106">Those source documents include time, expense, and journal entries, and also invoices.</span></span>

![如何将项目实际值跟踪到源文档](media/basic-guide-18.png)

## <a name="submitting-a-time-entry"></a><span data-ttu-id="c2bcc-108">提交时间条目</span><span class="sxs-lookup"><span data-stu-id="c2bcc-108">Submitting a time entry</span></span>

<span data-ttu-id="c2bcc-109">在 PSA 中，为映射到时间和材料合同子项的项目提交时间条目时，将创建两个日记帐行。</span><span class="sxs-lookup"><span data-stu-id="c2bcc-109">In PSA, when a time entry is submitted for a project that is mapped to a time-and-materials contract line, two journal lines are created.</span></span> <span data-ttu-id="c2bcc-110">一行针对成本，另一行针对未记帐销售。</span><span class="sxs-lookup"><span data-stu-id="c2bcc-110">One line is for cost, and the other line is for unbilled sales.</span></span> <span data-ttu-id="c2bcc-111">为映射到固定价格合同子项的项目提交时间条目时，仅为成本创建一个日记帐行。</span><span class="sxs-lookup"><span data-stu-id="c2bcc-111">When a time entry is submitted for a project that is mapped to a fixed-price contract line, a journal line is created only for cost.</span></span> 

<span data-ttu-id="c2bcc-112">有关输入默认价格的逻辑在日记帐行中。</span><span class="sxs-lookup"><span data-stu-id="c2bcc-112">Logic for entering default prices resides on the journal line.</span></span> <span data-ttu-id="c2bcc-113">时间条目中的所有字段值将复制到该日记帐行中。</span><span class="sxs-lookup"><span data-stu-id="c2bcc-113">All the field values from a time entry are copied to the journal line.</span></span> <span data-ttu-id="c2bcc-114">这些字段中包含交易日期、项目映射到的合同子项，以及相应价目表中的货币结果。</span><span class="sxs-lookup"><span data-stu-id="c2bcc-114">These fields include the date of the transaction, the contract line that the project is mapped to, and the currency result in the appropriate price list.</span></span> 

<span data-ttu-id="c2bcc-115">会影响默认价格的字段（如 **角色** 和 **部门**）会导致默认在日记帐行中输入相应价格。</span><span class="sxs-lookup"><span data-stu-id="c2bcc-115">The fields that affect default prices, such as **Role** and **Org Unit**, cause an appropriate price to be entered by default on the journal line.</span></span> <span data-ttu-id="c2bcc-116">如果在时间条目中添加自定义字段，并且希望将字段值传播到实际值，请在实际值条目中创建字段，然后使用字段映射将该字段从时间条目复制到实际值。</span><span class="sxs-lookup"><span data-stu-id="c2bcc-116">If you add a custom field on the time entry, and you want the field value to be propagated to actuals, create the field on the Actuals entity, and use field mappings to copy the field from the time entry to the actual.</span></span>

## <a name="submitting-an-expense-entry"></a><span data-ttu-id="c2bcc-117">提交支出条目</span><span class="sxs-lookup"><span data-stu-id="c2bcc-117">Submitting an expense entry</span></span>

<span data-ttu-id="c2bcc-118">在 PSA 中，为映射到时间和材料合同子项的项目提交支出条目时，将创建两个日记帐行。</span><span class="sxs-lookup"><span data-stu-id="c2bcc-118">In PSA, when an expense entry is submitted for a project that is mapped to a time-and-materials contract line, two journal lines are created.</span></span> <span data-ttu-id="c2bcc-119">一行针对成本，另一行针对未记帐销售。</span><span class="sxs-lookup"><span data-stu-id="c2bcc-119">One line is for cost, and the other line is for unbilled sales.</span></span> <span data-ttu-id="c2bcc-120">为映射到固定价格合同子项的项目提交支出条目时，仅为成本创建一个日记帐行。</span><span class="sxs-lookup"><span data-stu-id="c2bcc-120">When an expense entry is submitted for a project that is mapped to a fixed-price contract line, a journal line is created only for cost.</span></span>

<span data-ttu-id="c2bcc-121">用于输入支出的默认价格的逻辑基于在 **支出条目** 页中选择的支出类别。</span><span class="sxs-lookup"><span data-stu-id="c2bcc-121">Logic for entering default prices for expenses is based on the expense category that is selected on the **Expense entry** page.</span></span> <span data-ttu-id="c2bcc-122">交易日期、项目映射到的合同子项，以及货币全部用于确定相应价目表。</span><span class="sxs-lookup"><span data-stu-id="c2bcc-122">The transaction date, the contract line that the project is mapped to, and the currency are all used to determine the appropriate price list.</span></span> <span data-ttu-id="c2bcc-123">但是，对于价格本身，默认情况下将直接在成本和销售额的相关支出日记帐行中设置用户输入的金额。</span><span class="sxs-lookup"><span data-stu-id="c2bcc-123">However, for the price itself, the amount that the user entered is set directly on the related expense journal lines for cost and sales by default.</span></span>

<span data-ttu-id="c2bcc-124">在当前 PSA 版本中，不能在支出条目中基于类别录入默认单价。</span><span class="sxs-lookup"><span data-stu-id="c2bcc-124">In the current version of PSA, category-based entry of per-unit default prices on expense entries isn't available.</span></span>

## <a name="using-entry-journals-to-record-costs"></a><span data-ttu-id="c2bcc-125">使用条目日记帐记录成本</span><span class="sxs-lookup"><span data-stu-id="c2bcc-125">Using Entry journals to record costs</span></span>

<span data-ttu-id="c2bcc-126">在 PSA 中，可使用条目日记帐记录材料、费用、时间、支出或税务交易分类的成本或收入。</span><span class="sxs-lookup"><span data-stu-id="c2bcc-126">In PSA, Entry journals let you record the cost or revenue in the material, fee, time, expense, or tax transaction classes.</span></span> <span data-ttu-id="c2bcc-127">日记帐有标题、行和 **确认** 操作。</span><span class="sxs-lookup"><span data-stu-id="c2bcc-127">A journal has a header, lines, and a **Confirm** action.</span></span> <span data-ttu-id="c2bcc-128">下面是一些可能需要使用日记帐的场景：</span><span class="sxs-lookup"><span data-stu-id="c2bcc-128">Here are some scenarios where you might use a journal:</span></span>

- <span data-ttu-id="c2bcc-129">必须记录项目的材料实际成本和销售额。</span><span class="sxs-lookup"><span data-stu-id="c2bcc-129">You must record material actual costs and sales on a project.</span></span>
- <span data-ttu-id="c2bcc-130">必须将交易实际值从另一个系统移到 PSA。</span><span class="sxs-lookup"><span data-stu-id="c2bcc-130">You must move transaction actuals from another system to PSA.</span></span>
- <span data-ttu-id="c2bcc-131">必须记录另一个系统中出现的成本，如采购成本或分包成本。</span><span class="sxs-lookup"><span data-stu-id="c2bcc-131">You must record costs that occurred in another system, such as procurement or subcontracting costs.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="c2bcc-132">用户只有完全了解“实际值”对项目会计的影响，才能使用条目日记帐创建实际值。</span><span class="sxs-lookup"><span data-stu-id="c2bcc-132">Using Entry journals to create actuals should be done only by a user who is fully aware of the accounting impact the Actuals have on the project.</span></span> <span data-ttu-id="c2bcc-133">这是因为此应用程序不会验证日记帐行类型，也不会验证在日记帐行上输入的相关定价。</span><span class="sxs-lookup"><span data-stu-id="c2bcc-133">This is because the application does not validate the journal line type, or the related pricing that is entered on the journal line.</span></span> <span data-ttu-id="c2bcc-134">由于此日记帐类型会造成一定的影响，因此，对于谁有权创建条目日记帐，应该十分谨慎。</span><span class="sxs-lookup"><span data-stu-id="c2bcc-134">Because of the impact of this journal type, exercise adequate caution in who is given access to create Entry journals.</span></span>     


## <a name="recording-actuals-based-on-project-events"></a><span data-ttu-id="c2bcc-135">基于项目事件记录实际值</span><span class="sxs-lookup"><span data-stu-id="c2bcc-135">Recording actuals based on project events</span></span>

<span data-ttu-id="c2bcc-136">PSA 记录项目期间发生的财务交易。</span><span class="sxs-lookup"><span data-stu-id="c2bcc-136">PSA records the financial transactions that occur during a project.</span></span> <span data-ttu-id="c2bcc-137">这些交易记录为 **实际值**。</span><span class="sxs-lookup"><span data-stu-id="c2bcc-137">These transactions are recorded as **actuals**.</span></span> <span data-ttu-id="c2bcc-138">下表显示创建的不同类型的实际值，具体取决于项目是时间和材料还是固定价格，是否处于售前阶段，是否为内部项目。</span><span class="sxs-lookup"><span data-stu-id="c2bcc-138">The following tables show the different types of actuals that are created, depending on whether the project is a time-and-materials or fixed-price project, is in the presales stage, or is an internal project.</span></span>

<span data-ttu-id="c2bcc-139">**资源与项目的合同签订部门属于同一个部门**</span><span class="sxs-lookup"><span data-stu-id="c2bcc-139">**The resource belongs to same organizational unit as the project's contracting unit**</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="c2bcc-140">事件</span><span class="sxs-lookup"><span data-stu-id="c2bcc-140">Event</span></span></th>
<th colspan="4"><span data-ttu-id="c2bcc-141">可记帐项目或已售项目</span><span class="sxs-lookup"><span data-stu-id="c2bcc-141">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="c2bcc-142">售前阶段的项目</span><span class="sxs-lookup"><span data-stu-id="c2bcc-142">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="c2bcc-143">内部项目</span><span class="sxs-lookup"><span data-stu-id="c2bcc-143">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="c2bcc-144">时间和材料</span><span class="sxs-lookup"><span data-stu-id="c2bcc-144">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="c2bcc-145">固定价格</span><span class="sxs-lookup"><span data-stu-id="c2bcc-145">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="c2bcc-146">实际</span><span class="sxs-lookup"><span data-stu-id="c2bcc-146">Actuals</span></span></th>
<th><span data-ttu-id="c2bcc-147">交易货币</span><span class="sxs-lookup"><span data-stu-id="c2bcc-147">Transaction currency</span></span></th>
<th><span data-ttu-id="c2bcc-148">固定价格</span><span class="sxs-lookup"><span data-stu-id="c2bcc-148">Fixed price</span></span></th>
<th><span data-ttu-id="c2bcc-149">交易货币</span><span class="sxs-lookup"><span data-stu-id="c2bcc-149">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="c2bcc-150">创建时间条目。</span><span class="sxs-lookup"><span data-stu-id="c2bcc-150">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="c2bcc-151">实际值条目中无活动</span><span class="sxs-lookup"><span data-stu-id="c2bcc-151">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c2bcc-152">提交时间条目。</span><span class="sxs-lookup"><span data-stu-id="c2bcc-152">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="c2bcc-153">实际值条目中无活动</span><span class="sxs-lookup"><span data-stu-id="c2bcc-153">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="c2bcc-154">批准时间，并且审批期间可记帐工时不变或不增加。</span><span class="sxs-lookup"><span data-stu-id="c2bcc-154">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="c2bcc-155">成本实际值</span><span class="sxs-lookup"><span data-stu-id="c2bcc-155">Cost actual</span></span></td>
<td><span data-ttu-id="c2bcc-156">合同签订部门货币</span><span class="sxs-lookup"><span data-stu-id="c2bcc-156">Contracting unit currency</span></span></td>
<td rowspan="2"><span data-ttu-id="c2bcc-157">实际成本</span><span class="sxs-lookup"><span data-stu-id="c2bcc-157">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="c2bcc-158">合同签订部门货币</span><span class="sxs-lookup"><span data-stu-id="c2bcc-158">Contracting unit currency</span></span>
<td rowspan="2"><span data-ttu-id="c2bcc-159">成本实际值</span><span class="sxs-lookup"><span data-stu-id="c2bcc-159">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="c2bcc-160">成本实际值</span><span class="sxs-lookup"><span data-stu-id="c2bcc-160">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c2bcc-161">未记帐实际销售额 – 应计费</span><span class="sxs-lookup"><span data-stu-id="c2bcc-161">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="c2bcc-162">项目合同货币</span><span class="sxs-lookup"><span data-stu-id="c2bcc-162">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="c2bcc-163">批准时间，并且审批期间可记帐工时不变或不减少。</span><span class="sxs-lookup"><span data-stu-id="c2bcc-163">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="c2bcc-164">实际成本</span><span class="sxs-lookup"><span data-stu-id="c2bcc-164">Cost actual</span></span></td>
<td><span data-ttu-id="c2bcc-165">合同签订部门货币</span><span class="sxs-lookup"><span data-stu-id="c2bcc-165">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="c2bcc-166">实际成本</span><span class="sxs-lookup"><span data-stu-id="c2bcc-166">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="c2bcc-167">合同签订部门货币</span><span class="sxs-lookup"><span data-stu-id="c2bcc-167">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="c2bcc-168">实际成本</span><span class="sxs-lookup"><span data-stu-id="c2bcc-168">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="c2bcc-169">实际成本</span><span class="sxs-lookup"><span data-stu-id="c2bcc-169">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c2bcc-170">未记帐实际销售额 – 新数量的应计值</span><span class="sxs-lookup"><span data-stu-id="c2bcc-170">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="c2bcc-171">项目合同货币</span><span class="sxs-lookup"><span data-stu-id="c2bcc-171">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c2bcc-172">未记帐实际销售额 – 差额的非应计值</span><span class="sxs-lookup"><span data-stu-id="c2bcc-172">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="c2bcc-173">项目合同货币</span><span class="sxs-lookup"><span data-stu-id="c2bcc-173">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="c2bcc-174">确认发票，并且审批期间可记帐工时不变或不增加。</span><span class="sxs-lookup"><span data-stu-id="c2bcc-174">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="c2bcc-175">未记帐销售额冲销</span><span class="sxs-lookup"><span data-stu-id="c2bcc-175">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="c2bcc-176">项目合同货币</span><span class="sxs-lookup"><span data-stu-id="c2bcc-176">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="c2bcc-177">里程碑的已记帐销售额</span><span class="sxs-lookup"><span data-stu-id="c2bcc-177">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="c2bcc-178">项目合同货币</span><span class="sxs-lookup"><span data-stu-id="c2bcc-178">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="c2bcc-179">不适用</span><span class="sxs-lookup"><span data-stu-id="c2bcc-179">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="c2bcc-180">不适用</span><span class="sxs-lookup"><span data-stu-id="c2bcc-180">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c2bcc-181">已记帐销售额</span><span class="sxs-lookup"><span data-stu-id="c2bcc-181">Billed sales</span></span></td>
<td><span data-ttu-id="c2bcc-182">项目合同货币</span><span class="sxs-lookup"><span data-stu-id="c2bcc-182">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="c2bcc-183">确认发票，并且可记帐工时减少。</span><span class="sxs-lookup"><span data-stu-id="c2bcc-183">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="c2bcc-184">未记帐销售额冲销</span><span class="sxs-lookup"><span data-stu-id="c2bcc-184">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="c2bcc-185">项目合同货币</span><span class="sxs-lookup"><span data-stu-id="c2bcc-185">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="c2bcc-186">不适用</span><span class="sxs-lookup"><span data-stu-id="c2bcc-186">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="c2bcc-187">不适用</span><span class="sxs-lookup"><span data-stu-id="c2bcc-187">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="c2bcc-188">不适用</span><span class="sxs-lookup"><span data-stu-id="c2bcc-188">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="c2bcc-189">不适用</span><span class="sxs-lookup"><span data-stu-id="c2bcc-189">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c2bcc-190">已记帐销售额 – 新数量的应计值</span><span class="sxs-lookup"><span data-stu-id="c2bcc-190">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="c2bcc-191">项目合同货币</span><span class="sxs-lookup"><span data-stu-id="c2bcc-191">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c2bcc-192">已记帐实际销售额 – 差额的非应计值</span><span class="sxs-lookup"><span data-stu-id="c2bcc-192">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="c2bcc-193">项目合同货币</span><span class="sxs-lookup"><span data-stu-id="c2bcc-193">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="c2bcc-194">更正发票以增加应计费数量。</span><span class="sxs-lookup"><span data-stu-id="c2bcc-194">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="c2bcc-195">已记帐销售额 - 冲销</span><span class="sxs-lookup"><span data-stu-id="c2bcc-195">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="c2bcc-196">项目合同货币</span><span class="sxs-lookup"><span data-stu-id="c2bcc-196">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="c2bcc-197">里程碑的已记帐销售额冲销</span><span class="sxs-lookup"><span data-stu-id="c2bcc-197">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="c2bcc-198">里程碑状态从<strong>已开票</strong>更改为<strong>准备好开票</strong></span><span class="sxs-lookup"><span data-stu-id="c2bcc-198">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="c2bcc-199">项目合同货币</span><span class="sxs-lookup"><span data-stu-id="c2bcc-199">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="c2bcc-200">不适用</span><span class="sxs-lookup"><span data-stu-id="c2bcc-200">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="c2bcc-201">不适用</span><span class="sxs-lookup"><span data-stu-id="c2bcc-201">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c2bcc-202">已记帐销售额</span><span class="sxs-lookup"><span data-stu-id="c2bcc-202">Billed sales</span></span></td>
<td><span data-ttu-id="c2bcc-203">项目合同货币</span><span class="sxs-lookup"><span data-stu-id="c2bcc-203">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="c2bcc-204">更正发票以减少应计费数量。</span><span class="sxs-lookup"><span data-stu-id="c2bcc-204">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="c2bcc-205">已记帐销售额 - 冲销</span><span class="sxs-lookup"><span data-stu-id="c2bcc-205">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="c2bcc-206">项目合同货币</span><span class="sxs-lookup"><span data-stu-id="c2bcc-206">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c2bcc-207">新数量的已记帐销售额</span><span class="sxs-lookup"><span data-stu-id="c2bcc-207">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="c2bcc-208">项目合同货币</span><span class="sxs-lookup"><span data-stu-id="c2bcc-208">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c2bcc-209">未记帐销售额 – 差额的应计值</span><span class="sxs-lookup"><span data-stu-id="c2bcc-209">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="c2bcc-210">项目合同货币</span><span class="sxs-lookup"><span data-stu-id="c2bcc-210">Project contract currency</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="c2bcc-211">**资源与项目的合同签订部门不属于同一个部门**</span><span class="sxs-lookup"><span data-stu-id="c2bcc-211">**The resource belongs to an organizational unit that differs from the project's contracting unit**</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="c2bcc-212">事件</span><span class="sxs-lookup"><span data-stu-id="c2bcc-212">Event</span></span></th>
<th colspan="4"><span data-ttu-id="c2bcc-213">可记帐项目或已售项目</span><span class="sxs-lookup"><span data-stu-id="c2bcc-213">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="c2bcc-214">售前阶段的项目</span><span class="sxs-lookup"><span data-stu-id="c2bcc-214">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="c2bcc-215">内部项目</span><span class="sxs-lookup"><span data-stu-id="c2bcc-215">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="c2bcc-216">时间和材料</span><span class="sxs-lookup"><span data-stu-id="c2bcc-216">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="c2bcc-217">固定价格</span><span class="sxs-lookup"><span data-stu-id="c2bcc-217">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="c2bcc-218">实际</span><span class="sxs-lookup"><span data-stu-id="c2bcc-218">Actuals</span></span></th>
<th><span data-ttu-id="c2bcc-219">交易货币</span><span class="sxs-lookup"><span data-stu-id="c2bcc-219">Transaction currency</span></span></th>
<th><span data-ttu-id="c2bcc-220">固定价格</span><span class="sxs-lookup"><span data-stu-id="c2bcc-220">Fixed price</span></span></th>
<th><span data-ttu-id="c2bcc-221">交易货币</span><span class="sxs-lookup"><span data-stu-id="c2bcc-221">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="c2bcc-222">创建时间条目。</span><span class="sxs-lookup"><span data-stu-id="c2bcc-222">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="c2bcc-223">实际值条目中无活动</span><span class="sxs-lookup"><span data-stu-id="c2bcc-223">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c2bcc-224">提交时间条目。</span><span class="sxs-lookup"><span data-stu-id="c2bcc-224">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="c2bcc-225">实际值条目中无活动</span><span class="sxs-lookup"><span data-stu-id="c2bcc-225">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="4"><span data-ttu-id="c2bcc-226">批准时间，并且审批期间可记帐工时不变或不增加。</span><span class="sxs-lookup"><span data-stu-id="c2bcc-226">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="c2bcc-227">成本实际值</span><span class="sxs-lookup"><span data-stu-id="c2bcc-227">Cost actual</span></span></td>
<td><span data-ttu-id="c2bcc-228">合同签订部门货币</span><span class="sxs-lookup"><span data-stu-id="c2bcc-228">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="c2bcc-229">实际成本</span><span class="sxs-lookup"><span data-stu-id="c2bcc-229">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="c2bcc-230">合同签订部门货币</span><span class="sxs-lookup"><span data-stu-id="c2bcc-230">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="c2bcc-231">成本实际值</span><span class="sxs-lookup"><span data-stu-id="c2bcc-231">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="c2bcc-232">成本实际值</span><span class="sxs-lookup"><span data-stu-id="c2bcc-232">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c2bcc-233">未记帐实际销售额 – 应计费</span><span class="sxs-lookup"><span data-stu-id="c2bcc-233">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="c2bcc-234">项目合同货币</span><span class="sxs-lookup"><span data-stu-id="c2bcc-234">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c2bcc-235">资源单位成本</span><span class="sxs-lookup"><span data-stu-id="c2bcc-235">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="c2bcc-236">资源单位货币</span><span class="sxs-lookup"><span data-stu-id="c2bcc-236">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c2bcc-237">组织间销售</span><span class="sxs-lookup"><span data-stu-id="c2bcc-237">Interorganizational sales</span></span></td>
<td><span data-ttu-id="c2bcc-238">合同签订部门货币</span><span class="sxs-lookup"><span data-stu-id="c2bcc-238">Contracting unit currency</span></span></td>
</tr>
<tr>
<td rowspan="5"><span data-ttu-id="c2bcc-239">批准时间，并且审批期间可记帐工时不变或不减少。</span><span class="sxs-lookup"><span data-stu-id="c2bcc-239">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="c2bcc-240">实际成本</span><span class="sxs-lookup"><span data-stu-id="c2bcc-240">Cost actual</span></span></td>
<td><span data-ttu-id="c2bcc-241">合同签订部门货币</span><span class="sxs-lookup"><span data-stu-id="c2bcc-241">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="c2bcc-242">实际成本</span><span class="sxs-lookup"><span data-stu-id="c2bcc-242">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="c2bcc-243">合同签订部门货币</span><span class="sxs-lookup"><span data-stu-id="c2bcc-243">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="c2bcc-244">实际成本</span><span class="sxs-lookup"><span data-stu-id="c2bcc-244">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="c2bcc-245">实际成本</span><span class="sxs-lookup"><span data-stu-id="c2bcc-245">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c2bcc-246">资源单位成本</span><span class="sxs-lookup"><span data-stu-id="c2bcc-246">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="c2bcc-247">资源单位货币</span><span class="sxs-lookup"><span data-stu-id="c2bcc-247">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c2bcc-248">组织间销售</span><span class="sxs-lookup"><span data-stu-id="c2bcc-248">Interorganizational sales</span></span></td>
<td><span data-ttu-id="c2bcc-249">合同签订部门货币</span><span class="sxs-lookup"><span data-stu-id="c2bcc-249">Contracting unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c2bcc-250">未记帐实际销售额 – 新数量的应计值</span><span class="sxs-lookup"><span data-stu-id="c2bcc-250">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="c2bcc-251">项目合同货币</span><span class="sxs-lookup"><span data-stu-id="c2bcc-251">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c2bcc-252">未记帐实际销售额 – 差额的非应计值</span><span class="sxs-lookup"><span data-stu-id="c2bcc-252">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="c2bcc-253">项目合同货币</span><span class="sxs-lookup"><span data-stu-id="c2bcc-253">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="c2bcc-254">确认发票，并且审批期间可记帐工时不变或不增加。</span><span class="sxs-lookup"><span data-stu-id="c2bcc-254">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="c2bcc-255">未记帐销售额冲销</span><span class="sxs-lookup"><span data-stu-id="c2bcc-255">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="c2bcc-256">项目合同货币</span><span class="sxs-lookup"><span data-stu-id="c2bcc-256">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="c2bcc-257">里程碑的已记帐销售额</span><span class="sxs-lookup"><span data-stu-id="c2bcc-257">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="c2bcc-258">项目合同货币</span><span class="sxs-lookup"><span data-stu-id="c2bcc-258">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="c2bcc-259">不适用</span><span class="sxs-lookup"><span data-stu-id="c2bcc-259">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="c2bcc-260">不适用</span><span class="sxs-lookup"><span data-stu-id="c2bcc-260">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c2bcc-261">已记帐销售额</span><span class="sxs-lookup"><span data-stu-id="c2bcc-261">Billed sales</span></span></td>
<td><span data-ttu-id="c2bcc-262">项目合同货币</span><span class="sxs-lookup"><span data-stu-id="c2bcc-262">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="c2bcc-263">确认发票，并且可记帐工时减少。</span><span class="sxs-lookup"><span data-stu-id="c2bcc-263">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="c2bcc-264">未记帐销售额冲销</span><span class="sxs-lookup"><span data-stu-id="c2bcc-264">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="c2bcc-265">项目合同货币</span><span class="sxs-lookup"><span data-stu-id="c2bcc-265">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="c2bcc-266">不适用</span><span class="sxs-lookup"><span data-stu-id="c2bcc-266">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="c2bcc-267">不适用</span><span class="sxs-lookup"><span data-stu-id="c2bcc-267">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="c2bcc-268">不适用</span><span class="sxs-lookup"><span data-stu-id="c2bcc-268">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="c2bcc-269">不适用</span><span class="sxs-lookup"><span data-stu-id="c2bcc-269">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c2bcc-270">已记帐销售额 – 新数量的应计值</span><span class="sxs-lookup"><span data-stu-id="c2bcc-270">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="c2bcc-271">项目合同货币</span><span class="sxs-lookup"><span data-stu-id="c2bcc-271">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c2bcc-272">已记帐实际销售额 – 差额的非应计值</span><span class="sxs-lookup"><span data-stu-id="c2bcc-272">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="c2bcc-273">项目合同货币</span><span class="sxs-lookup"><span data-stu-id="c2bcc-273">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="c2bcc-274">更正发票以增加应计费数量。</span><span class="sxs-lookup"><span data-stu-id="c2bcc-274">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="c2bcc-275">已记帐销售额 - 冲销</span><span class="sxs-lookup"><span data-stu-id="c2bcc-275">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="c2bcc-276">项目合同货币</span><span class="sxs-lookup"><span data-stu-id="c2bcc-276">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="c2bcc-277">里程碑的已记帐销售额冲销</span><span class="sxs-lookup"><span data-stu-id="c2bcc-277">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="c2bcc-278">里程碑状态从<strong>已开票</strong>更改为<strong>准备好开票</strong></span><span class="sxs-lookup"><span data-stu-id="c2bcc-278">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="c2bcc-279">项目合同货币</span><span class="sxs-lookup"><span data-stu-id="c2bcc-279">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="c2bcc-280">不适用</span><span class="sxs-lookup"><span data-stu-id="c2bcc-280">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="c2bcc-281">不适用</span><span class="sxs-lookup"><span data-stu-id="c2bcc-281">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c2bcc-282">已记帐销售额</span><span class="sxs-lookup"><span data-stu-id="c2bcc-282">Billed sales</span></span></td>
<td><span data-ttu-id="c2bcc-283">项目合同货币</span><span class="sxs-lookup"><span data-stu-id="c2bcc-283">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="c2bcc-284">更正发票以减少应计费数量。</span><span class="sxs-lookup"><span data-stu-id="c2bcc-284">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="c2bcc-285">已记帐销售额 - 冲销</span><span class="sxs-lookup"><span data-stu-id="c2bcc-285">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="c2bcc-286">项目合同货币</span><span class="sxs-lookup"><span data-stu-id="c2bcc-286">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c2bcc-287">新数量的已记帐销售额</span><span class="sxs-lookup"><span data-stu-id="c2bcc-287">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="c2bcc-288">项目合同货币</span><span class="sxs-lookup"><span data-stu-id="c2bcc-288">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c2bcc-289">未记帐销售额 – 差额的应计值</span><span class="sxs-lookup"><span data-stu-id="c2bcc-289">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="c2bcc-290">项目合同货币</span><span class="sxs-lookup"><span data-stu-id="c2bcc-290">Project contract currency</span></span></td>
</tr>
</tbody>
</table>
