---
title: 更正基于项目的发票
description: 本主题提供关于如何在 Project Operations 中创建并确认基于项目的更正发票的信息。
author: rumant
ms.date: 03/29/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: f6b6670f823577bf7f784443f97f0b77e1e9a6aa
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/10/2021
ms.locfileid: "6012260"
---
# <a name="corrective-project-based-invoices"></a><span data-ttu-id="c9d30-103">更正基于项目的发票</span><span class="sxs-lookup"><span data-stu-id="c9d30-103">Corrective project-based invoices</span></span>

<span data-ttu-id="c9d30-104">_**适用于：** 面向资源/非库存场景的 Project Operations_</span><span class="sxs-lookup"><span data-stu-id="c9d30-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="c9d30-105">确认的项目发票可以更正以处理与客户和项目经理协商的变更或贷记。</span><span class="sxs-lookup"><span data-stu-id="c9d30-105">A confirmed project invoice can be corrected to process changes or credits as negotiated with the customer and project manager.</span></span>

<span data-ttu-id="c9d30-106">若要对已确认的发票进行编辑，请打开已确认的发票，选择 **更正此发票**。</span><span class="sxs-lookup"><span data-stu-id="c9d30-106">To make edits to a confirmed invoice, open the confirmed invoice and select **Correct this Invoice**.</span></span> 

> [!NOTE]
> <span data-ttu-id="c9d30-107">除非已确认项目发票，或者基于项目的发票具有预付款或保留款，或具有预付款或保留款的对帐信息，否则将无法进行此选择。</span><span class="sxs-lookup"><span data-stu-id="c9d30-107">This selection isn't available unless a project invoice is confirmed or the project-based invoice has advances or retainers or reconciliations of advances or retainers.</span></span>

<span data-ttu-id="c9d30-108">将从已确认的发票创建新的草稿发票。</span><span class="sxs-lookup"><span data-stu-id="c9d30-108">A new draft invoice is created from the confirmed invoice.</span></span> <span data-ttu-id="c9d30-109">之前已确认发票中的所有发票明细详细信息将被复制到新的草稿发票。</span><span class="sxs-lookup"><span data-stu-id="c9d30-109">All invoice line details from the previously confirmed invoice are copied to the new draft.</span></span> <span data-ttu-id="c9d30-110">以下是用于了解新的更正发票上的明细详细信息的一些要点：</span><span class="sxs-lookup"><span data-stu-id="c9d30-110">The following are some of the key points to understand about the line details on the new corrected invoice:</span></span>

- <span data-ttu-id="c9d30-111">所有数量都更新为零。</span><span class="sxs-lookup"><span data-stu-id="c9d30-111">All quantities are updated to zero.</span></span> <span data-ttu-id="c9d30-112">Dynamics 365 Project Operations 假定已开发票的所有项目已全部贷记。</span><span class="sxs-lookup"><span data-stu-id="c9d30-112">Dynamics 365 Project Operations assumes that all invoiced items are fully credited.</span></span> <span data-ttu-id="c9d30-113">如果需要，您可以手动更新这些数量以反映要开票的数量，而不是要贷记的数量。</span><span class="sxs-lookup"><span data-stu-id="c9d30-113">If needed, you can manually update these quantities to reflect the quantity that is being invoiced, and not the quantity that is being credited.</span></span> <span data-ttu-id="c9d30-114">根据您输入的数量，应用程序将计算贷记的数量。</span><span class="sxs-lookup"><span data-stu-id="c9d30-114">Based on the quantity you enter, the application calculates the credited quantity.</span></span> <span data-ttu-id="c9d30-115">在确认更正发票时，此金额会反映在创建的实际值中。</span><span class="sxs-lookup"><span data-stu-id="c9d30-115">This amount is reflected in the actuals that are created when the corrected invoice is confirmed.</span></span> <span data-ttu-id="c9d30-116">如果您要更改税额，必须输入正确的税额，而不是要贷记的税额。</span><span class="sxs-lookup"><span data-stu-id="c9d30-116">If you are making changes to the tax amount, you must enter the correct tax amount and not the tax amount that is being credited.</span></span>
- <span data-ttu-id="c9d30-117">里程碑更正始终处理为完全贷记。</span><span class="sxs-lookup"><span data-stu-id="c9d30-117">Milestone corrections are always processed as full credits.</span></span>


> [!IMPORTANT]
> <span data-ttu-id="c9d30-118">对于用于更正其他已开票费用的发票明细详细信息，**更正** 字段设置为 **是**。</span><span class="sxs-lookup"><span data-stu-id="c9d30-118">For invoice line details that are corrections to other already invoiced charges, the **Correction** field is set to **Yes**.</span></span> <span data-ttu-id="c9d30-119">对于具有更正的发票明细详细信息的发票，**具有更正** 字段设置为 **是**。</span><span class="sxs-lookup"><span data-stu-id="c9d30-119">For invoices that have corrected invoice line details, the **Has corrections** field is set to **Yes**.</span></span>

