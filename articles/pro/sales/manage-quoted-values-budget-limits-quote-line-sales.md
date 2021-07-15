---
title: 基于项目的报价单明细概述
description: 此主题提供为项目工作使用基于项目的报价单明细的信息。
author: rumant
ms.date: 03/30/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.custom: intro-internal
ms.openlocfilehash: b7076a4b9280472f8c30d0b58c3aa9b9bc86d651
ms.sourcegitcommit: 0fafe022731f0e1e8693382ff906e3f8541d34ca
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 07/07/2021
ms.locfileid: "6369860"
---
# <a name="project-based-quote-lines-overview"></a><span data-ttu-id="b6fe9-103">基于项目的报价单明细概述</span><span class="sxs-lookup"><span data-stu-id="b6fe9-103">Project-based quote lines overview</span></span> 

<span data-ttu-id="b6fe9-104">_**适用于：** 精简部署 - 估价交易开单，基于资源/非库存场景的 Project Operations_</span><span class="sxs-lookup"><span data-stu-id="b6fe9-104">_**Applies To:** Lite deployment - deal to proforma invoicing, Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="b6fe9-105">基于项目的报价单明细用于帮助预估协定中的项目工作。</span><span class="sxs-lookup"><span data-stu-id="b6fe9-105">Project-based quote lines are designed to help estimate the project work on an engagement.</span></span> <span data-ttu-id="b6fe9-106">基于项目的报价单明细的结构可以通过以下概念为项目预估进行扩展：</span><span class="sxs-lookup"><span data-stu-id="b6fe9-106">The structure of a project-based quote line is extended for project estimates with the following concepts:</span></span>

- <span data-ttu-id="b6fe9-107">记帐方法</span><span class="sxs-lookup"><span data-stu-id="b6fe9-107">Billing Method</span></span>
- <span data-ttu-id="b6fe9-108">项目和任务映射</span><span class="sxs-lookup"><span data-stu-id="b6fe9-108">Project and Task Mapping</span></span>
- <span data-ttu-id="b6fe9-109">包括的交易类</span><span class="sxs-lookup"><span data-stu-id="b6fe9-109">Included Transaction classes</span></span>
- <span data-ttu-id="b6fe9-110">上限</span><span class="sxs-lookup"><span data-stu-id="b6fe9-110">Not-to-Exceed Limit</span></span>
- <span data-ttu-id="b6fe9-111">应计费设置</span><span class="sxs-lookup"><span data-stu-id="b6fe9-111">Chargeability setup</span></span>
- <span data-ttu-id="b6fe9-112">使用报价单明细详细信息的预估</span><span class="sxs-lookup"><span data-stu-id="b6fe9-112">Estimation using Quote Line Details</span></span>
- <span data-ttu-id="b6fe9-113">报价单明细客户</span><span class="sxs-lookup"><span data-stu-id="b6fe9-113">Quote line Customers</span></span>

<span data-ttu-id="b6fe9-114">下表提供了有关基于项目的报价单明细的 **常规** 选项卡上字段的信息。</span><span class="sxs-lookup"><span data-stu-id="b6fe9-114">The following table provides information about the fields on the **General** tab of project-based quote line.</span></span> <span data-ttu-id="b6fe9-115">这些字段帮助为项目工作的详细、全面的预估建立基础。</span><span class="sxs-lookup"><span data-stu-id="b6fe9-115">These fields help set up the basis for a detailed, ground-up estimation for project work.</span></span>

