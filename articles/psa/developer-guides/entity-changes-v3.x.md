---
title: 实体、控件和用户界面更改 (Project Service Automation 3.x)
description: 此主题介绍 Microsoft Dynamics Project Service Automation 3.x 的解决方案更改。
author: makk
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 03/15/2019
ms.topic: article
ms.service: business-applications
ms.author: makk
audience: admin
search.audienceType:
- admin
- customizer
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: fa80f459260f30360e78a1e7bcc00706dbc0b5a4
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/15/2021
ms.locfileid: "5284887"
---
# <a name="entity-control-and-user-interface-changes-project-service-automation-3x"></a><span data-ttu-id="85246-103">实体、控件和用户界面更改 (Project Service Automation 3.x)</span><span class="sxs-lookup"><span data-stu-id="85246-103">Entity, control, and user interface changes (Project Service Automation 3.x)</span></span>

[!include [banner](../../includes/psa-now-project-operations.md)]


<span data-ttu-id="85246-104">随着 Microsoft Dynamics Project Service Automation (PSA) 3.x 的发布，对实体、控件、视图和用户界面进行了大量更改。</span><span class="sxs-lookup"><span data-stu-id="85246-104">With the release of Microsoft Dynamics Project Service Automation (PSA) 3.x, many changes have been made to the entities, controls, views, and user interface.</span></span> <span data-ttu-id="85246-105">此主题介绍这些重要更改。</span><span class="sxs-lookup"><span data-stu-id="85246-105">This topic provides information about these important changes.</span></span>

## <a name="parent-child-relationships-for-sales-document-sales-document-line-sales-document-line-detail-entities"></a><span data-ttu-id="85246-106">销售文档、销售文档明细、销售文档明细详细信息实体的父子关系</span><span class="sxs-lookup"><span data-stu-id="85246-106">Parent-child relationships for sales document, sales document line, sales document line detail entities</span></span>
<span data-ttu-id="85246-107">在 Dynamics 365 Project Service Automation (PSA) 版本 3.0 之前发布的版本中，销售文档、销售文档明细和销售文档明细详细信息实体之间的某些关系是通过其中存储相关实体的 GUID 字符串表示的字符串字段实施的。</span><span class="sxs-lookup"><span data-stu-id="85246-107">In versions of Dynamics 365 Project Service Automation (PSA) released prior to version 3.0, some of the relationships between sales documents, sales document lines, and sales document line detail entities were implemented through string fields that would hold a string representation of GUID of the related entity.</span></span> <span data-ttu-id="85246-108">这是因为平台限制导致解决方案的服务器端和客户端中需要大量自定义代码来让这些关系的工作方式类似典型 Dynamics CRM 实体关系的工作方式，并且让字符串字段充当查找字段。</span><span class="sxs-lookup"><span data-stu-id="85246-108">This was due to platform limitations that required significant custom code on the server and client sides of the solution to make those relationships work similar to typical Dynamics CRM entity relationships and to make string fields act like lookup fields.</span></span>

<span data-ttu-id="85246-109">PSA 3.0 已经过更新，现在利用销售文档与销售文档明细实体之间新的实体关系。</span><span class="sxs-lookup"><span data-stu-id="85246-109">PSA 3.0 has been updated to leverage the new entity relationships between sales document and sales document line entities.</span></span>

<span data-ttu-id="85246-110">因为现在可以使用查找字段指示对实体的引用，所以不再需要之前版本中用于存储相关实体的 GUID 字符串值的字段，因此已将其弃用。</span><span class="sxs-lookup"><span data-stu-id="85246-110">Because lookup fields can now be used to indicate references to entities, the fields that held the string value of the GUID of the related entity in previous versions are no longer needed and therefore have been deprecated.</span></span> <span data-ttu-id="85246-111">还弃用了用于处理旧字符串字段定义的关系的自定义客户端和服务器端代码。</span><span class="sxs-lookup"><span data-stu-id="85246-111">The custom client and server side code that handles the relationships defined by legacy string fields has also been deprecated.</span></span>

