---
title: 2022 年 3 月新增功能 - Project Operations 精简部署
description: 本主题提供有关 2022 年 3 月版 Project Operations 精简部署中可用的质量更新的信息。
author: sigitac
ms.date: 03/18/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 8a83491da1d312406dfb36f5ad214c307c15cfbf
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/14/2022
ms.locfileid: "8583739"
---
# <a name="whats-new-march-2022---project-operations-lite-deployment"></a>2022 年 3 月新增功能 - Project Operations 精简部署

_适用范围：精简部署 - 估价交易开票_

本主题适用于以下 Microsoft Dynamics 365 Project Operations 组件和版本：

- Dataverse 环境中的 Project Operations 版本 4.30.0.99

## <a name="features-included-in-this-release"></a>此版本中包括的功能

- 分包：供应商发票创建和匹配体验

## <a name="quality-updates"></a>质量更新

| 功能区域 | 参考编号 | 质量更新 |
| --- | --- | --- |
| 时间和支出 | 2388011 | 在批量审批期间向时间条目提交者显示拒绝注释。 |
| 项目规划和跟踪 | 2495294 | **任务详细信息** 页面上的项目详细信息不能进行编辑。 |
| 计费和定价 | 2499605 | 从报价单里程碑创建的合同里程碑被错误地标记为只读。 |
| 项目规划和跟踪 | 2506050 | 如果没有要保存的更改，操作集会保持待定状态一小时。 然后集被错误地标记为 **失败**，而它应该立即完成。 |
| 计费和定价 | 2507401 | 由于缓存不正确，错误地在项目中输入了默认合同签订部门。 |
| 计费和定价 | 2541660 | 双写入中的 **销售订单创建验证** 应仅适用于基于项目的订单。 |
| 计费和定价 | 2552745 | 税款在设置了拆分记帐规则的客户之间不拆分。 |
| 计费和定价 | 2558859 | 改进了设置定价维度时的错误消息。 |
| 计费和定价 | 2558933 | 当 **msdyn\_project** 添加为定价维度时，**从项目估算导入** 失败。 |
| 计费和定价 | 2559101 | 项目参数删除不会被阻止并导致问题。 |
|   商机管理 | 2570390 | 双写入插件强制报价单、订单和商机上的客户类型为 **客户**，即使该客户类型不正确。 |
| 计费和定价 | 2586097 | 从项目合同子项中删除项目时，不会冲销拆分的已记帐实际成本。 |
| 计费和定价 | 2589619 | 目录外材料的税款会传播到未记帐实际销售额和发票。 |
|   商机管理 | 2594015 | 对于具有 **Net60** 付款条款的客户，报价单不能作为赢单结束。 |
| 项目规划和跟踪 | 2595841 | 在 Project for the Web 中，用户在创建新资源请求时会收到关于缺少的 **msdyn\_actualstart** 的错误消息。 |
| 时间和支出 | 2602511 | 时间条目的 **拒绝者** 字段显示 **系统** 而不是指定用户为拒绝者。 |
| 时间和支出 | 2602528 | 项目审批者可以批准其未被列为审批者的项目的时间。 |
| 计费和定价 | 2608550 | 即使原始发票没有更改，也可以确认更正发票。 |

## <a name="removed-and-deprecated-features"></a>已删除和弃用的功能

[Project Operations 中已删除或弃用的功能](../../whats-new/removed-depreciated-features-project.md)主题描述了 Dynamics 365 Project Operations 已删除或弃用的功能。

- 已删除的功能在产品中已不再可用。
- 已弃用的功能在活跃的开发中不存在，而且在将来的更新中可能被移除。

在从产品中删除任何功能之前的 12 个月，[Project Operations 中已删除或弃用的功能](../../whats-new/removed-depreciated-features-project.md)主题中会显示弃用公告。
