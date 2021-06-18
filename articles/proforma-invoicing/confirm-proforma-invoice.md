---
title: 确认估价基于项目的发票
description: 此主题提供有关确认估价基于项目的发票的信息。
author: rumant
ms.date: 04/05/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 1e4591d97e9d895dade42b2bcce57f22208cba96
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/10/2021
ms.locfileid: "6012125"
---
# <a name="confirm-a-proforma-project-based-invoice"></a><span data-ttu-id="c7a58-103">确认估价基于项目的发票</span><span class="sxs-lookup"><span data-stu-id="c7a58-103">Confirm a proforma project-based invoice</span></span>

<span data-ttu-id="c7a58-104">_**适用于：** 面向资源/非库存场景的 Project Operations_</span><span class="sxs-lookup"><span data-stu-id="c7a58-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="c7a58-105">估价发票确认后，项目发票的状态将更新为 **已确认**。</span><span class="sxs-lookup"><span data-stu-id="c7a58-105">After a proforma invoice is confirmed, the status of the project invoice updates to **Confirmed**.</span></span> <span data-ttu-id="c7a58-106">发票确认后，将变为只读。</span><span class="sxs-lookup"><span data-stu-id="c7a58-106">When an invoice is confirmed, it becomes read-only.</span></span> <span data-ttu-id="c7a58-107">今后，仅当有客户发起的更正或信用额度时，才可以更正发票。</span><span class="sxs-lookup"><span data-stu-id="c7a58-107">Going forward, the invoice can only be corrected if there are any customer-initiated corrections or credits.</span></span>

