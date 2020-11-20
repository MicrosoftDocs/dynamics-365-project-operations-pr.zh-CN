---
title: 管理不可超出状态和验证
description: 此主题提供在 Project Operations 中执行的上限检查的相关信息。
author: rumant
manager: Annbe
ms.date: 10/22/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 09dea414e91a365f33bd23089c427b5f63f55c8e
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/28/2020
ms.locfileid: "4129982"
---
# <a name="manage-not-to-exceed-status-and-validations"></a><span data-ttu-id="37eb5-103">管理不可超出状态和验证</span><span class="sxs-lookup"><span data-stu-id="37eb5-103">Manage not-to-exceed status and validations</span></span> 

<span data-ttu-id="37eb5-104">_**适用于：** 基于资源/非库存场景的 Project Operations，精简部署 - 估价开票交易_</span><span class="sxs-lookup"><span data-stu-id="37eb5-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

## <a name="not-to-exceed-on-approvals"></a><span data-ttu-id="37eb5-105">审批中的上限</span><span class="sxs-lookup"><span data-stu-id="37eb5-105">Not-to-exceed on approvals</span></span>

<span data-ttu-id="37eb5-106">在提交时间或支出条目时，会创建审批记录。</span><span class="sxs-lookup"><span data-stu-id="37eb5-106">When a time or expense entry is submitted, an approval record is created.</span></span> <span data-ttu-id="37eb5-107">如果审批为应计费，并且映射到时间和材料合同子项，系统将在以下级别完成上限验证检查：</span><span class="sxs-lookup"><span data-stu-id="37eb5-107">If the approval is chargeable and maps to a time and material contract line, the system completes a not-to-exceed validation check at the following levels:</span></span>

  - <span data-ttu-id="37eb5-108">检查项目合同子项上客户的限制设置</span><span class="sxs-lookup"><span data-stu-id="37eb5-108">Check against the limit set up for the customer on the project contract line</span></span>
  - <span data-ttu-id="37eb5-109">检查合同子项上的限制设置</span><span class="sxs-lookup"><span data-stu-id="37eb5-109">Check against the limit set up on the contract line</span></span>
  - <span data-ttu-id="37eb5-110">检查客户的限制设置</span><span class="sxs-lookup"><span data-stu-id="37eb5-110">Check against the limit set up for the customer</span></span>
  - <span data-ttu-id="37eb5-111">检查合同上的限制设置</span><span class="sxs-lookup"><span data-stu-id="37eb5-111">Check against the limit set up on the contract</span></span>

<span data-ttu-id="37eb5-112">每个级别的检查涉及确保此审批中的销售金额值在计入已记录的计费积压金额，以及到目前在该级别已开票的金额后，不超过该级别的上限。</span><span class="sxs-lookup"><span data-stu-id="37eb5-112">The checks at each level involve ensuring that the amount of sales value on this approval will not violate the not-to-exceed limit at that level after accounting for the amount of billing backlog already recorded, and the amount invoiced to date at that level.</span></span>

<span data-ttu-id="37eb5-113">如果检查通过，审批将变为 **成功** 验证状态。</span><span class="sxs-lookup"><span data-stu-id="37eb5-113">If the check passes, the approval is given a validation status of **Success**.</span></span>

<span data-ttu-id="37eb5-114">如果检查未通过，审批将变为 **失败** 验证状态。</span><span class="sxs-lookup"><span data-stu-id="37eb5-114">If the check fails, the approval is given a validation status of **Failed**.</span></span> <span data-ttu-id="37eb5-115">上限验证详细信息将通知用户验证在哪个级别失败。</span><span class="sxs-lookup"><span data-stu-id="37eb5-115">The not-to-exceed validation detail will inform the user at which level the validation failed.</span></span>

<span data-ttu-id="37eb5-116">当提交的时间或支出条目被视为非应计费时，上限验证状态将设置为 **不适用**，验证详细信息为 **不适用**。</span><span class="sxs-lookup"><span data-stu-id="37eb5-116">When the submitted time or expense entry is considered non-chargeable, the not-to-exceed validation status is set to **Not Applicable** with the validation detail equal to **Not applicable**.</span></span>

## <a name="not-to-exceed-on-unbilled-sales-actuals"></a><span data-ttu-id="37eb5-117">未记帐实际销售额中的上限</span><span class="sxs-lookup"><span data-stu-id="37eb5-117">Not-to-exceed on unbilled sales actuals</span></span>

