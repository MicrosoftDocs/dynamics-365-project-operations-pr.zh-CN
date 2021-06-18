---
title: 管理记帐积压
description: 此主题提供有关如何在 Project Operations 中查看和处理记帐积压的信息。
author: rumant
ms.date: 04/05/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: d7c242937cd9dd277f8d92b7a29333c1fa272e5f
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/10/2021
ms.locfileid: "6011900"
---
# <a name="manage-billing-backlog"></a><span data-ttu-id="ffc33-103">管理记帐积压</span><span class="sxs-lookup"><span data-stu-id="ffc33-103">Manage billing backlog</span></span>

<span data-ttu-id="ffc33-104">_ **适用于：** 面向资源/非库存场景的 Project Operations</span><span class="sxs-lookup"><span data-stu-id="ffc33-104">_ **Applies To:** Project Operations for resource/non-stocked based scenarios</span></span>

<span data-ttu-id="ffc33-105">Dynamics 365 Project Operations 有专用视图来帮助管理计费积压。</span><span class="sxs-lookup"><span data-stu-id="ffc33-105">Dynamics 365 Project Operations has dedicated views to help manage the billing backlog.</span></span> <span data-ttu-id="ffc33-106">若要管理计费积压，请选择 **计费** 下的 **销售** 区域中的链接。</span><span class="sxs-lookup"><span data-stu-id="ffc33-106">To manage the billing backlog, select the links in the **Sales** area, under **Billing**.</span></span> 

<span data-ttu-id="ffc33-107">提供以下视图：</span><span class="sxs-lookup"><span data-stu-id="ffc33-107">The following views available:</span></span>

- <span data-ttu-id="ffc33-108">保留款和预付款</span><span class="sxs-lookup"><span data-stu-id="ffc33-108">Retainers and Advances</span></span>
- <span data-ttu-id="ffc33-109">可用的保留款和预付款</span><span class="sxs-lookup"><span data-stu-id="ffc33-109">Available Retainers and Advances</span></span>
- <span data-ttu-id="ffc33-110">固定价格里程碑</span><span class="sxs-lookup"><span data-stu-id="ffc33-110">Fixed Price Milestones</span></span>
- <span data-ttu-id="ffc33-111">时间和材料记帐积压</span><span class="sxs-lookup"><span data-stu-id="ffc33-111">Time and Material Billing Backlog</span></span>

## <a name="retainers-and-advances"></a><span data-ttu-id="ffc33-112">保留款和预付款</span><span class="sxs-lookup"><span data-stu-id="ffc33-112">Retainers and Advances</span></span>

<span data-ttu-id="ffc33-113"> **保留款和预付款** 视图会列出所有项目合同中的保留款和预付款。</span><span class="sxs-lookup"><span data-stu-id="ffc33-113">The **Retainers and Advances** view lists the retainers and advances across all project contracts.</span></span> <span data-ttu-id="ffc33-114">在对保留款和预付款开票后，预付款金额将变为可供使用。</span><span class="sxs-lookup"><span data-stu-id="ffc33-114">After a retainer or advance is invoiced, the amount of the advance becomes available to use.</span></span>

## <a name="available-retainers-and-advances"></a><span data-ttu-id="ffc33-115">可用的保留款和预付款</span><span class="sxs-lookup"><span data-stu-id="ffc33-115">Available Retainers and Advances</span></span>

<span data-ttu-id="ffc33-116"> **可用的保留款和预付款** 视图会列出所有项目合同中的所有可用保留款和预付款。</span><span class="sxs-lookup"><span data-stu-id="ffc33-116">The **Available Retainers and Advances** view lists all available retainers and advances across all project contracts.</span></span> <span data-ttu-id="ffc33-117">在对保留款和预付款开票后，预付款金额将变为可供使用，并添加到此列表中。</span><span class="sxs-lookup"><span data-stu-id="ffc33-117">After a retainer or advance is invoiced, the amount of the advance becomes available to use and is added to the list.</span></span> <span data-ttu-id="ffc33-118">保留款或预付款的金额用完后，将从列表中删除。</span><span class="sxs-lookup"><span data-stu-id="ffc33-118">After the amount of the retainer or advance is used completely, it's removed from the list.</span></span>

## <a name="fixed-price-milestones"></a><span data-ttu-id="ffc33-119">固定价格里程碑</span><span class="sxs-lookup"><span data-stu-id="ffc33-119">Fixed Price Milestones</span></span>

