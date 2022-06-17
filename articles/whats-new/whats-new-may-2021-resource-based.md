---
title: 2021 年 5 月新增功能 - 基于资源/非库存场景的 Project Operations
description: 本文提供有关 2021 年 5 月版基于资源/非库存场景的 Project Operations 中可用的质量更新的信息。
author: sigitac
ms.date: 05/11/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 425b0eb78b5f03d4b0da9a792d6e33fc96adf060
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8930399"
---
# <a name="whats-new-may-2021---project-operations-for-resourcenon-stocked-based-scenarios"></a>2021 年 5 月新增功能 - 基于资源/非库存场景的 Project Operations

_**适用于：** 面向资源/非库存场景的 Project Operations_

本文适用于以下 Dynamics 365 Project Operations 组件和版本：

- Dynamics 365 Dataverse 环境中的 Project Operations 版本 4.10.0.186 
- 财务和运营应用环境中的项目管理和会计版本 10.0.18

## <a name="features-included-in-this-release"></a>此版本中包括的功能

此版本包含以下功能：

- [计划模式](../project-management/scheduling-modes.md)：项目经理可以定义是否应使用固定持续时间、固定工作或固定单位调度模式来管理项目。
- [使用里程费率层级设置里程](../expense/set-up-mileage.md)：更新员工支出报表的里程费率层级。

## <a name="project-operations-dual-write-maps-updates"></a>Project Operations 双重写入映射更新

以下列表显示了在 Project Operations 2021 年 5 月发行版本中修改或添加的双重写入映射。

| 实体映射 | 更新版本 | 注释  |
| --- | --- | --- |
| 项目资金来源 (msdyn\_projectcontractsplitbillingrules) | 1.0.0.2 | 同步项目合同客户的付款条款。 |
| 项目发票方案 V2（发票） | 1.0.0.3 | 同步形式发票付款条款。 |
| Project Operations 集成项目供应商发票明细导出实体 (msdyn\_projectvendorinvoicelines) | 1.0.0.1 | 质量更新 |
| 项目 V2 (msdyn\_projects) | 1.0.0.2 | 质量更新 |

当更新 Project Operations Dataverse 解决方案和财务和运营应用解决方案版本时，应始终运行您环境中的最新映射版本并启用所有相关表映射。 如果未激活最新版本的映射，某些功能可能无法正常工作。 您可以在 **双重写入** 页的 **版本** 列中看到映射的活动版本。 要激活映射的新版本，请选择 **表映射版本**，选择最新版本，然后保存所选版本。 如果您自定义了现成的表映射，请重新应用更改。 有关详细信息，请参阅[应用程序生命周期管理](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management)。

如果您在启动映射时遇到问题，请按照双重写入疑难解答指南中[映射上缺少表列的问题](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps)一节中的说明操作。

## <a name="quality-updates"></a>质量更新

### <a name="project-operations-on-dataverse"></a>Dataverse 上的 Project Operations

| **功能区域** | **参考编号** | **质量更新** |
| --- | --- | --- |
| 计费和定价 | 2227635 | **计价单位组** 和 **单位** 字段中的值默认自 **材料估计** 网格中的产品。 |
| 计费和定价 | 2234127 | **任务 ID** 字段现在可以在过帐供应商发票后正确集成到 Dataverse 项目实际值。 |
| 计费和定价 | 2235564 | 保存日记帐行可确保日记帐行条目中显示的货币与保存后的行默认货币相匹配。 |
| 计费和定价 | 2246671 | 在开票期间使交易不收费会反转原始未开票销售记录并创建新的未开票销售记录作为不收费记录。 |
| 计费和定价 | 2264042 | 如果存在在环境中无效的发票更正详细信息，则不得阻止有效的发票更正。 |
| 计费和定价 | 2146367 | 项目发票抬头双重写入映射已扩展以包括付款条件。 |
|   商机管理 | 2086888 | 在将报价单复制到新复制报价单的可收费角色和类别之前，请勿添加已停用的角色和类别。 |
|   商机管理 | 2234376 | 只读字段在 **材料估算** 网格中显示为灰色。 |
|   商机管理 | 2238337 | 即使基于联系人的报价单与项目价目表无关，也可以保存此报价单。 |
|   商机管理 | 2239810 | 关闭丢失的报价单也会关闭关联的项目并取消任何预订。 |
| 项目规划和跟踪 | 2099559 | 在 **项目任务** 网格打开之前添加了对系统运行状况的额外验证。 |
| 项目规划和跟踪 | 2178987 | 修复了在 **项目** 页上选择 **下一个阶段** 时发生的临时错误。 |
| 资源管理 | 2224817 | 用于扩展预订的功能默认为正确的预订状态。 |
| 时间条目 | 2202476 | **时间条目** 页现在使用响应网格控件并修复了网格未对齐等问题。 |
| 时间条目 | 2223377 | **可预订资源** 页上的 **相关** 部分中隐藏了时间条目，以避免与可用性混淆。 |