<span data-ttu-id="37eb5-118">在时间或支出条目批准时，将创建成本和未记帐实际销售额记录。</span><span class="sxs-lookup"><span data-stu-id="37eb5-118">When a time or expense entry is approved, cost and unbilled sales actuals records are created.</span></span> <span data-ttu-id="37eb5-119">如果创建的未记帐实际销售额为应计费，并且映射到时间和材料合同子项，应用程序将在以下级别执行上限验证检查：</span><span class="sxs-lookup"><span data-stu-id="37eb5-119">If the unbilled sales actual being created is chargeable and maps to a time and material contract line, the application performs a not-to-exceed validation check at the following levels:</span></span>

  - <span data-ttu-id="37eb5-120">检查项目合同子项的客户的限制设置</span><span class="sxs-lookup"><span data-stu-id="37eb5-120">Check against the limit set up for the customer of the project contract line</span></span>
  - <span data-ttu-id="37eb5-121">检查合同子项上的限制设置</span><span class="sxs-lookup"><span data-stu-id="37eb5-121">Check against the limit set up on the contract line</span></span>
  - <span data-ttu-id="37eb5-122">检查客户的限制设置</span><span class="sxs-lookup"><span data-stu-id="37eb5-122">Check against the limit set up for the customer</span></span>
  - <span data-ttu-id="37eb5-123">检查合同上的限制设置</span><span class="sxs-lookup"><span data-stu-id="37eb5-123">Check against the limit set up on the contract</span></span>

<span data-ttu-id="37eb5-124">每个级别的检查确保实际值中的销售金额值在计入已记录的计费积压金额，以及到目前在该级别已开票的金额后，不超过该级别的上限。</span><span class="sxs-lookup"><span data-stu-id="37eb5-124">The checks at each level ensure that the amount of sales value on the actual will not violate the not-to-exceed limit at that level after accounting for the amount of billing backlog already recorded, and the amount invoiced to date at that level.</span></span>

<span data-ttu-id="37eb5-125">如果检查通过，未记帐实际销售额的上限将变为 **已提交** 状态。</span><span class="sxs-lookup"><span data-stu-id="37eb5-125">If the check passes, the unbilled sales actual is given a not-to-exceed status of **Committed**.</span></span>

<span data-ttu-id="37eb5-126">如果检查未通过，未记帐实际销售额的上限将变为 **失败** 状态。</span><span class="sxs-lookup"><span data-stu-id="37eb5-126">If the check fails, the unbilled sales actual is given a not-to-exceed status of **Failed**.</span></span> <span data-ttu-id="37eb5-127">验证详细信息将通知用户验证在哪个级别失败。</span><span class="sxs-lookup"><span data-stu-id="37eb5-127">The validation detail informs the user at which level the validation failed.</span></span>

<span data-ttu-id="37eb5-128">当未记帐实际销售额被视为非应计费或免费时，如果四个级别中任何级别都没有上限设置，或者创建的实际值为成本、保留款、资源单位或组织间销售，**上限状态** 和 **上限验证详细信息** 字段必须设置为 **不适用**。</span><span class="sxs-lookup"><span data-stu-id="37eb5-128">When the unbilled sales actual is considered non-chargeable or complimentary, if there is no not-to-exceed limit setup at any of the four levels, or if the actual being created is Cost, Retainer, Resourcing Unit, or Inter-organization Sales, the **Not-to-Exceed Status** and **Not-to-Exceed Validation Detail** fields must be set to **Not Applicable**.</span></span>

## <a name="reset-the-not-to-exceed-status"></a><span data-ttu-id="37eb5-129">重置上限状态</span><span class="sxs-lookup"><span data-stu-id="37eb5-129">Reset the not-to-exceed status</span></span>

<span data-ttu-id="37eb5-130">您可以对上限状态执行批量重置。</span><span class="sxs-lookup"><span data-stu-id="37eb5-130">You can perform a bulk reset of the not-to-exceed status.</span></span> <span data-ttu-id="37eb5-131">这让项目经理能够调整上限验证，将一个特定工作、时间或支出主体的开票放在已从可用上限金额提交的其他主体之前优先处理。</span><span class="sxs-lookup"><span data-stu-id="37eb5-131">This allows Project managers to adjust not-to-exceed validation to prioritize invoicing of one particular body of work, time, or expenses over others that are already committed from the available not-to-exceed amount.</span></span>

