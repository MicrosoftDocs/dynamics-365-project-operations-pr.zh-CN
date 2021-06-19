---
title: 收入确认概述
description: 本主题提供有关 Project Operations 中的收入确认的信息。
author: sigitac
ms.date: 11/16/2020
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: f5f962572c6ec0298d2d91d33f83e4120a498a6f
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/10/2021
ms.locfileid: "6013745"
---
# <a name="revenue-recognition-overview"></a><span data-ttu-id="16ba4-103">收入确认概述</span><span class="sxs-lookup"><span data-stu-id="16ba4-103">Revenue recognition overview</span></span>

<span data-ttu-id="16ba4-104">_**适用于：** 面向资源/非库存场景的 Project Operations_</span><span class="sxs-lookup"><span data-stu-id="16ba4-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="16ba4-105">在 Dynamics 365 Project Operations 中，收入确认原则因项目或部分项目的选定记帐方法而异。</span><span class="sxs-lookup"><span data-stu-id="16ba4-105">In Dynamics 365 Project Operations, revenue recognition principles vary based on the selected billing method for a project or portion of the project.</span></span> <span data-ttu-id="16ba4-106">本主题提供有关 Project Operations 中的收入确认的信息。</span><span class="sxs-lookup"><span data-stu-id="16ba4-106">This topic provides information about revenue recognition in Project Operations.</span></span>

## <a name="transactions-accounted-using-time-and-material-billing-method"></a><span data-ttu-id="16ba4-107">使用时间和材料记帐方法记帐的交易</span><span class="sxs-lookup"><span data-stu-id="16ba4-107">Transactions accounted using time and material billing method</span></span>

- <span data-ttu-id="16ba4-108">成本和收入确认相互关联。</span><span class="sxs-lookup"><span data-stu-id="16ba4-108">Cost and revenue recognition are connected.</span></span> <span data-ttu-id="16ba4-109">交易成本和未记帐销售额使用 [Project Operations 集成日记帐](../project-accounting/project-operations-integration-journal.md)过帐。</span><span class="sxs-lookup"><span data-stu-id="16ba4-109">Transaction cost and unbilled sales are posted using the [Project Operations Integration journal](../project-accounting/project-operations-integration-journal.md).</span></span>
- <span data-ttu-id="16ba4-110">项目成本和收入配置文件确定是否将未记帐销售交易过帐到总帐。</span><span class="sxs-lookup"><span data-stu-id="16ba4-110">Project cost and revenue profile determine if unbilled sales transactions are posted to the general ledger.</span></span> <span data-ttu-id="16ba4-111">如果选择了 **应计收入**，则系统在过帐期间会使用 **WIP 销售值** 和 **应计收入销售值** 帐户。</span><span class="sxs-lookup"><span data-stu-id="16ba4-111">If **Accrue revenue** is selected, the system uses the **WIP sales value** and the **Accrued revenue sales value** accounts during posting.</span></span> <span data-ttu-id="16ba4-112">下面是此方法的示例。</span><span class="sxs-lookup"><span data-stu-id="16ba4-112">The following is an example of this method.</span></span>  

  | <span data-ttu-id="16ba4-113">交易记录类型</span><span class="sxs-lookup"><span data-stu-id="16ba4-113">Transaction type</span></span> | <span data-ttu-id="16ba4-114">借方/贷方</span><span class="sxs-lookup"><span data-stu-id="16ba4-114">Debit/Credit</span></span> | <span data-ttu-id="16ba4-115">应收总额</span><span class="sxs-lookup"><span data-stu-id="16ba4-115">Amount</span></span> |
  | --- | --- | --- |
  | <span data-ttu-id="16ba4-116">WIP 销售值</span><span class="sxs-lookup"><span data-stu-id="16ba4-116">WIP Sales value</span></span> | <span data-ttu-id="16ba4-117">借方</span><span class="sxs-lookup"><span data-stu-id="16ba4-117">Debit</span></span> | <span data-ttu-id="16ba4-118">100</span><span class="sxs-lookup"><span data-stu-id="16ba4-118">100</span></span> |
  | <span data-ttu-id="16ba4-119">应计收入销售值</span><span class="sxs-lookup"><span data-stu-id="16ba4-119">Accrued revenue sales value</span></span> | <span data-ttu-id="16ba4-120">贷方</span><span class="sxs-lookup"><span data-stu-id="16ba4-120">Credit</span></span> | <span data-ttu-id="16ba4-121">100</span><span class="sxs-lookup"><span data-stu-id="16ba4-121">100</span></span> |