<span data-ttu-id="ffc33-120">**固定价格里程碑** 视图列出了所有项目合同子项的所有固定价格里程碑。</span><span class="sxs-lookup"><span data-stu-id="ffc33-120">The **Fixed Price Milestones** view lists all fixed price milestones across all project contract lines.</span></span> <span data-ttu-id="ffc33-121">从此视图中，可以将单个或多个里程碑标记为 **已准备好开单** 或 **未准备好开单**。</span><span class="sxs-lookup"><span data-stu-id="ffc33-121">From this view, single or multiple milestones can be marked as **Ready to invoice** or **Not ready to invoice**.</span></span> <span data-ttu-id="ffc33-122">将里程碑标记为 **可开票** 后，它可以被放到草稿发票上。</span><span class="sxs-lookup"><span data-stu-id="ffc33-122">Marking a milestone as **Ready to invoice** makes it available to be put on a draft invoice.</span></span>

<span data-ttu-id="ffc33-123">当多客户合同子项具有固定价格计费方法时，将为合同子项中的每个客户创建里程碑。</span><span class="sxs-lookup"><span data-stu-id="ffc33-123">When multi-customer contract lines have a fixed price billing method, a milestone is created for each customer on the contract line.</span></span> <span data-ttu-id="ffc33-124">可以创建里程碑，然后将其拆分为各个特定于客户的里程碑记录。</span><span class="sxs-lookup"><span data-stu-id="ffc33-124">A milestone can be created and then split into individual customer-specific milestone records.</span></span> <span data-ttu-id="ffc33-125">此拆分是内部的，依据为合同子项中的每个客户定义的计费百分比拆分。</span><span class="sxs-lookup"><span data-stu-id="ffc33-125">This split is internal and in accordance with the billing percentage split defined for each customer on the contract line.</span></span> <span data-ttu-id="ffc33-126">在 **固定价格里程碑** 视图中，您将看到各个特定于客户的里程碑记录。</span><span class="sxs-lookup"><span data-stu-id="ffc33-126">In the **Fixed Price Milestones** view, you will see the individual customer-specific milestone records.</span></span> <span data-ttu-id="ffc33-127">可以从此视图将这些里程碑记录中的各个记录单独标记为 **可开票**。</span><span class="sxs-lookup"><span data-stu-id="ffc33-127">Each of these milestone records can be marked as **Ready to Invoice** separately from this view.</span></span> <span data-ttu-id="ffc33-128">当一个或多个相关里程碑拆分被标记为 **已准备好开单** 时，标题状态会从 **未开始** 更新为 **正在进行**。</span><span class="sxs-lookup"><span data-stu-id="ffc33-128">When one or more of the related milestone splits are marked as **Ready to Invoice**, the header status updates to **In Progress** from **Not Started**.</span></span> <span data-ttu-id="ffc33-129">当所有里程碑拆分均已开票时，标题里程碑状态会更新为 **已完成**。</span><span class="sxs-lookup"><span data-stu-id="ffc33-129">When all of the milestone splits are invoiced, the header milestone status updates to **Completed**.</span></span>

<span data-ttu-id="ffc33-130">草稿发票上的里程碑将在此视图中显示，其记帐状态为 **客户发票已创建**。</span><span class="sxs-lookup"><span data-stu-id="ffc33-130">A milestone on a draft invoice is shown in this view with a billing status of **Customer Invoice Created**.</span></span> <span data-ttu-id="ffc33-131">在确认草稿发票时，记录上的计费状态将更新为 **客户发票已过帐**。</span><span class="sxs-lookup"><span data-stu-id="ffc33-131">When the draft invoice is confirmed, the billing status on the record is updated to **Customer Invoice Posted**.</span></span> 

> [!NOTE] 
> <span data-ttu-id="ffc33-132">请勿使用自定义代码更新此状态值。</span><span class="sxs-lookup"><span data-stu-id="ffc33-132">Do not update this status value by using custom code.</span></span> <span data-ttu-id="ffc33-133">使用自定义代码更新这些状态值时，Project Operations 将无法正常运行。</span><span class="sxs-lookup"><span data-stu-id="ffc33-133">Project Operations doesn't function correctly when these status values are updated with custom code.</span></span>

