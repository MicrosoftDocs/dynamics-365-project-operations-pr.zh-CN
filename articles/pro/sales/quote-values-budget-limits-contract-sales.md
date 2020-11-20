---
title: 项目报价单上的摘要信息 (Sales)
description: 此主题提供有关应用于和影响项目报价单的信息和设置的信息。  (Sales)
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: d050258ae457bb4392d5fa761442cfc7a444feb0
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/16/2020
ms.locfileid: "4072535"
---
# <a name="summary-information-on-a-project-quote-sales"></a><span data-ttu-id="d3f5e-104">项目报价单上的摘要信息 (Sales)</span><span class="sxs-lookup"><span data-stu-id="d3f5e-104">Summary information on a project quote (Sales)</span></span>

<span data-ttu-id="d3f5e-105">_**适用于：** 精简部署 - 估价交易开票_</span><span class="sxs-lookup"><span data-stu-id="d3f5e-105">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="d3f5e-106">本文介绍应用于项目报价单的信息。</span><span class="sxs-lookup"><span data-stu-id="d3f5e-106">This article explains the information that applies to a project quote.</span></span> <span data-ttu-id="d3f5e-107">这包括影响所有报价单明细的设置，以及有关跨所有明细项目汇总以驱动项目报价单的 KPI 的报价单的信息。</span><span class="sxs-lookup"><span data-stu-id="d3f5e-107">This includes the settings that impact all quote lines, and information about the quote that is summarized across all the line items to drive the KPIs of the project quote.</span></span>

<span data-ttu-id="d3f5e-108">下表列出了项目报价单中的摘要信息字段，这些字段是 Dynamics 365 Project Operations 所独有的，或者对 Dynamics 365 Sales 报价单中的行为有某些重要更改。</span><span class="sxs-lookup"><span data-stu-id="d3f5e-108">The following table lists the summary information fields on a project quote that are unique to Dynamics 365 Project Operations or have some important changes in behavior from Dynamics 365 Sales quotes.</span></span>

