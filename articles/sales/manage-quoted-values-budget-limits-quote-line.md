---
title: 基于项目的报价单明细概述
description: 此主题提供为项目工作使用基于项目的报价单明细的信息。
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: ea54d83b1e26d1ee3520dbfab9ba56ffd1191dc9
ms.sourcegitcommit: f6f86e80dfef15a7b5f9174b55dddf410522f7c8
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/31/2020
ms.locfileid: "4181846"
---
# <a name="project-based-quote-lines-overview"></a><span data-ttu-id="fb783-103">基于项目的报价单明细概述</span><span class="sxs-lookup"><span data-stu-id="fb783-103">Project-based quote lines overview</span></span>

<span data-ttu-id="fb783-104">_**适用于：** 面向资源/非库存场景的 Project Operations_</span><span class="sxs-lookup"><span data-stu-id="fb783-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="fb783-105">基于项目的报价单明细用于帮助预估协定中的项目工作。</span><span class="sxs-lookup"><span data-stu-id="fb783-105">Project-based quote lines are designed to help estimate the project work on an engagement.</span></span> <span data-ttu-id="fb783-106">基于项目的报价单明细的结构可以通过以下概念为项目预估进行扩展：</span><span class="sxs-lookup"><span data-stu-id="fb783-106">The structure of a project-based quote line is extended for project estimates with the following concepts:</span></span>

- <span data-ttu-id="fb783-107">记帐方法</span><span class="sxs-lookup"><span data-stu-id="fb783-107">Billing Method</span></span>
- <span data-ttu-id="fb783-108">项目映射</span><span class="sxs-lookup"><span data-stu-id="fb783-108">Project Mapping</span></span>
- <span data-ttu-id="fb783-109">包括的交易类</span><span class="sxs-lookup"><span data-stu-id="fb783-109">Included Transaction classes</span></span>
- <span data-ttu-id="fb783-110">上限</span><span class="sxs-lookup"><span data-stu-id="fb783-110">Not-to-Exceed Limit</span></span>
- <span data-ttu-id="fb783-111">应计费设置</span><span class="sxs-lookup"><span data-stu-id="fb783-111">Chargeability setup</span></span>
- <span data-ttu-id="fb783-112">使用报价单明细详细信息的预估</span><span class="sxs-lookup"><span data-stu-id="fb783-112">Estimation using Quote Line Details</span></span>
- <span data-ttu-id="fb783-113">报价单明细客户</span><span class="sxs-lookup"><span data-stu-id="fb783-113">Quote line Customers</span></span>

<span data-ttu-id="fb783-114">下表提供了有关基于项目的报价单明细的 **常规** 选项卡上字段的信息。</span><span class="sxs-lookup"><span data-stu-id="fb783-114">The following table provides information about the fields on the **General** tab of project-based quote line.</span></span> <span data-ttu-id="fb783-115">这些字段帮助为项目工作的详细、全面的预估建立基础。</span><span class="sxs-lookup"><span data-stu-id="fb783-115">These fields help set up the basis for a detailed, ground-up estimation for project work.</span></span>