### <a name="project-management-and-accounting-in-dynamics-365-finance"></a>Dynamics 365 Finance 中的项目管理和会计

| 功能区域 | 参考编号 | 质量更新 |
| --- | --- | --- |
| 项目管理和会计 | [545878](https://fix.lcs.dynamics.com/Issue/Details/?bugId=545878) | 面向基于资源的场景的 Project Operations：由于集成错误，您不能将报价单转换为赢单状态。 |
| 项目管理和会计 | [546604](https://fix.lcs.dynamics.com/Issue/Details/?bugId=546604) | Project Operations：由于检查重叠的合同子项和交易类型，导致您尝试将合同子项与项目 ID 关联时会出现错误。 |
| 项目管理和会计 | [547440](https://fix.lcs.dynamics.com/Issue/Details/?bugId=547440) | **ProjCDSProjectContractEntity** 可以设置不同客户的资金来源发票地址。 |
| 出差和支出 | [480451](https://fix.lcs.dynamics.com/Issue/Details/?bugId=480451) | 可能会发生与里程设置有关的过帐错误。 |
| 出差和支出 | [522084](https://fix.lcs.dynamics.com/Issue/Details/?bugId=522084) | **拆分到个人** 功能对外币支出交易不起作用。 |
| 出差和支出 | [523938](https://fix.lcs.dynamics.com/Issue/Details/?bugId=523938) | 支出类别下拉值显示不正确的代理类别，无论他们是否是资源。 |
| 出差和支出 | [539266](https://fix.lcs.dynamics.com/Issue/Details/?bugId=539266) | 由于 **资源/类别验证** 错误，您无法保存内部公司支出报表。 |
| 出差和支出 | [532610](https://fix.lcs.dynamics.com/Issue/Details/?bugId=532610) | 支出报表过帐中的错误里程费率计算有拆分明细。 |
| 出差和支出 | [537404](https://fix.lcs.dynamics.com/Issue/Details/?bugId=537404) | 当包含销售税且付款方式上的抵销帐户类型为 **工作人员** 时，您不能过帐内部公司支出报表。 |
| 出差和支出 | [542927](https://fix.lcs.dynamics.com/Issue/Details/?bugId=542927) | 回滚 **TTrvRequisitionLine** 数据实体与唯一索引相关联。 |
| 出差和支出 | [543239](https://fix.lcs.dynamics.com/Issue/Details/?bugId=543239) | 支出报表支持源文档行的创建和更新。 |
| 出差和支出 | [544323](https://fix.lcs.dynamics.com/Issue/Details/?bugId=544323) | 如果将销售税款过帐到目标法人，则会在公司内部方案中显示不正确的子分类帐日记帐。 |
| 出差和支出 | [546877](https://fix.lcs.dynamics.com/Issue/Details/?bugId=546877) | Project Operations：从 Dataverse 中删除支出估算后未从 Finance 中删除支出估算。 |
| 出差和支出 | [550575](https://fix.lcs.dynamics.com/Issue/Details/?bugId=550575) | 如果支出类别是非项目类别，则 **支出** 页上选择的财务维度不会复制到支出报表。 |
