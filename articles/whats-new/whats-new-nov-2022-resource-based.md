---
title: 2022 年 11 月新增功能 - 适用于基于资源/非库存场景的 Project Operations
description: 本文提供有关 2022 年 11 月版基于资源/非库存场景的 Microsoft Dynamics 365 Project Operations 中可用的质量更新的信息。
author: ryansandness
ms.date: 12/16/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: ryansandness
ms.openlocfilehash: 509e303aeb0567627590fd89c6888b59a414c6f1
ms.sourcegitcommit: 952fcefe33de192ad48f4108c3adbe658fd7b94f
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/08/2022
ms.locfileid: "9831070"
---
# <a name="whats-new-november-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>2022 年 11 月新增功能 - 适用于基于资源/非库存场景的 Project Operations

_**适用于：** 面向资源/非库存场景的 Project Operations_

本文适用于以下 Microsoft Dynamics 365 Project Operations 组件和版本：

- Dataverse 环境中的 Project Operations 版本 4.58.0.119
- Dynamics 365 Finance 环境中的项目管理和会计版本 10.0.30

## <a name="project-operations-dual-write-maps-updates"></a>Project Operations 双重写入映射更新

此版本中没有对 Project Operations 双重写入映射的更新。 有关 Project Operations 双重写入映射的当前列表和版本，请参阅 [Project Operations 双重写入映射版本](../environment/resource-dual-write-maps.md)。

当更新 Project Operations Dataverse 解决方案和 Finance 解决方案版本时，始终运行您环境中的最新映射版本并启用所有相关表映射。 如果未激活映射的最新版本，某些特性和功能可能无法正常运行。 您可以在 **双重写入** 页的 **版本** 列中查看映射的活动版本。 要激活映射的新版本，请选择 **表映射版本**，选择最新版本，然后保存所选版本。 如果您已经自定义了现成的表映射，请重新应用更改。 有关详细信息，请参阅[应用程序生命周期管理](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management)。

如果您在启动映射时遇到问题，请按照双重写入故障排除指南的[映射中缺少表列问题](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps)部分中的说明进行操作。

## <a name="quality-updates"></a>质量更新

### <a name="project-operations-on-dataverse"></a>Dataverse 上的 Project Operations

| 功能区域 | 参考编号 | 质量更新 |
| --- | --- | --- |
| 计费和定价 | 2781818 | 默认材料使用日志的价格时出现找不到密钥错误。 |
| 计费和定价 | 2922373 | 无法将报价单行链接到已作为丢单结束的项目。 |
| 计费和定价 | 2943206 | 项目实体中的 **合同子项** 应是可选的。 |
| 计费和定价 | 2953182 | 改进更正发票的错误消息。|
| 计费和定价 | 2959500 | 无法将报价单明细链接到与丢失的报价单关联的项目任务。|
| 计费和定价 | 2959560 | 在某些区域设置中以赢单结束报价单时收到“该客户已经在项目合同上”消息。 |
| 计费和定价 | 3031727 | 资源分配失败，出现必填字段“msdyn_Company”丢失错误。 |
| 计费和定价 | 3036905 | 从未在 ProjectTeamMember 上初始化负责公司。 |
| 商机管理 | 2763519 | EnsureProjectContractAllowsUpdates 中出现 Null 引用错误。 |
| 商机管理 | 2783798 | 在报价单明细上导入项目估算时，费用和材料估算缺少任务描述。|
| 商机管理 | 2988635 | 改进删除报价单中的客户时出现的错误消息说明。 |
| 商机管理 | 3001191 | 无法从将记帐方法指定为 Null 的商机创建报价单。 |
| 升级 | 3012324 | 名称中包含 Tab 等控制字符的项目的项目转换失败。 || 项目规划和跟踪 | 2790384 | 待定 OperationSet 超时过短。 |
| 项目规划和跟踪 | 3044275 | missingProjectSchedulerErrorMessage 缺少本地化。 |
| 项目规划和跟踪 | 3044277 | 未设置计划程序时不加载项目确认网格。|
| 资源管理 | 2943153 | 用于显示持续时间的两位小数的“更新跟踪”选项卡。|
| 转包 | 2932774 | 只读供应商发票明细会错误地引发错误。 |
| 转包 | 2939556 | 如果未激活，则供应商发票抬头状态不应设置为“草稿联机删除”。 |
| 时间和支出 | 2939998 | 在 ProjOps 中利用新的 TESA 版本。 |


### <a name="project-management-and-accounting-in-finance"></a>Finance 中的项目管理和会计

有关此更新中包含的缺陷修复的信息，请登录 Microsoft Dynamics Lifecycle Services，然后查看[知识库文章](https://fix.lcs.dynamics.com/Issue/Details?bugId=745468)。
