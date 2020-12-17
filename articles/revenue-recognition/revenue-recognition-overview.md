---
title: 收入确认概述
description: 本主题提供有关 Project Operations 中的收入确认的信息。
author: sigitac
manager: Annbe
ms.date: 11/16/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 6844f4c5d4cda8a6a901b0302448f70f4c597f5d
ms.sourcegitcommit: 2d399bc9d07807626f0d6b2d0cf304240c47591c
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/17/2020
ms.locfileid: "4531368"
---
# <a name="revenue-recognition-overview"></a><span data-ttu-id="ac8fb-103">收入确认概述</span><span class="sxs-lookup"><span data-stu-id="ac8fb-103">Revenue recognition overview</span></span>

<span data-ttu-id="ac8fb-104">_**适用于：** 面向资源/非库存场景的 Project Operations_</span><span class="sxs-lookup"><span data-stu-id="ac8fb-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="ac8fb-105">在 Dynamics 365 Project Operations 中，收入确认原则因项目或部分项目的选定记帐方法而异。</span><span class="sxs-lookup"><span data-stu-id="ac8fb-105">In Dynamics 365 Project Operations, revenue recognition principles vary based on the selected billing method for a project or portion of the project.</span></span> <span data-ttu-id="ac8fb-106">本主题提供有关 Project Operations 中的收入确认的信息。</span><span class="sxs-lookup"><span data-stu-id="ac8fb-106">This topic provides information about revenue recognition in Project Operations.</span></span>

## <a name="transactions-accounted-using-time-and-material-billing-method"></a><span data-ttu-id="ac8fb-107">使用时间和材料记帐方法记帐的交易</span><span class="sxs-lookup"><span data-stu-id="ac8fb-107">Transactions accounted using time and material billing method</span></span>

- <span data-ttu-id="ac8fb-108">成本和收入确认相互关联。</span><span class="sxs-lookup"><span data-stu-id="ac8fb-108">Cost and revenue recognition are connected.</span></span> <span data-ttu-id="ac8fb-109">交易成本和未记帐销售额使用 [Project Operations 集成日记帐](../project-accounting/project-operations-integration-journal.md)过帐。</span><span class="sxs-lookup"><span data-stu-id="ac8fb-109">Transaction cost and unbilled sales are posted using the [Project Operations Integration journal](../project-accounting/project-operations-integration-journal.md).</span></span>
- <span data-ttu-id="ac8fb-110">项目成本和收入配置文件确定是否将未记帐销售交易过帐到总帐。</span><span class="sxs-lookup"><span data-stu-id="ac8fb-110">Project cost and revenue profile determine if unbilled sales transactions are posted to the general ledger.</span></span> <span data-ttu-id="ac8fb-111">如果选择了 **应计收入**，则系统在过帐期间会使用 **WIP 销售值** 和 **应计收入销售值** 帐户。</span><span class="sxs-lookup"><span data-stu-id="ac8fb-111">If **Accrue revenue** is selected, the system uses the **WIP sales value** and the **Accrued revenue sales value** accounts during posting.</span></span> <span data-ttu-id="ac8fb-112">下面是此方法的示例。</span><span class="sxs-lookup"><span data-stu-id="ac8fb-112">The following is an example of this method.</span></span>  

  | <span data-ttu-id="ac8fb-113">交易记录类型</span><span class="sxs-lookup"><span data-stu-id="ac8fb-113">Transaction type</span></span> | <span data-ttu-id="ac8fb-114">借方/贷方</span><span class="sxs-lookup"><span data-stu-id="ac8fb-114">Debit/Credit</span></span> | <span data-ttu-id="ac8fb-115">应收总额</span><span class="sxs-lookup"><span data-stu-id="ac8fb-115">Amount</span></span> |
  | --- | --- | --- |
  | <span data-ttu-id="ac8fb-116">WIP 销售值</span><span class="sxs-lookup"><span data-stu-id="ac8fb-116">WIP Sales value</span></span> | <span data-ttu-id="ac8fb-117">借方</span><span class="sxs-lookup"><span data-stu-id="ac8fb-117">Debit</span></span> | <span data-ttu-id="ac8fb-118">100</span><span class="sxs-lookup"><span data-stu-id="ac8fb-118">100</span></span> |
  | <span data-ttu-id="ac8fb-119">应计收入销售值</span><span class="sxs-lookup"><span data-stu-id="ac8fb-119">Accrued revenue sales value</span></span> | <span data-ttu-id="ac8fb-120">贷方</span><span class="sxs-lookup"><span data-stu-id="ac8fb-120">Credit</span></span> | <span data-ttu-id="ac8fb-121">100</span><span class="sxs-lookup"><span data-stu-id="ac8fb-121">100</span></span> |