## <a name="time-and-material-billing-backlog"></a><span data-ttu-id="ffc33-134">时间和材料记帐积压</span><span class="sxs-lookup"><span data-stu-id="ffc33-134">Time and Material Billing Backlog</span></span>

<span data-ttu-id="ffc33-135">**时间和材料计费积压** 视图列出系统中所有项目合同的所有未开票的未记帐实际销售额。</span><span class="sxs-lookup"><span data-stu-id="ffc33-135">The **Time and Material Billing Backlog** view lists all unbilled sales actuals across all project contracts in the system that haven't been invoiced.</span></span> <span data-ttu-id="ffc33-136">从此视图，可以将单个或多个未记帐实际销售额标记为 **可开票** 或 **未准备好开发票**。</span><span class="sxs-lookup"><span data-stu-id="ffc33-136">Single or multiple unbilled sales actuals can be marked as **Ready to Invoice** or **Not Ready to Invoice** from this view.</span></span> <span data-ttu-id="ffc33-137">将未记帐实际销售额标记为 **可开票**，可以将它放到草稿发票上。</span><span class="sxs-lookup"><span data-stu-id="ffc33-137">Marking an unbilled sales actual as **Ready to Invoice** makes it available to be put on a draft invoice.</span></span>

<span data-ttu-id="ffc33-138">**不超出** 状态为 **失败** 的未记帐实际销售额无法标记为 **可开票**。</span><span class="sxs-lookup"><span data-stu-id="ffc33-138">Unbilled sales actuals with a **Not-to-Exceed** status of **Failed** can't be marked as **Ready to Invoice**.</span></span> <span data-ttu-id="ffc33-139">如果需要将实际值标记为 **已准备好开单**，请重置已提交合同子项上其他实际值的状态，然后重新评估 **上限** 状态。</span><span class="sxs-lookup"><span data-stu-id="ffc33-139">If the actuals need to be marked as **Ready to Invoice**, reset the status on other actuals on the contract line that are committed, and then re-evaluate the **Not-to-Exceed** status.</span></span>

<span data-ttu-id="ffc33-140">如果多客户合同子项具有时间和材料计费方法，在时间和支出被批准时，将根据为每个客户定义的计费百分比拆分，为合同子项上的每个客户创建未记帐实际销售额。</span><span class="sxs-lookup"><span data-stu-id="ffc33-140">If multi-customer contract lines have a time and material billing method, when time and expenses are approved, one unbilled sales actual is created for each customer on the contract line according to the billing percentage split defined for each of the customers.</span></span> <span data-ttu-id="ffc33-141">在 **时间和材料计费积压** 视图中，您将看到各个特定于客户的未记帐实际销售额。</span><span class="sxs-lookup"><span data-stu-id="ffc33-141">In the **Time and Material Billing Backlog** view, you will see these individual customer-specific unbilled sales actuals.</span></span> <span data-ttu-id="ffc33-142">可以从此视图将这些未记帐实际销售额记录中的各个记录单独标记为 **可开票**。</span><span class="sxs-lookup"><span data-stu-id="ffc33-142">Each of these unbilled sales actual records can be marked as **Ready to Invoice** separately from this view.</span></span>

<span data-ttu-id="ffc33-143">草稿发票上的未记帐销售实际值将显示在此视图中，其记帐状态为 **客户发票已创建**。</span><span class="sxs-lookup"><span data-stu-id="ffc33-143">An unbilled sales actual that's on a draft invoice is shown in this view with a billing status of **Customer Invoice Created**.</span></span> <span data-ttu-id="ffc33-144">确认草稿发票后，此记录上的记帐状态将更新为 **客户发票已过帐**。</span><span class="sxs-lookup"><span data-stu-id="ffc33-144">When the draft invoice is confirmed, the billing status on this record is updated to **Customer Invoice Posted**.</span></span> 

> [!NOTE] 
> <span data-ttu-id="ffc33-145">请勿使用自定义代码更新此状态值。</span><span class="sxs-lookup"><span data-stu-id="ffc33-145">Do not update this status value by using custom code.</span></span> <span data-ttu-id="ffc33-146">使用自定义代码更新这些状态值时，Project Operations 将无法正常运行。</span><span class="sxs-lookup"><span data-stu-id="ffc33-146">Project Operations doesn't function correctly when these status values are updated with custom code.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