| <span data-ttu-id="b6fe9-116">**字段**</span><span class="sxs-lookup"><span data-stu-id="b6fe9-116">**Field**</span></span> | <span data-ttu-id="b6fe9-117">**说明**</span><span class="sxs-lookup"><span data-stu-id="b6fe9-117">**Description**</span></span> | <span data-ttu-id="b6fe9-118">**下游影响**</span><span class="sxs-lookup"><span data-stu-id="b6fe9-118">**Downstream impact**</span></span> |
| --- | --- | --- |
| <span data-ttu-id="b6fe9-119">客户</span><span class="sxs-lookup"><span data-stu-id="b6fe9-119">Name</span></span> | <span data-ttu-id="b6fe9-120">报价单明细的名称，可帮助您确定估计的报价单的离散组件。</span><span class="sxs-lookup"><span data-stu-id="b6fe9-120">The name of quote line that helps you to identify the discrete component of the quote that is being estimated.</span></span> | <span data-ttu-id="b6fe9-121">将复制到此报价单赢单时从报价单明细创建的项目合同子项。</span><span class="sxs-lookup"><span data-stu-id="b6fe9-121">Copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="b6fe9-122">记帐方法</span><span class="sxs-lookup"><span data-stu-id="b6fe9-122">Billing Method</span></span> | <span data-ttu-id="b6fe9-123">在从商机创建的报价单中，此值从商机明细中的相应字段复制。</span><span class="sxs-lookup"><span data-stu-id="b6fe9-123">On a quote created from an opportunity, this value is copied from the corresponding field on the opportunity line.</span></span> <span data-ttu-id="b6fe9-124">此字段包括 Dynamics 365 Project Operations 支持的两个主要合同模型：</span><span class="sxs-lookup"><span data-stu-id="b6fe9-124">This field includes the two main contracting models supported by Dynamics 365 Project Operations:</span></span></br><span data-ttu-id="b6fe9-125">- 固定价格</span><span class="sxs-lookup"><span data-stu-id="b6fe9-125">- Fixed price</span></span></br><span data-ttu-id="b6fe9-126">- 时间和材料。</span><span class="sxs-lookup"><span data-stu-id="b6fe9-126">- Time and material.</span></span>| <span data-ttu-id="b6fe9-127">该值复制到赢得报价单时从此报价单明细创建的项目合同子项。</span><span class="sxs-lookup"><span data-stu-id="b6fe9-127">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="b6fe9-128">Project</span><span class="sxs-lookup"><span data-stu-id="b6fe9-128">Project</span></span> | <span data-ttu-id="b6fe9-129">使用此可选字段可以识别将用于交付此协定中的工作的项目。</span><span class="sxs-lookup"><span data-stu-id="b6fe9-129">Use this optional field to identify the project that will be used to deliver the work on this engagement.</span></span> <span data-ttu-id="b6fe9-130">将项目映射到报价单明细时，它将帮助设置应计费任务，还可以帮助将基于项目的预估作为报价单明细详细信息引入报价单明细。</span><span class="sxs-lookup"><span data-stu-id="b6fe9-130">When a project is mapped to a quote line, it helps with setting up chargeable tasks and also with bringing in a project-based estimate to the quote line as quote line details.</span></span> <span data-ttu-id="b6fe9-131">当项目未映射到基于项目的报价单明细时，应通过创建每个报价单明细详细信息来手动创建预估。</span><span class="sxs-lookup"><span data-stu-id="b6fe9-131">When a project is not mapped to a project-based quote line, the estimate should be created manually by creating each quote line detail.</span></span> | <span data-ttu-id="b6fe9-132">该值复制到赢得报价单时从此报价单明细创建的项目合同子项。</span><span class="sxs-lookup"><span data-stu-id="b6fe9-132">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span>|
| <span data-ttu-id="b6fe9-133">包含的任务</span><span class="sxs-lookup"><span data-stu-id="b6fe9-133">Included Tasks</span></span> | <span data-ttu-id="b6fe9-134">指示此报价单明细是否用于所选项目的全部或部分项目任务。</span><span class="sxs-lookup"><span data-stu-id="b6fe9-134">Indicates if this quote line is used for all or some of the project tasks for the selected project.</span></span> <span data-ttu-id="b6fe9-135">此字段具有以下可能的值：</span><span class="sxs-lookup"><span data-stu-id="b6fe9-135">This field has the following possible values:</span></span></br><span data-ttu-id="b6fe9-136">- 所有项目任务</span><span class="sxs-lookup"><span data-stu-id="b6fe9-136">- All project tasks</span></span></br><span data-ttu-id="b6fe9-137">- 仅所选项目任务</span><span class="sxs-lookup"><span data-stu-id="b6fe9-137">- Selected project tasks only</span></span></br><span data-ttu-id="b6fe9-138">此字段中的空白值等效于 **所有项目任务** 选项。</span><span class="sxs-lookup"><span data-stu-id="b6fe9-138">A blank value in this field is equivalent to the **All project tasks** option.</span></span> | <span data-ttu-id="b6fe9-139">如果在项目页上选择了 **仅限选定的项目任务**，则 **任务记帐设置** 选项卡允许您选择特定任务，以将这些任务与此报价单明细关联。</span><span class="sxs-lookup"><span data-stu-id="b6fe9-139">When **Selected project tasks only** is selected on the project page, the **Task billing setup** tab allows you to select specific tasks to associate them to this quote line.</span></span> <span data-ttu-id="b6fe9-140">该值复制到赢得报价单时从此报价单明细创建的项目合同子项。</span><span class="sxs-lookup"><span data-stu-id="b6fe9-140">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="b6fe9-141">包括时间</span><span class="sxs-lookup"><span data-stu-id="b6fe9-141">Include Time</span></span> | <span data-ttu-id="b6fe9-142">**是**/**否** 值指明所选项目的时间交易或人工成本是否将包含在此报价单明细估算中。</span><span class="sxs-lookup"><span data-stu-id="b6fe9-142">A **Yes**/**No** value indicates if time transactions or labor costs on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="b6fe9-143">**否** 值指示此报价单明细的预估中将不包括时间交易或人工成本。</span><span class="sxs-lookup"><span data-stu-id="b6fe9-143">A **No** value indicates that the time transactions or labor cost will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="b6fe9-144">**是** 值指示此报价单明细的预估中将包括时间交易或人工成本。</span><span class="sxs-lookup"><span data-stu-id="b6fe9-144">A **Yes** value indicates that the time transactions or labor cost will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="b6fe9-145">该值复制到赢得报价单时从此报价单明细创建的项目合同子项。</span><span class="sxs-lookup"><span data-stu-id="b6fe9-145">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="b6fe9-146">包括支出</span><span class="sxs-lookup"><span data-stu-id="b6fe9-146">Include Expense</span></span> | <span data-ttu-id="b6fe9-147">**是**/**否** 值指明所选项目的支出成本是否将包含在此报价单明细估算中。</span><span class="sxs-lookup"><span data-stu-id="b6fe9-147">A **Yes**/**No** value indicates if expense costs on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="b6fe9-148">**否** 值指示此报价单明细的预估中将不包括支出成本。</span><span class="sxs-lookup"><span data-stu-id="b6fe9-148">A **No** value indicates that the expense cost will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="b6fe9-149">**是** 值指示此报价单明细的预估中将包括支出成本。</span><span class="sxs-lookup"><span data-stu-id="b6fe9-149">A **Yes** value indicates that the expense cost will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="b6fe9-150">该值复制到赢得报价单时从此报价单明细创建的项目合同子项。</span><span class="sxs-lookup"><span data-stu-id="b6fe9-150">This value is copied over to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="b6fe9-151">包括材料</span><span class="sxs-lookup"><span data-stu-id="b6fe9-151">Include Material</span></span> | <span data-ttu-id="b6fe9-152">**是**/**否** 值指明所选项目的材料成本是否将包含在此报价单明细估算中。</span><span class="sxs-lookup"><span data-stu-id="b6fe9-152">A **Yes**/**No** value indicates if material costs on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="b6fe9-153">**否** 值指明材料成本将不包含在此报价单明细估算中。</span><span class="sxs-lookup"><span data-stu-id="b6fe9-153">A **No** value indicates that the material costs will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="b6fe9-154">**是** 值指明材料成本将包含在此报价单明细估算中。</span><span class="sxs-lookup"><span data-stu-id="b6fe9-154">A **Yes** value indicates that the material costs will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="b6fe9-155">该值复制到赢得报价单时从此报价单明细创建的项目合同子项。</span><span class="sxs-lookup"><span data-stu-id="b6fe9-155">This value is copied over to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="b6fe9-156">包括费用</span><span class="sxs-lookup"><span data-stu-id="b6fe9-156">Include Fee</span></span> | <span data-ttu-id="b6fe9-157">**是**/**否** 值指明所选项目的费用是否将包含在此报价单明细估算中。</span><span class="sxs-lookup"><span data-stu-id="b6fe9-157">A **Yes**/**No** value indicates if fees on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="b6fe9-158">**否** 值指示此报价单明细的预估中将不包括费用。</span><span class="sxs-lookup"><span data-stu-id="b6fe9-158">A **No** value indicates that the fees will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="b6fe9-159">**是** 值指示此报价单明细的预估中将包括费用。</span><span class="sxs-lookup"><span data-stu-id="b6fe9-159">A **Yes** value indicates that the fees will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="b6fe9-160">该值复制到赢得报价单时从此报价单明细创建的项目合同子项。</span><span class="sxs-lookup"><span data-stu-id="b6fe9-160">This value is copied to the Project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="b6fe9-161">配额数量</span><span class="sxs-lookup"><span data-stu-id="b6fe9-161">Quoted Amount</span></span> | <span data-ttu-id="b6fe9-162">这是针对基于项目的报价单明细中预测的所有工作将向客户报价的金额。</span><span class="sxs-lookup"><span data-stu-id="b6fe9-162">This is the amount that will be quoted to the customer for all the work forecasted on this project-based quote line.</span></span> <span data-ttu-id="b6fe9-163">在从商机创建的报价单中，此值从商机明细中的 **客户预算** 字段复制。</span><span class="sxs-lookup"><span data-stu-id="b6fe9-163">On a quote created from an opportunity, this value is copied from the **Customer Budget** field on the opportunity line.</span></span> <span data-ttu-id="b6fe9-164">当基于项目的报价单明细包含明细详细信息时，此字段将被锁定以进行编辑，并从报价单明细详细信息中的金额汇总。</span><span class="sxs-lookup"><span data-stu-id="b6fe9-164">When the project-based quote line has line details, this field is locked for editing and is summarized from the amount on the quote line details.</span></span> | <span data-ttu-id="b6fe9-165">该值复制到赢得报价单时从此报价单明细创建的项目合同子项。</span><span class="sxs-lookup"><span data-stu-id="b6fe9-165">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="b6fe9-166">预计税款</span><span class="sxs-lookup"><span data-stu-id="b6fe9-166">Estimated Tax</span></span> | <span data-ttu-id="b6fe9-167">这是一个可编辑字段，供用户在报价单明细中添加预估税款金额。</span><span class="sxs-lookup"><span data-stu-id="b6fe9-167">This is an editable field for the user to add the estimated tax amount on the quote line.</span></span> <span data-ttu-id="b6fe9-168">当基于项目的报价单明细包含明细详细信息时，此字段将被锁定以进行编辑，并从报价单明细详细信息中的税款金额汇总。</span><span class="sxs-lookup"><span data-stu-id="b6fe9-168">When a project-based quote line has line details, this field is locked for editing and is summarized from the tax amount on the quote line details.</span></span> | <span data-ttu-id="b6fe9-169">该值复制到赢得报价单时从此报价单明细创建的项目合同子项。</span><span class="sxs-lookup"><span data-stu-id="b6fe9-169">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="b6fe9-170">税后报价金额</span><span class="sxs-lookup"><span data-stu-id="b6fe9-170">Quoted Amount after Tax</span></span> | <span data-ttu-id="b6fe9-171">此字段是税后的报价单明细金额，是只读的。</span><span class="sxs-lookup"><span data-stu-id="b6fe9-171">This field is the quote line amount after tax and is read-only.</span></span> <span data-ttu-id="b6fe9-172">此字段中的金额计算为 *报价金额 + 税款*。</span><span class="sxs-lookup"><span data-stu-id="b6fe9-172">The amount in this field is calculated as *Quoted Amount + Tax*.</span></span> | <span data-ttu-id="b6fe9-173">该值复制到赢得报价单时从此报价单明细创建的项目合同子项。</span><span class="sxs-lookup"><span data-stu-id="b6fe9-173">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="b6fe9-174">上限</span><span class="sxs-lookup"><span data-stu-id="b6fe9-174">Not-to-exceed Limit</span></span> | <span data-ttu-id="b6fe9-175">此字段可编辑，仅在具有 **时间和材料** 计费方法的基于项目的报价单明细中可用。</span><span class="sxs-lookup"><span data-stu-id="b6fe9-175">This field is editable and is only available on project-based quote lines that have a **Time and Material** billing method.</span></span> | <span data-ttu-id="b6fe9-176">该值复制到赢得报价单时从此报价单明细创建的项目合同子项。</span><span class="sxs-lookup"><span data-stu-id="b6fe9-176">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="b6fe9-177">客户预算</span><span class="sxs-lookup"><span data-stu-id="b6fe9-177">Customer Budget</span></span> | <span data-ttu-id="b6fe9-178">此字段可编辑，如果报价单是从商机创建的，此字段将从商机明细中的相应字段复制。</span><span class="sxs-lookup"><span data-stu-id="b6fe9-178">This field is editable and is copied from the corresponding field on the opportunity line if the quote was created from an opportunity.</span></span> | <span data-ttu-id="b6fe9-179">该值复制到赢得报价单时从此报价单明细创建的项目合同子项。</span><span class="sxs-lookup"><span data-stu-id="b6fe9-179">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |


