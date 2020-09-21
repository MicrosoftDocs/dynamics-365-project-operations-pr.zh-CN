---
title: 实际
description: 本主题提供有关项目实际值的信息。
author: rumant
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/06/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: 44c6e85f-5b21-4e24-999c-15a2f065d977
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 8291e0eb8531e8e9690368675f333c44b6e92e48
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/24/2020
ms.locfileid: "3749767"
---
# <a name="actuals"></a><span data-ttu-id="4e66b-103">实际</span><span class="sxs-lookup"><span data-stu-id="4e66b-103">Actuals</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="4e66b-104">实际值是已完成的项目工作量。</span><span class="sxs-lookup"><span data-stu-id="4e66b-104">Actuals are the amount of work that has been completed on a project.</span></span> <span data-ttu-id="4e66b-105">可将项目实际值回溯到其源文档。</span><span class="sxs-lookup"><span data-stu-id="4e66b-105">Project actuals can be traced back to their source documents.</span></span> <span data-ttu-id="4e66b-106">这些源文档包括时间、支出和日记帐条目，以及发票。</span><span class="sxs-lookup"><span data-stu-id="4e66b-106">Those source documents include time, expense, and journal entries, and also invoices.</span></span>

![如何将项目实际值跟踪到源文档](media/basic-guide-18.png)

## <a name="submitting-a-time-entry"></a><span data-ttu-id="4e66b-108">提交时间条目</span><span class="sxs-lookup"><span data-stu-id="4e66b-108">Submitting a time entry</span></span>

<span data-ttu-id="4e66b-109">在 PSA 中，为映射到时间和材料合同子项的项目提交时间条目时，将创建两个日记帐行。</span><span class="sxs-lookup"><span data-stu-id="4e66b-109">In PSA, when a time entry is submitted for a project that is mapped to a time-and-materials contract line, two journal lines are created.</span></span> <span data-ttu-id="4e66b-110">一行针对成本，另一行针对未记帐销售。</span><span class="sxs-lookup"><span data-stu-id="4e66b-110">One line is for cost, and the other line is for unbilled sales.</span></span> <span data-ttu-id="4e66b-111">为映射到固定价格合同子项的项目提交时间条目时，仅为成本创建一个日记帐行。</span><span class="sxs-lookup"><span data-stu-id="4e66b-111">When a time entry is submitted for a project that is mapped to a fixed-price contract line, a journal line is created only for cost.</span></span> 

<span data-ttu-id="4e66b-112">有关输入默认价格的逻辑在日记帐行中。</span><span class="sxs-lookup"><span data-stu-id="4e66b-112">Logic for entering default prices resides on the journal line.</span></span> <span data-ttu-id="4e66b-113">时间条目中的所有字段值将复制到该日记帐行中。</span><span class="sxs-lookup"><span data-stu-id="4e66b-113">All the field values from a time entry are copied to the journal line.</span></span> <span data-ttu-id="4e66b-114">这些字段中包含交易日期、项目映射到的合同子项，以及相应价目表中的货币结果。</span><span class="sxs-lookup"><span data-stu-id="4e66b-114">These fields include the date of the transaction, the contract line that the project is mapped to, and the currency result in the appropriate price list.</span></span> 

<span data-ttu-id="4e66b-115">会影响默认价格的字段（如**角色**和**部门**）会导致默认在日记帐行中输入相应价格。</span><span class="sxs-lookup"><span data-stu-id="4e66b-115">The fields that affect default prices, such as **Role** and **Org Unit**, cause an appropriate price to be entered by default on the journal line.</span></span> <span data-ttu-id="4e66b-116">如果在时间条目中添加自定义字段，并且希望将字段值传播到实际值，请在实际值条目中创建字段，然后使用字段映射将该字段从时间条目复制到实际值。</span><span class="sxs-lookup"><span data-stu-id="4e66b-116">If you add a custom field on the time entry, and you want the field value to be propagated to actuals, create the field on the Actuals entity, and use field mappings to copy the field from the time entry to the actual.</span></span>

## <a name="submitting-an-expense-entry"></a><span data-ttu-id="4e66b-117">提交支出条目</span><span class="sxs-lookup"><span data-stu-id="4e66b-117">Submitting an expense entry</span></span>

