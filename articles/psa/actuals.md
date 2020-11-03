---
title: 实际值概述
description: 本主题提供有关项目实际值的信息。
author: rumant
manager: kfend
ms.service: dynamics-365-customerservice
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
ms.openlocfilehash: 9559cb2dcc38cb8058c5a9a3b97a35019fea486f
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/16/2020
ms.locfileid: "4072802"
---
# <a name="actuals-overview"></a><span data-ttu-id="0bc60-103">实际值概述</span><span class="sxs-lookup"><span data-stu-id="0bc60-103">Actuals overview</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="0bc60-104">实际值是已完成的项目工作量。</span><span class="sxs-lookup"><span data-stu-id="0bc60-104">Actuals are the amount of work that has been completed on a project.</span></span> <span data-ttu-id="0bc60-105">可将项目实际值回溯到其源文档。</span><span class="sxs-lookup"><span data-stu-id="0bc60-105">Project actuals can be traced back to their source documents.</span></span> <span data-ttu-id="0bc60-106">这些源文档包括时间、支出和日记帐条目，以及发票。</span><span class="sxs-lookup"><span data-stu-id="0bc60-106">Those source documents include time, expense, and journal entries, and also invoices.</span></span>

![如何将项目实际值跟踪到源文档](media/basic-guide-18.png)

## <a name="submitting-a-time-entry"></a><span data-ttu-id="0bc60-108">提交时间条目</span><span class="sxs-lookup"><span data-stu-id="0bc60-108">Submitting a time entry</span></span>

<span data-ttu-id="0bc60-109">在 PSA 中，为映射到时间和材料合同子项的项目提交时间条目时，将创建两个日记帐行。</span><span class="sxs-lookup"><span data-stu-id="0bc60-109">In PSA, when a time entry is submitted for a project that is mapped to a time-and-materials contract line, two journal lines are created.</span></span> <span data-ttu-id="0bc60-110">一行针对成本，另一行针对未记帐销售。</span><span class="sxs-lookup"><span data-stu-id="0bc60-110">One line is for cost, and the other line is for unbilled sales.</span></span> <span data-ttu-id="0bc60-111">为映射到固定价格合同子项的项目提交时间条目时，仅为成本创建一个日记帐行。</span><span class="sxs-lookup"><span data-stu-id="0bc60-111">When a time entry is submitted for a project that is mapped to a fixed-price contract line, a journal line is created only for cost.</span></span> 

<span data-ttu-id="0bc60-112">有关输入默认价格的逻辑在日记帐行中。</span><span class="sxs-lookup"><span data-stu-id="0bc60-112">Logic for entering default prices resides on the journal line.</span></span> <span data-ttu-id="0bc60-113">时间条目中的所有字段值将复制到该日记帐行中。</span><span class="sxs-lookup"><span data-stu-id="0bc60-113">All the field values from a time entry are copied to the journal line.</span></span> <span data-ttu-id="0bc60-114">这些字段中包含交易日期、项目映射到的合同子项，以及相应价目表中的货币结果。</span><span class="sxs-lookup"><span data-stu-id="0bc60-114">These fields include the date of the transaction, the contract line that the project is mapped to, and the currency result in the appropriate price list.</span></span> 

<span data-ttu-id="0bc60-115">会影响默认价格的字段（如 **角色** 和 **部门** ）会导致默认在日记帐行中输入相应价格。</span><span class="sxs-lookup"><span data-stu-id="0bc60-115">The fields that affect default prices, such as **Role** and **Org Unit** , cause an appropriate price to be entered by default on the journal line.</span></span> <span data-ttu-id="0bc60-116">如果在时间条目中添加自定义字段，并且希望将字段值传播到实际值，请在实际值条目中创建字段，然后使用字段映射将该字段从时间条目复制到实际值。</span><span class="sxs-lookup"><span data-stu-id="0bc60-116">If you add a custom field on the time entry, and you want the field value to be propagated to actuals, create the field on the Actuals entity, and use field mappings to copy the field from the time entry to the actual.</span></span>

## <a name="submitting-an-expense-entry"></a><span data-ttu-id="0bc60-117">提交支出条目</span><span class="sxs-lookup"><span data-stu-id="0bc60-117">Submitting an expense entry</span></span>

