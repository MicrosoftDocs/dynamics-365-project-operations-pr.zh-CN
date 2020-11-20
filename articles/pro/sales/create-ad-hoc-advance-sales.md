---
title: 在合同中创建临时预付款 - 精简
description: 此主题提供有关如何根据需要在合同中创建预付款的信息。
author: rumant
manager: Annbe
ms.date: 10/26/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: a6bf02c2e2ab2f3c696b1eab1b92a20272187bf5
ms.sourcegitcommit: f6f86e80dfef15a7b5f9174b55dddf410522f7c8
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/31/2020
ms.locfileid: "4181351"
---
# <a name="creating-an-ad-hoc-advance-on-a-contract---lite"></a><span data-ttu-id="d5541-103">在合同中创建临时预付款 - 精简</span><span class="sxs-lookup"><span data-stu-id="d5541-103">Creating an ad hoc advance on a contract - lite</span></span>

<span data-ttu-id="d5541-104">_**适用于：** 精简部署 - 估价交易开票_</span><span class="sxs-lookup"><span data-stu-id="d5541-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="d5541-105">Microsoft Dynamics 365 Project Operations 支持涉及预付款的开票场景。</span><span class="sxs-lookup"><span data-stu-id="d5541-105">Microsoft Dynamics 365 Project Operations supports invoicing scenarios that involve pre-payments and advances.</span></span> <span data-ttu-id="d5541-106">在 **Project Operations** 中使用 **预付款** 的流程与 **保留款** 合同类似。</span><span class="sxs-lookup"><span data-stu-id="d5541-106">The process for using **Advances** in **Project Operations** is similar to **Retainer** contracts.</span></span> 

<span data-ttu-id="d5541-107">完成以下步骤为客户的预付款开票。</span><span class="sxs-lookup"><span data-stu-id="d5541-107">Complete the following steps to invoice the customer for an advance.</span></span>

1. <span data-ttu-id="d5541-108">转到 **项目合同** 页，然后选择 **预付款和保留款** 选项卡。</span><span class="sxs-lookup"><span data-stu-id="d5541-108">Go to the **Project Contract** page, and then select the **Advances and Retainers** tab.</span></span>
2. <span data-ttu-id="d5541-109">在列出所有以前记录的预付款的子网格中，选择 **+ 新建项目合同保留款**。</span><span class="sxs-lookup"><span data-stu-id="d5541-109">In the subgrid that lists all the previously recorded advances and prepayments, select **+ New Project contract retainer**.</span></span> 

    <span data-ttu-id="d5541-110">**快速创建** 窗体将打开以记录预付款。</span><span class="sxs-lookup"><span data-stu-id="d5541-110">The **Quick Create** form opens for recording a prepayment or advance.</span></span>
    
