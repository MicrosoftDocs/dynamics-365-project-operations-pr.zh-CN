---
title: 2022 年 8 月新增功能 - 适用于基于资源/非库存场景的 Project Operations
description: 本文提供有关 2022 年 8 月版基于资源/非库存场景的 Microsoft Dynamics 365 Project Operations 中可用的质量更新的信息。
author: ramagadu
ms.date: 07/19/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: ramagadu
ms.openlocfilehash: 4042dca72a33f48e04e51af2a3cfd2da83146afd
ms.sourcegitcommit: 7ed8e77a92917f2d242988ca02bd7de9571cce5e
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/02/2022
ms.locfileid: "9403845"
---
# <a name="whats-new-august-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>2022 年 8 月新增功能 - 适用于基于资源/非库存场景的 Project Operations

_**适用于：** 面向资源/非库存场景的 Project Operations_

本文适用于以下 Microsoft Dynamics 365 Project Operations 组件和版本：

- Dataverse 环境中的 Project Operations 版本 4.45.0.53
- Dynamics 365 Finance 环境中的项目管理和会计版本 10.0.28

## <a name="project-operations-dual-write-maps-updates"></a>Project Operations 双重写入映射更新

此版本中没有对 Project Operations 双重写入映射的更新。 有关 Project Operations 双重写入映射的当前列表和版本，请参阅 [Project Operations 双重写入映射版本](../environment/resource-dual-write-maps.md)。

当更新 Project Operations Dataverse 解决方案和 Finance 解决方案版本时，始终运行您环境中的最新映射版本并启用所有相关表映射。 如果未激活映射的最新版本，某些特性和功能可能无法正常运行。 您可以在 **双重写入** 页的 **版本** 列中查看映射的活动版本。 要激活映射的新版本，请选择 **表映射版本**，选择最新版本，然后保存所选版本。 如果您已经自定义了现成的表映射，请重新应用更改。 有关详细信息，请参阅[应用程序生命周期管理](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management)。

如果您在启动映射时遇到问题，请按照双重写入故障排除指南的[映射中缺少表列问题](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps)部分中的说明进行操作。

## <a name="quality-updates"></a>质量更新

### <a name="project-operations-on-dataverse"></a>Dataverse 上的 Project Operations

| 功能区域 | 参考编号 | 质量更新 |
| --- | --- | --- |
|   商机管理 | 2762089 | 如果在组织中禁用自动保存，关闭合同时的错误将处理为丢失。|
|项目规划和跟踪 | 2767841 | 遥测更新项目实体创建或更新场景。|
|计费和定价 | 2771072 | 赢得报价单时的 Null 引用异常处理。|
|计费和定价 | 2844181 |获取相关 ID 并阻止创建发票失败。|
|计费和定价 | 2852836 | 在 CE 中创建和批准的内部公司支出缺少内部公司实际值。|


### <a name="project-management-and-accounting-in-finance"></a>Finance 中的项目管理和会计

有关此更新中包含的缺陷修复的信息，请登录 Microsoft Dynamics Lifecycle Services (LCS)，然后查看[知识库文章](https://fix.lcs.dynamics.com/Issue/Details?bugId=694438)。
