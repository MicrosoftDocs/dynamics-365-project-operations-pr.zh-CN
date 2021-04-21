---
title: 创建更正基于项目的发票
description: 此主题提供有关 Project Operations 的更正发票的信息。
author: rumant
manager: Annbe
ms.date: 03/29/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 32772d64b3fc77f0af9618edff40e3b295593454
ms.sourcegitcommit: 504c09365bf404c1f1aa9b5034c1e1e5bc9d0d54
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/31/2021
ms.locfileid: "5788836"
---
# <a name="create-corrective-project-based-invoices"></a><span data-ttu-id="2d5d6-103">创建更正基于项目的发票</span><span class="sxs-lookup"><span data-stu-id="2d5d6-103">Create corrective project-based invoices</span></span> 

<span data-ttu-id="2d5d6-104">_**适用于：** 面向资源/非库存场景的 Project Operations_</span><span class="sxs-lookup"><span data-stu-id="2d5d6-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="2d5d6-105">确认的项目发票可以更正以处理与客户和项目经理协商的变更或贷记。</span><span class="sxs-lookup"><span data-stu-id="2d5d6-105">A confirmed project invoice can be corrected to process changes or credits as negotiated with the customer and project manager.</span></span>

<span data-ttu-id="2d5d6-106">若要对已确认的发票进行编辑，请打开已确认的发票，选择 **更正此发票**。</span><span class="sxs-lookup"><span data-stu-id="2d5d6-106">To make edits to a confirmed invoice, open the confirmed invoice and select **Correct this Invoice**.</span></span> 

> [!NOTE]
> <span data-ttu-id="2d5d6-107">除非项目发票已确认，否则此选择不可用。</span><span class="sxs-lookup"><span data-stu-id="2d5d6-107">This selection isn't available unless a project invoice is confirmed.</span></span>

<span data-ttu-id="2d5d6-108">将从已确认的发票创建新的草稿发票。</span><span class="sxs-lookup"><span data-stu-id="2d5d6-108">A new draft invoice is created from the confirmed invoice.</span></span> <span data-ttu-id="2d5d6-109">之前已确认发票中的所有发票明细详细信息将被复制到新的草稿发票。</span><span class="sxs-lookup"><span data-stu-id="2d5d6-109">All invoice line details from the previously confirmed invoice are copied to the new draft.</span></span> <span data-ttu-id="2d5d6-110">以下是一些要点，可帮助您详细了解有关新更正发票的行详细信息：</span><span class="sxs-lookup"><span data-stu-id="2d5d6-110">The following are some key points to help you understand more about the line details on the new corrected invoice:</span></span>

