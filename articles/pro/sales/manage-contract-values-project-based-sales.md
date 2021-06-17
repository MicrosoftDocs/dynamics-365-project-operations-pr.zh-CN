---
title: 基于项目的合同子项概述
description: 此主题提供有关处理基于项目的合同子项的信息。
author: rumant
ms.date: 10/28/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 8af32b0475650db9c5862ea23d185588a631ade6
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/10/2021
ms.locfileid: "6003125"
---
# <a name="project-based-contract-lines-overview"></a><span data-ttu-id="d77d9-103">基于项目的合同子项概述</span><span class="sxs-lookup"><span data-stu-id="d77d9-103">Project-based contract lines overview</span></span>

<span data-ttu-id="d77d9-104">_**适用于：** 基于资源/非库存场景的 Project Operations，精简部署 - 估价开票交易_</span><span class="sxs-lookup"><span data-stu-id="d77d9-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="d77d9-105">Dynamics 365 Project Operations 中的基于项目的合同子项用于保留参与项目中项目工作特定组成部分的估算和计费协议。</span><span class="sxs-lookup"><span data-stu-id="d77d9-105">Project-based contract lines in Dynamics 365 Project Operations are designed to hold the estimate and billing agreements for specific components of project work on an engagement.</span></span> <span data-ttu-id="d77d9-106">基于项目的合同子项的结构已针对存在以下概念的项目估算和计费方案扩展：</span><span class="sxs-lookup"><span data-stu-id="d77d9-106">The structure of a project–based contract line is extended for project estimates and billing scenarios with the following concepts:</span></span>

- <span data-ttu-id="d77d9-107">计费方法</span><span class="sxs-lookup"><span data-stu-id="d77d9-107">Billing method</span></span>
- <span data-ttu-id="d77d9-108">项目和任务映射</span><span class="sxs-lookup"><span data-stu-id="d77d9-108">Project and task mapping</span></span>
- <span data-ttu-id="d77d9-109">包括的交易类</span><span class="sxs-lookup"><span data-stu-id="d77d9-109">Included transaction classes</span></span>
- <span data-ttu-id="d77d9-110">上限</span><span class="sxs-lookup"><span data-stu-id="d77d9-110">Not-to-exceed limit</span></span>
- <span data-ttu-id="d77d9-111">应计费设置</span><span class="sxs-lookup"><span data-stu-id="d77d9-111">Chargeability setup</span></span>
- <span data-ttu-id="d77d9-112">使用合同子项详细信息估算</span><span class="sxs-lookup"><span data-stu-id="d77d9-112">Estimates using contract line details</span></span>
- <span data-ttu-id="d77d9-113">合同子项客户</span><span class="sxs-lookup"><span data-stu-id="d77d9-113">Contract line customers</span></span>

<span data-ttu-id="d77d9-114">下表包括基于项目的合同子项的 **常规** 选项卡上的字段，这些字段帮助为基于项目的工作设定详细的基础估算和计费安排的基础。</span><span class="sxs-lookup"><span data-stu-id="d77d9-114">The following table includes the fields on the **General** tab of project–based contract lines that help set up the basis for a detailed, ground–up estimate and billing arrangements for project–based work.</span></span>