| <span data-ttu-id="d3f5e-109">**字段**</span><span class="sxs-lookup"><span data-stu-id="d3f5e-109">**Field**</span></span> | <span data-ttu-id="d3f5e-110">**位置**</span><span class="sxs-lookup"><span data-stu-id="d3f5e-110">**Location**</span></span> | <span data-ttu-id="d3f5e-111">**关联性、用途和指导**</span><span class="sxs-lookup"><span data-stu-id="d3f5e-111">**Relevance, purpose, and guidance**</span></span> | <span data-ttu-id="d3f5e-112">**下游影响**</span><span class="sxs-lookup"><span data-stu-id="d3f5e-112">**Downstream impact**</span></span> |
| --- | --- | --- | --- |
| <span data-ttu-id="d3f5e-113">Type</span><span class="sxs-lookup"><span data-stu-id="d3f5e-113">Type</span></span> | <span data-ttu-id="d3f5e-114">“摘要”选项卡（隐藏）</span><span class="sxs-lookup"><span data-stu-id="d3f5e-114">Summary tab (hidden)</span></span> | <span data-ttu-id="d3f5e-115">此选项集字段对以下选项进行哈希处理：</span><span class="sxs-lookup"><span data-stu-id="d3f5e-115">This option set field hash the following options:</span></span></br><span data-ttu-id="d3f5e-116">- 基于工作（仅在安装了 Project Operations 时可用）</span><span class="sxs-lookup"><span data-stu-id="d3f5e-116">- Work-based (available only when Project Operations is installed)</span></span></br><span data-ttu-id="d3f5e-117">- 基于项目（仅在安装了 Project Operations 和 Sales 时可用）</span><span class="sxs-lookup"><span data-stu-id="d3f5e-117">- Item-based (available only when Project Operations and Sales are installed)</span></span></br><span data-ttu-id="d3f5e-118">- 基于服务维护（通过安装 Dynamics 365 Field Service 提供）</span><span class="sxs-lookup"><span data-stu-id="d3f5e-118">- Service maintenance-based (available when Dynamics 365 Field Service is installed)</span></span> | <span data-ttu-id="d3f5e-119">当您使用 Project Operations 应用程序时，此字段的值会自动设置为 **基于工作** 。</span><span class="sxs-lookup"><span data-stu-id="d3f5e-119">When you use the Project Operations application, the value of this field is automatically set to **Work-based**.</span></span> <span data-ttu-id="d3f5e-120">这会将报价单分类为基于项目的报价单。</span><span class="sxs-lookup"><span data-stu-id="d3f5e-120">This classifies the quote as a project-based quote.</span></span> <span data-ttu-id="d3f5e-121">报价单应该是基于项目的，以支持所有特定于项目的扩展和功能。</span><span class="sxs-lookup"><span data-stu-id="d3f5e-121">A quote should be project-based to enable all project-specific extensions and functionality.</span></span> |
| <span data-ttu-id="d3f5e-122">潜在客户</span><span class="sxs-lookup"><span data-stu-id="d3f5e-122">Potential Customer</span></span> | <span data-ttu-id="d3f5e-123">“摘要”标签页</span><span class="sxs-lookup"><span data-stu-id="d3f5e-123">Summary tab</span></span> | <span data-ttu-id="d3f5e-124">对客户的公司或客户记录的引用。</span><span class="sxs-lookup"><span data-stu-id="d3f5e-124">Reference to the customer's company or account record.</span></span> <span data-ttu-id="d3f5e-125">从商机创建报价单时，将从商机上的相应字段复制此字段。</span><span class="sxs-lookup"><span data-stu-id="d3f5e-125">When a quote is created from an opportunity, this field is copied from the corresponding field on the opportunity.</span></span> | <span data-ttu-id="d3f5e-126">项目报价单上的货币根据客户的货币选择默认值。</span><span class="sxs-lookup"><span data-stu-id="d3f5e-126">The currency on the project quote is defaulted based on the currency of the customer.</span></span> <span data-ttu-id="d3f5e-127">但可以在保存报价单之前更改。</span><span class="sxs-lookup"><span data-stu-id="d3f5e-127">This can, however, be changed before the quote is saved.</span></span> |
| <span data-ttu-id="d3f5e-128">客户经理</span><span class="sxs-lookup"><span data-stu-id="d3f5e-128">Account Manager</span></span> | <span data-ttu-id="d3f5e-129">“摘要”标签页</span><span class="sxs-lookup"><span data-stu-id="d3f5e-129">Summary tab</span></span> | <span data-ttu-id="d3f5e-130">此交易的客户经理的姓名。</span><span class="sxs-lookup"><span data-stu-id="d3f5e-130">The name of the account Manager for this deal.</span></span> <span data-ttu-id="d3f5e-131">从商机创建报价单时，将从商机上的相应字段复制此字段。</span><span class="sxs-lookup"><span data-stu-id="d3f5e-131">When a quote is created from an opportunity, this field is copied from the corresponding field on the opportunity.</span></span> | <span data-ttu-id="d3f5e-132">客户经理负责在此项目完成之前管理与客户的关系。</span><span class="sxs-lookup"><span data-stu-id="d3f5e-132">The Account manager is responsible for managing the relationship with the customer through the completion of this project.</span></span> <span data-ttu-id="d3f5e-133">根据与客户经理关联的可预订资源记录，合同签订部门在项目报价单上选择默认值。</span><span class="sxs-lookup"><span data-stu-id="d3f5e-133">Based on the bookable resource record tied to the Account manager, the contracting unit defaults on the project quote.</span></span> |
| <span data-ttu-id="d3f5e-134">合同签订部门</span><span class="sxs-lookup"><span data-stu-id="d3f5e-134">Contracting Unit</span></span> | <span data-ttu-id="d3f5e-135">“摘要”标签页</span><span class="sxs-lookup"><span data-stu-id="d3f5e-135">Summary tab</span></span> | <span data-ttu-id="d3f5e-136">负责交付与此报价单关联的一个或多个项目的部门。</span><span class="sxs-lookup"><span data-stu-id="d3f5e-136">The organization unit that is responsible for the delivery of the project or projects associated with this quote.</span></span> <span data-ttu-id="d3f5e-137">从商机创建报价单时，将从商机上的相应字段复制此字段。</span><span class="sxs-lookup"><span data-stu-id="d3f5e-137">When a quote is created from an opportunity, this field is copied from the corresponding field on the opportunity.</span></span> | <span data-ttu-id="d3f5e-138">合同签订部门是在交易完成后将执行项目的公司部门。</span><span class="sxs-lookup"><span data-stu-id="d3f5e-138">The contracting unit is the division of the company that will be executing the projects after the deal is closed.</span></span> <span data-ttu-id="d3f5e-139">每个合同签订部门都有一种货币，此货币用于报告项目执行过程中产生的预估成本和实际成本。</span><span class="sxs-lookup"><span data-stu-id="d3f5e-139">Every contracting unit has a currency, and this currency is used to report estimated and actual costs incurred during the execution of the project.</span></span> |
| <span data-ttu-id="d3f5e-140">产品价目表</span><span class="sxs-lookup"><span data-stu-id="d3f5e-140">Product price list</span></span> | <span data-ttu-id="d3f5e-141">“摘要”标签页</span><span class="sxs-lookup"><span data-stu-id="d3f5e-141">Summary tab</span></span> | <span data-ttu-id="d3f5e-142">这是用于基于产品的报价单明细中的默认价格的价目表。</span><span class="sxs-lookup"><span data-stu-id="d3f5e-142">This is the price list that is used to default prices on the product-based quote lines.</span></span> <span data-ttu-id="d3f5e-143">此字段的选项列表显示价目表货币与报价单上的货币匹配的价目表列表。</span><span class="sxs-lookup"><span data-stu-id="d3f5e-143">The list of options for this field shows a list of price lists where the price list currency matches the currency on the quote.</span></span> <span data-ttu-id="d3f5e-144">从商机创建报价单时，将从商机上的相应字段复制此字段。</span><span class="sxs-lookup"><span data-stu-id="d3f5e-144">When a quote is created from an opportunity, this field is copied from the corresponding field on the opportunity.</span></span> <span data-ttu-id="d3f5e-145">商机上的这个字段默认来自客户记录，但可以更改。</span><span class="sxs-lookup"><span data-stu-id="d3f5e-145">This field on the opportunity is defaulted from the account record but can be changed.</span></span> | <span data-ttu-id="d3f5e-146">报价单赢单时，此字段值将复制到创建的项目合同中。</span><span class="sxs-lookup"><span data-stu-id="d3f5e-146">When a quote is won, the field value is copied to the project contract that is created.</span></span> |
| <span data-ttu-id="d3f5e-147">货币</span><span class="sxs-lookup"><span data-stu-id="d3f5e-147">Currency</span></span> | <span data-ttu-id="d3f5e-148">“摘要”标签页</span><span class="sxs-lookup"><span data-stu-id="d3f5e-148">Summary tab</span></span> | <span data-ttu-id="d3f5e-149">这指示将用于报告此交易的值的货币。</span><span class="sxs-lookup"><span data-stu-id="d3f5e-149">This indicates the currency that will be used for reporting the value of this deal.</span></span> <span data-ttu-id="d3f5e-150">它同时也是交易赢单时为客户开票所使用的货币。</span><span class="sxs-lookup"><span data-stu-id="d3f5e-150">This is also the currency in which the customer will be invoiced if the deal is won.</span></span> <span data-ttu-id="d3f5e-151">从商机创建报价单时，将从商机上的相应字段复制此字段。</span><span class="sxs-lookup"><span data-stu-id="d3f5e-151">When a quote is created from an opportunity, this field is copied from the corresponding field on the opportunity.</span></span> <span data-ttu-id="d3f5e-152">商机上的这个字段默认来自客户记录，但可以由用户更改。</span><span class="sxs-lookup"><span data-stu-id="d3f5e-152">This field on the opportunity defaults from the account record but can be changed by the user.</span></span> | <span data-ttu-id="d3f5e-153">保存报价单后，此字段不能再进行编辑。</span><span class="sxs-lookup"><span data-stu-id="d3f5e-153">After a quote is saved, this field is no longer editable.</span></span> <span data-ttu-id="d3f5e-154">它用于为报价单上的产品和项目价目表选择默认值。</span><span class="sxs-lookup"><span data-stu-id="d3f5e-154">This is used to default the product and project price lists on the quote.</span></span> <span data-ttu-id="d3f5e-155">报价单上的货币用于匹配价目表上的货币。</span><span class="sxs-lookup"><span data-stu-id="d3f5e-155">The currency on the quote is used to match the currency on the price list.</span></span> |
| <span data-ttu-id="d3f5e-156">上限</span><span class="sxs-lookup"><span data-stu-id="d3f5e-156">Not-to-exceed limit</span></span> | <span data-ttu-id="d3f5e-157">“摘要”标签页</span><span class="sxs-lookup"><span data-stu-id="d3f5e-157">Summary tab</span></span> | <span data-ttu-id="d3f5e-158">这表示客户同意此交易的最终值的商定上限。</span><span class="sxs-lookup"><span data-stu-id="d3f5e-158">This indicates the negotiated cap on the final value that the customer is agreeing to for this deal.</span></span> | <span data-ttu-id="d3f5e-159">此上限在执行期间进行评估，适用于与此交易关联的所有明细项目和项目。</span><span class="sxs-lookup"><span data-stu-id="d3f5e-159">This cap is evaluated during execution and is applicable across all line items and projects associated with this deal.</span></span> |
| <span data-ttu-id="d3f5e-160">要求交货日期</span><span class="sxs-lookup"><span data-stu-id="d3f5e-160">Requested delivery date</span></span> | <span data-ttu-id="d3f5e-161">“摘要”标签页</span><span class="sxs-lookup"><span data-stu-id="d3f5e-161">Summary tab</span></span> | <span data-ttu-id="d3f5e-162">从商机创建报价单时，将从商机上的相应字段复制此字段。</span><span class="sxs-lookup"><span data-stu-id="d3f5e-162">When a quote is created from an opportunity, this field is copied from the corresponding field on the opportunity.</span></span> | <span data-ttu-id="d3f5e-163">此日期用作生成发票计划的结束日期。</span><span class="sxs-lookup"><span data-stu-id="d3f5e-163">This date is used as the end date for generating invoice schedules.</span></span> |

