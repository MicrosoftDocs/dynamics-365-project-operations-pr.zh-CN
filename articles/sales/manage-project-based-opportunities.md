---
title: 管理基于项目的商机
description: 此主题提供有关如何处于与项目相关的商机的信息。
author: rumant
manager: Annbe
ms.date: 10/21/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 39ce52d5da4c7027ee2f2fa44579c0d4bf74925e
ms.sourcegitcommit: f8edff6422b82fdf2cea897faa6abb51e2c0c3c8
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/21/2020
ms.locfileid: "4087830"
---
# <a name="manage-project-based-opportunities"></a><span data-ttu-id="f3e16-103">管理基于项目的商机</span><span class="sxs-lookup"><span data-stu-id="f3e16-103">Manage project-based opportunities</span></span>

<span data-ttu-id="f3e16-104">_**适用于：** 基于资源/非库存场景的 Project Operations，精简部署 - 估价开票交易_</span><span class="sxs-lookup"><span data-stu-id="f3e16-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="f3e16-105">基于项目的公司通常将业务交付分布在多个国家和地区。</span><span class="sxs-lookup"><span data-stu-id="f3e16-105">Project-based companies typically have their operations for delivery spread across multiple countries and geographies.</span></span> <span data-ttu-id="f3e16-106">项目执行和交付的成本可能因管理交付的地理位置或部门而异。</span><span class="sxs-lookup"><span data-stu-id="f3e16-106">The cost of the project execution and delivery can vary  based on which geography or division manages the delivery.</span></span> <span data-ttu-id="f3e16-107">这继而会影响交易的利润。</span><span class="sxs-lookup"><span data-stu-id="f3e16-107">In turn, this can impact the margins of the deal.</span></span> <span data-ttu-id="f3e16-108">交付基于项目的服务通常涉及大量的人事资源时间、大量出差支出、材料成本和其他支出。</span><span class="sxs-lookup"><span data-stu-id="f3e16-108">Delivery of project-based services typically involves large quantities of human resource time, considerable expenses for travel, material costs, and other expenses.</span></span>

<span data-ttu-id="f3e16-109">Dynamics 365 Project Operations 中基于项目的商机在设计加入了对 Dynamics 365 Sales 的扩展。</span><span class="sxs-lookup"><span data-stu-id="f3e16-109">Project-based opportunities in Dynamics 365 Project Operations are designed with extensions to Dynamics 365 Sales.</span></span> <span data-ttu-id="f3e16-110">此主题将详细介绍基于项目的公司在管理基于项目的商机时所需的其他功能中包含的不同字段和业务逻辑。</span><span class="sxs-lookup"><span data-stu-id="f3e16-110">The topic provides details about the different fields and business logic included in the additional functionality that is required by project-based companies to manage project-based opportunities.</span></span>

## <a name="view-all-project-based-opportunities"></a><span data-ttu-id="f3e16-111">查看所有基于项目的商机</span><span class="sxs-lookup"><span data-stu-id="f3e16-111">View all project-based opportunities</span></span>

<span data-ttu-id="f3e16-112">可在 **商机** 列表页查看所有基于项目的商机的列表。</span><span class="sxs-lookup"><span data-stu-id="f3e16-112">A list of all the project-based opportunities can be seen from the **Opportunity** list page.</span></span> 

1. <span data-ttu-id="f3e16-113">转到 **销售** > **商机** 。</span><span class="sxs-lookup"><span data-stu-id="f3e16-113">Go to **Sales** > **Opportunities**.</span></span>
2. <span data-ttu-id="f3e16-114">使用 **视图切换器** 选择商机的其他筛选视图。</span><span class="sxs-lookup"><span data-stu-id="f3e16-114">Use the **View switcher** to select other filtered views of the opportunities.</span></span> <span data-ttu-id="f3e16-115">您可以使用自定义筛选条件创建您自己的视图，来配置这些视图和导航选项。</span><span class="sxs-lookup"><span data-stu-id="f3e16-115">You can create your own views with custom filter criteria to configure these views and navigation options.</span></span>

<span data-ttu-id="f3e16-116">可从此列表页或详细信息页面创建或删除项目商机。</span><span class="sxs-lookup"><span data-stu-id="f3e16-116">Project Opportunities can be created or deleted from this list page or the detail page.</span></span>

