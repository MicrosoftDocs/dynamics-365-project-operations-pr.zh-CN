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
ms.openlocfilehash: 48062eda1f524dd3ca0d5feccf11fd5577521275
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/10/2021
ms.locfileid: "5148722"
---
# <a name="entity-control-and-user-interface-changes-project-service-automation-3x"></a>实体、控件和用户界面更改 (Project Service Automation 3.x)

[!include [banner](../../includes/psa-now-project-operations.md)]


随着 Microsoft Dynamics Project Service Automation (PSA) 3.x 的发布，对实体、控件、视图和用户界面进行了大量更改。 此主题介绍这些重要更改。

## <a name="parent-child-relationships-for-sales-document-sales-document-line-sales-document-line-detail-entities"></a>销售文档、销售文档明细、销售文档明细详细信息实体的父子关系
在 Dynamics 365 Project Service Automation (PSA) 版本 3.0 之前发布的版本中，销售文档、销售文档明细和销售文档明细详细信息实体之间的某些关系是通过其中存储相关实体的 GUID 字符串表示的字符串字段实施的。 这是因为平台限制导致解决方案的服务器端和客户端中需要大量自定义代码来让这些关系的工作方式类似典型 Dynamics CRM 实体关系的工作方式，并且让字符串字段充当查找字段。

PSA 3.0 已经过更新，现在利用销售文档与销售文档明细实体之间新的实体关系。

因为现在可以使用查找字段指示对实体的引用，所以不再需要之前版本中用于存储相关实体的 GUID 字符串值的字段，因此已将其弃用。 还弃用了用于处理旧字符串字段定义的关系的自定义客户端和服务器端代码。

### <a name="entity-schema-changes"></a>实体架构更改
下表提供实体的已弃用字符串字段与新查找字段的一对一列表。 

 实体 |   弃用字段（字符串） | 新字段（查找）
--- | --- | ---
invoicedetail（发票明细） |  msdyn_contractline |    msdyn_contractlineid
msdyn_actual（实际值） | msdyn_salescontractline |   msdyn_salescontractlineid
msdyn_contractlineinvoiceschedule（项目合同子项发票计划） |    msdyn_contractline |    msdyn_contractlineid
msdyn_contractlinescheduleofvalue（项目合同子项里程碑） |   msdyn_contractline |    msdyn_contractlineid
msdyn_fact（事实） | msdyn_salescontractline |   msdyn_salescontractlineid
msdyn_invoicelinetransaction（发票明细详细信息） | msdyn_invoiceline <br> msdyn_salescontractline | msdyn_invoicelineid <br> msdyn_salescontractlineid
msdyn_journalline（日记帐行） |  msdyn_salescontractline |   msdyn_salescontractlineid
msdyn_orderlineresourcecategory（项目合同子项资源类别） | msdyn_salescontractline |   msdyn_contractlineid
msdyn_orderlinetransaction（项目合同子项详细信息） | msdyn_salescontractline |   msdyn_salescontractlineid
msdyn_orderlinetransactioncategory（项目合同子项交易类别） |   msdyn_contractline |    msdyn_contractlineid
msdyn_orderlinetransactionclassification（项目合同子项交易分类） |   msdyn_contractline |    msdyn_contractlineid
msdyn_quotelineinvoiceschedule（报价单明细发票计划） |  msdyn_quoteline |   msdyn_quotelineid
msdyn_quotelineresourcecategory（报价单明细资源类别） |    msdyn_quoteline |   msdyn_quotelineid
msdyn_quotelinescheduleofvalue（报价单明细里程碑） | msdyn_quoteline |   msdyn_quotelineid
msdyn_quotelinetransaction（报价单明细详细信息） |    msdyn_quoteline |   msdyn_quotelineid
msdyn_quotelinetransactioncategory（报价单明细交易类别） |  msdyn_quoteline |   msdyn_quotelineid
msdyn_quotelinetransactionclassification（报价单明细交易分类） |  msdyn_quoteline |   msdyn_quotelineid
SalesOrderDetail（订单明细） | msdyn_quotelineid | msdyn_quoteline 

### <a name="deprecated-custom-views-and-controls"></a>弃用的自定义视图和控件
已弃用了以下自定义视图和控件，及其相关项目。

- 应计费视图。
- **项目信息** 页上用于显示报价单明细的报价单明细详细信息的自定义网格视图。
- **项目信息** 页上用于显示销售订单明细的项目合同明细详细信息的自定义网格视图。

> [!NOTE]
> 有关已弃用资源的完整列表，请参阅 [Project Service Automation 3.x 中的已弃用 Web 资源](../developer-guides/web-resources-deprecated-v3.x.md)

## <a name="unified-client-interface-app-module"></a>统一客户端界面应用程序模块
由于引入了统一客户端界面 (UCI) 应用程序模块，所以系统中已移除了 PSA 站点地图条目。  
已弃用了与商机、报价单、订单、发票的窗体切换有关的功能，因为 UCI 应用程序模块中仅包含这些窗体的 PSA 版本，所以不再需要该功能。  

已弃用了以下 Web 资源：

- msdyn_\SalesDocument\SalesDocumentFormLoader.js
- msdyn_\SalesDocument\PSSalesDocumentCustomFormIds.js

> [!NOTE]
> 有关已弃用资源的完整列表，请参阅 [Project Service Automation 3.x 中的已弃用 Web 资源](../developer-guides/web-resources-deprecated-v3.x.md)。


