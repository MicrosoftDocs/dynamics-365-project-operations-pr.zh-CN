---
title: 2022 年 9 月新增功能 - 基于资源/非库存场景的 Project Operations
description: 本文提供有关 2022 年 9 月版基于资源/非库存场景的 Microsoft Dynamics 365 Project Operations 中可用的质量更新的信息。
author: ramagadu
ms.date: 09/28/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: ramagadu
ms.openlocfilehash: ef8b4dd98d64dac1e2420f8e6a104258f126f112
ms.sourcegitcommit: a2d720ac6d7ddb20a0967fe87992a376b2478208
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/04/2022
ms.locfileid: "9621207"
---
# <a name="whats-new-september-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>2022 年 9 月新增功能 - 基于资源/非库存场景的 Project Operations

_**适用于：** 面向资源/非库存场景的 Project Operations_

本文适用于以下 Microsoft Dynamics 365 Project Operations 组件和版本：

- Dataverse 环境中的 Project Operations 版本 4.46.0.60
- Dynamics 365 Finance 环境中的项目管理和会计版本 10.0.29

## <a name="features-included-in-this-release"></a>此版本中包括的功能

| 功能区域 | 功能名称 | 详细信息 |
| --- | --- | --- |
| 商机管理 | **报价单修订和激活**<br>Project Operations 引入了对销售流程的完全支持。 可以激活项目报价单来表示报价单为只读且正在接受审核的状态。 可以修订激活的报价单来创建具有递增修订号的新报价单。 激活的项目报价单或报价单修订可以作为赢单或丢单关闭。 | [激活和修订项目报价单](/dynamics365/project-operations/sales/activation-and-revision) |
| 计费和定价 | **与时区无关的价格默认**<br>Project Operations 在所有项目实际值中引入了与时区无关的日期概念。 现在，日记帐行和实际值中有一个新字段 **交易日期**，用于存储交易发生的日期，但不会将该日期转换为协调世界时。 此日期将用于下游流程，如价格默认和发票创建。 | <p>[确定基于项目的估算和实际值的成本费率](/dynamics365/project-operations/pricing-costing/cost-price-resolution)</p><p>[确定基于项目的估计值和实际值的销售价](/dynamics365/project-operations/pricing-costing/sales-price-resolution)</p> |
| 计费和定价 | **Project Operations 中的生效日期价格替代**<br>生效日期价格替代提供一种替代或更改价目表中特定价格的方法。 | [生效日期价格自定义](/dynamics365/project-operations/pricing-costing/dateffective_price_overrides) |
| 转包 | **分包和供应商发票对帐**<br>此功能让客户能够创建分包合同，来购买用于项目工作的资源时间、支出类别和材料。 另外还允许客户在财务和运营应用中记录供应商发票，这些发票将在 Dataverse 中提供给项目经理进行验证。 | <p>[分包合同管理](/dynamics365/project-operations/pro/subcontracting/managing-subcontracts-overview)</p><p>[创建供应商发票](/dynamics365/project-operations/procurement/vendor-invoicing-concept-and-creation)</p> |
| 时间和支出 | **全局审批者**<br>此功能支持独立软件供应商 (ISV) 和集中审批，不考虑项目或项目中团队成员的状态。 | [安全和审批](/dynamics365/project-operations/approvals/approvals-security) |
| 支出管理 | **以供应商货币过帐支出负债的功能**<br>此功能允许以现金付款方式的供应商货币过帐支出报表。 | [以供应商货币过帐支出负债的功能](/dynamics365/project-operations/expense/posting-expense-reports#enable-the-ability-to-post-expense-liability-in-vendor-currency-for-cash-payment-method-feature) |
| 项目采购 | **“即收即付”供应商付款**<br>此功能让“即收即付”(PWP) 功能可以用于 Project Operations 非库存环境。 它允许根据保留条款阻止/保留供应商付款，直到收到客户付款。 | [“即收即付”供应商付款](/dynamics365/project-operations/procurement/pay-when-paid) |
| 项目采购 | **项目采购申请**<br>此功能让用户能够在启用了 Dynamics 365 Customer Engagement 上的 Project Operations 集成的法人中创建与项目相关的采购订单。 项目采购订单可用于记录采购部门角色针对项目进行的非库存材料采购。 项目采购订单不会同步到 Dataverse。 但是，您可以使用虚拟实体在 Dataverse 中显示项目采购订单行，为项目经理提供信息。 与项目相关的供应商发票成本将与 Dataverse 中的项目实际值实体集成。 项目成本使用 Project Operations 集成日记账记录在项目子分类帐中。 | |

## <a name="project-operations-dual-write-maps-updates"></a>Project Operations 双重写入映射更新

下表显示了在 2022 年 9 月版 Project Operations 中修改或添加的双写入映射。

| 实体映射 | 更新版本 | 注释  |
| -------------- | ------------------- | ------------|
| Project Operations 集成实际值 (msdyn_actuals) | 1.0.0.15 | 此映射支持在基于资源的场景中使用 Project Operations 进行分包合同实际值处理。 |
| Project Operations 集成项目供应商发票导出实体 (msdyn_projectvendorinvoices) | 1.0.0.2 | 此映射支持在基于资源的场景中使用 Project Operations 进行分包合同实际值处理。 |
| Project Operations 集成项目供应商发票明细导出实体 (msdyn_projectvendorinvoicelines) | 1.0.0.5 | 此映射支持在基于资源的场景中使用 Project Operations 进行分包合同实际值处理。 |

当更新 Project Operations Dataverse 解决方案和 Finance 解决方案版本时，始终运行您环境中的最新映射版本并启用所有相关表映射。 如果未激活映射的最新版本，某些特性和功能可能无法正常运行。 您可以在 **双重写入** 页的 **版本** 列中查看映射的活动版本。 要激活映射的新版本，请选择 **表映射版本**，选择最新版本，然后保存所选版本。 如果您已经自定义了现成的表映射，请重新应用更改。 有关详细信息，请参阅[应用程序生命周期管理](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management)。

如果您在启动映射时遇到问题，请按照双重写入故障排除指南的[映射中缺少表列问题](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps)部分中的说明进行操作。

## <a name="quality-updates"></a>质量更新

### <a name="project-operations-on-dataverse"></a>Dataverse 上的 Project Operations

| 功能区域 | 参考编号 | 质量更新 |
| --- | --- | --- |
| 计费和定价 | 2754422 | 在 Dataverse 中复制项目时，材料和支出估算不会流入 Finance。 |
| 时间和支出 | 2787409 | 无效的审批者可以审批非项目时间条目。 |
| 商机管理 | 2788907 | 更新了对包含标志的订单行进行唯一性验证的错误消息。 |
| 时间和支出 | 2842253 | 时间审批的 null 异常处理。 |
| 计费和定价 | 2844181 | 获取相关 ID 失败会阻止发票创建。 |
| 计费和定价 | 2876628 | QLD、CLD - 估算价目表解析应使用价目表的旧日期范围字段。 |
| 转包 | 2893222 | 如果没有为分包合同子项指定角色，应该可以在团队成员上为任何角色选择该行。 |

### <a name="project-management-and-accounting-in-finance"></a>Finance 中的项目管理和会计

有关此更新中包含的缺陷修复的信息，请登录 Microsoft Dynamics Lifecycle Services，然后查看[知识库文章](https://fix.lcs.dynamics.com/Issue/Details?bugId=726559)。

## <a name="features-turned-on-by-default-in-upcoming-release"></a>即将发布的版本中默认启用的功能

下表列出了版本 10.0.30 中默认启用的功能。 大多数自动启用的功能都可以在[功能管理](/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview)中关闭。 将来，某些已自动开启的功能可能会从功能管理中移除并成为强制性功能。 此更改可确保客户使用当前功能，以便在添加时可以在当前功能的基础上生成增强功能。 永远不会在不到一年的时间内自动启用功能，除非确定它们是必不可少的功能。

| 功能名称 | 启用日期 | 功能添加时间 | 功能状态 | 模块 |
| --- | --- | --- |--- |--- |
| 当用户需要在同步和异步操作之间切换时，启用异步操作 | 2022 年 10 月 21 日 | 2021 年 4 月 9 日 | 默认打开 | 支出管理 |
| 需要对收据进行支出策略评估 | 2022 年 10 月 21 日 | 2021 年 12 月 20 日 | 默认打开 | 支出管理 |
| 委派工作人员创建的支出报表的列表视图 | 2022 年 10 月 21 日 | 2020 年 2 月 19 日 | 默认打开 | 支出管理 |
| 按会计年度进行的总里程数计算 | 2022 年 10 月 21 日 | 2022 年 5 月 10 日 | 默认打开 | 支出管理 |
