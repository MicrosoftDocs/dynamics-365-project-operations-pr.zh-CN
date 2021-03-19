---
title: 基于项目的报价单明细概述 - 精简
description: 此主题提供为项目工作使用基于项目的报价单明细的信息。 (Pro)
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 4865c06691fba09eacf5fe6449adfaf542444520
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/15/2021
ms.locfileid: "5272962"
---
# <a name="project-based-quote-lines-overview---lite"></a><span data-ttu-id="38c45-104">基于项目的报价单明细概述 - 精简</span><span class="sxs-lookup"><span data-stu-id="38c45-104">Project-based quote lines overview - lite</span></span>

<span data-ttu-id="38c45-105">_**适用于：** 精简部署 - 估价交易开票_</span><span class="sxs-lookup"><span data-stu-id="38c45-105">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="38c45-106">基于项目的报价单明细用于帮助预估协定中的项目工作。</span><span class="sxs-lookup"><span data-stu-id="38c45-106">Project-based quote lines are designed to help estimate the project work on an engagement.</span></span> <span data-ttu-id="38c45-107">基于项目的报价单明细的结构可以通过以下概念为项目预估进行扩展：</span><span class="sxs-lookup"><span data-stu-id="38c45-107">The structure of a project-based quote line is extended for project estimates with the following concepts:</span></span>

- <span data-ttu-id="38c45-108">记帐方法</span><span class="sxs-lookup"><span data-stu-id="38c45-108">Billing Method</span></span>
- <span data-ttu-id="38c45-109">项目和任务映射</span><span class="sxs-lookup"><span data-stu-id="38c45-109">Project and Task Mapping</span></span>
- <span data-ttu-id="38c45-110">包括的交易类</span><span class="sxs-lookup"><span data-stu-id="38c45-110">Included Transaction classes</span></span>
- <span data-ttu-id="38c45-111">上限</span><span class="sxs-lookup"><span data-stu-id="38c45-111">Not-to-Exceed Limit</span></span>
- <span data-ttu-id="38c45-112">应计费设置</span><span class="sxs-lookup"><span data-stu-id="38c45-112">Chargeability setup</span></span>
- <span data-ttu-id="38c45-113">使用报价单明细详细信息的预估</span><span class="sxs-lookup"><span data-stu-id="38c45-113">Estimation using Quote Line Details</span></span>
- <span data-ttu-id="38c45-114">报价单明细客户</span><span class="sxs-lookup"><span data-stu-id="38c45-114">Quote line Customers</span></span>

<span data-ttu-id="38c45-115">下表提供了有关基于项目的报价单明细的 **常规** 选项卡上字段的信息。</span><span class="sxs-lookup"><span data-stu-id="38c45-115">The following table provides information about the fields on the **General** tab of project-based quote line.</span></span> <span data-ttu-id="38c45-116">这些字段帮助为项目工作的详细、全面的预估建立基础。</span><span class="sxs-lookup"><span data-stu-id="38c45-116">These fields help set up the basis for a detailed, ground-up estimation for project work.</span></span>

