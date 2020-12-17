---
title: 项目合同 - 关键概念 - 精简
description: 此主题提供有关项目合同的关键概念的信息。
author: rumant
manager: Annbe
ms.date: 10/07/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 3381707457ef35ff604c716592afd8382b98ad5d
ms.sourcegitcommit: 573be7e36604ace82b35e439cfa748aa7c587415
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/25/2020
ms.locfileid: "4643027"
---
# <a name="project-contracts---key-concepts---lite"></a><span data-ttu-id="89f74-103">项目合同 - 关键概念 - 精简</span><span class="sxs-lookup"><span data-stu-id="89f74-103">Project contracts - Key concepts - lite</span></span>

<span data-ttu-id="89f74-104">_**适用于：** 精简部署 - 估价交易开票_</span><span class="sxs-lookup"><span data-stu-id="89f74-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="89f74-105">本主题提供了在 Dynamics 365 Project Operations 中开始使用项目合同之前要了解的关键概念：</span><span class="sxs-lookup"><span data-stu-id="89f74-105">This topic provides the key concepts to be aware of before you begin using Project contracts in Dynamics 365 Project Operations:</span></span>

## <a name="contracting-unit"></a><span data-ttu-id="89f74-106">合同签订部门</span><span class="sxs-lookup"><span data-stu-id="89f74-106">Contracting Unit</span></span>

<span data-ttu-id="89f74-107">合同签订部门代表负责项目交付的部门或惯例。</span><span class="sxs-lookup"><span data-stu-id="89f74-107">The contracting unit represents the division or practice that owns the delivery of the project.</span></span> <span data-ttu-id="89f74-108">您可以为每个合同签订部门设置资源成本。</span><span class="sxs-lookup"><span data-stu-id="89f74-108">You can set up resource costs for each contracting unit.</span></span> <span data-ttu-id="89f74-109">当您指定资源的资源成本时，您还可以为资源设置不同成本费率。</span><span class="sxs-lookup"><span data-stu-id="89f74-109">When you specify the resource cost for a resource, you will also be able to set up different cost rates for resources.</span></span> <span data-ttu-id="89f74-110">此合同签订部门借用来自企业内其他部门或惯例的这些资源。</span><span class="sxs-lookup"><span data-stu-id="89f74-110">This contracting unit borrows these resources from other division or practices within the enterprise.</span></span> <span data-ttu-id="89f74-111">资源的成本费率称为转让价格、资源借入或交换价格。</span><span class="sxs-lookup"><span data-stu-id="89f74-111">The cost rates for the resources are referred to as transfer prices, resource borrowing, or exchange prices.</span></span> <span data-ttu-id="89f74-112">设置从其他部门借入资源的成本费率时，应使用借出部门的货币。</span><span class="sxs-lookup"><span data-stu-id="89f74-112">When you set up the cost rates to borrow resources from other divisions, use the currency of the lending division.</span></span>

## <a name="cost-currency"></a><span data-ttu-id="89f74-113">成本货币</span><span class="sxs-lookup"><span data-stu-id="89f74-113">Cost Currency</span></span>

<span data-ttu-id="89f74-114">成本货币是在屏幕上报告成本使用的货币。</span><span class="sxs-lookup"><span data-stu-id="89f74-114">Cost currency is the currency in which costs are reported on screen.</span></span> <span data-ttu-id="89f74-115">此货币源自合同和项目的 **合同签订部门** 字段所附的货币。</span><span class="sxs-lookup"><span data-stu-id="89f74-115">This currency is derived from the currency attached to the **Contracting Unit** field on the contract and the project.</span></span> <span data-ttu-id="89f74-116">可以任何货币针对项目记录成本。</span><span class="sxs-lookup"><span data-stu-id="89f74-116">Costs can be logged in any currency against a project.</span></span> <span data-ttu-id="89f74-117">但是，在屏幕上显示时，存在从记录的货币成本到项目的成本货币的货币转换。</span><span class="sxs-lookup"><span data-stu-id="89f74-117">However, there is currency conversion from the currency the costs were recorded in, to the cost currency of the project when shown on the screen.</span></span>

<span data-ttu-id="89f74-118">由于 Common Data Service (CDS) 平台中的汇率不能具有时效性，因此，如果您更新货币汇率，屏幕上的成本总计可能会随时间发生变化。</span><span class="sxs-lookup"><span data-stu-id="89f74-118">Because the exchange rates in the Common Data Service (CDS) platform can't be date effective, the on-screen totals for cost may change over time if you update the currency exchange rates.</span></span> <span data-ttu-id="89f74-119">但是，数据库中记录的成本保持不变，因为金额以发生时所用的货币存储。</span><span class="sxs-lookup"><span data-stu-id="89f74-119">However, costs as recorded in the database remain unchanged because the amounts are stored in the currency that were incurred in.</span></span>