## <a name="validation-rules-for-fields-on-the-general-tab-of-project-based-quote-lines"></a><span data-ttu-id="b6fe9-180">基于项目的报价单明细的“常规”选项卡上字段的验证规则</span><span class="sxs-lookup"><span data-stu-id="b6fe9-180">Validation rules for fields on the General tab of project-based quote lines</span></span>

<span data-ttu-id="b6fe9-181">**规则 1**：如果 **包含的任务** 字段为空，或者将其设置为 **所有项目任务**，项目将包含在报价单明细中。</span><span class="sxs-lookup"><span data-stu-id="b6fe9-181">**Rule 1**: If the **Included Tasks** field is blank, or if it is set to **All project tasks**, a project is included in the quote line.</span></span>

<span data-ttu-id="b6fe9-182">**规则 2**：如果 **包含的任务** 字段为空，或者将其设置为 **所有项目任务**，项目和特定交易类只能包含在报价单的一个基于项目的报价单明细中。</span><span class="sxs-lookup"><span data-stu-id="b6fe9-182">**Rule 2**: If the **Included Tasks** field is blank, or if it is set to **All project tasks**, a project and a certain transaction class can only be included on one project-based quote line of a quote.</span></span>

<span data-ttu-id="b6fe9-183">**规则 3**：如果 **包含的任务** 字段设置为 **仅所选项目任务**，项目和特定交易类可以包含在报价单的多个基于项目的报价单明细中。</span><span class="sxs-lookup"><span data-stu-id="b6fe9-183">**Rule 3**: If the **Included Tasks** field is set to **Selected project tasks only**, a project and a certain transaction class can be included on multiple project-based quote lines of a quote.</span></span>