| <span data-ttu-id="d77d9-115">字段</span><span class="sxs-lookup"><span data-stu-id="d77d9-115">Field</span></span> | <span data-ttu-id="d77d9-116">描述</span><span class="sxs-lookup"><span data-stu-id="d77d9-116">Description</span></span> | <span data-ttu-id="d77d9-117">下游影响</span><span class="sxs-lookup"><span data-stu-id="d77d9-117">Downstream impact</span></span> |
| --- | --- | --- |
| <span data-ttu-id="d77d9-118">**客户**</span><span class="sxs-lookup"><span data-stu-id="d77d9-118">**Name**</span></span> | <span data-ttu-id="d77d9-119">合同子项的名称。</span><span class="sxs-lookup"><span data-stu-id="d77d9-119">Name of the contract line.</span></span> <span data-ttu-id="d77d9-120">标识正在估算的合同的独立部分。</span><span class="sxs-lookup"><span data-stu-id="d77d9-120">This identifies the discrete component of the contract that is being estimated.</span></span> <span data-ttu-id="d77d9-121">对于从报价单创建的项目合同，从基于项目的报价单明细的相应值复制此值。</span><span class="sxs-lookup"><span data-stu-id="d77d9-121">For a project contract created from a quote, this value is copied from a corresponding value of the project-based quote line.</span></span> | <span data-ttu-id="d77d9-122">创建发票时复制到从此合同子项创建的项目发票明细的名称。</span><span class="sxs-lookup"><span data-stu-id="d77d9-122">The name copied over to the project invoice line that is created from this contract line when the invoice is created.</span></span> |
| <span data-ttu-id="d77d9-123">**记帐方法**</span><span class="sxs-lookup"><span data-stu-id="d77d9-123">**Billing Method**</span></span> | <span data-ttu-id="d77d9-124">在从报价单创建的项目合同上，从报价单明细上的相应字段复制此值。</span><span class="sxs-lookup"><span data-stu-id="d77d9-124">On a project contract created from a quote, this value is copied from the corresponding field on the quote line.</span></span> <span data-ttu-id="d77d9-125">这是一个选项集，代表 Project Operations 支持的两个主要合同签订模型：</span><span class="sxs-lookup"><span data-stu-id="d77d9-125">This is an option set that represents the two main contracting models supported by Project Operations:</span></span></br><span data-ttu-id="d77d9-126">- **固定价格**</span><span class="sxs-lookup"><span data-stu-id="d77d9-126">- **Fixed Price**</span></span></br><span data-ttu-id="d77d9-127">- **时间和材料**</span><span class="sxs-lookup"><span data-stu-id="d77d9-127">- **Time and Material**</span></span> | <span data-ttu-id="d77d9-128">根据引用的合同子项的计费方法，将处理实际交易。</span><span class="sxs-lookup"><span data-stu-id="d77d9-128">Based on the billing method of the referenced contract line, the actual transaction will be processed.</span></span> <span data-ttu-id="d77d9-129">如果实际值引用的合同子项具有时间和材料计费方法，将创建成本和未记帐实际销售额记录。</span><span class="sxs-lookup"><span data-stu-id="d77d9-129">If the contract line referenced by the actual has a time and material billing method, cost and unbilled sales actual records are created.</span></span> <span data-ttu-id="d77d9-130">如果实际值引用的合同子项具有固定价格计费方法，将仅创建成本实际值。</span><span class="sxs-lookup"><span data-stu-id="d77d9-130">If the contract line referenced by the actual has a fixed price billing method, only a cost actual is created.</span></span> |
| <span data-ttu-id="d77d9-131">**Project**</span><span class="sxs-lookup"><span data-stu-id="d77d9-131">**Project**</span></span> | <span data-ttu-id="d77d9-132">使用此字段来标识将用于交付此参与项目中的工作的项目。</span><span class="sxs-lookup"><span data-stu-id="d77d9-132">Use this field to identify the project that will be used to deliver the work on this engagement.</span></span> | <span data-ttu-id="d77d9-133">该值将与 **包含的任务** 和 **包含的交易分类** 结合使用，以解析实际或估计行记录中的合同子项参考。</span><span class="sxs-lookup"><span data-stu-id="d77d9-133">This value will be used in conjunction with **Included Tasks** and **Included Transaction Classes** to resolve the contract line reference on an actual or estimate line record.</span></span> |
| <span data-ttu-id="d77d9-134">**包含的任务**</span><span class="sxs-lookup"><span data-stu-id="d77d9-134">**Included Tasks**</span></span> | <span data-ttu-id="d77d9-135">指示此合同子项是包含所选项目的所有项目任务，还是只包含部分任务。</span><span class="sxs-lookup"><span data-stu-id="d77d9-135">Indicates if this contract line includes all project tasks for the selected project or only a subset of the tasks.</span></span> <span data-ttu-id="d77d9-136">这是具有以下可能值的选项集：</span><span class="sxs-lookup"><span data-stu-id="d77d9-136">This is an option set that has the following possible values:</span></span></br><span data-ttu-id="d77d9-137">- **所有项目任务**</span><span class="sxs-lookup"><span data-stu-id="d77d9-137">- **All Project Tasks**</span></span></br><span data-ttu-id="d77d9-138">- **仅所选项目任务**。</span><span class="sxs-lookup"><span data-stu-id="d77d9-138">- **Selected Project Tasks Only**.</span></span> <span data-ttu-id="d77d9-139">此字段中的空值等同于选择 **所有项目任务**。</span><span class="sxs-lookup"><span data-stu-id="d77d9-139">A blank value in this field is equal to selecting **All Project Tasks**.</span></span> | <span data-ttu-id="d77d9-140">如果选择 **仅所选任务**，则可以在 **项目** 页面上的 **任务计费设置** 选项卡上选择特定任务并将其与此合同子项关联。</span><span class="sxs-lookup"><span data-stu-id="d77d9-140">If **Selected Tasks Only** is selected, you can select specific tasks and associate them to this contract line on the **Task Billing Setup** tab on the **Project** page.</span></span> <span data-ttu-id="d77d9-141">此值将与 **项目** 和 **包含的交易** 类结合使用，来解析实际或估算明细记录中的合同子项引用。</span><span class="sxs-lookup"><span data-stu-id="d77d9-141">The value will be used in conjunction with **Project** and **Included Transaction** classes to resolve the contract line reference on an actual or an estimate line record.</span></span> |
| <span data-ttu-id="d77d9-142">**包括时间**</span><span class="sxs-lookup"><span data-stu-id="d77d9-142">**Include Time**</span></span> | <span data-ttu-id="d77d9-143">**是**/**否** 值指明所选项目的时间交易或人工成本是否将包含在此合同子项中。</span><span class="sxs-lookup"><span data-stu-id="d77d9-143">A **Yes**/**No** value indicates if time transactions or labor costs on the selected project will be included on this contract line.</span></span> <span data-ttu-id="d77d9-144">**否** 值指示时间交易或人工成本将不包括在此合同子项中。</span><span class="sxs-lookup"><span data-stu-id="d77d9-144">A **No** value indicates that the time transactions or labor cost will not be included on this contract line.</span></span> <span data-ttu-id="d77d9-145">**是** 值指示包括。</span><span class="sxs-lookup"><span data-stu-id="d77d9-145">A **Yes** value indicates that they will.</span></span> | <span data-ttu-id="d77d9-146">该值与项目一起使用，以解析实际或估算行记录中的合同子项参考。</span><span class="sxs-lookup"><span data-stu-id="d77d9-146">This value is used in conjunction with the project to resolve the contract line reference on an actual or an estimate line record.</span></span> |
| <span data-ttu-id="d77d9-147">**包括支出**</span><span class="sxs-lookup"><span data-stu-id="d77d9-147">**Include Expense**</span></span> | <span data-ttu-id="d77d9-148">**是**/**否** 值指明所选项目的支出成本是否将包含在此合同子项中。</span><span class="sxs-lookup"><span data-stu-id="d77d9-148">A **Yes**/**No** value indicates if expense costs on the selected project will be included on this contract line.</span></span> <span data-ttu-id="d77d9-149">**否** 值指示支出成本将不包括在此合同子项中。</span><span class="sxs-lookup"><span data-stu-id="d77d9-149">A **No** value indicates that the expense cost will not be included on this contract line.</span></span> <span data-ttu-id="d77d9-150">**是** 值指示包括。</span><span class="sxs-lookup"><span data-stu-id="d77d9-150">A **Yes** value indicates that it will.</span></span> | <span data-ttu-id="d77d9-151">该值与项目一起使用，以解析实际或估算行记录中的合同子项参考。</span><span class="sxs-lookup"><span data-stu-id="d77d9-151">This value is used in conjunction with the project to resolve the contract line reference on an actual or an estimate line record.</span></span> |
| <span data-ttu-id="d77d9-152">**包括材料**</span><span class="sxs-lookup"><span data-stu-id="d77d9-152">**Include Materials**</span></span> | <span data-ttu-id="d77d9-153">**是**/**否** 值指明所选项目的材料成本是否将包含在此合同子项中。</span><span class="sxs-lookup"><span data-stu-id="d77d9-153">A **Yes**/**No** value indicates if material costs on the selected project will be included on this contract line.</span></span> <span data-ttu-id="d77d9-154">**否** 值指明材料成本将不包含在此合同子项中。</span><span class="sxs-lookup"><span data-stu-id="d77d9-154">A **No** value indicates that the material costs will not be included on this contract line.</span></span> <span data-ttu-id="d77d9-155">**是** 值指示包括。</span><span class="sxs-lookup"><span data-stu-id="d77d9-155">A **Yes** value indicates that it will.</span></span> | <span data-ttu-id="d77d9-156">该值与项目一起使用，以解析实际或估算行记录中的合同子项参考。</span><span class="sxs-lookup"><span data-stu-id="d77d9-156">This value is used in conjunction with the project to resolve the contract line reference on an actual or an estimate line record.</span></span> |
| <span data-ttu-id="d77d9-157">**包括费用**</span><span class="sxs-lookup"><span data-stu-id="d77d9-157">**Include Fee**</span></span> | <span data-ttu-id="d77d9-158">**是**/**否** 值指明所选项目的费用是否将包含在此合同子项中。</span><span class="sxs-lookup"><span data-stu-id="d77d9-158">A **Yes**/**No** value indicates if fees on the selected project will be included on this contract line.</span></span> <span data-ttu-id="d77d9-159">**否** 值指示费用将不包括在此合同子项中。</span><span class="sxs-lookup"><span data-stu-id="d77d9-159">A **No** value indicates that the fees will not be included on this contract line.</span></span> <span data-ttu-id="d77d9-160">**是** 值指示包括。</span><span class="sxs-lookup"><span data-stu-id="d77d9-160">A **Yes** value indicates that they will.</span></span> | <span data-ttu-id="d77d9-161">该值与项目一起使用，以解析实际或估算行记录中的合同子项参考。</span><span class="sxs-lookup"><span data-stu-id="d77d9-161">This value is used in conjunction with the project to resolve the contract line reference on an actual or an estimate line record.</span></span> |
| <span data-ttu-id="d77d9-162">**合同金额**</span><span class="sxs-lookup"><span data-stu-id="d77d9-162">**Contracted Amount**</span></span> | <span data-ttu-id="d77d9-163">在固定价格合同子项上，此金额是将为与此合同子项关联的所有工作组成部分向客户开票的商定值。</span><span class="sxs-lookup"><span data-stu-id="d77d9-163">On a fixed price contract line, this amount is the agreed-on value that will be invoiced to the customer for all the work components associated to this contract line.</span></span> <span data-ttu-id="d77d9-164">在时间和材料合同子项上，此金额是将为与此合同子项关联的所有工作组成部分向客户开票的估计值。</span><span class="sxs-lookup"><span data-stu-id="d77d9-164">On a time and material contract line, this amount is an estimated value of what will be invoiced to the customer for all the work components associated to this contract line.</span></span> <span data-ttu-id="d77d9-165">在从报价单创建的项目合同上，从报价单明细上的相应字段复制此值。</span><span class="sxs-lookup"><span data-stu-id="d77d9-165">On a project contract that is created from a quote, this value is copied from the corresponding field on the quote line.</span></span> <span data-ttu-id="d77d9-166">当基于项目的合同子项具有明细详细信息时，此字段将被锁定以进行编辑，值从合同子项详细信息中的金额汇总得出。</span><span class="sxs-lookup"><span data-stu-id="d77d9-166">When a project–based contract line has line details, this field is locked for editing and is summarized from the amount on the contract line details.</span></span> | <span data-ttu-id="d77d9-167">当合同子项具有明细详细信息时，可以通过更改明细详细信息中的金额来修改此值。</span><span class="sxs-lookup"><span data-stu-id="d77d9-167">When the contract line has line details, this value can be modified by changing the amounts on the line details.</span></span> <span data-ttu-id="d77d9-168">在固定价格合同子项中，此值用于生成定期计费里程碑上的税前金额。</span><span class="sxs-lookup"><span data-stu-id="d77d9-168">On a fixed price contract line, this value is used to generate the amount before tax on periodic billing milestones.</span></span> |
| <span data-ttu-id="d77d9-169">**预计税款**</span><span class="sxs-lookup"><span data-stu-id="d77d9-169">**Estimated Tax**</span></span> | <span data-ttu-id="d77d9-170">用户可以编辑此字段来在合同子项上输入估算税额。</span><span class="sxs-lookup"><span data-stu-id="d77d9-170">The user can edit this field to input the estimated tax amount on the contract line.</span></span> <span data-ttu-id="d77d9-171">当基于项目的合同子项具有明细详细信息时，此字段将被锁定以进行编辑，值从合同子项详细信息中的税额汇总得出。</span><span class="sxs-lookup"><span data-stu-id="d77d9-171">When a project–based contract line has line details, this field is locked for editing and is summarized from the tax amount on the contract line details.</span></span> | <span data-ttu-id="d77d9-172">当合同子项具有明细详细信息时，可以通过更改明细详细信息中的税额来修改此值。</span><span class="sxs-lookup"><span data-stu-id="d77d9-172">When the contract line has line details, this value can be modified by changing the tax amounts on the line details.</span></span> <span data-ttu-id="d77d9-173">在固定价格合同子项中，此值用于生成定期计费里程碑上的税款。</span><span class="sxs-lookup"><span data-stu-id="d77d9-173">On a fixed price contract line, this value is used to generate the tax on periodic billing milestones.</span></span> |
| <span data-ttu-id="d77d9-174">**税后合同金额**</span><span class="sxs-lookup"><span data-stu-id="d77d9-174">**Contracted Amount after Tax**</span></span> | <span data-ttu-id="d77d9-175">税后合同子项金额。</span><span class="sxs-lookup"><span data-stu-id="d77d9-175">The contract line amount after tax.</span></span> <span data-ttu-id="d77d9-176">此字段为只读字段，计算公式为 **合同金额 + 税款**。</span><span class="sxs-lookup"><span data-stu-id="d77d9-176">This field is read only and is calculated as **Contracted Amount + Tax**.</span></span> | <span data-ttu-id="d77d9-177">在固定价格合同子项中，此值用于生成定期计费里程碑。</span><span class="sxs-lookup"><span data-stu-id="d77d9-177">On a fixed price contract line, this value is used to generate periodic billing milestones.</span></span> |
| <span data-ttu-id="d77d9-178">**上限**</span><span class="sxs-lookup"><span data-stu-id="d77d9-178">**Not-to-Exceed Limit**</span></span> | <span data-ttu-id="d77d9-179">用户可以编辑此字段，它仅在将计费方法设置为时间和材料的基于项目的合同子项上可用。</span><span class="sxs-lookup"><span data-stu-id="d77d9-179">The user can edit this field and it is only available on project-based contract lines that have the billing method set as time and material.</span></span> | <span data-ttu-id="d77d9-180">用户可以编辑此字段。</span><span class="sxs-lookup"><span data-stu-id="d77d9-180">The user can edit this field.</span></span> <span data-ttu-id="d77d9-181">当时间和材料的实际值引用此合同子项以获取时间和材料值时，实际值中的金额将根据合同子项中的上限计算。</span><span class="sxs-lookup"><span data-stu-id="d77d9-181">When an actual for time and material references this contract line for time and material, the amount on the actual is evaluated against the not-to-exceed limit on the contract line.</span></span> <span data-ttu-id="d77d9-182">此计算在计入已花费和提交的金额后完成。</span><span class="sxs-lookup"><span data-stu-id="d77d9-182">This evaluation is completed after  the already spent and committed amounts are accounted for.</span></span> |
| <span data-ttu-id="d77d9-183">**客户预算**</span><span class="sxs-lookup"><span data-stu-id="d77d9-183">**Customer Budget**</span></span> | <span data-ttu-id="d77d9-184">如果合同是从报价单创建的，此字段可以编辑，值从报价单明细上的相应字段复制。</span><span class="sxs-lookup"><span data-stu-id="d77d9-184">This field is editable and is copied from the corresponding field on the quote line if the contract was created from a quote.</span></span> | <span data-ttu-id="d77d9-185">此字段仅用于提供信息，对下游没有任何意义。</span><span class="sxs-lookup"><span data-stu-id="d77d9-185">This field is only used for information and does not have any downstream significance.</span></span> |