## <a name="sales-currency"></a><span data-ttu-id="89f74-120">销售货币</span><span class="sxs-lookup"><span data-stu-id="89f74-120">Sales Currency</span></span>

<span data-ttu-id="89f74-121">Project Operations 中的销售货币是用于记录和显示预估和实际销售金额的货币。</span><span class="sxs-lookup"><span data-stu-id="89f74-121">Sales currency in Project Operations is the currency in which the estimated and actual sales amounts are recorded and shown.</span></span> <span data-ttu-id="89f74-122">销售货币还是客户为交易开票所使用的货币。</span><span class="sxs-lookup"><span data-stu-id="89f74-122">Sales currency is also the currency in which the customer is invoiced for the deal.</span></span> <span data-ttu-id="89f74-123">在项目合同上，销售货币默认来自客户记录，可以在创建合同时进行更改。</span><span class="sxs-lookup"><span data-stu-id="89f74-123">On a project contract, the sales currency defaults from the customer or account record and can be changed during when the contract is created.</span></span> <span data-ttu-id="89f74-124">当通过作为赢单结束报价单创建合同时，合同中的货币会默认为报价单上的货币。</span><span class="sxs-lookup"><span data-stu-id="89f74-124">When a contract is created by closing a quote as won, the currency on the contract is defaulted from the currency on the quote.</span></span>

<span data-ttu-id="89f74-125">当您从头创建项目合同时，**销售货币** 字段无法编辑。</span><span class="sxs-lookup"><span data-stu-id="89f74-125">When you create a project contract from scratch, the **Sales Currency** field can't be edited.</span></span> <span data-ttu-id="89f74-126">产品和项目价目表默认基于合同上的此货币。</span><span class="sxs-lookup"><span data-stu-id="89f74-126">Product and project price lists default based on this currency on the contract.</span></span>

<span data-ttu-id="89f74-127">与成本不同，销售值只能以销售货币记录。</span><span class="sxs-lookup"><span data-stu-id="89f74-127">Unlike costs, sales values can only be recorded in the sales currency.</span></span>

## <a name="billing-method"></a><span data-ttu-id="89f74-128">记帐方法</span><span class="sxs-lookup"><span data-stu-id="89f74-128">Billing Method</span></span>

<span data-ttu-id="89f74-129">通常，项目的合同签订模型有两种：固定费用和基于使用。</span><span class="sxs-lookup"><span data-stu-id="89f74-129">There are typically two types of contracting models for projects, fixed fee and consumption-based.</span></span> <span data-ttu-id="89f74-130">在 Project Operations 中，这些模型表示为具有两个可能值的计费方法：</span><span class="sxs-lookup"><span data-stu-id="89f74-130">These models are represented in Project Operations as billing methods with two possible values:</span></span>

- <span data-ttu-id="89f74-131">时间和材料：基于使用的合同签订模型，其中，每个发生的成本都由相应的收入支持。</span><span class="sxs-lookup"><span data-stu-id="89f74-131">Time and Material: A consumption-based contracting model where each incurred cost is backed by corresponding revenue.</span></span> <span data-ttu-id="89f74-132">随着您估算或产生更多成本，相应的估计销售额和实际销售额也将增加。</span><span class="sxs-lookup"><span data-stu-id="89f74-132">As you estimate or incur more costs, the corresponding estimated and actual sales also increase.</span></span> <span data-ttu-id="89f74-133">在具有此限定实际收入的计费方法的合同子项上指定上限。</span><span class="sxs-lookup"><span data-stu-id="89f74-133">Specify not-to-exceed limits on contract lines that have this billing method that caps off the actual revenue.</span></span> <span data-ttu-id="89f74-134">估计收入不受上限的影响。</span><span class="sxs-lookup"><span data-stu-id="89f74-134">Estimated revenue isn't impacted by not-to-exceed limits.</span></span>
- <span data-ttu-id="89f74-135">固定价格：一个固定费用合同签订模型，指示销售值将独立于所产生的成本。</span><span class="sxs-lookup"><span data-stu-id="89f74-135">Fixed Price: A fixed fee contracting model that indicates the sales values will be independent of the costs incurred.</span></span> <span data-ttu-id="89f74-136">销售值是固定的，不会随着您估算或产生更多成本而改变。</span><span class="sxs-lookup"><span data-stu-id="89f74-136">The sales value is fixed and doesn't change as you estimate or incur more costs.</span></span>

## <a name="project-price-lists"></a><span data-ttu-id="89f74-137">项目价目表</span><span class="sxs-lookup"><span data-stu-id="89f74-137">Project Price lists</span></span>

