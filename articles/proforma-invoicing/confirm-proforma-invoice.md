---
title: 确认估价账单
description: 本主题提供有关确认估价账单的信息。
author: rumant
manager: AnnBe
ms.date: 10/13/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: b2ed241509d2643d841ce55777e6e316612f70b8
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/15/2021
ms.locfileid: "5287857"
---
# <a name="confirm-a-proforma-invoice"></a><span data-ttu-id="f130d-103">确认估价账单</span><span class="sxs-lookup"><span data-stu-id="f130d-103">Confirm a proforma invoice</span></span>

<span data-ttu-id="f130d-104">_**适用于：** 面向资源/非库存场景的 Project Operations_</span><span class="sxs-lookup"><span data-stu-id="f130d-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="f130d-105">估价发票确认后，项目发票的状态将更新为 **已确认**。</span><span class="sxs-lookup"><span data-stu-id="f130d-105">After a proforma invoice is confirmed, the status of the project invoice updates to **Confirmed**.</span></span> <span data-ttu-id="f130d-106">发票确认后，将变为只读。</span><span class="sxs-lookup"><span data-stu-id="f130d-106">When an invoice is confirmed, it becomes read-only.</span></span> <span data-ttu-id="f130d-107">之后，只有在发票标记为已支付的情况下，在有任何客户发起更正或贷记时才可以更正发票。</span><span class="sxs-lookup"><span data-stu-id="f130d-107">Going forward, the invoice can only be corrected if there are any customer-initiated corrections or credits, or when it's marked as paid.</span></span>

