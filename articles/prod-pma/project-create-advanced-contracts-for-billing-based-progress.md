---
title: 根据进度创建高级计费合同
description: 本主题说明如何创建项目合同，以便您可以根据已完成工作的百分比为客户生成发票。
author: RadhikaRS
manager: AnnBe
ms.date: 03/26/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: b1de330df8cf85ed30c0ee4e4f2f2fe74d05dbff
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/15/2021
ms.locfileid: "5289493"
---
# <a name="create-advanced-contracts-for-billing-based-on-progress"></a><span data-ttu-id="5852e-103">根据进度创建高级计费合同</span><span class="sxs-lookup"><span data-stu-id="5852e-103">Create advanced contracts for billing based on progress</span></span>
[!include [banner](../includes/banner.md)]

<span data-ttu-id="5852e-104">本主题说明如何创建项目合同，以便您可以根据已完成工作的百分比为客户创建发票。</span><span class="sxs-lookup"><span data-stu-id="5852e-104">This topic explains how to create project contracts so that you can create invoices for customers, based on a percentage of completed work.</span></span> <span data-ttu-id="5852e-105">自动计算为项目设置工作的预算类别的发票金额。</span><span class="sxs-lookup"><span data-stu-id="5852e-105">Invoice amounts are automatically calculated for the budget categories of work that you set up for a project.</span></span> <span data-ttu-id="5852e-106">在与客户协商项目合同时设置发票计时。</span><span class="sxs-lookup"><span data-stu-id="5852e-106">The invoice timing is set when you negotiate the project contract with the customer.</span></span>

<span data-ttu-id="5852e-107">使用本主题介绍的过程设置合同、关联项目，以及计算为项目设置的工作预算类别的发票金额的开票规则。</span><span class="sxs-lookup"><span data-stu-id="5852e-107">Use the procedures in this topic to set up a contract, an associated project, and the billing rules that calculate invoice amounts for the budget categories of work that you set up for the project.</span></span>

<span data-ttu-id="5852e-108">创建了合同和项目后，可以设置项目的详细信息。</span><span class="sxs-lookup"><span data-stu-id="5852e-108">After you've created the contract and the project, you can set up the details of the project.</span></span> <span data-ttu-id="5852e-109">例如，您可以定义活动并可以将工作人员分配给项目。</span><span class="sxs-lookup"><span data-stu-id="5852e-109">For example, you can define activities and assign workers to the project.</span></span>

## <a name="example"></a><span data-ttu-id="5852e-110">示例</span><span class="sxs-lookup"><span data-stu-id="5852e-110">Example</span></span>

<span data-ttu-id="5852e-111">您的组织是软件开发公司。</span><span class="sxs-lookup"><span data-stu-id="5852e-111">Your organization is a software development firm.</span></span> <span data-ttu-id="5852e-112">您同意为客户开发总费用为 20,000 美元 (USD) 的工资核算包装。</span><span class="sxs-lookup"><span data-stu-id="5852e-112">You agree to develop a payroll accounting package for a customer for a total fee of 20,000 US dollars (USD).</span></span> <span data-ttu-id="5852e-113">完成项目的特定百分比时，您的组织同意向客户开发票。</span><span class="sxs-lookup"><span data-stu-id="5852e-113">Your organization agrees to invoice the customer as you complete specific percentages of the project.</span></span> <span data-ttu-id="5852e-114">您为工作设置了以下项目类别，以便可以在开票过程中使用它们：</span><span class="sxs-lookup"><span data-stu-id="5852e-114">You set up the following project categories for the work, so that you can use them in the billing process:</span></span>

- <span data-ttu-id="5852e-115">咨询业</span><span class="sxs-lookup"><span data-stu-id="5852e-115">Consulting</span></span>
- <span data-ttu-id="5852e-116">设计​​</span><span class="sxs-lookup"><span data-stu-id="5852e-116">Design</span></span>
- <span data-ttu-id="5852e-117">安装</span><span class="sxs-lookup"><span data-stu-id="5852e-117">Installation</span></span>

<span data-ttu-id="5852e-118">您还为每个类别完成的项目工作的百分比自动计算发票金额设置计费规则。</span><span class="sxs-lookup"><span data-stu-id="5852e-118">You also set up billing rules that automatically calculate the invoice amounts for the percentage of project work that is completed in each category.</span></span>

