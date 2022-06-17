---
title: 2021 年 4 月新增功能 - 基于资源/非库存场景的 Project Operations
description: 本文提供有关 2021 年 4 月版基于资源/非库存场景的 Project Operations 中可用的质量更新的信息。
author: sigitac
ms.date: 04/22/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: a060bdc4e4c9f37ec666b1cf4d078986ad1571db
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8912413"
---
# <a name="whats-new-april-2021---project-operations-for-resourcenon-stocked-based-scenarios"></a>2021 年 4 月新增功能 - 基于资源/非库存场景的 Project Operations

_**适用于：** 面向资源/非库存场景的 Project Operations_

本文适用于以下 Dynamics 365 Project Operations 组件和版本：

- Dataverse 环境中的 Project Operations 版本 4.9.0.221
- Dynamics 365 Finance 环境中的项目管理和会计版本 10.0.17

## <a name="features-included-in-this-release"></a>此版本中包括的功能

此版本包含以下功能：

- 项目的非库存材料。 关键功能包括：
  - 在项目的销售周期中对非库存材料进行估算和定价。 有关详细信息，请参阅[设置目录产品的成本和销售费率 - 精简](../pro/pricing-costing/set-up-cost-sales-rates-catalog-products.md)。
  - 在项目交付期间跟踪非库存材料的使用情况。 有关详细信息，请参阅[记录项目和项目任务的材料使用情况](../material/material-usage-log.md)。
  - 开票功能使用了非库存材料成本。 有关详细信息，请参阅[管理记帐积压](../proforma-invoicing/manage-billing-backlog.md)。
  - 有关如何配置此功能的信息，请参阅[配置非库存材料以及待定供应商发票](../procurement/configure-materials-nonstocked.md)
- 基于任务的记帐：添加了将项目任务与项目合同子项关联的功能，从使它们的记帐方法、发票频率和客户与合同子项上的这些内容相同。 此关联可确保根据项目任务的此设置进行准确的开票、会计、收入评估和识别。
- Dynamics 365 Dataverse 中的新 API 允许对 **计划实体** 执行创建、更新和删除操作。 有关详细信息，请参阅[使用计划 API 对计划实体执行操作](../project-management/schedule-api-preview.md)。

## <a name="project-operations-dual-write-maps-updates"></a>Project Operations 双重写入映射更新

以下列表显示了在 Project Operations 2021 年 4 月发行版本中修改或添加的双重写入映射。

| **实体映射** | **更新版本** | **注释** |
| --- | --- | --- |
| Project Operations 集成实际值 (msdyn\_actuals) | 1.0.0.14 | 修改了映射以同步材料项目实际值。 |
| 用于支出估算的 Project Operations 集成实体 (msdyn\_estimateslines) | 1.0.0.2 | 向财务和运营应用添加了项目合同子项同步，以提供基于任务的记帐支持。 |
| 用于工时估算的 Project Operations 集成实体 (msdyn\_resourceassignments) | 1.0.0.5 | 向财务和运营应用添加了项目合同子项同步，以提供基于任务的记帐支持。 |
| 用于材料估算的 Project Operations 集成表 (msdyn\_estimatelines) | 1.0.0.0 | 新表映射可将材料估算从 Dataverse 同步到财务和运营应用。 |
| Project Operations 集成项目供应商发票导出实体 (msdyn\_projectvendorinvoices) | 1.0.0.0 | 新表映射可将供应商发票标题从财务和运营应用同步到 Dataverse。 |
| Project Operations 集成项目供应商发票明细导出实体 (msdyn\_projectvendorinvoicelines) | 1.0.0.0 | 新表映射可将供应商发票明细从财务和运营应用同步到 Dataverse。 |