<span data-ttu-id="b6fe9-184">**规则 4**：如果商机有多个报价单，可能存在来自不同报价单的报价单明细，它们均引用同一个项目并包含相同的交易类。</span><span class="sxs-lookup"><span data-stu-id="b6fe9-184">**Rule 4**: If an opportunity has multiple quotes, there can be quote lines from different quotes that all reference the same project and include the same transaction class.</span></span>

<span data-ttu-id="b6fe9-185">**规则 5**：如果报价单不属于同一商机，则不能包括同一个项目和交易类。</span><span class="sxs-lookup"><span data-stu-id="b6fe9-185">**Rule 5**: If the quotes do not belong to the same opportunity, they can't include the same project and transaction class.</span></span>

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="59" valign="top">
                <p><span data-ttu-id="b6fe9-186">
                    <strong>商机</strong>
                </span><span class="sxs-lookup"><span data-stu-id="b6fe9-186">
                    <strong>Opportunity</strong>
                </span></span></p>
            </td>
            <td width="39" valign="top">
                <p><span data-ttu-id="b6fe9-187">
                    <strong>报价单</strong>
                </span><span class="sxs-lookup"><span data-stu-id="b6fe9-187">
                    <strong>Quote</strong>
                </span></span></p>
            </td>
            <td width="40" valign="top">
                <p><span data-ttu-id="b6fe9-188">
                    <strong>报价单明细</strong>
                </span><span class="sxs-lookup"><span data-stu-id="b6fe9-188">
                    <strong>Quote line</strong>
                </span></span></p>
            </td>
            <td width="41" valign="top">
                <p><span data-ttu-id="b6fe9-189">
                    <strong>Project</strong>
                </span><span class="sxs-lookup"><span data-stu-id="b6fe9-189">
                    <strong>Project</strong>
                </span></span></p>
            </td>
            <td width="77" valign="top">
                <p><span data-ttu-id="b6fe9-190">
                    <strong>包含的任务</strong>
                </span><span class="sxs-lookup"><span data-stu-id="b6fe9-190">
                    <strong>Included tasks</strong>
                </span></span></p>
            </td>
            <td width="45" valign="top">
                <p><span data-ttu-id="b6fe9-191">
                    <strong>包括时间</strong>
                </span><span class="sxs-lookup"><span data-stu-id="b6fe9-191">
                    <strong>Include Time</strong>
                </span></span></p>
            </td>
            <td width="46" valign="top">
                <p><span data-ttu-id="b6fe9-192">
                    <strong>包括支出</strong>
                </span><span class="sxs-lookup"><span data-stu-id="b6fe9-192">
                    <strong>Include Expense</strong>
                </span></span></p>
            </td>
            <td width="43" valign="top">
                <p><span data-ttu-id="b6fe9-193">
                    <strong>包括材料</strong>
                </span><span class="sxs-lookup"><span data-stu-id="b6fe9-193">
                    <strong>Include Material</strong>
                </span></span></p>
            </td>
            <td width="41" valign="top">
                <p><span data-ttu-id="b6fe9-194">
                    <strong>添加</strong>
                </span><span class="sxs-lookup"><span data-stu-id="b6fe9-194">
                    <strong>Include</strong>
                </span></span></p>
                <p><span data-ttu-id="b6fe9-195">
                    <strong>费用</strong>
                </span><span class="sxs-lookup"><span data-stu-id="b6fe9-195">
                    <strong>Fee</strong>
                </span></span></p>
            </td>
            <td width="49" valign="top">
                <p><span data-ttu-id="b6fe9-196">
                    <strong>有效/无效</strong>
                </span><span class="sxs-lookup"><span data-stu-id="b6fe9-196">
                    <strong>Valid/ Not valid</strong>
                </span></span></p>
            </td>
            <td width="200" valign="top">
                <p><span data-ttu-id="b6fe9-197">
                    <strong>原因</strong>
                </span><span class="sxs-lookup"><span data-stu-id="b6fe9-197">
                    <strong>Reason</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="b6fe9-198">O1</span><span class="sxs-lookup"><span data-stu-id="b6fe9-198">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="b6fe9-199">Q1</span><span class="sxs-lookup"><span data-stu-id="b6fe9-199">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="b6fe9-200">QL1</span><span class="sxs-lookup"><span data-stu-id="b6fe9-200">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="b6fe9-201">P1</span><span class="sxs-lookup"><span data-stu-id="b6fe9-201">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="b6fe9-202">空白</span><span class="sxs-lookup"><span data-stu-id="b6fe9-202">Blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="b6fe9-203">是</span><span class="sxs-lookup"><span data-stu-id="b6fe9-203">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="b6fe9-204">是</span><span class="sxs-lookup"><span data-stu-id="b6fe9-204">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="b6fe9-205">是</span><span class="sxs-lookup"><span data-stu-id="b6fe9-205">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="b6fe9-206">是</span><span class="sxs-lookup"><span data-stu-id="b6fe9-206">Yes</span></span> </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