<span data-ttu-id="5852e-119">预算经理已为项目类别创建预算。</span><span class="sxs-lookup"><span data-stu-id="5852e-119">The budget manager creates a budget for the project categories.</span></span> <span data-ttu-id="5852e-120">完成工作金额自动计算为与预算金额进行比较的实际工作的百分比。</span><span class="sxs-lookup"><span data-stu-id="5852e-120">The amount of completed work is automatically calculated as a percentage of actual work in comparison to the budgeted amounts.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="5852e-121">先决条件</span><span class="sxs-lookup"><span data-stu-id="5852e-121">Prerequisites</span></span>

<span data-ttu-id="5852e-122">在创建使用计费规则的项目之前，必须设置计费规则的编号规则以及用于过帐按进度付款的费用日记帐。</span><span class="sxs-lookup"><span data-stu-id="5852e-122">Before you create a project that uses billing rules, you must set up the number sequences for billing rules and a fee journal that is used to post progress billings.</span></span>

1. <span data-ttu-id="5852e-123">转至 **项目管理和核算** \> **设置** \> **项目管理和核算参数**。</span><span class="sxs-lookup"><span data-stu-id="5852e-123">Go to **Project management and accounting** \> **Setup** \> **Project management and accounting parameters**.</span></span>
2. <span data-ttu-id="5852e-124">在 **项目管理和核算参数** 页面上的 **编号规则** 选项卡上，设置要在创建计费规则时使用的编号规则。</span><span class="sxs-lookup"><span data-stu-id="5852e-124">On the **Project management and accounting parameters** page, on the **Number sequences** tab, set up the number sequence that you want to use when billing rules are created.</span></span>
3. <span data-ttu-id="5852e-125">转到 **项目管理和会计** \> **日记帐** \> **费用**。</span><span class="sxs-lookup"><span data-stu-id="5852e-125">Go to **Project management and accounting** \> **Journals** \> **Fee**.</span></span>
4. <span data-ttu-id="5852e-126">在 **费用日记帐** 页面，选择 **新建**，然后输入日记帐名称。</span><span class="sxs-lookup"><span data-stu-id="5852e-126">On the **Fee journal** page, select **New**, and enter the journal name.</span></span>

## <a name="create-a-contract-for-progress-billings"></a><span data-ttu-id="5852e-127">创建进度计费的合同</span><span class="sxs-lookup"><span data-stu-id="5852e-127">Create a contract for progress billings</span></span>

<span data-ttu-id="5852e-128">使用此过程可以创建固定价格项目的项目合同。</span><span class="sxs-lookup"><span data-stu-id="5852e-128">Use this procedure to create a project contract for a fixed-price project.</span></span> <span data-ttu-id="5852e-129">在项目完成的工作到达指定的百分比时，您创建某一项目发票。</span><span class="sxs-lookup"><span data-stu-id="5852e-129">You create a project invoice when the work that is completed on the project reaches a specified percentage.</span></span>

1. <span data-ttu-id="5852e-130">转到 **项目管理和核算** \> **项目** \> **项目合同**。</span><span class="sxs-lookup"><span data-stu-id="5852e-130">Go to **Project management and accounting** \> **Projects** \> **Project contracts**.</span></span>
2. <span data-ttu-id="5852e-131">在 **项目合同** 页面上，选择 **新建**。</span><span class="sxs-lookup"><span data-stu-id="5852e-131">On the **Project contracts** page, select **New**.</span></span>
3. <span data-ttu-id="5852e-132">在 **新建项目合同** 对话框中，设置以下字段：</span><span class="sxs-lookup"><span data-stu-id="5852e-132">In the **New project contract** dialog box, set the following fields:</span></span>

    - <span data-ttu-id="5852e-133">**客户**</span><span class="sxs-lookup"><span data-stu-id="5852e-133">**Name**</span></span>
    - <span data-ttu-id="5852e-134">**融资类型**</span><span class="sxs-lookup"><span data-stu-id="5852e-134">**Funding type**</span></span>
    - <span data-ttu-id="5852e-135">**融资来源**</span><span class="sxs-lookup"><span data-stu-id="5852e-135">**Funding source**</span></span>
    - <span data-ttu-id="5852e-136">**销售币种** – 默认情况下，该币种用于与项目合同的客户发票。</span><span class="sxs-lookup"><span data-stu-id="5852e-136">**Sales currency** – By default, this currency is used for customer invoices that are associated with the project contract.</span></span> <span data-ttu-id="5852e-137">但是，您可以更改特定客户发票上的销售币种。</span><span class="sxs-lookup"><span data-stu-id="5852e-137">However, you can change the sales currency on a specific customer invoice.</span></span>