| <span data-ttu-id="38c45-117">**字段**</span><span class="sxs-lookup"><span data-stu-id="38c45-117">**Field**</span></span> | <span data-ttu-id="38c45-118">**说明**</span><span class="sxs-lookup"><span data-stu-id="38c45-118">**Description**</span></span> | <span data-ttu-id="38c45-119">**下游影响**</span><span class="sxs-lookup"><span data-stu-id="38c45-119">**Downstream impact**</span></span> |
| --- | --- | --- |
| <span data-ttu-id="38c45-120">客户</span><span class="sxs-lookup"><span data-stu-id="38c45-120">Name</span></span> | <span data-ttu-id="38c45-121">应会帮助您识别正在预估的报价单的分散部分的报价单明细的名称。</span><span class="sxs-lookup"><span data-stu-id="38c45-121">The name of quote line which should help you identify the discrete component of the quote that is being estimated.</span></span> | <span data-ttu-id="38c45-122">将复制到此报价单赢单时从报价单明细创建的项目合同子项。</span><span class="sxs-lookup"><span data-stu-id="38c45-122">Copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="38c45-123">记帐方法</span><span class="sxs-lookup"><span data-stu-id="38c45-123">Billing Method</span></span> | <span data-ttu-id="38c45-124">在从商机创建的报价单中，此值从商机明细中的相应字段复制。</span><span class="sxs-lookup"><span data-stu-id="38c45-124">On a quote created from an opportunity, this value is copied from the corresponding field on the opportunity line.</span></span> <span data-ttu-id="38c45-125">此字段包括 Dynamics 365 Project Operations 支持的两个主要合同模型：</span><span class="sxs-lookup"><span data-stu-id="38c45-125">This field includes the two main contracting models supported by Dynamics 365 Project Operations:</span></span></br><span data-ttu-id="38c45-126">- 固定价格</span><span class="sxs-lookup"><span data-stu-id="38c45-126">- Fixed price</span></span></br><span data-ttu-id="38c45-127">- 时间和材料。</span><span class="sxs-lookup"><span data-stu-id="38c45-127">- Time and material.</span></span>| <span data-ttu-id="38c45-128">此字段值将复制到此报价单赢单时从报价单明细创建的项目合同子项。</span><span class="sxs-lookup"><span data-stu-id="38c45-128">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="38c45-129">Project</span><span class="sxs-lookup"><span data-stu-id="38c45-129">Project</span></span> | <span data-ttu-id="38c45-130">使用此可选字段可以识别将用于交付此协定中的工作的项目。</span><span class="sxs-lookup"><span data-stu-id="38c45-130">Use this optional field to identify the project that will be used to deliver the work on this engagement.</span></span> <span data-ttu-id="38c45-131">将项目映射到报价单明细时，它将帮助设置应计费任务，还可以帮助将基于项目的预估作为报价单明细详细信息引入报价单明细。</span><span class="sxs-lookup"><span data-stu-id="38c45-131">When a project is mapped to a quote line, it helps with setting up chargeable tasks and also with bringing in a project-based estimate to the quote line as quote line details.</span></span> <span data-ttu-id="38c45-132">当项目未映射到基于项目的报价单明细时，应通过创建每个报价单明细详细信息来手动创建预估。</span><span class="sxs-lookup"><span data-stu-id="38c45-132">When a project is not mapped to a project-based quote line, the estimate should be created manually by creating each quote line detail.</span></span> | <span data-ttu-id="38c45-133">此字段值将复制到此报价单赢单时从报价单明细创建的项目合同子项。</span><span class="sxs-lookup"><span data-stu-id="38c45-133">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span>|
| <span data-ttu-id="38c45-134">包含的任务</span><span class="sxs-lookup"><span data-stu-id="38c45-134">Included Tasks</span></span> | <span data-ttu-id="38c45-135">指示此报价单明细是否用于所选项目的全部或部分项目任务。</span><span class="sxs-lookup"><span data-stu-id="38c45-135">Indicates if this quote line is used for all or some of the project tasks for the selected project.</span></span> <span data-ttu-id="38c45-136">此字段具有以下可能的值：</span><span class="sxs-lookup"><span data-stu-id="38c45-136">This field has the following possible values:</span></span></br><span data-ttu-id="38c45-137">- 所有项目任务</span><span class="sxs-lookup"><span data-stu-id="38c45-137">- All project tasks</span></span></br><span data-ttu-id="38c45-138">- 仅所选项目任务</span><span class="sxs-lookup"><span data-stu-id="38c45-138">- Selected project tasks only</span></span></br><span data-ttu-id="38c45-139">此字段中的空白值等效于 **所有项目任务** 选项。</span><span class="sxs-lookup"><span data-stu-id="38c45-139">A blank value in this field is equivalent to the **All project tasks** option.</span></span> | <span data-ttu-id="38c45-140">如果选择了 **仅所选项目任务**，在项目页面上，您可以通过 **任务记帐设置** 选项卡选择特定任务来将其与此报价单明细关联。</span><span class="sxs-lookup"><span data-stu-id="38c45-140">When **Selected project tasks only** is selected then on the project page, the **Task billing setup** tab allows you to select specific tasks to associate them to this quote line.</span></span> <span data-ttu-id="38c45-141">此字段值将复制到此报价单赢单时从报价单明细创建的项目合同子项。</span><span class="sxs-lookup"><span data-stu-id="38c45-141">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="38c45-142">包括时间</span><span class="sxs-lookup"><span data-stu-id="38c45-142">Include Time</span></span> | <span data-ttu-id="38c45-143">**是**/**否** 标志指示此报价单明细的预估中是否包括所选项目的时间交易或人工成本。</span><span class="sxs-lookup"><span data-stu-id="38c45-143">A **Yes**/**No** flag indicates if time transactions or labor costs on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="38c45-144">**否** 值指示此报价单明细的预估中将不包括时间交易或人工成本。</span><span class="sxs-lookup"><span data-stu-id="38c45-144">A **No** value indicates that the time transactions or labor cost will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="38c45-145">**是** 值指示此报价单明细的预估中将包括时间交易或人工成本。</span><span class="sxs-lookup"><span data-stu-id="38c45-145">A **Yes** value indicates that the time transactions or labor cost will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="38c45-146">此字段值将复制到此报价单赢单时从报价单明细创建的项目合同子项。</span><span class="sxs-lookup"><span data-stu-id="38c45-146">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="38c45-147">包括支出</span><span class="sxs-lookup"><span data-stu-id="38c45-147">Include Expense</span></span> | <span data-ttu-id="38c45-148">**是**/**否** 标志指示此报价单明细的预估中是否包括所选项目的支出成本。</span><span class="sxs-lookup"><span data-stu-id="38c45-148">A **Yes**/**No** flag indicates if expense costs on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="38c45-149">**否** 值指示此报价单明细的预估中将不包括支出成本。</span><span class="sxs-lookup"><span data-stu-id="38c45-149">A **No** value indicates that the expense cost will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="38c45-150">**是** 值指示此报价单明细的预估中将包括支出成本。</span><span class="sxs-lookup"><span data-stu-id="38c45-150">A **Yes** value indicates that the expense cost will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="38c45-151">此字段值将复制到此报价单赢单时从报价单明细创建的项目合同子项。</span><span class="sxs-lookup"><span data-stu-id="38c45-151">This field value is copied over to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="38c45-152">包括费用</span><span class="sxs-lookup"><span data-stu-id="38c45-152">Include Fee</span></span> | <span data-ttu-id="38c45-153">**是**/**否** 标志指示此报价单明细的预估中是否包括所选项目的费用。</span><span class="sxs-lookup"><span data-stu-id="38c45-153">A **Yes**/**No** flag indicates if fees on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="38c45-154">**否** 值指示此报价单明细的预估中将不包括费用。</span><span class="sxs-lookup"><span data-stu-id="38c45-154">A **No** value indicates that the Fees will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="38c45-155">**是** 值指示此报价单明细的预估中将包括费用。</span><span class="sxs-lookup"><span data-stu-id="38c45-155">A **Yes** value indicates that the Fees will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="38c45-156">此字段值将复制到此报价单赢单时从报价单明细创建的项目合同子项。</span><span class="sxs-lookup"><span data-stu-id="38c45-156">This field value is copied to the Project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="38c45-157">配额数量</span><span class="sxs-lookup"><span data-stu-id="38c45-157">Quoted Amount</span></span> | <span data-ttu-id="38c45-158">这是将针对此基于项目的报价单明细上预测的所有工作向客户报价的金额。</span><span class="sxs-lookup"><span data-stu-id="38c45-158">This is amount that will be quoted to the customer for all the work forecasted on this project-based quote line.</span></span> <span data-ttu-id="38c45-159">在从商机创建的报价单中，此值从商机明细中的 **客户预算** 字段复制。</span><span class="sxs-lookup"><span data-stu-id="38c45-159">On a quote created from an opportunity, this value is copied from the **Customer Budget** field on the opportunity line.</span></span> <span data-ttu-id="38c45-160">当基于项目的报价单明细包含明细详细信息时，此字段将被锁定以进行编辑，并从报价单明细详细信息中的金额汇总。</span><span class="sxs-lookup"><span data-stu-id="38c45-160">When the project-based quote line has line details, this field is locked for editing and is summarized from the amount on the quote line details.</span></span> | <span data-ttu-id="38c45-161">此字段值将复制到此报价单赢单时从报价单明细创建的项目合同子项。</span><span class="sxs-lookup"><span data-stu-id="38c45-161">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="38c45-162">预计税款</span><span class="sxs-lookup"><span data-stu-id="38c45-162">Estimated Tax</span></span> | <span data-ttu-id="38c45-163">这是一个可编辑字段，供用户在报价单明细中添加预估税款金额。</span><span class="sxs-lookup"><span data-stu-id="38c45-163">This is an editable field for the user to add the estimated tax amount on the quote line.</span></span> <span data-ttu-id="38c45-164">当基于项目的报价单明细包含明细详细信息时，此字段将被锁定以进行编辑，并从报价单明细详细信息中的税款金额汇总。</span><span class="sxs-lookup"><span data-stu-id="38c45-164">When a project-based quote line has line details, this field is locked for editing and is summarized from the tax amount on the quote line details.</span></span> | <span data-ttu-id="38c45-165">此字段值将复制到此报价单赢单时从报价单明细创建的项目合同子项。</span><span class="sxs-lookup"><span data-stu-id="38c45-165">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="38c45-166">税后报价金额</span><span class="sxs-lookup"><span data-stu-id="38c45-166">Quoted Amount after Tax</span></span> | <span data-ttu-id="38c45-167">此字段是税后的报价单明细金额，是只读的。</span><span class="sxs-lookup"><span data-stu-id="38c45-167">This field is the quote line amount after tax and is read-only.</span></span> <span data-ttu-id="38c45-168">此字段中的金额计算为 *报价金额 + 税款*。</span><span class="sxs-lookup"><span data-stu-id="38c45-168">The amount in this field is calculated as *Quoted Amount + Tax*.</span></span> | <span data-ttu-id="38c45-169">此字段值将复制到此报价单赢单时从报价单明细创建的项目合同子项。</span><span class="sxs-lookup"><span data-stu-id="38c45-169">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="38c45-170">上限</span><span class="sxs-lookup"><span data-stu-id="38c45-170">Not-to-exceed Limit</span></span> | <span data-ttu-id="38c45-171">此字段可编辑，仅在具有 **时间和材料** 计费方法的基于项目的报价单明细中可用。</span><span class="sxs-lookup"><span data-stu-id="38c45-171">This field is editable and is only available on project-based quote lines that have a **Time and Material** billing method.</span></span> | <span data-ttu-id="38c45-172">此字段值将复制到此报价单赢单时从报价单明细创建的项目合同子项。</span><span class="sxs-lookup"><span data-stu-id="38c45-172">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="38c45-173">客户预算</span><span class="sxs-lookup"><span data-stu-id="38c45-173">Customer Budget</span></span> | <span data-ttu-id="38c45-174">此字段可编辑，如果报价单是从商机创建的，此字段将从商机明细中的相应字段复制。</span><span class="sxs-lookup"><span data-stu-id="38c45-174">This field is editable and is copied from the corresponding field on the opportunity line if the quote was created from an opportunity.</span></span> | <span data-ttu-id="38c45-175">此字段值将复制到此报价单赢单时从报价单明细创建的项目合同子项。</span><span class="sxs-lookup"><span data-stu-id="38c45-175">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |


