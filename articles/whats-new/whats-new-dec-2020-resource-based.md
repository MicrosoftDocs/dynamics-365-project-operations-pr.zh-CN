---
title: 2020 年 12 月新增功能 - 面向资源/非库存场景的 Project Operations
description: 此主题提供有关 2020 年 12 月版本的面向资源/非库存场景的 Project Operations 中推出的质量更新的信息。
author: sigitac
manager: tfehr
ms.date: 12/04/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 3889402ab991e307bc3fe5463098dfab383a53b4
ms.sourcegitcommit: 04c446746aad97fc3f4c3d441983c586b918a3a6
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/11/2020
ms.locfileid: "4727869"
---
# <a name="whats-new-december-2020---project-operations-for-resourcenon-stocked-based-scenarios"></a>2020 年 12 月新增功能 - 面向资源/非库存场景的 Project Operations

_**适用于：** 面向资源/非库存场景的 Project Operations_

此主题适用于以下 Dynamics 365 Project Operations 组件和版本：

- Dataverse 环境中的 Project Operations 版本 4.5.0.134
- Dynamics 365 Finance 环境中的项目管理和会计版本 10.0.15

有关如何更新到此版本的信息，请参阅[在 Finance 环境中更新 Project Operations](ur5-nonstocked-installation.md)。

## <a name="features-included-in-this-release"></a>此版本中包括的功能
此版本包含以下功能：

  - [内部公司开票](../project-accounting/intercompany-invoicing-overview.md) 
  - [客户预付款和保留款](../pro/sales/set-up-advances-retainer-based-contracts-sales.md)

## <a name="updates-to-project-operations-for-resource-non-stocked-based-scenarios"></a>面向资源/非库存场景的 Project Operations 更新

### <a name="project-operations-on-dataverse"></a>Dataverse 上的 Project Operations

| 功能区域                    | 参考编号 | 质量更新                                                                                                                                               |
|---------------------------------|------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 计费和定价             | 1986009          | 在将项目链接到合同子项或从合同子项取消链接之前，手动创建的日记帐行经确认后性能不一致                     |
| 计费和定价             | 2028174          | 对账单明细详细信息所做的更新应会遵循日记帐更正逻辑                                                                                  |
| 计费和定价             | 2028315          | 可编辑嵌套网格行为修复                                                                                                                        |
| 计费和定价             | 2031070          | 调整纠正的发票明细详细信息必须遵循日记帐更正逻辑                                                                              |
| 计费和定价             | 2034186          | 必须能够更新合同子项上的项目                                                                                                        |
| 计费和定价             | 2034206          | 从合同子项中取消链接项目过程中，必须在实际冲销期间设置调整状态                                                        |
| 计费和定价             | 2040871          | “支出估算”网格上可进行“允许使用计价单位”和“计价单位组”单元格更新                                                                                       |
| 计费和定价             | 2053754          | 通过账单编辑创建的实际值不会标有调整状态和记帐状态                                                                |
| 计费和定价             | 2057874          | 在发票明细详细信息编辑过程中创建了正确的交易连接                                                                                     |
| 计费和定价             | 2057875          | 在发票明细详细信息编辑过程中创建了正确的交易起源                                                                                        |
| 计费和定价           | 2057944          | 对于因账单更正而未准备开票的实际值，“不超出”状态被设置为“已提交”                                             |
| 计费和定价           | 2066169          | 在使用双重写入集成时更新负的未记帐销售额记录的会计日期                                                            |
| 计费和定价           | 2067622          | 在生成里程碑时应显示处理图标                                                                                                |
| 计费和定价           | 2067624          | 生成里程碑时，应将合同金额标记为“业务建议的”                                                                      |
| 计费和定价           | 2086880          | 对于基于项目的报价单明细，在功能区上隐藏 **建议** 按钮                                                                                                |
| 计费和定价           | 2098140          | 针对集成环境显示 **更正账单** 按钮                                                                                             |
| 部署和配置  | 2101152          | 对于使用 Power Platform 管理中心中的 Project Operations 模板创建的新环境，必须执行所有安装后操作               |
| 商机管理        | 2086601          | 不应将已停用的角色和类别复制到报价单明细和合同子项上的“应计费角色和应计费类别”列表中 |
| 项目规划和跟踪 | 1949065          | 按 200% 缩放时数据可见性能够正常工作                                                                                                                   |
| 项目规划和跟踪 | 2046317          | 可以在 Project Operations 中重命名项目实体                                                                                   |
| 项目规划和跟踪 | 2057171          | 更新了 **项目** 页上的 **项目开始日期** 字段为空时的错误消息                                                           |
| 项目规划和跟踪 | 2057197          | 不支持随任务引用一起复制估算行                                                                                                     |
| 项目规划和跟踪 | 2060687          | 现在，时区警告在特定持续时间之后会消失                                                                                                      |
| 资源管理           | 1832887          | 默认资源类别 ID 必须为静态，才能确保为 Dataverse 和 Finance 环境加载可重复使用的数据                                                 |
| 时间和支出              | 2081793          | **支出类别名称** 必须映射到 Finance and Operations 应用中的 **支出类别描述** 字段                                                  |
| 时间和支出              | 2034882          | 安装了 Dynamics 365 Field Service 后，会针对时间条目在命令栏上显示两次 **新建** 按钮                                          |
| 时间和支出              | 2056028          | 更新 **编辑时间** 页以包含时间行                                                                                                              |
| 时间和支出              | 1983747          | 时间条目图表显示其他数据                                                                                                                   |

