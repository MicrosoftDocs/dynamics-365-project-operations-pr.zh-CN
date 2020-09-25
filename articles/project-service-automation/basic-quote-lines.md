---
title: 报价单和报价单明细
description: 本主题提供有关报价单和报价单明细的信息。
author: rumant
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 3/01/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: c56dce28-0c87-4cec-9720-c8331d4ca40b
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 649fbd137a0f79c6ec513497aa4eddfe63d64a56
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/24/2020
ms.locfileid: "3749620"
---
# <a name="quotes-and-quote-lines"></a><span data-ttu-id="49ac2-103">报价单和报价单明细</span><span class="sxs-lookup"><span data-stu-id="49ac2-103">Quotes and quote lines</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="49ac2-104">在 Dynamics 365 Project Service Automation 中，有两种类型的报价单：项目报价单和销售报价单。</span><span class="sxs-lookup"><span data-stu-id="49ac2-104">In Dynamics 365 Project Service Automation, there are two types of quotes: project quotes and sales quotes.</span></span> <span data-ttu-id="49ac2-105">下面是这两种类型的差别：</span><span class="sxs-lookup"><span data-stu-id="49ac2-105">The two types differ in the following ways:</span></span>

- <span data-ttu-id="49ac2-106">在销售报价单中，明细项只有一个网格。</span><span class="sxs-lookup"><span data-stu-id="49ac2-106">On a sales quote, there is only one grid for line items.</span></span> <span data-ttu-id="49ac2-107">在项目报价单中，明细项有两个网格：一个针对项目明细，一个针对产品明细。</span><span class="sxs-lookup"><span data-stu-id="49ac2-107">On a project quote, there are two grids for line items: one for project lines and one for product lines.</span></span>
- <span data-ttu-id="49ac2-108">销售报价单支持激活和修订。</span><span class="sxs-lookup"><span data-stu-id="49ac2-108">A sales quote supports activation and revisions.</span></span> <span data-ttu-id="49ac2-109">项目报价单不支持这些处理。</span><span class="sxs-lookup"><span data-stu-id="49ac2-109">A project quote doesn’t support those processes.</span></span>
- <span data-ttu-id="49ac2-110">可以向一个销售报价单附加多个订单。</span><span class="sxs-lookup"><span data-stu-id="49ac2-110">You can attach multiple orders to a sales quote.</span></span> <span data-ttu-id="49ac2-111">只能向一个项目报价单附加一个项目合同。</span><span class="sxs-lookup"><span data-stu-id="49ac2-111">You can attach only one project contract to a project quote.</span></span>
- <span data-ttu-id="49ac2-112">销售报价单赢单后可以不结束相关商机。</span><span class="sxs-lookup"><span data-stu-id="49ac2-112">You can win a sales quote and keep the related opportunity open.</span></span> <span data-ttu-id="49ac2-113">项目报价单赢单后将结束相关商机。</span><span class="sxs-lookup"><span data-stu-id="49ac2-113">After a project quote is won, the related opportunity is closed.</span></span>
- <span data-ttu-id="49ac2-114">项目报价单中不包含项目报价单中包含的一些字段和概念。</span><span class="sxs-lookup"><span data-stu-id="49ac2-114">A sales quote doesn't include some fields and concepts that are included on a project quote has fields.</span></span> <span data-ttu-id="49ac2-115">这些字段包括**合同签订部门**、**客户经理**和**帐单邮寄地址联系人姓名**。</span><span class="sxs-lookup"><span data-stu-id="49ac2-115">The fields include **Contracting Unit**, **Account Manager**, and **Bill to Contact Name**.</span></span>  
- <span data-ttu-id="49ac2-116">也可以通过一个名称为**类型**且基于选项集的字段识别销售报价单和项目报价单。</span><span class="sxs-lookup"><span data-stu-id="49ac2-116">Sales quotes and project quotes are also identified by an option set–based field that is named **Type**.</span></span> <span data-ttu-id="49ac2-117">对于销售报价单，此字段的值为**基于物料**。</span><span class="sxs-lookup"><span data-stu-id="49ac2-117">For a sales quote, this field has the value **Item-based**.</span></span> <span data-ttu-id="49ac2-118">对于项目报价单，其值为**基于工作**。</span><span class="sxs-lookup"><span data-stu-id="49ac2-118">For a project quote, it has the value **Work-based**.</span></span>