### <a name="entity-schema-changes"></a><span data-ttu-id="85246-112">实体架构更改</span><span class="sxs-lookup"><span data-stu-id="85246-112">Entity schema changes</span></span>
<span data-ttu-id="85246-113">下表提供实体的已弃用字符串字段与新查找字段的一对一列表。</span><span class="sxs-lookup"><span data-stu-id="85246-113">The following table provides a one-to-one list of the deprecated string fields and the new lookup fields for the entities.</span></span> 

 <span data-ttu-id="85246-114">实体</span><span class="sxs-lookup"><span data-stu-id="85246-114">Entity</span></span> |   <span data-ttu-id="85246-115">弃用字段（字符串）</span><span class="sxs-lookup"><span data-stu-id="85246-115">Deprecated field (String)</span></span> | <span data-ttu-id="85246-116">新字段（查找）</span><span class="sxs-lookup"><span data-stu-id="85246-116">New field (Lookup)</span></span>
--- | --- | ---
<span data-ttu-id="85246-117">invoicedetail（发票明细）</span><span class="sxs-lookup"><span data-stu-id="85246-117">invoicedetail (Invoice Line)</span></span> |  <span data-ttu-id="85246-118">msdyn_contractline</span><span class="sxs-lookup"><span data-stu-id="85246-118">msdyn_contractline</span></span> |    <span data-ttu-id="85246-119">msdyn_contractlineid</span><span class="sxs-lookup"><span data-stu-id="85246-119">msdyn_contractlineid</span></span>
<span data-ttu-id="85246-120">msdyn_actual（实际值）</span><span class="sxs-lookup"><span data-stu-id="85246-120">msdyn_actual (Actual)</span></span> | <span data-ttu-id="85246-121">msdyn_salescontractline</span><span class="sxs-lookup"><span data-stu-id="85246-121">msdyn_salescontractline</span></span> |   <span data-ttu-id="85246-122">msdyn_salescontractlineid</span><span class="sxs-lookup"><span data-stu-id="85246-122">msdyn_salescontractlineid</span></span>
<span data-ttu-id="85246-123">msdyn_contractlineinvoiceschedule（项目合同子项发票计划）</span><span class="sxs-lookup"><span data-stu-id="85246-123">msdyn_contractlineinvoiceschedule (Project Contract Line Invoice Schedule)</span></span> |    <span data-ttu-id="85246-124">msdyn_contractline</span><span class="sxs-lookup"><span data-stu-id="85246-124">msdyn_contractline</span></span> |    <span data-ttu-id="85246-125">msdyn_contractlineid</span><span class="sxs-lookup"><span data-stu-id="85246-125">msdyn_contractlineid</span></span>
<span data-ttu-id="85246-126">msdyn_contractlinescheduleofvalue（项目合同子项里程碑）</span><span class="sxs-lookup"><span data-stu-id="85246-126">msdyn_contractlinescheduleofvalue (Project Contract Line Milestone)</span></span> |   <span data-ttu-id="85246-127">msdyn_contractline</span><span class="sxs-lookup"><span data-stu-id="85246-127">msdyn_contractline</span></span> |    <span data-ttu-id="85246-128">msdyn_contractlineid</span><span class="sxs-lookup"><span data-stu-id="85246-128">msdyn_contractlineid</span></span>
<span data-ttu-id="85246-129">msdyn_fact（事实）</span><span class="sxs-lookup"><span data-stu-id="85246-129">msdyn_fact (Fact)</span></span> | <span data-ttu-id="85246-130">msdyn_salescontractline</span><span class="sxs-lookup"><span data-stu-id="85246-130">msdyn_salescontractline</span></span> |   <span data-ttu-id="85246-131">msdyn_salescontractlineid</span><span class="sxs-lookup"><span data-stu-id="85246-131">msdyn_salescontractlineid</span></span>
<span data-ttu-id="85246-132">msdyn_invoicelinetransaction（发票明细详细信息）</span><span class="sxs-lookup"><span data-stu-id="85246-132">msdyn_invoicelinetransaction (Invoice Line Detail)</span></span> | <span data-ttu-id="85246-133">msdyn_invoiceline</span><span class="sxs-lookup"><span data-stu-id="85246-133">msdyn_invoiceline</span></span> <br> <span data-ttu-id="85246-134">msdyn_salescontractline</span><span class="sxs-lookup"><span data-stu-id="85246-134">msdyn_salescontractline</span></span> | <span data-ttu-id="85246-135">msdyn_invoicelineid</span><span class="sxs-lookup"><span data-stu-id="85246-135">msdyn_invoicelineid</span></span> <br> <span data-ttu-id="85246-136">msdyn_salescontractlineid</span><span class="sxs-lookup"><span data-stu-id="85246-136">msdyn_salescontractlineid</span></span>
<span data-ttu-id="85246-137">msdyn_journalline（日记帐行）</span><span class="sxs-lookup"><span data-stu-id="85246-137">msdyn_journalline (Journal Line)</span></span> |  <span data-ttu-id="85246-138">msdyn_salescontractline</span><span class="sxs-lookup"><span data-stu-id="85246-138">msdyn_salescontractline</span></span> |   <span data-ttu-id="85246-139">msdyn_salescontractlineid</span><span class="sxs-lookup"><span data-stu-id="85246-139">msdyn_salescontractlineid</span></span>
<span data-ttu-id="85246-140">msdyn_orderlineresourcecategory（项目合同子项资源类别）</span><span class="sxs-lookup"><span data-stu-id="85246-140">msdyn_orderlineresourcecategory (Project Contract Line Resource Category)</span></span> | <span data-ttu-id="85246-141">msdyn_salescontractline</span><span class="sxs-lookup"><span data-stu-id="85246-141">msdyn_salescontractline</span></span> |   <span data-ttu-id="85246-142">msdyn_contractlineid</span><span class="sxs-lookup"><span data-stu-id="85246-142">msdyn_contractlineid</span></span>
<span data-ttu-id="85246-143">msdyn_orderlinetransaction（项目合同子项详细信息）</span><span class="sxs-lookup"><span data-stu-id="85246-143">msdyn_orderlinetransaction (Project Contract Line Detail)</span></span> | <span data-ttu-id="85246-144">msdyn_salescontractline</span><span class="sxs-lookup"><span data-stu-id="85246-144">msdyn_salescontractline</span></span> |   <span data-ttu-id="85246-145">msdyn_salescontractlineid</span><span class="sxs-lookup"><span data-stu-id="85246-145">msdyn_salescontractlineid</span></span>
<span data-ttu-id="85246-146">msdyn_orderlinetransactioncategory（项目合同子项交易类别）</span><span class="sxs-lookup"><span data-stu-id="85246-146">msdyn_orderlinetransactioncategory (Project Contract Line Transaction Category)</span></span> |   <span data-ttu-id="85246-147">msdyn_contractline</span><span class="sxs-lookup"><span data-stu-id="85246-147">msdyn_contractline</span></span> |    <span data-ttu-id="85246-148">msdyn_contractlineid</span><span class="sxs-lookup"><span data-stu-id="85246-148">msdyn_contractlineid</span></span>
<span data-ttu-id="85246-149">msdyn_orderlinetransactionclassification（项目合同子项交易分类）</span><span class="sxs-lookup"><span data-stu-id="85246-149">msdyn_orderlinetransactionclassification (Project Contract Line Transaction Classification)</span></span> |   <span data-ttu-id="85246-150">msdyn_contractline</span><span class="sxs-lookup"><span data-stu-id="85246-150">msdyn_contractline</span></span> |    <span data-ttu-id="85246-151">msdyn_contractlineid</span><span class="sxs-lookup"><span data-stu-id="85246-151">msdyn_contractlineid</span></span>
<span data-ttu-id="85246-152">msdyn_quotelineinvoiceschedule（报价单明细发票计划）</span><span class="sxs-lookup"><span data-stu-id="85246-152">msdyn_quotelineinvoiceschedule (Quote Line Invoice Schedule)</span></span> |  <span data-ttu-id="85246-153">msdyn_quoteline</span><span class="sxs-lookup"><span data-stu-id="85246-153">msdyn_quoteline</span></span> |   <span data-ttu-id="85246-154">msdyn_quotelineid</span><span class="sxs-lookup"><span data-stu-id="85246-154">msdyn_quotelineid</span></span>
<span data-ttu-id="85246-155">msdyn_quotelineresourcecategory（报价单明细资源类别）</span><span class="sxs-lookup"><span data-stu-id="85246-155">msdyn_quotelineresourcecategory (Quote Line Resource Category)</span></span> |    <span data-ttu-id="85246-156">msdyn_quoteline</span><span class="sxs-lookup"><span data-stu-id="85246-156">msdyn_quoteline</span></span> |   <span data-ttu-id="85246-157">msdyn_quotelineid</span><span class="sxs-lookup"><span data-stu-id="85246-157">msdyn_quotelineid</span></span>
<span data-ttu-id="85246-158">msdyn_quotelinescheduleofvalue（报价单明细里程碑）</span><span class="sxs-lookup"><span data-stu-id="85246-158">msdyn_quotelinescheduleofvalue (Quote Line Milestone)</span></span> | <span data-ttu-id="85246-159">msdyn_quoteline</span><span class="sxs-lookup"><span data-stu-id="85246-159">msdyn_quoteline</span></span> |   <span data-ttu-id="85246-160">msdyn_quotelineid</span><span class="sxs-lookup"><span data-stu-id="85246-160">msdyn_quotelineid</span></span>
<span data-ttu-id="85246-161">msdyn_quotelinetransaction（报价单明细详细信息）</span><span class="sxs-lookup"><span data-stu-id="85246-161">msdyn_quotelinetransaction (Quote Line Detail)</span></span> |    <span data-ttu-id="85246-162">msdyn_quoteline</span><span class="sxs-lookup"><span data-stu-id="85246-162">msdyn_quoteline</span></span> |   <span data-ttu-id="85246-163">msdyn_quotelineid</span><span class="sxs-lookup"><span data-stu-id="85246-163">msdyn_quotelineid</span></span>
<span data-ttu-id="85246-164">msdyn_quotelinetransactioncategory（报价单明细交易类别）</span><span class="sxs-lookup"><span data-stu-id="85246-164">msdyn_quotelinetransactioncategory (Quote Line Transaction Category)</span></span> |  <span data-ttu-id="85246-165">msdyn_quoteline</span><span class="sxs-lookup"><span data-stu-id="85246-165">msdyn_quoteline</span></span> |   <span data-ttu-id="85246-166">msdyn_quotelineid</span><span class="sxs-lookup"><span data-stu-id="85246-166">msdyn_quotelineid</span></span>
<span data-ttu-id="85246-167">msdyn_quotelinetransactionclassification（报价单明细交易分类）</span><span class="sxs-lookup"><span data-stu-id="85246-167">msdyn_quotelinetransactionclassification (Quote Line Transaction Classification)</span></span> |  <span data-ttu-id="85246-168">msdyn_quoteline</span><span class="sxs-lookup"><span data-stu-id="85246-168">msdyn_quoteline</span></span> |   <span data-ttu-id="85246-169">msdyn_quotelineid</span><span class="sxs-lookup"><span data-stu-id="85246-169">msdyn_quotelineid</span></span>
<span data-ttu-id="85246-170">SalesOrderDetail（订单明细）</span><span class="sxs-lookup"><span data-stu-id="85246-170">SalesOrderDetail (Order Line)</span></span> | <span data-ttu-id="85246-171">msdyn_quotelineid</span><span class="sxs-lookup"><span data-stu-id="85246-171">msdyn_quotelineid</span></span> | <span data-ttu-id="85246-172">msdyn_quoteline</span><span class="sxs-lookup"><span data-stu-id="85246-172">msdyn_quoteline</span></span> 

