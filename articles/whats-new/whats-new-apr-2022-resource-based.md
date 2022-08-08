---
title: 2022 年 4 月新增功能 - 基于资源/非库存场景的 Project Operations
description: 本文提供有关 2022 年 4 月版基于资源/非库存场景的 Microsoft Dynamics 365 Project Operations 中可用的质量更新的信息。
author: sigitac
ms.date: 04/08/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 999006b2c2fe2b31d6e47910a3f1a55cab415f0e
ms.sourcegitcommit: 5c971b15295046b3c92ff6638dd1352129f1c390
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 07/01/2022
ms.locfileid: "9110873"
---
# <a name="whats-new-april-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>2022 年 4 月新增功能 - 基于资源/非库存场景的 Project Operations

_**适用于：** 面向资源/非库存场景的 Project Operations_

本文适用于以下 Microsoft Dynamics 365 Project Operations 组件和版本：

- Dataverse 环境中的 Project Operations 版本 4.41.0.45
- Dynamics 365 Finance 环境中的项目管理和会计版本 10.0.26

## <a name="features-included-in-this-release"></a>此版本中包括的功能

采购类别可用于项目采购订单和待定供应商发票。 有关详细信息，请参阅[将采购类别用于项目采购订单和待定供应商发票](../procurement/configure-procurement-categories.md)。

## <a name="project-operations-dual-write-maps-updates"></a>Project Operations 双重写入映射更新

下表显示了在 2022 年 3 月版 Project Operations 中修改或添加的双写入映射。

| 实体映射 | 更新版本 | 注释  |
| -------------- | ------------------- | ------------|
| Project Operations 集成项目供应商发票明细导出实体 msdyn\_projectvendorinvoicelines | 1.0.0.4 | 此映射支持将采购类别用于采购订单和待定供应商发票。 |

当更新 Project Operations Dataverse 解决方案和 Finance 解决方案版本时，始终运行您环境中的最新映射版本并启用所有相关表映射。 如果未激活映射的最新版本，某些特性和功能可能无法正常运行。 您可以在 **双重写入** 页的 **版本** 列中查看映射的活动版本。 要激活映射的新版本，请选择 **表映射版本**，选择最新版本，然后保存所选版本。 如果您已经自定义了现成的表映射，请重新应用更改。 有关详细信息，请参阅[应用程序生命周期管理](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management)。

如果您在启动映射时遇到问题，请按照双重写入故障排除指南的[映射中缺少表列问题](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps)部分中的说明进行操作。

## <a name="quality-updates"></a>质量更新

### <a name="project-operations-on-dataverse"></a>Dataverse 上的 Project Operations

| 功能区域 | 参考编号 | 质量更新 |
| ------------ | ---------------- | -------------- |
| 时间和支出 | 2573900 | **新式审批** 功能必须默认启用。 |
| 计费和定价 | 2603313 | 修复了阻止添加包含产品的报价单和合同子项的重复记录错误。 |
| 部署和配置 | 2611368 | 客户必须能够使用现代应用程序设计器向解决方案最多添加五个自定义实体。 |
| 时间和支出 | 2628285 | 修复了在时间条目导入期间影响设置正确资源类别的能力的问题。 |
|   商机管理| 2628815 | 更新了报价单明细详细信息说明的字数限制以匹配任务主题的字符限制，以使主题超过 100 个字符的任务能够成功导入。 |
| 时间和支出| 2629547 | 项目审批的 **提交者** 字段必须指向提交记录的用户。 |
| 时间和支出| 2629865 | 复制项目时任务的 **复制类别** 字段。 |
| 时间和支出| 2636463 | 修复了新式审批窗体中的审批筛选器。 |
| 项目规划和跟踪 | 2648300 | 修复了阻止更改项目负责人的问题。 |
| 计费和定价 | 2563000 | 不能允许有货币与合同货币不同的未记帐销售额的日记帐行。 |

### <a name="project-management-and-accounting-in-dynamics-365-finance"></a>Dynamics 365 Finance 中的项目管理和会计

有关此更新中包含的缺陷修复的信息，请登录 Microsoft Dynamics Lifecycle Services (LCS)，然后查看[知识库文章](https://fix.lcs.dynamics.com/Issue/Details?bugId=662864)。