<span data-ttu-id="0bc60-118">在 PSA 中，为映射到时间和材料合同子项的项目提交支出条目时，将创建两个日记帐行。</span><span class="sxs-lookup"><span data-stu-id="0bc60-118">In PSA, when an expense entry is submitted for a project that is mapped to a time-and-materials contract line, two journal lines are created.</span></span> <span data-ttu-id="0bc60-119">一行针对成本，另一行针对未记帐销售。</span><span class="sxs-lookup"><span data-stu-id="0bc60-119">One line is for cost, and the other line is for unbilled sales.</span></span> <span data-ttu-id="0bc60-120">为映射到固定价格合同子项的项目提交支出条目时，仅为成本创建一个日记帐行。</span><span class="sxs-lookup"><span data-stu-id="0bc60-120">When an expense entry is submitted for a project that is mapped to a fixed-price contract line, a journal line is created only for cost.</span></span>

<span data-ttu-id="0bc60-121">用于输入支出的默认价格的逻辑基于在 **支出条目** 页中选择的支出类别。</span><span class="sxs-lookup"><span data-stu-id="0bc60-121">Logic for entering default prices for expenses is based on the expense category that is selected on the **Expense entry** page.</span></span> <span data-ttu-id="0bc60-122">交易日期、项目映射到的合同子项，以及货币全部用于确定相应价目表。</span><span class="sxs-lookup"><span data-stu-id="0bc60-122">The transaction date, the contract line that the project is mapped to, and the currency are all used to determine the appropriate price list.</span></span> <span data-ttu-id="0bc60-123">但是，对于价格本身，默认情况下将直接在成本和销售额的相关支出日记帐行中设置用户输入的金额。</span><span class="sxs-lookup"><span data-stu-id="0bc60-123">However, for the price itself, the amount that the user entered is set directly on the related expense journal lines for cost and sales by default.</span></span>

<span data-ttu-id="0bc60-124">在当前 PSA 版本中，不能在支出条目中基于类别录入默认单价。</span><span class="sxs-lookup"><span data-stu-id="0bc60-124">In the current version of PSA, category-based entry of per-unit default prices on expense entries isn't available.</span></span>

## <a name="using-entry-journals-to-record-costs"></a><span data-ttu-id="0bc60-125">使用条目日记帐记录成本</span><span class="sxs-lookup"><span data-stu-id="0bc60-125">Using Entry journals to record costs</span></span>

<span data-ttu-id="0bc60-126">在 PSA 中，可使用条目日记帐记录材料、费用、时间、支出或税务交易分类的成本或收入。</span><span class="sxs-lookup"><span data-stu-id="0bc60-126">In PSA, Entry journals let you record the cost or revenue in the material, fee, time, expense, or tax transaction classes.</span></span> <span data-ttu-id="0bc60-127">日记帐有标题、行和 **确认** 操作。</span><span class="sxs-lookup"><span data-stu-id="0bc60-127">A journal has a header, lines, and a **Confirm** action.</span></span> <span data-ttu-id="0bc60-128">下面是一些可能需要使用日记帐的场景：</span><span class="sxs-lookup"><span data-stu-id="0bc60-128">Here are some scenarios where you might use a journal:</span></span>

- <span data-ttu-id="0bc60-129">必须记录项目的材料实际成本和销售额。</span><span class="sxs-lookup"><span data-stu-id="0bc60-129">You must record material actual costs and sales on a project.</span></span>
- <span data-ttu-id="0bc60-130">必须将交易实际值从另一个系统移到 PSA。</span><span class="sxs-lookup"><span data-stu-id="0bc60-130">You must move transaction actuals from another system to PSA.</span></span>
- <span data-ttu-id="0bc60-131">必须记录另一个系统中出现的成本，如采购成本或分包成本。</span><span class="sxs-lookup"><span data-stu-id="0bc60-131">You must record costs that occurred in another system, such as procurement or subcontracting costs.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="0bc60-132">用户只有完全了解“实际值”对项目会计的影响，才能使用条目日记帐创建实际值。</span><span class="sxs-lookup"><span data-stu-id="0bc60-132">Using Entry journals to create actuals should be done only by a user who is fully aware of the accounting impact the Actuals have on the project.</span></span> <span data-ttu-id="0bc60-133">这是因为此应用程序不会验证日记帐行类型，也不会验证在日记帐行上输入的相关定价。</span><span class="sxs-lookup"><span data-stu-id="0bc60-133">This is because the application does not validate the journal line type, or the related pricing that is entered on the journal line.</span></span> <span data-ttu-id="0bc60-134">由于此日记帐类型会造成一定的影响，因此，对于谁有权创建条目日记帐，应该十分谨慎。</span><span class="sxs-lookup"><span data-stu-id="0bc60-134">Because of the impact of this journal type, exercise adequate caution in who is given access to create Entry journals.</span></span>     