## <a name="validation-rules-for-fields-on-the-general-tab-of-project-based-quote-lines"></a><span data-ttu-id="38c45-176">基于项目的报价单明细的“常规”选项卡上字段的验证规则</span><span class="sxs-lookup"><span data-stu-id="38c45-176">Validation rules for fields on the General tab of project-based quote lines</span></span>

<span data-ttu-id="38c45-177">**规则 1**：如果 **包含的任务** 字段为空，或者将其设置为 **所有项目任务**，项目将包含在报价单明细中。</span><span class="sxs-lookup"><span data-stu-id="38c45-177">**Rule 1**: If the **Included Tasks** field is blank, or if it is set to **All project tasks**, a project is included in the quote line.</span></span>

<span data-ttu-id="38c45-178">**规则 2**：如果 **包含的任务** 字段为空，或者将其设置为 **所有项目任务**，项目和特定交易类只能包含在报价单的一个基于项目的报价单明细中。</span><span class="sxs-lookup"><span data-stu-id="38c45-178">**Rule 2**: If the **Included Tasks** field is blank, or if it is set to **All project tasks**, a project and a certain transaction class can only be included on one project-based quote line of a quote.</span></span>

<span data-ttu-id="38c45-179">**规则 3**：如果 **包含的任务** 字段设置为 **仅所选项目任务**，项目和特定交易类可以包含在报价单的多个基于项目的报价单明细中。</span><span class="sxs-lookup"><span data-stu-id="38c45-179">**Rule 3**: If the **Included Tasks** field is set to **Selected project tasks only**, a project and a certain transaction class can be included on multiple project-based quote lines of a quote.</span></span>

