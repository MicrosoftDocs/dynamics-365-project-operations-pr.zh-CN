---
title: 2021 年 6 月新增功能 - 适用于基于资源/非库存场景的 Project Operations
description: 本文提供有关 2021 年 6 月版基于资源/非库存场景的 Project Operations 中可用的质量更新的信息。
author: sigitac
ms.date: 06/14/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 5bc8475554c4348fa1e88b9090450bd3bfaa924e
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8910573"
---
# <a name="whats-new-june-2021---project-operations-for-resourcenon-stocked-based-scenarios"></a>2021 年 6 月新增功能 - 适用于基于资源/非库存场景的 Project Operations

_**适用于：** 面向资源/非库存场景的 Project Operations_

本文适用于以下 Dynamics 365 Project Operations 组件和版本：

- Dynamics 365 Dataverse 环境上的 Project Operations 版本 4.11.0.156 或 4.11.0.164。
- 财务和运营应用环境中的项目管理和会计版本 10.0.19。

## <a name="features-included-in-this-release"></a>此版本中包括的功能

此版本包含以下功能：

- 能够删除[用于调整场景的项目发票方案行](../invoicing/correct-project-invoice-proposals.md)。
- 细化支出行反映支出报表[支出报表重新打造新功能](../expense/expense-reports-reimagined.md#new-features)中的子类别名称。
- 在创建新支出时，付款方式在新支出窗格中可用。
- 项目日程安排 API 的正式发布。 此新功能允许客户以编程方式对项目任务、资源分配、任务依赖项和项目团队成员记录执行创建、更新和删除操作。 有关详细信息，请参阅[使用项目日程安排 API 执行操作和计划实体](../project-management/schedule-api-preview.md)。

## <a name="project-operations-dual-write-maps-updates"></a>Project Operations 双重写入映射更新

此版本中没有对 Project Operations 双重写入映射的更新。 

有关 Project Operations 双重写入映射的当前列表和版本，请参阅 [Project Operations 双重写入映射版本](../environment/resource-dual-write-maps.md)。

当更新 Project Operations Dataverse 解决方案和财务和运营应用解决方案版本时，应始终运行您环境中的最新映射版本并启用所有相关表映射。 如果未激活最新版本的映射，某些功能可能无法正常工作。 您可以在 **版本** 列中的 **双重写入** 页面上查看映射的活动版本。 通过选择 **表映射版本**，选择最新版本，然后保存选定版本，激活映射的新版本。 如果您自定义了现成的表映射，请重新应用更改。 有关详细信息，请参阅[应用程序生命周期管理](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management)。

如果在启动映射时遇到问题，请按照双重写入故障排除指南的[映射上缺少表列问题](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps)部分中的说明操作。

## <a name="quality-updates"></a>质量更新

### <a name="project-operations-on-dataverse"></a>Dataverse 上的 Project Operations

| **功能区域** | **参考编号** | **质量更新** |
| --- | --- | --- |
| 计费和定价 | 2281417 | 修复了与通过发票计划自动发票创建操作失败有关的问题。 |
| 计费和定价 | 2287835 | 改进了发票确认性能。 |
| 商机管理 | 2222555 | 在使用 **从项目估计导入** 时，材料估计应计费必须正确复制到报价单明细详细信息。 |
| 商机管理 | 2223427 | 现在，自定义允许用于操作 **GenerateRetainersFromRetainerScheduleOptions**。 |
| 商机管理 | 2277528 | 修复了具有多个客户的项目合同子项的记帐里程碑值计算。 |
| 项目规划和跟踪 | 2226110 | 修复了 **项目团队** 网格中 **生成要求** 函数的间歇性问题。 |
| 项目规划和跟踪 | 2208109 | 用户无法使用一种货币创建项目，而使用另一种货币创建相关任务。 |
| 项目规划和跟踪 | 2258228 | 允许使用计划 API 修改 **计划** 实体的字段列表已更新。 |
| 项目规划和跟踪 | 2293989 | 必须将正确的语言和区域设置传递到 **项目任务** 网格。 |
| 资源管理 | 2220493 | 修复了在将资源请求快速标记为完成时 **任务** 网格中的用户体验。 |
| 资源管理 | 2330496 | 修复了 **日程安排板** 加载问题。 （质量更新在版本 4.11.0.164 中提供） |
| 时间和支出 | 2194431 | **时间条目** 网格必须遵守在 **系统设置** 中设置的一周的开始。 |
| 时间和支出 | 2277311 | 在删除 **时间条目** 网格的单元格中的值后，光标将保留在网格中。 |

### <a name="project-management-and-accounting-on-dynamics-365-finance"></a>Dynamics 365 Finance 中的项目管理和会计

| 功能区域 | 参考编号 | 质量更新 |
| --- | --- | --- |
| 项目管理和会计 | [552976](https://fix.lcs.dynamics.com/Issue/Details/?bugId=552976) | **窗体注释** 和 **窗体设置** 在与 Project Operations 集成的 Finance 法人中的 **项目管理设置** 下不可见。 |
| 项目管理和会计 | [527970](https://fix.lcs.dynamics.com/Issue/Details/?bugId=527970) | 当项目发票凭证的 **过帐类型** = **销售税** 时，增值税的默认说明为空。 |
| 项目管理和会计 | [565089](https://fix.lcs.dynamics.com/Issue/Details/?bugId=565089) | 当在具有 Project Operations 集成的 Dataverse 中使用基于任务的记帐时，将过帐双重交易。 |
| 项目管理和会计 | [566869](https://fix.lcs.dynamics.com/Issue/Details/?bugId=566869) | 在使用 Project Operations 集成时，收入识别中的完成百分比不正确。 |
| 项目管理和会计 | [568107](https://fix.lcs.dynamics.com/Issue/Details/?bugId=568107) | 在 Project Operations 集成方案中，待定供应商发票上的收入应计是双倍的。 |
| 项目管理和会计 | [572370](https://fix.lcs.dynamics.com/Issue/Details/?bugId=572370) | 当收入配置文件规则设置为 **组** 设置时，无法过帐集成日记帐。 |
| 项目管理和会计 | [573596](https://fix.lcs.dynamics.com/Issue/Details/?bugId=573596) | 对于包含具有多个度量单位的行的项目采购订单，无法过帐采购发票。 |
| 项目管理和会计 | [573637](https://fix.lcs.dynamics.com/Issue/Details/?bugId=573637) | 无法使用项目 **V2** 数据实体更新项目上的默认财务维度。 |
| 项目管理和会计 | [577211](https://fix.lcs.dynamics.com/Issue/Details/?bugId=577211) | 创建项目估计的批处理流程的完成时间过长。 |
| 项目管理和会计 | [582329](https://fix.lcs.dynamics.com/Issue/Details/?bugId=582329) | 删除合同也会删除与客户关联的地址。 |
| 出差和支出 | [514930](https://fix.lcs.dynamics.com/Issue/Details/?bugId=514930) | 未正确评估支出报表审批工作流条件。 |
| 出差和支出 | [519304](https://fix.lcs.dynamics.com/Issue/Details/?bugId=519304) | 支出报表策略未正确评估项目 ID。 |
| 出差和支出 | [522463](https://fix.lcs.dynamics.com/Issue/Details/?bugId=522463) | **针对内部公司支出交易拆分为个人** 操作无法正确工作。 |
| 出差和支出 | [534702](https://fix.lcs.dynamics.com/Issue/Details/?bugId=534702) | 当删除某些出差申请时，会意外删除支出报表行理由。 当支出报表和出差申请的 recID 相同时，会发生此情况。 |
| 出差和支出 | [544368](https://fix.lcs.dynamics.com/Issue/Details/?bugId=544368) | 当支出报表策略中需要 **项目 ID** 字段时，支出移动应用中存在问题。 |
| 出差和支出 | [545331](https://fix.lcs.dynamics.com/Issue/Details/?bugId=545331) | 无法编辑与项目关联的内部公司支出。 相反，将显示以下错误消息“对象引用未设置为对象的实例。” |
| 出差和支出 | [548659](https://fix.lcs.dynamics.com/Issue/Details/?bugId=548659) | 在过帐支出报表后，错误的货币和金额将在银行分类帐中列出。 |
| 出差和支出 | [558336](https://fix.lcs.dynamics.com/Issue/Details/?bugId=558336) | 已对 *删除信用卡交易* 功能进行了改进。  |
| 出差和支出 | [525070](https://fix.lcs.dynamics.com/Issue/Details/?bugId=525070) | 当在法人中指定不同的报告货币时，支出报表中包括的销售税的计算不一致。 |
| 出差和支出 | [527779](https://fix.lcs.dynamics.com/Issue/Details/?bugId=527779) | 当添加新现金出差支出时，性能会受到影响。 |
| 出差和支出 | [537841](https://fix.lcs.dynamics.com/Issue/Details/?bugId=537841) | 未在支出报表上触发支出策略规则。 |
| 出差和支出 | [566386](https://fix.lcs.dynamics.com/Issue/Details/?bugId=566386) | 使用数据管理框架上传新的共享类别会删除所有共享类别的所有子类别。 |
| 出差和支出 | [574131](https://fix.lcs.dynamics.com/Issue/Details/?bugId=574131) | 当您创建支出行并选择类别时，将显示以下错误消息“销售税组 DOM 和物料销售税组 STD 的组合无效。” |
| 出差和支出 | [574900](https://fix.lcs.dynamics.com/Issue/Details/?bugId=574900) | 支出移动应用程序中存在同步问题。 |
