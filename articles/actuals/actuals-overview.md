---
title: 实际值主页
description: 此主题提供有关如何在 Microsoft Dynamics 365 Project Operations 中使用实际值的信息。
author: rumant
manager: AnnBe
ms.date: 09/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: ''
ms.search.industry: ''
ms.author: rumant
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 75ad336a995aba3505325466433a5c5e2bb3e776
ms.sourcegitcommit: 56c42d7f5995a674426a1c2a81bae897dceb391c
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/01/2020
ms.locfileid: "3907307"
---
# <a name="actuals"></a><span data-ttu-id="dd2ce-103">实际值</span><span class="sxs-lookup"><span data-stu-id="dd2ce-103">Actuals</span></span>

<span data-ttu-id="dd2ce-104">_**适用于：** 面向资源/非库存场景的 Project Operations_</span><span class="sxs-lookup"><span data-stu-id="dd2ce-104">_**Applies to:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="dd2ce-105">实际值是已完成的项目工作量。</span><span class="sxs-lookup"><span data-stu-id="dd2ce-105">Actuals are the amount of work that has been completed on a project.</span></span> <span data-ttu-id="dd2ce-106">它们是根据时间和支出条目以及日记帐条目和发票创建的。</span><span class="sxs-lookup"><span data-stu-id="dd2ce-106">They are created as a result of time and expense entries, and journal entries and invoices.</span></span>

## <a name="journal-lines-and-time-submission"></a><span data-ttu-id="dd2ce-107">日记帐行和时间提交</span><span class="sxs-lookup"><span data-stu-id="dd2ce-107">Journal lines and time submission</span></span>

<span data-ttu-id="dd2ce-108">有关时间条目的详细信息，请参阅[时间条目概述](../time/time-entry-overview.md)。</span><span class="sxs-lookup"><span data-stu-id="dd2ce-108">For more information about time entry, see [Time entry overview](../time/time-entry-overview.md).</span></span>

### <a name="time-and-materials"></a><span data-ttu-id="dd2ce-109">时间和材料</span><span class="sxs-lookup"><span data-stu-id="dd2ce-109">Time and materials</span></span>

<span data-ttu-id="dd2ce-110">当提交的时间条目链接到映射到时间和材料合同子项的项目时，系统将创建两个日记帐行，一个用于成本，一个用于未记帐销售。</span><span class="sxs-lookup"><span data-stu-id="dd2ce-110">When a time entry that is submitted is linked to a project that is mapped to a time-and-materials contract line, the system creates two journal lines, one for cost and one for unbilled sales.</span></span>

### <a name="fixed-price"></a><span data-ttu-id="dd2ce-111">固定价格</span><span class="sxs-lookup"><span data-stu-id="dd2ce-111">Fixed price</span></span>

<span data-ttu-id="dd2ce-112">当提交的时间条目链接到映射到固定价格合同子项的项目时，系统将为成本创建一个日记帐行。</span><span class="sxs-lookup"><span data-stu-id="dd2ce-112">When a time entry that is submitted is linked to a project that is mapped to a fixed-price contract line, the system creates one journal line for cost.</span></span>

### <a name="default-pricing"></a><span data-ttu-id="dd2ce-113">默认定价</span><span class="sxs-lookup"><span data-stu-id="dd2ce-113">Default pricing</span></span>

<span data-ttu-id="dd2ce-114">有关创建默认价格的逻辑在日记帐行中。</span><span class="sxs-lookup"><span data-stu-id="dd2ce-114">The logic for creating default prices resides on the journal line.</span></span> <span data-ttu-id="dd2ce-115">时间条目中的字段值将复制到该日记帐行中。</span><span class="sxs-lookup"><span data-stu-id="dd2ce-115">The field values from the time entry are copied to the journal line.</span></span> <span data-ttu-id="dd2ce-116">这些值包含交易日期、项目映射到的合同子项，以及相应价目表中的货币结果。</span><span class="sxs-lookup"><span data-stu-id="dd2ce-116">These values include the transaction date, the contract line that the project is mapped to, and the currency result in the appropriate price list.</span></span>