- <span data-ttu-id="2d5d6-111">所有数量都更新为零。</span><span class="sxs-lookup"><span data-stu-id="2d5d6-111">All quantities are updated to zero.</span></span> <span data-ttu-id="2d5d6-112">这假定已开发票的所有项目已全部贷记。</span><span class="sxs-lookup"><span data-stu-id="2d5d6-112">This assumes that all invoiced items are fully credited.</span></span> <span data-ttu-id="2d5d6-113">如果需要，您可以手动更新这些数量以反映要开票的数量，而不是要贷记的数量。</span><span class="sxs-lookup"><span data-stu-id="2d5d6-113">If needed, you can manually update these quantities to reflect the quantity that is being invoiced, and not the quantity that is being credited.</span></span> <span data-ttu-id="2d5d6-114">根据您输入的数量，应用程序将计算贷记的数量。</span><span class="sxs-lookup"><span data-stu-id="2d5d6-114">Based on the quantity you enter, the application calculates the credited quantity.</span></span> <span data-ttu-id="2d5d6-115">在确认更正发票时，此金额会反映在创建的实际值中。</span><span class="sxs-lookup"><span data-stu-id="2d5d6-115">This amount is reflected in the actuals that are created when the corrected invoice is confirmed.</span></span> <span data-ttu-id="2d5d6-116">如果您要更改税额，必须输入正确的税额，而不是要贷记的税额。</span><span class="sxs-lookup"><span data-stu-id="2d5d6-116">If you are making changes to the tax amount, you must enter the correct tax amount and not the tax amount that is being credited.</span></span>
- <span data-ttu-id="2d5d6-117">里程碑更正始终处理为完全贷记。</span><span class="sxs-lookup"><span data-stu-id="2d5d6-117">Milestone corrections are always processed as full credits.</span></span>
- <span data-ttu-id="2d5d6-118">如果客户开票的金额不正确，可以更正保留款或预付款金额。</span><span class="sxs-lookup"><span data-stu-id="2d5d6-118">Retainer or advance amounts can be corrected if the customer was invoiced for an incorrect amount.</span></span>
- <span data-ttu-id="2d5d6-119">如果使用了不正确的金额与之前确认的发票上的费用对帐，可以更正保留款或预付款的对帐。</span><span class="sxs-lookup"><span data-stu-id="2d5d6-119">Reconciliations of retainers and advances can be corrected if an incorrect amount was used to reconcile against the charges on a previously confirmed invoice.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="2d5d6-120">用于更正其他已开票费用的发票明细详细信息的 **更正** 字段设置为 **是**。</span><span class="sxs-lookup"><span data-stu-id="2d5d6-120">Invoice line details that are corrections to other already invoiced charges have the **Correction** field set to **Yes**.</span></span> <span data-ttu-id="2d5d6-121">包含更正发票明细详细信息的发票具有名为 **具有更正** 的字段，此字段也会设置为 **是**。</span><span class="sxs-lookup"><span data-stu-id="2d5d6-121">Invoices that have corrected invoice line details have a field called **Has corrections** that is also set to **Yes**.</span></span>

## <a name="actuals-created-on-confirmation-of-a-corrective-invoice"></a><span data-ttu-id="2d5d6-122">确认纠正发票时创建的实际值</span><span class="sxs-lookup"><span data-stu-id="2d5d6-122">Actuals created on confirmation of a corrective invoice</span></span>

<span data-ttu-id="2d5d6-123">下表列出了确认纠正发票后创建的实际值。</span><span class="sxs-lookup"><span data-stu-id="2d5d6-123">The following table lists the actuals that are created when a corrective invoice is confirmed.</span></span>

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="216" valign="top">
                <p><span data-ttu-id="2d5d6-124">
                    <strong>方案</strong>
                </span><span class="sxs-lookup"><span data-stu-id="2d5d6-124">
                    <strong>Scenario</strong>
                </span></span></p>
            </td>
            <td width="808" valign="top">
                <p><span data-ttu-id="2d5d6-125">
                    <strong>确认时创建的实际值</strong>
                </span><span class="sxs-lookup"><span data-stu-id="2d5d6-125">
                    <strong>Actuals created on confirmation</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="4" valign="top">
                <p>
<span data-ttu-id="2d5d6-126">确认已开票预付款或保留款的更正。<strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="2d5d6-126">Confirm the correction of an invoiced advance or retainer.<strong></strong>
                </span></span></p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="2d5d6-127">为对帐创建的保留款或预付款的未记帐销售额冲销。</span><span class="sxs-lookup"><span data-stu-id="2d5d6-127">An unbilled sales reversal of the retainer or advance that was created for reconciliation.</span></span> <span data-ttu-id="2d5d6-128">此金额为正值，因为它用于取消在对保留款或预付款开票时创建的负值。</span><span class="sxs-lookup"><span data-stu-id="2d5d6-128">This amount is positive because it is meant to cancel out the negative that was created when the retainer or advance was invoiced.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="2d5d6-129">将为保留款或预付款中的金额创建已记帐销售额冲销实际值，以冲销原始已记帐销售额。</span><span class="sxs-lookup"><span data-stu-id="2d5d6-129">A billed sales reversal actual is created for the amount on the retainer or advance to reverse the original billed sales.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="2d5d6-130">将为基于保留款或预付款的更正发票明细上的更正金额创建新的已记帐实际销售额。</span><span class="sxs-lookup"><span data-stu-id="2d5d6-130">A new billed sales actual is created for the corrected amount on the retainer or advance-based corrected invoice line.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="2d5d6-131">基于保留款或预付款的更正发票明细的负金额的未记帐实际销售额，将用于对帐。</span><span class="sxs-lookup"><span data-stu-id="2d5d6-131">An unbilled sales actual of negative amount of the retainer or advance-based corrected invoice line, which will be used for reconciliation.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="4" valign="top">
                <p>
