---
title: 2021 年 8 月新增功能 - Project Operations 精简版部署
description: 本文提供有关 2021 年 8 月版 Project Operations 精简部署中可用的质量更新的信息。
author: sigitac
ms.date: 08/10/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 84318a26d97355fe56794e1d1532576cde4af661
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8922027"
---
# <a name="whats-new-august-2021---project-operations-lite-deployment"></a>2021 年 8 月新增功能 - Project Operations 精简版部署

_适用范围：精简部署 - 估价交易开票_

本文适用于以下 Dynamics 365 Project Operations 组件和版本：

  - Dataverse 环境中的 Project Operations 版本 4.13.0.152

## <a name="features-included-in-this-release"></a>此版本中包括的功能

此版本包含以下功能：

- **审批集**：审批集将时间、支出或材料用量审批请求组合在一起，构成较小的操作子集。 此分组允许项目按特定顺序处理审批，并允许重试和排序。 对于大量审批来说，组合请求可以提升审批处理的可靠性和可跟踪性。 有关详细信息，请参阅[审批集](../../approvals/approval-sets.md)。

## <a name="quality-updates"></a>质量更新

### <a name="project-operations-on-dataverse"></a>Dataverse 上的 Project Operations

| **功能区域** | **参考编号** | **质量更新** |
| --- | --- | --- |
| 计费和定价 | 2295625 | 必须将里程碑名称从发票计划复制到发票行明细。 |
| 计费和定价 | 2316323 | Project Operations 中基于资源的方案的估价发票中的折扣不应可编辑。 |
|   商机管理 | 2338619 | 只能通过页面调用 **商机** 和 **报价单** 业务规则。 |
| 资源管理 | 2316523 | 使用来自附加了角色的资源要求的 **发送请求** 时，不应显示错误。 |
| 资源管理 | 2326885 | 通过项目创建资源要求不应显示错误。 |
| 时间和支出 | 2335584 | 时间条目中已弃用的任务流。 |
| 时间和支出 | 2336884 | **复制周** 时间条目按钮必须不仅支持当前用户。 |