<span data-ttu-id="49ac2-119">此主题主要介绍项目报价单的详细信息。</span><span class="sxs-lookup"><span data-stu-id="49ac2-119">This topic will focus on the details of project quotes.</span></span>

<span data-ttu-id="49ac2-120">PSA 中的项目报价单可以包含多个明细项或报价单明细。</span><span class="sxs-lookup"><span data-stu-id="49ac2-120">A project quote in PSA can have multiple line items or quote lines.</span></span> <span data-ttu-id="49ac2-121">实际上，项目报价单有两个明细项网格。</span><span class="sxs-lookup"><span data-stu-id="49ac2-121">In fact, a project quote has two grids for line items.</span></span> <span data-ttu-id="49ac2-122">一个网格针对基于项目且可用于执行更详细估算的明细。</span><span class="sxs-lookup"><span data-stu-id="49ac2-122">One grid is for project-based lines that allow for detailed estimations.</span></span> <span data-ttu-id="49ac2-123">另一个网格针对基于产品且使用简单单价和基于数量的方法的明细。</span><span class="sxs-lookup"><span data-stu-id="49ac2-123">The other grid is for product-based lines that use a simple unit price and quantity-based approach.</span></span>

- <span data-ttu-id="49ac2-124">**基于项目** – 估算需要多少工作量后确定金额（报价值）。</span><span class="sxs-lookup"><span data-stu-id="49ac2-124">**Project-based** – The amount (quoted value) is determined after you estimate how much work is required.</span></span> <span data-ttu-id="49ac2-125">可以在高级别估算工作量，也可以直接作为每项报价单明细下的明细详细信息估算。</span><span class="sxs-lookup"><span data-stu-id="49ac2-125">You can estimate work at a high level, or you can estimate it directly as line details below each quote line.</span></span> <span data-ttu-id="49ac2-126">最后，可以使用下面和项目计划基于基础估算来估算工作量。</span><span class="sxs-lookup"><span data-stu-id="49ac2-126">Finally, you can estimate work based on ground-up estimates, by using a project and project plan.</span></span> <span data-ttu-id="49ac2-127">只有使用 Project Service Automation 创建且基于项目的报价单中才有基于项目的报价单明细。</span><span class="sxs-lookup"><span data-stu-id="49ac2-127">Project-based quote lines are found only in project-based quotes that are created by using Project Service Automation.</span></span> <span data-ttu-id="49ac2-128">这种类型的报价单明细是 Microsoft Dynamics 365 Sales 中支持的目录外报价单明细的自定义形式。</span><span class="sxs-lookup"><span data-stu-id="49ac2-128">This type of quote line is a customized form of the write-in quote lines that are available in Microsoft Dynamics 365 Sales.</span></span>
- <span data-ttu-id="49ac2-129">**基于产品** – 基于所售单位数量和产品的销售单价确定金额（报价值）。</span><span class="sxs-lookup"><span data-stu-id="49ac2-129">**Product-based** – The amount (quoted value) is determined based on the quantity of units that is sold and the product's unit sales price.</span></span> <span data-ttu-id="49ac2-130">基于产品的明细中的产品可以来自 Sales 中的产品目录，也可以是您定义的产品。</span><span class="sxs-lookup"><span data-stu-id="49ac2-130">The product on a product-based line can come from a product catalog in Sales, or it can be a product that you define.</span></span> <span data-ttu-id="49ac2-131">使用 PSA 创建且基于项目的报价单也支持这种类型的报价单明细。</span><span class="sxs-lookup"><span data-stu-id="49ac2-131">This type of quote line is also available on project-based quotes that are created by using PSA.</span></span>

<span data-ttu-id="49ac2-132">报价单中的金额是基于产品的明细和基于项目的明细的总和。</span><span class="sxs-lookup"><span data-stu-id="49ac2-132">The amount on a quote is the total across the product-based lines and the project-based lines.</span></span>

> [!NOTE]
> <span data-ttu-id="49ac2-133">报价单和报价单明细在 PSA 中不是必需的。</span><span class="sxs-lookup"><span data-stu-id="49ac2-133">Quotes and quote lines aren't required in PSA.</span></span> <span data-ttu-id="49ac2-134">可以从项目合同（已售项目）开始项目流程。</span><span class="sxs-lookup"><span data-stu-id="49ac2-134">You can start the project process with a project contract (sold project).</span></span> <span data-ttu-id="49ac2-135">但是，始终需要商机，无论从报价单还是项目合同开始。</span><span class="sxs-lookup"><span data-stu-id="49ac2-135">However, an opportunity is always required, regardless of whether you start with a quote or a project contract.</span></span>

