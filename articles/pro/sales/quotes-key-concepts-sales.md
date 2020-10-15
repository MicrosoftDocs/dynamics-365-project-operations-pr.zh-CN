---
title: 项目报价单关键概念
description: 此主题提供有关在 Project Operations 中使用项目报价单的信息。
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 64d2fd9bab9452d71e8cd194fbab70edadf00b93
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/28/2020
ms.locfileid: "3896270"
---
# <a name="project-quote-key-concepts"></a><span data-ttu-id="dda38-103">项目报价单关键概念</span><span class="sxs-lookup"><span data-stu-id="dda38-103">Project quote key concepts</span></span>

<span data-ttu-id="dda38-104">_**适用于：** 精简部署 - 估价交易开票_</span><span class="sxs-lookup"><span data-stu-id="dda38-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="dda38-105">以下是在 Dynamics 365 Project Operations 中开始使用项目报价单之前要知道的关键概念：</span><span class="sxs-lookup"><span data-stu-id="dda38-105">The following are key concepts to be aware of before you begin using project quotes in Dynamics 365 Project Operations:</span></span>

## <a name="contracting-unit"></a><span data-ttu-id="dda38-106">合同签订部门</span><span class="sxs-lookup"><span data-stu-id="dda38-106">Contracting unit</span></span>

<span data-ttu-id="dda38-107">合同签订部门代表负责项目交付的部门或惯例。</span><span class="sxs-lookup"><span data-stu-id="dda38-107">The contracting unit represents the division or practice that owns the project delivery.</span></span> <span data-ttu-id="dda38-108">您可以为每个合同签订部门设置资源成本。</span><span class="sxs-lookup"><span data-stu-id="dda38-108">You can set up resource costs for each contracting unit.</span></span> <span data-ttu-id="dda38-109">当您在合同签订部门中为资源指定资源成本时，您还可以为向此合同签订部门借用的资源，或企业内的其他部门或惯例设置不同的成本率。</span><span class="sxs-lookup"><span data-stu-id="dda38-109">When you specify resource cost for a resource in the contracting unit, you will also be able to set up different cost rates for resources that this contracting unit borrows from, or other division or practices within the enterprise.</span></span> <span data-ttu-id="dda38-110">这些称为转让价格、资源借入或交换价格。</span><span class="sxs-lookup"><span data-stu-id="dda38-110">These are referred to as transfer prices, resource borrowing, or exchange prices.</span></span> <span data-ttu-id="dda38-111">设置从其他部门借入资源的成本时，您还可以选择以借出部门的货币设置这些成本率。</span><span class="sxs-lookup"><span data-stu-id="dda38-111">When you set up the cost of borrowing resources from other divisions, you can also choose to set up those cost rates in the currency of the lending division.</span></span>

## <a name="cost-currency"></a><span data-ttu-id="dda38-112">成本货币</span><span class="sxs-lookup"><span data-stu-id="dda38-112">Cost currency</span></span>

<span data-ttu-id="dda38-113">Project Operations 中的成本货币是报告成本使用的货币。</span><span class="sxs-lookup"><span data-stu-id="dda38-113">Cost currency in Project Operations is the currency in which costs are reported.</span></span> <span data-ttu-id="dda38-114">此货币源自报价单、合同和项目的**合同签订部门**字段所附的货币。</span><span class="sxs-lookup"><span data-stu-id="dda38-114">This currency is derived from the currency attached to the **Contracting unit** field on the quote, contract, and project.</span></span> <span data-ttu-id="dda38-115">可以任何货币针对项目记录成本。</span><span class="sxs-lookup"><span data-stu-id="dda38-115">Costs can be logged in any currency against a project.</span></span> <span data-ttu-id="dda38-116">但是，存在从记录的货币成本到项目的成本货币的货币转换。</span><span class="sxs-lookup"><span data-stu-id="dda38-116">However, there is currency conversion from the currency costs were recorded in, to the cost currency of the project.</span></span>

<span data-ttu-id="dda38-117">由于 CDS 平台中的汇率不能具有时效性，因此，如果您更新货币汇率，屏幕上的成本总计可能会随时间发生变化。</span><span class="sxs-lookup"><span data-stu-id="dda38-117">Because of the exchange rates in the CDS platform can't be date-effective, the on-screen totals for cost may change over time if you update currency exchange rates.</span></span> <span data-ttu-id="dda38-118">但是，数据库中记录的成本保持不变，因为金额以发生时所用的货币存储。</span><span class="sxs-lookup"><span data-stu-id="dda38-118">However, costs recorded in the database remain unchanged because the amounts are stored in the currency that they were incurred in.</span></span>

