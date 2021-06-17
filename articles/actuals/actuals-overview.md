---
title: 实际值
description: 本主题提供有关如何在 Microsoft Dynamics 365 Project Operations 中使用实际值的信息。
author: rumant
ms.date: 04/01/2021
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: ''
ms.search.industry: ''
ms.author: rumant
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 78c7a9486d0338adfd7770447f21d17509e654f7
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/10/2021
ms.locfileid: "5996600"
---
# <a name="actuals"></a><span data-ttu-id="c69f2-103">实际值</span><span class="sxs-lookup"><span data-stu-id="c69f2-103">Actuals</span></span> 

<span data-ttu-id="c69f2-104">_**适用于：** 基于资源/非库存场景的 Project Operations，精简部署 - 估价开票交易_</span><span class="sxs-lookup"><span data-stu-id="c69f2-104">_**Applies to:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="c69f2-105">实际值表示项目中已审阅和批准的财务和计划进度。</span><span class="sxs-lookup"><span data-stu-id="c69f2-105">Actuals represent the reviewed and approved financial and schedule progress on a project.</span></span> <span data-ttu-id="c69f2-106">之所以创建它们，是因为审批了时间、支出、材料使用条目以及日记帐条目和发票。</span><span class="sxs-lookup"><span data-stu-id="c69f2-106">They are created as a result of approval of time, expense, material usage entries, and journal entries and invoices.</span></span>

## <a name="journal-lines-and-time-submission"></a><span data-ttu-id="c69f2-107">日记帐行和时间提交</span><span class="sxs-lookup"><span data-stu-id="c69f2-107">Journal lines and time submission</span></span>

<span data-ttu-id="c69f2-108">有关时间条目的详细信息，请参阅[时间条目概述](../time/time-entry-overview.md)。</span><span class="sxs-lookup"><span data-stu-id="c69f2-108">For more information about time entry, see [Time entry overview](../time/time-entry-overview.md).</span></span>

### <a name="time-and-materials"></a><span data-ttu-id="c69f2-109">时间和材料</span><span class="sxs-lookup"><span data-stu-id="c69f2-109">Time and materials</span></span>

<span data-ttu-id="c69f2-110">当提交的时间条目链接到映射到时间和材料合同子项的项目时，系统将创建两个日记帐行，一个用于成本，一个用于未记帐销售。</span><span class="sxs-lookup"><span data-stu-id="c69f2-110">When a time entry that is submitted is linked to a project that is mapped to a time-and-materials contract line, the system creates two journal lines, one for cost and one for unbilled sales.</span></span>

### <a name="fixed-price"></a><span data-ttu-id="c69f2-111">固定价格</span><span class="sxs-lookup"><span data-stu-id="c69f2-111">Fixed price</span></span>

<span data-ttu-id="c69f2-112">当提交的时间条目链接到映射到固定价格合同子项的项目时，系统将为成本创建一个日记帐行。</span><span class="sxs-lookup"><span data-stu-id="c69f2-112">When a time entry that is submitted is linked to a project that is mapped to a fixed-price contract line, the system creates one journal line for cost.</span></span>

### <a name="default-pricing"></a><span data-ttu-id="c69f2-113">默认定价</span><span class="sxs-lookup"><span data-stu-id="c69f2-113">Default pricing</span></span>

<span data-ttu-id="c69f2-114">有关创建默认价格的逻辑在日记帐行中。</span><span class="sxs-lookup"><span data-stu-id="c69f2-114">The logic for creating default prices resides on the journal line.</span></span> <span data-ttu-id="c69f2-115">时间条目中的字段值将复制到该日记帐行中。</span><span class="sxs-lookup"><span data-stu-id="c69f2-115">The field values from the time entry are copied to the journal line.</span></span> <span data-ttu-id="c69f2-116">这些值包含交易日期、项目映射到的合同子项，以及相应价目表中的货币结果。</span><span class="sxs-lookup"><span data-stu-id="c69f2-116">These values include the transaction date, the contract line that the project is mapped to, and the currency result in the appropriate price list.</span></span>