## <a name="project-based-quote-lines"></a><span data-ttu-id="49ac2-136">基于项目的报价单明细</span><span class="sxs-lookup"><span data-stu-id="49ac2-136">Project-based quote lines</span></span>

<span data-ttu-id="49ac2-137">PSA 中基于项目的报价单明细采用以下记帐方法：</span><span class="sxs-lookup"><span data-stu-id="49ac2-137">A project-based quote line in PSA has the following billing methods:</span></span>

- <span data-ttu-id="49ac2-138">时间和材料</span><span class="sxs-lookup"><span data-stu-id="49ac2-138">Time and material</span></span>
- <span data-ttu-id="49ac2-139">固定价格</span><span class="sxs-lookup"><span data-stu-id="49ac2-139">Fixed price</span></span>

### <a name="time-and-material"></a><span data-ttu-id="49ac2-140">时间和材料</span><span class="sxs-lookup"><span data-stu-id="49ac2-140">Time and material</span></span>

<span data-ttu-id="49ac2-141">时间和材料记帐方法基于消耗。</span><span class="sxs-lookup"><span data-stu-id="49ac2-141">The Time and material billing method is based on consumption.</span></span> <span data-ttu-id="49ac2-142">选择此记帐方法时，项目产生成本时向客户开票。</span><span class="sxs-lookup"><span data-stu-id="49ac2-142">When you select this billing method, the customer is invoiced as the project incurs costs.</span></span> <span data-ttu-id="49ac2-143">按照基于日期的定期频率创建发票。</span><span class="sxs-lookup"><span data-stu-id="49ac2-143">Invoices are created on a date-based periodic frequency.</span></span> <span data-ttu-id="49ac2-144">在销售流程中，时间和材料组成部分的报价值仅向客户提供最终成本的估算。</span><span class="sxs-lookup"><span data-stu-id="49ac2-144">During the sales process, the quoted value of a time-and-material component gives only an estimate of the final cost to the customer.</span></span> <span data-ttu-id="49ac2-145">供应商不承诺自己完全按照报价值完成项目。</span><span class="sxs-lookup"><span data-stu-id="49ac2-145">The vendor doesn't commit itself to completing the project at exactly the quoted value.</span></span> <span data-ttu-id="49ac2-146">时间和材料组成部分会加大客户的风险。</span><span class="sxs-lookup"><span data-stu-id="49ac2-146">Time-and-material components increase the customer's risk.</span></span> <span data-ttu-id="49ac2-147">客户可能希望协商更多底线条款以将风险降到最低。</span><span class="sxs-lookup"><span data-stu-id="49ac2-147">Customers might want to negotiate additional not-to-exceed clauses to minimize their risk.</span></span> <span data-ttu-id="49ac2-148">PSA 不支持设置底线条款。</span><span class="sxs-lookup"><span data-stu-id="49ac2-148">PSA doesn't support setting not-to-exceed clauses.</span></span>

### <a name="fixed-price"></a><span data-ttu-id="49ac2-149">固定价格</span><span class="sxs-lookup"><span data-stu-id="49ac2-149">Fixed price</span></span>

<span data-ttu-id="49ac2-150">在固定价格记帐方法中，供应商承诺以固定成本向客户交付项目。</span><span class="sxs-lookup"><span data-stu-id="49ac2-150">In the Fixed price billing method, a vendor commits itself to delivering the project at a fixed cost to the customer.</span></span> <span data-ttu-id="49ac2-151">无论供应商在交付固定价格报价单明细时产生了多少成本，都按该报价单明细的报价值向客户记帐。</span><span class="sxs-lookup"><span data-stu-id="49ac2-151">The customer is billed the quoted value of the fixed-price quote line, regardless of the costs that the vendor incurs to deliver that quote line.</span></span> <span data-ttu-id="49ac2-152">固定价格报价单明细值按照以下方法记帐：</span><span class="sxs-lookup"><span data-stu-id="49ac2-152">The fixed-price quote line value is billed in one of the following ways:</span></span> 