| <span data-ttu-id="fb783-116">**字段**</span><span class="sxs-lookup"><span data-stu-id="fb783-116">**Field**</span></span> | <span data-ttu-id="fb783-117">**说明**</span><span class="sxs-lookup"><span data-stu-id="fb783-117">**Description**</span></span> | <span data-ttu-id="fb783-118">**下游影响**</span><span class="sxs-lookup"><span data-stu-id="fb783-118">**Downstream impact**</span></span> |
| --- | --- | --- |
| <span data-ttu-id="fb783-119">客户</span><span class="sxs-lookup"><span data-stu-id="fb783-119">Name</span></span> | <span data-ttu-id="fb783-120">应会帮助您识别正在预估的报价单的分散部分的报价单明细的名称。</span><span class="sxs-lookup"><span data-stu-id="fb783-120">The name of quote line which should help you identify the discrete component of the quote that is being estimated.</span></span> | <span data-ttu-id="fb783-121">将复制到此报价单赢单时从报价单明细创建的项目合同子项。</span><span class="sxs-lookup"><span data-stu-id="fb783-121">Copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="fb783-122">记帐方法</span><span class="sxs-lookup"><span data-stu-id="fb783-122">Billing Method</span></span> | <span data-ttu-id="fb783-123">在从商机创建的报价单中，此值从商机明细中的相应字段复制。</span><span class="sxs-lookup"><span data-stu-id="fb783-123">On a quote created from an opportunity, this value is copied from the corresponding field on the opportunity line.</span></span> <span data-ttu-id="fb783-124">此字段包括 Dynamics 365 Project Operations 支持的两个主要合同签订模型：</span><span class="sxs-lookup"><span data-stu-id="fb783-124">This field includes the two main contracting models supported by Dynamics 365 Project Operations:</span></span></br><span data-ttu-id="fb783-125">- 固定价格</span><span class="sxs-lookup"><span data-stu-id="fb783-125">- Fixed price</span></span></br><span data-ttu-id="fb783-126">- 时间和材料。</span><span class="sxs-lookup"><span data-stu-id="fb783-126">- Time and material.</span></span>| <span data-ttu-id="fb783-127">此字段值将复制到此报价单赢单时从报价单明细创建的项目合同子项。</span><span class="sxs-lookup"><span data-stu-id="fb783-127">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="fb783-128">Project</span><span class="sxs-lookup"><span data-stu-id="fb783-128">Project</span></span> | <span data-ttu-id="fb783-129">使用此可选字段可以识别将用于交付此协定中的工作的项目。</span><span class="sxs-lookup"><span data-stu-id="fb783-129">Use this optional field to identify the project that will be used to deliver the work on this engagement.</span></span> <span data-ttu-id="fb783-130">将项目映射到报价单明细时，它将帮助设置应计费任务，还可以帮助将基于项目的预估作为报价单明细详细信息引入报价单明细。</span><span class="sxs-lookup"><span data-stu-id="fb783-130">When a project is mapped to a quote line, it helps with setting up chargeable tasks and also with bringing in a project-based estimate to the quote line as quote line details.</span></span> <span data-ttu-id="fb783-131">当项目未映射到基于项目的报价单明细时，应通过创建每个报价单明细详细信息来手动创建预估。</span><span class="sxs-lookup"><span data-stu-id="fb783-131">When a project is not mapped to a project-based quote line, the estimate should be created manually by creating each quote line detail.</span></span> | <span data-ttu-id="fb783-132">此字段值将复制到此报价单赢单时从报价单明细创建的项目合同子项。</span><span class="sxs-lookup"><span data-stu-id="fb783-132">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="fb783-133">包括时间</span><span class="sxs-lookup"><span data-stu-id="fb783-133">Include Time</span></span> | <span data-ttu-id="fb783-134">**是**/**否** 标志指示此报价单明细的预估中是否包括所选项目的时间交易或人工成本。</span><span class="sxs-lookup"><span data-stu-id="fb783-134">A **Yes**/**No** flag indicates if time transactions or labor costs on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="fb783-135">**否** 值指示此报价单明细的预估中将不包括时间交易或人工成本。</span><span class="sxs-lookup"><span data-stu-id="fb783-135">A **No** value indicates that the time transactions or labor cost will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="fb783-136">**是** 值指示此报价单明细的预估中将包括时间交易或人工成本。</span><span class="sxs-lookup"><span data-stu-id="fb783-136">A **Yes** value indicates that the time transactions or labor cost will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="fb783-137">此字段值将复制到此报价单赢单时从报价单明细创建的项目合同子项。</span><span class="sxs-lookup"><span data-stu-id="fb783-137">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="fb783-138">包括支出</span><span class="sxs-lookup"><span data-stu-id="fb783-138">Include Expense</span></span> | <span data-ttu-id="fb783-139">**是**/**否** 标志指示此报价单明细的预估中是否包括所选项目的支出成本。</span><span class="sxs-lookup"><span data-stu-id="fb783-139">A **Yes**/**No** flag indicates if expense costs on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="fb783-140">**否** 值指示此报价单明细的预估中将不包括支出成本。</span><span class="sxs-lookup"><span data-stu-id="fb783-140">A **No** value indicates that the expense cost will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="fb783-141">**是** 值指示此报价单明细的预估中将包括支出成本。</span><span class="sxs-lookup"><span data-stu-id="fb783-141">A **Yes** value indicates that the expense cost will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="fb783-142">此字段值将复制到此报价单赢单时从报价单明细创建的项目合同子项。</span><span class="sxs-lookup"><span data-stu-id="fb783-142">This field value is copied over to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="fb783-143">包括费用</span><span class="sxs-lookup"><span data-stu-id="fb783-143">Include Fee</span></span> | <span data-ttu-id="fb783-144">**是**/**否** 标志指示此报价单明细的预估中是否包括所选项目的费用。</span><span class="sxs-lookup"><span data-stu-id="fb783-144">A **Yes**/**No** flag indicates if fees on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="fb783-145">**否** 值指示此报价单明细的预估中将不包括费用。</span><span class="sxs-lookup"><span data-stu-id="fb783-145">A **No** value indicates that the Fees will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="fb783-146">**是** 值指示此报价单明细的预估中将包括费用。</span><span class="sxs-lookup"><span data-stu-id="fb783-146">A **Yes** value indicates that the Fees will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="fb783-147">此字段值将复制到此报价单赢单时从报价单明细创建的项目合同子项。</span><span class="sxs-lookup"><span data-stu-id="fb783-147">This field value is copied to the Project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="fb783-148">配额数量</span><span class="sxs-lookup"><span data-stu-id="fb783-148">Quoted Amount</span></span> | <span data-ttu-id="fb783-149">这是将针对此基于项目的报价单明细上预测的所有工作向客户报价的金额。</span><span class="sxs-lookup"><span data-stu-id="fb783-149">This is amount that will be quoted to the customer for all the work forecasted on this project-based quote line.</span></span> <span data-ttu-id="fb783-150">在从商机创建的报价单中，此值从商机明细中的 **客户预算** 字段复制。</span><span class="sxs-lookup"><span data-stu-id="fb783-150">On a quote created from an opportunity, this value is copied from the **Customer Budget** field on the opportunity line.</span></span> <span data-ttu-id="fb783-151">当基于项目的报价单明细包含明细详细信息时，此字段将被锁定以进行编辑，并从报价单明细详细信息中的金额汇总。</span><span class="sxs-lookup"><span data-stu-id="fb783-151">When the project-based quote line has line details, this field is locked for editing and is summarized from the amount on the quote line details.</span></span> | <span data-ttu-id="fb783-152">此字段值将复制到此报价单赢单时从报价单明细创建的项目合同子项。</span><span class="sxs-lookup"><span data-stu-id="fb783-152">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="fb783-153">预计税款</span><span class="sxs-lookup"><span data-stu-id="fb783-153">Estimated Tax</span></span> | <span data-ttu-id="fb783-154">这是一个可编辑字段，供用户在报价单明细中添加预估税款金额。</span><span class="sxs-lookup"><span data-stu-id="fb783-154">This is an editable field for the user to add the estimated tax amount on the quote line.</span></span> <span data-ttu-id="fb783-155">当基于项目的报价单明细包含明细详细信息时，此字段将被锁定以进行编辑，并从报价单明细详细信息中的税款金额汇总。</span><span class="sxs-lookup"><span data-stu-id="fb783-155">When a project-based quote line has line details, this field is locked for editing and is summarized from the tax amount on the quote line details.</span></span> | <span data-ttu-id="fb783-156">此字段值将复制到此报价单赢单时从报价单明细创建的项目合同子项。</span><span class="sxs-lookup"><span data-stu-id="fb783-156">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="fb783-157">税后报价金额</span><span class="sxs-lookup"><span data-stu-id="fb783-157">Quoted Amount after Tax</span></span> | <span data-ttu-id="fb783-158">此字段是税后的报价单明细金额，是只读的。</span><span class="sxs-lookup"><span data-stu-id="fb783-158">This field is the quote line amount after tax and is read-only.</span></span> <span data-ttu-id="fb783-159">此字段中的金额计算为 *报价金额 + 税款*。</span><span class="sxs-lookup"><span data-stu-id="fb783-159">The amount in this field is calculated as *Quoted Amount + Tax*.</span></span> | <span data-ttu-id="fb783-160">此字段值将复制到此报价单赢单时从报价单明细创建的项目合同子项。</span><span class="sxs-lookup"><span data-stu-id="fb783-160">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="fb783-161">上限</span><span class="sxs-lookup"><span data-stu-id="fb783-161">Not-to-exceed Limit</span></span> | <span data-ttu-id="fb783-162">此字段可编辑，仅在具有 **时间和材料** 计费方法的基于项目的报价单明细中可用。</span><span class="sxs-lookup"><span data-stu-id="fb783-162">This field is editable and is only available on project-based quote lines that have a **Time and Material** billing method.</span></span> | <span data-ttu-id="fb783-163">此字段值将复制到此报价单赢单时从报价单明细创建的项目合同子项。</span><span class="sxs-lookup"><span data-stu-id="fb783-163">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="fb783-164">客户预算</span><span class="sxs-lookup"><span data-stu-id="fb783-164">Customer Budget</span></span> | <span data-ttu-id="fb783-165">此字段可编辑，如果报价单是从商机创建的，此字段将从商机明细中的相应字段复制。</span><span class="sxs-lookup"><span data-stu-id="fb783-165">This field is editable and is copied from the corresponding field on the opportunity line if the quote was created from an opportunity.</span></span> | <span data-ttu-id="fb783-166">此字段值将复制到此报价单赢单时从报价单明细创建的项目合同子项。</span><span class="sxs-lookup"><span data-stu-id="fb783-166">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |

## <a name="validation-rules-for-fields-on-the-general-tab-of-project-based-quote-lines"></a><span data-ttu-id="fb783-167">基于项目的报价单明细的“常规”选项卡上字段的验证规则</span><span class="sxs-lookup"><span data-stu-id="fb783-167">Validation rules for fields on the General tab of project-based quote lines</span></span>

<span data-ttu-id="fb783-168">**规则 1**：所选项目上的某个交易类只能包含在报价单的一个基于项目的报价单明细中。</span><span class="sxs-lookup"><span data-stu-id="fb783-168">**Rule 1**: A certain transaction class on the selected project can only be included on one project-based quote line of a quote.</span></span>

<span data-ttu-id="fb783-169">**规则 2**：如果商机有多个报价单，可能存在来自不同报价单的报价单明细，它们均引用同一个项目并包含相同的交易类。</span><span class="sxs-lookup"><span data-stu-id="fb783-169">**Rule 2**: If an opportunity has multiple quotes, there can be quote lines from different quotes that all reference the same project and include the same transaction class.</span></span>

<span data-ttu-id="fb783-170">**规则 3**：如果报价单不属于同一商机，则不能包括同一个项目和交易类。</span><span class="sxs-lookup"><span data-stu-id="fb783-170">**Rule 3**: If the quotes do not belong to the same opportunity, they can't include the same project and transaction class.</span></span>