<span data-ttu-id="dd2ce-117">会影响默认定价的字段（如**角色**和**部门**）用于确定日记帐行中的适当价格。</span><span class="sxs-lookup"><span data-stu-id="dd2ce-117">The fields that affect default pricing, such as **Role** and **Org Unit**, are used to determine the appropriate price on the journal line.</span></span> <span data-ttu-id="dd2ce-118">您可以在时间条目中添加自定义字段。</span><span class="sxs-lookup"><span data-stu-id="dd2ce-118">You can add a custom field on the time entry.</span></span> <span data-ttu-id="dd2ce-119">如果您希望将字段值传播到实际值，请在实际值条目中创建字段，然后使用字段映射将该字段从时间条目复制到实际值。</span><span class="sxs-lookup"><span data-stu-id="dd2ce-119">If you want the field value to be propagated to actuals, create the field on the Actuals entity, and use field mappings to copy the field from the time entry to the actual.</span></span>

## <a name="journal-lines-and-basic-expense-submission"></a><span data-ttu-id="dd2ce-120">日记帐行和基本支出提交</span><span class="sxs-lookup"><span data-stu-id="dd2ce-120">Journal lines and basic expense submission</span></span>

<span data-ttu-id="dd2ce-121">有关支出条目的详细信息，请参阅[支出概述](../expense/expense-overview.md)。</span><span class="sxs-lookup"><span data-stu-id="dd2ce-121">For more information about expense entry, see [Expense overview](../expense/expense-overview.md).</span></span>

### <a name="time-and-materials"></a><span data-ttu-id="dd2ce-122">时间和材料</span><span class="sxs-lookup"><span data-stu-id="dd2ce-122">Time and materials</span></span>

<span data-ttu-id="dd2ce-123">当提交的基本支出条目链接到映射到时间和材料合同子项的项目时，系统将创建两个日记帐行，一个用于成本，一个用于未记帐销售。</span><span class="sxs-lookup"><span data-stu-id="dd2ce-123">When a basic expense entry that is submitted is linked to a project that is mapped to a time-and-materials contract line, the system creates two journal lines, one for cost and one for unbilled sales.</span></span>

### <a name="fixed-price"></a><span data-ttu-id="dd2ce-124">固定价格</span><span class="sxs-lookup"><span data-stu-id="dd2ce-124">Fixed price</span></span>

<span data-ttu-id="dd2ce-125">当提交的基本支出条目链接到映射到固定价格合同子项的项目时，系统将为成本创建一个日记帐行。</span><span class="sxs-lookup"><span data-stu-id="dd2ce-125">When a basic expense entry that is submitted is linked to a project that is mapped to a fixed-price contract line, the system creates one journal line for cost.</span></span>

### <a name="default-pricing"></a><span data-ttu-id="dd2ce-126">默认定价</span><span class="sxs-lookup"><span data-stu-id="dd2ce-126">Default pricing</span></span>

<span data-ttu-id="dd2ce-127">为支出输入默认价格的逻辑基于支出类别。</span><span class="sxs-lookup"><span data-stu-id="dd2ce-127">The logic for entering default prices for expenses is based on the expense category.</span></span> <span data-ttu-id="dd2ce-128">交易日期、项目映射到的合同子项，以及货币全部用于确定相应价目表。</span><span class="sxs-lookup"><span data-stu-id="dd2ce-128">The transaction date, the contract line that the project is mapped to, and the currency are all used to determine the appropriate price list.</span></span> <span data-ttu-id="dd2ce-129">但是，默认情况下，将直接在成本和销售额的相关支出日记帐行中设置为价格本身输入的金额。</span><span class="sxs-lookup"><span data-stu-id="dd2ce-129">However, by default, the amount that is entered for the price itself is set directly on the related expense journal lines for cost and sales.</span></span>

<span data-ttu-id="dd2ce-130">不能在支出条目中基于类别输入默认单价。</span><span class="sxs-lookup"><span data-stu-id="dd2ce-130">Category-based entry of per-unit default prices on expense entries isn't available.</span></span>