<span data-ttu-id="38c45-180">**规则 4**：如果商机有多个报价单，可能存在来自不同报价单的报价单明细，它们均引用同一个项目并包含相同的交易类。</span><span class="sxs-lookup"><span data-stu-id="38c45-180">**Rule 4**: If an opportunity has multiple quotes, there can be quote lines from different quotes that all reference the same project and include the same transaction class.</span></span>

<span data-ttu-id="38c45-181">**规则 5**：如果报价单不属于同一商机，则不能包括同一个项目和交易类。</span><span class="sxs-lookup"><span data-stu-id="38c45-181">**Rule 5**: If the quotes do not belong to the same opportunity, they can't include the same project and transaction class.</span></span>

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="61" valign="top">
                <p><span data-ttu-id="38c45-182">
                    <strong>商机</strong>
                </span><span class="sxs-lookup"><span data-stu-id="38c45-182">
                    <strong>Opportunity</strong>
                </span></span></p>
            </td>
            <td width="41" valign="top">
                <p><span data-ttu-id="38c45-183">
                    <strong>报价单</strong>
                </span><span class="sxs-lookup"><span data-stu-id="38c45-183">
                    <strong>Quote</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="38c45-184">
                    <strong>报价单明细</strong>
                </span><span class="sxs-lookup"><span data-stu-id="38c45-184">
                    <strong>Quote line</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="38c45-185">
                    <strong>Project</strong>
                </span><span class="sxs-lookup"><span data-stu-id="38c45-185">
                    <strong>Project</strong>
                </span></span></p>
            </td>
            <td width="90" valign="top">
                <p><span data-ttu-id="38c45-186">
                    <strong>包含的任务</strong>
                </span><span class="sxs-lookup"><span data-stu-id="38c45-186">
                    <strong>Included tasks</strong>
                </span></span></p>
            </td>
            <td width="48" valign="top">
                <p><span data-ttu-id="38c45-187">
                    <strong>包括时间</strong>
                </span><span class="sxs-lookup"><span data-stu-id="38c45-187">
                    <strong>Include Time</strong>
                </span></span></p>
            </td>
            <td width="48" valign="top">
                <p><span data-ttu-id="38c45-188">
                    <strong>包括支出</strong>
                </span><span class="sxs-lookup"><span data-stu-id="38c45-188">
                    <strong>Include Expense</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="38c45-189">
                    <strong>添加</strong>
                </span><span class="sxs-lookup"><span data-stu-id="38c45-189">
                    <strong>Include</strong>
                </span></span></p>
                <p><span data-ttu-id="38c45-190">
                    <strong>费用</strong>
                </span><span class="sxs-lookup"><span data-stu-id="38c45-190">
                    <strong>Fee</strong>
                </span></span></p>
            </td>
            <td width="54" valign="top">
                <p><span data-ttu-id="38c45-191">
                    <strong>有效/无效</strong>
                </span><span class="sxs-lookup"><span data-stu-id="38c45-191">
                    <strong>Valid/ Not valid</strong>
                </span></span></p>
            </td>
            <td width="308" valign="top">
                <p><span data-ttu-id="38c45-192">
                    <strong>原因</strong>
                </span><span class="sxs-lookup"><span data-stu-id="38c45-192">
                    <strong>Reason</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="38c45-193">O1</span><span class="sxs-lookup"><span data-stu-id="38c45-193">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="38c45-194">Q1</span><span class="sxs-lookup"><span data-stu-id="38c45-194">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="38c45-195">QL1</span><span class="sxs-lookup"><span data-stu-id="38c45-195">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="38c45-196">P1</span><span class="sxs-lookup"><span data-stu-id="38c45-196">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="38c45-197">空白</span><span class="sxs-lookup"><span data-stu-id="38c45-197">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="38c45-198">是</span><span class="sxs-lookup"><span data-stu-id="38c45-198">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="38c45-199">是</span><span class="sxs-lookup"><span data-stu-id="38c45-199">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="38c45-200">是</span><span class="sxs-lookup"><span data-stu-id="38c45-200">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="38c45-201">无效</span><span class="sxs-lookup"><span data-stu-id="38c45-201">Not valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="38c45-202">违反规则 #2。</span><span class="sxs-lookup"><span data-stu-id="38c45-202">Violation of Rule #2.</span></span> <span data-ttu-id="38c45-203">P1 项目的时间、支出和费用包含在报价单明细 QL1 和 QL2 中。</span><span class="sxs-lookup"><span data-stu-id="38c45-203">Time, Expense, and Fees on P1 project are included on quote lines QL1 and QL2.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="38c45-204">O1</span><span class="sxs-lookup"><span data-stu-id="38c45-204">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="38c45-205">Q1</span><span class="sxs-lookup"><span data-stu-id="38c45-205">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="38c45-206">QL2</span><span class="sxs-lookup"><span data-stu-id="38c45-206">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="38c45-207">P1</span><span class="sxs-lookup"><span data-stu-id="38c45-207">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="38c45-208">空白</span><span class="sxs-lookup"><span data-stu-id="38c45-208">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="38c45-209">是</span><span class="sxs-lookup"><span data-stu-id="38c45-209">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="38c45-210">是</span><span class="sxs-lookup"><span data-stu-id="38c45-210">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="38c45-211">是</span><span class="sxs-lookup"><span data-stu-id="38c45-211">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="90" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="308" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="38c45-212">O1</span><span class="sxs-lookup"><span data-stu-id="38c45-212">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="38c45-213">Q1</span><span class="sxs-lookup"><span data-stu-id="38c45-213">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="38c45-214">QL1</span><span class="sxs-lookup"><span data-stu-id="38c45-214">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="38c45-215">P1</span><span class="sxs-lookup"><span data-stu-id="38c45-215">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="38c45-216">空白</span><span class="sxs-lookup"><span data-stu-id="38c45-216">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="38c45-217">是</span><span class="sxs-lookup"><span data-stu-id="38c45-217">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="38c45-218">No</span><span class="sxs-lookup"><span data-stu-id="38c45-218">No</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="38c45-219">是</span><span class="sxs-lookup"><span data-stu-id="38c45-219">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="38c45-220">无效</span><span class="sxs-lookup"><span data-stu-id="38c45-220">Not valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="38c45-221">违反规则 #2。</span><span class="sxs-lookup"><span data-stu-id="38c45-221">Violation of Rule #2.</span></span> <span data-ttu-id="38c45-222">P1 项目的时间和费用包含在报价单明细 QL1 和 QL2 中。</span><span class="sxs-lookup"><span data-stu-id="38c45-222">Time and Fees on P1 project are included on quote lines QL1 and QL2.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="38c45-223">O1</span><span class="sxs-lookup"><span data-stu-id="38c45-223">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="38c45-224">Q1</span><span class="sxs-lookup"><span data-stu-id="38c45-224">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="38c45-225">QL2</span><span class="sxs-lookup"><span data-stu-id="38c45-225">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="38c45-226">P1</span><span class="sxs-lookup"><span data-stu-id="38c45-226">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="38c45-227">空白</span><span class="sxs-lookup"><span data-stu-id="38c45-227">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="38c45-228">是</span><span class="sxs-lookup"><span data-stu-id="38c45-228">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="38c45-229">是</span><span class="sxs-lookup"><span data-stu-id="38c45-229">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="38c45-230">是</span><span class="sxs-lookup"><span data-stu-id="38c45-230">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="90" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="108" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="38c45-231">O1</span><span class="sxs-lookup"><span data-stu-id="38c45-231">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="38c45-232">Q1</span><span class="sxs-lookup"><span data-stu-id="38c45-232">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="38c45-233">QL1</span><span class="sxs-lookup"><span data-stu-id="38c45-233">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="38c45-234">P1</span><span class="sxs-lookup"><span data-stu-id="38c45-234">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="38c45-235">空白</span><span class="sxs-lookup"><span data-stu-id="38c45-235">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="38c45-236">是</span><span class="sxs-lookup"><span data-stu-id="38c45-236">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="38c45-237">No</span><span class="sxs-lookup"><span data-stu-id="38c45-237">No</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="38c45-238">是</span><span class="sxs-lookup"><span data-stu-id="38c45-238">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="38c45-239">有效</span><span class="sxs-lookup"><span data-stu-id="38c45-239">Valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                  <p>