- <span data-ttu-id="49ac2-153">作为项目开始或结束时，或达到项目里程碑时的包干金额。</span><span class="sxs-lookup"><span data-stu-id="49ac2-153">As a lump-sum amount at the start or end of the project, or when a project milestone is reached.</span></span> 
- <span data-ttu-id="49ac2-154">按报价单明细中固定值的等额分期付款的，基于时间的频率。</span><span class="sxs-lookup"><span data-stu-id="49ac2-154">At a date-based frequency of equal installments of the fixed value on the quote line.</span></span> <span data-ttu-id="49ac2-155">这些分期付款称为定期里程碑。</span><span class="sxs-lookup"><span data-stu-id="49ac2-155">These installments are known as periodic milestones.</span></span>
- <span data-ttu-id="49ac2-156">在货币值根据工作进程或达到的项目特定里程碑调整的分期付款中。</span><span class="sxs-lookup"><span data-stu-id="49ac2-156">In installments that have a monetary value that is aligned with the progress of work or specific milestones that are achieved on the project.</span></span> <span data-ttu-id="49ac2-157">在此情况下，每笔分期付款的值可能不同，但是全部累加必须等于报价单明细中的固定值。</span><span class="sxs-lookup"><span data-stu-id="49ac2-157">In this case, the value of each installment can differ, but they must all add up to the fixed value on the quote line.</span></span>

<span data-ttu-id="49ac2-158">在 PSA 中，固定价格报价单明细支持所有三种发票计划。</span><span class="sxs-lookup"><span data-stu-id="49ac2-158">PSA supports all three types of invoice schedules for fixed-price quote lines.</span></span>

## <a name="transaction-classification"></a><span data-ttu-id="49ac2-159">交易分类</span><span class="sxs-lookup"><span data-stu-id="49ac2-159">Transaction classification</span></span>

<span data-ttu-id="49ac2-160">专业服务组织通常按成本分类对其客户保价和开票。</span><span class="sxs-lookup"><span data-stu-id="49ac2-160">Professional service organizations typically quote and invoice their customers by classification of costs.</span></span> <span data-ttu-id="49ac2-161">在 PSA 中，成本使用以下交易分类表示：</span><span class="sxs-lookup"><span data-stu-id="49ac2-161">In PSA, costs are represented by the following transaction classifications:</span></span>

- <span data-ttu-id="49ac2-162">**时间** – 此分类表示项目的人工或人力资源时间的成本。</span><span class="sxs-lookup"><span data-stu-id="49ac2-162">**Time** – This classification represents the cost of labor or human resources' time on a project.</span></span>
- <span data-ttu-id="49ac2-163">**支出**: – 此分类表示项目的其他所有类型的支出。</span><span class="sxs-lookup"><span data-stu-id="49ac2-163">**Expense**: – This classification represents all other kinds of expenses on a project.</span></span> <span data-ttu-id="49ac2-164">因为支出的分类可能非常宽泛，所以大多数组织会创建子类别，如旅行、租车、酒店或办公用品。</span><span class="sxs-lookup"><span data-stu-id="49ac2-164">Because expenses can be broadly classified, most organizations create subcategories, such as travel, car rental, hotel, or office supplies.</span></span>
- <span data-ttu-id="49ac2-165">**费用** – 此分类表示对客户收取的杂项开销、租金和其他项目。</span><span class="sxs-lookup"><span data-stu-id="49ac2-165">**Fee** – This classification represents miscellaneous overhead, penalties, and other items that are charged to the customer.</span></span> 
- <span data-ttu-id="49ac2-166">**税** – 此分类表示用户在输入支出时加上的税额。</span><span class="sxs-lookup"><span data-stu-id="49ac2-166">**Tax** – This classification represents tax amounts that users add while they enter expenses.</span></span>
- <span data-ttu-id="49ac2-167">**材料交易** – 此分类表示已确认项目发票中产品明细内的实际值。</span><span class="sxs-lookup"><span data-stu-id="49ac2-167">**Material transaction** – This classification represents actuals from product lines on a confirmed project invoice.</span></span>
- <span data-ttu-id="49ac2-168">**里程碑** – PSA 中的固定价格记帐使用此分类。</span><span class="sxs-lookup"><span data-stu-id="49ac2-168">**Milestone** – This classification is used by the fixed-price billing logic in PSA.</span></span>