## <a name="recording-actuals-based-on-project-events"></a><span data-ttu-id="0bc60-135">基于项目事件记录实际值</span><span class="sxs-lookup"><span data-stu-id="0bc60-135">Recording actuals based on project events</span></span>

<span data-ttu-id="0bc60-136">PSA 记录项目期间发生的财务交易。</span><span class="sxs-lookup"><span data-stu-id="0bc60-136">PSA records the financial transactions that occur during a project.</span></span> <span data-ttu-id="0bc60-137">这些交易记录为 **实际值** 。</span><span class="sxs-lookup"><span data-stu-id="0bc60-137">These transactions are recorded as **actuals**.</span></span> <span data-ttu-id="0bc60-138">下表显示创建的不同类型的实际值，具体取决于项目是时间和材料还是固定价格，是否处于售前阶段，是否为内部项目。</span><span class="sxs-lookup"><span data-stu-id="0bc60-138">The following tables show the different types of actuals that are created, depending on whether the project is a time-and-materials or fixed-price project, is in the presales stage, or is an internal project.</span></span>

<span data-ttu-id="0bc60-139">**资源与项目的合同签订部门属于同一个部门**</span><span class="sxs-lookup"><span data-stu-id="0bc60-139">**The resource belongs to same organizational unit as the project's contracting unit**</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="0bc60-140">事件</span><span class="sxs-lookup"><span data-stu-id="0bc60-140">Event</span></span></th>
<th colspan="4"><span data-ttu-id="0bc60-141">可记帐项目或已售项目</span><span class="sxs-lookup"><span data-stu-id="0bc60-141">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="0bc60-142">售前阶段的项目</span><span class="sxs-lookup"><span data-stu-id="0bc60-142">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="0bc60-143">内部项目</span><span class="sxs-lookup"><span data-stu-id="0bc60-143">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="0bc60-144">时间和材料</span><span class="sxs-lookup"><span data-stu-id="0bc60-144">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="0bc60-145">固定价格</span><span class="sxs-lookup"><span data-stu-id="0bc60-145">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="0bc60-146">实际</span><span class="sxs-lookup"><span data-stu-id="0bc60-146">Actuals</span></span></th>
<th><span data-ttu-id="0bc60-147">交易货币</span><span class="sxs-lookup"><span data-stu-id="0bc60-147">Transaction currency</span></span></th>
<th><span data-ttu-id="0bc60-148">固定价格</span><span class="sxs-lookup"><span data-stu-id="0bc60-148">Fixed price</span></span></th>
<th><span data-ttu-id="0bc60-149">交易货币</span><span class="sxs-lookup"><span data-stu-id="0bc60-149">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="0bc60-150">创建时间条目。</span><span class="sxs-lookup"><span data-stu-id="0bc60-150">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="0bc60-151">实际值条目中无活动</span><span class="sxs-lookup"><span data-stu-id="0bc60-151">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0bc60-152">提交时间条目。</span><span class="sxs-lookup"><span data-stu-id="0bc60-152">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="0bc60-153">实际值条目中无活动</span><span class="sxs-lookup"><span data-stu-id="0bc60-153">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="0bc60-154">批准时间，并且审批期间可记帐工时不变或不增加。</span><span class="sxs-lookup"><span data-stu-id="0bc60-154">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="0bc60-155">成本实际值</span><span class="sxs-lookup"><span data-stu-id="0bc60-155">Cost actual</span></span></td>
<td><span data-ttu-id="0bc60-156">合同签订部门货币</span><span class="sxs-lookup"><span data-stu-id="0bc60-156">Contracting unit currency</span></span></td>
<td rowspan="2"><span data-ttu-id="0bc60-157">实际成本</span><span class="sxs-lookup"><span data-stu-id="0bc60-157">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="0bc60-158">合同签订部门货币</span><span class="sxs-lookup"><span data-stu-id="0bc60-158">Contracting unit currency</span></span>
<td rowspan="2"><span data-ttu-id="0bc60-159">成本实际值</span><span class="sxs-lookup"><span data-stu-id="0bc60-159">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="0bc60-160">成本实际值</span><span class="sxs-lookup"><span data-stu-id="0bc60-160">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0bc60-161">未记帐实际销售额 – 应计费</span><span class="sxs-lookup"><span data-stu-id="0bc60-161">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="0bc60-162">项目合同货币</span><span class="sxs-lookup"><span data-stu-id="0bc60-162">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="0bc60-163">批准时间，并且审批期间可记帐工时不变或不减少。</span><span class="sxs-lookup"><span data-stu-id="0bc60-163">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="0bc60-164">实际成本</span><span class="sxs-lookup"><span data-stu-id="0bc60-164">Cost actual</span></span></td>
<td><span data-ttu-id="0bc60-165">合同签订部门货币</span><span class="sxs-lookup"><span data-stu-id="0bc60-165">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="0bc60-166">实际成本</span><span class="sxs-lookup"><span data-stu-id="0bc60-166">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="0bc60-167">合同签订部门货币</span><span class="sxs-lookup"><span data-stu-id="0bc60-167">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="0bc60-168">实际成本</span><span class="sxs-lookup"><span data-stu-id="0bc60-168">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="0bc60-169">实际成本</span><span class="sxs-lookup"><span data-stu-id="0bc60-169">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0bc60-170">未记帐实际销售额 – 新数量的应计值</span><span class="sxs-lookup"><span data-stu-id="0bc60-170">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="0bc60-171">项目合同货币</span><span class="sxs-lookup"><span data-stu-id="0bc60-171">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0bc60-172">未记帐实际销售额 – 差额的非应计值</span><span class="sxs-lookup"><span data-stu-id="0bc60-172">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="0bc60-173">项目合同货币</span><span class="sxs-lookup"><span data-stu-id="0bc60-173">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="0bc60-174">确认发票，并且审批期间可记帐工时不变或不增加。</span><span class="sxs-lookup"><span data-stu-id="0bc60-174">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="0bc60-175">未记帐销售额冲销</span><span class="sxs-lookup"><span data-stu-id="0bc60-175">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="0bc60-176">项目合同货币</span><span class="sxs-lookup"><span data-stu-id="0bc60-176">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="0bc60-177">里程碑的已记帐销售额</span><span class="sxs-lookup"><span data-stu-id="0bc60-177">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="0bc60-178">项目合同货币</span><span class="sxs-lookup"><span data-stu-id="0bc60-178">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="0bc60-179">不适用</span><span class="sxs-lookup"><span data-stu-id="0bc60-179">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="0bc60-180">不适用</span><span class="sxs-lookup"><span data-stu-id="0bc60-180">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0bc60-181">已记帐销售额</span><span class="sxs-lookup"><span data-stu-id="0bc60-181">Billed sales</span></span></td>
<td><span data-ttu-id="0bc60-182">项目合同货币</span><span class="sxs-lookup"><span data-stu-id="0bc60-182">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="0bc60-183">确认发票，并且可记帐工时减少。</span><span class="sxs-lookup"><span data-stu-id="0bc60-183">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="0bc60-184">未记帐销售额冲销</span><span class="sxs-lookup"><span data-stu-id="0bc60-184">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="0bc60-185">项目合同货币</span><span class="sxs-lookup"><span data-stu-id="0bc60-185">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="0bc60-186">不适用</span><span class="sxs-lookup"><span data-stu-id="0bc60-186">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="0bc60-187">不适用</span><span class="sxs-lookup"><span data-stu-id="0bc60-187">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="0bc60-188">不适用</span><span class="sxs-lookup"><span data-stu-id="0bc60-188">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="0bc60-189">不适用</span><span class="sxs-lookup"><span data-stu-id="0bc60-189">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0bc60-190">已记帐销售额 – 新数量的应计值</span><span class="sxs-lookup"><span data-stu-id="0bc60-190">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="0bc60-191">项目合同货币</span><span class="sxs-lookup"><span data-stu-id="0bc60-191">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0bc60-192">已记帐实际销售额 – 差额的非应计值</span><span class="sxs-lookup"><span data-stu-id="0bc60-192">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="0bc60-193">项目合同货币</span><span class="sxs-lookup"><span data-stu-id="0bc60-193">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="0bc60-194">更正发票以增加应计费数量。</span><span class="sxs-lookup"><span data-stu-id="0bc60-194">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="0bc60-195">已记帐销售额 - 冲销</span><span class="sxs-lookup"><span data-stu-id="0bc60-195">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="0bc60-196">项目合同货币</span><span class="sxs-lookup"><span data-stu-id="0bc60-196">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="0bc60-197">里程碑的已记帐销售额冲销</span><span class="sxs-lookup"><span data-stu-id="0bc60-197">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="0bc60-198">里程碑状态从<strong>已开票</strong>更改为<strong>准备好开票</strong></span><span class="sxs-lookup"><span data-stu-id="0bc60-198">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="0bc60-199">项目合同货币</span><span class="sxs-lookup"><span data-stu-id="0bc60-199">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="0bc60-200">不适用</span><span class="sxs-lookup"><span data-stu-id="0bc60-200">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="0bc60-201">不适用</span><span class="sxs-lookup"><span data-stu-id="0bc60-201">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0bc60-202">已记帐销售额</span><span class="sxs-lookup"><span data-stu-id="0bc60-202">Billed sales</span></span></td>
<td><span data-ttu-id="0bc60-203">项目合同货币</span><span class="sxs-lookup"><span data-stu-id="0bc60-203">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="0bc60-204">更正发票以减少应计费数量。</span><span class="sxs-lookup"><span data-stu-id="0bc60-204">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="0bc60-205">已记帐销售额 - 冲销</span><span class="sxs-lookup"><span data-stu-id="0bc60-205">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="0bc60-206">项目合同货币</span><span class="sxs-lookup"><span data-stu-id="0bc60-206">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0bc60-207">新数量的已记帐销售额</span><span class="sxs-lookup"><span data-stu-id="0bc60-207">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="0bc60-208">项目合同货币</span><span class="sxs-lookup"><span data-stu-id="0bc60-208">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0bc60-209">未记帐销售额 – 差额的应计值</span><span class="sxs-lookup"><span data-stu-id="0bc60-209">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="0bc60-210">项目合同货币</span><span class="sxs-lookup"><span data-stu-id="0bc60-210">Project contract currency</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="0bc60-211">**资源与项目的合同签订部门不属于同一个部门**</span><span class="sxs-lookup"><span data-stu-id="0bc60-211">**The resource belongs to an organizational unit that differs from the project's contracting unit**</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="0bc60-212">事件</span><span class="sxs-lookup"><span data-stu-id="0bc60-212">Event</span></span></th>
<th colspan="4"><span data-ttu-id="0bc60-213">可记帐项目或已售项目</span><span class="sxs-lookup"><span data-stu-id="0bc60-213">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="0bc60-214">售前阶段的项目</span><span class="sxs-lookup"><span data-stu-id="0bc60-214">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="0bc60-215">内部项目</span><span class="sxs-lookup"><span data-stu-id="0bc60-215">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="0bc60-216">时间和材料</span><span class="sxs-lookup"><span data-stu-id="0bc60-216">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="0bc60-217">固定价格</span><span class="sxs-lookup"><span data-stu-id="0bc60-217">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="0bc60-218">实际</span><span class="sxs-lookup"><span data-stu-id="0bc60-218">Actuals</span></span></th>
<th><span data-ttu-id="0bc60-219">交易货币</span><span class="sxs-lookup"><span data-stu-id="0bc60-219">Transaction currency</span></span></th>
<th><span data-ttu-id="0bc60-220">固定价格</span><span class="sxs-lookup"><span data-stu-id="0bc60-220">Fixed price</span></span></th>
<th><span data-ttu-id="0bc60-221">交易货币</span><span class="sxs-lookup"><span data-stu-id="0bc60-221">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="0bc60-222">创建时间条目。</span><span class="sxs-lookup"><span data-stu-id="0bc60-222">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="0bc60-223">实际值条目中无活动</span><span class="sxs-lookup"><span data-stu-id="0bc60-223">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0bc60-224">提交时间条目。</span><span class="sxs-lookup"><span data-stu-id="0bc60-224">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="0bc60-225">实际值条目中无活动</span><span class="sxs-lookup"><span data-stu-id="0bc60-225">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="4"><span data-ttu-id="0bc60-226">批准时间，并且审批期间可记帐工时不变或不增加。</span><span class="sxs-lookup"><span data-stu-id="0bc60-226">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="0bc60-227">成本实际值</span><span class="sxs-lookup"><span data-stu-id="0bc60-227">Cost actual</span></span></td>
<td><span data-ttu-id="0bc60-228">合同签订部门货币</span><span class="sxs-lookup"><span data-stu-id="0bc60-228">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="0bc60-229">实际成本</span><span class="sxs-lookup"><span data-stu-id="0bc60-229">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="0bc60-230">合同签订部门货币</span><span class="sxs-lookup"><span data-stu-id="0bc60-230">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="0bc60-231">成本实际值</span><span class="sxs-lookup"><span data-stu-id="0bc60-231">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="0bc60-232">成本实际值</span><span class="sxs-lookup"><span data-stu-id="0bc60-232">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0bc60-233">未记帐实际销售额 – 应计费</span><span class="sxs-lookup"><span data-stu-id="0bc60-233">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="0bc60-234">项目合同货币</span><span class="sxs-lookup"><span data-stu-id="0bc60-234">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0bc60-235">资源单位成本</span><span class="sxs-lookup"><span data-stu-id="0bc60-235">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="0bc60-236">资源单位货币</span><span class="sxs-lookup"><span data-stu-id="0bc60-236">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0bc60-237">组织间销售</span><span class="sxs-lookup"><span data-stu-id="0bc60-237">Interorganizational sales</span></span></td>
<td><span data-ttu-id="0bc60-238">合同签订部门货币</span><span class="sxs-lookup"><span data-stu-id="0bc60-238">Contracting unit currency</span></span></td>
</tr>
<tr>
<td rowspan="5"><span data-ttu-id="0bc60-239">批准时间，并且审批期间可记帐工时不变或不减少。</span><span class="sxs-lookup"><span data-stu-id="0bc60-239">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="0bc60-240">实际成本</span><span class="sxs-lookup"><span data-stu-id="0bc60-240">Cost actual</span></span></td>
<td><span data-ttu-id="0bc60-241">合同签订部门货币</span><span class="sxs-lookup"><span data-stu-id="0bc60-241">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="0bc60-242">实际成本</span><span class="sxs-lookup"><span data-stu-id="0bc60-242">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="0bc60-243">合同签订部门货币</span><span class="sxs-lookup"><span data-stu-id="0bc60-243">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="0bc60-244">实际成本</span><span class="sxs-lookup"><span data-stu-id="0bc60-244">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="0bc60-245">实际成本</span><span class="sxs-lookup"><span data-stu-id="0bc60-245">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0bc60-246">资源单位成本</span><span class="sxs-lookup"><span data-stu-id="0bc60-246">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="0bc60-247">资源单位货币</span><span class="sxs-lookup"><span data-stu-id="0bc60-247">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0bc60-248">组织间销售</span><span class="sxs-lookup"><span data-stu-id="0bc60-248">Interorganizational sales</span></span></td>
<td><span data-ttu-id="0bc60-249">合同签订部门货币</span><span class="sxs-lookup"><span data-stu-id="0bc60-249">Contracting unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0bc60-250">未记帐实际销售额 – 新数量的应计值</span><span class="sxs-lookup"><span data-stu-id="0bc60-250">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="0bc60-251">项目合同货币</span><span class="sxs-lookup"><span data-stu-id="0bc60-251">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0bc60-252">未记帐实际销售额 – 差额的非应计值</span><span class="sxs-lookup"><span data-stu-id="0bc60-252">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="0bc60-253">项目合同货币</span><span class="sxs-lookup"><span data-stu-id="0bc60-253">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="0bc60-254">确认发票，并且审批期间可记帐工时不变或不增加。</span><span class="sxs-lookup"><span data-stu-id="0bc60-254">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="0bc60-255">未记帐销售额冲销</span><span class="sxs-lookup"><span data-stu-id="0bc60-255">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="0bc60-256">项目合同货币</span><span class="sxs-lookup"><span data-stu-id="0bc60-256">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="0bc60-257">里程碑的已记帐销售额</span><span class="sxs-lookup"><span data-stu-id="0bc60-257">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="0bc60-258">项目合同货币</span><span class="sxs-lookup"><span data-stu-id="0bc60-258">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="0bc60-259">不适用</span><span class="sxs-lookup"><span data-stu-id="0bc60-259">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="0bc60-260">不适用</span><span class="sxs-lookup"><span data-stu-id="0bc60-260">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0bc60-261">已记帐销售额</span><span class="sxs-lookup"><span data-stu-id="0bc60-261">Billed sales</span></span></td>
<td><span data-ttu-id="0bc60-262">项目合同货币</span><span class="sxs-lookup"><span data-stu-id="0bc60-262">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="0bc60-263">确认发票，并且可记帐工时减少。</span><span class="sxs-lookup"><span data-stu-id="0bc60-263">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="0bc60-264">未记帐销售额冲销</span><span class="sxs-lookup"><span data-stu-id="0bc60-264">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="0bc60-265">项目合同货币</span><span class="sxs-lookup"><span data-stu-id="0bc60-265">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="0bc60-266">不适用</span><span class="sxs-lookup"><span data-stu-id="0bc60-266">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="0bc60-267">不适用</span><span class="sxs-lookup"><span data-stu-id="0bc60-267">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="0bc60-268">不适用</span><span class="sxs-lookup"><span data-stu-id="0bc60-268">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="0bc60-269">不适用</span><span class="sxs-lookup"><span data-stu-id="0bc60-269">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0bc60-270">已记帐销售额 – 新数量的应计值</span><span class="sxs-lookup"><span data-stu-id="0bc60-270">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="0bc60-271">项目合同货币</span><span class="sxs-lookup"><span data-stu-id="0bc60-271">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0bc60-272">已记帐实际销售额 – 差额的非应计值</span><span class="sxs-lookup"><span data-stu-id="0bc60-272">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="0bc60-273">项目合同货币</span><span class="sxs-lookup"><span data-stu-id="0bc60-273">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="0bc60-274">更正发票以增加应计费数量。</span><span class="sxs-lookup"><span data-stu-id="0bc60-274">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="0bc60-275">已记帐销售额 - 冲销</span><span class="sxs-lookup"><span data-stu-id="0bc60-275">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="0bc60-276">项目合同货币</span><span class="sxs-lookup"><span data-stu-id="0bc60-276">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="0bc60-277">里程碑的已记帐销售额冲销</span><span class="sxs-lookup"><span data-stu-id="0bc60-277">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="0bc60-278">里程碑状态从<strong>已开票</strong>更改为<strong>准备好开票</strong></span><span class="sxs-lookup"><span data-stu-id="0bc60-278">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="0bc60-279">项目合同货币</span><span class="sxs-lookup"><span data-stu-id="0bc60-279">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="0bc60-280">不适用</span><span class="sxs-lookup"><span data-stu-id="0bc60-280">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="0bc60-281">不适用</span><span class="sxs-lookup"><span data-stu-id="0bc60-281">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0bc60-282">已记帐销售额</span><span class="sxs-lookup"><span data-stu-id="0bc60-282">Billed sales</span></span></td>
<td><span data-ttu-id="0bc60-283">项目合同货币</span><span class="sxs-lookup"><span data-stu-id="0bc60-283">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="0bc60-284">更正发票以减少应计费数量。</span><span class="sxs-lookup"><span data-stu-id="0bc60-284">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="0bc60-285">已记帐销售额 - 冲销</span><span class="sxs-lookup"><span data-stu-id="0bc60-285">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="0bc60-286">项目合同货币</span><span class="sxs-lookup"><span data-stu-id="0bc60-286">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0bc60-287">新数量的已记帐销售额</span><span class="sxs-lookup"><span data-stu-id="0bc60-287">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="0bc60-288">项目合同货币</span><span class="sxs-lookup"><span data-stu-id="0bc60-288">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0bc60-289">未记帐销售额 – 差额的应计值</span><span class="sxs-lookup"><span data-stu-id="0bc60-289">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="0bc60-290">项目合同货币</span><span class="sxs-lookup"><span data-stu-id="0bc60-290">Project contract currency</span></span></td>
</tr>
</tbody>
</table>