<span data-ttu-id="38c45-240">P1 项目的时间和费用包含在 QL1 上。</span><span class="sxs-lookup"><span data-stu-id="38c45-240">Time and Fees on P1 project are included on QL1.</span></span>
<span data-ttu-id="38c45-241">P1 项目的支出包含在 QL2 中。</span><span class="sxs-lookup"><span data-stu-id="38c45-241">Expense on P1 project is included on QL2.</span></span>
<span data-ttu-id="38c45-242">每个报价单明细中包含的内容没有重叠，是有效的。</span><span class="sxs-lookup"><span data-stu-id="38c45-242">There is no overlap in what is being included on each quote line and is valid.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="38c45-243">O1</span><span class="sxs-lookup"><span data-stu-id="38c45-243">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="38c45-244">Q1</span><span class="sxs-lookup"><span data-stu-id="38c45-244">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="38c45-245">QL2</span><span class="sxs-lookup"><span data-stu-id="38c45-245">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="38c45-246">P1</span><span class="sxs-lookup"><span data-stu-id="38c45-246">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="38c45-247">空白</span><span class="sxs-lookup"><span data-stu-id="38c45-247">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="38c45-248">No</span><span class="sxs-lookup"><span data-stu-id="38c45-248">No</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="38c45-249">是</span><span class="sxs-lookup"><span data-stu-id="38c45-249">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="38c45-250">No</span><span class="sxs-lookup"><span data-stu-id="38c45-250">No</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="90" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="308" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="38c45-251">O1</span><span class="sxs-lookup"><span data-stu-id="38c45-251">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="38c45-252">Q1</span><span class="sxs-lookup"><span data-stu-id="38c45-252">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="38c45-253">QL1</span><span class="sxs-lookup"><span data-stu-id="38c45-253">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="38c45-254">P1</span><span class="sxs-lookup"><span data-stu-id="38c45-254">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="38c45-255">仅所选任务</span><span class="sxs-lookup"><span data-stu-id="38c45-255">Selected tasks only</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="38c45-256">是</span><span class="sxs-lookup"><span data-stu-id="38c45-256">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="38c45-257">是</span><span class="sxs-lookup"><span data-stu-id="38c45-257">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="38c45-258">是</span><span class="sxs-lookup"><span data-stu-id="38c45-258">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="38c45-259">无效</span><span class="sxs-lookup"><span data-stu-id="38c45-259">Not valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="38c45-260">违反上方的规则 #2</span><span class="sxs-lookup"><span data-stu-id="38c45-260">Violation of Rule #2 above</span></span> </p>
                <p>
