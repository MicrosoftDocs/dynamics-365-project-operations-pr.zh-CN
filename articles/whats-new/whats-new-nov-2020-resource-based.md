---
title: 2020 年 11 月新增功能 - 面向资源/非库存场景的 Project Operations
description: 此主题提供有关 2020 年 11 月版本的面向资源/非库存场景的 Project Operations 中推出的质量更新的信息。
author: sigitac
ms.date: 10/30/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: b76ebbff1cc2720e699334601d425879f2d20770
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/14/2022
ms.locfileid: "8600363"
---
# <a name="whats-new-november-2020---project-operations-for-resourcenon-stocked-based-scenarios"></a>2020 年 11 月新增功能 - 面向资源/非库存场景的 Project Operations

_**适用于：** 面向资源/非库存场景的 Project Operations_

此主题适用于以下 Dynamics 365 Project Operations 组件和版本：

- CDS 环境中的 Project Operations 版本 4.4.0.70
- Dynamics 365 Finance 环境中的项目管理和会计版本 10.0.14

## <a name="updates-to-project-operations-for-resource-non-stocked-based-scenarios"></a>面向资源/非库存场景的 Project Operations 更新

### <a name="project-operations-on-cds"></a>CDS 上的 Project Operations

| 功能区域                 | 参考编号 | 质量更新                                                                                                                                                                    |
|------------------------------|------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|   商机管理       | 2036993          | 当报价单明细类型为 **所有任务** 时，估算明细和资源分配合同子项将在报价单赢单时更新。                                                 |
| 计费和定价          | 2070392          | 发票上的项目合同子项会在每次选择 **刷新发票交易** 时增加。                                                                         |
| 项目规划             | 2043336          | 无法删除项目团队成员记录。                                                                                                                                  |
| 项目规划             | 2046013          | 加载期间和更改时间分段类型时，估算标记列的行为不一致。                                                                                   |
| 项目规划             | 2046647          | 从项目团队成员生成资源要求时，开始时间和结束时间减少一小时。                                                                      |
| 项目规划             | 2053879          | （根据即将到来的 CDS 部署），当出现错误“为 ConditionOperator.In 传递的值为空”时，PublishUnassignedAssignments 会中断保存任务的尝试。                       |
| 项目规划             | 2055501          | 将 **项目开始日期** 保留为空会导致计划失败。                                                                                                      |
| 项目规划             | 2066817          | 无法使用 **任务** 选项卡上的人员选取器创建通用资源。                                                                                                   |
| 项目规划             | 2067034          | **查看详细信息** 按钮在 **任务详细信息** 页上不可用。                                                                                                       |
| 资源管理          | 2046667          | 通用团队成员不会被删除，即使所有资源都已结束工作。                                                                                                    |
| 时间和快速支出条目 | 2047499          | 时间条目页上的 **新建** 按钮打开的是 **新建电子邮件签名** 页。                                                                                               |
| 时间和快速支出条目 | 2059859          | 创建支出条目时，会打开不是预期的弹出窗口。                                                                                                                         |
| 其他                        | 2044181          | （卸载采购订单）在尝试卸载 msdyn_ProjectServiceCore_Patch 和 msdyn Project service 核心解决方案时发生错误“记录不可用”。  |

### <a name="project-management-and-accounting-in-dynamics-365-finance"></a>Dynamics 365 Finance 中的项目管理和会计

| 功能区域        | 参考编号 | 质量更新                                                                                                                                                            |
|---------------------|------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 收入确认 | [451662](https://fix.lcs.dynamics.com/Issue/Details/?bugId=451662)           | 当合同在完成方法中使用外币和工作进度百分比时，项目估计完成百分比错误。                     |
| 收入确认 | [469894](https://fix.lcs.dynamics.com/Issue/Details/?bugId=469894)           | 无法使用 **实际成本** 完成方法过帐估计值。                                                                                                    |
| 收入确认 | [485439](https://fix.lcs.dynamics.com/Issue/Details/?bugId=485439)           | 由于公司货币和交易货币不同时出现的凭证不均衡错误导致取消失败。                                              |
| 支出管理  | [456882](https://fix.lcs.dynamics.com/Issue/Details/?bugId=456822)           | 对于非管理员用户，支出明细列的查找值（如 **项目 ID** 和 **支出类别**）在数据连接器框中不能正确显示。 |
| 支出管理  | [469300](https://fix.lcs.dynamics.com/Issue/Details/?bugId=469300)           | 不能为支出类别显示记录属性默认值。                                                                                                         |
| 支出管理  | [469302](https://fix.lcs.dynamics.com/Issue/Details/?bugId=469302)           | 支出集成必须包含支出报表中的明细属性。                                                                                             |
| 开票           | [462499](https://fix.lcs.dynamics.com/Issue/Details/?bugId=462499)           | 由于出现指示 FD 组合未经验证的错误消息，无法过帐项目发票方案。                                                    |
| 开票           | [470614](https://fix.lcs.dynamics.com/Issue/Details/?bugId=470614)           | 无法从 **发票** 详细信息页查看交易。                                                                                                              |
| 开票           | [480070](https://fix.lcs.dynamics.com/Issue/Details/?bugId=480070)           | 发票方案明细可以删除。                                                                                                                                  |
| 项目核算  | [470293](https://fix.lcs.dynamics.com/Issue/Details/?bugId=470293)           | **预测** 菜单项在 **项目** 列表页上不可见。                                                                                                   |
| 项目核算  | [475873](https://fix.lcs.dynamics.com/Issue/Details/?bugId=475873)           | 无法打开 **项目对帐单**   > **交易和预测**。                                                                                                       |
| 项目核算  | [475879](https://fix.lcs.dynamics.com/Issue/Details/?bugId=475879)           | 未为已开票的项目交易启用 **调整核算**。                                                                                                  |
| 项目核算  | [480962](https://fix.lcs.dynamics.com/Issue/Details/?bugId=480962)           | 过帐 **集成** 日记帐时，**ProjCDSActualsImport** 表中未包括会计详细信息。                                                  |
| 项目核算  | [482558](https://fix.lcs.dynamics.com/Issue/Details/?bugId=482558)           | 当您删除资源分配，然后重新添加时，项目预测条目加倍。                                                                            |
| 项目核算  | [502019](https://fix.lcs.dynamics.com/Issue/Details/?bugId=502019)           | 选择项目 ID 链接不能打开 CDS 深层链接 URL。                                                                                                         |
| 项目核算  | [505458](https://fix.lcs.dynamics.com/Issue/Details/?bugId=505458)           | 无法在 CDS 中更新任务的开始日期。                                                                                                                           |
| 项目核算  | [510041](https://fix.lcs.dynamics.com/Issue/Details/?bugId=510041)           | 启用此功能后，在不进行 CDS 集成时不能使用多个合同子项。                                                                                   |

### <a name="regulatory-updates"></a>法规更新
有关财务和运营应用的监管更新的信息，请参阅[监管更新](/dynamics365/finance/localizations/regulatory-updates)。 您还可以登录到 LCS，使用问题搜索工具查看计划的法规更新。 通过问题搜索，您可以按国家/地区、功能类型和发布进行搜索。


[!INCLUDE[footer-include](../includes/footer-banner.md)]