## <a name="business-process-flow-for-project-based-deals"></a><span data-ttu-id="f3e16-117">基于项目的交易的业务流程</span><span class="sxs-lookup"><span data-stu-id="f3e16-117">Business process flow for project-based deals</span></span>

<span data-ttu-id="f3e16-118">Project Operations 中基于项目的交易支持以下业务流程：</span><span class="sxs-lookup"><span data-stu-id="f3e16-118">The following business process flows are supported for project-based deals in Project Operations:</span></span>

- <span data-ttu-id="f3e16-119">潜在顾客转化为商机业务流程</span><span class="sxs-lookup"><span data-stu-id="f3e16-119">Lead to Opportunity business process</span></span>
- <span data-ttu-id="f3e16-120">商机销售流程</span><span class="sxs-lookup"><span data-stu-id="f3e16-120">Opportunity sales process</span></span>

### <a name="lead-to-opportunity-business-process"></a><span data-ttu-id="f3e16-121">潜在顾客转化为商机业务流程</span><span class="sxs-lookup"><span data-stu-id="f3e16-121">Lead to opportunity business process</span></span> 
<span data-ttu-id="f3e16-122">潜在顾客转化为商机业务流程支持以下阶段：</span><span class="sxs-lookup"><span data-stu-id="f3e16-122">The lead to opportunity business process supports the following stages:</span></span>

| <span data-ttu-id="f3e16-123">阶段</span><span class="sxs-lookup"><span data-stu-id="f3e16-123">Stage</span></span> | <span data-ttu-id="f3e16-124">映射实体</span><span class="sxs-lookup"><span data-stu-id="f3e16-124">Mapped entity</span></span> | <span data-ttu-id="f3e16-125">功能</span><span class="sxs-lookup"><span data-stu-id="f3e16-125">Functionality</span></span> |
| --- | --- | --- |
| <span data-ttu-id="f3e16-126">授予资格</span><span class="sxs-lookup"><span data-stu-id="f3e16-126">Qualify</span></span> | <span data-ttu-id="f3e16-127">潜在顾客</span><span class="sxs-lookup"><span data-stu-id="f3e16-127">Lead</span></span> | <span data-ttu-id="f3e16-128">授予潜在顾客创建客户、联系人和商机的资格。</span><span class="sxs-lookup"><span data-stu-id="f3e16-128">Qualify the lead to create an account, contact, and an opportunity.</span></span> |
| <span data-ttu-id="f3e16-129">制定</span><span class="sxs-lookup"><span data-stu-id="f3e16-129">Develop</span></span> | <span data-ttu-id="f3e16-130">商机​​</span><span class="sxs-lookup"><span data-stu-id="f3e16-130">Opportunity</span></span> | <span data-ttu-id="f3e16-131">开发商机以添加有关所涉及的工作、关键利益干系人和竞争的更多信息。</span><span class="sxs-lookup"><span data-stu-id="f3e16-131">Develop the opportunity to add more information on the work involved, key stakeholders, and competition.</span></span> |
| <span data-ttu-id="f3e16-132">建议</span><span class="sxs-lookup"><span data-stu-id="f3e16-132">Propose</span></span> | <span data-ttu-id="f3e16-133">商机​​</span><span class="sxs-lookup"><span data-stu-id="f3e16-133">Opportunity</span></span> | <span data-ttu-id="f3e16-134">制定方案并获得内部审查团队的批准。</span><span class="sxs-lookup"><span data-stu-id="f3e16-134">Develop the proposal and get approval from the internal review team.</span></span> |
| <span data-ttu-id="f3e16-135">结束</span><span class="sxs-lookup"><span data-stu-id="f3e16-135">Close</span></span> | <span data-ttu-id="f3e16-136">商机​​</span><span class="sxs-lookup"><span data-stu-id="f3e16-136">Opportunity</span></span> | <span data-ttu-id="f3e16-137">赢得商机以达成交易。</span><span class="sxs-lookup"><span data-stu-id="f3e16-137">Win the opportunity to close the deal.</span></span> |