<span data-ttu-id="b6fe9-207">无效</span><span class="sxs-lookup"><span data-stu-id="b6fe9-207">Not valid</span></span> </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
<span data-ttu-id="b6fe9-208">违反规则 #2。</span><span class="sxs-lookup"><span data-stu-id="b6fe9-208">Violation of Rule #2.</span></span> <span data-ttu-id="b6fe9-209">P1 项目的时间、支出和费用包含在报价单明细 QL1 和 QL2 中</span><span class="sxs-lookup"><span data-stu-id="b6fe9-209">Time, Expense, and Fees on P1 project are included on quote lines QL1 and QL2</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="b6fe9-210">O1</span><span class="sxs-lookup"><span data-stu-id="b6fe9-210">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="b6fe9-211">Q1</span><span class="sxs-lookup"><span data-stu-id="b6fe9-211">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="b6fe9-212">QL2</span><span class="sxs-lookup"><span data-stu-id="b6fe9-212">QL2</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="b6fe9-213">P1</span><span class="sxs-lookup"><span data-stu-id="b6fe9-213">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="b6fe9-214">空白</span><span class="sxs-lookup"><span data-stu-id="b6fe9-214">Blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="b6fe9-215">是</span><span class="sxs-lookup"><span data-stu-id="b6fe9-215">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="b6fe9-216">是</span><span class="sxs-lookup"><span data-stu-id="b6fe9-216">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="b6fe9-217">是</span><span class="sxs-lookup"><span data-stu-id="b6fe9-217">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="b6fe9-218">是</span><span class="sxs-lookup"><span data-stu-id="b6fe9-218">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
            </td>
            <td width="39" valign="top">
            </td>
            <td width="40" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="77" valign="top">
            </td>
            <td width="45" valign="top">
            </td>
            <td width="46" valign="top">
            </td>
            <td width="43" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="49" valign="top">
            </td>
            <td width="200" valign="top">
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="b6fe9-219">O1</span><span class="sxs-lookup"><span data-stu-id="b6fe9-219">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="b6fe9-220">Q1</span><span class="sxs-lookup"><span data-stu-id="b6fe9-220">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="b6fe9-221">QL1</span><span class="sxs-lookup"><span data-stu-id="b6fe9-221">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="b6fe9-222">P1</span><span class="sxs-lookup"><span data-stu-id="b6fe9-222">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="b6fe9-223">空白</span><span class="sxs-lookup"><span data-stu-id="b6fe9-223">Blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="b6fe9-224">是</span><span class="sxs-lookup"><span data-stu-id="b6fe9-224">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="b6fe9-225">No</span><span class="sxs-lookup"><span data-stu-id="b6fe9-225">No</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="b6fe9-226">是</span><span class="sxs-lookup"><span data-stu-id="b6fe9-226">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="b6fe9-227">是</span><span class="sxs-lookup"><span data-stu-id="b6fe9-227">Yes</span></span> </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
<span data-ttu-id="b6fe9-228">无效</span><span class="sxs-lookup"><span data-stu-id="b6fe9-228">Not valid</span></span> </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
<span data-ttu-id="b6fe9-229">违反规则 #2。</span><span class="sxs-lookup"><span data-stu-id="b6fe9-229">Violation of Rule #2.</span></span> <span data-ttu-id="b6fe9-230">P1 项目的时间、材料和费用包含在报价单明细 QL1 和 QL2 中</span><span class="sxs-lookup"><span data-stu-id="b6fe9-230">Time, Material, and Fees on P1 project are included on quote lines QL1 and QL2</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="b6fe9-231">O1</span><span class="sxs-lookup"><span data-stu-id="b6fe9-231">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="b6fe9-232">Q1</span><span class="sxs-lookup"><span data-stu-id="b6fe9-232">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="b6fe9-233">QL2</span><span class="sxs-lookup"><span data-stu-id="b6fe9-233">QL2</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="b6fe9-234">P1</span><span class="sxs-lookup"><span data-stu-id="b6fe9-234">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="b6fe9-235">空白</span><span class="sxs-lookup"><span data-stu-id="b6fe9-235">Blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="b6fe9-236">是</span><span class="sxs-lookup"><span data-stu-id="b6fe9-236">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="b6fe9-237">是</span><span class="sxs-lookup"><span data-stu-id="b6fe9-237">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="b6fe9-238">是</span><span class="sxs-lookup"><span data-stu-id="b6fe9-238">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="b6fe9-239">是</span><span class="sxs-lookup"><span data-stu-id="b6fe9-239">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
            </td>
            <td width="39" valign="top">
            </td>
            <td width="40" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="77" valign="top">
            </td>
            <td width="45" valign="top">
            </td>
            <td width="46" valign="top">
            </td>
            <td width="43" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="49" valign="top">
            </td>
            <td width="200" valign="top">
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="b6fe9-240">O1</span><span class="sxs-lookup"><span data-stu-id="b6fe9-240">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="b6fe9-241">Q1</span><span class="sxs-lookup"><span data-stu-id="b6fe9-241">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="b6fe9-242">QL1</span><span class="sxs-lookup"><span data-stu-id="b6fe9-242">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="b6fe9-243">P1</span><span class="sxs-lookup"><span data-stu-id="b6fe9-243">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="b6fe9-244">空白</span><span class="sxs-lookup"><span data-stu-id="b6fe9-244">Blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="b6fe9-245">是</span><span class="sxs-lookup"><span data-stu-id="b6fe9-245">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="b6fe9-246">No</span><span class="sxs-lookup"><span data-stu-id="b6fe9-246">No</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="b6fe9-247">是</span><span class="sxs-lookup"><span data-stu-id="b6fe9-247">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="b6fe9-248">是</span><span class="sxs-lookup"><span data-stu-id="b6fe9-248">Yes</span></span> </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
<span data-ttu-id="b6fe9-249">有效</span><span class="sxs-lookup"><span data-stu-id="b6fe9-249">Valid</span></span> </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
<span data-ttu-id="b6fe9-250">P1 项目的时间、材料和费用包含在 QL1 中</span><span class="sxs-lookup"><span data-stu-id="b6fe9-250">Time, Material, and Fees on P1 project are included on QL1</span></span> <br>
<span data-ttu-id="b6fe9-251">P1 项目的支出包含在 QL2 中</span><span class="sxs-lookup"><span data-stu-id="b6fe9-251">Expense on P1 project is included on QL2</span></span> <br>
<span data-ttu-id="b6fe9-252">每个报价单明细中包含的内容均无重叠，因此有效。</span><span class="sxs-lookup"><span data-stu-id="b6fe9-252">No overlap in what is being included on each quote line and therefore valid.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="b6fe9-253">O1</span><span class="sxs-lookup"><span data-stu-id="b6fe9-253">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="b6fe9-254">Q1</span><span class="sxs-lookup"><span data-stu-id="b6fe9-254">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="b6fe9-255">QL2</span><span class="sxs-lookup"><span data-stu-id="b6fe9-255">QL2</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="b6fe9-256">P1</span><span class="sxs-lookup"><span data-stu-id="b6fe9-256">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="b6fe9-257">空白</span><span class="sxs-lookup"><span data-stu-id="b6fe9-257">Blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="b6fe9-258">No</span><span class="sxs-lookup"><span data-stu-id="b6fe9-258">No</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="b6fe9-259">是</span><span class="sxs-lookup"><span data-stu-id="b6fe9-259">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="b6fe9-260">No</span><span class="sxs-lookup"><span data-stu-id="b6fe9-260">No</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="b6fe9-261">No</span><span class="sxs-lookup"><span data-stu-id="b6fe9-261">No</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
            </td>
            <td width="39" valign="top">
            </td>
            <td width="40" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="77" valign="top">
            </td>
            <td width="45" valign="top">
            </td>
            <td width="46" valign="top">
            </td>
            <td width="43" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="49" valign="top">
            </td>
            <td width="200" valign="top">
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="b6fe9-262">O1</span><span class="sxs-lookup"><span data-stu-id="b6fe9-262">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="b6fe9-263">Q1</span><span class="sxs-lookup"><span data-stu-id="b6fe9-263">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="b6fe9-264">QL1</span><span class="sxs-lookup"><span data-stu-id="b6fe9-264">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="b6fe9-265">P1</span><span class="sxs-lookup"><span data-stu-id="b6fe9-265">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="b6fe9-266">仅所选任务</span><span class="sxs-lookup"><span data-stu-id="b6fe9-266">Selected tasks only</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="b6fe9-267">是</span><span class="sxs-lookup"><span data-stu-id="b6fe9-267">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="b6fe9-268">是</span><span class="sxs-lookup"><span data-stu-id="b6fe9-268">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="b6fe9-269">是</span><span class="sxs-lookup"><span data-stu-id="b6fe9-269">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="b6fe9-270">是</span><span class="sxs-lookup"><span data-stu-id="b6fe9-270">Yes</span></span> </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
<span data-ttu-id="b6fe9-271">无效</span><span class="sxs-lookup"><span data-stu-id="b6fe9-271">Not valid</span></span> </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
<span data-ttu-id="b6fe9-272">违反规则 #2</span><span class="sxs-lookup"><span data-stu-id="b6fe9-272">Violation of Rule #2</span></span> </p>
                <p>