### <a name="project-management-and-accounting-in-dynamics-365-finance"></a>Dynamics 365 Finance 中的项目管理和会计

| 功能区域                        | 参考编号 | 质量更新                                                                                                                                                                                                                                                   |
|-------------------------------------|------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 项目管理和会计 | [441680](https://fix.lcs.dynamics.com/Issue/Details/?bugId=441680)           | 为物料需求退回而阻止了调整                                                                                                                                                                                                        |
| 项目管理和会计 | [446498](https://fix.lcs.dynamics.com/Issue/Details/?bugId=446498)           | 窗体注释未出现在已设置格式的项目账单中                                                                                                                                                                                                          |
| 项目管理和会计 | [453407](https://fix.lcs.dynamics.com/Issue/Details/?bugId=453407)           | 不允许用墨西哥项目账单 CFDI 33 更新账单方案中的付款方式                                                                                                                                                           |
| 项目管理和会计 | [458149](https://fix.lcs.dynamics.com/Issue/Details/?bugId=458149)           | 未在 **集成** 日记帐中考虑自动将会计日期设置为未结期间的参数                                                                                                                                                             |
| 项目管理和会计 | [470293](https://fix.lcs.dynamics.com/Issue/Details/?bugId=470293)           | 预测菜单项在 **项目** 列表页上不可见                                                                                                                                                                                                      |
| 项目管理和会计 | [475873](https://fix.lcs.dynamics.com/Issue/Details/?bugId=475873)           | 无法打开 **项目对帐单** > **交易和预测**                                                                                                                                                                                                      |
| 项目管理和会计 | [482558](https://fix.lcs.dynamics.com/Issue/Details/?bugId=482558)           | 删除和读取资源分配会将 Finance 中的项目预测条目加倍                                                                                                                                                                   |
| 项目管理和会计 | [484468](https://fix.lcs.dynamics.com/Issue/Details/?bugId=484468)           | 如果项目上没有合同子项，则无法在 Dataverse 中创建项目估算                                                                                                                                                                 |
| 项目管理和会计 | [485439](https://fix.lcs.dynamics.com/Issue/Details/?bugId=485439)           | 由于公司货币和交易货币不同时出现的凭证不均衡错误导致取消失败                                                                                                                                            |
| 项目管理和会计 | [488382](https://fix.lcs.dynamics.com/Issue/Details/?bugId=488382)           | 固定价格项目的已过帐项目交易中的账单状态筛选器不起作用                                                                                                                                                            |
| 项目管理和会计 | [505458](https://fix.lcs.dynamics.com/Issue/Details/?bugId=505458)           | 无法在 Dataverse 中更新任务的开始日期                                                                                                                                                                                                                    |
| 项目管理和会计 | [507172](https://fix.lcs.dynamics.com/Issue/Details/?bugId=507172)           | 能够删除 Project Operations 集成方案中的账单方案明细                                                                                                                                                                                    |
| 项目管理和会计 | [509989](https://fix.lcs.dynamics.com/Issue/Details/?bugId=509989)           | 能够删除 Project Operations 集成方案中的账单方案明细                                                                                                                                                                                    |
| 项目管理和会计 | [510041](https://fix.lcs.dynamics.com/Issue/Details/?bugId=510041)           | 在没有 Dataverse 集成的情况下阻止启用多个合同子项功能                                                                                                                                                                                        |
| 项目管理和会计 | [510527](https://fix.lcs.dynamics.com/Issue/Details/?bugId=510527)           | 当记帐开票 = 损益时，估算屏幕开票收入为零 (0)                                                                                                                                                                          |
| 项目管理和会计 | [514364](https://fix.lcs.dynamics.com/Issue/Details/?bugId=514364)           | WIP - 内部公司项目开票中的销售值过帐选择了意外帐户                                                                                                                                                                           |
| 项目管理和会计 | [522799](https://fix.lcs.dynamics.com/Issue/Details/?bugId=522799)           | 无法在启用 Project Operations 的情况下执行估算/收入识别                                                                                                                                                                         |
| 旅行和支出                | [378738](https://fix.lcs.dynamics.com/Issue/Details/?bugId=378738)           | 代理输入的支出会返回给支出用户，而不是代理                                                                                                                                                                                           |
| 旅行和支出                | [409489](https://fix.lcs.dynamics.com/Issue/Details/?bugId=409489)           | 提交工作流的支出报表工作流代理用户未被标识为工作流发起者                                                                                                                                                             |
| 旅行和支出                | [464658](https://fix.lcs.dynamics.com/Issue/Details/?bugId=464658)           | 法律实体替代中的默认维度在内部公司支出报表上不起作用                                                                                                                                                                    |
| 旅行和支出                | [472892](https://fix.lcs.dynamics.com/Issue/Details/?bugId=472892)           | 关于每日支出类别的最后一日餐饮减少量计算的问题                                                                                                                                                                                    |
| 旅行和支出                | [473646](https://fix.lcs.dynamics.com/Issue/Details/?bugId=473646)           | 从链接到出差申请的支出报表中删除支出行项目后，**出差申请** 页面上的 **待对帐金额** 字段不会更新                                                                                                       |
| 旅行和支出                | [474396](https://fix.lcs.dynamics.com/Issue/Details/?bugId=474396)           | 在提交到工作流后支出报表验证了策略                                                                                                                                                                                           |
| 旅行和支出                | [475777](https://fix.lcs.dynamics.com/Issue/Details/?bugId=475777)            | 不为条目代理正确显示出差支出收据                                                                                                                                                                                            |
| 旅行和支出                | [477714](https://fix.lcs.dynamics.com/Issue/Details/?bugId=477714)            | 将用户语言设置为 es-MX 时，每个员工的支出类型不会显示详细支出                                                                                                                         |
| 旅行和支出                | [477831](https://fix.lcs.dynamics.com/Issue/Details/?bugId=477831)            | 支出报表允许为支出类别输入错误的子类别                                                                                                                                                                                       |
| 旅行和支出                | [478630](https://fix.lcs.dynamics.com/Issue/Details/?bugId=478630)            | 在支出报表金额超过现金预付款金额时，预付现金与支出报表对帐不能按预期方式工作                                                                                                           |
| 旅行和支出                | [486680](https://fix.lcs.dynamics.com/Issue/Details/?bugId=486680)            | ProjProjectLookup 相关查询的性能问题。 由于执行查询需要较长时间，因此会阻止客户。                                                                                                                     |
| 旅行和支出                | [487531](https://fix.lcs.dynamics.com/Issue/Details/?bugId=487531)            | **允许根据抵销付款帐户对交易进行分组** 和 **过帐时更正会计日期** 打开后过帐的支出报表表明会计日期未在 **会计分配** 表上分组，这会影响销售税记录 |
| 旅行和支出                | [491759](https://fix.lcs.dynamics.com/Issue/Details/?bugId=491759)            | 如果在支出报表行上使用了 **冲销费用增值税**，则导入的外币信用卡交易会创建不正确的供应商交易                                                                                                                     |
| 旅行和支出                | [506175](https://fix.lcs.dynamics.com/Issue/Details/?bugId=506175)            | 如果在标题级别添加了项目 ID，则无法创建内部公司支出报表                                                                                                                                                                 |
| 旅行和支出                | [509491](https://fix.lcs.dynamics.com/Issue/Details/?bugId=509491)            | 当支出金额超过现金预付款金额时出现支出付款问题                                                                                                                                                                          |
| 旅行和支出                | [509556](https://fix.lcs.dynamics.com/Issue/Details/?bugId=509556)            | 如果将用户角色分派给特定组织，则内部公司支出报表中的项目 ID 信息为空                                                                                                                                           |
| 旅行和支出                | [513845](https://fix.lcs.dynamics.com/Issue/Details/?bugId=513845)            | 已完成支出报表自动过帐工作流，但未过帐发票                                                                                                                                                                                          |

### <a name="regulatory-updates"></a>法规更新
有关 Finance and Operations 应用的法规更新的信息，请参阅[法规更新](https://docs.microsoft.com/dynamics365/finance/localizations/regulatory-updates)。 您还可以登录到 LCS，使用问题搜索工具查看计划的法规更新。 通过问题搜索，您可以按国家/地区、功能类型和发布进行搜索。