<span data-ttu-id="c69f2-117">对默认定价有影响的字段（如 **角色** 和 **资源单位**）用于在日记帐行上确定相应的价格。</span><span class="sxs-lookup"><span data-stu-id="c69f2-117">The fields that affect default pricing, such as **Role** and **Resourcing Unit**, are used to determine the appropriate price on the journal line.</span></span> <span data-ttu-id="c69f2-118">您可以在时间条目中添加自定义字段。</span><span class="sxs-lookup"><span data-stu-id="c69f2-118">You can add a custom field on the time entry.</span></span> <span data-ttu-id="c69f2-119">如果希望将字段值传播到实际值，可以在 **实际值** 和 **日记帐行** 表中创建该字段。</span><span class="sxs-lookup"><span data-stu-id="c69f2-119">If you want the field value to be propagated to actuals, create the field in the **Actuals** and **Journal Line** tables.</span></span> <span data-ttu-id="c69f2-120">使用自定义代码通过日记帐行（使用交易起源）将所选字段值从“时间条目”传播到“实际值”。</span><span class="sxs-lookup"><span data-stu-id="c69f2-120">Use custom code to propagate the selected field value from Time Entry to Actuals through the journal line using transaction origins.</span></span> <span data-ttu-id="c69f2-121">有关交易起源和连接的详细信息，请参阅[将实际值链接到原始记录](linkingactuals.md#example-how-transaction-origin-works-with-transaction-connection)。</span><span class="sxs-lookup"><span data-stu-id="c69f2-121">For more information about transaction origins and connections, see [Linking Actuals to original records](linkingactuals.md#example-how-transaction-origin-works-with-transaction-connection).</span></span>

## <a name="journal-lines-and-basic-expense-submission"></a><span data-ttu-id="c69f2-122">日记帐行和基本支出提交</span><span class="sxs-lookup"><span data-stu-id="c69f2-122">Journal lines and basic expense submission</span></span>

<span data-ttu-id="c69f2-123">有关支出条目的详细信息，请参阅[支出概述](../expense/expense-overview.md)。</span><span class="sxs-lookup"><span data-stu-id="c69f2-123">For more information about expense entry, see [Expense overview](../expense/expense-overview.md).</span></span>

### <a name="time-and-materials"></a><span data-ttu-id="c69f2-124">时间和材料</span><span class="sxs-lookup"><span data-stu-id="c69f2-124">Time and materials</span></span>

<span data-ttu-id="c69f2-125">当提交的基本支出条目链接到映射到时间和材料合同子项的项目时，系统将创建两个日记帐行，一个用于成本，一个用于未记帐销售。</span><span class="sxs-lookup"><span data-stu-id="c69f2-125">When a basic expense entry that is submitted is linked to a project that is mapped to a time-and-materials contract line, the system creates two journal lines, one for cost and one for unbilled sales.</span></span>

### <a name="fixed-price"></a><span data-ttu-id="c69f2-126">固定价格</span><span class="sxs-lookup"><span data-stu-id="c69f2-126">Fixed price</span></span>

<span data-ttu-id="c69f2-127">将提交的基本支出条目链接到映射至固定价格合同子项的项目时，系统会为成本创建一个日记帐行。</span><span class="sxs-lookup"><span data-stu-id="c69f2-127">When a submitted basic expense entry is linked to a project that's mapped to a fixed-price contract line, the system creates one journal line for cost.</span></span>

### <a name="default-pricing"></a><span data-ttu-id="c69f2-128">默认定价</span><span class="sxs-lookup"><span data-stu-id="c69f2-128">Default pricing</span></span>

<span data-ttu-id="c69f2-129">为支出输入默认价格的逻辑基于支出类别。</span><span class="sxs-lookup"><span data-stu-id="c69f2-129">The logic for entering default prices for expenses is based on the expense category.</span></span> <span data-ttu-id="c69f2-130">交易日期、项目映射到的合同子项，以及货币全部用于确定相应价目表。</span><span class="sxs-lookup"><span data-stu-id="c69f2-130">The transaction date, the contract line that the project is mapped to, and the currency, are all used to determine the appropriate price list.</span></span> <span data-ttu-id="c69f2-131">对默认定价有影响的字段（如 **交易类别** 和 **单位**）用于在日记帐行上确定相应的价格。</span><span class="sxs-lookup"><span data-stu-id="c69f2-131">The fields that affect default pricing, such as **Transaction Category** and **Unit**, are used to determine the appropriate price on the journal line.</span></span> <span data-ttu-id="c69f2-132">不过，只有当价目表中的定价方法是 **单价** 时，这才起作用。</span><span class="sxs-lookup"><span data-stu-id="c69f2-132">However, this only works when the pricing method in the price list is **Price per unit**.</span></span> <span data-ttu-id="c69f2-133">如果定价方式为 **按成本** 或 **成本加价**，则创建支出条目时输入的价格用于成本，并且会根据定价方式计算销售日记帐行上的价格。</span><span class="sxs-lookup"><span data-stu-id="c69f2-133">If pricing method is **At cost** or **Markup over cost**, the price entered when the expense entry is created is used for cost and the price on the sales journal line is calculated based on the pricing method.</span></span> 

<span data-ttu-id="c69f2-134">您可以对支出条目添加自定义字段。</span><span class="sxs-lookup"><span data-stu-id="c69f2-134">You can add a custom field on the expense entry.</span></span> <span data-ttu-id="c69f2-135">如果希望将字段值传播到实际值，可以在 **实际值** 和 **日记帐行** 表中创建该字段。</span><span class="sxs-lookup"><span data-stu-id="c69f2-135">If you want the field value to be propagated to actuals, create the field in the **Actuals** and **Journal Line** tables.</span></span> <span data-ttu-id="c69f2-136">使用自定义代码通过日记帐行（使用交易起源）将所选字段值从“时间条目”传播到“实际值”。</span><span class="sxs-lookup"><span data-stu-id="c69f2-136">Use custom code to propagate the selected field value from Time Entry to Actuals through the journal line using transaction origins.</span></span> <span data-ttu-id="c69f2-137">有关交易起源和连接的详细信息，请参阅[将实际值链接到原始记录](linkingactuals.md#example-how-transaction-origin-works-with-transaction-connection)。</span><span class="sxs-lookup"><span data-stu-id="c69f2-137">For more information about transaction origins and connections, see [Linking Actuals to original records](linkingactuals.md#example-how-transaction-origin-works-with-transaction-connection).</span></span>

## <a name="journal-lines-and-material-usage-log-submission"></a><span data-ttu-id="c69f2-138">日记帐行和材料使用日志提交</span><span class="sxs-lookup"><span data-stu-id="c69f2-138">Journal lines and material usage log submission</span></span>

<span data-ttu-id="c69f2-139">有关支出条目的详细信息，请参阅[材料使用日志](../material/material-usage-log.md)。</span><span class="sxs-lookup"><span data-stu-id="c69f2-139">For more information about expense entry, see [Material Usage Log](../material/material-usage-log.md).</span></span>

### <a name="time-and-materials"></a><span data-ttu-id="c69f2-140">时间和材料</span><span class="sxs-lookup"><span data-stu-id="c69f2-140">Time and materials</span></span>

<span data-ttu-id="c69f2-141">当已提交的材料使用日志条目链接到映射至时间和材料合同子项的项目时，系统将创建两个日记帐行，一个是成本日记帐行，一个是未记帐销售的日记帐行。</span><span class="sxs-lookup"><span data-stu-id="c69f2-141">When a submitted material usage log entry is linked to a project that is mapped to a time and materials contract line, the system creates two journal lines, one for cost and one for unbilled sales.</span></span>

### <a name="fixed-price"></a><span data-ttu-id="c69f2-142">固定价格</span><span class="sxs-lookup"><span data-stu-id="c69f2-142">Fixed price</span></span>

<span data-ttu-id="c69f2-143">将提交的材料使用日志条目链接到映射至固定价格合同子项的项目时，系统会为成本创建一个日记帐行。</span><span class="sxs-lookup"><span data-stu-id="c69f2-143">When a submitted material usage log entry is linked to a project that is mapped to a fixed-price contract line, the system creates one journal line for cost.</span></span>

### <a name="default-pricing"></a><span data-ttu-id="c69f2-144">默认定价</span><span class="sxs-lookup"><span data-stu-id="c69f2-144">Default pricing</span></span>

<span data-ttu-id="c69f2-145">用于输入材料默认价格的逻辑基于产品和单位组合。</span><span class="sxs-lookup"><span data-stu-id="c69f2-145">The logic for entering default prices for material is based on the product and unit combination.</span></span> <span data-ttu-id="c69f2-146">交易日期、项目映射到的合同子项，以及货币全部用于确定相应价目表。</span><span class="sxs-lookup"><span data-stu-id="c69f2-146">The transaction date, the contract line that the project is mapped to, and the currency, are all used to determine the appropriate price list.</span></span> <span data-ttu-id="c69f2-147">对默认定价有影响的字段（如 **产品 ID** 和 **单位**）用于在日记帐行上确定相应的价格。</span><span class="sxs-lookup"><span data-stu-id="c69f2-147">The fields that affect default pricing, such as **Product ID** and **Unit**, are used to determine the appropriate price on the journal line.</span></span> <span data-ttu-id="c69f2-148">不过，这仅对目录产品有效。</span><span class="sxs-lookup"><span data-stu-id="c69f2-148">However, this only works for catalog products.</span></span> <span data-ttu-id="c69f2-149">对于目录外产品，创建材料使用日志条目时输入的价格用于日记帐行上的成本和销售价格。</span><span class="sxs-lookup"><span data-stu-id="c69f2-149">For write-in products, the price entered when the material usage log entry is created is used for cost and sales price on the journal lines.</span></span> 

<span data-ttu-id="c69f2-150">您可以对 **材料使用日志** 条目添加自定义字段。</span><span class="sxs-lookup"><span data-stu-id="c69f2-150">You can add a custom field on the **Material Usage Log** entry.</span></span> <span data-ttu-id="c69f2-151">如果希望将字段值传播到实际值，可以在 **实际值** 和 **日记帐行** 表中创建该字段。</span><span class="sxs-lookup"><span data-stu-id="c69f2-151">If you want the field value to be propagated to actuals, create the field in the **Actuals** and **Journal Line** tables.</span></span> <span data-ttu-id="c69f2-152">使用自定义代码通过日记帐行（使用交易起源）将所选字段值从“时间条目”传播到“实际值”。</span><span class="sxs-lookup"><span data-stu-id="c69f2-152">Use custom code to propagate the selected field value from Time Entry to Actuals through the journal line using transaction origins.</span></span> <span data-ttu-id="c69f2-153">有关交易起源和连接的详细信息，请参阅[将实际值链接到原始记录](linkingactuals.md#example-how-transaction-origin-works-with-transaction-connection)。</span><span class="sxs-lookup"><span data-stu-id="c69f2-153">For more information about transaction origins and connections, see [Linking Actuals to original records](linkingactuals.md#example-how-transaction-origin-works-with-transaction-connection).</span></span>

## <a name="use-entry-journals-to-record-costs"></a><span data-ttu-id="c69f2-154">使用条目日记帐记录成本</span><span class="sxs-lookup"><span data-stu-id="c69f2-154">Use entry journals to record costs</span></span>

<span data-ttu-id="c69f2-155">您可以使用条目日记帐记录材料、费用、时间、支出或税务交易类的成本或收入。</span><span class="sxs-lookup"><span data-stu-id="c69f2-155">You can use entry journals to record the cost or revenue in the material, fee, time, expense, or tax transaction classes.</span></span> <span data-ttu-id="c69f2-156">日记帐可以用于以下目的：</span><span class="sxs-lookup"><span data-stu-id="c69f2-156">Journals can be used for the following purposes:</span></span>

- <span data-ttu-id="c69f2-157">将交易实际值从另一个系统移到 Microsoft Dynamics 365 Project Operations。</span><span class="sxs-lookup"><span data-stu-id="c69f2-157">Move transaction actuals from another system to Microsoft Dynamics 365 Project Operations.</span></span>
- <span data-ttu-id="c69f2-158">记录另一个系统中发生的成本。</span><span class="sxs-lookup"><span data-stu-id="c69f2-158">Record costs that occurred in another system.</span></span> <span data-ttu-id="c69f2-159">这些成本可能包括采购成本或分包成本。</span><span class="sxs-lookup"><span data-stu-id="c69f2-159">These costs can include procurement or subcontracting costs.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="c69f2-160">应用程序不验证日记帐行类型或在日记帐行中输入的相关定价。</span><span class="sxs-lookup"><span data-stu-id="c69f2-160">The application doesn't validate the journal line type or the related pricing that is entered on the journal line.</span></span> <span data-ttu-id="c69f2-161">因此，只有完全了解实际值对项目产生的会计影响的用户才应使用条目日记帐创建实际值。</span><span class="sxs-lookup"><span data-stu-id="c69f2-161">Therefore, only a user who is fully aware of the accounting impact that actuals have on the project should use entry journals to create actuals.</span></span> <span data-ttu-id="c69f2-162">由于此日记帐类型的影响，您应该仔细选择有权创建条目日记帐的人。</span><span class="sxs-lookup"><span data-stu-id="c69f2-162">Because of the impact of this journal type, you should carefully choose who has access to create entry journals.</span></span>

## <a name="record-actuals-based-on-project-events"></a><span data-ttu-id="c69f2-163">基于项目事件记录实际值</span><span class="sxs-lookup"><span data-stu-id="c69f2-163">Record actuals based on project events</span></span>

<span data-ttu-id="c69f2-164">Project Operations 记录项目期间发生的财务交易。</span><span class="sxs-lookup"><span data-stu-id="c69f2-164">Project Operations records the financial transactions that occur during a project.</span></span> <span data-ttu-id="c69f2-165">这些交易记录为实际值。</span><span class="sxs-lookup"><span data-stu-id="c69f2-165">These transactions are recorded as actuals.</span></span> <span data-ttu-id="c69f2-166">下表显示创建的不同类型的实际值，具体取决于项目是时间和材料还是固定价格，是否处于售前阶段，是否为内部项目。</span><span class="sxs-lookup"><span data-stu-id="c69f2-166">The following tables show the different types of actuals that are created, depending on whether the project is a time-and-materials or fixed-price project, is in the presales stage, or is an internal project.</span></span>

### <a name="the-resource-belongs-to-same-organizational-unit-as-the-projects-contracting-unit"></a><span data-ttu-id="c69f2-167">资源与项目的合同签订部门属于同一个部门</span><span class="sxs-lookup"><span data-stu-id="c69f2-167">The resource belongs to same organizational unit as the project's contracting unit</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="c69f2-168">事件</span><span class="sxs-lookup"><span data-stu-id="c69f2-168">Event</span></span></th>
<th colspan="4"><span data-ttu-id="c69f2-169">可记帐项目或已售项目</span><span class="sxs-lookup"><span data-stu-id="c69f2-169">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="c69f2-170">售前阶段的项目</span><span class="sxs-lookup"><span data-stu-id="c69f2-170">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="c69f2-171">内部项目</span><span class="sxs-lookup"><span data-stu-id="c69f2-171">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="c69f2-172">时间和材料</span><span class="sxs-lookup"><span data-stu-id="c69f2-172">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="c69f2-173">固定价格</span><span class="sxs-lookup"><span data-stu-id="c69f2-173">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="c69f2-174">实际</span><span class="sxs-lookup"><span data-stu-id="c69f2-174">Actuals</span></span></th>
<th><span data-ttu-id="c69f2-175">交易货币</span><span class="sxs-lookup"><span data-stu-id="c69f2-175">Transaction currency</span></span></th>
<th><span data-ttu-id="c69f2-176">固定价格</span><span class="sxs-lookup"><span data-stu-id="c69f2-176">Fixed price</span></span></th>
<th><span data-ttu-id="c69f2-177">交易货币</span><span class="sxs-lookup"><span data-stu-id="c69f2-177">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="c69f2-178">创建时间条目。</span><span class="sxs-lookup"><span data-stu-id="c69f2-178">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="c69f2-179">实际值条目中无活动</span><span class="sxs-lookup"><span data-stu-id="c69f2-179">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c69f2-180">提交时间条目。</span><span class="sxs-lookup"><span data-stu-id="c69f2-180">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="c69f2-181">实际值条目中无活动</span><span class="sxs-lookup"><span data-stu-id="c69f2-181">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="c69f2-182">批准时间，并且审批期间可记帐工时不变或不增加。</span><span class="sxs-lookup"><span data-stu-id="c69f2-182">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="c69f2-183">成本实际值</span><span class="sxs-lookup"><span data-stu-id="c69f2-183">Cost actual</span></span></td>
<td><span data-ttu-id="c69f2-184">合同签订部门货币</span><span class="sxs-lookup"><span data-stu-id="c69f2-184">Contracting unit currency</span></span></td>
<td rowspan="2"><span data-ttu-id="c69f2-185">实际成本</span><span class="sxs-lookup"><span data-stu-id="c69f2-185">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="c69f2-186">合同签订部门货币</span><span class="sxs-lookup"><span data-stu-id="c69f2-186">Contracting unit currency</span></span>
<td rowspan="2"><span data-ttu-id="c69f2-187">成本实际值</span><span class="sxs-lookup"><span data-stu-id="c69f2-187">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="c69f2-188">成本实际值</span><span class="sxs-lookup"><span data-stu-id="c69f2-188">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c69f2-189">未记帐实际销售额 – 应计费</span><span class="sxs-lookup"><span data-stu-id="c69f2-189">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="c69f2-190">项目合同货币</span><span class="sxs-lookup"><span data-stu-id="c69f2-190">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="c69f2-191">批准时间，并且审批期间可记帐工时不变或不减少。</span><span class="sxs-lookup"><span data-stu-id="c69f2-191">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="c69f2-192">实际成本</span><span class="sxs-lookup"><span data-stu-id="c69f2-192">Cost actual</span></span></td>
<td><span data-ttu-id="c69f2-193">合同签订部门货币</span><span class="sxs-lookup"><span data-stu-id="c69f2-193">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="c69f2-194">实际成本</span><span class="sxs-lookup"><span data-stu-id="c69f2-194">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="c69f2-195">合同签订部门货币</span><span class="sxs-lookup"><span data-stu-id="c69f2-195">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="c69f2-196">实际成本</span><span class="sxs-lookup"><span data-stu-id="c69f2-196">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="c69f2-197">实际成本</span><span class="sxs-lookup"><span data-stu-id="c69f2-197">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c69f2-198">未记帐实际销售额 – 新数量的应计值</span><span class="sxs-lookup"><span data-stu-id="c69f2-198">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="c69f2-199">项目合同货币</span><span class="sxs-lookup"><span data-stu-id="c69f2-199">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c69f2-200">未记帐实际销售额 – 差额的非应计值</span><span class="sxs-lookup"><span data-stu-id="c69f2-200">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="c69f2-201">项目合同货币</span><span class="sxs-lookup"><span data-stu-id="c69f2-201">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="c69f2-202">确认发票，并且审批期间可记帐工时不变或不增加。</span><span class="sxs-lookup"><span data-stu-id="c69f2-202">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="c69f2-203">未记帐销售额冲销</span><span class="sxs-lookup"><span data-stu-id="c69f2-203">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="c69f2-204">项目合同货币</span><span class="sxs-lookup"><span data-stu-id="c69f2-204">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="c69f2-205">里程碑的已记帐销售额</span><span class="sxs-lookup"><span data-stu-id="c69f2-205">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="c69f2-206">项目合同货币</span><span class="sxs-lookup"><span data-stu-id="c69f2-206">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="c69f2-207">不适用</span><span class="sxs-lookup"><span data-stu-id="c69f2-207">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="c69f2-208">不适用</span><span class="sxs-lookup"><span data-stu-id="c69f2-208">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c69f2-209">已记帐销售额</span><span class="sxs-lookup"><span data-stu-id="c69f2-209">Billed sales</span></span></td>
<td><span data-ttu-id="c69f2-210">项目合同货币</span><span class="sxs-lookup"><span data-stu-id="c69f2-210">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="c69f2-211">确认发票，并且可记帐工时减少。</span><span class="sxs-lookup"><span data-stu-id="c69f2-211">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="c69f2-212">未记帐销售额冲销</span><span class="sxs-lookup"><span data-stu-id="c69f2-212">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="c69f2-213">项目合同货币</span><span class="sxs-lookup"><span data-stu-id="c69f2-213">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="c69f2-214">不适用</span><span class="sxs-lookup"><span data-stu-id="c69f2-214">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="c69f2-215">不适用</span><span class="sxs-lookup"><span data-stu-id="c69f2-215">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="c69f2-216">不适用</span><span class="sxs-lookup"><span data-stu-id="c69f2-216">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="c69f2-217">不适用</span><span class="sxs-lookup"><span data-stu-id="c69f2-217">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c69f2-218">已记帐销售额 – 新数量的应计值</span><span class="sxs-lookup"><span data-stu-id="c69f2-218">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="c69f2-219">项目合同货币</span><span class="sxs-lookup"><span data-stu-id="c69f2-219">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c69f2-220">已记帐实际销售额 – 差额的非应计值</span><span class="sxs-lookup"><span data-stu-id="c69f2-220">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="c69f2-221">项目合同货币</span><span class="sxs-lookup"><span data-stu-id="c69f2-221">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="c69f2-222">更正发票以增加应计费数量。</span><span class="sxs-lookup"><span data-stu-id="c69f2-222">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="c69f2-223">已记帐销售额 - 冲销</span><span class="sxs-lookup"><span data-stu-id="c69f2-223">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="c69f2-224">项目合同货币</span><span class="sxs-lookup"><span data-stu-id="c69f2-224">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="c69f2-225">里程碑的已记帐销售额冲销</span><span class="sxs-lookup"><span data-stu-id="c69f2-225">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="c69f2-226">里程碑状态从<strong>已开票</strong>更改为<strong>准备好开票</strong></span><span class="sxs-lookup"><span data-stu-id="c69f2-226">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="c69f2-227">项目合同货币</span><span class="sxs-lookup"><span data-stu-id="c69f2-227">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="c69f2-228">不适用</span><span class="sxs-lookup"><span data-stu-id="c69f2-228">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="c69f2-229">不适用</span><span class="sxs-lookup"><span data-stu-id="c69f2-229">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c69f2-230">已记帐销售额</span><span class="sxs-lookup"><span data-stu-id="c69f2-230">Billed sales</span></span></td>
<td><span data-ttu-id="c69f2-231">项目合同货币</span><span class="sxs-lookup"><span data-stu-id="c69f2-231">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="c69f2-232">更正发票以减少应计费数量。</span><span class="sxs-lookup"><span data-stu-id="c69f2-232">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="c69f2-233">已记帐销售额 - 冲销</span><span class="sxs-lookup"><span data-stu-id="c69f2-233">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="c69f2-234">项目合同货币</span><span class="sxs-lookup"><span data-stu-id="c69f2-234">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c69f2-235">新数量的已记帐销售额</span><span class="sxs-lookup"><span data-stu-id="c69f2-235">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="c69f2-236">项目合同货币</span><span class="sxs-lookup"><span data-stu-id="c69f2-236">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c69f2-237">未记帐销售额 – 差额的应计值</span><span class="sxs-lookup"><span data-stu-id="c69f2-237">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="c69f2-238">项目合同货币</span><span class="sxs-lookup"><span data-stu-id="c69f2-238">Project contract currency</span></span></td>
</tr>
</tbody>
</table>

### <a name="the-resource-belongs-to-an-organizational-unit-that-differs-from-the-projects-contracting-unit"></a><span data-ttu-id="c69f2-239">资源与项目的合同签订部门不属于同一个部门</span><span class="sxs-lookup"><span data-stu-id="c69f2-239">The resource belongs to an organizational unit that differs from the project's contracting unit</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="c69f2-240">事件</span><span class="sxs-lookup"><span data-stu-id="c69f2-240">Event</span></span></th>
<th colspan="4"><span data-ttu-id="c69f2-241">可记帐项目或已售项目</span><span class="sxs-lookup"><span data-stu-id="c69f2-241">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="c69f2-242">售前阶段的项目</span><span class="sxs-lookup"><span data-stu-id="c69f2-242">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="c69f2-243">内部项目</span><span class="sxs-lookup"><span data-stu-id="c69f2-243">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="c69f2-244">时间和材料</span><span class="sxs-lookup"><span data-stu-id="c69f2-244">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="c69f2-245">固定价格</span><span class="sxs-lookup"><span data-stu-id="c69f2-245">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="c69f2-246">实际</span><span class="sxs-lookup"><span data-stu-id="c69f2-246">Actuals</span></span></th>
<th><span data-ttu-id="c69f2-247">交易货币</span><span class="sxs-lookup"><span data-stu-id="c69f2-247">Transaction currency</span></span></th>
<th><span data-ttu-id="c69f2-248">固定价格</span><span class="sxs-lookup"><span data-stu-id="c69f2-248">Fixed price</span></span></th>
<th><span data-ttu-id="c69f2-249">交易货币</span><span class="sxs-lookup"><span data-stu-id="c69f2-249">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="c69f2-250">创建时间条目。</span><span class="sxs-lookup"><span data-stu-id="c69f2-250">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="c69f2-251">实际值条目中无活动</span><span class="sxs-lookup"><span data-stu-id="c69f2-251">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c69f2-252">提交时间条目。</span><span class="sxs-lookup"><span data-stu-id="c69f2-252">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="c69f2-253">实际值条目中无活动</span><span class="sxs-lookup"><span data-stu-id="c69f2-253">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="4"><span data-ttu-id="c69f2-254">批准时间，并且审批期间可记帐工时不变或不增加。</span><span class="sxs-lookup"><span data-stu-id="c69f2-254">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="c69f2-255">成本实际值</span><span class="sxs-lookup"><span data-stu-id="c69f2-255">Cost actual</span></span></td>
<td><span data-ttu-id="c69f2-256">合同签订部门货币</span><span class="sxs-lookup"><span data-stu-id="c69f2-256">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="c69f2-257">实际成本</span><span class="sxs-lookup"><span data-stu-id="c69f2-257">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="c69f2-258">合同签订部门货币</span><span class="sxs-lookup"><span data-stu-id="c69f2-258">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="c69f2-259">成本实际值</span><span class="sxs-lookup"><span data-stu-id="c69f2-259">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="c69f2-260">成本实际值</span><span class="sxs-lookup"><span data-stu-id="c69f2-260">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c69f2-261">未记帐实际销售额 – 应计费</span><span class="sxs-lookup"><span data-stu-id="c69f2-261">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="c69f2-262">项目合同货币</span><span class="sxs-lookup"><span data-stu-id="c69f2-262">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c69f2-263">资源单位成本</span><span class="sxs-lookup"><span data-stu-id="c69f2-263">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="c69f2-264">资源单位货币</span><span class="sxs-lookup"><span data-stu-id="c69f2-264">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c69f2-265">组织间销售</span><span class="sxs-lookup"><span data-stu-id="c69f2-265">Interorganizational sales</span></span></td>
<td><span data-ttu-id="c69f2-266">合同签订部门货币</span><span class="sxs-lookup"><span data-stu-id="c69f2-266">Contracting unit currency</span></span></td>
</tr>
<tr>
<td rowspan="5"><span data-ttu-id="c69f2-267">批准时间，并且审批期间可记帐工时不变或不减少。</span><span class="sxs-lookup"><span data-stu-id="c69f2-267">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="c69f2-268">实际成本</span><span class="sxs-lookup"><span data-stu-id="c69f2-268">Cost actual</span></span></td>
<td><span data-ttu-id="c69f2-269">合同签订部门货币</span><span class="sxs-lookup"><span data-stu-id="c69f2-269">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="c69f2-270">实际成本</span><span class="sxs-lookup"><span data-stu-id="c69f2-270">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="c69f2-271">合同签订部门货币</span><span class="sxs-lookup"><span data-stu-id="c69f2-271">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="c69f2-272">实际成本</span><span class="sxs-lookup"><span data-stu-id="c69f2-272">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="c69f2-273">实际成本</span><span class="sxs-lookup"><span data-stu-id="c69f2-273">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c69f2-274">资源单位成本</span><span class="sxs-lookup"><span data-stu-id="c69f2-274">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="c69f2-275">资源单位货币</span><span class="sxs-lookup"><span data-stu-id="c69f2-275">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c69f2-276">组织间销售</span><span class="sxs-lookup"><span data-stu-id="c69f2-276">Interorganizational sales</span></span></td>
<td><span data-ttu-id="c69f2-277">合同签订部门货币</span><span class="sxs-lookup"><span data-stu-id="c69f2-277">Contracting unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c69f2-278">未记帐实际销售额 – 新数量的应计值</span><span class="sxs-lookup"><span data-stu-id="c69f2-278">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="c69f2-279">项目合同货币</span><span class="sxs-lookup"><span data-stu-id="c69f2-279">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c69f2-280">未记帐实际销售额 – 差额的非应计值</span><span class="sxs-lookup"><span data-stu-id="c69f2-280">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="c69f2-281">项目合同货币</span><span class="sxs-lookup"><span data-stu-id="c69f2-281">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="c69f2-282">确认发票，并且审批期间可记帐工时不变或不增加。</span><span class="sxs-lookup"><span data-stu-id="c69f2-282">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="c69f2-283">未记帐销售额冲销</span><span class="sxs-lookup"><span data-stu-id="c69f2-283">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="c69f2-284">项目合同货币</span><span class="sxs-lookup"><span data-stu-id="c69f2-284">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="c69f2-285">里程碑的已记帐销售额</span><span class="sxs-lookup"><span data-stu-id="c69f2-285">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="c69f2-286">项目合同货币</span><span class="sxs-lookup"><span data-stu-id="c69f2-286">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="c69f2-287">不适用</span><span class="sxs-lookup"><span data-stu-id="c69f2-287">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="c69f2-288">不适用</span><span class="sxs-lookup"><span data-stu-id="c69f2-288">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c69f2-289">已记帐销售额</span><span class="sxs-lookup"><span data-stu-id="c69f2-289">Billed sales</span></span></td>
<td><span data-ttu-id="c69f2-290">项目合同货币</span><span class="sxs-lookup"><span data-stu-id="c69f2-290">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="c69f2-291">确认发票，并且可记帐工时减少。</span><span class="sxs-lookup"><span data-stu-id="c69f2-291">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="c69f2-292">未记帐销售额冲销</span><span class="sxs-lookup"><span data-stu-id="c69f2-292">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="c69f2-293">项目合同货币</span><span class="sxs-lookup"><span data-stu-id="c69f2-293">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="c69f2-294">不适用</span><span class="sxs-lookup"><span data-stu-id="c69f2-294">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="c69f2-295">不适用</span><span class="sxs-lookup"><span data-stu-id="c69f2-295">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="c69f2-296">不适用</span><span class="sxs-lookup"><span data-stu-id="c69f2-296">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="c69f2-297">不适用</span><span class="sxs-lookup"><span data-stu-id="c69f2-297">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c69f2-298">已记帐销售额 – 新数量的应计值</span><span class="sxs-lookup"><span data-stu-id="c69f2-298">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="c69f2-299">项目合同货币</span><span class="sxs-lookup"><span data-stu-id="c69f2-299">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c69f2-300">已记帐实际销售额 – 差额的非应计值</span><span class="sxs-lookup"><span data-stu-id="c69f2-300">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="c69f2-301">项目合同货币</span><span class="sxs-lookup"><span data-stu-id="c69f2-301">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="c69f2-302">更正发票以增加应计费数量。</span><span class="sxs-lookup"><span data-stu-id="c69f2-302">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="c69f2-303">已记帐销售额 - 冲销</span><span class="sxs-lookup"><span data-stu-id="c69f2-303">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="c69f2-304">项目合同货币</span><span class="sxs-lookup"><span data-stu-id="c69f2-304">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="c69f2-305">里程碑的已记帐销售额冲销</span><span class="sxs-lookup"><span data-stu-id="c69f2-305">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="c69f2-306">里程碑状态从<strong>已开票</strong>更改为<strong>准备好开票</strong></span><span class="sxs-lookup"><span data-stu-id="c69f2-306">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="c69f2-307">项目合同货币</span><span class="sxs-lookup"><span data-stu-id="c69f2-307">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="c69f2-308">不适用</span><span class="sxs-lookup"><span data-stu-id="c69f2-308">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="c69f2-309">不适用</span><span class="sxs-lookup"><span data-stu-id="c69f2-309">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c69f2-310">已记帐销售额</span><span class="sxs-lookup"><span data-stu-id="c69f2-310">Billed sales</span></span></td>
<td><span data-ttu-id="c69f2-311">项目合同货币</span><span class="sxs-lookup"><span data-stu-id="c69f2-311">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="c69f2-312">更正发票以减少应计费数量。</span><span class="sxs-lookup"><span data-stu-id="c69f2-312">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="c69f2-313">已记帐销售额 - 冲销</span><span class="sxs-lookup"><span data-stu-id="c69f2-313">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="c69f2-314">项目合同货币</span><span class="sxs-lookup"><span data-stu-id="c69f2-314">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c69f2-315">新数量的已记帐销售额</span><span class="sxs-lookup"><span data-stu-id="c69f2-315">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="c69f2-316">项目合同货币</span><span class="sxs-lookup"><span data-stu-id="c69f2-316">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c69f2-317">未记帐销售额 – 差额的应计值</span><span class="sxs-lookup"><span data-stu-id="c69f2-317">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="c69f2-318">项目合同货币</span><span class="sxs-lookup"><span data-stu-id="c69f2-318">Project contract currency</span></span></td>
</tr>
</tbody>
</table>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
