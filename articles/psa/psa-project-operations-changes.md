---
title: 从 Project Service Automation 到 Project Operations 的功能变化
description: 本文概述了从 Project Service Automation 到 Dynamics 365 Project Operations 的功能变化。
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 02/03/2022
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.reviewer: johnmichalak
ms.openlocfilehash: a9c69fc4296d30763f3994a4955e64ab258ceb4f
ms.sourcegitcommit: 675e9f3615e701c5f998de3a5ea3e25df11ae107
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/09/2022
ms.locfileid: "9459915"
---
# <a name="feature-changes-from-project-service-automation-to-project-operations"></a>从 Project Service Automation 到 Project Operations 的功能变化

从 Dynamics 365 Project Service Automation 到 Dynamics 365 Project Operations Lite 的升级将分三个阶段进行。 本文提供有关升级完成后您可能会看到的主要变化的信息。

| 升级交付 | 第 1 阶段 <br>（2022 年 1 月） | 第 2 阶段 <br>（2022 年 11 月） | 第 3 阶段  |
|------------------|------------------------|---------------------------|---------------------------|
| 项目不依赖工作分解结构 (WBS)。 | :heavy_check_mark: | :heavy_check_mark: | :heavy_check_mark: |
| WBS 包含在当前支持的 Project Operations 限制中。 | &nbsp; | :heavy_check_mark: | :heavy_check_mark: |
| Project Operations 的当前受支持限制外的 WBS，包括对 Project Desktop Client 的支持。 | &nbsp; | &nbsp; | :heavy_check_mark: |

## <a name="project-management"></a>项目管理