### <a name="opportunity-sales-process"></a><span data-ttu-id="f3e16-138">商机销售流程</span><span class="sxs-lookup"><span data-stu-id="f3e16-138">Opportunity sales process</span></span>
<span data-ttu-id="f3e16-139">Project Operations 的商机销售流程是 Sales 应用程序中商机销售流程业务流程的扩展。</span><span class="sxs-lookup"><span data-stu-id="f3e16-139">The Opportunity sales process in Project Operations is an extension to the Opportunity sales process business flow in the Sales application.</span></span> <span data-ttu-id="f3e16-140">此业务流程设计为开箱即用，可以在基于项目的商机中支持以下阶段。</span><span class="sxs-lookup"><span data-stu-id="f3e16-140">This business process is designed out-of-the-box to support the following stages in a project-based opportunity.</span></span>

| <span data-ttu-id="f3e16-141">阶段</span><span class="sxs-lookup"><span data-stu-id="f3e16-141">Stage</span></span> | <span data-ttu-id="f3e16-142">映射实体</span><span class="sxs-lookup"><span data-stu-id="f3e16-142">Mapped entity</span></span> | <span data-ttu-id="f3e16-143">功能</span><span class="sxs-lookup"><span data-stu-id="f3e16-143">Functionality</span></span> |
| --- | --- | --- |
| <span data-ttu-id="f3e16-144">授予资格</span><span class="sxs-lookup"><span data-stu-id="f3e16-144">Qualify</span></span> | <span data-ttu-id="f3e16-145">商机​​</span><span class="sxs-lookup"><span data-stu-id="f3e16-145">Opportunity</span></span> | <span data-ttu-id="f3e16-146">授予潜在顾客创建客户、联系人和商机的资格。</span><span class="sxs-lookup"><span data-stu-id="f3e16-146">Qualify the lead to create an account, contact, and an opportunity.</span></span> |
| <span data-ttu-id="f3e16-147">建议</span><span class="sxs-lookup"><span data-stu-id="f3e16-147">Propose</span></span> | <span data-ttu-id="f3e16-148">报价单</span><span class="sxs-lookup"><span data-stu-id="f3e16-148">Quote</span></span> | <span data-ttu-id="f3e16-149">使用项目报价单制定方案并获得内部审查团队的批准。</span><span class="sxs-lookup"><span data-stu-id="f3e16-149">Develop the proposal using project quotes and get approval from the internal review team.</span></span> |
| <span data-ttu-id="f3e16-150">合同</span><span class="sxs-lookup"><span data-stu-id="f3e16-150">Contract</span></span> | <span data-ttu-id="f3e16-151">项目合同</span><span class="sxs-lookup"><span data-stu-id="f3e16-151">Project Contract</span></span> | <span data-ttu-id="f3e16-152">赢得报价单以创建合同并开始项目的执行和交付。</span><span class="sxs-lookup"><span data-stu-id="f3e16-152">Win the quote to create the contract and begin execution and delivery on the project.</span></span> |
| <span data-ttu-id="f3e16-153">结束</span><span class="sxs-lookup"><span data-stu-id="f3e16-153">Close</span></span> | <span data-ttu-id="f3e16-154">项目合同</span><span class="sxs-lookup"><span data-stu-id="f3e16-154">Project Contract</span></span> | <span data-ttu-id="f3e16-155">成功完成工作并关闭项目合同。</span><span class="sxs-lookup"><span data-stu-id="f3e16-155">Finish the work successfully and close the project contract.</span></span> |

> [!NOTE]
> <span data-ttu-id="f3e16-156">如果基于项目的交易从潜在顾客开始，潜在顾客转化为商机业务流程优先。</span><span class="sxs-lookup"><span data-stu-id="f3e16-156">If your project-based deal started with a Lead, the Lead to Opportunity business process takes precedence.</span></span>
>
> <span data-ttu-id="f3e16-157">如果基于项目的交易从商机开始，商机销售流程优先。</span><span class="sxs-lookup"><span data-stu-id="f3e16-157">If your project-based deal started with an Opportunity, the Opportunity sales process takes precedence.</span></span>

<span data-ttu-id="f3e16-158">您可以编辑产品业务流程或创建您自己的业务流程，来根据需要跟踪销售流程。</span><span class="sxs-lookup"><span data-stu-id="f3e16-158">You can edit the product business process flow or create your own business process flows to track your sales process as needed.</span></span> <span data-ttu-id="f3e16-159">有关业务流程的详细信息，请参阅[业务流程概述](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/customize/business-process-flows-overview)。</span><span class="sxs-lookup"><span data-stu-id="f3e16-159">For more information about the business process flow, see [Business process flows overview](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/customize/business-process-flows-overview).</span></span>
