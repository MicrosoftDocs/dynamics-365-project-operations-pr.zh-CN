---
title: 2022 年 6 月新增功能 - 基于资源/非库存场景的 Project Operations
description: 本文提供有关 2022 年 6 月版基于资源/非库存场景的 Microsoft Dynamics 365 Project Operations 中可用的质量更新的信息。
author: sigitac
ms.date: 06/03/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: fde1f0be42eecfc5ee809cb9b2191d3aeae57131
ms.sourcegitcommit: 51745acac29dfacba43a4003d86baff4d6ca2fb8
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/14/2022
ms.locfileid: "8959398"
---
# <a name="whats-new-june-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>2022 年 6 月新增功能 - 基于资源/非库存场景的 Project Operations

_**适用于：** 面向资源/非库存场景的 Project Operations_

本文适用于以下 Microsoft Dynamics 365 Project Operations 组件和版本：

- Dataverse 环境中的 Project Operations 版本 4.43.0.77
- Dynamics 365 Finance 环境中的项目管理和会计版本 10.0.27

## <a name="project-operations-dual-write-maps-updates"></a>Project Operations 双重写入映射更新

下表显示了在 Project Operations 2022 年 6 月版中修改或添加的双写入映射。

| 实体映射 | 更新版本 | 注释  |
| --- | --- | --- |
| Project Operations 集成项目供应商发票导出实体 (msdyn_projectvendorinvoices) | 1.0.0.1 | 弃用了旧字段并映射到新字段以进行供应商发票状态跟踪。 |

当更新 Project Operations Dataverse 解决方案和 Finance 解决方案版本时，始终运行您环境中的最新映射版本并启用所有相关表映射。 如果未激活映射的最新版本，某些特性和功能可能无法正常运行。 您可以在 **双重写入** 页的 **版本** 列中查看映射的活动版本。 要激活映射的新版本，请选择 **表映射版本**，选择最新版本，然后保存所选版本。 如果您已经自定义了现成的表映射，请重新应用更改。 有关详细信息，请参阅[应用程序生命周期管理](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management)。

如果您在启动映射时遇到问题，请按照双重写入故障排除指南的[映射中缺少表列问题](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps)部分中的说明进行操作。

## <a name="quality-updates"></a>质量更新

### <a name="project-operations-on-dataverse"></a>Dataverse 上的 Project Operations

| 功能区域 | 参考编号 | 质量更新 |
| --- | --- | --- |
| 转包 | 2708885 | 修复了用户创建可预订资源预订标题记录时，未填写可预订资源时出现的错误信息。 |
| 项目规划和跟踪 | 2629441 | 更正了工作流触发逻辑，以帮助防止更新项目任务时出现无限循环。 |
| 时间和支出 | 2641209 | 从分配/预订导入时间条目必须保留可预订资源引用。 |
| 项目规划和跟踪 | 2651148 | 必须保护项目文档标题。|
| 项目规划和跟踪 | 2653145 | 添加了验证以确保不能创建名称中包含无效字符的项目记录。 |
| 时间和支出 | 2654710 | 更正了 **审批** 页面上的筛选。 |
| 计费和定价 | 2667805 | 添加了验证，以帮助阻止在支持的未记帐实际销售额不存在时创建已记帐实际销售额。 |
| 计费和定价 | 2668378 | 添加了验证，以帮助阻止添加自定义定价维度，除非填写了逻辑名称和字段名称。 |
| 转包 | 2677485 | 更新了供应商发票明细双写入映射的目标版本。 |
| 时间和支出 | 2700428 | 改进了审批逻辑，以确保即使其中一个审批集在系统作业中卡住，也可以处理项目的其他审批集。 |

### <a name="project-management-and-accounting-in-finance"></a>Finance 中的项目管理和会计

有关此更新中包含的缺陷修复的信息，请登录 Microsoft Dynamics Lifecycle Services (LCS)，然后查看[知识库文章](https://fix.lcs.dynamics.com/Issue/Details?bugId=673271)。