### <a name="deprecated-custom-views-and-controls"></a><span data-ttu-id="85246-173">弃用的自定义视图和控件</span><span class="sxs-lookup"><span data-stu-id="85246-173">Deprecated custom views and controls</span></span>
<span data-ttu-id="85246-174">已弃用了以下自定义视图和控件，及其相关项目。</span><span class="sxs-lookup"><span data-stu-id="85246-174">The following custom views and controls, and their related artifacts, have been deprecated.</span></span>

- <span data-ttu-id="85246-175">应计费视图。</span><span class="sxs-lookup"><span data-stu-id="85246-175">Chargeability view.</span></span>
- <span data-ttu-id="85246-176">**项目信息** 页上用于显示报价单明细的报价单明细详细信息的自定义网格视图。</span><span class="sxs-lookup"><span data-stu-id="85246-176">Custom grid controls for showing quote line details on the **Project Information** page for the quote line.</span></span>
- <span data-ttu-id="85246-177">**项目信息** 页上用于显示销售订单明细的项目合同明细详细信息的自定义网格视图。</span><span class="sxs-lookup"><span data-stu-id="85246-177">Custom grid controls for showing project contract line details on the **Project Information** page for the sales order line.</span></span>

> [!NOTE]
> <span data-ttu-id="85246-178">有关已弃用资源的完整列表，请参阅 [Project Service Automation 3.x 中的已弃用 Web 资源](../developer-guides/web-resources-deprecated-v3.x.md)</span><span class="sxs-lookup"><span data-stu-id="85246-178">For the full list of deprecated resources, see [Deprecated Web resources in Project Service Automation v3.x](../developer-guides/web-resources-deprecated-v3.x.md)</span></span>