## <a name="validation-rules-for-the-options-on-the-general-tab-of-project-based-contract-lines"></a><span data-ttu-id="d77d9-186">基于项目的合同子项的“常规”选项卡上选项的验证规则</span><span class="sxs-lookup"><span data-stu-id="d77d9-186">Validation rules for the options on the General tab of project-based contract lines</span></span>

<span data-ttu-id="d77d9-187">规则 1：如果 **包含的任务** 字段为空或设置为 **所有项目任务**，项目的所有任务都将包含在合同子项中。</span><span class="sxs-lookup"><span data-stu-id="d77d9-187">Rule 1: If the **Included Tasks** field is blank or set to **All Project Tasks**, all tasks of the project are included on the contract line.</span></span>

<span data-ttu-id="d77d9-188">规则 2：当 **包含的任务** 字段为空或明确设置为 **所有项目任务** 时，项目和特定交易类只能包含在合同的一个基于项目的合同子项中。</span><span class="sxs-lookup"><span data-stu-id="d77d9-188">Rule 2: When the **Included Tasks** field is blank or explicitly set to **All Project Tasks**, a project and a certain transaction class can only be included on one project-based contract line of a contract.</span></span>

<span data-ttu-id="d77d9-189">规则 3：当 **包含的任务** 字段设置为 **仅所选项目任务** 时，项目和特定交易类可以包含在合同的多个基于项目的合同子项中。</span><span class="sxs-lookup"><span data-stu-id="d77d9-189">Rule 3: When the **Included Tasks** field is set to **Selected Project Tasks Only**, a project and a certain transaction class can be included on multiple project-based contract lines of a contract.</span></span>

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="43" valign="top">
                <p><span data-ttu-id="d77d9-190">
                    <strong>合同</strong>
                </span><span class="sxs-lookup"><span data-stu-id="d77d9-190">
                    <strong>Contract</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="d77d9-191">
                    <strong>合同子项</strong>
                </span><span class="sxs-lookup"><span data-stu-id="d77d9-191">
                    <strong>Contract line</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="d77d9-192">
                    <strong>Project</strong>
                </span><span class="sxs-lookup"><span data-stu-id="d77d9-192">
                    <strong>Project</strong>
                </span></span></p>
            </td>
            <td width="67" valign="top">
                <p><span data-ttu-id="d77d9-193">
                    <strong>包含的任务</strong>
                </span><span class="sxs-lookup"><span data-stu-id="d77d9-193">
                    <strong>Included tasks</strong>
                </span></span></p>
            </td>
            <td width="48" valign="top">
                <p><span data-ttu-id="d77d9-194">
                    <strong>包括时间</strong>
                </span><span class="sxs-lookup"><span data-stu-id="d77d9-194">
                    <strong>Include Time</strong>
                </span></span></p>
            </td>
            <td width="48" valign="top">
                <p><span data-ttu-id="d77d9-195">
                    <strong>包括支出</strong>
                </span><span class="sxs-lookup"><span data-stu-id="d77d9-195">
                    <strong>Include Expense</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="d77d9-196">
                    <strong>包括材料</strong>
                </span><span class="sxs-lookup"><span data-stu-id="d77d9-196">
                    <strong>Include Materials</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="d77d9-197">
                    <strong>添加</strong>
                </span><span class="sxs-lookup"><span data-stu-id="d77d9-197">
                    <strong>Include</strong>
                </span></span></p>
                <p><span data-ttu-id="d77d9-198">
                    <strong>费用</strong>
                </span><span class="sxs-lookup"><span data-stu-id="d77d9-198">
                    <strong>Fee</strong>
                </span></span></p>
            </td>
            <td width="53" valign="top">
                <p><span data-ttu-id="d77d9-199">
                    <strong>有效/无效</strong>
                </span><span class="sxs-lookup"><span data-stu-id="d77d9-199">
                    <strong>Valid/ Not valid</strong>
                </span></span></p>
            </td>
            <td width="250" valign="top">
                <p><span data-ttu-id="d77d9-200">
                    <strong>原因</strong>
                </span><span class="sxs-lookup"><span data-stu-id="d77d9-200">
                    <strong>Reason</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="d77d9-201">C1</span><span class="sxs-lookup"><span data-stu-id="d77d9-201">C1</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="d77d9-202">CL1</span><span class="sxs-lookup"><span data-stu-id="d77d9-202">CL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d77d9-203">P1</span><span class="sxs-lookup"><span data-stu-id="d77d9-203">P1</span></span> </p>
            </td>
            <td width="67" valign="top">
                <p>