<span data-ttu-id="d3f5e-164">以下是项目报价单上可用的选项卡和 KPI，它们是 Project Operations 所特有的，或对 Sales 报价单的行为有一些重要更改：</span><span class="sxs-lookup"><span data-stu-id="d3f5e-164">Below are the tabs and KPIs available on a project quote that are unique to Project Operations or have some important changes in behavior from Sales quotes:</span></span>

| <span data-ttu-id="d3f5e-165">**字段**</span><span class="sxs-lookup"><span data-stu-id="d3f5e-165">**Field**</span></span> | <span data-ttu-id="d3f5e-166">**位置**</span><span class="sxs-lookup"><span data-stu-id="d3f5e-166">**Location**</span></span> | <span data-ttu-id="d3f5e-167">**关联性、用途和指导**</span><span class="sxs-lookup"><span data-stu-id="d3f5e-167">**Relevance, purpose and guidance**</span></span> |
| --- | --- | --- |
| <span data-ttu-id="d3f5e-168">利润率分析</span><span class="sxs-lookup"><span data-stu-id="d3f5e-168">Profitability analysis</span></span> | <span data-ttu-id="d3f5e-169">报价单上的选项卡</span><span class="sxs-lookup"><span data-stu-id="d3f5e-169">Tab on the Quote</span></span> | <span data-ttu-id="d3f5e-170">此选项卡显示以下指标：</span><span class="sxs-lookup"><span data-stu-id="d3f5e-170">The tab shows the following metrics:</span></span></br><span data-ttu-id="d3f5e-171">- 总应计成本</span><span class="sxs-lookup"><span data-stu-id="d3f5e-171">- Total chargeable cost</span></span></br></br><span data-ttu-id="d3f5e-172">- 总非应计成本</span><span class="sxs-lookup"><span data-stu-id="d3f5e-172">- Total non-chargeable cost</span></span></br><span data-ttu-id="d3f5e-173">- 收入总额</span><span class="sxs-lookup"><span data-stu-id="d3f5e-173">- Total revenue</span></span></br><span data-ttu-id="d3f5e-174">- 收入总额（基础货币）</span><span class="sxs-lookup"><span data-stu-id="d3f5e-174">- Total revenue (base)</span></span></br><span data-ttu-id="d3f5e-175">- 毛利</span><span class="sxs-lookup"><span data-stu-id="d3f5e-175">- Gross margin</span></span></br><span data-ttu-id="d3f5e-176">- 调整后的毛利润</span><span class="sxs-lookup"><span data-stu-id="d3f5e-176">- Adjusted gross margin</span></span>|
| <span data-ttu-id="d3f5e-177">与客户预期比较</span><span class="sxs-lookup"><span data-stu-id="d3f5e-177">Comparison to Customer Expectations</span></span> | <span data-ttu-id="d3f5e-178">报价单上的选项卡</span><span class="sxs-lookup"><span data-stu-id="d3f5e-178">Tab on the Quote</span></span> | <span data-ttu-id="d3f5e-179">此选项卡显示以下指标：</span><span class="sxs-lookup"><span data-stu-id="d3f5e-179">This tab shows the following metrics:</span></span></br><span data-ttu-id="d3f5e-180">- 预计完成日期</span><span class="sxs-lookup"><span data-stu-id="d3f5e-180">- Estimated completion</span></span></br><span data-ttu-id="d3f5e-181">- 要求完成日期</span><span class="sxs-lookup"><span data-stu-id="d3f5e-181">- Requested completion</span></span></br><span data-ttu-id="d3f5e-182">- 客户预算</span><span class="sxs-lookup"><span data-stu-id="d3f5e-182">- Customer budget</span></span></br><span data-ttu-id="d3f5e-183">- 报价值</span><span class="sxs-lookup"><span data-stu-id="d3f5e-183">- Quote value</span></span> |
| <span data-ttu-id="d3f5e-184">报价单分析</span><span class="sxs-lookup"><span data-stu-id="d3f5e-184">Quote analysis</span></span> | <span data-ttu-id="d3f5e-185">报价单上的选项卡</span><span class="sxs-lookup"><span data-stu-id="d3f5e-185">Tab on the Quote</span></span> | <span data-ttu-id="d3f5e-186">此选项卡汇总了项目报价单的以下几个主要 KPI</span><span class="sxs-lookup"><span data-stu-id="d3f5e-186">This tab summarizes the following top KPIs for a project quote</span></span></br><span data-ttu-id="d3f5e-187">- 比较客户对预算和计划的期望</span><span class="sxs-lookup"><span data-stu-id="d3f5e-187">- Comparison to customer expectations for budget and schedule</span></span></br><span data-ttu-id="d3f5e-188">- 毛利</span><span class="sxs-lookup"><span data-stu-id="d3f5e-188">- Gross margin</span></span></br><span data-ttu-id="d3f5e-189">- 调整后的毛利润</span><span class="sxs-lookup"><span data-stu-id="d3f5e-189">- Adjusted gross margin</span></span> |