4. <span data-ttu-id="5852e-138">选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="5852e-138">Select **OK**.</span></span> <span data-ttu-id="5852e-139">此信息将复制到 **项目合同** 页面的标题中。</span><span class="sxs-lookup"><span data-stu-id="5852e-139">The information is copied to the header of the **Project contracts** page.</span></span>
5. <span data-ttu-id="5852e-140">在 **项目合同** 页面上，填写项目所需的其余信息。</span><span class="sxs-lookup"><span data-stu-id="5852e-140">On the **Project contracts** page, fill in the rest of the required information for the project.</span></span>

## <a name="create-a-project-for-progress-billings"></a><span data-ttu-id="5852e-141">创建进度计费的项目</span><span class="sxs-lookup"><span data-stu-id="5852e-141">Create a project for progress billings</span></span>

<span data-ttu-id="5852e-142">按照以下步骤创建项目以及任何与项目合同相关联的子项目。</span><span class="sxs-lookup"><span data-stu-id="5852e-142">Follow these steps to create a project and any subprojects that are associated with a project contract.</span></span>

1. <span data-ttu-id="5852e-143">转到 **项目管理和会计** \> **项目** \> **全部项目**。</span><span class="sxs-lookup"><span data-stu-id="5852e-143">Go to **Project management and accounting** \> **Projects** \> **All projects**.</span></span>
2. <span data-ttu-id="5852e-144">在 **所有项目** 页面上，选择 **新建**。</span><span class="sxs-lookup"><span data-stu-id="5852e-144">On the **All projects** page, select **New**.</span></span>
3. <span data-ttu-id="5852e-145">在 **新建项目** 对话框的 **项目类型** 字段中，选择 **时间和材料**。</span><span class="sxs-lookup"><span data-stu-id="5852e-145">In the **New project** dialog box, in the **Project type** field, select **Time and material**.</span></span>
4. <span data-ttu-id="5852e-146">选择项目组。</span><span class="sxs-lookup"><span data-stu-id="5852e-146">Select a project group.</span></span> <span data-ttu-id="5852e-147">项目组定义分配给组的项目的过帐信息。</span><span class="sxs-lookup"><span data-stu-id="5852e-147">A project group defines the posting information for the projects that are assigned to the group.</span></span>
5. <span data-ttu-id="5852e-148">选择 **创建项目**。</span><span class="sxs-lookup"><span data-stu-id="5852e-148">Select **Create project**.</span></span>
6. <span data-ttu-id="5852e-149">在创建项目后，将项目阶段设置为 **进行中**。</span><span class="sxs-lookup"><span data-stu-id="5852e-149">After the project is created, set the project stage to **In process**.</span></span>

## <a name="create-a-budget-for-a-project"></a><span data-ttu-id="5852e-150">创建项目预算</span><span class="sxs-lookup"><span data-stu-id="5852e-150">Create a budget for a project</span></span>

<span data-ttu-id="5852e-151">预算类别用于就各类别完成的工作百分比自动计算发票金额。</span><span class="sxs-lookup"><span data-stu-id="5852e-151">Budget categories are used to automatically calculate the invoice amounts for the percentage of work that is completed for each category.</span></span> <span data-ttu-id="5852e-152">请按照以下步骤创建估计成本的预算类别。</span><span class="sxs-lookup"><span data-stu-id="5852e-152">Follow these steps to create budget categories for the estimated costs.</span></span>