<span data-ttu-id="49ac2-169">可以为每项报价单明细关联这些交易分类中的一种或多种。</span><span class="sxs-lookup"><span data-stu-id="49ac2-169">One or more of these transaction classifications can be associated with each quote line.</span></span> <span data-ttu-id="49ac2-170">报价单赢单后，将把交易分类与报价单明细之间关联转给合同明细。</span><span class="sxs-lookup"><span data-stu-id="49ac2-170">After a quote is won, the mapping between transaction classification and quote line is transferred to the contract line.</span></span>
 
> ![将交易类型映射到报价单和合同明细的屏幕截图](media/basic-guide-5.png)
  
<span data-ttu-id="49ac2-172">例如，报价单中可能包含以下两项报价单明细：</span><span class="sxs-lookup"><span data-stu-id="49ac2-172">For example, a quote might contain the following two quote lines:</span></span> 
- <span data-ttu-id="49ac2-173">使用了其中适用时间和费用交易分类的时间和材料记帐方法的咨询工作。</span><span class="sxs-lookup"><span data-stu-id="49ac2-173">Consulting work that uses a Time and material billing method where time and fee transaction classifications are applicable.</span></span> <span data-ttu-id="49ac2-174">例如，根据所用时间和材料向客户开 **Dynamics AX 实施**示例项目所有时间和费用交易的发票。</span><span class="sxs-lookup"><span data-stu-id="49ac2-174">For example, all time and fee transactions for the **Dynamics AX Implementation** example project are invoiced to the customer based on the time and materials that are used.</span></span> 
- <span data-ttu-id="49ac2-175">采用固定价格记帐方法的相关旅行支出。</span><span class="sxs-lookup"><span data-stu-id="49ac2-175">Related travel expenses that use a Fixed price billing method.</span></span> <span data-ttu-id="49ac2-176">例如，按固定货币值向 **Dynamics AX 实施**示例项目的所有旅行支出开票。</span><span class="sxs-lookup"><span data-stu-id="49ac2-176">For example, all travel expenses for the **Dynamics AX Implementation** example project are invoiced at a fixed monetary value.</span></span>

> [!NOTE]
> <span data-ttu-id="49ac2-177">项目和与报价单明细或合同子项关联的**时间**、**支出**和**费用**交易分类的组合必须唯一。</span><span class="sxs-lookup"><span data-stu-id="49ac2-177">The combination of the project and transaction classifications of **Time**, **Expense**, and **Fee** that are associated with a quote line or contract line must be unique.</span></span> <span data-ttu-id="49ac2-178">如果将项目和交易分类的同一个组合与多项合同子项或报价单明细关联，PSA 将无法正常工作。</span><span class="sxs-lookup"><span data-stu-id="49ac2-178">If the same combination of project and transaction class is associated with more than one contract line or quote line, PSA won't work correctly.</span></span>

## <a name="billing-types"></a><span data-ttu-id="49ac2-179">记帐类型</span><span class="sxs-lookup"><span data-stu-id="49ac2-179">Billing types</span></span>

<span data-ttu-id="49ac2-180">**记帐类型**字段定义 PSA 中的应计费概念。</span><span class="sxs-lookup"><span data-stu-id="49ac2-180">The **Billing Type** field defines the concept of chargeability in PSA.</span></span> <span data-ttu-id="49ac2-181">它是可以具有以下值的选项集：</span><span class="sxs-lookup"><span data-stu-id="49ac2-181">It's an option set that has the following possible values:</span></span>