<span data-ttu-id="89f74-138">项目价目表用于提供时间、支出和其他项目相关组件的默认价格（不是成本费率）。</span><span class="sxs-lookup"><span data-stu-id="89f74-138">Project price lists are used to default prices, not cost rates, for time, expense, and other project-related components.</span></span> <span data-ttu-id="89f74-139">可以有多个价目表。</span><span class="sxs-lookup"><span data-stu-id="89f74-139">There can be multiple prices lists.</span></span> <span data-ttu-id="89f74-140">每个价目表对每个项目合同有自己的时效。</span><span class="sxs-lookup"><span data-stu-id="89f74-140">Each price list has its own date effectivity for each project contract.</span></span> <span data-ttu-id="89f74-141">Project Operations 不支持项目价目表上有重叠的有效期。</span><span class="sxs-lookup"><span data-stu-id="89f74-141">Overlapping date-effectivity on project price lists isn't supported in Project Operations.</span></span>

<span data-ttu-id="89f74-142">当通过赢得项目报价单创建项目合同时，将复制项目价目表，其中包含合同名称和日期。</span><span class="sxs-lookup"><span data-stu-id="89f74-142">When a project contract is created by winning a project quote, project price lists are copied with the contract name and date included.</span></span> <span data-ttu-id="89f74-143">复制此信息将构成此项目合同上项目组件的自定义定价。</span><span class="sxs-lookup"><span data-stu-id="89f74-143">Copying this information constitutes custom pricing for project components on this project contract.</span></span>

## <a name="product-price-lists"></a><span data-ttu-id="89f74-144">产品价目表</span><span class="sxs-lookup"><span data-stu-id="89f74-144">Product price lists</span></span>

<span data-ttu-id="89f74-145">产品价目表用于提供合同中基于产品的明细的默认价格（不是成本费率）。</span><span class="sxs-lookup"><span data-stu-id="89f74-145">Product price lists are used to default prices, not cost rates, for product-based lines on contract.</span></span> <span data-ttu-id="89f74-146">每个合同只有一个产品价目表。</span><span class="sxs-lookup"><span data-stu-id="89f74-146">There is only one product price list per contract.</span></span>

## <a name="transaction-classes"></a><span data-ttu-id="89f74-147">交易类</span><span class="sxs-lookup"><span data-stu-id="89f74-147">Transaction Classes</span></span>

<span data-ttu-id="89f74-148">Project Operations 支持四种交易类：</span><span class="sxs-lookup"><span data-stu-id="89f74-148">Project Operations supports four types of transaction classes:</span></span>

- <span data-ttu-id="89f74-149">时间</span><span class="sxs-lookup"><span data-stu-id="89f74-149">Time</span></span>
- <span data-ttu-id="89f74-150">支出</span><span class="sxs-lookup"><span data-stu-id="89f74-150">Expense</span></span>
- <span data-ttu-id="89f74-151">材料</span><span class="sxs-lookup"><span data-stu-id="89f74-151">Material</span></span>
- <span data-ttu-id="89f74-152">费用</span><span class="sxs-lookup"><span data-stu-id="89f74-152">Fee</span></span>

<span data-ttu-id="89f74-153">成本和销售值可以基于时间、支出和材料交易类预估和生成。</span><span class="sxs-lookup"><span data-stu-id="89f74-153">Cost and sales values can be estimated and incurred on Time, Expense, and Material transaction classes.</span></span> <span data-ttu-id="89f74-154">费用属于仅收入交易类。</span><span class="sxs-lookup"><span data-stu-id="89f74-154">Fee is a revenue-only transaction class.</span></span>

## <a name="work-entities-and-billing-entities"></a><span data-ttu-id="89f74-155">工作实体和计费实体</span><span class="sxs-lookup"><span data-stu-id="89f74-155">Work entities and Billing entities</span></span>

<span data-ttu-id="89f74-156">代表工作的实体是项目和任务。</span><span class="sxs-lookup"><span data-stu-id="89f74-156">Entities that represent work are projects and tasks.</span></span> <span data-ttu-id="89f74-157">代表计费方面的实体是合同子项。</span><span class="sxs-lookup"><span data-stu-id="89f74-157">Entities that represent billing aspects are contract lines.</span></span> <span data-ttu-id="89f74-158">您可以通过将不同的工作实体与合同子项相关联来将其与计费选项关联。</span><span class="sxs-lookup"><span data-stu-id="89f74-158">You can tie different work entities to billing options by tying them to contract lines.</span></span>

## <a name="multi-customer-deals"></a><span data-ttu-id="89f74-159">多客户交易</span><span class="sxs-lookup"><span data-stu-id="89f74-159">Multi-customer deals</span></span>