当更新 Project Operations Dataverse 解决方案和 Finance and Operations 解决方案版本时，您应该始终运行您环境中的最新映射版本并启用所有相关表映射。 如果未激活最新版本的映射，某些功能可能无法正常工作。 您可以在 **双重写入** 页的 **版本** 列中看到映射的活动版本。 您可以通过选择 **表映射版本**，选择最新版本，然后保存所选版本来激活映射的新版本。 如果您自定义了现成的表映射，请重新应用更改。 有关详细信息，请参阅[应用程序生命周期管理](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management)。

如果您在启动映射时遇到问题，请按照双重写入疑难解答指南中[映射上缺少表列的问题](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps)一节中的说明操作。

## <a name="quality-updates"></a>质量更新

### <a name="project-operations-in-dynamics-365-dataverse"></a>Dynamics 365 Dataverse 中的 Project Operations

| **功能区域** | **参考编号** | **质量更新** |
| --- | --- | --- |
| 计费和定价 | 2124532 | 当原始发票上有保留款金额或核销的保留款金额时，估价发票上会显示 **更正发票** 按钮。 该按钮只对运行 Finance 版本 10.0.19 或更高版本的环境显示。 |
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

### <a name="project-management-and-accounting-in-dynamics-365-finance"></a>Dynamics 365 Finance 中的项目管理和会计