<span data-ttu-id="38c45-261">Q1 包含项目 P1 中某个任务子集的时间、支出和费用。</span><span class="sxs-lookup"><span data-stu-id="38c45-261">Q1 includes Time, Expenses, and Fees on a subset of tasks on project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="38c45-262">QL2 包括整个项目 P1 的时间、支出和费用，与 Q1 中所包含的内容重叠。</span><span class="sxs-lookup"><span data-stu-id="38c45-262">QL2 includes Time, Expenses, and Fees for the whole project P1 and overlaps with what is included on Q1.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="38c45-263">O1</span><span class="sxs-lookup"><span data-stu-id="38c45-263">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="38c45-264">Q1</span><span class="sxs-lookup"><span data-stu-id="38c45-264">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="38c45-265">QL2</span><span class="sxs-lookup"><span data-stu-id="38c45-265">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="38c45-266">P1</span><span class="sxs-lookup"><span data-stu-id="38c45-266">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="38c45-267">空白</span><span class="sxs-lookup"><span data-stu-id="38c45-267">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="38c45-268">是</span><span class="sxs-lookup"><span data-stu-id="38c45-268">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="38c45-269">是</span><span class="sxs-lookup"><span data-stu-id="38c45-269">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="38c45-270">是</span><span class="sxs-lookup"><span data-stu-id="38c45-270">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="90" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="108" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="38c45-271">O1</span><span class="sxs-lookup"><span data-stu-id="38c45-271">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="38c45-272">Q1</span><span class="sxs-lookup"><span data-stu-id="38c45-272">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="38c45-273">QL1</span><span class="sxs-lookup"><span data-stu-id="38c45-273">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="38c45-274">P1</span><span class="sxs-lookup"><span data-stu-id="38c45-274">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="38c45-275">仅所选任务</span><span class="sxs-lookup"><span data-stu-id="38c45-275">Selected tasks only</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="38c45-276">是</span><span class="sxs-lookup"><span data-stu-id="38c45-276">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="38c45-277">是</span><span class="sxs-lookup"><span data-stu-id="38c45-277">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="38c45-278">是</span><span class="sxs-lookup"><span data-stu-id="38c45-278">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="38c45-279">有效</span><span class="sxs-lookup"><span data-stu-id="38c45-279">Valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="38c45-280">根据上方的规则 #3，</span><span class="sxs-lookup"><span data-stu-id="38c45-280">Per Rule #3 above,</span></span> </p>
                <p>
