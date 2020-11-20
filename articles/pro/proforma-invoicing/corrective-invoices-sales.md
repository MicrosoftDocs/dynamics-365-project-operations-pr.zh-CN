---
title: 已更正发票 - 精简
description: 此主题提供有关 Project Operations 中的更正发票的信息
author: rumant
manager: Annbe
ms.date: 10/15/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 55bec8ad1d9c2b55cabb453321f13df8b7cd1614
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/30/2020
ms.locfileid: "4176420"
---
# <a name="corrected-invoices---lite"></a><span data-ttu-id="f9b30-103">已更正发票 - 精简</span><span class="sxs-lookup"><span data-stu-id="f9b30-103">Corrected invoices - lite</span></span>

<span data-ttu-id="f9b30-104">_**适用于：** 精简部署 - 估价交易开票_</span><span class="sxs-lookup"><span data-stu-id="f9b30-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="f9b30-105">确认的项目发票可以更正以处理与客户和项目经理协商的变更或贷记。</span><span class="sxs-lookup"><span data-stu-id="f9b30-105">A confirmed project invoice can be corrected to process changes or credits as negotiated with the customer and project manager.</span></span>

<span data-ttu-id="f9b30-106">若要对已确认的发票进行编辑，请打开已确认的发票，选择 **更正此发票**。</span><span class="sxs-lookup"><span data-stu-id="f9b30-106">To make edits to a confirmed invoice, open the confirmed invoice and select **Correct this Invoice**.</span></span> 

> [!NOTE]
> <span data-ttu-id="f9b30-107">除非项目发票已确认，否则此选择不可用。</span><span class="sxs-lookup"><span data-stu-id="f9b30-107">This selection isn't available unless a project invoice is confirmed.</span></span>

<span data-ttu-id="f9b30-108">将从已确认的发票创建新的草稿发票。</span><span class="sxs-lookup"><span data-stu-id="f9b30-108">A new draft invoice is created from the confirmed invoice.</span></span> <span data-ttu-id="f9b30-109">之前已确认发票中的所有发票明细详细信息将被复制到新的草稿发票。</span><span class="sxs-lookup"><span data-stu-id="f9b30-109">All invoice line details from the previously confirmed invoice are copied to the new draft.</span></span> <span data-ttu-id="f9b30-110">以下是用于了解新的更正发票上的明细详细信息的一些要点：</span><span class="sxs-lookup"><span data-stu-id="f9b30-110">The following are some of the key points to understand about the line details on the new corrected invoice:</span></span>