| **功能区域** | **参考编号** | **质量更新** |
| --- | --- | --- |
| 项目管理和会计 | [491941](https://fix.lcs.dynamics.com/Issue/Details/?bugId=491941) | 冲销估算消除在 **定期** 部分不起作用。  |
| 项目管理和会计 | [509773](https://fix.lcs.dynamics.com/Issue/Details/?bugId=509773) | **会计调整** 功能会使选择了 **不允许手动输入** 的分类帐科目产生问题。 |
| 项目管理和会计 | [510728](https://fix.lcs.dynamics.com/Issue/Details/?bugId=5109728) | 添加了业务逻辑，以处理更正发票，包括保留款金额或核销的保留者金额。 |
| 项目管理和会计 | [514364](https://fix.lcs.dynamics.com/Issue/Details/?bugId=514364) | 内部公司项目开票中的 WIP 销售值过帐选择了意外帐户。 |
| 项目管理和会计 | [521807](https://fix.lcs.dynamics.com/Issue/Details/?bugId=521807) | 在 Project Operations 中处理保留款时，如果在为预付款开具发票后更改合同的默认项目，则会导致入账扣缴问题。 |
| 项目管理和会计 | [527319](https://fix.lcs.dynamics.com/Issue/Details/?bugId=527319) | 在 Project Operations 中，如果需要，从合同中删除项目应该会重置合同的默认项目。 |
| 项目管理和会计 | [528212](https://fix.lcs.dynamics.com/Issue/Details/?bugId=528212) | 在 Project Operations 中，错误的支出明细会显示在公司内部发票上的 **添加明细** 列表中。 |
| 项目管理和会计 | [543968](https://fix.lcs.dynamics.com/Issue/Details/?bugId=543968) | 在 Project Operations 中，**购买协议** 页在与 Project Operations 集成的财务法律实体中不可见。 |
| 项目管理和会计 | [545878](https://fix.lcs.dynamics.com/Issue/Details/?bugId=545878) | 由于 Dataverse 集成错误，因此无法在 Project Operations 中将报价单转换为赢单状态。 |
| 项目管理和会计 | [547440](https://fix.lcs.dynamics.com/Issue/Details/?bugId=547440) | **ProjCDSProjectContractEntity** 可以设置不同客户的资金来源发票地址。  |
| 项目管理和会计 | [557376](https://fix.lcs.dynamics.com/Issue/Details/?bugId=557376) | 在 Project Operations 中，当您为交易创建过帐发票时，未选择任何维度。 |
| 旅行和支出 | [441256](https://fix.lcs.dynamics.com/Issue/Details/?bugId=441256) | 如果已逐行批准并过帐支出报表，则不会更新为支出报表更新预付现金余额。 |
| 出差和支出 | [482041](https://fix.lcs.dynamics.com/Issue/Details/?bugId=482041) | 分项公司间支出报表的税金计算不正确。 |
| 出差和支出 | [483469](https://fix.lcs.dynamics.com/Issue/Details/?bugId=483469) | 与项目相关的其他字段将显示在重新打造的 **公司间支出报表** 页上。 |
| 出差和支出 | [486592](https://fix.lcs.dynamics.com/Issue/Details/?bugId=486592) | 支出报表的标题回执上出现不正确的错误消息。 |
| 出差和支出 | [487971](https://fix.lcs.dynamics.com/Issue/Details/?bugId=487971) | 如果将销售税款过帐到目标法人，则会在公司内部方案中错误地过帐支出报表。 |
| 出差和支出 | [505696](https://fix.lcs.dynamics.com/Issue/Details/?bugId=505696) | 不会在审批支出报表上打印报表提交日期。 |
| 出差和支出 | [508726](https://fix.lcs.dynamics.com/Issue/Details/?bugId=508726) | 不会在审批支出后填充 **批准日期** 和 **拒绝日期** 字段。 |
| 出差和支出 | [509913](https://fix.lcs.dynamics.com/Issue/Details/?bugId=509913) | 为一个员工创建的出差申请可用于另一个员工的支出报表。 |
| 出差和支出 | [518186](https://fix.lcs.dynamics.com/Issue/Details/?bugId=518186) | 在添加新支出明细时，将锁定支出类别。 |
| 出差和支出 | [520914](https://fix.lcs.dynamics.com/Issue/Details/?bugId=520914) | 逐项列出已经拆分的支出报表行将导致应付帐款\总帐凭证过帐不完整，并且会中断会计源资源管理器，因为 **TRVEXPTRANS.SOURCEDOCUMENTLINE** 重复。 |
| 出差和支出 | [521943](https://fix.lcs.dynamics.com/Issue/Details/?bugId=521943) | 出差申请策略无法正常使用。 |
| 出差和支出 | [522567](https://fix.lcs.dynamics.com/Issue/Details/?bugId=522567) | 供应商客户名称不会显示在支出报表的已过帐项目交易上。 |
| 出差和支出 | [525106](https://fix.lcs.dynamics.com/Issue/Details/?bugId=525106) | 在 Project Operations 中，无法批准内部公司项目的任务时间。 |
| 出差和支出 | [526336](https://fix.lcs.dynamics.com/Issue/Details/?bugId=526336) | 过帐后，预付现金退回类别未更新预付现金余额。 |
| 出差和支出 | [527218](https://fix.lcs.dynamics.com/Issue/Details/?bugId=527218) | 在使用导入的信用卡交易以外币创建并且与项目相关联的支出报表中，销售价格计算不正确。 |
| 出差和支出 | [542927](https://fix.lcs.dynamics.com/Issue/Details/?bugId=542927) | 回滚了 **TTrvRequisitionLine** 数据实体及相关的唯一索引。 |
| 出差和支出 | [543239](https://fix.lcs.dynamics.com/Issue/Details/?bugId=543239) | 向 **SOURCEDOCUMENTLINE** 生成中添加了检测。 |
| 出差和支出 | [544323](https://fix.lcs.dynamics.com/Issue/Details/?bugId=544323) | 如果将销售税款过帐到目标法人，则会在公司内部方案中显示错误的子分类帐日记帐。 |
| 出差和支出 | [546877](https://fix.lcs.dynamics.com/Issue/Details/?bugId=546877) | 在 Project Operations 中，从 Dataverse 中删除支出估算后未从 Finance 中删除支出估算。 |
| 出差和支出 | [550575](https://fix.lcs.dynamics.com/Issue/Details/?bugId=550575) | 如果支出类别是非项目类别，则 **支出** 页上选择的财务维度不会复制到支出报表。 |