1. <span data-ttu-id="5852e-153">转到 **项目管理和会计** \> **项目** \> **全部项目**。</span><span class="sxs-lookup"><span data-stu-id="5852e-153">Go to **Project management and accounting** \> **Projects** \> **All projects**.</span></span>
2. <span data-ttu-id="5852e-154">在 **所有项目** 页面上，选择并打开所需的项目。</span><span class="sxs-lookup"><span data-stu-id="5852e-154">On the **All projects** page, select and open the project that you want.</span></span>
3. <span data-ttu-id="5852e-155">在 **项目** 页面，在操作窗格的 **计划** 选项卡上，在 **预算** 组中，选择 **项目预算**。</span><span class="sxs-lookup"><span data-stu-id="5852e-155">On the **Projects** page, on the Action Pane, on the **Plan** tab, in the **Budget** group, select **Project budget**.</span></span>
4. <span data-ttu-id="5852e-156">在 **项目预算** 页面，输入项目中每个类别的估计成本。</span><span class="sxs-lookup"><span data-stu-id="5852e-156">On the **Project budget** page, enter an estimated cost for each category in the project.</span></span>

## <a name="create-billing-rules-for-progress-billings"></a><span data-ttu-id="5852e-157">创建按进度的付款比率项规则</span><span class="sxs-lookup"><span data-stu-id="5852e-157">Create billing rules for progress billings</span></span>

1. <span data-ttu-id="5852e-158">转到 **项目管理和核算** \> **项目** \> **项目合同**。</span><span class="sxs-lookup"><span data-stu-id="5852e-158">Go to **Project management and accounting** \> **Projects** \> **Project contracts**.</span></span>
2. <span data-ttu-id="5852e-159">在 **项目合同** 页面上，选择并打开一个项目合同。</span><span class="sxs-lookup"><span data-stu-id="5852e-159">On the **Project contracts** page, select and open a project contract.</span></span>
3. <span data-ttu-id="5852e-160">在项目合同页面，在 **计费规则** 快速选项卡上，选择 **添加**。</span><span class="sxs-lookup"><span data-stu-id="5852e-160">On the project contract page, on the **Billing rules** FastTab, select **Add**.</span></span>
4. <span data-ttu-id="5852e-161">在 **计费规则** 页面，在 **行类型** 字段中，选择 **进度**。</span><span class="sxs-lookup"><span data-stu-id="5852e-161">On the **Billing rule** page, in the **Line type** field, select **Progress**.</span></span>
5. <span data-ttu-id="5852e-162">在 **计费规则行详细信息** 快速选项卡上，在 **合同价值** 字段中，输入合同的总值。</span><span class="sxs-lookup"><span data-stu-id="5852e-162">On the **Billing rule line details** FastTab, in the **Contract value** field, enter the total value of the contract.</span></span>
6. <span data-ttu-id="5852e-163">在 **类别** 字段中，选择要过帐的费用交易记录的类别。</span><span class="sxs-lookup"><span data-stu-id="5852e-163">In the **Category** field, select the category to post the fee transaction to.</span></span>
7. <span data-ttu-id="5852e-164">在 **项目** 字段中，选择使用此计费规则的项目。</span><span class="sxs-lookup"><span data-stu-id="5852e-164">In the **Project** field, select the project that uses this billing rule.</span></span>
8. <span data-ttu-id="5852e-165">可选：将计费规则分配到其他项目。</span><span class="sxs-lookup"><span data-stu-id="5852e-165">Optional: Assign the billing rule to additional projects.</span></span> <span data-ttu-id="5852e-166">在 **项目** 快速选项卡上的 **可用项目** 部分，选择一个项目，然后选择右箭头按钮将该项目添加到 **所选项目** 部分。</span><span class="sxs-lookup"><span data-stu-id="5852e-166">On the **Project** FastTab, in the **Available projects** section, select a project, and then select the right arrow button to add the project to the **Selected projects** section.</span></span>
9. <span data-ttu-id="5852e-167">可选：计算客户从发票上的付款预扣的百分比金额。</span><span class="sxs-lookup"><span data-stu-id="5852e-167">Optional: Calculate the percentage amount that the customer withholds from payments on an invoice.</span></span> <span data-ttu-id="5852e-168">在 **付款保留条款** 快速选项卡上，选择融资来源，然后在 **保留百分比** 字段中输入保留百分比。</span><span class="sxs-lookup"><span data-stu-id="5852e-168">On the **Payment retention terms** FastTab, select the funding source, and then, in the **Retention percentage** field, enter the retention percentage.</span></span>
10. <span data-ttu-id="5852e-169">重复这些步骤创建项目合同的其他计费规则。</span><span class="sxs-lookup"><span data-stu-id="5852e-169">Repeat these steps to create additional billing rules for the project contract.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]