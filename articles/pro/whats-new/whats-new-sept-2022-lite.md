---
title: 2022 年 9 月新增功能 - Project Operations 精简部署
description: 本文提供有关 2022 年 9 月版 Microsoft Dynamics 365 Project Operations 精简部署中可用的质量更新的信息。
author: ramagadu
ms.date: 09/28/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: ramagadu
ms.openlocfilehash: a02ac7a69489bc7974eb0e63c11fa5de74795b78
ms.sourcegitcommit: b3a70bc4f2850cff5c2b7114cff7bd61ec298143
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/06/2022
ms.locfileid: "9634841"
---
# <a name="whats-new-september-2022---project-operations-lite-deployment"></a>2022 年 9 月新增功能 - Project Operations 精简部署

_**适用于：** 精简部署 - 估价交易开票_

本文适用于以下 Microsoft Dynamics 365 Project Operations 组件和版本：

- Dataverse 环境中的 Project Operations 版本 4.46.0.60

## <a name="features-included-in-this-release"></a>此版本中包括的功能

| 功能区域 | 功能名称 | 详细信息 |
| --- | --- | --- |
| 商机管理 | **报价单修订和激活**<br>Project Operations 引入了对销售流程的完全支持。 可以激活项目报价单来表示报价单为只读且正在接受审核的状态。 可以修订激活的报价单来创建具有递增修订号的新报价单。 激活的项目报价单或报价单修订可以作为赢单或丢单关闭。 | [激活和修订项目报价单](/dynamics365/project-operations/sales/activation-and-revision) |
| 计费和定价 | **与时区无关的价格默认**<br>Project Operations 在所有项目实际值中引入了与时区无关的日期概念。 现在，日记帐行和实际值中有一个新字段 **交易日期**，用于存储交易发生的日期，但不会将该日期转换为协调世界时。 此日期将用于下游流程，如价格默认和发票创建。 | <p>[确定基于项目的估算和实际值的成本费率](/dynamics365/project-operations/pro/pricing-costing/cost-price-resolution-sales)</p><p>[确定基于项目的估计值和实际值的销售价](/dynamics365/project-operations/pro/pricing-costing/sales-price-resolution-sales)</p> |
| 计费和定价 | **Project Operations 中的生效日期价格替代**<br>生效日期价格替代提供一种替代或更改价目表中特定价格的方法。 | [生效日期价格自定义](/dynamics365/project-operations/pricing-costing/dateffective_price_overrides) |
| 时间和支出 | **全局审批者**<br>此功能支持独立软件供应商 (ISV) 和集中审批，不考虑项目或项目中团队成员的状态。 | [安全和审批](/dynamics365/project-operations/approvals/approvals-security) |
|项目规划和跟踪|**使用项目计划 API 对计划实体执行操作** </br> </br>资源分配信息编辑 API 允许开发人员在任何支持的日期范围内以编程方式指定任务被分配人的工作量，以进行更精细的分时间段工作量计划。|[使用项目计划 API 对计划实体执行操作](/dynamics365/project-operations/project-management/schedule-api-preview)|

## <a name="quality-updates"></a>质量更新

| 功能区域 | 参考编号 | 质量更新 |
| --- | --- | --- |
| 计费和定价 | 2754422 | 在 Dataverse 中复制项目时，材料和支出估算不会流入 Dynamics 365 Finance。 |
| 时间和支出 | 2787409 | 无效的审批者可以审批非项目时间条目。 |
| 商机管理 | 2788907 | 更新了对包含标志的订单行进行唯一性验证的错误消息。 |
| 时间和支出 | 2842253 | 时间审批的 null 异常处理。 |
| 计费和定价 | 2844181 | 获取相关 ID 失败会阻止发票创建。 |
| 计费和定价 | 2876628 | QLD、CLD - 估算价目表解析应使用价目表的旧日期范围字段。 |
| 转包 | 2893222 | 如果没有为分包合同子项指定角色，应该可以在团队成员上为任何角色选择该行。 |
