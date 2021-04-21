---
title: 更正项目发票
description: 本主题提供关于如何在 Project Operations 中创建并确认更正发票的信息。
author: rumant
manager: Annbe
ms.date: 04/05/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: ae6d881e4e68b9f467478afe9735fc3186e6b0a8
ms.sourcegitcommit: ca0fc078d1a12484eca193fe051b8442c0559db8
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/07/2021
ms.locfileid: "5866580"
---
# <a name="corrective-project-invoices"></a><span data-ttu-id="c7da5-103">更正项目发票</span><span class="sxs-lookup"><span data-stu-id="c7da5-103">Corrective project invoices</span></span>

<span data-ttu-id="c7da5-104">_**适用于：** 精简部署 - 估价交易开票_</span><span class="sxs-lookup"><span data-stu-id="c7da5-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="c7da5-105">确认的项目发票可以更正以处理与客户和项目经理协商的变更或贷记。</span><span class="sxs-lookup"><span data-stu-id="c7da5-105">A confirmed project invoice can be corrected to process changes or credits as negotiated with the customer and project manager.</span></span>

<span data-ttu-id="c7da5-106">若要对已确认的发票进行编辑，请打开已确认的发票，选择 **更正此发票**。</span><span class="sxs-lookup"><span data-stu-id="c7da5-106">To make edits to a confirmed invoice, open the confirmed invoice and select **Correct this Invoice**.</span></span> 

> [!NOTE]
> <span data-ttu-id="c7da5-107">除非项目发票已确认，否则此选择不可用。</span><span class="sxs-lookup"><span data-stu-id="c7da5-107">This selection isn't available unless a project invoice is confirmed.</span></span>

<span data-ttu-id="c7da5-108">将从已确认的发票创建新的草稿发票。</span><span class="sxs-lookup"><span data-stu-id="c7da5-108">A new draft invoice is created from the confirmed invoice.</span></span> <span data-ttu-id="c7da5-109">之前已确认发票中的所有发票明细详细信息将被复制到新的草稿发票。</span><span class="sxs-lookup"><span data-stu-id="c7da5-109">All invoice line details from the previously confirmed invoice are copied to the new draft.</span></span> <span data-ttu-id="c7da5-110">以下是用于了解新的更正发票上的明细详细信息的一些要点：</span><span class="sxs-lookup"><span data-stu-id="c7da5-110">The following are some of the key points to understand about the line details on the new corrected invoice:</span></span>

- <span data-ttu-id="c7da5-111">所有数量都更新为零。</span><span class="sxs-lookup"><span data-stu-id="c7da5-111">All quantities are updated to zero.</span></span> <span data-ttu-id="c7da5-112">应用程序假定所有已开票的项均已完全贷记。</span><span class="sxs-lookup"><span data-stu-id="c7da5-112">The application assumes that all invoiced items are fully credited.</span></span> <span data-ttu-id="c7da5-113">如果需要，您可以手动更新这些数量以反映要开票的数量，而不是要贷记的数量。</span><span class="sxs-lookup"><span data-stu-id="c7da5-113">If needed, you can manually update these quantities to reflect the quantity that is being invoiced, and not the quantity that is being credited.</span></span> <span data-ttu-id="c7da5-114">根据您输入的数量，应用程序将计算贷记的数量。</span><span class="sxs-lookup"><span data-stu-id="c7da5-114">Based on the quantity you enter, the application calculates the credited quantity.</span></span> <span data-ttu-id="c7da5-115">在确认更正发票时，此金额会反映在创建的实际值中。</span><span class="sxs-lookup"><span data-stu-id="c7da5-115">This amount is reflected in the actuals that are created when the corrected invoice is confirmed.</span></span> <span data-ttu-id="c7da5-116">如果您要更改税额，必须输入正确的税额，而不是要贷记的税额。</span><span class="sxs-lookup"><span data-stu-id="c7da5-116">If you are making changes to the tax amount, you must enter the correct tax amount and not the tax amount that is being credited.</span></span>
- <span data-ttu-id="c7da5-117">之前已确认的基于产品的合同子项不会复制。</span><span class="sxs-lookup"><span data-stu-id="c7da5-117">Previously confirmed product-based contract lines are not copied over.</span></span> <span data-ttu-id="c7da5-118">不支持在基于产品的项目发票上处理更正。</span><span class="sxs-lookup"><span data-stu-id="c7da5-118">Processing corrections on a product-based project invoice is not supported.</span></span>
- <span data-ttu-id="c7da5-119">里程碑更正始终处理为完全贷记。</span><span class="sxs-lookup"><span data-stu-id="c7da5-119">Milestone corrections are always processed as full credits.</span></span>
- <span data-ttu-id="c7da5-120">如果客户开票的金额不正确，可以更正保留款或预付款金额。</span><span class="sxs-lookup"><span data-stu-id="c7da5-120">Retainer or advance amounts can be corrected if the customer was invoiced for an incorrect amount.</span></span>
- <span data-ttu-id="c7da5-121">如果使用了不正确的金额与之前确认的发票上的费用对帐，可以更正保留款或预付款的对帐。</span><span class="sxs-lookup"><span data-stu-id="c7da5-121">Reconciliations of retainers and advances can be corrected if an incorrect amount was used to reconcile against the charges on a previously confirmed invoice.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="c7da5-122">作为其他已开票费用的更正内容的发票明细详细信息，会将字段 **更正** 设置为 **是**。</span><span class="sxs-lookup"><span data-stu-id="c7da5-122">Invoice line details that are corrections to other already invoiced charges have the field **Correction** set to **Yes**.</span></span> <span data-ttu-id="c7da5-123">包含更正发票明细详细信息的发票具有名为 **具有更正** 的字段，此字段也会设置为 **是**。</span><span class="sxs-lookup"><span data-stu-id="c7da5-123">Invoices that have corrected invoice line details have a field called **Has corrections** that is also set to **Yes**.</span></span>