<span data-ttu-id="4e66b-118">在 PSA 中，为映射到时间和材料合同子项的项目提交支出条目时，将创建两个日记帐行。</span><span class="sxs-lookup"><span data-stu-id="4e66b-118">In PSA, when an expense entry is submitted for a project that is mapped to a time-and-materials contract line, two journal lines are created.</span></span> <span data-ttu-id="4e66b-119">一行针对成本，另一行针对未记帐销售。</span><span class="sxs-lookup"><span data-stu-id="4e66b-119">One line is for cost, and the other line is for unbilled sales.</span></span> <span data-ttu-id="4e66b-120">为映射到固定价格合同子项的项目提交支出条目时，仅为成本创建一个日记帐行。</span><span class="sxs-lookup"><span data-stu-id="4e66b-120">When an expense entry is submitted for a project that is mapped to a fixed-price contract line, a journal line is created only for cost.</span></span>

<span data-ttu-id="4e66b-121">用于输入支出的默认价格的逻辑基于在**支出条目**页中选择的支出类别。</span><span class="sxs-lookup"><span data-stu-id="4e66b-121">Logic for entering default prices for expenses is based on the expense category that is selected on the **Expense entry** page.</span></span> <span data-ttu-id="4e66b-122">交易日期、项目映射到的合同子项，以及货币全部用于确定相应价目表。</span><span class="sxs-lookup"><span data-stu-id="4e66b-122">The transaction date, the contract line that the project is mapped to, and the currency are all used to determine the appropriate price list.</span></span> <span data-ttu-id="4e66b-123">但是，对于价格本身，默认情况下将直接在成本和销售额的相关支出日记帐行中设置用户输入的金额。</span><span class="sxs-lookup"><span data-stu-id="4e66b-123">However, for the price itself, the amount that the user entered is set directly on the related expense journal lines for cost and sales by default.</span></span>

<span data-ttu-id="4e66b-124">在当前 PSA 版本中，不能在支出条目中基于类别录入默认单价。</span><span class="sxs-lookup"><span data-stu-id="4e66b-124">In the current version of PSA, category-based entry of per-unit default prices on expense entries isn't available.</span></span>

## <a name="using-journals-to-record-costs"></a><span data-ttu-id="4e66b-125">使用日记帐记录成本</span><span class="sxs-lookup"><span data-stu-id="4e66b-125">Using journals to record costs</span></span>

<span data-ttu-id="4e66b-126">在 PSA 中，日记帐用于记录材料、费用、时间、支出或税务交易分类的成本或收入。</span><span class="sxs-lookup"><span data-stu-id="4e66b-126">In PSA, journals let you record cost or revenue in the material, fee, time, expense, or tax transaction classes.</span></span> <span data-ttu-id="4e66b-127">日记帐有标题、行和**确认**操作。</span><span class="sxs-lookup"><span data-stu-id="4e66b-127">A journal has a header, lines, and a **Confirm** action.</span></span> <span data-ttu-id="4e66b-128">下面是一些可能需要使用日记帐的场景：</span><span class="sxs-lookup"><span data-stu-id="4e66b-128">Here are some scenarios where you might use a journal:</span></span>

- <span data-ttu-id="4e66b-129">必须记录项目的材料实际成本和销售额。</span><span class="sxs-lookup"><span data-stu-id="4e66b-129">You must record material actual costs and sales on a project.</span></span>
- <span data-ttu-id="4e66b-130">必须将交易实际值从另一个系统移到 PSA。</span><span class="sxs-lookup"><span data-stu-id="4e66b-130">You must move transaction actuals from another system to PSA.</span></span>
- <span data-ttu-id="4e66b-131">必须记录另一个系统中出现的成本，如采购成本或分包成本。</span><span class="sxs-lookup"><span data-stu-id="4e66b-131">You must record costs that occurred in another system, such as procurement or subcontracting costs.</span></span>

## <a name="recording-actuals-based-on-project-events"></a><span data-ttu-id="4e66b-132">基于项目事件记录实际值</span><span class="sxs-lookup"><span data-stu-id="4e66b-132">Recording actuals based on project events</span></span>