<span data-ttu-id="d77d9-204">空白</span><span class="sxs-lookup"><span data-stu-id="d77d9-204">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="d77d9-205">是</span><span class="sxs-lookup"><span data-stu-id="d77d9-205">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="d77d9-206">是</span><span class="sxs-lookup"><span data-stu-id="d77d9-206">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d77d9-207">是</span><span class="sxs-lookup"><span data-stu-id="d77d9-207">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d77d9-208">是</span><span class="sxs-lookup"><span data-stu-id="d77d9-208">Yes</span></span> </p>
            </td>
            <td width="53" rowspan="2" valign="top">
                <p>
<span data-ttu-id="d77d9-209">无效</span><span class="sxs-lookup"><span data-stu-id="d77d9-209">Not valid</span></span> </p>
            </td>
            <td width="250" rowspan="2" valign="top">
                <p>
<span data-ttu-id="d77d9-210">违反规则 #2。</span><span class="sxs-lookup"><span data-stu-id="d77d9-210">Violation of Rule #2.</span></span> <span data-ttu-id="d77d9-211">P1 项目的时间、支出、材料和费用均包含在合同子项 CL1 和 CL2 中。</span><span class="sxs-lookup"><span data-stu-id="d77d9-211">Time, Expense, Materials, and Fees on P1 project are included on both Contract lines CL1 and CL2.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="d77d9-212">C1</span><span class="sxs-lookup"><span data-stu-id="d77d9-212">C1</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="d77d9-213">CL2</span><span class="sxs-lookup"><span data-stu-id="d77d9-213">CL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d77d9-214">P1</span><span class="sxs-lookup"><span data-stu-id="d77d9-214">P1</span></span> </p>
            </td>
            <td width="67" valign="top">
                <p>