3. <span data-ttu-id="d5541-111">下表列出了记录预付款的字段，以及在创建新预付款时需要记住的注意事项：</span><span class="sxs-lookup"><span data-stu-id="d5541-111">The table below lists the fields for recording an advance and the considerations to keep in mind as you create new ones:</span></span>

    | <span data-ttu-id="d5541-112">字段</span><span class="sxs-lookup"><span data-stu-id="d5541-112">Field</span></span> | <span data-ttu-id="d5541-113">描述</span><span class="sxs-lookup"><span data-stu-id="d5541-113">Description</span></span> | <span data-ttu-id="d5541-114">下游影响</span><span class="sxs-lookup"><span data-stu-id="d5541-114">Downstream impact</span></span> |
    | --- | --- | --- |
    | <span data-ttu-id="d5541-115">**项目合同客户**</span><span class="sxs-lookup"><span data-stu-id="d5541-115">**Project Contract Customer**</span></span> | <span data-ttu-id="d5541-116">此字段指示将就此预付款为合同中的哪个客户开票。</span><span class="sxs-lookup"><span data-stu-id="d5541-116">This field indicates which customer on the contract will be invoiced for this advance.</span></span> | <span data-ttu-id="d5541-117">如果您在合同中有多个客户，想要为每个客户的特定保留款或预付款金额开票，请为每个客户单独创建预付款。</span><span class="sxs-lookup"><span data-stu-id="d5541-117">If you have multiple customers on the contract and want to invoice each of them for a specific retainer or advance amount, create an advance for each customer individually.</span></span> |
    | <span data-ttu-id="d5541-118">**说明**</span><span class="sxs-lookup"><span data-stu-id="d5541-118">**Description**</span></span> | <span data-ttu-id="d5541-119">预付款的用途或时间的说明，帮助识别此预付款。</span><span class="sxs-lookup"><span data-stu-id="d5541-119">The description of the purpose or timing of the advance to help identify this advance.</span></span> | <span data-ttu-id="d5541-120">此说明显示在此预付款的发票明细上。</span><span class="sxs-lookup"><span data-stu-id="d5541-120">This description is displayed on the invoice line for this advance.</span></span> |
    | <span data-ttu-id="d5541-121">**金额**</span><span class="sxs-lookup"><span data-stu-id="d5541-121">**Amount**</span></span> | <span data-ttu-id="d5541-122">预付款的金额。</span><span class="sxs-lookup"><span data-stu-id="d5541-122">The amount for the pre-payment or advance.</span></span> | <span data-ttu-id="d5541-123">此金额显示在此预付款的发票明细上。</span><span class="sxs-lookup"><span data-stu-id="d5541-123">This amount is displayed on the invoice line for this advance.</span></span> |
    | <span data-ttu-id="d5541-124">**账单日期**</span><span class="sxs-lookup"><span data-stu-id="d5541-124">**Invoice Date**</span></span> | <span data-ttu-id="d5541-125">就此预付款向客户开票的日期。</span><span class="sxs-lookup"><span data-stu-id="d5541-125">The date on which this advance is invoiced to the customer.</span></span> | <span data-ttu-id="d5541-126">此日期是为此预付款创建发票明细的自动发票创建流程的日期。</span><span class="sxs-lookup"><span data-stu-id="d5541-126">This is the date for the automated invoice creation process to create an invoice line for this advance.</span></span> |
    | <span data-ttu-id="d5541-127">**账单状态**</span><span class="sxs-lookup"><span data-stu-id="d5541-127">**Invoice Status**</span></span> | <span data-ttu-id="d5541-128">这是一个选项设置，指示此预付款是否已添加到此客户的草稿发票中。</span><span class="sxs-lookup"><span data-stu-id="d5541-128">This is an option setting that indicates whether this advance is added to a draft invoice for this customer.</span></span> <span data-ttu-id="d5541-129">值可以为：</span><span class="sxs-lookup"><span data-stu-id="d5541-129">The possible values are:</span></span></br><span data-ttu-id="d5541-130">- **未准备好开具账单**</span><span class="sxs-lookup"><span data-stu-id="d5541-130">- **Not ready to invoice**</span></span></br><span data-ttu-id="d5541-131">- **已准备好开具账单**</span><span class="sxs-lookup"><span data-stu-id="d5541-131">- **Ready to invoice**</span></span> | <span data-ttu-id="d5541-132">在将预付款标记为 **可开票** 时，它将在草稿发票上添加为明细时间。</span><span class="sxs-lookup"><span data-stu-id="d5541-132">When an advance or pre-payment is marked as **Ready to invoice**, it is added as a line time on a draft invoice.</span></span> <span data-ttu-id="d5541-133">只有完全开票的预付款才能用于与下一个发票期间的项目成本对帐。</span><span class="sxs-lookup"><span data-stu-id="d5541-133">Only a fully invoiced advance can be used to reconcile against project costs for the next invoice period.</span></span> |

4. <span data-ttu-id="d5541-134">在快速创建对话中选择 **保存并关闭** 记录预付款。</span><span class="sxs-lookup"><span data-stu-id="d5541-134">Select **Save and close** on the quick create dialog to record the advance or the pre-payment.</span></span>