<span data-ttu-id="89f74-160">多客户交易在一个交易中有多个客户要开票。</span><span class="sxs-lookup"><span data-stu-id="89f74-160">Multi- customer deals have more than one customer to invoice on a deal.</span></span> <span data-ttu-id="89f74-161">常见示例包括：</span><span class="sxs-lookup"><span data-stu-id="89f74-161">Common examples include:</span></span>

- <span data-ttu-id="89f74-162">OEM 企业及其合作伙伴：合作伙伴和经销商销售包含一些增值服务的产品，通常涉及与客户的特定交易。</span><span class="sxs-lookup"><span data-stu-id="89f74-162">OEM Enterprises and their partners: Partners and resellers sell a product with some value-added services, typically involving a particular deal with a customer.</span></span> <span data-ttu-id="89f74-163">OEM 提出要为项目的一部分提供资金。</span><span class="sxs-lookup"><span data-stu-id="89f74-163">The OEM offers to finance a portion of the project.</span></span> 

- <span data-ttu-id="89f74-164">公共事业项目：地方政府的多个部门同意为一个项目提供资金，并根据先前商定的拆分方式开票。</span><span class="sxs-lookup"><span data-stu-id="89f74-164">Public sector projects: Multiple departments of a local government agree to fund a project and are invoiced according to a previously agreed split.</span></span> <span data-ttu-id="89f74-165">例如，学区和地方政府同意为修建游泳池提供资金。</span><span class="sxs-lookup"><span data-stu-id="89f74-165">For example, s school district and the local government agree to fund the building of a swimming pool.</span></span>

## <a name="invoice-schedules"></a><span data-ttu-id="89f74-166">发票计划</span><span class="sxs-lookup"><span data-stu-id="89f74-166">Invoice Schedules</span></span>

<span data-ttu-id="89f74-167">发票计划特定于每个合同子项，是使用自动开票的必需条件。</span><span class="sxs-lookup"><span data-stu-id="89f74-167">Invoice schedules are specific to each contract line and are required for automatic invoicing to work.</span></span> <span data-ttu-id="89f74-168">发票计划根据特定开始和完成日期以及开票频率创建。</span><span class="sxs-lookup"><span data-stu-id="89f74-168">Invoice schedules are created based on certain start and finish dates and invoice frequency.</span></span> <span data-ttu-id="89f74-169">在配置自动发票创建流程时，在合同阶段使用此计划。</span><span class="sxs-lookup"><span data-stu-id="89f74-169">The schedules are used in the contract stage when the automatic invoice creation process is configured.</span></span> <span data-ttu-id="89f74-170">从报价单创建项目合同时，会将发票计划从报价单复制到项目合同。</span><span class="sxs-lookup"><span data-stu-id="89f74-170">When a project contract is created from a quote, the invoice schedule is copied to the project contract from the quote.</span></span>

## <a name="changes-from-the-dynamics-365-sales-contract"></a><span data-ttu-id="89f74-171">Dynamics 365 Sales 合同的更改</span><span class="sxs-lookup"><span data-stu-id="89f74-171">Changes from the Dynamics 365 Sales contract</span></span>

<span data-ttu-id="89f74-172">Project Operations 合同基于 Dynamics 365 Sales 合同构建。</span><span class="sxs-lookup"><span data-stu-id="89f74-172">Project Operations contracts are built on Dynamics 365 Sales contracts.</span></span> <span data-ttu-id="89f74-173">但是，应注意一些重要的功能偏差和差异：</span><span class="sxs-lookup"><span data-stu-id="89f74-173">However, there are some important deviations and differences in functionality that you should be aware of:</span></span>

- <span data-ttu-id="89f74-174">Project Operations 合同有两种不同类型的明细，一个用于项目，一个用于产品。</span><span class="sxs-lookup"><span data-stu-id="89f74-174">Project Operations contracts have two different types of lines, one for projects and one for products.</span></span>
- <span data-ttu-id="89f74-175">Project Operations 合同具有自己的窗体和 UI 元素、业务规则、插件中的业务逻辑以及客户端脚本，这些让它们区别于 Sales 合同。</span><span class="sxs-lookup"><span data-stu-id="89f74-175">Project Operations contracts have their own form and UI elements, business rules, business logic in plug-ins, and client-side scripts that make them unique from Sales contracts.</span></span>

<span data-ttu-id="89f74-176">出于这些原因，您不应该交换使用销售合同和项目合同。</span><span class="sxs-lookup"><span data-stu-id="89f74-176">For these reasons, you shouldn't use a Sales contract and Project contract interchangeably.</span></span>