<span data-ttu-id="c7a58-108">下表列出了系统创建的实际值。</span><span class="sxs-lookup"><span data-stu-id="c7a58-108">The following table lists the actuals created by the system.</span></span> <span data-ttu-id="c7a58-109">在确认草稿项目发票之前对草稿项目发票执行某些操作时会创建这些实际值。</span><span class="sxs-lookup"><span data-stu-id="c7a58-109">These actuals are created when certain operations are performed on the draft project invoice before it is confirmed.</span></span>

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="216" valign="top">
                <p><span data-ttu-id="c7a58-110">
                    <strong>方案</strong>
                </span><span class="sxs-lookup"><span data-stu-id="c7a58-110">
                    <strong>Scenario</strong>
                </span></span></p>
            </td>
            <td width="808" valign="top">
                <p><span data-ttu-id="c7a58-111">
                    <strong>确认时创建的实际值</strong>
                </span><span class="sxs-lookup"><span data-stu-id="c7a58-111">
                    <strong>Actuals created on confirmation</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="c7a58-112">为预付款或保留款开票</span><span class="sxs-lookup"><span data-stu-id="c7a58-112">Invoicing an advance or retainer</span></span> </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="c7a58-113">对于预付款或保留款中的金额，将创建类型为<strong>保留款</strong>的已记帐实际销售额。</span><span class="sxs-lookup"><span data-stu-id="c7a58-113">A billed sales actual of type, <strong>Retainer</strong> is created for the amount on the advance or retainer.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="c7a58-114">用于对帐的保留款或预付款为负金额的未记帐销售实际值。</span><span class="sxs-lookup"><span data-stu-id="c7a58-114">An unbilled sales actual with a negative amount of the retainer or advance to be used for reconciliation.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="c7a58-115">对发票上的保留款或预付款完全对帐之后。</span><span class="sxs-lookup"><span data-stu-id="c7a58-115">After fully reconciling a retainer or advance on an invoice.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="c7a58-116">为对帐创建的保留款或预付款的未记帐销售额冲销。</span><span class="sxs-lookup"><span data-stu-id="c7a58-116">An unbilled sales reversal of the retainer or advance that was created for reconciliation.</span></span> <span data-ttu-id="c7a58-117">此金额为正值，因为它用于取消在对保留款或预付款开票时创建的负值。</span><span class="sxs-lookup"><span data-stu-id="c7a58-117">This amount is positive as it's meant to cancel out the negative that was created when the retainer or advance was invoiced.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="c7a58-118">此发票上金额的已记帐实际销售额。</span><span class="sxs-lookup"><span data-stu-id="c7a58-118">A billed sales actual for the amount on this invoice.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="c7a58-119">对发票上的保留款或预付款部分对帐之后。</span><span class="sxs-lookup"><span data-stu-id="c7a58-119">After partially reconciling a retainer or advance on an invoice.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="c7a58-120">为对帐创建的保留款或预付款的未记帐销售额冲销。</span><span class="sxs-lookup"><span data-stu-id="c7a58-120">An unbilled sales reversal of the retainer or advance that was created for reconciliation.</span></span> <span data-ttu-id="c7a58-121">此金额为正值，因为它用于取消在对保留款或预付款开票时创建的负值。</span><span class="sxs-lookup"><span data-stu-id="c7a58-121">This amount is positive as it's meant to cancel out the negative that was created when the retainer or advance was invoiced.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="c7a58-122">此发票上金额的已记帐实际销售额。</span><span class="sxs-lookup"><span data-stu-id="c7a58-122">A billed sales actual for the amount on this invoice.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="c7a58-123">要用于对未来发票进行对帐的剩余保留款或预付款金额的负未记帐实际销售额。</span><span class="sxs-lookup"><span data-stu-id="c7a58-123">A negative unbilled sales actual of the remaining retainer or advance amount to be used for reconciliation on future invoices.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="c7a58-124">为草稿发票未进行任何编辑的时间交易开票。</span><span class="sxs-lookup"><span data-stu-id="c7a58-124">Invoicing a time transaction without any edits on the draft invoice.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="c7a58-125">原始时间审批中时数和金额的未记帐销售额冲销。</span><span class="sxs-lookup"><span data-stu-id="c7a58-125">An unbilled sales reversal for the hours and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="c7a58-126">原始时间审批中时数和金额的已记帐实际销售额。</span><span class="sxs-lookup"><span data-stu-id="c7a58-126">A billed sales actual for the hours and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="c7a58-127">为进行了编辑以减少数量的时间交易开票。</span><span class="sxs-lookup"><span data-stu-id="c7a58-127">Invoicing a time transaction that was edited to reduce the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="c7a58-128">原始时间审批中时数和金额的未记帐销售额冲销。</span><span class="sxs-lookup"><span data-stu-id="c7a58-128">An unbilled sales reversal for the hours and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="c7a58-129">编辑的发票明细详细信息中的时数和金额应计费的新未记帐实际销售额，实际销售额的冲销和相等的已记帐实际销售额。</span><span class="sxs-lookup"><span data-stu-id="c7a58-129">A new unbilled sales actual that is chargeable for the hours and amount on the edited invoice line detail, a reversal of the sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="c7a58-130">一个新的未记帐销售实际值，在减去编辑的发票明行明细上的更正数字、销售实际值冲销和等值的已记帐销售实际值后，该未记帐销售实际值为非应计费。</span><span class="sxs-lookup"><span data-stu-id="c7a58-130">A new unbilled sales actual that is non-chargeable for the remaining hours and amount after deducting the corrected figures on the edited invoice line detail, a reversal of the sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="c7a58-131">为进行了编辑以增加数量的时间交易开票。</span><span class="sxs-lookup"><span data-stu-id="c7a58-131">Invoicing a time transaction that was edited to increase the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="c7a58-132">原始时间审批中时数和金额的未记帐销售额冲销。</span><span class="sxs-lookup"><span data-stu-id="c7a58-132">An unbilled sales reversal for the hours and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="c7a58-133">编辑的发票明细详细信息中的时数和金额应计费的新未记帐实际销售额，未记帐实际销售额的冲销和相等的已记帐实际销售额。</span><span class="sxs-lookup"><span data-stu-id="c7a58-133">A new unbilled sales actual that is chargeable for the hours and amount on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="c7a58-134">为草稿发票未进行任何编辑的支出交易开票。</span><span class="sxs-lookup"><span data-stu-id="c7a58-134">Invoicing an expense transaction without any edits on the draft invoice.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="c7a58-135">原始支出审批中数量和金额的未记帐销售额冲销。</span><span class="sxs-lookup"><span data-stu-id="c7a58-135">An unbilled sales reversal for the quantity and amount on the original expense approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="c7a58-136">原始支出审批中数量和金额的已记帐实际销售额。</span><span class="sxs-lookup"><span data-stu-id="c7a58-136">A billed sales actual for the quantity and amount on the original expense approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="c7a58-137">为进行了编辑以减少数量的支出交易开票。</span><span class="sxs-lookup"><span data-stu-id="c7a58-137">Invoicing an expense transaction that was edited to reduce the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="c7a58-138">原始支出审批中数量和金额的未记帐销售额冲销。</span><span class="sxs-lookup"><span data-stu-id="c7a58-138">An unbilled sales reversal for the quantity and amount on the original expense approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="c7a58-139">编辑的发票明细详细信息中的数量和金额应计费的新未记帐实际销售额，未记帐实际销售额的冲销和相等的已记帐实际销售额。</span><span class="sxs-lookup"><span data-stu-id="c7a58-139">A new unbilled sales actual that is chargeable for the quantity and amount on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="c7a58-140">编辑的发票明细详细信息中扣除更正的数字后剩余数量不应计费的新未记帐实际销售额，未记帐实际销售额的冲销和相等的已记帐实际销售额。</span><span class="sxs-lookup"><span data-stu-id="c7a58-140">A new unbilled sales actual that is non-chargeable for the remaining quantity and amount after deducting the corrected figures on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="c7a58-141">为进行了编辑以增加数量的支出交易开票。</span><span class="sxs-lookup"><span data-stu-id="c7a58-141">Invoicing an expense transaction that was edited to increase the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="c7a58-142">原始支出审批中数量和金额的未记帐销售额冲销。</span><span class="sxs-lookup"><span data-stu-id="c7a58-142">An unbilled sales reversal for the quantity and amount on the original expense approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="c7a58-143">编辑的发票明细详细信息中的数量和金额应计费的新未记帐实际销售额，未记帐实际销售额的冲销和相等的已记帐实际销售额。</span><span class="sxs-lookup"><span data-stu-id="c7a58-143">A new unbilled sales actual that is chargeable for quantity and amount on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span> 
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="c7a58-144">在未对草稿发票进行任何编辑的情况下对材料交易开具发票。</span><span class="sxs-lookup"><span data-stu-id="c7a58-144">Invoicing a material transaction without any edits on the draft invoice.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="c7a58-145">原始材料使用审批中数量和金额的未记帐销售冲销。</span><span class="sxs-lookup"><span data-stu-id="c7a58-145">An unbilled sales reversal for the quantity and amount on the original material usage approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="c7a58-146">原始材料使用审批中数量和金额的记帐销售实际值。</span><span class="sxs-lookup"><span data-stu-id="c7a58-146">A billed sales actual for the quantity and amount on the original material usage approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="c7a58-147">对为减少数量而编辑的材料交易开具发票。</span><span class="sxs-lookup"><span data-stu-id="c7a58-147">Invoicing a material transaction that was edited to reduce the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="c7a58-148">原始时间使用审批中数量和金额的未记帐销售冲销。</span><span class="sxs-lookup"><span data-stu-id="c7a58-148">An unbilled sales reversal for the quantity and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="c7a58-149">编辑的发票明细详细信息中的数量和金额应计费的新未记帐实际销售额，未记帐实际销售额的冲销和相等的已记帐实际销售额。</span><span class="sxs-lookup"><span data-stu-id="c7a58-149">A new unbilled sales actual that is chargeable for the quantity and amount on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="c7a58-150">编辑的发票明细详细信息中扣除更正的数字后剩余数量不应计费的新未记帐实际销售额，未记帐实际销售额的冲销和相等的已记帐实际销售额。</span><span class="sxs-lookup"><span data-stu-id="c7a58-150">A new unbilled sales actual that is non-chargeable for the remaining quantity and amount after deducting the corrected figures on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="c7a58-151">对为增加数量而编辑的材料交易开具发票。</span><span class="sxs-lookup"><span data-stu-id="c7a58-151">Invoicing a material transaction that was edited to increase the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="c7a58-152">原始材料使用审批中数量和金额的未记帐销售冲销。</span><span class="sxs-lookup"><span data-stu-id="c7a58-152">An unbilled sales reversal for the quantity and amount on the original material usage approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="c7a58-153">编辑的发票明细详细信息中的数量和金额应计费的新未记帐实际销售额，未记帐实际销售额的冲销和相等的已记帐实际销售额。</span><span class="sxs-lookup"><span data-stu-id="c7a58-153">A new unbilled sales actual that is chargeable for the quantity and amount on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="c7a58-154">为费用开票。</span><span class="sxs-lookup"><span data-stu-id="c7a58-154">Invoicing a fee.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="c7a58-155">原始日记帐行中费用金额的未记帐销售额冲销。</span><span class="sxs-lookup"><span data-stu-id="c7a58-155">An unbilled sales reversal for the fee amount on the original journal line.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="c7a58-156">原始费用日记帐行中数量和金额的已记帐实际销售额。</span><span class="sxs-lookup"><span data-stu-id="c7a58-156">A billed sales actual for the quantity and amount on the original fee journal line.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="c7a58-157">为里程碑开票。</span><span class="sxs-lookup"><span data-stu-id="c7a58-157">Invoicing a milestone.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="c7a58-158">项目合同子项上原始里程碑上的里程碑金额的已记帐实际销售额。</span><span class="sxs-lookup"><span data-stu-id="c7a58-158">A billed sales actual for the milestone amount on the original milestone on the project contract line.</span></span>
                </p>
            </td>
        </tr>
       
    </tbody>
</table>

[!INCLUDE[footer-include](../includes/footer-banner.md)]