<span data-ttu-id="2d5d6-132">确认之前对帐的保留款或预付款的更正。</span><span class="sxs-lookup"><span data-stu-id="2d5d6-132">A confirmation of the correction of a previously reconciled retainer or advance.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="2d5d6-133">为对帐创建的保留款或预付款的未记帐销售额冲销。</span><span class="sxs-lookup"><span data-stu-id="2d5d6-133">An unbilled sales reversal of the retainer or advance that was created for reconciliation.</span></span> <span data-ttu-id="2d5d6-134">此金额为正值，用于取消之前对帐发生时创建的负值。</span><span class="sxs-lookup"><span data-stu-id="2d5d6-134">This amount is positive and is meant to cancel out the negative that was created when the previous reconciliation occurred.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="2d5d6-135">之前发票上金额的已记帐销售额冲销实际值。</span><span class="sxs-lookup"><span data-stu-id="2d5d6-135">A billed sales reversal actual for the amount on the previous invoice.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="2d5d6-136">更正发票上应用的更正保留款金额的新的已记帐实际销售额。</span><span class="sxs-lookup"><span data-stu-id="2d5d6-136">A new billed sales actual for the corrected retainer amount that is applied on the corrected invoice.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="2d5d6-137">具有更正的剩余保留款或预付款的负金额的未记帐实际销售额，将用于以后发票的对帐。</span><span class="sxs-lookup"><span data-stu-id="2d5d6-137">An unbilled sales actual with a negative amount from the corrected leftover retainer or advance, which will be used for reconciliation on later invoices.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="2d5d6-138">为之前开票的时间交易的完全贷记开票。</span><span class="sxs-lookup"><span data-stu-id="2d5d6-138">Invoicing the full credit of a previously invoiced time transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="2d5d6-139">原始时间发票明细详细信息中时数和金额的已记帐销售额冲销。</span><span class="sxs-lookup"><span data-stu-id="2d5d6-139">A billed sales reversal for the hours and amount on the original invoice line detail for time.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="2d5d6-140">原始时间发票明细详细信息中时数和金额的新的未记帐实际销售额。</span><span class="sxs-lookup"><span data-stu-id="2d5d6-140">A new unbilled sales actual for the hours and amount on the original invoice line detail for time.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="2d5d6-141">为时间交易中的部分贷记开票。</span><span class="sxs-lookup"><span data-stu-id="2d5d6-141">Invoicing the partial credit on a time transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="2d5d6-142">原始时间发票明细详细信息中已开票时数和金额的已记帐销售额冲销。</span><span class="sxs-lookup"><span data-stu-id="2d5d6-142">A billed sales reversal for the hours and amount invoiced on the original invoice line detail for time.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="2d5d6-143">编辑的发票明细详细信息中的时数和金额应计费的新未记帐实际销售额，此实际销售额的冲销和相等的已记帐实际销售额。</span><span class="sxs-lookup"><span data-stu-id="2d5d6-143">A new unbilled sales actual that is chargeable for the hours and amount on the edited invoice line detail, a reversal of this, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="2d5d6-144">扣除发票明细详细信息中的更正数字后，剩余时数和金额应计费的新的未记帐实际销售额。</span><span class="sxs-lookup"><span data-stu-id="2d5d6-144">A new unbilled sales actual that is chargeable for the remaining hours and amount after deducting the corrected figures on the invoice line detail.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="2d5d6-145">为之前开票的支出交易的完全贷记开票。</span><span class="sxs-lookup"><span data-stu-id="2d5d6-145">Invoicing the full credit of a previously invoiced expense transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="2d5d6-146">原始支出发票明细详细信息中数量和金额的已记帐销售额冲销。</span><span class="sxs-lookup"><span data-stu-id="2d5d6-146">A billed sales reversal for the quantity and amount on the original invoice line detail for the expense.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="2d5d6-147">原始支出发票明细详细信息中数量和金额的新的未记帐实际销售额。</span><span class="sxs-lookup"><span data-stu-id="2d5d6-147">A new unbilled sales actual for the quantity and amount on the original invoice line detail for the expense.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="2d5d6-148">为之前开票的支出交易的部分贷记开票。</span><span class="sxs-lookup"><span data-stu-id="2d5d6-148">Invoicing the partial credit of a previously invoiced expense transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="2d5d6-149">原始支出发票明细详细信息中已开票数量和金额的已记帐销售额冲销。</span><span class="sxs-lookup"><span data-stu-id="2d5d6-149">A billed sales reversal for the quantity and amount invoiced on the original invoice line detail for an expense.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="2d5d6-150">更正后的发票明细详细信息中的数量和金额应计费的新未记帐实际销售额，此实际销售额的冲销和相等的已记帐实际销售额。</span><span class="sxs-lookup"><span data-stu-id="2d5d6-150">A new unbilled sales actual that is chargeable for the quantity and amount on the corrected invoice line detail, a reversal of this, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="2d5d6-151">扣除发票明细详细信息中的更正数字后，剩余数量和金额应计费的新的未记帐实际销售额。</span><span class="sxs-lookup"><span data-stu-id="2d5d6-151">A new unbilled sales actual that is chargeable for the remaining quantity and amount after deducting the corrected figures on the invoice line detail.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="2d5d6-152">为之前开票的费用交易的完全贷记开票。</span><span class="sxs-lookup"><span data-stu-id="2d5d6-152">Invoicing the full credit of a previously invoiced fee transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="2d5d6-153">原始费用发票明细详细信息中数量和金额的已记帐销售额冲销。</span><span class="sxs-lookup"><span data-stu-id="2d5d6-153">A billed sales reversal for the quantity and amount on the original invoice line detail for the fee.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="2d5d6-154">原始费用发票明细详细信息中数量和金额的新的未记帐实际销售额。</span><span class="sxs-lookup"><span data-stu-id="2d5d6-154">A new unbilled sales actual for the quantity and amount on the original invoice line detail for the fee.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="2d5d6-155">为之前开票的费用交易的部分贷记开票。</span><span class="sxs-lookup"><span data-stu-id="2d5d6-155">Invoicing the partial credit of a previously invoiced fee transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="2d5d6-156">原始费用发票明细详细信息中已开票数量和金额的已记帐销售额冲销。</span><span class="sxs-lookup"><span data-stu-id="2d5d6-156">A billed sales reversal for the quantity and amount invoiced on the original invoice line detail for fee.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="2d5d6-157">编辑后的纠正发票明细详细信息中的数量和金额应计费的新未记帐实际销售额，此实际销售额的冲销和相等的已记帐实际销售额。</span><span class="sxs-lookup"><span data-stu-id="2d5d6-157">A new unbilled sales actual that is chargeable for the quantity and amount on the edited corrective invoice line detail, a reversal of this, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="2d5d6-158">为之前开票的里程碑的完全贷记开票。</span><span class="sxs-lookup"><span data-stu-id="2d5d6-158">Invoicing the full credit of a previously invoiced milestone.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="2d5d6-159">原始里程碑发票明细详细信息中金额的已记帐销售额冲销。</span><span class="sxs-lookup"><span data-stu-id="2d5d6-159">A billed sales reversal for the amount on the original invoice line detail for the milestone.</span></span>
                </p>
                <p>
<span data-ttu-id="2d5d6-160">里程碑上的发票状态从<b>客户发票已过帐</b>更新为<b>已准备好开单</b>。</span><span class="sxs-lookup"><span data-stu-id="2d5d6-160">The invoice status on the milestone is updated from <b>Customer invoice posted</b> to <b>Ready to Invoice</b>.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="2d5d6-161">为之前开票的里程碑的部分贷记开票。</span><span class="sxs-lookup"><span data-stu-id="2d5d6-161">Invoicing the partial credit of a previously invoiced milestone.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="2d5d6-162">不支持</span><span class="sxs-lookup"><span data-stu-id="2d5d6-162">Unsupported</span></span> </p>
            </td>
        </tr>        
    </tbody>
</table>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
