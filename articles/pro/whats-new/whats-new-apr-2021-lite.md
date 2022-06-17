---
title: 2021 年 4 月新增功能 - Project Operations 精简部署
description: 本文提供有关 2021 年 4 月版 Project Operations 精简部署中可用的质量更新的信息。
author: sigitac
ms.date: 04/07/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 987eeaf2e57659a6facae6b0a3688f15992e8bb9
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8931228"
---
# <a name="whats-new-april-2021---project-operations-lite-deployment"></a>2021 年 4 月新增功能 - Project Operations 精简部署

_适用范围：精简部署 - 估价交易开票_

本文适用于以下 Dynamics 365 Project Operations 组件和版本：

  - Dataverse 环境中的 Project Operations 版本 4.9.0.221 

## <a name="features-included-in-this-release"></a>此版本中包括的功能

此版本包含以下功能：

- 项目的非库存材料。 关键功能包括：
  - 在项目的销售周期中对非库存材料进行估算和定价。 有关详细信息，请参阅[设置目录产品的成本和销售费率 - 精简](../pricing-costing/set-up-cost-sales-rates-catalog-products.md)。
  - 在项目交付期间跟踪非库存材料的使用情况。 有关详细信息，请参阅[记录项目和项目任务的材料使用情况](../../material/material-usage-log.md)。
  - 开票功能使用了非库存材料成本。 有关详细信息，请参阅[管理记帐积压 - 精简](../proforma-invoicing/manage-billing-backlog-sales.md#product-billing-backlog)。
  - Dynamics 365 Dataverse 中的新 API 允许对 **计划实体** 执行创建、更新和删除操作。 有关详细信息，请参阅[使用计划 API 对计划实体执行操作](../../project-management/schedule-api-preview.md)。

## <a name="quality-updates"></a>质量更新

| **功能区域** | **参考编号** | **质量更新** |
| --- | --- | --- |
| 计费和定价 | 2224568 | 添加了用于启用涉及调用发票确认插件的自定义项的逻辑。 |
| 计费和定价 | 2101098 | 改进了估价发票默认字段的逻辑：**帐单寄往地址**、**帐单邮寄地址名称** 和 **付款条款** 现在根据相应的项目合同客户记录进行默认。 |
| 计费和定价 | 2021413 | 更新了 **任务** 实体上的 **实际成本** 和 **销售** 字段，以包含任务未记帐和记帐费用中的销售值。 |
| 计费和定价 | 2182110 | 复制项目合同时，将在目标项目合同中重新生成合同子项 ID，以确保其唯一性。 |
| 商机管理 | 2186741 | 添加了验证以确保无法对现有报价单明细详细信息更新 **来源** 字段和 **交易类型**。 |
| 商机管理 | 2191353 | 不能基于时间和材料合同子项创建里程碑。 |
| 商机管理 | 2216956 | 修正了 **更新价格** 的问题。 |
| 规划和跟踪 | 2182979 | 改进了项目复制功能，以确保从原始项目复制支出估算明细。 |
| 规划和跟踪 | 2184144 | 改进了项目复制功能，以确保从原始项目复制资源位置名称。 |
| 规划和跟踪 | 2184799 | 项目复制：加强了控制，以确保在复制过程中不能更改估计的开始日期。 |
| 规划和跟踪 | 2185134 | 项目副本：目标项目的预计开始日期设置为今天的日期。 |
| 规划和跟踪 | 2196373 | 项目复制：确保项目经理和团队成员记录不会在项目团队中重复。 |
| 规划和跟踪 | 2211833 | 项目副本：将资源分派从来源项目任务复制到目标项目。 |
| 规划和跟踪 | 2186541 | 修正了按资源分组时 **估算** 网格中的问题。 |
| 规划和跟踪 | 2166906 | 任务中的交易类别必须复制到 **资源分派** 实体。 |
| 资源管理 | 2125362 | 修正了使用基于小时的分配方法创建通用团队成员的问题。 |
| 时间和支出 | 2113603 | 修复了从 **时间条目** 页删除属性的自定义项相关问题。 系统现在会先检查页面上是否存在该属性，然后再使用脚本访问它们。 |
| 时间和支出 | 2204377 | 在输入时间期间选择 **复制周** 时，必须自动显示复制的时间表。 |
| 时间和支出 | 2209059 | 可以为 Dynamics 365 Field Service 时间条目编辑 **状态** 字段。 |