用户体验中最显著的变化将出现在项目计划方面。 Project Operations 通过利用 [Project for the Web](https://support.microsoft.com/en-us/office/what-is-project-for-the-web-c19b2421-3c9d-4037-97c6-f66b6e1d2eb5) 提供的计划功能，采用全新的现代体验来管理工作分解结构 (WBS)。

## <a name="differences-in-the-scheduling-experience"></a>计划体验的不同之处

下表总结了 Project Service Automation 和 Project Operations 之间的计划差异。

|  日程安排     |   Project Operations   |   PSA   |
|-----------------|------------------------|---------|
| 项目模板 - 能够在创建项目时定义和应用项目模板  |  &nbsp;    | :heavy_check_mark: |
| 项目工作分解结构 (WBS) 与桌面客户端的集成   |    &nbsp;  | :heavy_check_mark: |
| 约束 - 开始不早于，完成不晚于  | :heavy_check_mark: |   &nbsp;  |
| 里程碑 - 持续时间为零的任务   | :heavy_check_mark:  |  &nbsp;  |
| 资源驱动的任务将遵从所分配资源的可用性   | :heavy_check_mark: |  &nbsp;    |
| 分时段编辑 - 每天编辑计划和工作   |   &nbsp;  | :heavy_check_mark: |
| 自动/手动计划 - 使用项目计划引擎自动或手动计划任务 |  &nbsp; | :heavy_check_mark:  |
| 直接在用户界面中编辑大型项目：可编辑的计划大小没有限制  | 500 任务限制  | :heavy_check_mark:       |
| 完成百分比 - 标记任务进度   | :heavy_check_mark:  |  &nbsp;  |
| [项目计划模式](../project-management/scheduling-modes.md) - 将项目定义为固定单位、固定工作量或固定持续时间 | :heavy_check_mark: | &nbsp; |
| 时间线 - 构建和自定义时间线视图以可视化计划详细信息并与利益干系人进行沟通。 | :heavy_check_mark:  | &nbsp; |
| 工作量驱动的任务 - 计划引擎支持将任务计划为工作量驱动  | :heavy_check_mark:  | &nbsp; |
| **任务信息** 对话框 - 使用对话框保存任务详细信息 | :heavy_check_mark:  |  &nbsp;  |
| 拖放 - 选择多个任务并修改任务在 WBS 上的位置 | :heavy_check_mark: | &nbsp;  |
| 灵活的持久视图 - 定义更精细的任务属性视图   | :heavy_check_mark:  | &nbsp; |
| 对 WBS 进行排序和筛选  | :heavy_check_mark:  | &nbsp; |
| 非瀑布项目交付的版块视图  | :heavy_check_mark:   | &nbsp; |
| 时间线视图 - 交互式甘特图，用于可视化和编辑 WBS   | :heavy_check_mark:  | &nbsp; |
| 键盘快捷方式 - 使用键盘快捷方式进行常见操作，如缩进或插入  | :heavy_check_mark:  |  &nbsp; |
| 多级撤消 - 执行假设分析，通过撤消和重新应用一整套操作来充分了解更改的影响 | :heavy_check_mark: | &nbsp; |
| 剪切/复制/粘贴 - 通过在应用程序之间复制和粘贴计划详细信息来协作制定计划  | :heavy_check_mark: | &nbsp; |
| 任务清单 - 最多可将 20 个清单项添加到任务中   | :heavy_check_mark: | &nbsp; |

## <a name="project-planning"></a>项目规划

与 Project Service Automation 中的 **项目** 页面相比，Project Operations 中的 **项目** 页面有很多不同之处。

作为第 1 阶段升级的一部分，以下操作已被从 **项目** 页面中删除：

  - **在 MS Project 中打开**
  - **创建模板**
  - **取消与 MS Project 的链接**

Project Operations 中的 **项目** 页面包括以下新选项卡。

- **材料估算**
- **任务记帐设置**

**状态** 选项卡已被删除，**状态** 字段现在位于具有项目计划模式的 **摘要** 选项卡上。

   ![项目页面的更新。](media/projectform.png)

**计划** 选项卡已重命名为 **任务** 选项卡，具有 Project for the Web 的新项目计划体验。

   ![新的项目任务选项卡。](media/tasktab.png)

## <a name="scheduling-modes"></a>计划模式

Project Operations 引入了一项新功能[计划模式](../project-management/scheduling-modes.md)。 在 Project Operations 中，所有现有 Project Service Automation 项目都将默认为 **固定持续时间**。 但是，可以通过转到 **设置** > **参数** > **参数** > **计划模式** 来管理新项目的默认设置。

   ![计划模式的项目参数设置。](media/projectparameter.png)

## <a name="project-planning-limits"></a>项目计划限制

Project Operations 依赖 Project for the Web 进行所有项目计划操作。 Project for the Web 使用下表中的限制管理工作分解结构。

| **字段**                                          | **限制**             |
|----------------------------------------------------|-----------------------|
| 项目的最大总任务数                  | 500                   |
| 项目的最长总持续时间               | 3650 天（10 年）  |
| 项目的最大总资源数              | 300                   |
| 项目的最大总链接数（仅后续项） | 600                   |
| 项目的最大总自定义字段数          | 10                    |
| 最大层次结构级别                            | 10 个级别             |
| 最大链接数（后续项 + 前置项）            | 20                    |
| 叶节点任务的最长持续时间                      | 1250 天             |
| 摘要任务的最长持续时间                 | 3650 天（10 年）  |
| 分配给任务的最大资源数               | 20 个资源          |
| 任务支持的日期范围                    | 1/1/2000 - 12/31/2149 |
| 清单项                                    | 20                    |

## <a name="project-planning-extensibility-and-development"></a>项目计划的扩展性和开发

升级到 Project Operations 后，您必须使用项目计划 API 对以下实体执行创建、更新和删除操作：

|   实体名称           |   实体逻辑名称       |
|-------------------------|-----------------------------|
| 集成                 | msdyn_project               |
| 项目任务            | msdyn_projecttask           |
| 项目任务依赖关系 | msdyn_projecttaskdependency |
| 资源分派     | msdyn_resourceassignment    |
| 项目 Bucket          | msdyn_projectbucket         |
| 项目团队成员     | msdyn_projectteam           |

如果您当前有涉及这些实体的自定义，请参阅[使用项目计划 API 执行计划实体的操作](../project-management/schedule-api-preview.md)获取实施指南。

## <a name="data-model-changes"></a>数据模型变化

作为升级阶段 1 的一部分，对数据模型进行了一些更改。 这些更改主要是对现有实体的字段更改。 在第 1 阶段，实体 **msydn_project** 和 **msdyn_projectteam** 是对自定义的重构。 

> [!IMPORTANT]
> 本节会随着未来升级阶段的完成更新其他实体的内容。

以下字段已替换为新字段。

|   Entity          |   旧逻辑名称   |   新逻辑名称    |
|-------------------|----------------------|-----------------------|
| msdyn_project     | msdyn_actualhours    | msdyn_effortcompleted |
| msdyn_project     | msdyn_plannedhours   | msdyn_effort          |
| msdyn_project     | msdyn_remaininghours | msdyn_effortremaining |
| msdyn_project     | msdyn_scheduledend   | msdyn_finish          |
| msdyn_project     | msdyn_wbsduration    | msdyn_duration        |
| msdyn_projectteam | msdyn_assignedhours  | msdyn_effort          |
| msdyn_projectteam | msdyn_from           | msdyn_start           |
| msdyn_projectteam | msdyn_to             | msdyn_finish          |

添加了以下字段。

|   Entity          |   逻辑名称                               |   说明  |
|-------------------|----------------------------------------------|---------------|
| msdyn_project     | msdyn_actualfeesales                         | 显示项目的实际费用销售额的汇总值。 仅用于 Project Service Automation。 |
| msdyn_project     | msdyn_actualmaterialcost                     | 显示项目的实际材料成本的汇总值。 仅用于 Project Service Automation。 |
| msdyn_project     | msdyn_actualmaterialsales                    | 显示项目的实际材料销售额的汇总值。 仅用于 Project Service Automation。 |
| msdyn_project     | msdyn_businesscase                           |                |
| msdyn_project     | msdyn_contractlineproject                    | 与此项目关联的合同子项。 |
| msdyn_project     | msdyn_copyprojectcorrelationid               | 这是一个内部系统字段，用于与相关标识符相关的 **复制项目**。 仅用于 Project Service Automation。 |
| msdyn_project     | msdyn_copyprojectsessionid                   | 这是一个内部系统字段，用于与会话标识符相关的 **复制项目**。 仅用于 Project Service Automation。 |
| msdyn_project     | msdyn_globalrevisiontoken                    | 上一次从项目计划服务同步 xRM 全局修订标记。 |
| msdyn_project     | msdyn_msprojectdocument                      | 属于项目的 Microsoft Project 文档。 |
| msdyn_project     | msdyn_plannedmaterialcost                    | 项目的计划材料成本的汇总值。 仅用于 Project Service Automation。 |
| msdyn_project     | msdyn_plannedmaterialsales                   | 项目的计划材料销售额的汇总值。 仅用于 Project Service Automation。 |
| msdyn_project     | msdyn_program                                | 与此项目相关的计划。 |
| msdyn_project     | msdyn_quotelineproject                       | 与此项目关联的报价单明细。 |
| msdyn_project     | msdyn_replaylogheader                        | 重播日志的标题。 |
| msdyn_project     | msdyn_schedulemode                           | 用于项目上所有任务的默认计划模式。  |
| msdyn_project     | msdyn_taskearlieststart                      | 项目中任何任务的最早开始日期。  |
| msdyn_project     | msdyn_valuestatement                         |                |
| msdyn_projectteam | msdyn_copiedfromprojectteammember            | 从中复制此项目团队成员的项目团队成员。 |
| msdyn_projectteam | msdyn_creategenericteammemberwithrequirement | 指示是否为新创建的通用团队成员创建资源要求。  |
| msdyn_projectteam | msdyn_deletestatus                           | 团队成员的删除状态，用于跟踪是否有删除请求发送到项目计划服务，以及它是否在预期时间窗口内成功发回响应。 |
| msdyn_projectteam | msdyn_effortcompleted                        | 跟踪团队成员对其工作分配已完成的工作量。 |
| msdyn_projectteam | msdyn_effortremaining                        | 跟踪团队成员对其工作分配已完成的工作量。 |
| msdyn_projectteam | msdyn_markedfordeletiontimer                 | 从团队成员向项目计划服务发送删除请求到团队成员在 Microsoft Dataverse 上被实际删除的等待期。|
| msdyn_projectteam | msdyn_markedfordeletiontimestamp             | 记录团队成员删除请求发送到项目计划服务时的时间戳。 |
| msdyn_projectteam | msdyn_copiedfromprojectteammember            | 显示从中复制此项目团队成员的项目团队成员。  |

## <a name="project-templates"></a>项目模板

Project Operations 不提供对项目模板的支持。 但是，您可以使用[项目复制 API](../project-management/dev-copy-project.md) 复制很多核心功能。

## <a name="desktop-add-in-support"></a>桌面加载项支持

升级的前 2 个阶段将不提供对 Microsoft Project 桌面加载项的支持。 在第 3 阶段，项目大于 Project for the Web 当前支持限制的客户能够使用桌面加载项。

## <a name="editing-resource-assignment-contours"></a>编辑资源分配信息

当升级的第 2 阶段可用时，编辑资源分配信息的功能将可用。

## <a name="billing-and-pricing"></a>计费和定价

Project Operations 中添加了以下新功能。 这些功能本质上是在原功能基础上的增加，不会影响 Project Service Automation 数据模型。

- [记录项目和项目任务的材料使用情况](../material/material-usage-log.md)
- [分包合同管理](../pro/subcontracting/managing-subcontracts-overview.md)
- [预付款和保留款合同](../pro/sales/set-up-advances-retainer-based-contracts-sales.md)
- [合同上限状态和验证](../pro/proforma-invoicing/manage-nte-status-validations-sales.md)
- [基于任务的记帐](../pro/sales/mapping-projects-tasks-quote-line-sales.md)

## <a name="deprecated-components"></a>弃用组件

下表记录了升级后移至弃用组件解决方案的所有弃用字段。 有关详细信息和解决方案的链接，请参阅 [Dynamics 365 Project Service Automation 3x 到 Project Operations 4x 弃用组件](https://github.com/microsoft/Dynamics365-Project-Operations-PowerApps/tree/main/3x-4x-deprecated-solution)。

### <a name="invoicedetail"></a>invoicedetail

| 字段                                                    |
|-----------------------------------------------------------------------------------------------|
|invoicedetail.msdyn_contractline    |

### <a name="msdyn_actual"></a>msdyn_actual

| 字段                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_actual.msdyn_salescontractline                                                          |

### <a name="msdyn_characteristicreqforteammember"></a>msdyn_characteristicreqforteammember

| 字段                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_characteristicreqforteammember.msdyn_characteristic                                     |
| msdyn_characteristicreqforteammember.msdyn_characteristicreqforteammemberid                   |
| msdyn_characteristicreqforteammember.msdyn_characteristictype                                 |
| msdyn_characteristicreqforteammember.msdyn_name                                               |
| msdyn_characteristicreqforteammember.msdyn_ratingvalue                                        |
| msdyn_characteristicreqforteammember.msdyn_resourcerequirementid                              |

### <a name="msdyn_contractlineinvoiceschedule"></a>msdyn_contractlineinvoiceschedule

| 字段                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_contractlineinvoiceschedule.msdyn_contractline                                          |
| msdyn_contractlinescheduleofvalue.msdyn_contractline                                          |
 
### <a name="msdyn_dataexport"></a>msdyn_dataexport

| 字段                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_dataexport.msdyn_dataexportid                                                           |
| msdyn_dataexport.msdyn_datatoken                                                              |
| msdyn_dataexport.msdyn_entityname                                                             |
| msdyn_dataexport.msdyn_exportedrecordcount                                                    |
| msdyn_dataexport.msdyn_exportstatus                                                           |
| msdyn_dataexport.msdyn_linkedentitydata                                                       |
| msdyn_dataexport.msdyn_name                                                                   |
| msdyn_dataexport.msdyn_pagingdata                                                             |

### <a name="msdyn_fact"></a>msdyn_fact

| 字段                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_fact.msdyn_salescontractline                                                            |

### <a name="msdyn_findworkevent"></a>msdyn_findworkevent

| 字段                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_findworkevent.msdyn_bookableresource                                                    |
| msdyn_findworkevent.msdyn_findworkeventid                                                     |
| msdyn_findworkevent.msdyn_name                                                                |
| msdyn_findworkevent.msdyn_timestamp                                                           |
| msdyn_findworkevent.msdyn_type                                                                |
| msdyn_findworkevent.msdyn_value                                                               |
| msdyn_findworkevent.msdyn_work                                                                |

### <a name="msdyn_invoicelinetransaction"></a>msdyn_invoicelinetransaction

| 字段                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_invoicelinetransaction.msdyn_invoiceline                                                |
| msdyn_invoicelinetransaction.msdyn_salescontractline                                          |

### <a name="msdyn_journalline"></a>msdyn_journalline

| 字段                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_journalline.msdyn_salescontractline                                                     |

### <a name="msdyn_opportunitylineresourcecategory"></a>msdyn_opportunitylineresourcecategory

| 字段                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_opportunitylineresourcecategory.msdyn_billingtype                                       |
| msdyn_opportunitylineresourcecategory.msdyn_description                                       |
| msdyn_opportunitylineresourcecategory.msdyn_opportunitylineresourcecategoryid                 |
| msdyn_opportunitylineresourcecategory.msdyn_opportunitylinetransactionclassification          |
| msdyn_opportunitylineresourcecategory.msdyn_resourcecategory                                  |

### <a name="msdyn_opportunitylinetransaction"></a>msdyn_opportunitylinetransaction

| 字段                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_opportunitylinetransaction.msdyn_accountcustomer                                        |
| msdyn_opportunitylinetransaction.msdyn_accountingdate                                         |
| msdyn_opportunitylinetransaction.msdyn_accountvendor                                          |
| msdyn_opportunitylinetransaction.msdyn_amount                                                 |
| msdyn_opportunitylinetransaction.msdyn_amount_base                                            |
| msdyn_opportunitylinetransaction.msdyn_amountmethod                                           |
| msdyn_opportunitylinetransaction.msdyn_basisamount                                            |
| msdyn_opportunitylinetransaction.msdyn_basisamount_base                                       |
| msdyn_opportunitylinetransaction.msdyn_basisprice                                             |
| msdyn_opportunitylinetransaction.msdyn_basisprice_base                                        |
| msdyn_opportunitylinetransaction.msdyn_basisquantity                                          |
| msdyn_opportunitylinetransaction.msdyn_billingtype                                            |
| msdyn_opportunitylinetransaction.msdyn_bookableresource                                       |
| msdyn_opportunitylinetransaction.msdyn_contactcustomer                                        |
| msdyn_opportunitylinetransaction.msdyn_contactvendor                                          |
| msdyn_opportunitylinetransaction.msdyn_customertype                                           |
| msdyn_opportunitylinetransaction.msdyn_description                                            |
| msdyn_opportunitylinetransaction.msdyn_documentdate                                           |
| msdyn_opportunitylinetransaction.msdyn_enddatetime                                            |
| msdyn_opportunitylinetransaction.msdyn_exchangeratedate                                       |
| msdyn_opportunitylinetransaction.msdyn_opportunityline                                        |
| msdyn_opportunitylinetransaction.msdyn_opportunitylinetransactionid                           |
| msdyn_opportunitylinetransaction.msdyn_percent                                                |
| msdyn_opportunitylinetransaction.msdyn_price                                                  |
| msdyn_opportunitylinetransaction.msdyn_price_base                                             |
| msdyn_opportunitylinetransaction.msdyn_pricelist                                              |
| msdyn_opportunitylinetransaction.msdyn_product                                                |
| msdyn_opportunitylinetransaction.msdyn_project                                                |
| msdyn_opportunitylinetransaction.msdyn_quantity                                               |
| msdyn_opportunitylinetransaction.msdyn_resourcecategory                                       |
| msdyn_opportunitylinetransaction.msdyn_resourceorganizationalunitid                           |
| msdyn_opportunitylinetransaction.msdyn_startdatetime                                          |
| msdyn_opportunitylinetransaction.msdyn_task                                                   |
| msdyn_opportunitylinetransaction.msdyn_transactioncategory                                    |
| msdyn_opportunitylinetransaction.msdyn_transactionclassification                              |
| msdyn_opportunitylinetransaction.msdyn_transactiontypecode                                    |
| msdyn_opportunitylinetransaction.msdyn_unit                                                   |
| msdyn_opportunitylinetransaction.msdyn_unitschedule                                           |
| msdyn_opportunitylinetransaction.msdyn_vendortype                                             |

### <a name="msdyn_opportunitylinetransactioncategory"></a>msdyn_opportunitylinetransactioncategory

| 字段                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_opportunitylinetransactioncategory.msdyn_billingtype                                    |
| msdyn_opportunitylinetransactioncategory.msdyn_description                                    |
| msdyn_opportunitylinetransactioncategory.msdyn_opportunitylinetransactioncategoryid           |
| msdyn_opportunitylinetransactioncategory.msdyn_opportunitylinetransactionclassification       |
| msdyn_opportunitylinetransactioncategory.msdyn_transactioncategory                            |

### <a name="msdyn_opportunitylinetransactionclassificatio"></a>msdyn_opportunitylinetransactionclassificatio

| 字段                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_opportunitylinetransactionclassificatio.msdyn_billingtype                               |
| msdyn_opportunitylinetransactionclassificatio.msdyn_description                               |
| msdyn_opportunitylinetransactionclassificatio.msdyn_include                                   |
| msdyn_opportunitylinetransactionclassificatio.msdyn_opportunityline                           |
| msdyn_opportunitylinetransactionclassificatio.msdyn_opportunitylinetransactionclassificatioid |
| msdyn_opportunitylinetransactionclassificatio.msdyn_transactionclassification                 |

### <a name="msdyn_orderlineresourcecategory"></a>msdyn_orderlineresourcecategory

| 字段                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_orderlineresourcecategory.msdyn_contractline                                            |

### <a name="msdyn_orderlinetransaction"></a>msdyn_orderlinetransaction

| 字段                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_orderlinetransaction.msdyn_salescontractline                                            |
| msdyn_orderlinetransactioncategory.msdyn_contractline                                         |

### <a name="msdyn_orderlinetransactionclassification"></a>msdyn_orderlinetransactionclassification

| 字段                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_orderlinetransactionclassification.msdyn_contractline                                   |

### <a name="msdyn_project"></a>msdyn_project

| 字段                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_project.msdyn_actualdurationminutes                                                     |
| msdyn_project.msdyn_actualhours                                                               |
| msdyn_project.msdyn_istemplate                                                                |
| msdyn_project.msdyn_plannedhours                                                              |
| msdyn_project.msdyn_projecttemplate                                                           |
| msdyn_project.msdyn_remaininghours                                                            |
| msdyn_project.msdyn_scheduleddurationminutes                                                  |
| msdyn_project.msdyn_scheduledend                                                              |
| msdyn_project.msdyn_stagename                                                                 |
| msdyn_project.msdyn_wbsduration                                                               |


### <a name="msdyn_projecttask"></a>msdyn_projecttask

| 字段                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_projecttask.msdyn_actualdurationminutes                                                 |
| msdyn_projecttask.msdyn_actualeffort                                                          |
| msdyn_projecttask.msdyn_aggregationdirection                                                  |
| msdyn_projecttask.msdyn_assignedresources                                                     |
| msdyn_projecttask.msdyn_assignedteammembers                                                   |
| msdyn_projecttask.msdyn_autoscheduling                                                        |
| msdyn_projecttask.msdyn_costestimatecontour                                                   |
| msdyn_projecttask.msdyn_effortcontour                                                         |
| msdyn_projecttask.msdyn_islinetask                                                            |
| msdyn_projecttask.msdyn_numberofresources                                                     |
| msdyn_projecttask.msdyn_remaininghours                                                        |
| msdyn_projecttask.msdyn_resourceutilization                                                   |
| msdyn_projecttask.msdyn_salesestimatecontour                                                  |
| msdyn_projecttask.msdyn_scheduledhours                                                        |
| msdyn_projecttask.msdyn_wbsid                                                                 |

### <a name="msdyn_projecttaskstatususer"></a>msdyn_projecttaskstatususer

| 字段                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_projecttaskstatususer.msdyn_bookableresource                                            |
| msdyn_projecttaskstatususer.msdyn_description                                                 |
| msdyn_projecttaskstatususer.msdyn_expectedcompletiondate                                      |
| msdyn_projecttaskstatususer.msdyn_expectedhourstocomplete                                     |
| msdyn_projecttaskstatususer.msdyn_iscompleted                                                 |
| msdyn_projecttaskstatususer.msdyn_name                                                        |
| msdyn_projecttaskstatususer.msdyn_percentcomplete                                             |
| msdyn_projecttaskstatususer.msdyn_projecttaskid                                               |
| msdyn_projecttaskstatususer.msdyn_projecttaskstatusindicator                                  |
| msdyn_projecttaskstatususer.msdyn_projecttaskstatususerid                                     |

### <a name="msdyn_projectteam"></a>msdyn_projectteam

| 字段                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_projectteam.msdyn_applicantcount                                                        |
| msdyn_projectteam.msdyn_applicantsavailable                                                   |
| msdyn_projectteam.msdyn_assignedhours                                                         |
| msdyn_projectteam.msdyn_description                                                           |
| msdyn_projectteam.msdyn_from                                                                  |
| msdyn_projectteam.msdyn_hoursrequested                                                        |
| msdyn_projectteam.msdyn_membershipstatus                                                      |
| msdyn_projectteam.msdyn_number                                                                |
| msdyn_projectteam.msdyn_to                                                                    |

### <a name="msdyn_projectteammembersignup"></a>msdyn_projectteammembersignup

| 字段                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_projectteammembersignup.msdyn_bookableresource                                          |
| msdyn_projectteammembersignup.msdyn_membershipstatus                                          |
| msdyn_projectteammembersignup.msdyn_name                                                      |
| msdyn_projectteammembersignup.msdyn_projectteammembersignupid                                 |
| msdyn_projectteammembersignup.msdyn_teammembership                                            |

### <a name="msdyn_projecttransactioncategory"></a>msdyn_projecttransactioncategory

| 字段                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_projecttransactioncategory.msdyn_billingtype                                            |
| msdyn_projecttransactioncategory.msdyn_name                                                   |
| msdyn_projecttransactioncategory.msdyn_project                                                |
| msdyn_projecttransactioncategory.msdyn_projecttransactioncategoryid                           |
| msdyn_projecttransactioncategory.msdyn_transactioncategory                                    |

### <a name="msdyn_quotelineinvoiceschedule"></a>msdyn_quotelineinvoiceschedule

| 字段                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_quotelineinvoiceschedule.msdyn_quoteline                                                |
| msdyn_quotelineresourcecategory.msdyn_quoteline                                               |
| msdyn_quotelinescheduleofvalue.msdyn_quoteline                                                |
| msdyn_quotelinetransaction.msdyn_quoteline                                                    |
| msdyn_quotelinetransactioncategory.msdyn_quoteline                                            |
| msdyn_quotelinetransactionclassification.msdyn_quoteline                                      |

### <a name="msdyn_resourceassignment"></a>msdyn_resourceassignment

| 字段                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_resourceassignment.msdyn_hours                                                          |
| msdyn_resourceassignment.msdyn_fromdate                                                       |
| msdyn_resourceassignment.msdyn_msprojectclientid                                              |
| msdyn_resourceassignment.msdyn_todate                                                         |
| msdyn_resourceassignmentdetail.msdyn_duration                                                 |
| msdyn_resourceassignmentdetail.msdyn_from                                                     |
| msdyn_resourceassignmentdetail.msdyn_name                                                     |
| msdyn_resourceassignmentdetail.msdyn_resourceassignmentdetailid                               |
| msdyn_resourceassignmentdetail.msdyn_resourceassignmentid                                     |

### <a name="salesorderdetail"></a>salesorderdetail

| 字段                                                    |
|-----------------------------------------------------------------------------------------------|
| salesorderdetail.msdyn_quoteline                                                              |