<table border="1" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="61" valign="top">
                <p><span data-ttu-id="fb783-171">
                    <strong>商机</strong>
                </span><span class="sxs-lookup"><span data-stu-id="fb783-171">
                    <strong>Opportunity</strong>
                </span></span></p>
            </td>
            <td width="41" valign="top">
                <p><span data-ttu-id="fb783-172">
                    <strong>报价单</strong>
                </span><span class="sxs-lookup"><span data-stu-id="fb783-172">
                    <strong>Quote</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="fb783-173">
                    <strong>报价单明细</strong>
                </span><span class="sxs-lookup"><span data-stu-id="fb783-173">
                    <strong>Quote line</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="fb783-174">
                    <strong>Project</strong>
                </span><span class="sxs-lookup"><span data-stu-id="fb783-174">
                    <strong>Project</strong>
                </span></span></p>
            </td>
            <td width="48" valign="top">
                <p><span data-ttu-id="fb783-175">
                    <strong>包括时间</strong>
                </span><span class="sxs-lookup"><span data-stu-id="fb783-175">
                    <strong>Include time</strong>
                </span></span></p>
            </td>
            <td width="48" valign="top">
                <p><span data-ttu-id="fb783-176">
                    <strong>包括支出</strong>
                </span><span class="sxs-lookup"><span data-stu-id="fb783-176">
                    <strong>Include expense</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="fb783-177">
                    <strong>添加</strong>
                </span><span class="sxs-lookup"><span data-stu-id="fb783-177">
                    <strong>Include</strong>
                </span></span></p>
                <p><span data-ttu-id="fb783-178">
                    <strong>费用</strong>
                </span><span class="sxs-lookup"><span data-stu-id="fb783-178">
                    <strong>fee</strong>
                </span></span></p>
            </td>
            <td width="54" valign="top">
                <p><span data-ttu-id="fb783-179">
                    <strong>有效/无效</strong>
                </span><span class="sxs-lookup"><span data-stu-id="fb783-179">
                    <strong>Valid/ Not valid</strong>
                </span></span></p>
            </td>
            <td width="308" valign="top">
                <p><span data-ttu-id="fb783-180">
                    <strong>原因</strong>
                </span><span class="sxs-lookup"><span data-stu-id="fb783-180">
                    <strong>Reason</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="fb783-181">O1</span><span class="sxs-lookup"><span data-stu-id="fb783-181">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="fb783-182">Q1</span><span class="sxs-lookup"><span data-stu-id="fb783-182">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="fb783-183">QL1</span><span class="sxs-lookup"><span data-stu-id="fb783-183">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="fb783-184">P1</span><span class="sxs-lookup"><span data-stu-id="fb783-184">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="fb783-185">是</span><span class="sxs-lookup"><span data-stu-id="fb783-185">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="fb783-186">是</span><span class="sxs-lookup"><span data-stu-id="fb783-186">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="fb783-187">是</span><span class="sxs-lookup"><span data-stu-id="fb783-187">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="fb783-188">无效</span><span class="sxs-lookup"><span data-stu-id="fb783-188">Not valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="fb783-189">违反规则 #1。</span><span class="sxs-lookup"><span data-stu-id="fb783-189">Violation of Rule #1.</span></span> <span data-ttu-id="fb783-190">P1 项目的时间、支出和费用包含在两个报价单明细 QL1 和 QL2 中。</span><span class="sxs-lookup"><span data-stu-id="fb783-190">Time, Expense, and Fees on P1 project are included on both quote lines, QL1 and QL2.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="fb783-191">O1</span><span class="sxs-lookup"><span data-stu-id="fb783-191">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="fb783-192">Q1</span><span class="sxs-lookup"><span data-stu-id="fb783-192">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="fb783-193">QL2</span><span class="sxs-lookup"><span data-stu-id="fb783-193">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="fb783-194">P1</span><span class="sxs-lookup"><span data-stu-id="fb783-194">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="fb783-195">是</span><span class="sxs-lookup"><span data-stu-id="fb783-195">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="fb783-196">是</span><span class="sxs-lookup"><span data-stu-id="fb783-196">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="fb783-197">是</span><span class="sxs-lookup"><span data-stu-id="fb783-197">Yes</span></span> </p>
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
<span data-ttu-id="fb783-198">O1</span><span class="sxs-lookup"><span data-stu-id="fb783-198">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="fb783-199">Q1</span><span class="sxs-lookup"><span data-stu-id="fb783-199">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="fb783-200">QL1</span><span class="sxs-lookup"><span data-stu-id="fb783-200">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="fb783-201">P1</span><span class="sxs-lookup"><span data-stu-id="fb783-201">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="fb783-202">是</span><span class="sxs-lookup"><span data-stu-id="fb783-202">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="fb783-203">No</span><span class="sxs-lookup"><span data-stu-id="fb783-203">No</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="fb783-204">是</span><span class="sxs-lookup"><span data-stu-id="fb783-204">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="fb783-205">无效</span><span class="sxs-lookup"><span data-stu-id="fb783-205">Not valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="fb783-206">违反规则 #1。</span><span class="sxs-lookup"><span data-stu-id="fb783-206">Violation of Rule #1.</span></span> <span data-ttu-id="fb783-207">P1 项目的时间和费用包含在两个报价单明细 QL1 和 QL2 中。</span><span class="sxs-lookup"><span data-stu-id="fb783-207">Time and Fees on P1 project are included on both quote lines, QL1 and QL2.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="fb783-208">O1</span><span class="sxs-lookup"><span data-stu-id="fb783-208">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="fb783-209">Q1</span><span class="sxs-lookup"><span data-stu-id="fb783-209">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="fb783-210">QL2</span><span class="sxs-lookup"><span data-stu-id="fb783-210">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="fb783-211">P1</span><span class="sxs-lookup"><span data-stu-id="fb783-211">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="fb783-212">是</span><span class="sxs-lookup"><span data-stu-id="fb783-212">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="fb783-213">是</span><span class="sxs-lookup"><span data-stu-id="fb783-213">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="fb783-214">是</span><span class="sxs-lookup"><span data-stu-id="fb783-214">Yes</span></span> </p>
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
<span data-ttu-id="fb783-215">O1</span><span class="sxs-lookup"><span data-stu-id="fb783-215">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="fb783-216">Q1</span><span class="sxs-lookup"><span data-stu-id="fb783-216">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="fb783-217">QL1</span><span class="sxs-lookup"><span data-stu-id="fb783-217">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="fb783-218">P1</span><span class="sxs-lookup"><span data-stu-id="fb783-218">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="fb783-219">是</span><span class="sxs-lookup"><span data-stu-id="fb783-219">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="fb783-220">No</span><span class="sxs-lookup"><span data-stu-id="fb783-220">No</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="fb783-221">是</span><span class="sxs-lookup"><span data-stu-id="fb783-221">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="fb783-222">有效</span><span class="sxs-lookup"><span data-stu-id="fb783-222">Valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                 <p>
<span data-ttu-id="fb783-223">P1 项目的时间和费用包含在 QL1 上。</span><span class="sxs-lookup"><span data-stu-id="fb783-223">Time and fees on P1 project are included on QL1.</span></span>
<span data-ttu-id="fb783-224">P1 项目的支出包含在 QL2 中。</span><span class="sxs-lookup"><span data-stu-id="fb783-224">Expense on P1 project is included on QL2.</span></span>
<span data-ttu-id="fb783-225">每个报价单明细中包含的内容没有重叠，因此是有效的。</span><span class="sxs-lookup"><span data-stu-id="fb783-225">There is no overlap in what is being included on each quote line so it is valid.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="fb783-226">O1</span><span class="sxs-lookup"><span data-stu-id="fb783-226">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="fb783-227">Q1</span><span class="sxs-lookup"><span data-stu-id="fb783-227">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="fb783-228">QL2</span><span class="sxs-lookup"><span data-stu-id="fb783-228">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="fb783-229">P1</span><span class="sxs-lookup"><span data-stu-id="fb783-229">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="fb783-230">No</span><span class="sxs-lookup"><span data-stu-id="fb783-230">No</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="fb783-231">是</span><span class="sxs-lookup"><span data-stu-id="fb783-231">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="fb783-232">No</span><span class="sxs-lookup"><span data-stu-id="fb783-232">No</span></span> </p>
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
<span data-ttu-id="fb783-233">O1</span><span class="sxs-lookup"><span data-stu-id="fb783-233">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="fb783-234">Q1</span><span class="sxs-lookup"><span data-stu-id="fb783-234">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="fb783-235">QL1</span><span class="sxs-lookup"><span data-stu-id="fb783-235">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="fb783-236">P1</span><span class="sxs-lookup"><span data-stu-id="fb783-236">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="fb783-237">是</span><span class="sxs-lookup"><span data-stu-id="fb783-237">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="fb783-238">是</span><span class="sxs-lookup"><span data-stu-id="fb783-238">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="fb783-239">是</span><span class="sxs-lookup"><span data-stu-id="fb783-239">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="fb783-240">无效</span><span class="sxs-lookup"><span data-stu-id="fb783-240">Not valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="fb783-241">违反上方的规则 #1</span><span class="sxs-lookup"><span data-stu-id="fb783-241">Violation of Rule #1 above</span></span> </p>
                <p>