<span data-ttu-id="37eb5-132">上限状态在未记帐实际销售额中重置后，已提交金额将减少。</span><span class="sxs-lookup"><span data-stu-id="37eb5-132">After the not-to-exceed status is reset on unbilled sales actuals, the committed amount is reduced.</span></span> <span data-ttu-id="37eb5-133">项目经理可以选择以前未通过上限验证的另一个工作、时间或支出主体，对其进行重新评估。</span><span class="sxs-lookup"><span data-stu-id="37eb5-133">The Project manager can select another body of work, time, or expenses that previously failed the not-to-exceed validation and reevaluate them.</span></span> <span data-ttu-id="37eb5-134">已提交金额减少后，这些实际值将通过验证。</span><span class="sxs-lookup"><span data-stu-id="37eb5-134">With the reduction in the committed amount, these actuals will now pass the validation.</span></span> <span data-ttu-id="37eb5-135">这将帮助项目经理对该期间内的可开票交易施加更大的影响和控制。</span><span class="sxs-lookup"><span data-stu-id="37eb5-135">This helps the Project manager exert greater influence and control over the invoiceable transactions for that period.</span></span>

<span data-ttu-id="37eb5-136">若要重置上限状态，从 **时间和材料计费积压** 或 **实际值** 视图中选择一个或多个实际值，然后选择 **重置上限状态**。</span><span class="sxs-lookup"><span data-stu-id="37eb5-136">To reset the not-to-exceed status, select one or more actuals from the **Time and Material Billing Backlog** or **Actuals** view, and then select **Reset Not-to-Exceed Status**.</span></span>

<span data-ttu-id="37eb5-137">上限状态将在所有相关的选定实际值中重置为 **未评估**。</span><span class="sxs-lookup"><span data-stu-id="37eb5-137">The not-to-exceed status is reset to **Not Evaluated** on all of the relevant selected actuals.</span></span> <span data-ttu-id="37eb5-138">重置上限状态的实际值是指尚未开票、不在草稿发票上且标记为应计费的未记帐实际销售额。</span><span class="sxs-lookup"><span data-stu-id="37eb5-138">Actuals that have their not-to-exceed status reset are unbilled sales actuals that aren't already invoiced, not on a draft invoice, and are marked as chargeable.</span></span> <span data-ttu-id="37eb5-139">任何其他所选的实际值都将被忽略。</span><span class="sxs-lookup"><span data-stu-id="37eb5-139">Any other selected actuals are ignored.</span></span>

## <a name="reevaluate-not-to-exceed-status"></a><span data-ttu-id="37eb5-140">重新评估上限状态</span><span class="sxs-lookup"><span data-stu-id="37eb5-140">Reevaluate not-to-exceed status</span></span>

<span data-ttu-id="37eb5-141">您可以对上限状态执行批量重新评估。</span><span class="sxs-lookup"><span data-stu-id="37eb5-141">You can perform a bulk re-evaluation of the not-to-exceed status.</span></span> <span data-ttu-id="37eb5-142">重新评估上限状态在下列情况下很有用：</span><span class="sxs-lookup"><span data-stu-id="37eb5-142">Re-evaluation of the not-to-exceed status is useful when:</span></span>

  - <span data-ttu-id="37eb5-143">客户存在上限重新协商，实际值需要重新计算。</span><span class="sxs-lookup"><span data-stu-id="37eb5-143">There was a renegotiation of not-to-exceed limits with the customer and actuals will need to be reevaluated.</span></span>
  - <span data-ttu-id="37eb5-144">项目经理想要通过将一个工作主体优先于另一个主体处理来对未记帐销售额积压的开票进行调整。</span><span class="sxs-lookup"><span data-stu-id="37eb5-144">The Project manager wants to fine-tune the invoicing of unbilled sales backlog by prioritizing one body of work over another.</span></span>

<span data-ttu-id="37eb5-145">若要重新评估上限状态，从 **时间和材料计费积压** 或 **实际值** 视图中选择一个或多个实际值，然后选择 **重新评估上限状态**。</span><span class="sxs-lookup"><span data-stu-id="37eb5-145">To reevaluate the not-to-exceed status, select one or more actuals from the **Time and Material Billing Backlog** or **Actuals** view, and select **Reevaluate Not-to-Exceed Status**.</span></span>

<span data-ttu-id="37eb5-146">所有具有上限的相关的选定实际值将根据上限设置进行评估。</span><span class="sxs-lookup"><span data-stu-id="37eb5-146">All of the relevant selected actuals with a not-to-exceed limit will be evaluated against the not-to-exceed limit setup.</span></span> <span data-ttu-id="37eb5-147">与重新评估上限状态有关的实际值是指未开票、不在草稿发票上且标记为应计费的未记帐实际销售额。</span><span class="sxs-lookup"><span data-stu-id="37eb5-147">Actuals that are relevant for re-evaluating the not-to-exceed status are unbilled sales actuals that are not invoiced, not on a draft invoice, and are marked as chargeable.</span></span> <span data-ttu-id="37eb5-148">选择的任何其他选定实际值。</span><span class="sxs-lookup"><span data-stu-id="37eb5-148">Any other select actuals selected.</span></span>