<span data-ttu-id="d77d9-215">空白</span><span class="sxs-lookup"><span data-stu-id="d77d9-215">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="d77d9-216">是</span><span class="sxs-lookup"><span data-stu-id="d77d9-216">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="d77d9-217">是</span><span class="sxs-lookup"><span data-stu-id="d77d9-217">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d77d9-218">是</span><span class="sxs-lookup"><span data-stu-id="d77d9-218">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d77d9-219">是</span><span class="sxs-lookup"><span data-stu-id="d77d9-219">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
            </td>
            <td width="65" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="67" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="53" valign="top">
            </td>
            <td width="250" valign="top">
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="d77d9-220">C1</span><span class="sxs-lookup"><span data-stu-id="d77d9-220">C1</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="d77d9-221">CL1</span><span class="sxs-lookup"><span data-stu-id="d77d9-221">CL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d77d9-222">P1</span><span class="sxs-lookup"><span data-stu-id="d77d9-222">P1</span></span> </p>
            </td>
            <td width="67" valign="top">
                <p>
<span data-ttu-id="d77d9-223">空白</span><span class="sxs-lookup"><span data-stu-id="d77d9-223">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="d77d9-224">是</span><span class="sxs-lookup"><span data-stu-id="d77d9-224">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="d77d9-225">No</span><span class="sxs-lookup"><span data-stu-id="d77d9-225">No</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d77d9-226">是</span><span class="sxs-lookup"><span data-stu-id="d77d9-226">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d77d9-227">是</span><span class="sxs-lookup"><span data-stu-id="d77d9-227">Yes</span></span> </p>
            </td>
            <td width="53" rowspan="2" valign="top">
                <p>