- <span data-ttu-id="f9b30-111">所有数量都更新为零。</span><span class="sxs-lookup"><span data-stu-id="f9b30-111">All quantities are updated to zero.</span></span> <span data-ttu-id="f9b30-112">应用程序假定所有已开票的项均已完全贷记。</span><span class="sxs-lookup"><span data-stu-id="f9b30-112">The application assumes that all invoiced items are fully credited.</span></span> <span data-ttu-id="f9b30-113">如果需要，您可以手动更新这些数量以反映要开票的数量，而不是要贷记的数量。</span><span class="sxs-lookup"><span data-stu-id="f9b30-113">If needed, you can manually update these quantities to reflect the quantity that is being invoiced, and not the quantity that is being credited.</span></span> <span data-ttu-id="f9b30-114">根据您输入的数量，应用程序将计算贷记的数量。</span><span class="sxs-lookup"><span data-stu-id="f9b30-114">Based on the quantity you enter, the application calculates the credited quantity.</span></span> <span data-ttu-id="f9b30-115">在确认更正发票时，此金额会反映在创建的实际值中。</span><span class="sxs-lookup"><span data-stu-id="f9b30-115">This amount is reflected in the actuals that are created when the corrected invoice is confirmed.</span></span> <span data-ttu-id="f9b30-116">如果您要更改税额，必须输入正确的税额，而不是要贷记的税额。</span><span class="sxs-lookup"><span data-stu-id="f9b30-116">If you are making changes to the tax amount, you must enter the correct tax amount and not the tax amount that is being credited.</span></span>
- <span data-ttu-id="f9b30-117">之前已确认的基于产品的合同子项不会复制。</span><span class="sxs-lookup"><span data-stu-id="f9b30-117">Previously confirmed product-based contract lines are not copied over.</span></span> <span data-ttu-id="f9b30-118">不支持在基于产品的项目发票上处理更正。</span><span class="sxs-lookup"><span data-stu-id="f9b30-118">Processing corrections on a product-based project invoice is not supported.</span></span>
- <span data-ttu-id="f9b30-119">里程碑更正始终处理为完全贷记。</span><span class="sxs-lookup"><span data-stu-id="f9b30-119">Milestone corrections are always processed as full credits.</span></span>
- <span data-ttu-id="f9b30-120">如果客户开票的金额不正确，可以更正保留款或预付款金额。</span><span class="sxs-lookup"><span data-stu-id="f9b30-120">Retainer or advance amounts can be corrected if the customer was invoiced for an incorrect amount.</span></span>
- <span data-ttu-id="f9b30-121">如果使用了不正确的金额与之前确认的发票上的费用对帐，可以更正保留款或预付款的对帐。</span><span class="sxs-lookup"><span data-stu-id="f9b30-121">Reconciliations of retainers and advances can be corrected if an incorrect amount was used to reconcile against the charges on a previously confirmed invoice.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="f9b30-122">作为其他已开票费用的更正内容的发票明细详细信息，会将字段 **更正** 设置为 **是**。</span><span class="sxs-lookup"><span data-stu-id="f9b30-122">Invoice line details that are corrections to other already invoiced charges have the field **Correction** set to **Yes**.</span></span> <span data-ttu-id="f9b30-123">包含更正发票明细详细信息的发票具有名为 **具有更正** 的字段，此字段也会设置为 **是**。</span><span class="sxs-lookup"><span data-stu-id="f9b30-123">Invoices that have corrected invoice line details have a field called **Has corrections** that is also set to **Yes**.</span></span>

## <a name="actuals-created-on-confirmation-of-a-corrective-invoice"></a><span data-ttu-id="f9b30-124">确认纠正发票时创建的实际值：</span><span class="sxs-lookup"><span data-stu-id="f9b30-124">Actuals created on Confirmation of a corrective invoice:</span></span>

<span data-ttu-id="f9b30-125">以下是应用程序在确认之前，基于对草稿纠正发票执行的操作确认纠正时创建的实际值。</span><span class="sxs-lookup"><span data-stu-id="f9b30-125">Below are the actuals created by the application on confirmation of a corrective based on the operations performed on the draft corrective invoice before confirmation.</span></span>

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="216" valign="top">
                <p><span data-ttu-id="f9b30-126">
                    <strong>方案</strong>
                </span><span class="sxs-lookup"><span data-stu-id="f9b30-126">
                    <strong>Scenario</strong>
                </span></span></p>
            </td>
            <td width="808" valign="top">
                <p><span data-ttu-id="f9b30-127">
                    <strong>确认时创建的实际值</strong>
                </span><span class="sxs-lookup"><span data-stu-id="f9b30-127">
                    <strong>Actuals created on confirmation</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="4" valign="top">
                <p>
<span data-ttu-id="f9b30-128">确认已开票预付款或保留款的更正。<strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="f9b30-128">Confirm the correction of an invoiced advance or retainer.<strong></strong>
                </span></span></p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="f9b30-129">为对帐创建的保留款或预付款的未记帐销售额冲销。</span><span class="sxs-lookup"><span data-stu-id="f9b30-129">An unbilled sales reversal of the retainer or advance that was created for reconciliation.</span></span> <span data-ttu-id="f9b30-130">此金额为正值，因为它用于取消在对保留款或预付款开票时创建的负值。</span><span class="sxs-lookup"><span data-stu-id="f9b30-130">This amount is positive because it is meant to cancel out the negative that was created when the retainer or advance was invoiced.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="f9b30-131">将为保留款或预付款中的金额创建已记帐销售额冲销实际值，以冲销原始已记帐销售额。</span><span class="sxs-lookup"><span data-stu-id="f9b30-131">A billed sales reversal actual is created for the amount on the retainer or advance to reverse the original billed sales.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="f9b30-132">将为基于保留款或预付款的更正发票明细上的更正金额创建新的已记帐实际销售额。</span><span class="sxs-lookup"><span data-stu-id="f9b30-132">A new billed sales actual is created for the corrected amount on the retainer or advance-based corrected invoice line.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="f9b30-133">基于保留款或预付款的更正发票明细的负金额的未记帐实际销售额，将用于对帐。</span><span class="sxs-lookup"><span data-stu-id="f9b30-133">An unbilled sales actual of negative amount of the retainer or advance-based corrected invoice line, which will be used for reconciliation.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="4" valign="top">
                <p>