## <a name="actuals-created-when-a-corrective-invoice-is-confirmed"></a><span data-ttu-id="c7da5-124">确认更正发票后创建的实际值</span><span class="sxs-lookup"><span data-stu-id="c7da5-124">Actuals created when a corrective invoice is confirmed</span></span>

<span data-ttu-id="c7da5-125">下表列出了确认纠正发票后创建的实际值。</span><span class="sxs-lookup"><span data-stu-id="c7da5-125">The following table lists the actuals that are created when a corrective invoice is confirmed.</span></span>

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="216" valign="top">
                <p><span data-ttu-id="c7da5-126">
                    <strong>方案</strong>
                </span><span class="sxs-lookup"><span data-stu-id="c7da5-126">
                    <strong>Scenario</strong>
                </span></span></p>
            </td>
            <td width="808" valign="top">
                <p><span data-ttu-id="c7da5-127">
                    <strong>确认时创建的实际值</strong>
                </span><span class="sxs-lookup"><span data-stu-id="c7da5-127">
                    <strong>Actuals created on confirmation</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="4" valign="top">
                <p>
<span data-ttu-id="c7da5-128">确认已开票预付款或保留款的更正。<strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="c7da5-128">Confirm the correction of an invoiced advance or retainer.<strong></strong>
                </span></span></p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="c7da5-129">为对帐创建的保留款或预付款的未记帐销售额冲销。</span><span class="sxs-lookup"><span data-stu-id="c7da5-129">An unbilled sales reversal of the retainer or advance that was created for reconciliation.</span></span> <span data-ttu-id="c7da5-130">此金额为正值，因为它用于取消在对保留款或预付款开票时创建的负值。</span><span class="sxs-lookup"><span data-stu-id="c7da5-130">This amount is positive because it is meant to cancel out the negative that was created when the retainer or advance was invoiced.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="c7da5-131">将为保留款或预付款中的金额创建已记帐销售额冲销实际值，以冲销原始已记帐销售额。</span><span class="sxs-lookup"><span data-stu-id="c7da5-131">A billed sales reversal actual is created for the amount on the retainer or advance to reverse the original billed sales.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="c7da5-132">将为基于保留款或预付款的更正发票明细上的更正金额创建新的已记帐实际销售额。</span><span class="sxs-lookup"><span data-stu-id="c7da5-132">A new billed sales actual is created for the corrected amount on the retainer or advance-based corrected invoice line.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="c7da5-133">基于保留款或预付款的更正发票明细的负金额的未记帐实际销售额，将用于对帐。</span><span class="sxs-lookup"><span data-stu-id="c7da5-133">An unbilled sales actual of negative amount of the retainer or advance-based corrected invoice line, which will be used for reconciliation.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="4" valign="top">
                <p>