<span data-ttu-id="d77d9-228">无效</span><span class="sxs-lookup"><span data-stu-id="d77d9-228">Not valid</span></span> </p>
            </td>
            <td width="250" rowspan="2" valign="top">
                <p>
<span data-ttu-id="d77d9-229">违反规则 #2。</span><span class="sxs-lookup"><span data-stu-id="d77d9-229">Violation of Rule #2.</span></span> <span data-ttu-id="d77d9-230">P1 项目的时间、材料和费用均包含在合同子项 CL1 和 CL2 中。</span><span class="sxs-lookup"><span data-stu-id="d77d9-230">Time, Materials, and Fees on P1 project are included on both Contract lines CL1 and CL2.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="d77d9-231">C1</span><span class="sxs-lookup"><span data-stu-id="d77d9-231">C1</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="d77d9-232">CL2</span><span class="sxs-lookup"><span data-stu-id="d77d9-232">CL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d77d9-233">P1</span><span class="sxs-lookup"><span data-stu-id="d77d9-233">P1</span></span> </p>
            </td>
            <td width="67" valign="top">
                <p>
<span data-ttu-id="d77d9-234">空白</span><span class="sxs-lookup"><span data-stu-id="d77d9-234">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="d77d9-235">是</span><span class="sxs-lookup"><span data-stu-id="d77d9-235">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="d77d9-236">是</span><span class="sxs-lookup"><span data-stu-id="d77d9-236">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d77d9-237">是</span><span class="sxs-lookup"><span data-stu-id="d77d9-237">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d77d9-238">是</span><span class="sxs-lookup"><span data-stu-id="d77d9-238">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
            </td>
            <td width="65" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="67" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="53" valign="top">
            </td>
            <td width="250" valign="top">
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="d77d9-239">C1</span><span class="sxs-lookup"><span data-stu-id="d77d9-239">C1</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="d77d9-240">CL1</span><span class="sxs-lookup"><span data-stu-id="d77d9-240">CL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d77d9-241">P1</span><span class="sxs-lookup"><span data-stu-id="d77d9-241">P1</span></span> </p>
            </td>
            <td width="67" valign="top">
                <p>