- <span data-ttu-id="16ba4-122">开票期间确认了收入。</span><span class="sxs-lookup"><span data-stu-id="16ba4-122">Revenue is recognized during invoicing.</span></span> <span data-ttu-id="16ba4-123">系统在过帐期间使用 **开票收入** 帐户。</span><span class="sxs-lookup"><span data-stu-id="16ba4-123">The system uses the **Invoiced revenue** account during posting.</span></span> <span data-ttu-id="16ba4-124">下面是此方法的示例。</span><span class="sxs-lookup"><span data-stu-id="16ba4-124">The following is an example of this method.</span></span>  

  | <span data-ttu-id="16ba4-125">交易记录类型</span><span class="sxs-lookup"><span data-stu-id="16ba4-125">Transaction type</span></span> | <span data-ttu-id="16ba4-126">借方/贷方</span><span class="sxs-lookup"><span data-stu-id="16ba4-126">Debit/Credit</span></span> | <span data-ttu-id="16ba4-127">应收总额</span><span class="sxs-lookup"><span data-stu-id="16ba4-127">Amount</span></span> |
  | --- | --- | --- |
  | <span data-ttu-id="16ba4-128">客户余额</span><span class="sxs-lookup"><span data-stu-id="16ba4-128">Customer balance</span></span> | <span data-ttu-id="16ba4-129">借方</span><span class="sxs-lookup"><span data-stu-id="16ba4-129">Debit</span></span> | <span data-ttu-id="16ba4-130">120</span><span class="sxs-lookup"><span data-stu-id="16ba4-130">120</span></span> |
  | <span data-ttu-id="16ba4-131">销售税应付款</span><span class="sxs-lookup"><span data-stu-id="16ba4-131">Sales tax payable</span></span> | <span data-ttu-id="16ba4-132">贷方</span><span class="sxs-lookup"><span data-stu-id="16ba4-132">Credit</span></span> | <span data-ttu-id="16ba4-133">20</span><span class="sxs-lookup"><span data-stu-id="16ba4-133">20</span></span> |
  | <span data-ttu-id="16ba4-134">已开票收入</span><span class="sxs-lookup"><span data-stu-id="16ba4-134">Invoiced Revenue</span></span> | <span data-ttu-id="16ba4-135">贷方</span><span class="sxs-lookup"><span data-stu-id="16ba4-135">Credit</span></span> | <span data-ttu-id="16ba4-136">100</span><span class="sxs-lookup"><span data-stu-id="16ba4-136">100</span></span> |

