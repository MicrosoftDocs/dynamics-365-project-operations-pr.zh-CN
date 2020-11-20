---
title: 确认估价发票 - 精简
description: 此主题提供有关在 Project Operations 中确认估价发票的信息。
author: rumant
manager: Annbe
ms.date: 10/13/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 02b671e4ad327b2448529d7119211613f3a9cb27
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/30/2020
ms.locfileid: "4176510"
---
# <a name="confirm-a-proforma-invoice---lite"></a><span data-ttu-id="7b29a-103">确认估价发票 - 精简</span><span class="sxs-lookup"><span data-stu-id="7b29a-103">Confirm a proforma invoice - lite</span></span>

<span data-ttu-id="7b29a-104">_**适用于：** 精简部署 - 估价交易开票_</span><span class="sxs-lookup"><span data-stu-id="7b29a-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="7b29a-105">估价发票确认后，项目发票的状态将更新为 **已确认**。</span><span class="sxs-lookup"><span data-stu-id="7b29a-105">After a proforma invoice is confirmed, the status of the project invoice updates to **Confirmed**.</span></span> <span data-ttu-id="7b29a-106">发票确认后，将变为只读。</span><span class="sxs-lookup"><span data-stu-id="7b29a-106">When an invoice is confirmed, it becomes read-only.</span></span> <span data-ttu-id="7b29a-107">之后，只有在发票标记为已支付的情况下，在有任何客户发起更正或贷记时才可以更正发票。</span><span class="sxs-lookup"><span data-stu-id="7b29a-107">Going forward, the invoice can only be corrected if there are any customer-initiated corrections or credits, of if the invoice is marked as paid.</span></span>