<span data-ttu-id="d77d9-242">空白</span><span class="sxs-lookup"><span data-stu-id="d77d9-242">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="d77d9-243">是</span><span class="sxs-lookup"><span data-stu-id="d77d9-243">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="d77d9-244">No</span><span class="sxs-lookup"><span data-stu-id="d77d9-244">No</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d77d9-245">是</span><span class="sxs-lookup"><span data-stu-id="d77d9-245">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d77d9-246">是</span><span class="sxs-lookup"><span data-stu-id="d77d9-246">Yes</span></span> </p>
            </td>
            <td width="53" rowspan="2" valign="top">
                <p>
<span data-ttu-id="d77d9-247">有效</span><span class="sxs-lookup"><span data-stu-id="d77d9-247">Valid</span></span> </p>
            </td>
            <td width="250" rowspan="2" valign="top">
                <p>
<span data-ttu-id="d77d9-248">P1 项目的时间、材料和费用包含在 CL1 中。</span><span class="sxs-lookup"><span data-stu-id="d77d9-248">Time, Materials, and Fees on P1 project are included on CL1.</span></span>
                </p>
                <ul>
                    <li>
<span data-ttu-id="d77d9-249">P1 项目的支出包含在 CL2 中。</span><span class="sxs-lookup"><span data-stu-id="d77d9-249">Expense on P1 project is included on CL2.</span></span>
                    </li>
                </ul>
                <p>
<span data-ttu-id="d77d9-250">每个合同子项中包含的内容均无重叠，因此有效。</span><span class="sxs-lookup"><span data-stu-id="d77d9-250">No overlap in what is being included on each Contract line and therefore valid.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="d77d9-251">C1</span><span class="sxs-lookup"><span data-stu-id="d77d9-251">C1</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="d77d9-252">CL2</span><span class="sxs-lookup"><span data-stu-id="d77d9-252">CL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d77d9-253">P1</span><span class="sxs-lookup"><span data-stu-id="d77d9-253">P1</span></span> </p>
            </td>
            <td width="67" valign="top">
                <p>
<span data-ttu-id="d77d9-254">空白</span><span class="sxs-lookup"><span data-stu-id="d77d9-254">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="d77d9-255">No</span><span class="sxs-lookup"><span data-stu-id="d77d9-255">No</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="d77d9-256">是</span><span class="sxs-lookup"><span data-stu-id="d77d9-256">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d77d9-257">No</span><span class="sxs-lookup"><span data-stu-id="d77d9-257">No</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d77d9-258">No</span><span class="sxs-lookup"><span data-stu-id="d77d9-258">No</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
            </td>
            <td width="65" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="67" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="53" valign="top">
            </td>
            <td width="250" valign="top">
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="d77d9-259">C1</span><span class="sxs-lookup"><span data-stu-id="d77d9-259">C1</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="d77d9-260">CL1</span><span class="sxs-lookup"><span data-stu-id="d77d9-260">CL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d77d9-261">P1</span><span class="sxs-lookup"><span data-stu-id="d77d9-261">P1</span></span> </p>
            </td>
            <td width="67" valign="top">
                <p>
<span data-ttu-id="d77d9-262">仅所选任务</span><span class="sxs-lookup"><span data-stu-id="d77d9-262">Selected tasks only</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="d77d9-263">是</span><span class="sxs-lookup"><span data-stu-id="d77d9-263">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="d77d9-264">是</span><span class="sxs-lookup"><span data-stu-id="d77d9-264">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d77d9-265">是</span><span class="sxs-lookup"><span data-stu-id="d77d9-265">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d77d9-266">是</span><span class="sxs-lookup"><span data-stu-id="d77d9-266">Yes</span></span> </p>
            </td>
            <td width="53" rowspan="2" valign="top">
                <p>
<span data-ttu-id="d77d9-267">无效</span><span class="sxs-lookup"><span data-stu-id="d77d9-267">Not valid</span></span> </p>
            </td>
            <td width="250" rowspan="2" valign="top">
                <p>
<span data-ttu-id="d77d9-268">违反规则 #2</span><span class="sxs-lookup"><span data-stu-id="d77d9-268">Violation of Rule #2</span></span> </p>
                <p>