<span data-ttu-id="fb783-242">Q1 包含整个项目 P1 的时间、支出和费用。</span><span class="sxs-lookup"><span data-stu-id="fb783-242">Q1 includes Time, Expenses, and Fees for the whole project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="fb783-243">QL2 包括整个项目 P1 的时间、支出和费用，与 Q1 中所包含的内容重叠。</span><span class="sxs-lookup"><span data-stu-id="fb783-243">QL2 includes Time, Expenses, and Fees for the whole project P1 and overlaps with what is included on Q1.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="fb783-244">O1</span><span class="sxs-lookup"><span data-stu-id="fb783-244">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="fb783-245">Q1</span><span class="sxs-lookup"><span data-stu-id="fb783-245">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="fb783-246">QL2</span><span class="sxs-lookup"><span data-stu-id="fb783-246">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="fb783-247">P1</span><span class="sxs-lookup"><span data-stu-id="fb783-247">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="fb783-248">是</span><span class="sxs-lookup"><span data-stu-id="fb783-248">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="fb783-249">是</span><span class="sxs-lookup"><span data-stu-id="fb783-249">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="fb783-250">是</span><span class="sxs-lookup"><span data-stu-id="fb783-250">Yes</span></span> </p>
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
<span data-ttu-id="fb783-251">O1</span><span class="sxs-lookup"><span data-stu-id="fb783-251">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="fb783-252">Q1</span><span class="sxs-lookup"><span data-stu-id="fb783-252">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="fb783-253">QL1</span><span class="sxs-lookup"><span data-stu-id="fb783-253">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="fb783-254">P1</span><span class="sxs-lookup"><span data-stu-id="fb783-254">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="fb783-255">是</span><span class="sxs-lookup"><span data-stu-id="fb783-255">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="fb783-256">是</span><span class="sxs-lookup"><span data-stu-id="fb783-256">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="fb783-257">是</span><span class="sxs-lookup"><span data-stu-id="fb783-257">Yes</span></span> </p>
            </td>
            <td width="54" valign="top">
                <p>