- <span data-ttu-id="49ac2-182">**应计费** – 此角色/类别累积的成本是推动项目执行的成本，是客户要为这项工作支付的费用。</span><span class="sxs-lookup"><span data-stu-id="49ac2-182">**Chargeable** – The cost that is accrued by this role/category is a direct cost that drives project execution, and the customer will pay for this work.</span></span> <span data-ttu-id="49ac2-183">可以以时间和材料或固定价格安排的形式管理付款。</span><span class="sxs-lookup"><span data-stu-id="49ac2-183">The payment can be administered as a time-and-material or fixed-price arrangement.</span></span> <span data-ttu-id="49ac2-184">但是，花费此时间的员工将获得自己的可记帐工作的认可。</span><span class="sxs-lookup"><span data-stu-id="49ac2-184">However, the employee who spends this time will receive the corresponding credit for his or her billable utilization.</span></span>
- <span data-ttu-id="49ac2-185">**非应计费** – 此角色/类别累积的成本被视为推动项目执行的成本，虽然客户不认可此工作或不为此工作付款。</span><span class="sxs-lookup"><span data-stu-id="49ac2-185">**Non-chargeable** – The cost that is accrued by this role/category is considered a direct cost that drives project execution, even though the customer doesn't recognize this fact and won't pay for this work.</span></span> <span data-ttu-id="49ac2-186">不认可花费此时间的员工的此项可记帐工作。</span><span class="sxs-lookup"><span data-stu-id="49ac2-186">The employee who spends this time won't be credited with billable utilization for it.</span></span>
- <span data-ttu-id="49ac2-187">**免费** – 此角色/类别累积的成本被视为推动项目执行的成本，并且客户认可这一点。</span><span class="sxs-lookup"><span data-stu-id="49ac2-187">**Complimentary** – The cost that is accrued by this role/category is considered a direct cost that drives project execution, and the customer recognizes this fact.</span></span> <span data-ttu-id="49ac2-188">认可花费此时间的员工的可记帐工作。</span><span class="sxs-lookup"><span data-stu-id="49ac2-188">The employee who spends this time will be credited for billable utilization for it.</span></span> <span data-ttu-id="49ac2-189">但是不向客户收取此项成本的费用。</span><span class="sxs-lookup"><span data-stu-id="49ac2-189">However, this cost isn't charged to the customer.</span></span>
- <span data-ttu-id="49ac2-190">**不可用** – 使用此选项跟踪不需要跟踪收入的内部项目的累积成本。</span><span class="sxs-lookup"><span data-stu-id="49ac2-190">**Not available** – The costs that are incurred on internal projects that don't require revenue tracking are tracked by using this option.</span></span>

## <a name="invoice-schedule"></a><span data-ttu-id="49ac2-191">发票计划</span><span class="sxs-lookup"><span data-stu-id="49ac2-191">Invoice schedule</span></span>

<span data-ttu-id="49ac2-192">发票计划是要为项目开票的一系列日期。</span><span class="sxs-lookup"><span data-stu-id="49ac2-192">An invoice schedule is a series of dates when invoicing for a project occurs.</span></span> <span data-ttu-id="49ac2-193">（可选）在 PSA 中，可以为报价单明细创建发票计划。</span><span class="sxs-lookup"><span data-stu-id="49ac2-193">You can optionally create an invoice schedule on a quote line in PSA.</span></span> <span data-ttu-id="49ac2-194">每个报价单明细可以有自己的发票计划。</span><span class="sxs-lookup"><span data-stu-id="49ac2-194">Each quote line can have its own invoice schedule.</span></span> <span data-ttu-id="49ac2-195">若要创建发票计划，必须提供以下属性值：</span><span class="sxs-lookup"><span data-stu-id="49ac2-195">To create an invoice schedule, you must provide the following attribute values:</span></span>

- <span data-ttu-id="49ac2-196">记帐开始日期</span><span class="sxs-lookup"><span data-stu-id="49ac2-196">A billing start date</span></span> 
- <span data-ttu-id="49ac2-197">表示项目记帐结束日期的交付日期。</span><span class="sxs-lookup"><span data-stu-id="49ac2-197">A delivery date that represents the billing end date on the project</span></span>
- <span data-ttu-id="49ac2-198">发票频率</span><span class="sxs-lookup"><span data-stu-id="49ac2-198">An invoice frequency</span></span>

<span data-ttu-id="49ac2-199">PSA 使用这些属性值生成一组要开票的暂定日期。</span><span class="sxs-lookup"><span data-stu-id="49ac2-199">PSA uses these three attribute values to generate a tentative set of dates to establish invoicing on.</span></span>

## <a name="invoice-frequency"></a><span data-ttu-id="49ac2-200">发票频率</span><span class="sxs-lookup"><span data-stu-id="49ac2-200">Invoice frequency</span></span>

<span data-ttu-id="49ac2-201">发票频率是一种实体，其中存储的属性值可帮助表示发票的创建频率。</span><span class="sxs-lookup"><span data-stu-id="49ac2-201">Invoice frequency is an entity that stores attribute values that help express the frequency of invoice creation.</span></span> <span data-ttu-id="49ac2-202">以下属性表示或定义发票频率实体：</span><span class="sxs-lookup"><span data-stu-id="49ac2-202">The following attributes express or define the Invoice frequency entity:</span></span>