<span data-ttu-id="d77d9-269">C1 包括项目 P1 中任务子集的时间、材料、支出和费用。</span><span class="sxs-lookup"><span data-stu-id="d77d9-269">C1 includes Time, Materials, Expenses and Fees on a subset of tasks on project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="d77d9-270">CL2 包括整个项目 P1 的时间、材料、支出和费用，因此与 C1 中包含的内容重叠。</span><span class="sxs-lookup"><span data-stu-id="d77d9-270">CL2 includes Time, Materials, Expenses and Fees for the whole project P1 and therefore overlaps with what is included on C1.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="d77d9-271">C1</span><span class="sxs-lookup"><span data-stu-id="d77d9-271">C1</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="d77d9-272">CL2</span><span class="sxs-lookup"><span data-stu-id="d77d9-272">CL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d77d9-273">P1</span><span class="sxs-lookup"><span data-stu-id="d77d9-273">P1</span></span> </p>
            </td>
            <td width="67" valign="top">
                <p>
<span data-ttu-id="d77d9-274">空白</span><span class="sxs-lookup"><span data-stu-id="d77d9-274">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="d77d9-275">是</span><span class="sxs-lookup"><span data-stu-id="d77d9-275">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="d77d9-276">是</span><span class="sxs-lookup"><span data-stu-id="d77d9-276">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d77d9-277">是</span><span class="sxs-lookup"><span data-stu-id="d77d9-277">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d77d9-278">是</span><span class="sxs-lookup"><span data-stu-id="d77d9-278">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
            </td>
            <td width="65" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="67" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="53" valign="top">
            </td>
            <td width="250" valign="top">
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="d77d9-279">C1</span><span class="sxs-lookup"><span data-stu-id="d77d9-279">C1</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="d77d9-280">CL1</span><span class="sxs-lookup"><span data-stu-id="d77d9-280">CL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d77d9-281">P1</span><span class="sxs-lookup"><span data-stu-id="d77d9-281">P1</span></span> </p>
            </td>
            <td width="67" valign="top">
                <p>
<span data-ttu-id="d77d9-282">仅所选任务</span><span class="sxs-lookup"><span data-stu-id="d77d9-282">Selected tasks only</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="d77d9-283">是</span><span class="sxs-lookup"><span data-stu-id="d77d9-283">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="d77d9-284">是</span><span class="sxs-lookup"><span data-stu-id="d77d9-284">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d77d9-285">是</span><span class="sxs-lookup"><span data-stu-id="d77d9-285">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d77d9-286">是</span><span class="sxs-lookup"><span data-stu-id="d77d9-286">Yes</span></span> </p>
            </td>
            <td width="53" rowspan="2" valign="top">
                <p>
<span data-ttu-id="d77d9-287">有效</span><span class="sxs-lookup"><span data-stu-id="d77d9-287">Valid</span></span> </p>
            </td>
            <td width="250" rowspan="2" valign="top">
                <p>
<span data-ttu-id="d77d9-288">根据规则 #3</span><span class="sxs-lookup"><span data-stu-id="d77d9-288">Per Rule #3</span></span> </p>
                <p>
<span data-ttu-id="d77d9-289">C1 包括项目 P1 中任务子集的时间、支出、材料和费用。</span><span class="sxs-lookup"><span data-stu-id="d77d9-289">C1 includes Time, Expenses, Materials, and Fees on a subset of tasks on project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="d77d9-290">CL2 包括项目 P1 中任务子集的时间、支出、材料和费用。</span><span class="sxs-lookup"><span data-stu-id="d77d9-290">CL2 includes Time, Expenses, Materials, and Fees for a subset of tasks on project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="d77d9-291">唯一的额外验证是验证 CL1 上的任务子集是否与 CL2 上的任务子集不同，以确保没有重叠。</span><span class="sxs-lookup"><span data-stu-id="d77d9-291">The only additional validation is around the subset of tasks on CL1 is different from the subset of tasks on CL2 to ensure that there are no overlaps there.</span></span> <span data-ttu-id="d77d9-292">当任务关联时，这由系统完成。</span><span class="sxs-lookup"><span data-stu-id="d77d9-292">This is done by the system when tasks are associated.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="d77d9-293">C1</span><span class="sxs-lookup"><span data-stu-id="d77d9-293">C1</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="d77d9-294">CL2</span><span class="sxs-lookup"><span data-stu-id="d77d9-294">CL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d77d9-295">P1</span><span class="sxs-lookup"><span data-stu-id="d77d9-295">P1</span></span> </p>
            </td>
            <td width="67" valign="top">
                <p>
<span data-ttu-id="d77d9-296">仅所选任务</span><span class="sxs-lookup"><span data-stu-id="d77d9-296">Selected tasks only</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="d77d9-297">是</span><span class="sxs-lookup"><span data-stu-id="d77d9-297">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="d77d9-298">是</span><span class="sxs-lookup"><span data-stu-id="d77d9-298">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d77d9-299">是</span><span class="sxs-lookup"><span data-stu-id="d77d9-299">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d77d9-300">是</span><span class="sxs-lookup"><span data-stu-id="d77d9-300">Yes</span></span> </p>
            </td>
        </tr>
    </tbody>
</table>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