<span data-ttu-id="7b29a-108">下表列出了系统创建的实际值。</span><span class="sxs-lookup"><span data-stu-id="7b29a-108">The following table lists the actuals created by the system.</span></span> <span data-ttu-id="7b29a-109">在确认草稿项目发票之前对草稿项目发票执行某些操作时会创建这些实际值。</span><span class="sxs-lookup"><span data-stu-id="7b29a-109">These actuals are created when certain operations are performed on the draft project invoice before it is confirmed.</span></span>

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="216" valign="top">
                <p><span data-ttu-id="7b29a-110">
                    <strong>方案</strong>
                </span><span class="sxs-lookup"><span data-stu-id="7b29a-110">
                    <strong>Scenario</strong>
                </span></span></p>
            </td>
            <td width="808" valign="top">
                <p><span data-ttu-id="7b29a-111">
                    <strong>确认时创建的实际值</strong>
                </span><span class="sxs-lookup"><span data-stu-id="7b29a-111">
                    <strong>Actuals created on confirmation</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="7b29a-112">为预付款或保留款开票</span><span class="sxs-lookup"><span data-stu-id="7b29a-112">Invoicing an advance or retainer</span></span> </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="7b29a-113">对于预付款或保留款中的金额，将创建类型为<strong>保留款</strong>的已记帐实际销售额。</span><span class="sxs-lookup"><span data-stu-id="7b29a-113">A billed sales actual of type, <strong>Retainer</strong> is created for the amount on the advance or retainer.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="7b29a-114">要用于对帐的负保留款或预付款金额的未记帐实际销售额。</span><span class="sxs-lookup"><span data-stu-id="7b29a-114">An unbilled sales actual of a negative amount of the retainer or advance to be used for reconciliation.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="7b29a-115">对发票上的保留款或预付款完全对帐之后。</span><span class="sxs-lookup"><span data-stu-id="7b29a-115">After fully reconciling a retainer or advance on an invoice.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="7b29a-116">为对帐创建的保留款或预付款的未记帐销售额冲销。</span><span class="sxs-lookup"><span data-stu-id="7b29a-116">An unbilled sales reversal of the retainer or advance that was created for reconciliation.</span></span> <span data-ttu-id="7b29a-117">此金额为正值，因为它用于取消在对保留款或预付款开票时创建的负值。</span><span class="sxs-lookup"><span data-stu-id="7b29a-117">This amount is positive as it's meant to cancel out the negative that was created when the retainer or advance was invoiced.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="7b29a-118">此发票上金额的已记帐实际销售额。</span><span class="sxs-lookup"><span data-stu-id="7b29a-118">A billed sales actual for the amount on this invoice.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="7b29a-119">对发票上的保留款或预付款部分对帐之后。</span><span class="sxs-lookup"><span data-stu-id="7b29a-119">After partially reconciling a retainer or advance on an invoice.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="7b29a-120">为对帐创建的保留款或预付款的未记帐销售额冲销。</span><span class="sxs-lookup"><span data-stu-id="7b29a-120">An unbilled sales reversal of the retainer or advance that was created for reconciliation.</span></span> <span data-ttu-id="7b29a-121">此金额为正值，因为它用于取消在对保留款或预付款开票时创建的负值。</span><span class="sxs-lookup"><span data-stu-id="7b29a-121">This amount is positive as it's meant to cancel out the negative that was created when the retainer or advance was invoiced.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="7b29a-122">此发票上金额的已记帐实际销售额。</span><span class="sxs-lookup"><span data-stu-id="7b29a-122">A billed sales actual for the amount on this invoice.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="7b29a-123">要用于对未来发票进行对帐的剩余保留款或预付款金额的负未记帐实际销售额。</span><span class="sxs-lookup"><span data-stu-id="7b29a-123">A negative unbilled sales actual of the remaining retainer or advance amount to be used for reconciliation on future invoices.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="7b29a-124">为草稿发票未进行任何编辑的时间交易开票。</span><span class="sxs-lookup"><span data-stu-id="7b29a-124">Invoicing a time transaction without any edits on the draft invoice.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="7b29a-125">原始时间审批中时数和金额的未记帐销售额冲销。</span><span class="sxs-lookup"><span data-stu-id="7b29a-125">An unbilled sales reversal for the hours and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="7b29a-126">原始时间审批中时数和金额的已记帐实际销售额。</span><span class="sxs-lookup"><span data-stu-id="7b29a-126">A billed sales actual for the hours and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="7b29a-127">为进行了编辑以减少数量的时间交易开票。</span><span class="sxs-lookup"><span data-stu-id="7b29a-127">Invoicing a time transaction that was edited to reduce the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="7b29a-128">原始时间审批中时数和金额的未记帐销售额冲销。</span><span class="sxs-lookup"><span data-stu-id="7b29a-128">An unbilled sales reversal for the hours and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="7b29a-129">编辑的发票明细详细信息中的时数和金额应计费的新未记帐实际销售额，实际销售额的冲销和相等的已记帐实际销售额。</span><span class="sxs-lookup"><span data-stu-id="7b29a-129">A new unbilled sales actual that is chargeable for the hours and amount on the edited invoice line detail, a reversal of the sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="7b29a-130">编辑的发票明细详细信息中扣除更正的数字后剩余时数不应计费的新未记帐实际销售额，实际销售额的冲销和相等的已记帐实际销售额。</span><span class="sxs-lookup"><span data-stu-id="7b29a-130">A new unbilled sales actual that is non-chargeable for the remaining hours and amount after deducting the corrected figures on edited invoice line detail, a reversal of the sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="7b29a-131">为进行了编辑以增加数量的时间交易开票。</span><span class="sxs-lookup"><span data-stu-id="7b29a-131">Invoicing a time transaction that was edited to increase the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="7b29a-132">原始时间审批中时数和金额的未记帐销售额冲销。</span><span class="sxs-lookup"><span data-stu-id="7b29a-132">An unbilled sales reversal for the hours and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="7b29a-133">编辑的发票明细详细信息中的时数和金额应计费的新未记帐实际销售额，未记帐实际销售额的冲销和相等的已记帐实际销售额。</span><span class="sxs-lookup"><span data-stu-id="7b29a-133">A new unbilled sales actual that is chargeable for the hours and amount on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="7b29a-134">为草稿发票未进行任何编辑的支出交易开票。</span><span class="sxs-lookup"><span data-stu-id="7b29a-134">Invoicing an expense transaction without any edits on draft invoice.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="7b29a-135">原始支出审批中数量和金额的未记帐销售额冲销。</span><span class="sxs-lookup"><span data-stu-id="7b29a-135">An unbilled sales reversal for the quantity and amount on the original expense approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="7b29a-136">原始支出审批中数量和金额的已记帐实际销售额</span><span class="sxs-lookup"><span data-stu-id="7b29a-136">A billed sales actual for the quantity and amount on the original expense approval</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="7b29a-137">为进行了编辑以减少数量的支出交易开票。</span><span class="sxs-lookup"><span data-stu-id="7b29a-137">Invoicing an expense transaction that was edited to reduce the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="7b29a-138">原始支出审批中数量和金额的未记帐销售额冲销。</span><span class="sxs-lookup"><span data-stu-id="7b29a-138">An unbilled sales reversal for the quantity and amount on the original expense approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="7b29a-139">编辑的发票明细详细信息中的数量和金额应计费的新未记帐实际销售额，未记帐实际销售额的冲销和相等的已记帐实际销售额。</span><span class="sxs-lookup"><span data-stu-id="7b29a-139">A new unbilled sales actual that is chargeable for the quantity and amount on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="7b29a-140">编辑的发票明细详细信息中扣除更正的数字后剩余数量不应计费的新未记帐实际销售额，未记帐实际销售额的冲销和相等的已记帐实际销售额。</span><span class="sxs-lookup"><span data-stu-id="7b29a-140">A new unbilled sales actual that is non-chargeable for the remaining quantity and amount after deducting the corrected figures on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="7b29a-141">为进行了编辑以增加数量的支出交易开票。</span><span class="sxs-lookup"><span data-stu-id="7b29a-141">Invoicing an expense transaction that was edited to increase the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="7b29a-142">原始支出审批中数量和金额的未记帐销售额冲销。</span><span class="sxs-lookup"><span data-stu-id="7b29a-142">An unbilled sales reversal for the quantity and amount on the original expense approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="7b29a-143">编辑的发票明细详细信息中的数量和金额应计费的新未记帐实际销售额，未记帐实际销售额的冲销和相等的已记帐实际销售额。</span><span class="sxs-lookup"><span data-stu-id="7b29a-143">A new unbilled sales actual that is chargeable for quantity and amount on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span> 
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="7b29a-144">为费用开票。</span><span class="sxs-lookup"><span data-stu-id="7b29a-144">Invoicing a fee.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="7b29a-145">原始日记帐行中费用金额的未记帐销售额冲销。</span><span class="sxs-lookup"><span data-stu-id="7b29a-145">An unbilled sales reversal for the fee amount on the original journal line.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="7b29a-146">原始费用日记帐行中数量和金额的已记帐实际销售额。</span><span class="sxs-lookup"><span data-stu-id="7b29a-146">A billed sales actual for the quantity and amount on the original fee journal line.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="7b29a-147">为里程碑开票。</span><span class="sxs-lookup"><span data-stu-id="7b29a-147">Invoicing a milestone.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="7b29a-148">项目合同子项上原始里程碑上的里程碑金额的已记帐实际销售额。</span><span class="sxs-lookup"><span data-stu-id="7b29a-148">A billed sales actual for the milestone amount on the original milestone on the project contract line.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="7b29a-149">为基于产品的合同子项开票。</span><span class="sxs-lookup"><span data-stu-id="7b29a-149">Invoicing a product-based contract line.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="7b29a-150">数量和金额来自基于产品的合同子项的产品明细的已记帐实际销售额。</span><span class="sxs-lookup"><span data-stu-id="7b29a-150">A billed sales actual for the product line with the quantity and amount coming from the product-based contract line.</span></span>
                </p>
            </td>
        </tr>
    </tbody>
</table>