## <a name="use-entry-journals-to-record-costs"></a><span data-ttu-id="dd2ce-131">使用条目日记帐记录成本</span><span class="sxs-lookup"><span data-stu-id="dd2ce-131">Use entry journals to record costs</span></span>

<span data-ttu-id="dd2ce-132">您可以使用条目日记帐记录材料、费用、时间、支出或税务交易类的成本或收入。</span><span class="sxs-lookup"><span data-stu-id="dd2ce-132">You can use entry journals to record the cost or revenue in the material, fee, time, expense, or tax transaction classes.</span></span> <span data-ttu-id="dd2ce-133">日记帐可以用于以下目的：</span><span class="sxs-lookup"><span data-stu-id="dd2ce-133">Journals can be used for the following purposes:</span></span>

- <span data-ttu-id="dd2ce-134">记录项目的材料实际成本和销售额。</span><span class="sxs-lookup"><span data-stu-id="dd2ce-134">Record the actual cost of materials and sales on a project.</span></span>
- <span data-ttu-id="dd2ce-135">将交易实际值从另一个系统移至 Microsoft Dynamics 365 Project Operations。</span><span class="sxs-lookup"><span data-stu-id="dd2ce-135">Move transaction actuals from another system to Microsoft Dynamics 365 Project Operations.</span></span>
- <span data-ttu-id="dd2ce-136">记录另一个系统中发生的成本。</span><span class="sxs-lookup"><span data-stu-id="dd2ce-136">Record costs that occurred in another system.</span></span> <span data-ttu-id="dd2ce-137">这些成本可能包括采购成本或分包成本。</span><span class="sxs-lookup"><span data-stu-id="dd2ce-137">These costs can include procurement or subcontracting costs.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="dd2ce-138">应用程序不验证日记帐行类型或在日记帐行中输入的相关定价。</span><span class="sxs-lookup"><span data-stu-id="dd2ce-138">The application doesn't validate the journal line type or the related pricing that is entered on the journal line.</span></span> <span data-ttu-id="dd2ce-139">因此，只有完全了解实际值对项目产生的会计影响的用户才应使用条目日记帐创建实际值。</span><span class="sxs-lookup"><span data-stu-id="dd2ce-139">Therefore, only a user who is fully aware of the accounting impact that actuals have on the project should use entry journals to create actuals.</span></span> <span data-ttu-id="dd2ce-140">由于此日记帐类型的影响，您应该仔细选择有权创建条目日记帐的人。</span><span class="sxs-lookup"><span data-stu-id="dd2ce-140">Because of the impact of this journal type, you should carefully choose who has access to create entry journals.</span></span>
## <a name="record-actuals-based-on-project-events"></a><span data-ttu-id="dd2ce-141">基于项目事件记录实际值</span><span class="sxs-lookup"><span data-stu-id="dd2ce-141">Record actuals based on project events</span></span>

<span data-ttu-id="dd2ce-142">Project Operations 记录项目期间发生的财务交易。</span><span class="sxs-lookup"><span data-stu-id="dd2ce-142">Project Operations records the financial transactions that occur during a project.</span></span> <span data-ttu-id="dd2ce-143">这些交易记录为实际值。</span><span class="sxs-lookup"><span data-stu-id="dd2ce-143">These transactions are recorded as actuals.</span></span> <span data-ttu-id="dd2ce-144">下表显示创建的不同类型的实际值，具体取决于项目是时间和材料还是固定价格，是否处于售前阶段，是否为内部项目。</span><span class="sxs-lookup"><span data-stu-id="dd2ce-144">The following tables show the different types of actuals that are created, depending on whether the project is a time-and-materials or fixed-price project, is in the presales stage, or is an internal project.</span></span>