## <a name="sales-currency"></a><span data-ttu-id="dda38-119">销售货币</span><span class="sxs-lookup"><span data-stu-id="dda38-119">Sales currency</span></span>

<span data-ttu-id="dda38-120">Project Operations 中的销售货币是用于记录和显示预估和实际销售金额的货币。</span><span class="sxs-lookup"><span data-stu-id="dda38-120">Sales currency in Project Operations is the currency in which the estimated and actual sales amounts are recorded and shown.</span></span> <span data-ttu-id="dda38-121">它还是客户为交易开票所使用的货币。</span><span class="sxs-lookup"><span data-stu-id="dda38-121">It is also the currency in which the customer is invoiced for the deal.</span></span> <span data-ttu-id="dda38-122">在项目报价单上，销售货币默认来自客户记录，可以在创建报价单时进行更改。</span><span class="sxs-lookup"><span data-stu-id="dda38-122">On a project quote, the sales currency defaults from the customer or account record and can be changed when the quote is created.</span></span> <span data-ttu-id="dda38-123">保存报价单后，将无法更改销售货币。</span><span class="sxs-lookup"><span data-stu-id="dda38-123">After the quote is saved, the sales currency can't be changed.</span></span> <span data-ttu-id="dda38-124">产品和项目价目表默认基于报价单的销售货币。</span><span class="sxs-lookup"><span data-stu-id="dda38-124">Product and project price lists default based on the sales currency of the quote.</span></span>

<span data-ttu-id="dda38-125">与成本不同，销售值只能以销售货币记录。</span><span class="sxs-lookup"><span data-stu-id="dda38-125">Unlike costs, sales values can only be recorded in the Sales currency.</span></span>

## <a name="billing-method"></a><span data-ttu-id="dda38-126">计费方法</span><span class="sxs-lookup"><span data-stu-id="dda38-126">Billing method</span></span>

<span data-ttu-id="dda38-127">项目通常具有固定费用和基于使用的合同签订模型。</span><span class="sxs-lookup"><span data-stu-id="dda38-127">Projects typically have fixed fee and consumption-based contracting models.</span></span> <span data-ttu-id="dda38-128">这在项 Project Operations 中以**计费方法**表示，其具有两个值：时间和材料与固定价格。</span><span class="sxs-lookup"><span data-stu-id="dda38-128">This is represented in Project Operations as **Billing Method** and has two values, time and material and fixed price.</span></span>

- <span data-ttu-id="dda38-129">**时间和材料：** 这是一个基于使用的合同模型，其中，每个发生的成本都由相应的收入支持。</span><span class="sxs-lookup"><span data-stu-id="dda38-129">**Time and material:** This is a consumption-based contract model where each cost incurred is backed by corresponding revenue.</span></span> <span data-ttu-id="dda38-130">随着您预估或产生更多成本，相应的预估销售额和实际销售额也将增加。</span><span class="sxs-lookup"><span data-stu-id="dda38-130">As you estimate or incur more costs, the corresponding estimated and actual sales will also increase.</span></span> <span data-ttu-id="dda38-131">您可以在具有此计费方法的报价单明细上指定上限。</span><span class="sxs-lookup"><span data-stu-id="dda38-131">You can specify not-to-exceed limits on quote lines that have this billing method.</span></span> <span data-ttu-id="dda38-132">这会限制实际收入。</span><span class="sxs-lookup"><span data-stu-id="dda38-132">This will cap off the actual revenue.</span></span> <span data-ttu-id="dda38-133">预估收入不受上限的影响。</span><span class="sxs-lookup"><span data-stu-id="dda38-133">Estimated revenue is not impacted by not-to-exceed limits.</span></span>
- <span data-ttu-id="dda38-134">**固定价格：** 这是一个固定费用合同模型，指示销售值将独立于所产生的成本。</span><span class="sxs-lookup"><span data-stu-id="dda38-134">**Fixed price:** This is a fixed fee contract model that indicates the sales values will be independent of the costs incurred.</span></span> <span data-ttu-id="dda38-135">销售值是固定的，不会随着您预估或产生更多成本而改变。</span><span class="sxs-lookup"><span data-stu-id="dda38-135">The sales value is fixed and does not change as you estimate or incur more costs.</span></span>

## <a name="project-price-lists"></a><span data-ttu-id="dda38-136">项目价目表</span><span class="sxs-lookup"><span data-stu-id="dda38-136">Project price lists</span></span>