<span data-ttu-id="c7da5-134">确认之前对帐的保留款或预付款的更正。</span><span class="sxs-lookup"><span data-stu-id="c7da5-134">A confirmation of the correction of a previously reconciled retainer or advance.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="c7da5-135">为对帐创建的保留款或预付款的未记帐销售额冲销。</span><span class="sxs-lookup"><span data-stu-id="c7da5-135">An unbilled sales reversal of the retainer or advance that was created for reconciliation.</span></span> <span data-ttu-id="c7da5-136">此金额为正值，用于取消之前对帐发生时创建的负值。</span><span class="sxs-lookup"><span data-stu-id="c7da5-136">This amount is positive and is meant to cancel out the negative that was created when the previous reconciliation occurred.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="c7da5-137">之前发票上金额的已记帐销售额冲销实际值。</span><span class="sxs-lookup"><span data-stu-id="c7da5-137">A billed sales reversal actual for the amount on the previous invoice.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="c7da5-138">更正发票上应用的更正保留款金额的新的已记帐实际销售额。</span><span class="sxs-lookup"><span data-stu-id="c7da5-138">A new billed sales actual for the corrected retainer amount that is applied on the corrected invoice.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="c7da5-139">具有更正的剩余保留款或预付款的负金额的未记帐实际销售额，将用于以后发票的对帐。</span><span class="sxs-lookup"><span data-stu-id="c7da5-139">An unbilled sales actual with a negative amount from the corrected leftover retainer or advance, which will be used for reconciliation on later invoices.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="c7da5-140">为之前开票的时间交易的完全贷记开票。</span><span class="sxs-lookup"><span data-stu-id="c7da5-140">Invoicing the full credit of a previously invoiced time transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="c7da5-141">原始时间发票明细详细信息中时数和金额的已记帐销售额冲销。</span><span class="sxs-lookup"><span data-stu-id="c7da5-141">A billed sales reversal for the hours and amount on the original invoice line detail for time.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="c7da5-142">原始时间发票明细详细信息中时数和金额的新的未记帐实际销售额。</span><span class="sxs-lookup"><span data-stu-id="c7da5-142">A new unbilled sales actual for the hours and amount on the original invoice line detail for time.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="c7da5-143">为时间交易中的部分贷记开票。</span><span class="sxs-lookup"><span data-stu-id="c7da5-143">Invoicing the partial credit on a time transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="c7da5-144">原始时间发票明细详细信息中已开票时数和金额的已记帐销售额冲销。</span><span class="sxs-lookup"><span data-stu-id="c7da5-144">A billed sales reversal for the hours and amount invoiced on the original invoice line detail for time.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="c7da5-145">编辑的发票明细详细信息中的时数和金额应计费的新未记帐实际销售额，此实际销售额的冲销和相等的已记帐实际销售额。</span><span class="sxs-lookup"><span data-stu-id="c7da5-145">A new unbilled sales actual that is chargeable for the hours and amount on the edited invoice line detail, a reversal of this, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="c7da5-146">扣除发票明细详细信息中的更正数字后，剩余时数和金额应计费的新的未记帐实际销售额。</span><span class="sxs-lookup"><span data-stu-id="c7da5-146">A new unbilled sales actual that is chargeable for the remaining hours and amount after deducting the corrected figures on the invoice line detail.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="c7da5-147">为之前开票的支出交易的完全贷记开票。</span><span class="sxs-lookup"><span data-stu-id="c7da5-147">Invoicing the full credit of a previously invoiced expense transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="c7da5-148">原始支出发票明细详细信息中数量和金额的已记帐销售额冲销。</span><span class="sxs-lookup"><span data-stu-id="c7da5-148">A billed sales reversal for the quantity and amount on the original invoice line detail for the expense.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="c7da5-149">原始支出发票明细详细信息中数量和金额的新的未记帐实际销售额。</span><span class="sxs-lookup"><span data-stu-id="c7da5-149">A new unbilled sales actual for the quantity and amount on the original invoice line detail for the expense.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="c7da5-150">为之前开票的支出交易的部分贷记开票。</span><span class="sxs-lookup"><span data-stu-id="c7da5-150">Invoicing the partial credit of a previously invoiced expense transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="c7da5-151">原始支出发票明细详细信息中已开票数量和金额的已记帐销售额冲销。</span><span class="sxs-lookup"><span data-stu-id="c7da5-151">A billed sales reversal for the quantity and amount invoiced on the original invoice line detail for an expense.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="c7da5-152">更正后的发票明细详细信息中的数量和金额应计费的新未记帐实际销售额，此实际销售额的冲销和相等的已记帐实际销售额。</span><span class="sxs-lookup"><span data-stu-id="c7da5-152">A new unbilled sales actual that is chargeable for the quantity and amount on the corrected invoice line detail, a reversal of this, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="c7da5-153">扣除发票明细详细信息中的更正数字后，剩余数量和金额应计费的新的未记帐实际销售额。</span><span class="sxs-lookup"><span data-stu-id="c7da5-153">A new unbilled sales actual that is chargeable for the remaining quantity and amount after deducting the corrected figures on the invoice line detail.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="c7da5-154">对先前已开票材料交易的全部贷记开具发票。</span><span class="sxs-lookup"><span data-stu-id="c7da5-154">Invoicing the full credit of a previously invoiced material transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="c7da5-155">原始材料发票明细详细信息中数量和金额的记帐销售冲销。</span><span class="sxs-lookup"><span data-stu-id="c7da5-155">A billed sales reversal for the quantity and amount on the original invoice line detail for material.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="c7da5-156">原始材料发票明细详细信息中数量和金额的新未记帐销售实际值。</span><span class="sxs-lookup"><span data-stu-id="c7da5-156">A new unbilled sales actual for the quantity and amount on the original invoice line detail for material.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="c7da5-157">对材料交易上的部分贷记开具发票。</span><span class="sxs-lookup"><span data-stu-id="c7da5-157">Invoicing the partial credit on a material transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="c7da5-158">原始材料发票明细详细信息中开票的数量和金额的记帐销售冲销。</span><span class="sxs-lookup"><span data-stu-id="c7da5-158">A billed sales reversal for the quantity and amount invoiced on the original invoice line detail for material.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="c7da5-159">一个新的未记帐销售实际值，对于编辑的发票明行明细上的数量和金额、其冲销和等值的已记帐销售实际值，该未记帐销售实际值为非应计费。</span><span class="sxs-lookup"><span data-stu-id="c7da5-159">A new unbilled sales actual that is chargeable for the quantity and amount on the edited invoice line detail, a reversal of this, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="c7da5-160">扣除发票明细详细信息中的更正数字后，剩余数量和金额应计费的新的未记帐实际销售额。</span><span class="sxs-lookup"><span data-stu-id="c7da5-160">A new unbilled sales actual that is chargeable for the remaining quantity and amount after deducting the corrected figures on the invoice line detail.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="c7da5-161">为之前开票的费用交易的完全贷记开票。</span><span class="sxs-lookup"><span data-stu-id="c7da5-161">Invoicing the full credit of a previously invoiced fee transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="c7da5-162">原始费用发票明细详细信息中数量和金额的已记帐销售额冲销。</span><span class="sxs-lookup"><span data-stu-id="c7da5-162">A billed sales reversal for the quantity and amount on the original invoice line detail for the fee.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="c7da5-163">原始费用发票明细详细信息中数量和金额的新的未记帐实际销售额。</span><span class="sxs-lookup"><span data-stu-id="c7da5-163">A new unbilled sales actual for the quantity and amount on the original invoice line detail for the fee.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="c7da5-164">为之前开票的费用交易的部分贷记开票。</span><span class="sxs-lookup"><span data-stu-id="c7da5-164">Invoicing the partial credit of a previously invoiced fee transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="c7da5-165">原始费用发票明细详细信息中已开票数量和金额的已记帐销售额冲销。</span><span class="sxs-lookup"><span data-stu-id="c7da5-165">A billed sales reversal for the quantity and amount invoiced on the original invoice line detail for fee.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="c7da5-166">编辑后的纠正发票明细详细信息中的数量和金额应计费的新未记帐实际销售额，此实际销售额的冲销和相等的已记帐实际销售额。</span><span class="sxs-lookup"><span data-stu-id="c7da5-166">A new unbilled sales actual that is chargeable for the quantity and amount on the edited corrective invoice line detail, a reversal of this, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="c7da5-167">为之前开票的里程碑的完全贷记开票。</span><span class="sxs-lookup"><span data-stu-id="c7da5-167">Invoicing the full credit of a previously invoiced milestone.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="c7da5-168">原始里程碑发票明细详细信息中金额的已记帐销售额冲销。</span><span class="sxs-lookup"><span data-stu-id="c7da5-168">A billed sales reversal for the amount on the original invoice line detail for the milestone.</span></span>
                </p>
                <p>
<span data-ttu-id="c7da5-169">里程碑的发票状态从<b>客户发票已过帐</b>更新为<b>已准备好开单</b>。</span><span class="sxs-lookup"><span data-stu-id="c7da5-169">The invoice status of the milestone is updated from <b>Customer Invoice Posted</b> to <b>Ready to Invoice</b>.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="c7da5-170">为之前开票的里程碑的部分贷记开票。</span><span class="sxs-lookup"><span data-stu-id="c7da5-170">Invoicing the partial credit of a previously invoiced milestone.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="c7da5-171">不支持</span><span class="sxs-lookup"><span data-stu-id="c7da5-171">Unsupported</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="c7da5-172">之前已开票的基于产品的合同子项的贷记和更正。</span><span class="sxs-lookup"><span data-stu-id="c7da5-172">Credits and corrections of a previously invoiced product-based contract line.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="c7da5-173">不支持</span><span class="sxs-lookup"><span data-stu-id="c7da5-173">Unsupported</span></span> </p>
            </td>
        </tr>
    </tbody>
</table>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