<span data-ttu-id="b6fe9-273">Q1 包括项目 P1 中任务子集的时间、材料、支出和费用</span><span class="sxs-lookup"><span data-stu-id="b6fe9-273">Q1 includes Time, Material, Expenses and Fees on a subset of tasks on project P1</span></span> </p>
                <p>
<span data-ttu-id="b6fe9-274">QL2 包含整个项目 P1 的时间、支出和费用，因此与 Q1 中包含的内容重叠。</span><span class="sxs-lookup"><span data-stu-id="b6fe9-274">QL2 includes Time, Expenses, and Fees for the whole project P1 and therefore overlaps with what is included on Q1.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="b6fe9-275">O1</span><span class="sxs-lookup"><span data-stu-id="b6fe9-275">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="b6fe9-276">Q1</span><span class="sxs-lookup"><span data-stu-id="b6fe9-276">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="b6fe9-277">QL2</span><span class="sxs-lookup"><span data-stu-id="b6fe9-277">QL2</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="b6fe9-278">P1</span><span class="sxs-lookup"><span data-stu-id="b6fe9-278">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="b6fe9-279">空白</span><span class="sxs-lookup"><span data-stu-id="b6fe9-279">Blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="b6fe9-280">是</span><span class="sxs-lookup"><span data-stu-id="b6fe9-280">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="b6fe9-281">是</span><span class="sxs-lookup"><span data-stu-id="b6fe9-281">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="b6fe9-282">是</span><span class="sxs-lookup"><span data-stu-id="b6fe9-282">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="b6fe9-283">是</span><span class="sxs-lookup"><span data-stu-id="b6fe9-283">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
            </td>
            <td width="39" valign="top">
            </td>
            <td width="40" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="77" valign="top">
            </td>
            <td width="45" valign="top">
            </td>
            <td width="46" valign="top">
            </td>
            <td width="43" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="49" valign="top">
            </td>
            <td width="200" valign="top">
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="b6fe9-284">O1</span><span class="sxs-lookup"><span data-stu-id="b6fe9-284">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="b6fe9-285">Q1</span><span class="sxs-lookup"><span data-stu-id="b6fe9-285">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="b6fe9-286">QL1</span><span class="sxs-lookup"><span data-stu-id="b6fe9-286">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="b6fe9-287">P1</span><span class="sxs-lookup"><span data-stu-id="b6fe9-287">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="b6fe9-288">仅所选任务</span><span class="sxs-lookup"><span data-stu-id="b6fe9-288">Selected tasks only</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="b6fe9-289">是</span><span class="sxs-lookup"><span data-stu-id="b6fe9-289">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="b6fe9-290">是</span><span class="sxs-lookup"><span data-stu-id="b6fe9-290">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="b6fe9-291">是</span><span class="sxs-lookup"><span data-stu-id="b6fe9-291">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="b6fe9-292">是</span><span class="sxs-lookup"><span data-stu-id="b6fe9-292">Yes</span></span> </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
<span data-ttu-id="b6fe9-293">有效</span><span class="sxs-lookup"><span data-stu-id="b6fe9-293">Valid</span></span> </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
<span data-ttu-id="b6fe9-294">根据规则 #3，</span><span class="sxs-lookup"><span data-stu-id="b6fe9-294">Per Rule #3,</span></span> </p>
                <p>