<span data-ttu-id="dda38-137">项目价目表是用于与时间、支出和其他项目相关组件的默认价格（不是成本率）的价目表。</span><span class="sxs-lookup"><span data-stu-id="dda38-137">Project price lists are price lists that are used to default prices, not cost rates, for time, expense, and other project-related components.</span></span> <span data-ttu-id="dda38-138">可以有多个价目表，每个价目表对于每个项目报价单可以有其自己的时效。</span><span class="sxs-lookup"><span data-stu-id="dda38-138">There can be multiple prices lists, and each list can have its own date effectivity for each project quote.</span></span> <span data-ttu-id="dda38-139">Project Operations 不支持项目价目表上有重叠的有效期。</span><span class="sxs-lookup"><span data-stu-id="dda38-139">Overlapping date effectivity on project price lists is not supported in Project Operations.</span></span>

## <a name="product-price-lists"></a><span data-ttu-id="dda38-140">产品价目表</span><span class="sxs-lookup"><span data-stu-id="dda38-140">Product price lists</span></span>

<span data-ttu-id="dda38-141">产品价目表是用于报价单中基于产品的行的默认价格（不是成本率）的价目表。</span><span class="sxs-lookup"><span data-stu-id="dda38-141">Product price lists are price lists that are used to default prices, not cost rates, for product-based lines on a quote.</span></span> <span data-ttu-id="dda38-142">每个报价单只有一个产品价目表。</span><span class="sxs-lookup"><span data-stu-id="dda38-142">There is only one product price list per quote.</span></span>

## <a name="transaction-classes"></a><span data-ttu-id="dda38-143">交易类</span><span class="sxs-lookup"><span data-stu-id="dda38-143">Transaction classes</span></span>

<span data-ttu-id="dda38-144">Project Operations 支持四种交易类：</span><span class="sxs-lookup"><span data-stu-id="dda38-144">Project Operations supports four types of transaction classes:</span></span>

- <span data-ttu-id="dda38-145">时间</span><span class="sxs-lookup"><span data-stu-id="dda38-145">Time</span></span>
- <span data-ttu-id="dda38-146">支出</span><span class="sxs-lookup"><span data-stu-id="dda38-146">Expense</span></span>
- <span data-ttu-id="dda38-147">材料</span><span class="sxs-lookup"><span data-stu-id="dda38-147">Material</span></span>
- <span data-ttu-id="dda38-148">费用</span><span class="sxs-lookup"><span data-stu-id="dda38-148">Fee</span></span>

<span data-ttu-id="dda38-149">成本和销售值可以基于时间、支出和材料交易类预估和生成。</span><span class="sxs-lookup"><span data-stu-id="dda38-149">Cost and sales values can be estimated and incurred on Time, Expense, and Material transaction classes.</span></span> <span data-ttu-id="dda38-150">费用属于仅收入交易类。</span><span class="sxs-lookup"><span data-stu-id="dda38-150">Fee is a revenue only class of transactions.</span></span>

## <a name="work-entities-and-billing-entities"></a><span data-ttu-id="dda38-151">工作实体和计费实体</span><span class="sxs-lookup"><span data-stu-id="dda38-151">Work entities and billing entities</span></span>

<span data-ttu-id="dda38-152">代表工作的实体是“项目”和“任务”。</span><span class="sxs-lookup"><span data-stu-id="dda38-152">Entities that represent work are Projects and Tasks.</span></span> <span data-ttu-id="dda38-153">代表计费的实体是“报价单明细”和“合同子项”。</span><span class="sxs-lookup"><span data-stu-id="dda38-153">Entities that represent billing are Quote lines and Contract lines.</span></span> <span data-ttu-id="dda38-154">您可以通过将不同的工作实体与报价单或合同子项相关联来将其链接到计费选项。</span><span class="sxs-lookup"><span data-stu-id="dda38-154">You can link different work entities to billing options by associating them with Quote or Contract lines.</span></span>

## <a name="multi-customer-deals"></a><span data-ttu-id="dda38-155">多客户交易</span><span class="sxs-lookup"><span data-stu-id="dda38-155">Multi-customer deals</span></span>

<span data-ttu-id="dda38-156">如果有多个客户要开票，则会发生多客户交易。</span><span class="sxs-lookup"><span data-stu-id="dda38-156">Multi-customer deals occur are when there is more than one customer to invoice.</span></span> <span data-ttu-id="dda38-157">常见的示例包括：</span><span class="sxs-lookup"><span data-stu-id="dda38-157">Common examples of this include:</span></span>

