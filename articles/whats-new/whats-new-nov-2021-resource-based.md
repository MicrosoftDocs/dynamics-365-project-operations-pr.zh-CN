---
title: 2021 年 11 月新增功能 - 面向资源/非库存场景的 Project Operations
description: 本主题提供有关 2021 年 11 月版 Project Operations 中可用于基于资源/非库存方案的质量更新的信息。
author: sigitac
ms.date: 11/09/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 20f277bc9b6f571c0144eaaa867bb97c0cf30ddb
ms.sourcegitcommit: 04ebe764afa22742b3fbf8f12af31e8eea93682e
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/23/2021
ms.locfileid: "7827314"
---
# <a name="whats-new-november-2021---project-operations-for-resourcenon-stocked-based-scenarios"></a>2021 年 11 月新增功能 - 面向资源/非库存场景的 Project Operations

*适用范围：适用于基于资源/非库存场景的 Project Operations*

本主题适用于以下 Microsoft Dynamics 365 Project Operations 组件和版本：

- Dataverse 环境中的 Project Operations 版本 4.26.0.145、4.26.0.148 或 4.26.0.150
- Dynamics 365 Finance 环境中的项目管理和会计版本 10.0.22

## <a name="features-included-in-this-release"></a>此版本中包括的功能

此版本包含以下功能：

- 项目计划应用编程接口 (API) 现在支持创建和删除项目 Bucket 的功能。

## <a name="project-operations-dual-write-maps-updates"></a>Project Operations 双重写入映射更新

此版本中没有对 Project Operations 双重写入映射的更新。 有关 Project Operations 双重写入映射的当前列表和版本，请参阅 [Project Operations 双重写入映射版本](/dynamics365/project-operations/environment/resource-dual-write-maps)。

当更新 Project Operations Dataverse 解决方案和 Finance 解决方案版本时，始终运行您环境中的最新映射版本并启用所有相关表映射。 如果未激活映射的最新版本，某些特性和功能可能无法正常运行。 您可以在 **双重写入** 页的 **版本** 列中查看映射的活动版本。 要激活映射的新版本，请选择 **表映射版本**，选择最新版本，然后保存所选版本。 如果您已经自定义了现成的表映射，请重新应用更改。 有关详细信息，请参阅[应用程序生命周期管理](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management)。

如果您在启动映射时遇到问题，请按照双重写入故障排除指南的[映射中缺少表列问题](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps)部分中的说明进行操作。

## <a name="quality-updates"></a>质量更新

### <a name="project-operations-in-dataverse"></a>Dataverse 中的 Project Operations

| 功能区域 | 参考编号 | 质量更新 |
| --- | --- | --- |
| 计费和定价 | 2240080 | **付款条款** 字段在估价单上不能重复。 |
| 计费和定价 | 2358236 | 发票更正必须允许进行具有零价格行的更正。 |
| 资源管理 | 2410072 | 允许将分配给任务的资源设置为项目经理。 |
| 计费和定价 | 2430234 | 修复成本绩效计算问题。 |
| 时间和支出 | 2436978 | 允许以 hh:mm 格式输入时间。 |
| 计费和定价 | 2448623 | 允许在价目表与组织单位相关联后更新价目表。 |
| 时间和支出 | 2460396 | 允许通过清除单元格来删除时间条目。 |
| 计费和定价 | 2467386 | 允许删除具有任务的项目，即使该任务与已赢单的报价单相关联也不例外。 |
| 时间和支出 | 2461744 | **我未通过的审批** 视图仅包含处于 **已提交** 阶段的项目审批。 |
| 时间和支出 | 2464082 | 当目标状态匹配时，删除从项目审批到审批集的链接。 |
| 时间和支出 | 2468108 | 计划作业不应为审批集设置 **正在处理** 状态。 |
| 时间和支出 | 2471503 | 删除存在了 7 天的审批集。 |
| 计费和定价 | 2480687 | 创建报价单行里程碑时不能删除报价单行引用。 |

### <a name="project-management-and-accounting-in-finance"></a>Finance 中的项目管理和会计

| 功能区域 | 参考编号 | 质量更新 |
| --- | --- | --- |
| 项目管理和会计 | [584732](https://fix.lcs.dynamics.com/Issue/Details/?bugId=584732) | 项目支出交易中保留的供应商金额未显示在交易列表中。 |
| 项目管理和会计 | [593068](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593068) | 当启用供应商发票集成时，内部公司供应商发票将损坏。 |
| 项目管理和会计 | [593382](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593382) | 项目发票的付款条款无法按预期方式发挥作用。 |
| 项目管理和会计 | [596263](https://fix.lcs.dynamics.com/Issue/Details/?bugId=596263) | 在发布供应商保留后，凭证过帐有不正确的附加行。 |
| 项目管理和会计 | [598758](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598758) | 过帐 Project Operations 集成日记帐时，此操作因缺少未过帐到的帐户的维度而失败。 |
| 项目管理和会计 | [602650](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602650) | 将采购类别分配给项目时，待定供应商发票上的 **项目** 选项卡不可编辑。 |
| 项目管理和会计 | [605121](https://fix.lcs.dynamics.com/Issue/Details/?bugId=605121) | 如果您未登录到 Project Operations Dataverse，则缺少导航窗格。 |
| 项目管理和会计 | [602728](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602728) | 当您在已应用保留款案例中过帐项目发票中的收入时，会出现问题，因为凭证上的交易不平衡。 |
| 项目管理和会计 | [603624](https://fix.lcs.dynamics.com/Issue/Details/?bugId=603624) | 过帐发票建议后创建估算会阻止导入更正行。 |
| 项目管理和会计 | [606083](https://fix.lcs.dynamics.com/Issue/Details/?bugId=606083) | 应该不能修改已完全开票的里程碑记录。 |
| 出差和支出 | [575305](https://fix.lcs.dynamics.com/Issue/Details/?bugId=575305) | 当您在支出移动应用中搜索类别时，所有支出报表都可见。 |
| 出差和支出 | [583101](https://fix.lcs.dynamics.com/Issue/Details/?bugId=583101) | 从信用卡交易创建的支出中过帐的供应商交易和销售税交易金额不正确。 |
| 出差和支出 | [583760](https://fix.lcs.dynamics.com/Issue/Details/?bugId=583760) | 刷新 **支出报表** 页时，会出现无关的警告。 |
| 出差和支出 | [598656](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598656) | 在删除临时审批者，然后通过工作流重新提交支出报表时，使用了错误的临时审批者。 |
| 出差和支出 | [612742](https://fix.lcs.dynamics.com/Issue/Details/?bugId=612742) | 发生与里程设置相关的过帐错误。 |