## <a name="unified-client-interface-app-module"></a><span data-ttu-id="85246-179">统一客户端界面应用程序模块</span><span class="sxs-lookup"><span data-stu-id="85246-179">Unified Client Interface App Module</span></span>
<span data-ttu-id="85246-180">由于引入了统一客户端界面 (UCI) 应用程序模块，所以系统中已移除了 PSA 站点地图条目。</span><span class="sxs-lookup"><span data-stu-id="85246-180">With the introduction of Unified Client Interface (UCI) App Modules, the PSA site map entries have been removed from the system.</span></span>  
<span data-ttu-id="85246-181">已弃用了与商机、报价单、订单、发票的窗体切换有关的功能，因为 UCI 应用程序模块中仅包含这些窗体的 PSA 版本，所以不再需要该功能。</span><span class="sxs-lookup"><span data-stu-id="85246-181">Functionality related to form switching for Opportunity, Quote, Order, Invoice has been deprecated as it is no longer required because the UCI App Module includes only PSA versions of the forms.</span></span>  

<span data-ttu-id="85246-182">已弃用了以下 Web 资源：</span><span class="sxs-lookup"><span data-stu-id="85246-182">The following web resources have been deprecated:</span></span>

- <span data-ttu-id="85246-183">msdyn_\SalesDocument\SalesDocumentFormLoader.js</span><span class="sxs-lookup"><span data-stu-id="85246-183">msdyn_\SalesDocument\SalesDocumentFormLoader.js</span></span>
- <span data-ttu-id="85246-184">msdyn_\SalesDocument\PSSalesDocumentCustomFormIds.js</span><span class="sxs-lookup"><span data-stu-id="85246-184">msdyn_\SalesDocument\PSSalesDocumentCustomFormIds.js</span></span>

> [!NOTE]
> <span data-ttu-id="85246-185">有关已弃用资源的完整列表，请参阅 [Project Service Automation 3.x 中的已弃用 Web 资源](../developer-guides/web-resources-deprecated-v3.x.md)。</span><span class="sxs-lookup"><span data-stu-id="85246-185">For the full list of deprecated resources, see [Deprecated Web resources in Project Service Automation v3.x](../developer-guides/web-resources-deprecated-v3.x.md).</span></span>




[!INCLUDE[footer-include](../../includes/footer-banner.md)]