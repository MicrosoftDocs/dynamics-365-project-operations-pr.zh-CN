---
title: 2021 年 3 月 Project Operations 中的新增功能或变更功能 - 适用于库存/生产订单场景
description: 本文提供有关 2021 年 3 月版基于库存/生产场景的 Project Operations 中可用的质量更新的信息。
author: andchoi
ms.date: 03/22/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: andchoi
ms.openlocfilehash: fffa9d70574c8c91b63ceb5055af64a49c9d398b
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8911309"
---
# <a name="whats-new-or-changed-in-project-operations-march-2021-for-stockedproduction-based-scenarios"></a>2021 年 3 月 Project Operations 中的新增功能或变更功能 - 适用于库存/生产订单场景

_**适用范围：** 面向库存/生产订单场景的 Project Operations_

本文适用于以下 Dynamics 365 Project Operations 组件和版本：

- Dynamics 365 Finance 环境中的项目管理和会计版本 10.0.17

## <a name="features-included-in-this-release"></a>此版本中包括的功能
此版本包含以下功能：

  - [项目发票方案性能](../project-invoice-proposal-performance.md)
 
### <a name="quality-updates"></a>质量更新

| 功能区域                        | 参考编号 | 质量更新                                                                                                                                                                                                                                                   |
|-------------------------------------|------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 项目管理和会计 | [420064](https://fix.lcs.dynamics.com/Issue/Details/?bugId=420064) | 重新计算库存后，未更新已过帐的负数项目交易。                                                                                                                      |
| 项目管理和会计 | [438692](https://fix.lcs.dynamics.com/Issue/Details/?bugId=438692) | 如果没有为资金来源分配交易或发票，则可以删除资金来源。                                                                                                           |
| 项目管理和会计 | [439470](https://fix.lcs.dynamics.com/Issue/Details/?bugId=439470) | 实际估算交易不会显示上一期间中的支出和项目交易。                                                                                                       |
| 项目管理和会计 | [452710](https://fix.lcs.dynamics.com/Issue/Details/?bugId=452710) | 对于项目项要求的装箱单，分类帐描述值不正确。                                                                                                              |
| 项目管理和会计 | [455602](https://fix.lcs.dynamics.com/Issue/Details/?bugId=455602) | 当针对项目过帐日记帐后，不会从凭证中的员工和项目中选择财务维度。                                                                               |
| 项目管理和会计 | [472988](https://fix.lcs.dynamics.com/Issue/Details/?bugId=472988) | 在项目发票总额中更新明细净额时，将用过帐交易中的调整金额填充销售额。                                                                               |
| 项目管理和会计 | [477969](https://fix.lcs.dynamics.com/Issue/Details/?bugId=477969) | 查看 **付款时支付供应商发票** 页面上的供应商发票明细时，发票未选择项目 ID 参考。                                                                                                   |
| 项目管理和会计 | [478667](https://fix.lcs.dynamics.com/Issue/Details/?bugId=478667) | 具有多个资金来源的固定价格项目的 **帐户内** 页面上的合同金额不正确。                                                                                                  |
| 项目管理和会计 | [481443](https://fix.lcs.dynamics.com/Issue/Details/?bugId=481443) | 即使过帐抵销后，固定价格项目的应计收入也不会调整。                                                                                                                                |
| 项目管理和会计 | [483209](https://fix.lcs.dynamics.com/Issue/Details/?bugId=483209) | 在通过发票方案为项目销售订单开具发票时，未更新信用证状态。                                                                                                  |
| 项目管理和会计 | [484274](https://fix.lcs.dynamics.com/Issue/Details/?bugId=484274) | 为购买订单开具发票并且发票包含采购类别和项目时，客户将收到错误的帐户信息。                                                                                              |
| 项目管理和会计 | [484817](https://fix.lcs.dynamics.com/Issue/Details/?bugId=484817) | 通过定期批处理作业生成的项目发票方案具有金额为零的重复交易。                                                                                                  |
| 项目管理和会计 | [486817](https://fix.lcs.dynamics.com/Issue/Details/?bugId=486817) | 在运行项目损益报表时，删除错误限制检查。                                                                                                                                  |
| 项目管理和会计 | [488076](https://fix.lcs.dynamics.com/Issue/Details/?bugId=488076) | 在 **时间和材料项目代码** 上使用 **过帐成本** 功能时，通过内部公司重新计费过帐的支出不会显示损益条目。                                                         |
| 项目管理和会计 | [488382](https://fix.lcs.dynamics.com/Issue/Details/?bugId=488382) | 固定价格项目的已过帐项目交易的 **发票状态** 筛选器不工作。                                                                                                   |
| 项目管理和会计 | [488783](https://fix.lcs.dynamics.com/Issue/Details/?bugId=488783) | 由于代理记录重复，因此时间表条目会重复。                                                                                                                                           |
| 项目管理和会计 | [491941](https://fix.lcs.dynamics.com/Issue/Details/?bugId=491941) | 冲销估算消除在 **定期** 中无法正常工作。                                                                                                                                                 |
| 项目管理和会计 | [498010](https://fix.lcs.dynamics.com/Issue/Details/?bugId=498010) | 添加其他范围时，无法从 **项目管理和会计** 模块中的 **调整交易** 选项中选择适当的数据。 忽略了 **其他** 筛选器。                      |
| 项目管理和会计 | [508494](https://fix.lcs.dynamics.com/Issue/Details/?bugId=508494) | 在记录作业后，无法重置生产订单的状态。                                                                                                              |
| 项目管理和会计 | [509716](https://fix.lcs.dynamics.com/Issue/Details/?bugId=509716) | 来自项目的具有自动预留和可承诺能力 (CTP) 的项目不会保留。                                                                                                                      |
| 项目管理和会计 | [509773](https://fix.lcs.dynamics.com/Issue/Details/?bugId=509773) | **会计调整** 功能会使选择了 **不允许手动输入** 的分类帐科目产生问题。                                                                     |
| 项目管理和会计 | [510079](https://fix.lcs.dynamics.com/Issue/Details/?bugId=510079) | 在删除估算后，不应在项目对帐单上的 **应计收入 - 销售值** 字段中显示任何值。                                                                                 |
| 项目管理和会计 | [510607](https://fix.lcs.dynamics.com/Issue/Details/?bugId=510607) | 通过角色定价进行项目调整时，成本和销售价格不正确。                                                                                                                        |
| 项目管理和会计 | [10728](https://fix.lcs.dynamics.com/Issue/Details/?bugId=10728) | 在 Project Operations 中，在部分保留款更正之后，保留款更正发票不起作用。                                                                                                                   |
| 项目管理和会计 | [510743](https://fix.lcs.dynamics.com/Issue/Details/?bugId=510743) | 只有取消内部公司采购订单时，才应启用 **移除链接** 选项。                                                                                                                                          |
| 项目管理和会计 | [514364](https://fix.lcs.dynamics.com/Issue/Details/?bugId=514364) | 内部公司项目开票中的 WIP 销售值过帐选择了意外帐户。                                                                                                                  |
| 项目管理和会计 | [514432](https://fix.lcs.dynamics.com/Issue/Details/?bugId=514432) | 当发票方案包含为贷方通知单选择的明细时，不会重新计算计费规则中的费用。                                                                                            |
| 项目管理和会计 | [515820](https://fix.lcs.dynamics.com/Issue/Details/?bugId=515820) | 如果尚未针对支出交易运行项目发票方案，则“联邦奖项查询支出”计划会显示收据金额。                                               |
| 项目管理和会计 | [516301](https://fix.lcs.dynamics.com/Issue/Details/?bugId=516301) | 在项目报表中，具有 **余额** 项目组的服务项目的 WIP 成本不正确。                                                                                               |
| 项目管理和会计 | [516553](https://fix.lcs.dynamics.com/Issue/Details/?bugId=516553) | 无法对与项目关联的自由文本发票进行更正。                                                                                                                                                  |
| 项目管理和会计 | [517074](https://fix.lcs.dynamics.com/Issue/Details/?bugId=517074) | 当您根据零销售价格调整项目交易时，将创建发票状态为 **非应计费** 的新调整交易。                                                               |
| 项目管理和会计 | [517414](https://fix.lcs.dynamics.com/Issue/Details/?bugId=517414) | 如果您同时调整多个明细，则过帐项目调整期间会出现问题。                                                                                                                               |
| 项目管理和会计 | [518001](https://fix.lcs.dynamics.com/Issue/Details/?bugId=518001) | 如果过帐装箱单后产品成本价格和项目需求数量发生变化，则过帐调整后的成本金额不正确。                                                                   |
| 项目管理和会计 | [518092](https://fix.lcs.dynamics.com/Issue/Details/?bugId=518092) | 直接交付采购订单的财务维度不正确，已由销售订单财务维度替换。                                                              |
| 项目管理和会计 | [518605](https://fix.lcs.dynamics.com/Issue/Details/?bugId=518605) | 当预测数量为零时，负数量项目日记帐行不会更新预测。                                                                                        |
| 项目管理和会计 | [518657](https://fix.lcs.dynamics.com/Issue/Details/?bugId=518657) | 尝试使用 Microsoft Excel 导入项目要求会导致收据日期错误。                                                                                                                                                    |
| 项目管理和会计 | [519200](https://fix.lcs.dynamics.com/Issue/Details/?bugId=519200) | 过帐发票时，不会更新供应商发票交易的项目项交易参考。                                                                                               |
| 项目管理和会计 | [519716](https://fix.lcs.dynamics.com/Issue/Details/?bugId=519716) | 当您发布项目发票方案时，可能会出现以下错误：“添加预扣除的保留款发票后，交易未以报告货币保持平衡”。                                                                    |
| 项目管理和会计 | [520268](https://fix.lcs.dynamics.com/Issue/Details/?bugId=520268) | 如果使用项目布局，则 **供应商付款保留** 报表中不会填充项目 ID 和项目名称。                                                                                              |
| 项目管理和会计 | [520872](https://fix.lcs.dynamics.com/Issue/Details/?bugId=520872) | 如果通过数据实体创建项目，则分类帐过帐排序优先级不正确。                                                                                                                      |
| 项目管理和会计 | [521150](https://fix.lcs.dynamics.com/Issue/Details/?bugId=521150) | 对于基于具有供应商保留金额的采购订单生成的已过帐项目交易，成本金额不正确。 这会导致项目对帐单和固定价格项目成本控制中生成错误的值。 |
| 项目管理和会计 | [521374](https://fix.lcs.dynamics.com/Issue/Details/?bugId=521374) | 在更新标题时，项目销售报价单错误地更新了单价。                                                                                                                    |
| 项目管理和会计 | [521807](https://fix.lcs.dynamics.com/Issue/Details/?bugId=521807) | 在 Project Operations 中处理保留款时，如果在为预付款开具发票后更改合同的默认项目，则以后会导致入账扣缴问题。                                                                        |
| 项目管理和会计 | [521857](https://fix.lcs.dynamics.com/Issue/Details/?bugId=521857) | 供应商发票和项目销售价格的发票日期已更改。                                                                                                                                  |
| 项目管理和会计 | [522897](https://fix.lcs.dynamics.com/Issue/Details/?bugId=520872) | 当您调整具有不同汇率的公司间交易时，会出现问题。                                                                                                                |
| 项目管理和会计 | [522983](https://fix.lcs.dynamics.com/Issue/Details/?bugId=522983) | 在带有部分产品收据和部分发票的采购订单发票流程中，带有项目需求和采购订单的承诺成本不正确。                                                |
| 项目管理和会计 | [523960](https://fix.lcs.dynamics.com/Issue/Details/?bugId=523960) | 用汇率冲销估算时，会出现不正确的值。                                                                                                                                             |
| 项目管理和会计 | [524242](https://fix.lcs.dynamics.com/Issue/Details/?bugId=524242) | 以小时为单位的工作量将在任务级别的工作分解结构模板上自动清除。                                                                                                                         |
| 项目管理和会计 | [524911](https://fix.lcs.dynamics.com/Issue/Details/?bugId=524911) | 当您将报价的状态更新为 **缺失** 时，您启动的所有状态为 **已创建** 或 **已发送** 的报价单的状态也会更新为 **缺失**。                 |
| 项目管理和会计 | [525182](https://fix.lcs.dynamics.com/Issue/Details/?bugId=525182) | 如果交付日期在将来，则销售发票在发票方案中不可见。                                                                                                                  |
| 项目管理和会计 | [526180](https://fix.lcs.dynamics.com/Issue/Details/?bugId=526180) | **项目项日记帐明细** 实体的业务逻辑发生了变化。                                                                                                                                          |
| 项目管理和会计 | [526522](https://fix.lcs.dynamics.com/Issue/Details/?bugId=526522) | 公司间客户发票上的应计收入与时间表和外币重估不匹配。                                                                                 |
| 项目管理和会计 | [526650](https://fix.lcs.dynamics.com/Issue/Details/?bugId=526650) | 根据项目采购申请或项目创建了项目采购订单明细上的交货提醒后，错误地计算了承诺成本。                    |
| 项目管理和会计 | [526812](https://fix.lcs.dynamics.com/Issue/Details/?bugId=526812) | 调整项目时，可能会发生以下错误：“库存单位中未更新财务数据”。                                                                                                             |
| 项目管理和会计 | [527319](https://fix.lcs.dynamics.com/Issue/Details/?bugId=527319) | 在 Project Operations 中，如果需要，从合同中删除项目应该会重置合同的默认项目。                                                                                       |
| 项目管理和会计 | [527945](https://fix.lcs.dynamics.com/Issue/Details/?bugId=527945) | 在核销使用税时，项目支出的销售价格不正确。                                                                                                                                         |
| 项目管理和会计 | [528020](https://fix.lcs.dynamics.com/Issue/Details/?bugId=528020) | 用其他发票更新项目采购订单明细时，项目项需求上过帐了错误的数量。                                                                                                 |
| 项目管理和会计 | [528212](https://fix.lcs.dynamics.com/Issue/Details/?bugId=528212) | 在 Project Operations 中，错误的支出明细会显示在公司内部发票上的 **添加明细** 列表中。                                                                                                |
| 项目管理和会计 | [529887](https://fix.lcs.dynamics.com/Issue/Details/?bugId=529887) | 当使用发票注册和发票批准过帐交易时，**项目过帐交易** 页面上的 **供应商帐户** 字段为空白。                                                                  |
| 项目管理和会计 | [530008](https://fix.lcs.dynamics.com/Issue/Details/?bugId=530008) | 调整中未考虑原始项目日期，当 **将调整日期用作新项目日期** 设置为 **否** 时，这会导致错误。                                                                     |
| 项目管理和会计 | [530241](https://fix.lcs.dynamics.com/Issue/Details/?bugId=530241) | 如果交易币种与公司货币不同，则与项目相关的一般日记帐和支出日记帐上的销售价格计算不正确。                                     |
| 项目管理和会计 | [530658](https://fix.lcs.dynamics.com/Issue/Details/?bugId=530658) | 未在项目采购订单的部分发票的凭证上显示销售交易。                                                                                                                          |
| 项目管理和会计 | [530883](https://fix.lcs.dynamics.com/Issue/Details/?bugId=530883) | 项目会计和项目经理角色无法使用批准组设置创建小时日记帐。                                                                                                         |
| 项目管理和会计 | [531974](https://fix.lcs.dynamics.com/Issue/Details/?bugId=531974) | 无法发布使用 Microsoft Excel 导入的支出报表。                                                                                                                                                              |
| 项目管理和会计 | [532106](https://fix.lcs.dynamics.com/Issue/Details/?bugId=532106) | 由于 **消息** 字段未激活，因此无法创建时间表策略。                                                                                                                               |
| 项目管理和会计 | [532548](https://fix.lcs.dynamics.com/Issue/Details/?bugId=532548) | 存在内部公司方案中允许进行供应商交易冲销的问题。 这适用于供应商发票和支出报表。                                                                                 |
| 项目管理和会计 | [532692](https://fix.lcs.dynamics.com/Issue/Details/?bugId=532692) | 无法重置批准的时间表上的分发。                                                                                                                                                     |
| 项目管理和会计 | [532843](https://fix.lcs.dynamics.com/Issue/Details/?bugId=532843) | 用小时和项目日记帐的汇率冲销估算时，会出现不正确的值。                                                                                                                  |
| 项目管理和会计 | [533426](https://fix.lcs.dynamics.com/Issue/Details/?bugId=533426) | 项目调整不能正确地用间接成本更新销售额。                                                                                                                              |
| 项目管理和会计 | [534597](https://fix.lcs.dynamics.com/Issue/Details/?bugId=534597) | 当您过帐小时日记帐时，会出现以下错误消息：“未指定维度值”。                                                                                                                                  |
| 项目管理和会计 | [535428](https://fix.lcs.dynamics.com/Issue/Details/?bugId=535428) | 使用其他货币的项目合同无法正确计算凭证上的记帐货币。                                                                                              |
| 项目管理和会计 | [535652](https://fix.lcs.dynamics.com/Issue/Details/?bugId=535652) | 内部公司时间表 WIP 过帐使用了错误的销售 WIP 帐户。                                                                                                                                     |
| 项目管理和会计 | [536536](https://fix.lcs.dynamics.com/Issue/Details/?bugId=536536) | 当应用折扣并更新仓库时，项目报价将错误地计算价格。                                                                                                       |
| 项目管理和会计 | [537905](https://fix.lcs.dynamics.com/Issue/Details/?bugId=537905) | 在项目交易中使用项目成本调整后运行重新计算时，会出现以下错误消息：“由于错误而暂停重新计算”。                                                               |
| 项目管理和会计 | [540622](https://fix.lcs.dynamics.com/Issue/Details/?bugId=540622) | 应计收入过程中将交易从可计费调整为不可计费时，将不会创建总帐条目。                                                                                              |
| 项目管理和会计 | [540633](https://fix.lcs.dynamics.com/Issue/Details/?bugId=540633) | 打开项目供应商发票保留功能 **启用成本金额计算** 时，不会使用“付款时支付”功能创建 **ProjTrans**。                                             |
| 项目管理和会计 | [541421](https://fix.lcs.dynamics.com/Issue/Details/?bugId=541421) | **创建发票方案** 页面存在多个问题。                                                                                                                                                     |
| 项目管理和会计 | [543968](https://fix.lcs.dynamics.com/Issue/Details/?bugId=543968) | 在 Project Operations 中，**购买协议** 页在与 Project Operations 集成的财务法律实体中不可见。                                                                                             |
| 项目管理和会计 | [544132](https://fix.lcs.dynamics.com/Issue/Details/?bugId=544132) | 即使打开了 **自动将会计日期设置为下一个开放期** 选项，也无法过帐会计日期在结束期间内的高级日记帐。                                                |
| 项目管理和会计 | [545878](https://fix.lcs.dynamics.com/Issue/Details/?bugId=545878) | 由于 Dataverse 集成错误，因此无法在 Project Operations 中将报价单转换为赢单状态。                                                                                                                                       |
| 项目管理和会计 | [546604](https://fix.lcs.dynamics.com/Issue/Details/?bugId=546604) | 在 Project Operations 中，由于检查重叠的合同子项和交易类型，导致您尝试将合同子项与项目 ID 关联时会出现错误消息。                                                |
| 项目管理和会计 | [547440](https://fix.lcs.dynamics.com/Issue/Details/?bugId=547440) | **ProjCDSProjectContractEntity** 可以设置不同客户的资金来源发票地址。                                                                                                             |
| 项目管理和会计 | [547606](https://fix.lcs.dynamics.com/Issue/Details/?bugId=547606) | 在 10.0.15 更新之后，页面上的资源标准查找功能不可用。                                                                                                                    |
| 项目管理和会计 | [547831](https://fix.lcs.dynamics.com/Issue/Details/?bugId=547831) | 当项目组设置为 **余额** 时，总账凭证上的分类帐科目和过帐类型不正确，非库存服务项的采购订单凭证上的过帐类型不正确。                                 |
| 项目管理和会计 | [550030](https://fix.lcs.dynamics.com/Issue/Details/?bugId=550030) | 即使 **阻止选择父活动** 设置为“否”，也不会针对待处理的供应商发票显示活动编号。                                                                    |
| 项目管理和会计 | [557376](https://fix.lcs.dynamics.com/Issue/Details/?bugId=557376) | 在 Project Operations 中，当您为交易创建过帐发票时，未选择任何维度。                                                                                                                   |
| 项目管理和会计 | [442814](https://fix.lcs.dynamics.com/Issue/Details/?bugId=442814) | 在项目管理和会计中，无法针对内部公司时间表准确反映转移价格的优先级。                                                                            |
| 项目管理和会计 | [533530](https://fix.lcs.dynamics.com/Issue/Details/?bugId=533530) | 旧的工作分解结构 (WBS) 类方法 **ProjWBSUpdateController::updateOutlineNumbersAndPublishInPreOrder** 已弃用。                                                                                                   |

### <a name="regulatory-updates"></a>法规更新
有关财务和运营应用的监管更新的信息，请参阅[监管更新](/dynamics365/finance/localizations/regulatory-updates)。 您还可以登录到 LCS，使用问题搜索工具查看计划的法规更新。 通过问题搜索，您可以按国家/地区、功能类型和发布进行搜索。


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