- <span data-ttu-id="16ba4-137">如果在过帐未记帐销售额时增加了收入，则系统将在开票时冲销应计收入。</span><span class="sxs-lookup"><span data-stu-id="16ba4-137">If revenue was accrued when the unbilled sales are posted, the system will reverse the accrued revenue at invoicing.</span></span>

  | <span data-ttu-id="16ba4-138">交易记录类型</span><span class="sxs-lookup"><span data-stu-id="16ba4-138">Transaction type</span></span> | <span data-ttu-id="16ba4-139">借方/贷方</span><span class="sxs-lookup"><span data-stu-id="16ba4-139">Debit/Credit</span></span> | <span data-ttu-id="16ba4-140">应收总额</span><span class="sxs-lookup"><span data-stu-id="16ba4-140">Amount</span></span> |
  | --- | --- | --- |
  | <span data-ttu-id="16ba4-141">WIP 销售值</span><span class="sxs-lookup"><span data-stu-id="16ba4-141">WIP Sales value</span></span> | <span data-ttu-id="16ba4-142">贷方</span><span class="sxs-lookup"><span data-stu-id="16ba4-142">Credit</span></span> | <span data-ttu-id="16ba4-143">100</span><span class="sxs-lookup"><span data-stu-id="16ba4-143">100</span></span> |
  | <span data-ttu-id="16ba4-144">应计收入销售值</span><span class="sxs-lookup"><span data-stu-id="16ba4-144">Accrued revenue sales value</span></span> | <span data-ttu-id="16ba4-145">借方</span><span class="sxs-lookup"><span data-stu-id="16ba4-145">Debit</span></span> | <span data-ttu-id="16ba4-146">100</span><span class="sxs-lookup"><span data-stu-id="16ba4-146">100</span></span> |

## <a name="transactions-accounted-using-the-fixed-price-billing-method"></a><span data-ttu-id="16ba4-147">使用固定价格记帐方法记帐的交易</span><span class="sxs-lookup"><span data-stu-id="16ba4-147">Transactions accounted using the fixed price billing method</span></span>

- <span data-ttu-id="16ba4-148">成本和收入确认相互独立。</span><span class="sxs-lookup"><span data-stu-id="16ba4-148">Cost and revenue recognition are separate.</span></span> <span data-ttu-id="16ba4-149">交易成本使用 [Project Operations 集成日记帐](../project-accounting/project-operations-integration-journal.md)过帐。</span><span class="sxs-lookup"><span data-stu-id="16ba4-149">Transaction cost is posted using the [Project Operations Integration journal](../project-accounting/project-operations-integration-journal.md).</span></span> <span data-ttu-id="16ba4-150">系统未创建未记帐销售交易。</span><span class="sxs-lookup"><span data-stu-id="16ba4-150">Unbilled sales transactions aren't created.</span></span>
- <span data-ttu-id="16ba4-151">如果针对项目成本和收入配置文件将 **用于项目完成计算的原则** 设置为 **无 WIP**，则可以在开票期间确认收入。</span><span class="sxs-lookup"><span data-stu-id="16ba4-151">Revenue can be recognized during invoicing if the project cost and revenue profile have **Principle used for project completion calculations** set to **No WIP**.</span></span> <span data-ttu-id="16ba4-152">仅对短期、简单的项目使用此方法。</span><span class="sxs-lookup"><span data-stu-id="16ba4-152">Only use this method for short term, simple projects.</span></span>
- <span data-ttu-id="16ba4-153">可以将固定价格收入估算与 **已完成合同** 或 **完成百分比收入确认** 方法配合使用来确认收入。</span><span class="sxs-lookup"><span data-stu-id="16ba4-153">Revenue can be recognized using fixed price revenue estimates, with either the **Completed contract** or **Percent completion revenue recognition** method.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="16ba4-154">其他资源</span><span class="sxs-lookup"><span data-stu-id="16ba4-154">Additional resources</span></span>
[<span data-ttu-id="16ba4-155">“配置收费项目会计”文章</span><span class="sxs-lookup"><span data-stu-id="16ba4-155">Configure accounting for billable projects article</span></span>](../project-accounting/configure-accounting-billable-projects.md)

[<span data-ttu-id="16ba4-156">固定价格收入估算项目</span><span class="sxs-lookup"><span data-stu-id="16ba4-156">Fixed price revenue estimate projects</span></span>](rev-rec-percentage-completion-method.md)

[<span data-ttu-id="16ba4-157">管理收入估算</span><span class="sxs-lookup"><span data-stu-id="16ba4-157">Manage revenue estimates</span></span>](rev-rec-completed-contract-method.md)

[<span data-ttu-id="16ba4-158">完成成本计算方法</span><span class="sxs-lookup"><span data-stu-id="16ba4-158">Cost to complete methods</span></span>](cost-complete-methods.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]