<span data-ttu-id="fb783-258">有效</span><span class="sxs-lookup"><span data-stu-id="fb783-258">Valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="fb783-259">根据规则 #2，Q1 和 Q2 是同一个商机中的两个报价单，因此它们都可以针对项目的相同组件进行预估。</span><span class="sxs-lookup"><span data-stu-id="fb783-259">Based on Rule #2, Q1 and Q2 are two quotes on the same opportunity, so they can both estimate for the same components of a project.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="fb783-260">O1</span><span class="sxs-lookup"><span data-stu-id="fb783-260">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="fb783-261">Q2</span><span class="sxs-lookup"><span data-stu-id="fb783-261">Q2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="fb783-262">Q2 上的 QL1</span><span class="sxs-lookup"><span data-stu-id="fb783-262">QL1 on Q2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="fb783-263">P1</span><span class="sxs-lookup"><span data-stu-id="fb783-263">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="fb783-264">是</span><span class="sxs-lookup"><span data-stu-id="fb783-264">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="fb783-265">是</span><span class="sxs-lookup"><span data-stu-id="fb783-265">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="fb783-266">是</span><span class="sxs-lookup"><span data-stu-id="fb783-266">Yes</span></span> </p>
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
<span data-ttu-id="fb783-267">O1</span><span class="sxs-lookup"><span data-stu-id="fb783-267">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="fb783-268">Q1</span><span class="sxs-lookup"><span data-stu-id="fb783-268">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="fb783-269">QL1</span><span class="sxs-lookup"><span data-stu-id="fb783-269">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="fb783-270">P1</span><span class="sxs-lookup"><span data-stu-id="fb783-270">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="fb783-271">是</span><span class="sxs-lookup"><span data-stu-id="fb783-271">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="fb783-272">是</span><span class="sxs-lookup"><span data-stu-id="fb783-272">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="fb783-273">是</span><span class="sxs-lookup"><span data-stu-id="fb783-273">Yes</span></span> </p>
            </td>
            <td width="54" valign="top">
                <p>