- <span data-ttu-id="ac8fb-122">开票期间确认了收入。</span><span class="sxs-lookup"><span data-stu-id="ac8fb-122">Revenue is recognized during invoicing.</span></span> <span data-ttu-id="ac8fb-123">系统在过帐期间使用 **开票收入** 帐户。</span><span class="sxs-lookup"><span data-stu-id="ac8fb-123">The system uses the **Invoiced revenue** account during posting.</span></span> <span data-ttu-id="ac8fb-124">下面是此方法的示例。</span><span class="sxs-lookup"><span data-stu-id="ac8fb-124">The following is an example of this method.</span></span>  

  | <span data-ttu-id="ac8fb-125">交易记录类型</span><span class="sxs-lookup"><span data-stu-id="ac8fb-125">Transaction type</span></span> | <span data-ttu-id="ac8fb-126">借方/贷方</span><span class="sxs-lookup"><span data-stu-id="ac8fb-126">Debit/Credit</span></span> | <span data-ttu-id="ac8fb-127">应收总额</span><span class="sxs-lookup"><span data-stu-id="ac8fb-127">Amount</span></span> |
  | --- | --- | --- |
  | <span data-ttu-id="ac8fb-128">客户余额</span><span class="sxs-lookup"><span data-stu-id="ac8fb-128">Customer balance</span></span> | <span data-ttu-id="ac8fb-129">借方</span><span class="sxs-lookup"><span data-stu-id="ac8fb-129">Debit</span></span> | <span data-ttu-id="ac8fb-130">120</span><span class="sxs-lookup"><span data-stu-id="ac8fb-130">120</span></span> |
  | <span data-ttu-id="ac8fb-131">销售税应付款</span><span class="sxs-lookup"><span data-stu-id="ac8fb-131">Sales tax payable</span></span> | <span data-ttu-id="ac8fb-132">贷方</span><span class="sxs-lookup"><span data-stu-id="ac8fb-132">Credit</span></span> | <span data-ttu-id="ac8fb-133">20</span><span class="sxs-lookup"><span data-stu-id="ac8fb-133">20</span></span> |
  | <span data-ttu-id="ac8fb-134">已开票收入</span><span class="sxs-lookup"><span data-stu-id="ac8fb-134">Invoiced Revenue</span></span> | <span data-ttu-id="ac8fb-135">贷方</span><span class="sxs-lookup"><span data-stu-id="ac8fb-135">Credit</span></span> | <span data-ttu-id="ac8fb-136">100</span><span class="sxs-lookup"><span data-stu-id="ac8fb-136">100</span></span> |