### <a name="the-resource-belongs-to-same-organizational-unit-as-the-projects-contracting-unit"></a><span data-ttu-id="dd2ce-145">资源与项目的合同签订部门属于同一个部门</span><span class="sxs-lookup"><span data-stu-id="dd2ce-145">The resource belongs to same organizational unit as the project's contracting unit</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="dd2ce-146">事件</span><span class="sxs-lookup"><span data-stu-id="dd2ce-146">Event</span></span></th>
<th colspan="4"><span data-ttu-id="dd2ce-147">可记帐项目或已售项目</span><span class="sxs-lookup"><span data-stu-id="dd2ce-147">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="dd2ce-148">售前阶段的项目</span><span class="sxs-lookup"><span data-stu-id="dd2ce-148">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="dd2ce-149">内部项目</span><span class="sxs-lookup"><span data-stu-id="dd2ce-149">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="dd2ce-150">时间和材料</span><span class="sxs-lookup"><span data-stu-id="dd2ce-150">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="dd2ce-151">固定价格</span><span class="sxs-lookup"><span data-stu-id="dd2ce-151">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="dd2ce-152">实际</span><span class="sxs-lookup"><span data-stu-id="dd2ce-152">Actuals</span></span></th>
<th><span data-ttu-id="dd2ce-153">交易货币</span><span class="sxs-lookup"><span data-stu-id="dd2ce-153">Transaction currency</span></span></th>
<th><span data-ttu-id="dd2ce-154">固定价格</span><span class="sxs-lookup"><span data-stu-id="dd2ce-154">Fixed price</span></span></th>
<th><span data-ttu-id="dd2ce-155">交易货币</span><span class="sxs-lookup"><span data-stu-id="dd2ce-155">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="dd2ce-156">创建时间条目。</span><span class="sxs-lookup"><span data-stu-id="dd2ce-156">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="dd2ce-157">实际值条目中无活动</span><span class="sxs-lookup"><span data-stu-id="dd2ce-157">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="dd2ce-158">提交时间条目。</span><span class="sxs-lookup"><span data-stu-id="dd2ce-158">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="dd2ce-159">实际值条目中无活动</span><span class="sxs-lookup"><span data-stu-id="dd2ce-159">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="dd2ce-160">批准时间，并且审批期间可记帐工时不变或不增加。</span><span class="sxs-lookup"><span data-stu-id="dd2ce-160">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="dd2ce-161">成本实际值</span><span class="sxs-lookup"><span data-stu-id="dd2ce-161">Cost actual</span></span></td>
<td><span data-ttu-id="dd2ce-162">合同签订部门货币</span><span class="sxs-lookup"><span data-stu-id="dd2ce-162">Contracting unit currency</span></span></td>
<td rowspan="2"><span data-ttu-id="dd2ce-163">实际成本</span><span class="sxs-lookup"><span data-stu-id="dd2ce-163">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="dd2ce-164">合同签订部门货币</span><span class="sxs-lookup"><span data-stu-id="dd2ce-164">Contracting unit currency</span></span>
<td rowspan="2"><span data-ttu-id="dd2ce-165">成本实际值</span><span class="sxs-lookup"><span data-stu-id="dd2ce-165">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="dd2ce-166">成本实际值</span><span class="sxs-lookup"><span data-stu-id="dd2ce-166">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="dd2ce-167">未记帐实际销售额 – 应计费</span><span class="sxs-lookup"><span data-stu-id="dd2ce-167">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="dd2ce-168">项目合同货币</span><span class="sxs-lookup"><span data-stu-id="dd2ce-168">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="dd2ce-169">批准时间，并且审批期间可记帐工时不变或不减少。</span><span class="sxs-lookup"><span data-stu-id="dd2ce-169">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="dd2ce-170">实际成本</span><span class="sxs-lookup"><span data-stu-id="dd2ce-170">Cost actual</span></span></td>
<td><span data-ttu-id="dd2ce-171">合同签订部门货币</span><span class="sxs-lookup"><span data-stu-id="dd2ce-171">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="dd2ce-172">实际成本</span><span class="sxs-lookup"><span data-stu-id="dd2ce-172">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="dd2ce-173">合同签订部门货币</span><span class="sxs-lookup"><span data-stu-id="dd2ce-173">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="dd2ce-174">实际成本</span><span class="sxs-lookup"><span data-stu-id="dd2ce-174">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="dd2ce-175">实际成本</span><span class="sxs-lookup"><span data-stu-id="dd2ce-175">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="dd2ce-176">未记帐实际销售额 – 新数量的应计值</span><span class="sxs-lookup"><span data-stu-id="dd2ce-176">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="dd2ce-177">项目合同货币</span><span class="sxs-lookup"><span data-stu-id="dd2ce-177">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="dd2ce-178">未记帐实际销售额 – 差额的非应计值</span><span class="sxs-lookup"><span data-stu-id="dd2ce-178">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="dd2ce-179">项目合同货币</span><span class="sxs-lookup"><span data-stu-id="dd2ce-179">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="dd2ce-180">确认发票，并且审批期间可记帐工时不变或不增加。</span><span class="sxs-lookup"><span data-stu-id="dd2ce-180">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="dd2ce-181">未记帐销售额冲销</span><span class="sxs-lookup"><span data-stu-id="dd2ce-181">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="dd2ce-182">项目合同货币</span><span class="sxs-lookup"><span data-stu-id="dd2ce-182">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="dd2ce-183">里程碑的已记帐销售额</span><span class="sxs-lookup"><span data-stu-id="dd2ce-183">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="dd2ce-184">项目合同货币</span><span class="sxs-lookup"><span data-stu-id="dd2ce-184">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="dd2ce-185">不适用</span><span class="sxs-lookup"><span data-stu-id="dd2ce-185">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="dd2ce-186">不适用</span><span class="sxs-lookup"><span data-stu-id="dd2ce-186">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="dd2ce-187">已记帐销售额</span><span class="sxs-lookup"><span data-stu-id="dd2ce-187">Billed sales</span></span></td>
<td><span data-ttu-id="dd2ce-188">项目合同货币</span><span class="sxs-lookup"><span data-stu-id="dd2ce-188">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="dd2ce-189">确认发票，并且可记帐工时减少。</span><span class="sxs-lookup"><span data-stu-id="dd2ce-189">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="dd2ce-190">未记帐销售额冲销</span><span class="sxs-lookup"><span data-stu-id="dd2ce-190">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="dd2ce-191">项目合同货币</span><span class="sxs-lookup"><span data-stu-id="dd2ce-191">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="dd2ce-192">不适用</span><span class="sxs-lookup"><span data-stu-id="dd2ce-192">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="dd2ce-193">不适用</span><span class="sxs-lookup"><span data-stu-id="dd2ce-193">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="dd2ce-194">不适用</span><span class="sxs-lookup"><span data-stu-id="dd2ce-194">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="dd2ce-195">不适用</span><span class="sxs-lookup"><span data-stu-id="dd2ce-195">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="dd2ce-196">已记帐销售额 – 新数量的应计值</span><span class="sxs-lookup"><span data-stu-id="dd2ce-196">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="dd2ce-197">项目合同货币</span><span class="sxs-lookup"><span data-stu-id="dd2ce-197">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="dd2ce-198">已记帐实际销售额 – 差额的非应计值</span><span class="sxs-lookup"><span data-stu-id="dd2ce-198">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="dd2ce-199">项目合同货币</span><span class="sxs-lookup"><span data-stu-id="dd2ce-199">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="dd2ce-200">更正发票以增加应计费数量。</span><span class="sxs-lookup"><span data-stu-id="dd2ce-200">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="dd2ce-201">已记帐销售额 - 冲销</span><span class="sxs-lookup"><span data-stu-id="dd2ce-201">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="dd2ce-202">项目合同货币</span><span class="sxs-lookup"><span data-stu-id="dd2ce-202">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="dd2ce-203">里程碑的已记帐销售额冲销</span><span class="sxs-lookup"><span data-stu-id="dd2ce-203">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="dd2ce-204">里程碑状态从<strong>已开票</strong>更改为<strong>准备好开票</strong></span><span class="sxs-lookup"><span data-stu-id="dd2ce-204">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="dd2ce-205">项目合同货币</span><span class="sxs-lookup"><span data-stu-id="dd2ce-205">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="dd2ce-206">不适用</span><span class="sxs-lookup"><span data-stu-id="dd2ce-206">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="dd2ce-207">不适用</span><span class="sxs-lookup"><span data-stu-id="dd2ce-207">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="dd2ce-208">已记帐销售额</span><span class="sxs-lookup"><span data-stu-id="dd2ce-208">Billed sales</span></span></td>
<td><span data-ttu-id="dd2ce-209">项目合同货币</span><span class="sxs-lookup"><span data-stu-id="dd2ce-209">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="dd2ce-210">更正发票以减少应计费数量。</span><span class="sxs-lookup"><span data-stu-id="dd2ce-210">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="dd2ce-211">已记帐销售额 - 冲销</span><span class="sxs-lookup"><span data-stu-id="dd2ce-211">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="dd2ce-212">项目合同货币</span><span class="sxs-lookup"><span data-stu-id="dd2ce-212">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="dd2ce-213">新数量的已记帐销售额</span><span class="sxs-lookup"><span data-stu-id="dd2ce-213">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="dd2ce-214">项目合同货币</span><span class="sxs-lookup"><span data-stu-id="dd2ce-214">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="dd2ce-215">未记帐销售额 – 差额的应计值</span><span class="sxs-lookup"><span data-stu-id="dd2ce-215">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="dd2ce-216">项目合同货币</span><span class="sxs-lookup"><span data-stu-id="dd2ce-216">Project contract currency</span></span></td>
</tr>
</tbody>
</table>