<span data-ttu-id="f130d-108">下表列出了系统创建的实际值。</span><span class="sxs-lookup"><span data-stu-id="f130d-108">The following table lists the actuals created by the system.</span></span> <span data-ttu-id="f130d-109">在确认草稿项目发票之前对草稿项目发票执行某些操作时会创建这些实际值。</span><span class="sxs-lookup"><span data-stu-id="f130d-109">These actuals are created when certain operations are performed on the draft project invoice before it is confirmed.</span></span>

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="416" valign="top">
                <p><span data-ttu-id="f130d-110">
                    <strong>方案</strong>
                </span><span class="sxs-lookup"><span data-stu-id="f130d-110">
                    <strong>Scenario</strong>
                </span></span></p>
            </td>
            <td width="608" valign="top">
                <p><span data-ttu-id="f130d-111">
                    <strong>确认时创建的实际值</strong>
                </span><span class="sxs-lookup"><span data-stu-id="f130d-111">
                    <strong>Actuals created on confirmation</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="f130d-112">为草稿发票未进行任何编辑的时间交易开票。</span><span class="sxs-lookup"><span data-stu-id="f130d-112">Invoicing a time transaction without any edits on the draft invoice.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="f130d-113">原始时间审批中时数和金额的未记帐销售额冲销。</span><span class="sxs-lookup"><span data-stu-id="f130d-113">An unbilled sales reversal for the hours and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="f130d-114">原始时间审批中时数和金额的已记帐实际销售额。</span><span class="sxs-lookup"><span data-stu-id="f130d-114">A billed sales actual for the hours and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="f130d-115">为进行了编辑以减少数量的时间交易开票。</span><span class="sxs-lookup"><span data-stu-id="f130d-115">Invoicing a time transaction that was edited to reduce the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="f130d-116">原始时间审批中时数和金额的未记帐销售额冲销。</span><span class="sxs-lookup"><span data-stu-id="f130d-116">An unbilled sales reversal for the hours and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="f130d-117">编辑的发票明细详细信息中的时数和金额应计费的新未记帐实际销售额，未记帐实际销售额的冲销和相等的已记帐实际销售额。</span><span class="sxs-lookup"><span data-stu-id="f130d-117">A new unbilled sales actual that is chargeable for the hours and amount on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="f130d-118">编辑的发票明细详细信息中扣除更正的数字后剩余时数不应计费的新未记帐实际销售额，未记帐实际销售额的冲销和相等的已记帐实际销售额。</span><span class="sxs-lookup"><span data-stu-id="f130d-118">A new unbilled sales actual that is non-chargeable for the remaining hours and amount after deducting the corrected figures on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="f130d-119">为进行了编辑以增加数量的时间交易开票。</span><span class="sxs-lookup"><span data-stu-id="f130d-119">Invoicing a time transaction that was edited to increase the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="f130d-120">原始时间审批中时数和金额的未记帐销售额冲销。</span><span class="sxs-lookup"><span data-stu-id="f130d-120">An unbilled sales reversal for the hours and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="f130d-121">编辑的发票明细详细信息中的时数和金额应计费的新未记帐实际销售额，未记帐实际销售额的冲销和相等的已记帐实际销售额。</span><span class="sxs-lookup"><span data-stu-id="f130d-121">A new unbilled sales actual that is chargeable for the hours and amount on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="f130d-122">为草稿发票未进行任何编辑的支出交易开票。</span><span class="sxs-lookup"><span data-stu-id="f130d-122">Invoicing an expense transaction without any edits on the draft invoice.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="f130d-123">原始支出审批中数量和金额的未记帐销售额冲销。</span><span class="sxs-lookup"><span data-stu-id="f130d-123">An unbilled sales reversal for the quantity and amount on the original expense approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="f130d-124">原始支出审批中数量和金额的已记帐实际销售额。</span><span class="sxs-lookup"><span data-stu-id="f130d-124">A billed sales actual for the quantity and amount on the original expense approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="f130d-125">为进行了编辑以减少数量的支出交易开票。</span><span class="sxs-lookup"><span data-stu-id="f130d-125">Invoicing an expense transaction that was edited to reduce the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="f130d-126">原始支出审批中数量和金额的未记帐销售额冲销。</span><span class="sxs-lookup"><span data-stu-id="f130d-126">An unbilled sales reversal for the quantity and amount on the original expense approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="f130d-127">编辑的发票明细详细信息中的数量和金额应计费的新未记帐实际销售额，未记帐实际销售额的冲销和相等的已记帐实际销售额。</span><span class="sxs-lookup"><span data-stu-id="f130d-127">A new unbilled sales actual that is chargeable for the quantity and amount on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span> 
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="f130d-128">编辑的发票明细详细信息中扣除更正的数字后剩余数量不应计费的新未记帐实际销售额，未记帐实际销售额的冲销和已记帐实际销售额的对等值。</span><span class="sxs-lookup"><span data-stu-id="f130d-128">A new unbilled sales actual that is non-chargeable for the remaining quantity and amount after deducting the corrected figures on edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent of the billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="f130d-129">为进行了编辑以增加数量的支出交易开票。</span><span class="sxs-lookup"><span data-stu-id="f130d-129">Invoicing an expense transaction that was edited to increase the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="f130d-130">原始支出审批中数量和金额的未记帐销售额冲销。</span><span class="sxs-lookup"><span data-stu-id="f130d-130">An unbilled sales reversal for the quantity and amount on the original expense approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="f130d-131">编辑的发票明细详细信息中的数量和金额应计费的新未记帐实际销售额，未记帐实际销售额的冲销和相等的已记帐实际销售额。</span><span class="sxs-lookup"><span data-stu-id="f130d-131">A new unbilled sales actual that is chargeable for quantity and amount on the edited invoice line detail, a reversal of the untilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="f130d-132">为费用开票。</span><span class="sxs-lookup"><span data-stu-id="f130d-132">Invoicing a fee.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="f130d-133">原始日记帐行中费用金额的未记帐销售额冲销。</span><span class="sxs-lookup"><span data-stu-id="f130d-133">An unbilled sales reversal for the fee amount on the original journal line.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="f130d-134">原始费用日记帐行中数量和金额的已记帐实际销售额。</span><span class="sxs-lookup"><span data-stu-id="f130d-134">A billed sales actual for the quantity and amount on the original fee journal line.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="f130d-135">为里程碑开票。</span><span class="sxs-lookup"><span data-stu-id="f130d-135">Invoicing a milestone.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="f130d-136">项目合同子项上原始里程碑上的里程碑金额的已记帐实际销售额。</span><span class="sxs-lookup"><span data-stu-id="f130d-136">A billed sales actual for the milestone amount on the original milestone on the project contract line.</span></span>
                </p>
            </td>
        </tr>
    </tbody>
</table>


[!INCLUDE[footer-include](../includes/footer-banner.md)]