<span data-ttu-id="4e66b-133">PSA 记录项目期间发生的财务交易。</span><span class="sxs-lookup"><span data-stu-id="4e66b-133">PSA records the financial transactions that occur during a project.</span></span> <span data-ttu-id="4e66b-134">这些交易记录为**实际值**。</span><span class="sxs-lookup"><span data-stu-id="4e66b-134">These transactions are recorded as **actuals**.</span></span> <span data-ttu-id="4e66b-135">下表显示创建的不同类型的实际值，具体取决于项目是时间和材料还是固定价格，是否处于售前阶段，是否为内部项目。</span><span class="sxs-lookup"><span data-stu-id="4e66b-135">The following tables show the different types of actuals that are created, depending on whether the project is a time-and-materials or fixed-price project, is in the presales stage, or is an internal project.</span></span>

<span data-ttu-id="4e66b-136">**资源与项目的合同签订部门属于同一个部门**</span><span class="sxs-lookup"><span data-stu-id="4e66b-136">**The resource belongs to same organizational unit as the project's contracting unit**</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="4e66b-137">事件</span><span class="sxs-lookup"><span data-stu-id="4e66b-137">Event</span></span></th>
<th colspan="4"><span data-ttu-id="4e66b-138">可记帐项目或已售项目</span><span class="sxs-lookup"><span data-stu-id="4e66b-138">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="4e66b-139">售前阶段的项目</span><span class="sxs-lookup"><span data-stu-id="4e66b-139">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="4e66b-140">内部项目</span><span class="sxs-lookup"><span data-stu-id="4e66b-140">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="4e66b-141">时间和材料</span><span class="sxs-lookup"><span data-stu-id="4e66b-141">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="4e66b-142">固定价格</span><span class="sxs-lookup"><span data-stu-id="4e66b-142">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="4e66b-143">实际</span><span class="sxs-lookup"><span data-stu-id="4e66b-143">Actuals</span></span></th>
<th><span data-ttu-id="4e66b-144">交易货币</span><span class="sxs-lookup"><span data-stu-id="4e66b-144">Transaction currency</span></span></th>
<th><span data-ttu-id="4e66b-145">固定价格</span><span class="sxs-lookup"><span data-stu-id="4e66b-145">Fixed price</span></span></th>
<th><span data-ttu-id="4e66b-146">交易货币</span><span class="sxs-lookup"><span data-stu-id="4e66b-146">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="4e66b-147">创建时间条目。</span><span class="sxs-lookup"><span data-stu-id="4e66b-147">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="4e66b-148">实际值条目中无活动</span><span class="sxs-lookup"><span data-stu-id="4e66b-148">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4e66b-149">提交时间条目。</span><span class="sxs-lookup"><span data-stu-id="4e66b-149">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="4e66b-150">实际值条目中无活动</span><span class="sxs-lookup"><span data-stu-id="4e66b-150">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="4e66b-151">批准时间，并且审批期间可记帐工时不变或不增加。</span><span class="sxs-lookup"><span data-stu-id="4e66b-151">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="4e66b-152">成本实际值</span><span class="sxs-lookup"><span data-stu-id="4e66b-152">Cost actual</span></span></td>
<td><span data-ttu-id="4e66b-153">合同签订部门货币</span><span class="sxs-lookup"><span data-stu-id="4e66b-153">Contracting unit currency</span></span></td>
<td rowspan="2"><span data-ttu-id="4e66b-154">实际成本</span><span class="sxs-lookup"><span data-stu-id="4e66b-154">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="4e66b-155">合同签订部门货币</span><span class="sxs-lookup"><span data-stu-id="4e66b-155">Contracting unit currency</span></span>
<td rowspan="2"><span data-ttu-id="4e66b-156">成本实际值</span><span class="sxs-lookup"><span data-stu-id="4e66b-156">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="4e66b-157">成本实际值</span><span class="sxs-lookup"><span data-stu-id="4e66b-157">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4e66b-158">未记帐实际销售额 – 应计费</span><span class="sxs-lookup"><span data-stu-id="4e66b-158">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="4e66b-159">项目合同货币</span><span class="sxs-lookup"><span data-stu-id="4e66b-159">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="4e66b-160">批准时间，并且审批期间可记帐工时不变或不减少。</span><span class="sxs-lookup"><span data-stu-id="4e66b-160">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="4e66b-161">实际成本</span><span class="sxs-lookup"><span data-stu-id="4e66b-161">Cost actual</span></span></td>
<td><span data-ttu-id="4e66b-162">合同签订部门货币</span><span class="sxs-lookup"><span data-stu-id="4e66b-162">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="4e66b-163">实际成本</span><span class="sxs-lookup"><span data-stu-id="4e66b-163">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="4e66b-164">合同签订部门货币</span><span class="sxs-lookup"><span data-stu-id="4e66b-164">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="4e66b-165">实际成本</span><span class="sxs-lookup"><span data-stu-id="4e66b-165">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="4e66b-166">实际成本</span><span class="sxs-lookup"><span data-stu-id="4e66b-166">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4e66b-167">未记帐实际销售额 – 新数量的应计值</span><span class="sxs-lookup"><span data-stu-id="4e66b-167">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="4e66b-168">项目合同货币</span><span class="sxs-lookup"><span data-stu-id="4e66b-168">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4e66b-169">未记帐实际销售额 – 差额的非应计值</span><span class="sxs-lookup"><span data-stu-id="4e66b-169">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="4e66b-170">项目合同货币</span><span class="sxs-lookup"><span data-stu-id="4e66b-170">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="4e66b-171">确认发票，并且审批期间可记帐工时不变或不增加。</span><span class="sxs-lookup"><span data-stu-id="4e66b-171">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="4e66b-172">未记帐销售额冲销</span><span class="sxs-lookup"><span data-stu-id="4e66b-172">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="4e66b-173">项目合同货币</span><span class="sxs-lookup"><span data-stu-id="4e66b-173">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="4e66b-174">里程碑的已记帐销售额</span><span class="sxs-lookup"><span data-stu-id="4e66b-174">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="4e66b-175">项目合同货币</span><span class="sxs-lookup"><span data-stu-id="4e66b-175">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="4e66b-176">不适用</span><span class="sxs-lookup"><span data-stu-id="4e66b-176">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="4e66b-177">不适用</span><span class="sxs-lookup"><span data-stu-id="4e66b-177">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4e66b-178">已记帐销售额</span><span class="sxs-lookup"><span data-stu-id="4e66b-178">Billed sales</span></span></td>
<td><span data-ttu-id="4e66b-179">项目合同货币</span><span class="sxs-lookup"><span data-stu-id="4e66b-179">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="4e66b-180">确认发票，并且可记帐工时减少。</span><span class="sxs-lookup"><span data-stu-id="4e66b-180">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="4e66b-181">未记帐销售额冲销</span><span class="sxs-lookup"><span data-stu-id="4e66b-181">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="4e66b-182">项目合同货币</span><span class="sxs-lookup"><span data-stu-id="4e66b-182">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="4e66b-183">不适用</span><span class="sxs-lookup"><span data-stu-id="4e66b-183">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="4e66b-184">不适用</span><span class="sxs-lookup"><span data-stu-id="4e66b-184">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="4e66b-185">不适用</span><span class="sxs-lookup"><span data-stu-id="4e66b-185">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="4e66b-186">不适用</span><span class="sxs-lookup"><span data-stu-id="4e66b-186">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4e66b-187">已记帐销售额 – 新数量的应计值</span><span class="sxs-lookup"><span data-stu-id="4e66b-187">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="4e66b-188">项目合同货币</span><span class="sxs-lookup"><span data-stu-id="4e66b-188">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4e66b-189">已记帐实际销售额 – 差额的非应计值</span><span class="sxs-lookup"><span data-stu-id="4e66b-189">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="4e66b-190">项目合同货币</span><span class="sxs-lookup"><span data-stu-id="4e66b-190">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="4e66b-191">更正发票以增加应计费数量。</span><span class="sxs-lookup"><span data-stu-id="4e66b-191">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="4e66b-192">已记帐销售额 - 冲销</span><span class="sxs-lookup"><span data-stu-id="4e66b-192">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="4e66b-193">项目合同货币</span><span class="sxs-lookup"><span data-stu-id="4e66b-193">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="4e66b-194">里程碑的已记帐销售额冲销</span><span class="sxs-lookup"><span data-stu-id="4e66b-194">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="4e66b-195">里程碑状态从<strong>已开票</strong>更改为<strong>准备好开票</strong></span><span class="sxs-lookup"><span data-stu-id="4e66b-195">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="4e66b-196">项目合同货币</span><span class="sxs-lookup"><span data-stu-id="4e66b-196">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="4e66b-197">不适用</span><span class="sxs-lookup"><span data-stu-id="4e66b-197">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="4e66b-198">不适用</span><span class="sxs-lookup"><span data-stu-id="4e66b-198">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4e66b-199">已记帐销售额</span><span class="sxs-lookup"><span data-stu-id="4e66b-199">Billed sales</span></span></td>
<td><span data-ttu-id="4e66b-200">项目合同货币</span><span class="sxs-lookup"><span data-stu-id="4e66b-200">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="4e66b-201">更正发票以减少应计费数量。</span><span class="sxs-lookup"><span data-stu-id="4e66b-201">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="4e66b-202">已记帐销售额 - 冲销</span><span class="sxs-lookup"><span data-stu-id="4e66b-202">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="4e66b-203">项目合同货币</span><span class="sxs-lookup"><span data-stu-id="4e66b-203">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4e66b-204">新数量的已记帐销售额</span><span class="sxs-lookup"><span data-stu-id="4e66b-204">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="4e66b-205">项目合同货币</span><span class="sxs-lookup"><span data-stu-id="4e66b-205">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4e66b-206">未记帐销售额 – 差额的应计值</span><span class="sxs-lookup"><span data-stu-id="4e66b-206">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="4e66b-207">项目合同货币</span><span class="sxs-lookup"><span data-stu-id="4e66b-207">Project contract currency</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="4e66b-208">**资源与项目的合同签订部门不属于同一个部门**</span><span class="sxs-lookup"><span data-stu-id="4e66b-208">**The resource belongs to an organizational unit that differs from the project's contracting unit**</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="4e66b-209">事件</span><span class="sxs-lookup"><span data-stu-id="4e66b-209">Event</span></span></th>
<th colspan="4"><span data-ttu-id="4e66b-210">可记帐项目或已售项目</span><span class="sxs-lookup"><span data-stu-id="4e66b-210">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="4e66b-211">售前阶段的项目</span><span class="sxs-lookup"><span data-stu-id="4e66b-211">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="4e66b-212">内部项目</span><span class="sxs-lookup"><span data-stu-id="4e66b-212">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="4e66b-213">时间和材料</span><span class="sxs-lookup"><span data-stu-id="4e66b-213">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="4e66b-214">固定价格</span><span class="sxs-lookup"><span data-stu-id="4e66b-214">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="4e66b-215">实际</span><span class="sxs-lookup"><span data-stu-id="4e66b-215">Actuals</span></span></th>
<th><span data-ttu-id="4e66b-216">交易货币</span><span class="sxs-lookup"><span data-stu-id="4e66b-216">Transaction currency</span></span></th>
<th><span data-ttu-id="4e66b-217">固定价格</span><span class="sxs-lookup"><span data-stu-id="4e66b-217">Fixed price</span></span></th>
<th><span data-ttu-id="4e66b-218">交易货币</span><span class="sxs-lookup"><span data-stu-id="4e66b-218">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="4e66b-219">创建时间条目。</span><span class="sxs-lookup"><span data-stu-id="4e66b-219">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="4e66b-220">实际值条目中无活动</span><span class="sxs-lookup"><span data-stu-id="4e66b-220">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4e66b-221">提交时间条目。</span><span class="sxs-lookup"><span data-stu-id="4e66b-221">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="4e66b-222">实际值条目中无活动</span><span class="sxs-lookup"><span data-stu-id="4e66b-222">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="4"><span data-ttu-id="4e66b-223">批准时间，并且审批期间可记帐工时不变或不增加。</span><span class="sxs-lookup"><span data-stu-id="4e66b-223">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="4e66b-224">成本实际值</span><span class="sxs-lookup"><span data-stu-id="4e66b-224">Cost actual</span></span></td>
<td><span data-ttu-id="4e66b-225">合同签订部门货币</span><span class="sxs-lookup"><span data-stu-id="4e66b-225">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="4e66b-226">实际成本</span><span class="sxs-lookup"><span data-stu-id="4e66b-226">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="4e66b-227">合同签订部门货币</span><span class="sxs-lookup"><span data-stu-id="4e66b-227">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="4e66b-228">成本实际值</span><span class="sxs-lookup"><span data-stu-id="4e66b-228">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="4e66b-229">成本实际值</span><span class="sxs-lookup"><span data-stu-id="4e66b-229">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4e66b-230">未记帐实际销售额 – 应计费</span><span class="sxs-lookup"><span data-stu-id="4e66b-230">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="4e66b-231">项目合同货币</span><span class="sxs-lookup"><span data-stu-id="4e66b-231">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4e66b-232">资源单位成本</span><span class="sxs-lookup"><span data-stu-id="4e66b-232">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="4e66b-233">资源单位货币</span><span class="sxs-lookup"><span data-stu-id="4e66b-233">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4e66b-234">组织间销售</span><span class="sxs-lookup"><span data-stu-id="4e66b-234">Interorganizational sales</span></span></td>
<td><span data-ttu-id="4e66b-235">合同签订部门货币</span><span class="sxs-lookup"><span data-stu-id="4e66b-235">Contracting unit currency</span></span></td>
</tr>
<tr>
<td rowspan="5"><span data-ttu-id="4e66b-236">批准时间，并且审批期间可记帐工时不变或不减少。</span><span class="sxs-lookup"><span data-stu-id="4e66b-236">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="4e66b-237">实际成本</span><span class="sxs-lookup"><span data-stu-id="4e66b-237">Cost actual</span></span></td>
<td><span data-ttu-id="4e66b-238">合同签订部门货币</span><span class="sxs-lookup"><span data-stu-id="4e66b-238">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="4e66b-239">实际成本</span><span class="sxs-lookup"><span data-stu-id="4e66b-239">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="4e66b-240">合同签订部门货币</span><span class="sxs-lookup"><span data-stu-id="4e66b-240">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="4e66b-241">实际成本</span><span class="sxs-lookup"><span data-stu-id="4e66b-241">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="4e66b-242">实际成本</span><span class="sxs-lookup"><span data-stu-id="4e66b-242">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4e66b-243">资源单位成本</span><span class="sxs-lookup"><span data-stu-id="4e66b-243">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="4e66b-244">资源单位货币</span><span class="sxs-lookup"><span data-stu-id="4e66b-244">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4e66b-245">组织间销售</span><span class="sxs-lookup"><span data-stu-id="4e66b-245">Interorganizational sales</span></span></td>
<td><span data-ttu-id="4e66b-246">合同签订部门货币</span><span class="sxs-lookup"><span data-stu-id="4e66b-246">Contracting unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4e66b-247">未记帐实际销售额 – 新数量的应计值</span><span class="sxs-lookup"><span data-stu-id="4e66b-247">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="4e66b-248">项目合同货币</span><span class="sxs-lookup"><span data-stu-id="4e66b-248">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4e66b-249">未记帐实际销售额 – 差额的非应计值</span><span class="sxs-lookup"><span data-stu-id="4e66b-249">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="4e66b-250">项目合同货币</span><span class="sxs-lookup"><span data-stu-id="4e66b-250">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="4e66b-251">确认发票，并且审批期间可记帐工时不变或不增加。</span><span class="sxs-lookup"><span data-stu-id="4e66b-251">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="4e66b-252">未记帐销售额冲销</span><span class="sxs-lookup"><span data-stu-id="4e66b-252">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="4e66b-253">项目合同货币</span><span class="sxs-lookup"><span data-stu-id="4e66b-253">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="4e66b-254">里程碑的已记帐销售额</span><span class="sxs-lookup"><span data-stu-id="4e66b-254">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="4e66b-255">项目合同货币</span><span class="sxs-lookup"><span data-stu-id="4e66b-255">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="4e66b-256">不适用</span><span class="sxs-lookup"><span data-stu-id="4e66b-256">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="4e66b-257">不适用</span><span class="sxs-lookup"><span data-stu-id="4e66b-257">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4e66b-258">已记帐销售额</span><span class="sxs-lookup"><span data-stu-id="4e66b-258">Billed sales</span></span></td>
<td><span data-ttu-id="4e66b-259">项目合同货币</span><span class="sxs-lookup"><span data-stu-id="4e66b-259">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="4e66b-260">确认发票，并且可记帐工时减少。</span><span class="sxs-lookup"><span data-stu-id="4e66b-260">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="4e66b-261">未记帐销售额冲销</span><span class="sxs-lookup"><span data-stu-id="4e66b-261">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="4e66b-262">项目合同货币</span><span class="sxs-lookup"><span data-stu-id="4e66b-262">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="4e66b-263">不适用</span><span class="sxs-lookup"><span data-stu-id="4e66b-263">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="4e66b-264">不适用</span><span class="sxs-lookup"><span data-stu-id="4e66b-264">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="4e66b-265">不适用</span><span class="sxs-lookup"><span data-stu-id="4e66b-265">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="4e66b-266">不适用</span><span class="sxs-lookup"><span data-stu-id="4e66b-266">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4e66b-267">已记帐销售额 – 新数量的应计值</span><span class="sxs-lookup"><span data-stu-id="4e66b-267">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="4e66b-268">项目合同货币</span><span class="sxs-lookup"><span data-stu-id="4e66b-268">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4e66b-269">已记帐实际销售额 – 差额的非应计值</span><span class="sxs-lookup"><span data-stu-id="4e66b-269">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="4e66b-270">项目合同货币</span><span class="sxs-lookup"><span data-stu-id="4e66b-270">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="4e66b-271">更正发票以增加应计费数量。</span><span class="sxs-lookup"><span data-stu-id="4e66b-271">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="4e66b-272">已记帐销售额 - 冲销</span><span class="sxs-lookup"><span data-stu-id="4e66b-272">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="4e66b-273">项目合同货币</span><span class="sxs-lookup"><span data-stu-id="4e66b-273">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="4e66b-274">里程碑的已记帐销售额冲销</span><span class="sxs-lookup"><span data-stu-id="4e66b-274">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="4e66b-275">里程碑状态从<strong>已开票</strong>更改为<strong>准备好开票</strong></span><span class="sxs-lookup"><span data-stu-id="4e66b-275">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="4e66b-276">项目合同货币</span><span class="sxs-lookup"><span data-stu-id="4e66b-276">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="4e66b-277">不适用</span><span class="sxs-lookup"><span data-stu-id="4e66b-277">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="4e66b-278">不适用</span><span class="sxs-lookup"><span data-stu-id="4e66b-278">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4e66b-279">已记帐销售额</span><span class="sxs-lookup"><span data-stu-id="4e66b-279">Billed sales</span></span></td>
<td><span data-ttu-id="4e66b-280">项目合同货币</span><span class="sxs-lookup"><span data-stu-id="4e66b-280">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="4e66b-281">更正发票以减少应计费数量。</span><span class="sxs-lookup"><span data-stu-id="4e66b-281">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="4e66b-282">已记帐销售额 - 冲销</span><span class="sxs-lookup"><span data-stu-id="4e66b-282">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="4e66b-283">项目合同货币</span><span class="sxs-lookup"><span data-stu-id="4e66b-283">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4e66b-284">新数量的已记帐销售额</span><span class="sxs-lookup"><span data-stu-id="4e66b-284">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="4e66b-285">项目合同货币</span><span class="sxs-lookup"><span data-stu-id="4e66b-285">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4e66b-286">未记帐销售额 – 差额的应计值</span><span class="sxs-lookup"><span data-stu-id="4e66b-286">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="4e66b-287">项目合同货币</span><span class="sxs-lookup"><span data-stu-id="4e66b-287">Project contract currency</span></span></td>
</tr>
</tbody>
</table>