<span data-ttu-id="38c45-281">Q1 包含项目 P1 中某个任务子集的时间、支出和费用。</span><span class="sxs-lookup"><span data-stu-id="38c45-281">Q1 includes Time, Expenses, and Fees on a subset of tasks on project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="38c45-282">QL2 包含项目 P1 中某个任务子集的时间、支出和费用。</span><span class="sxs-lookup"><span data-stu-id="38c45-282">QL2 includes Time, Expenses, and Fees for a subset of tasks on project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="38c45-283">唯一的附加验证围绕 QL1 上的任务子集，此任务子集与 QL2 上的任务子集不同。</span><span class="sxs-lookup"><span data-stu-id="38c45-283">The only additional validation is around the subset of tasks on QL1 which are different from the subset of tasks on QL2.</span></span> <span data-ttu-id="38c45-284">这可以确保没有重叠。</span><span class="sxs-lookup"><span data-stu-id="38c45-284">This ensures that there are no overlaps.</span></span> <span data-ttu-id="38c45-285">当任务关联时，这由系统完成。</span><span class="sxs-lookup"><span data-stu-id="38c45-285">This is done by the system when tasks are associated.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="38c45-286">O1</span><span class="sxs-lookup"><span data-stu-id="38c45-286">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="38c45-287">Q1</span><span class="sxs-lookup"><span data-stu-id="38c45-287">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="38c45-288">QL2</span><span class="sxs-lookup"><span data-stu-id="38c45-288">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="38c45-289">P1</span><span class="sxs-lookup"><span data-stu-id="38c45-289">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="38c45-290">仅所选任务</span><span class="sxs-lookup"><span data-stu-id="38c45-290">Selected tasks only</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="38c45-291">是</span><span class="sxs-lookup"><span data-stu-id="38c45-291">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="38c45-292">是</span><span class="sxs-lookup"><span data-stu-id="38c45-292">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="38c45-293">是</span><span class="sxs-lookup"><span data-stu-id="38c45-293">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="90" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="308" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="38c45-294">O1</span><span class="sxs-lookup"><span data-stu-id="38c45-294">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="38c45-295">Q1</span><span class="sxs-lookup"><span data-stu-id="38c45-295">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="38c45-296">QL1</span><span class="sxs-lookup"><span data-stu-id="38c45-296">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="38c45-297">P1</span><span class="sxs-lookup"><span data-stu-id="38c45-297">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="38c45-298">所有项目任务或空白</span><span class="sxs-lookup"><span data-stu-id="38c45-298">All project tasks or blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="38c45-299">是</span><span class="sxs-lookup"><span data-stu-id="38c45-299">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="38c45-300">是</span><span class="sxs-lookup"><span data-stu-id="38c45-300">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="38c45-301">是</span><span class="sxs-lookup"><span data-stu-id="38c45-301">Yes</span></span> </p>
            </td>
            <td width="54" valign="top">
                <p>