<span data-ttu-id="f9b30-134">确认之前对帐的保留款或预付款的更正。</span><span class="sxs-lookup"><span data-stu-id="f9b30-134">A confirmation of the correction of a previously reconciled retainer or advance.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="f9b30-135">为对帐创建的保留款或预付款的未记帐销售额冲销。</span><span class="sxs-lookup"><span data-stu-id="f9b30-135">An unbilled sales reversal of the retainer or advance that was created for reconciliation.</span></span> <span data-ttu-id="f9b30-136">此金额为正值，用于取消之前对帐发生时创建的负值。</span><span class="sxs-lookup"><span data-stu-id="f9b30-136">This amount is positive and is meant to cancel out the negative that was created when the previous reconciliation occurred.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="f9b30-137">之前发票上金额的已记帐销售额冲销实际值。</span><span class="sxs-lookup"><span data-stu-id="f9b30-137">A billed sales reversal actual for the amount on the previous invoice.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="f9b30-138">更正发票上应用的更正保留款金额的新的已记帐实际销售额。</span><span class="sxs-lookup"><span data-stu-id="f9b30-138">A new billed sales actual for the corrected retainer amount that is applied on the corrected invoice.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="f9b30-139">具有更正的剩余保留款或预付款的负金额的未记帐实际销售额，将用于以后发票的对帐。</span><span class="sxs-lookup"><span data-stu-id="f9b30-139">An unbilled sales actual with a negative amount from the corrected leftover retainer or advance, which will be used for reconciliation on later invoices.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="f9b30-140">为之前开票的时间交易的完全贷记开票。</span><span class="sxs-lookup"><span data-stu-id="f9b30-140">Invoicing the full credit of a previously invoiced time transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="f9b30-141">原始时间发票明细详细信息中时数和金额的已记帐销售额冲销。</span><span class="sxs-lookup"><span data-stu-id="f9b30-141">A billed sales reversal for the hours and amount on the original invoice line detail for time.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="f9b30-142">原始时间发票明细详细信息中时数和金额的新的未记帐实际销售额。</span><span class="sxs-lookup"><span data-stu-id="f9b30-142">A new unbilled sales actual for the hours and amount on the original invoice line detail for time.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="f9b30-143">为时间交易中的部分贷记开票。</span><span class="sxs-lookup"><span data-stu-id="f9b30-143">Invoicing the partial credit on a time transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="f9b30-144">原始时间发票明细详细信息中已开票时数和金额的已记帐销售额冲销。</span><span class="sxs-lookup"><span data-stu-id="f9b30-144">A billed sales reversal for the hours and amount invoiced on the original invoice line detail for time.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="f9b30-145">编辑的发票明细详细信息中的时数和金额应计费的新未记帐实际销售额，此实际销售额的冲销和相等的已记帐实际销售额。</span><span class="sxs-lookup"><span data-stu-id="f9b30-145">A new unbilled sales actual that is chargeable for the hours and amount on the edited invoice line detail, a reversal of this, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="f9b30-146">扣除发票明细详细信息中的更正数字后，剩余时数和金额应计费的新的未记帐实际销售额。</span><span class="sxs-lookup"><span data-stu-id="f9b30-146">A new unbilled sales actual that is chargeable for the remaining hours and amount after deducting the corrected figures on the invoice line detail.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="f9b30-147">为之前开票的支出交易的完全贷记开票。</span><span class="sxs-lookup"><span data-stu-id="f9b30-147">Invoicing the full credit of a previously invoiced expense transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="f9b30-148">原始支出发票明细详细信息中数量和金额的已记帐销售额冲销。</span><span class="sxs-lookup"><span data-stu-id="f9b30-148">A billed sales reversal for the quantity and amount on the original invoice line detail for the expense.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="f9b30-149">原始支出发票明细详细信息中数量和金额的新的未记帐实际销售额。</span><span class="sxs-lookup"><span data-stu-id="f9b30-149">A new unbilled sales actual for the quantity and amount on the original invoice line detail for the expense.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="f9b30-150">为之前开票的支出交易的部分贷记开票。</span><span class="sxs-lookup"><span data-stu-id="f9b30-150">Invoicing the partial credit of a previously invoiced expense transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="f9b30-151">原始支出发票明细详细信息中已开票数量和金额的已记帐销售额冲销。</span><span class="sxs-lookup"><span data-stu-id="f9b30-151">A billed sales reversal for the quantity and amount invoiced on the original invoice line detail for an expense.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="f9b30-152">更正后的发票明细详细信息中的数量和金额应计费的新未记帐实际销售额，此实际销售额的冲销和相等的已记帐实际销售额。</span><span class="sxs-lookup"><span data-stu-id="f9b30-152">A new unbilled sales actual that is chargeable for the quantity and amount on the corrected invoice line detail, a reversal of this, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="f9b30-153">扣除发票明细详细信息中的更正数字后，剩余数量和金额应计费的新的未记帐实际销售额。</span><span class="sxs-lookup"><span data-stu-id="f9b30-153">A new unbilled sales actual that is chargeable for the remaining quantity and amount after deducting the corrected figures on the invoice line detail.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="f9b30-154">为之前开票的费用交易的完全贷记开票。</span><span class="sxs-lookup"><span data-stu-id="f9b30-154">Invoicing the full credit of a previously invoiced fee transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="f9b30-155">原始费用发票明细详细信息中数量和金额的已记帐销售额冲销。</span><span class="sxs-lookup"><span data-stu-id="f9b30-155">A billed sales reversal for the quantity and amount on the original invoice line detail for the fee.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="f9b30-156">原始费用发票明细详细信息中数量和金额的新的未记帐实际销售额。</span><span class="sxs-lookup"><span data-stu-id="f9b30-156">A new unbilled sales actual for the quantity and amount on the original invoice line detail for the fee.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="f9b30-157">为之前开票的费用交易的部分贷记开票。</span><span class="sxs-lookup"><span data-stu-id="f9b30-157">Invoicing the partial credit of a previously invoiced fee transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="f9b30-158">原始费用发票明细详细信息中已开票数量和金额的已记帐销售额冲销。</span><span class="sxs-lookup"><span data-stu-id="f9b30-158">A billed sales reversal for the quantity and amount invoiced on the original invoice line detail for fee.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="f9b30-159">编辑后的纠正发票明细详细信息中的数量和金额应计费的新未记帐实际销售额，此实际销售额的冲销和相等的已记帐实际销售额。</span><span class="sxs-lookup"><span data-stu-id="f9b30-159">A new unbilled sales actual that is chargeable for the quantity and amount on the edited corrective invoice line detail, a reversal of this, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="f9b30-160">为之前开票的里程碑的完全贷记开票。</span><span class="sxs-lookup"><span data-stu-id="f9b30-160">Invoicing the full credit of a previously invoiced milestone.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="f9b30-161">原始里程碑发票明细详细信息中金额的已记帐销售额冲销。</span><span class="sxs-lookup"><span data-stu-id="f9b30-161">A billed sales reversal for the amount on the original invoice line detail for the milestone.</span></span>
                </p>
                <p>
<span data-ttu-id="f9b30-162">项目合同子项上的里程碑发票或记帐状态将更新为 **可开票**。</span><span class="sxs-lookup"><span data-stu-id="f9b30-162">The milestone invoice or billing status on the project contract line is updated to **Ready to Invoice**.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="f9b30-163">为之前开票的里程碑的部分贷记开票。</span><span class="sxs-lookup"><span data-stu-id="f9b30-163">Invoicing the partial credit of a previously invoiced milestone.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="f9b30-164">不支持</span><span class="sxs-lookup"><span data-stu-id="f9b30-164">Unsupported</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="f9b30-165">之前已开票的基于产品的合同子项的贷记和更正。</span><span class="sxs-lookup"><span data-stu-id="f9b30-165">Credits and corrections of a previously invoiced product-based contract line.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="f9b30-166">不支持</span><span class="sxs-lookup"><span data-stu-id="f9b30-166">Unsupported</span></span> </p>
            </td>
        </tr>
    </tbody>
</table>