<span data-ttu-id="fb783-274">有效</span><span class="sxs-lookup"><span data-stu-id="fb783-274">Valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="fb783-275">根据规则 #3，Q1 和 Q2 是不同商机中的两个报价单，因此它们不能针对项目的相同组件进行预估。</span><span class="sxs-lookup"><span data-stu-id="fb783-275">Based on Rule #3, Q1 and Q2 are two quotes on different opportunities, so they can't estimate for the same components of the same project.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="fb783-276">O2</span><span class="sxs-lookup"><span data-stu-id="fb783-276">O2</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="fb783-277">Q1</span><span class="sxs-lookup"><span data-stu-id="fb783-277">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="fb783-278">QL1</span><span class="sxs-lookup"><span data-stu-id="fb783-278">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="fb783-279">P1</span><span class="sxs-lookup"><span data-stu-id="fb783-279">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="fb783-280">是</span><span class="sxs-lookup"><span data-stu-id="fb783-280">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="fb783-281">是</span><span class="sxs-lookup"><span data-stu-id="fb783-281">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="fb783-282">是</span><span class="sxs-lookup"><span data-stu-id="fb783-282">Yes</span></span> </p>
            </td>
            <td width="54" valign="top">
                <p>
<span data-ttu-id="fb783-283">无效</span><span class="sxs-lookup"><span data-stu-id="fb783-283">Not Valid</span></span> </p>
            </td>
        </tr>
    </tbody>
</table>