### <a name="the-resource-belongs-to-an-organizational-unit-that-differs-from-the-projects-contracting-unit"></a><span data-ttu-id="dd2ce-217">资源与项目的合同签订部门不属于同一个部门</span><span class="sxs-lookup"><span data-stu-id="dd2ce-217">The resource belongs to an organizational unit that differs from the project's contracting unit</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="dd2ce-218">事件</span><span class="sxs-lookup"><span data-stu-id="dd2ce-218">Event</span></span></th>
<th colspan="4"><span data-ttu-id="dd2ce-219">可记帐项目或已售项目</span><span class="sxs-lookup"><span data-stu-id="dd2ce-219">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="dd2ce-220">售前阶段的项目</span><span class="sxs-lookup"><span data-stu-id="dd2ce-220">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="dd2ce-221">内部项目</span><span class="sxs-lookup"><span data-stu-id="dd2ce-221">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="dd2ce-222">时间和材料</span><span class="sxs-lookup"><span data-stu-id="dd2ce-222">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="dd2ce-223">固定价格</span><span class="sxs-lookup"><span data-stu-id="dd2ce-223">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="dd2ce-224">实际</span><span class="sxs-lookup"><span data-stu-id="dd2ce-224">Actuals</span></span></th>
<th><span data-ttu-id="dd2ce-225">交易货币</span><span class="sxs-lookup"><span data-stu-id="dd2ce-225">Transaction currency</span></span></th>
<th><span data-ttu-id="dd2ce-226">固定价格</span><span class="sxs-lookup"><span data-stu-id="dd2ce-226">Fixed price</span></span></th>
<th><span data-ttu-id="dd2ce-227">交易货币</span><span class="sxs-lookup"><span data-stu-id="dd2ce-227">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="dd2ce-228">创建时间条目。</span><span class="sxs-lookup"><span data-stu-id="dd2ce-228">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="dd2ce-229">实际值条目中无活动</span><span class="sxs-lookup"><span data-stu-id="dd2ce-229">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="dd2ce-230">提交时间条目。</span><span class="sxs-lookup"><span data-stu-id="dd2ce-230">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="dd2ce-231">实际值条目中无活动</span><span class="sxs-lookup"><span data-stu-id="dd2ce-231">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="4"><span data-ttu-id="dd2ce-232">批准时间，并且审批期间可记帐工时不变或不增加。</span><span class="sxs-lookup"><span data-stu-id="dd2ce-232">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="dd2ce-233">成本实际值</span><span class="sxs-lookup"><span data-stu-id="dd2ce-233">Cost actual</span></span></td>
<td><span data-ttu-id="dd2ce-234">合同签订部门货币</span><span class="sxs-lookup"><span data-stu-id="dd2ce-234">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="dd2ce-235">实际成本</span><span class="sxs-lookup"><span data-stu-id="dd2ce-235">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="dd2ce-236">合同签订部门货币</span><span class="sxs-lookup"><span data-stu-id="dd2ce-236">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="dd2ce-237">成本实际值</span><span class="sxs-lookup"><span data-stu-id="dd2ce-237">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="dd2ce-238">成本实际值</span><span class="sxs-lookup"><span data-stu-id="dd2ce-238">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="dd2ce-239">未记帐实际销售额 – 应计费</span><span class="sxs-lookup"><span data-stu-id="dd2ce-239">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="dd2ce-240">项目合同货币</span><span class="sxs-lookup"><span data-stu-id="dd2ce-240">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="dd2ce-241">资源单位成本</span><span class="sxs-lookup"><span data-stu-id="dd2ce-241">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="dd2ce-242">资源单位货币</span><span class="sxs-lookup"><span data-stu-id="dd2ce-242">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="dd2ce-243">组织间销售</span><span class="sxs-lookup"><span data-stu-id="dd2ce-243">Interorganizational sales</span></span></td>
<td><span data-ttu-id="dd2ce-244">合同签订部门货币</span><span class="sxs-lookup"><span data-stu-id="dd2ce-244">Contracting unit currency</span></span></td>
</tr>
<tr>
<td rowspan="5"><span data-ttu-id="dd2ce-245">批准时间，并且审批期间可记帐工时不变或不减少。</span><span class="sxs-lookup"><span data-stu-id="dd2ce-245">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="dd2ce-246">实际成本</span><span class="sxs-lookup"><span data-stu-id="dd2ce-246">Cost actual</span></span></td>
<td><span data-ttu-id="dd2ce-247">合同签订部门货币</span><span class="sxs-lookup"><span data-stu-id="dd2ce-247">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="dd2ce-248">实际成本</span><span class="sxs-lookup"><span data-stu-id="dd2ce-248">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="dd2ce-249">合同签订部门货币</span><span class="sxs-lookup"><span data-stu-id="dd2ce-249">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="dd2ce-250">实际成本</span><span class="sxs-lookup"><span data-stu-id="dd2ce-250">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="dd2ce-251">实际成本</span><span class="sxs-lookup"><span data-stu-id="dd2ce-251">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="dd2ce-252">资源单位成本</span><span class="sxs-lookup"><span data-stu-id="dd2ce-252">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="dd2ce-253">资源单位货币</span><span class="sxs-lookup"><span data-stu-id="dd2ce-253">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="dd2ce-254">组织间销售</span><span class="sxs-lookup"><span data-stu-id="dd2ce-254">Interorganizational sales</span></span></td>
<td><span data-ttu-id="dd2ce-255">合同签订部门货币</span><span class="sxs-lookup"><span data-stu-id="dd2ce-255">Contracting unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="dd2ce-256">未记帐实际销售额 – 新数量的应计值</span><span class="sxs-lookup"><span data-stu-id="dd2ce-256">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="dd2ce-257">项目合同货币</span><span class="sxs-lookup"><span data-stu-id="dd2ce-257">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="dd2ce-258">未记帐实际销售额 – 差额的非应计值</span><span class="sxs-lookup"><span data-stu-id="dd2ce-258">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="dd2ce-259">项目合同货币</span><span class="sxs-lookup"><span data-stu-id="dd2ce-259">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="dd2ce-260">确认发票，并且审批期间可记帐工时不变或不增加。</span><span class="sxs-lookup"><span data-stu-id="dd2ce-260">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="dd2ce-261">未记帐销售额冲销</span><span class="sxs-lookup"><span data-stu-id="dd2ce-261">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="dd2ce-262">项目合同货币</span><span class="sxs-lookup"><span data-stu-id="dd2ce-262">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="dd2ce-263">里程碑的已记帐销售额</span><span class="sxs-lookup"><span data-stu-id="dd2ce-263">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="dd2ce-264">项目合同货币</span><span class="sxs-lookup"><span data-stu-id="dd2ce-264">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="dd2ce-265">不适用</span><span class="sxs-lookup"><span data-stu-id="dd2ce-265">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="dd2ce-266">不适用</span><span class="sxs-lookup"><span data-stu-id="dd2ce-266">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="dd2ce-267">已记帐销售额</span><span class="sxs-lookup"><span data-stu-id="dd2ce-267">Billed sales</span></span></td>
<td><span data-ttu-id="dd2ce-268">项目合同货币</span><span class="sxs-lookup"><span data-stu-id="dd2ce-268">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="dd2ce-269">确认发票，并且可记帐工时减少。</span><span class="sxs-lookup"><span data-stu-id="dd2ce-269">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="dd2ce-270">未记帐销售额冲销</span><span class="sxs-lookup"><span data-stu-id="dd2ce-270">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="dd2ce-271">项目合同货币</span><span class="sxs-lookup"><span data-stu-id="dd2ce-271">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="dd2ce-272">不适用</span><span class="sxs-lookup"><span data-stu-id="dd2ce-272">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="dd2ce-273">不适用</span><span class="sxs-lookup"><span data-stu-id="dd2ce-273">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="dd2ce-274">不适用</span><span class="sxs-lookup"><span data-stu-id="dd2ce-274">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="dd2ce-275">不适用</span><span class="sxs-lookup"><span data-stu-id="dd2ce-275">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="dd2ce-276">已记帐销售额 – 新数量的应计值</span><span class="sxs-lookup"><span data-stu-id="dd2ce-276">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="dd2ce-277">项目合同货币</span><span class="sxs-lookup"><span data-stu-id="dd2ce-277">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="dd2ce-278">已记帐实际销售额 – 差额的非应计值</span><span class="sxs-lookup"><span data-stu-id="dd2ce-278">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="dd2ce-279">项目合同货币</span><span class="sxs-lookup"><span data-stu-id="dd2ce-279">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="dd2ce-280">更正发票以增加应计费数量。</span><span class="sxs-lookup"><span data-stu-id="dd2ce-280">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="dd2ce-281">已记帐销售额 - 冲销</span><span class="sxs-lookup"><span data-stu-id="dd2ce-281">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="dd2ce-282">项目合同货币</span><span class="sxs-lookup"><span data-stu-id="dd2ce-282">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="dd2ce-283">里程碑的已记帐销售额冲销</span><span class="sxs-lookup"><span data-stu-id="dd2ce-283">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="dd2ce-284">里程碑状态从<strong>已开票</strong>更改为<strong>准备好开票</strong></span><span class="sxs-lookup"><span data-stu-id="dd2ce-284">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="dd2ce-285">项目合同货币</span><span class="sxs-lookup"><span data-stu-id="dd2ce-285">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="dd2ce-286">不适用</span><span class="sxs-lookup"><span data-stu-id="dd2ce-286">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="dd2ce-287">不适用</span><span class="sxs-lookup"><span data-stu-id="dd2ce-287">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="dd2ce-288">已记帐销售额</span><span class="sxs-lookup"><span data-stu-id="dd2ce-288">Billed sales</span></span></td>
<td><span data-ttu-id="dd2ce-289">项目合同货币</span><span class="sxs-lookup"><span data-stu-id="dd2ce-289">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="dd2ce-290">更正发票以减少应计费数量。</span><span class="sxs-lookup"><span data-stu-id="dd2ce-290">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="dd2ce-291">已记帐销售额 - 冲销</span><span class="sxs-lookup"><span data-stu-id="dd2ce-291">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="dd2ce-292">项目合同货币</span><span class="sxs-lookup"><span data-stu-id="dd2ce-292">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="dd2ce-293">新数量的已记帐销售额</span><span class="sxs-lookup"><span data-stu-id="dd2ce-293">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="dd2ce-294">项目合同货币</span><span class="sxs-lookup"><span data-stu-id="dd2ce-294">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="dd2ce-295">未记帐销售额 – 差额的应计值</span><span class="sxs-lookup"><span data-stu-id="dd2ce-295">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="dd2ce-296">项目合同货币</span><span class="sxs-lookup"><span data-stu-id="dd2ce-296">Project contract currency</span></span></td>
</tr>
</tbody>
</table>