- <span data-ttu-id="dda38-158">**OEM 企业及其合作伙伴：** 合作伙伴和经销商销售具有增值服务的产品。</span><span class="sxs-lookup"><span data-stu-id="dda38-158">**OEM Enterprises and their partners:** Partners and resellers sell a product with value-added services.</span></span> <span data-ttu-id="dda38-159">这通常是在与客户进行特定交易期间，OEM 提供为项目的一部分提供资金时出现的场景。</span><span class="sxs-lookup"><span data-stu-id="dda38-159">This is usually a scenario where during a particular deal with a customer, the OEM offers to finance a portion of the project.</span></span> 

- <span data-ttu-id="dda38-160">**公共事业项目：** 地方政府的多个部门同意为一个项目提供资金，并根据先前商定的拆分方式开票。</span><span class="sxs-lookup"><span data-stu-id="dda38-160">**Public sector projects:** Multiple departments of a local government agree to fund a project and are invoiced according to a previously agreed split.</span></span> <span data-ttu-id="dda38-161">例如，学区和城市或地方政府部门同意为修建游泳池提供资金。</span><span class="sxs-lookup"><span data-stu-id="dda38-161">For example, a school district and the city or local government department agree to fund the building of a swimming pool.</span></span>

## <a name="invoice-schedules"></a><span data-ttu-id="dda38-162">发票计划</span><span class="sxs-lookup"><span data-stu-id="dda38-162">Invoice schedules</span></span>

<span data-ttu-id="dda38-163">发票计划特定于每个报价单明细，也是可选的。</span><span class="sxs-lookup"><span data-stu-id="dda38-163">Invoice schedules are specific to each quote line and are also optional.</span></span> <span data-ttu-id="dda38-164">发票计划根据特定开始和完成日期以及开票频率创建。</span><span class="sxs-lookup"><span data-stu-id="dda38-164">Invoice schedules are created based on certain start and finish dates and invoice frequency.</span></span> <span data-ttu-id="dda38-165">在配置自动发票创建流程时，在合同阶段使用发票计划。</span><span class="sxs-lookup"><span data-stu-id="dda38-165">Invoice schedules are used in the contract stage when the automatic invoice creation process is configured.</span></span> <span data-ttu-id="dda38-166">在报价单阶段，此计划是可选的。</span><span class="sxs-lookup"><span data-stu-id="dda38-166">In the quote stage, the schedules are optional.</span></span> <span data-ttu-id="dda38-167">在**报价单**阶段创建发票计划后，它们将被复制到报价单赢单时创建的项目合同中。</span><span class="sxs-lookup"><span data-stu-id="dda38-167">When invoice schedules are created in the **Quote** stage, they are copied to the project contract that is created when a project quote is won.</span></span>

## <a name="changes-from-dynamics-365-sales-quote"></a><span data-ttu-id="dda38-168">与 Dynamics 365 Sales 报价单的差异：</span><span class="sxs-lookup"><span data-stu-id="dda38-168">Changes from Dynamics 365 Sales quote:</span></span>

<span data-ttu-id="dda38-169">Project Operations 报价单基于 Dynamics 365 Sales 报价单构建。</span><span class="sxs-lookup"><span data-stu-id="dda38-169">Project Operations quotes are built on the Dynamics 365 Sales quotes.</span></span> <span data-ttu-id="dda38-170">但是，应注意一些重要的功能差异：</span><span class="sxs-lookup"><span data-stu-id="dda38-170">However, there are some important differences in functionality that you should be aware of:</span></span>

- <span data-ttu-id="dda38-171">不支持**修订**和**激活**操作。</span><span class="sxs-lookup"><span data-stu-id="dda38-171">The **Revise** and **Activate** actions are not supported.</span></span>
- <span data-ttu-id="dda38-172">Project Operations 报价单有两种不同类型的明细。</span><span class="sxs-lookup"><span data-stu-id="dda38-172">Project Operations quotes have two different types of lines.</span></span> <span data-ttu-id="dda38-173">一种用于项目，另一种用于产品。</span><span class="sxs-lookup"><span data-stu-id="dda38-173">One is for projects and the other is for products.</span></span>
- <span data-ttu-id="dda38-174">Project Operations 报价单具有自己的窗体和 UI 元素、业务规则、插件中的业务逻辑以及客户端脚本，这些让它们区别于 Sales 报价单。</span><span class="sxs-lookup"><span data-stu-id="dda38-174">Project Operations quotes have their own form and UI elements, business rules, business logic in plug-ins, and client-side scripts that make them unique from Sales quotes.</span></span>

<span data-ttu-id="dda38-175">由于这些原因，建议不要交替使用 Sales 报价单和 Project Operations 报价单。</span><span class="sxs-lookup"><span data-stu-id="dda38-175">For these reasons, it is not recommended to use a Sales quote and a Project Operations quote interchangeably.</span></span>