<span data-ttu-id="38c45-302">有效</span><span class="sxs-lookup"><span data-stu-id="38c45-302">Valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="38c45-303">根据规则 #5，Q1 和 Q2 是同一个商机中的两个报价单，因此它们都可以针对项目的相同组件进行预估。</span><span class="sxs-lookup"><span data-stu-id="38c45-303">Based on Rule #5, Q1 and Q2 are two quotes on the same opportunity, so they can both estimate for the same components of a project.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="38c45-304">O1</span><span class="sxs-lookup"><span data-stu-id="38c45-304">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="38c45-305">Q2</span><span class="sxs-lookup"><span data-stu-id="38c45-305">Q2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="38c45-306">QL1</span><span class="sxs-lookup"><span data-stu-id="38c45-306">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="38c45-307">P1</span><span class="sxs-lookup"><span data-stu-id="38c45-307">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="38c45-308">所有项目任务或空白</span><span class="sxs-lookup"><span data-stu-id="38c45-308">All project tasks or blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="38c45-309">是</span><span class="sxs-lookup"><span data-stu-id="38c45-309">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="38c45-310">是</span><span class="sxs-lookup"><span data-stu-id="38c45-310">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="38c45-311">是</span><span class="sxs-lookup"><span data-stu-id="38c45-311">Yes</span></span> </p>
            </td>
            <td width="54" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="90" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="308" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="38c45-312">O1</span><span class="sxs-lookup"><span data-stu-id="38c45-312">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="38c45-313">Q1</span><span class="sxs-lookup"><span data-stu-id="38c45-313">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="38c45-314">QL1</span><span class="sxs-lookup"><span data-stu-id="38c45-314">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="38c45-315">P1</span><span class="sxs-lookup"><span data-stu-id="38c45-315">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="38c45-316">所有项目任务或空白</span><span class="sxs-lookup"><span data-stu-id="38c45-316">All project tasks or blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="38c45-317">是</span><span class="sxs-lookup"><span data-stu-id="38c45-317">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="38c45-318">是</span><span class="sxs-lookup"><span data-stu-id="38c45-318">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="38c45-319">是</span><span class="sxs-lookup"><span data-stu-id="38c45-319">Yes</span></span> </p>
            </td>
            <td width="54" valign="top">
                <p>
<span data-ttu-id="38c45-320">有效</span><span class="sxs-lookup"><span data-stu-id="38c45-320">Valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="38c45-321">根据规则 #4，Q1 和 Q2 是不同商机中的两个报价单，因此它们不能针对项目的相同组件进行预估。</span><span class="sxs-lookup"><span data-stu-id="38c45-321">Based on Rule #4, Q1 and Q2 are two quotes on different opportunities, so they can't estimate for the same components of the same project.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="38c45-322">O2</span><span class="sxs-lookup"><span data-stu-id="38c45-322">O2</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="38c45-323">Q1</span><span class="sxs-lookup"><span data-stu-id="38c45-323">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="38c45-324">QL1</span><span class="sxs-lookup"><span data-stu-id="38c45-324">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="38c45-325">P1</span><span class="sxs-lookup"><span data-stu-id="38c45-325">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="38c45-326">所有项目任务或空白</span><span class="sxs-lookup"><span data-stu-id="38c45-326">All project tasks or blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="38c45-327">是</span><span class="sxs-lookup"><span data-stu-id="38c45-327">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="38c45-328">是</span><span class="sxs-lookup"><span data-stu-id="38c45-328">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="38c45-329">是</span><span class="sxs-lookup"><span data-stu-id="38c45-329">Yes</span></span> </p>
            </td>
            <td width="54" valign="top">
                <p>
<span data-ttu-id="38c45-330">无效</span><span class="sxs-lookup"><span data-stu-id="38c45-330">Not Valid</span></span> </p>
            </td>
        </tr>
    </tbody>
</table>



[!INCLUDE[footer-include](../../includes/footer-banner.md)]