- <span data-ttu-id="49ac2-203">**时间段** - 支持月、两周和周时间段。</span><span class="sxs-lookup"><span data-stu-id="49ac2-203">**Period** - Monthly, biweekly, and weekly periods are supported.</span></span> 
- <span data-ttu-id="49ac2-204">**每个时间段的运行次数** - 对于周和两周时间段，只能为每个时间段定义一次运行。</span><span class="sxs-lookup"><span data-stu-id="49ac2-204">**Runs per period** - For weekly and biweekly periods, you can define only one run per period.</span></span> <span data-ttu-id="49ac2-205">对于月时间段，可以为每个时间段定义一到四次运行。</span><span class="sxs-lookup"><span data-stu-id="49ac2-205">For monthly periods, you can define between one and four runs per period.</span></span> 
- <span data-ttu-id="49ac2-206">**运行天数** – 应该开票的运行天数。</span><span class="sxs-lookup"><span data-stu-id="49ac2-206">**Days of run** – The days when invoicing should be run.</span></span> <span data-ttu-id="49ac2-207">可以以两种方式配置此属性：</span><span class="sxs-lookup"><span data-stu-id="49ac2-207">You can configure this attribute in two ways:</span></span>
  - <span data-ttu-id="49ac2-208">**工作日** - 例如，可指定每个星期一或每隔一个星期一运行开票。</span><span class="sxs-lookup"><span data-stu-id="49ac2-208">**Weekdays** - For example, you can specify that invoicing is run every Monday or every second Monday.</span></span> <span data-ttu-id="49ac2-209">必须将开票设置为在工作日运行的客户可能会首选这种配置。</span><span class="sxs-lookup"><span data-stu-id="49ac2-209">Customers who must set invoicing to run on a working day might prefer this kind of configuration..</span></span> 
  - <span data-ttu-id="49ac2-210">**日历日** - 例如，可指定在每月十七号或二十一号运行开票。</span><span class="sxs-lookup"><span data-stu-id="49ac2-210">**Calendar days** - For example, you can specify that invoicing is run on the seventh and twenty-first days of every month.</span></span> <span data-ttu-id="49ac2-211">某些组织可能首选这种配置，因为可以帮助确保每月按固定计划运行开票。</span><span class="sxs-lookup"><span data-stu-id="49ac2-211">Some organizations might prefer this kind of configuration, because it helps guarantee that invoicing in run on a fixed schedule every month.</span></span>
  
### <a name="invoice-schedule-for-a-fixed-price-quote-line"></a><span data-ttu-id="49ac2-212">固定价格报价单明细的发票计划</span><span class="sxs-lookup"><span data-stu-id="49ac2-212">Invoice schedule for a fixed-price quote line</span></span>

<span data-ttu-id="49ac2-213">对于固定价格报价单明细，可使用**发票计划**网格创建等于报价单明细值的记帐里程碑。</span><span class="sxs-lookup"><span data-stu-id="49ac2-213">For a fixed-price quote line, you can use the **Invoice Schedule** grid to create billing milestones that equal the value of the quote line.</span></span>

- <span data-ttu-id="49ac2-214">若要创建等分记帐里程碑，请选择一个发票频率，输入报价单明细的记帐开始日期，然后在报价单标头的**摘要**部分中输入报价单的**请求的完成日期**。</span><span class="sxs-lookup"><span data-stu-id="49ac2-214">To create billing milestones that are equally divided, select an invoice frequency, enter the billing start date on the quote line, and select **Requested Completion Date** for the quote in the **Summary** section of the quote header.</span></span> <span data-ttu-id="49ac2-215">然后选择**生成定期里程碑**基于所选发票频率创建等分里程碑。</span><span class="sxs-lookup"><span data-stu-id="49ac2-215">Then select **Generate Periodic Milestones** to create equally split milestones based on the selected invoice frequency.</span></span> 
- <span data-ttu-id="49ac2-216">若要创建包干记帐里程碑，请创建一个里程碑，然后输入报价单明细值作为里程碑金额。</span><span class="sxs-lookup"><span data-stu-id="49ac2-216">To create a lump-sum billing milestone, create a milestone, and then enter the quote line value as the milestone amount.</span></span>
- <span data-ttu-id="49ac2-217">若要创建基于项目计划中的特定任务的记帐里程碑，请创建一个里程碑，然后将其映射到项目在记帐里程碑 UI 中的计划元素。</span><span class="sxs-lookup"><span data-stu-id="49ac2-217">To create billing milestones that are based on specific tasks in the project plan, create a milestone, and map it to the project's schedule element in the billing milestone UI.</span></span>