<span data-ttu-id="b6fe9-295">Q1 包括项目 P1 中任务子集的时间、材料、支出和费用。</span><span class="sxs-lookup"><span data-stu-id="b6fe9-295">Q1 includes Time, Material, Expenses, and Fees on a subset of tasks on project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="b6fe9-296">QL2 包括项目 P1 中任务子集的时间、材料、支出和费用。</span><span class="sxs-lookup"><span data-stu-id="b6fe9-296">QL2 includes Time, Material, Expenses, and Fees for a subset of tasks on project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="b6fe9-297">唯一的额外验证是验证 QL1 上的任务子集是否与 QL2 上的任务子集不同，以确保没有重叠。</span><span class="sxs-lookup"><span data-stu-id="b6fe9-297">The only additional validation is around the subset of tasks on QL1 which is different from the subset of tasks on QL2 to ensure that there is no overlap.</span></span> <span data-ttu-id="b6fe9-298">当任务关联时，这由系统完成。</span><span class="sxs-lookup"><span data-stu-id="b6fe9-298">This is done by the system when tasks are associated.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="b6fe9-299">O1</span><span class="sxs-lookup"><span data-stu-id="b6fe9-299">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="b6fe9-300">Q1</span><span class="sxs-lookup"><span data-stu-id="b6fe9-300">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="b6fe9-301">QL2</span><span class="sxs-lookup"><span data-stu-id="b6fe9-301">QL2</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="b6fe9-302">P1</span><span class="sxs-lookup"><span data-stu-id="b6fe9-302">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="b6fe9-303">仅所选任务</span><span class="sxs-lookup"><span data-stu-id="b6fe9-303">Selected tasks only</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="b6fe9-304">是</span><span class="sxs-lookup"><span data-stu-id="b6fe9-304">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="b6fe9-305">是</span><span class="sxs-lookup"><span data-stu-id="b6fe9-305">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="b6fe9-306">是</span><span class="sxs-lookup"><span data-stu-id="b6fe9-306">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="b6fe9-307">是</span><span class="sxs-lookup"><span data-stu-id="b6fe9-307">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
            </td>
            <td width="39" valign="top">
            </td>
            <td width="40" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="77" valign="top">
            </td>
            <td width="45" valign="top">
            </td>
            <td width="46" valign="top">
            </td>
            <td width="43" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="49" valign="top">
            </td>
            <td width="200" valign="top">
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="b6fe9-308">O1</span><span class="sxs-lookup"><span data-stu-id="b6fe9-308">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="b6fe9-309">Q1</span><span class="sxs-lookup"><span data-stu-id="b6fe9-309">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="b6fe9-310">QL1</span><span class="sxs-lookup"><span data-stu-id="b6fe9-310">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="b6fe9-311">P1</span><span class="sxs-lookup"><span data-stu-id="b6fe9-311">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="b6fe9-312">所有项目任务或空白</span><span class="sxs-lookup"><span data-stu-id="b6fe9-312">All project tasks or blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="b6fe9-313">是</span><span class="sxs-lookup"><span data-stu-id="b6fe9-313">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="b6fe9-314">是</span><span class="sxs-lookup"><span data-stu-id="b6fe9-314">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="b6fe9-315">是</span><span class="sxs-lookup"><span data-stu-id="b6fe9-315">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="b6fe9-316">是</span><span class="sxs-lookup"><span data-stu-id="b6fe9-316">Yes</span></span> </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
<span data-ttu-id="b6fe9-317">有效</span><span class="sxs-lookup"><span data-stu-id="b6fe9-317">Valid</span></span> </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
<span data-ttu-id="b6fe9-318">按照规则 #5，Q1 和 Q2 是相同商机的两个报价单，因此可以对项目的相同组件对其进行估算。</span><span class="sxs-lookup"><span data-stu-id="b6fe9-318">Per Rule #5, Q1 and Q2 are two quotes on the same opportunity, so they can both estimate for the same components of a project.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="b6fe9-319">O1</span><span class="sxs-lookup"><span data-stu-id="b6fe9-319">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="b6fe9-320">Q2</span><span class="sxs-lookup"><span data-stu-id="b6fe9-320">Q2</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="b6fe9-321">QL1</span><span class="sxs-lookup"><span data-stu-id="b6fe9-321">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="b6fe9-322">P1</span><span class="sxs-lookup"><span data-stu-id="b6fe9-322">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="b6fe9-323">所有项目任务或空白</span><span class="sxs-lookup"><span data-stu-id="b6fe9-323">All project tasks or blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="b6fe9-324">是</span><span class="sxs-lookup"><span data-stu-id="b6fe9-324">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="b6fe9-325">是</span><span class="sxs-lookup"><span data-stu-id="b6fe9-325">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="b6fe9-326">是</span><span class="sxs-lookup"><span data-stu-id="b6fe9-326">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="b6fe9-327">是</span><span class="sxs-lookup"><span data-stu-id="b6fe9-327">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
            </td>
            <td width="39" valign="top">
            </td>
            <td width="40" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="77" valign="top">
            </td>
            <td width="45" valign="top">
            </td>
            <td width="46" valign="top">
            </td>
            <td width="43" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="49" valign="top">
            </td>
            <td width="200" valign="top">
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="b6fe9-328">O1</span><span class="sxs-lookup"><span data-stu-id="b6fe9-328">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="b6fe9-329">Q1</span><span class="sxs-lookup"><span data-stu-id="b6fe9-329">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="b6fe9-330">QL1</span><span class="sxs-lookup"><span data-stu-id="b6fe9-330">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="b6fe9-331">P1</span><span class="sxs-lookup"><span data-stu-id="b6fe9-331">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="b6fe9-332">所有项目任务或空白</span><span class="sxs-lookup"><span data-stu-id="b6fe9-332">All project tasks or blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="b6fe9-333">是</span><span class="sxs-lookup"><span data-stu-id="b6fe9-333">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="b6fe9-334">是</span><span class="sxs-lookup"><span data-stu-id="b6fe9-334">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="b6fe9-335">是</span><span class="sxs-lookup"><span data-stu-id="b6fe9-335">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="b6fe9-336">是</span><span class="sxs-lookup"><span data-stu-id="b6fe9-336">Yes</span></span> </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
<span data-ttu-id="b6fe9-337">无效</span><span class="sxs-lookup"><span data-stu-id="b6fe9-337">Not Valid</span></span> </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
<span data-ttu-id="b6fe9-338">按照规则 #4，Q1 和 Q2 是不同商机的两个报价单，因此不能对相同项目的相同组件对其进行估算。</span><span class="sxs-lookup"><span data-stu-id="b6fe9-338">Per Rule #4, Q1 and Q2 are two quotes on different opportunities, so they can't estimate for the same components of same project.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="b6fe9-339">O2</span><span class="sxs-lookup"><span data-stu-id="b6fe9-339">O2</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="b6fe9-340">Q1</span><span class="sxs-lookup"><span data-stu-id="b6fe9-340">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="b6fe9-341">QL1</span><span class="sxs-lookup"><span data-stu-id="b6fe9-341">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="b6fe9-342">P1</span><span class="sxs-lookup"><span data-stu-id="b6fe9-342">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="b6fe9-343">所有项目任务或空白</span><span class="sxs-lookup"><span data-stu-id="b6fe9-343">All project tasks or blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="b6fe9-344">是</span><span class="sxs-lookup"><span data-stu-id="b6fe9-344">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="b6fe9-345">是</span><span class="sxs-lookup"><span data-stu-id="b6fe9-345">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="b6fe9-346">是</span><span class="sxs-lookup"><span data-stu-id="b6fe9-346">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="b6fe9-347">是</span><span class="sxs-lookup"><span data-stu-id="b6fe9-347">Yes</span></span> </p>
            </td>
        </tr>
    </tbody>
</table>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