- <span data-ttu-id="ac8fb-137">如果在过帐未记帐销售额时增加了收入，则系统将在开票时冲销应计收入。</span><span class="sxs-lookup"><span data-stu-id="ac8fb-137">If revenue was accrued when the unbilled sales are posted, the system will reverse the accrued revenue at invoicing.</span></span>

  | <span data-ttu-id="ac8fb-138">交易记录类型</span><span class="sxs-lookup"><span data-stu-id="ac8fb-138">Transaction type</span></span> | <span data-ttu-id="ac8fb-139">借方/贷方</span><span class="sxs-lookup"><span data-stu-id="ac8fb-139">Debit/Credit</span></span> | <span data-ttu-id="ac8fb-140">应收总额</span><span class="sxs-lookup"><span data-stu-id="ac8fb-140">Amount</span></span> |
  | --- | --- | --- |
  | <span data-ttu-id="ac8fb-141">WIP 销售值</span><span class="sxs-lookup"><span data-stu-id="ac8fb-141">WIP Sales value</span></span> | <span data-ttu-id="ac8fb-142">贷方</span><span class="sxs-lookup"><span data-stu-id="ac8fb-142">Credit</span></span> | <span data-ttu-id="ac8fb-143">100</span><span class="sxs-lookup"><span data-stu-id="ac8fb-143">100</span></span> |
  | <span data-ttu-id="ac8fb-144">应计收入销售值</span><span class="sxs-lookup"><span data-stu-id="ac8fb-144">Accrued revenue sales value</span></span> | <span data-ttu-id="ac8fb-145">借方</span><span class="sxs-lookup"><span data-stu-id="ac8fb-145">Debit</span></span> | <span data-ttu-id="ac8fb-146">100</span><span class="sxs-lookup"><span data-stu-id="ac8fb-146">100</span></span> |

## <a name="transactions-accounted-using-the-fixed-price-billing-method"></a><span data-ttu-id="ac8fb-147">使用固定价格记帐方法记帐的交易</span><span class="sxs-lookup"><span data-stu-id="ac8fb-147">Transactions accounted using the fixed price billing method</span></span>

- <span data-ttu-id="ac8fb-148">成本和收入确认相互独立。</span><span class="sxs-lookup"><span data-stu-id="ac8fb-148">Cost and revenue recognition are separate.</span></span> <span data-ttu-id="ac8fb-149">交易成本使用 [Project Operations 集成日记帐](../project-accounting/project-operations-integration-journal.md)过帐。</span><span class="sxs-lookup"><span data-stu-id="ac8fb-149">Transaction cost is posted using the [Project Operations Integration journal](../project-accounting/project-operations-integration-journal.md).</span></span> <span data-ttu-id="ac8fb-150">系统未创建未记帐销售交易。</span><span class="sxs-lookup"><span data-stu-id="ac8fb-150">Unbilled sales transactions aren't created.</span></span>
- <span data-ttu-id="ac8fb-151">如果针对项目成本和收入配置文件将 **用于项目完成计算的原则** 设置为 **无 WIP**，则可以在开票期间确认收入。</span><span class="sxs-lookup"><span data-stu-id="ac8fb-151">Revenue can be recognized during invoicing if the project cost and revenue profile have **Principle used for project completion calculations** set to **No WIP**.</span></span> <span data-ttu-id="ac8fb-152">仅对短期、简单的项目使用此方法。</span><span class="sxs-lookup"><span data-stu-id="ac8fb-152">Only use this method for short term, simple projects.</span></span>
- <span data-ttu-id="ac8fb-153">可以将固定价格收入估算与 **已完成合同** 或 **完成百分比收入确认** 方法配合使用来确认收入。</span><span class="sxs-lookup"><span data-stu-id="ac8fb-153">Revenue can be recognized using fixed price revenue estimates, with either the **Completed contract** or **Percent completion revenue recognition** method.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="ac8fb-154">其他资源</span><span class="sxs-lookup"><span data-stu-id="ac8fb-154">Additional resources</span></span>
[<span data-ttu-id="ac8fb-155">“配置收费项目会计”文章</span><span class="sxs-lookup"><span data-stu-id="ac8fb-155">Configure accounting for billable projects article</span></span>](../project-accounting/configure-accounting-billable-projects.md)

[<span data-ttu-id="ac8fb-156">固定价格收入估算项目</span><span class="sxs-lookup"><span data-stu-id="ac8fb-156">Fixed price revenue estimate projects</span></span>](rev-rec-percentage-completion-method.md)

[<span data-ttu-id="ac8fb-157">管理收入估算</span><span class="sxs-lookup"><span data-stu-id="ac8fb-157">Manage revenue estimates</span></span>](rev-rec-completed-contract-method.md)

[<span data-ttu-id="ac8fb-158">完成成本计算方法</span><span class="sxs-lookup"><span data-stu-id="ac8fb-158">Cost to complete methods</span></span>](cost-complete-methods.md)