## <a name="actuals-created-when-a-corrective-invoice-is-confirmed"></a><span data-ttu-id="c9d30-120">确认更正发票后创建的实际值</span><span class="sxs-lookup"><span data-stu-id="c9d30-120">Actuals created when a corrective invoice is confirmed</span></span>

<span data-ttu-id="c9d30-121">下表列出了确认纠正发票后创建的实际值。</span><span class="sxs-lookup"><span data-stu-id="c9d30-121">The following table lists the actuals that are created when a corrective invoice is confirmed.</span></span>

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="216" valign="top">
                <p><span data-ttu-id="c9d30-122">
                    <strong>方案</strong>
                </span><span class="sxs-lookup"><span data-stu-id="c9d30-122">
                    <strong>Scenario</strong>
                </span></span></p>
            </td>
            <td width="808" valign="top">
                <p><span data-ttu-id="c9d30-123">
                    <strong>确认时创建的实际值</strong>
                </span><span class="sxs-lookup"><span data-stu-id="c9d30-123">
                    <strong>Actuals created on confirmation</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="c9d30-124">为之前开票的时间交易的完全贷记开票。</span><span class="sxs-lookup"><span data-stu-id="c9d30-124">Invoicing the full credit of a previously invoiced time transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="c9d30-125">原始时间发票明细详细信息中时数和金额的已记帐销售额冲销。</span><span class="sxs-lookup"><span data-stu-id="c9d30-125">A billed sales reversal for the hours and amount on the original invoice line detail for time.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="c9d30-126">原始时间发票明细详细信息中时数和金额的新的未记帐实际销售额。</span><span class="sxs-lookup"><span data-stu-id="c9d30-126">A new unbilled sales actual for the hours and amount on the original invoice line detail for time.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="c9d30-127">为时间交易中的部分贷记开票。</span><span class="sxs-lookup"><span data-stu-id="c9d30-127">Invoicing the partial credit on a time transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="c9d30-128">原始时间发票明细详细信息中已开票时数和金额的已记帐销售额冲销。</span><span class="sxs-lookup"><span data-stu-id="c9d30-128">A billed sales reversal for the hours and amount invoiced on the original invoice line detail for time.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="c9d30-129">编辑的发票明细详细信息中的时数和金额应计费的新未记帐实际销售额，此实际销售额的冲销和相等的已记帐实际销售额。</span><span class="sxs-lookup"><span data-stu-id="c9d30-129">A new unbilled sales actual that is chargeable for the hours and amount on the edited invoice line detail, a reversal of this, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="c9d30-130">扣除发票明细详细信息中的更正数字后，剩余时数和金额应计费的新的未记帐实际销售额。</span><span class="sxs-lookup"><span data-stu-id="c9d30-130">A new unbilled sales actual that is chargeable for the remaining hours and amount after deducting the corrected figures on the invoice line detail.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="c9d30-131">为之前开票的支出交易的完全贷记开票。</span><span class="sxs-lookup"><span data-stu-id="c9d30-131">Invoicing the full credit of a previously invoiced expense transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="c9d30-132">原始支出发票明细详细信息中数量和金额的已记帐销售额冲销。</span><span class="sxs-lookup"><span data-stu-id="c9d30-132">A billed sales reversal for the quantity and amount on the original invoice line detail for the expense.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="c9d30-133">原始支出发票明细详细信息中数量和金额的新的未记帐实际销售额。</span><span class="sxs-lookup"><span data-stu-id="c9d30-133">A new unbilled sales actual for the quantity and amount on the original invoice line detail for the expense.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="c9d30-134">为之前开票的支出交易的部分贷记开票。</span><span class="sxs-lookup"><span data-stu-id="c9d30-134">Invoicing the partial credit of a previously invoiced expense transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="c9d30-135">原始支出发票明细详细信息中已开票数量和金额的已记帐销售额冲销。</span><span class="sxs-lookup"><span data-stu-id="c9d30-135">A billed sales reversal for the quantity and amount invoiced on the original invoice line detail for an expense.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="c9d30-136">更正后的发票明细详细信息中的数量和金额应计费的新未记帐实际销售额，此实际销售额的冲销和相等的已记帐实际销售额。</span><span class="sxs-lookup"><span data-stu-id="c9d30-136">A new unbilled sales actual that is chargeable for the quantity and amount on the corrected invoice line detail, a reversal of this, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="c9d30-137">扣除发票明细详细信息中的更正数字后，剩余数量和金额应计费的新的未记帐实际销售额。</span><span class="sxs-lookup"><span data-stu-id="c9d30-137">A new unbilled sales actual that is chargeable for the remaining quantity and amount after deducting the corrected figures on the invoice line detail.</span></span>
                </p>
            </td>
        </tr>
                <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="c9d30-138">对先前已开票材料交易的全部贷记开具发票。</span><span class="sxs-lookup"><span data-stu-id="c9d30-138">Invoicing the full credit of a previously invoiced material transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="c9d30-139">原始材料发票明细详细信息中数量和金额的记帐销售冲销。</span><span class="sxs-lookup"><span data-stu-id="c9d30-139">A billed sales reversal for the quantity and amount on the original invoice line detail for material.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="c9d30-140">原始材料发票明细详细信息中数量和金额的新未记帐销售实际值。</span><span class="sxs-lookup"><span data-stu-id="c9d30-140">A new unbilled sales actual for the quantity and amount on the original invoice line detail for material.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="c9d30-141">对材料交易上的部分贷记开具发票。</span><span class="sxs-lookup"><span data-stu-id="c9d30-141">Invoicing the partial credit on a material transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="c9d30-142">原始材料发票明细详细信息中开票的数量和金额的记帐销售冲销。</span><span class="sxs-lookup"><span data-stu-id="c9d30-142">A billed sales reversal for the quantity and amount invoiced on the original invoice line detail for material.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="c9d30-143">一个新的未记帐销售实际值，对于编辑的发票明行明细上的数量和金额、其冲销和等值的已记帐销售实际值，该未记帐销售实际值为非应计费。</span><span class="sxs-lookup"><span data-stu-id="c9d30-143">A new unbilled sales actual that is chargeable for the quantity and amount on the edited invoice line detail, a reversal of this, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="c9d30-144">扣除发票明细详细信息中的更正数字后，剩余数量和金额应计费的新的未记帐实际销售额。</span><span class="sxs-lookup"><span data-stu-id="c9d30-144">A new unbilled sales actual that is chargeable for the remaining quantity and amount after deducting the corrected figures on the invoice line detail.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="c9d30-145">为之前开票的费用交易的完全贷记开票。</span><span class="sxs-lookup"><span data-stu-id="c9d30-145">Invoicing the full credit of a previously invoiced fee transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="c9d30-146">原始费用发票明细详细信息中数量和金额的已记帐销售额冲销。</span><span class="sxs-lookup"><span data-stu-id="c9d30-146">A billed sales reversal for the quantity and amount on the original invoice line detail for the fee.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="c9d30-147">原始费用发票明细详细信息中数量和金额的新的未记帐实际销售额。</span><span class="sxs-lookup"><span data-stu-id="c9d30-147">A new unbilled sales actual for the quantity and amount on the original invoice line detail for the fee.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="c9d30-148">为之前开票的费用交易的部分贷记开票。</span><span class="sxs-lookup"><span data-stu-id="c9d30-148">Invoicing the partial credit of a previously invoiced fee transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="c9d30-149">原始费用发票明细详细信息中已开票数量和金额的已记帐销售额冲销。</span><span class="sxs-lookup"><span data-stu-id="c9d30-149">A billed sales reversal for the quantity and amount invoiced on the original invoice line detail for fee.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="c9d30-150">编辑后的纠正发票明细详细信息中的数量和金额应计费的新未记帐实际销售额，此实际销售额的冲销和相等的已记帐实际销售额。</span><span class="sxs-lookup"><span data-stu-id="c9d30-150">A new unbilled sales actual that is chargeable for the quantity and amount on the edited corrective invoice line detail, a reversal of this, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="c9d30-151">为之前开票的里程碑的完全贷记开票。</span><span class="sxs-lookup"><span data-stu-id="c9d30-151">Invoicing the full credit of a previously invoiced milestone.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="c9d30-152">原始里程碑发票明细详细信息中金额的已记帐销售额冲销。</span><span class="sxs-lookup"><span data-stu-id="c9d30-152">A billed sales reversal for the amount on the original invoice line detail for the milestone.</span></span>
                </p>
                <p>
<span data-ttu-id="c9d30-153">里程碑的发票状态从<b>客户发票已过帐</b>更新为<b>已准备好开单</b>。</span><span class="sxs-lookup"><span data-stu-id="c9d30-153">The invoice status of the milestone is updated from <b>Customer Invoice Posted</b> to <b>Ready to Invoice</b>.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="c9d30-154">为之前开票的里程碑的部分贷记开票。</span><span class="sxs-lookup"><span data-stu-id="c9d30-154">Invoicing the partial credit of a previously invoiced milestone.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="c9d30-155">不支持这种情况。</span><span class="sxs-lookup"><span data-stu-id="c9d30-155">This scenario isn't supported.</span></span>
                </p>
            </td>
        </tr>       
    </tbody>
</table>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
