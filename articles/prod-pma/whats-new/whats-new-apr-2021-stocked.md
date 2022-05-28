---
title: 2021 年 4 月 Project Operations 中的新增功能或变更功能 - 适用于库存/生产订单场景
description: 本主题提供有关 2021 年 4 月版适用于库存/生产订单场景的 Project Operations 中提供的质量更新的信息。
author: andchoi
ms.date: 04/22/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: andchoi
ms.openlocfilehash: 42b4da3a77d56891454d094cd771575ff9bff081
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/14/2022
ms.locfileid: "8589599"
---
# <a name="whats-new-or-changed-in-project-operations-april-2021-for-stockedproduction-based-scenarios"></a>2021 年 4 月 Project Operations 中的新增功能或变更功能 - 适用于库存/生产订单场景

_**适用范围：** 面向库存/生产订单场景的 Project Operations_

此主题适用于以下 Dynamics 365 Project Operations 组件和版本：

- Dynamics 365 Finance 环境中的项目管理和会计版本 10.0.18
 
### <a name="quality-updates"></a>质量更新
                                                                                                                                                                                  
| 功能区域                      | 参考编号| 质量更新                                                                                                                                                                          |
|-----------------------------------|--------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 项目管理和会计 | [534393](https://fix.lcs.dynamics.com/Issue/Details/?bugId=534393) | **项目排序** 网格上发生错误。                                                                                                                                                      |
| 项目管理和会计 | [542850](https://fix.lcs.dynamics.com/Issue/Details/?bugId=542850) | 在对项目采购订单的单价和数量进行更正后，承诺金额变高。                                                                                    |
| 项目管理和会计 | [543645](https://fix.lcs.dynamics.com/Issue/Details/?bugId=543645) | 声明了 **ProjParameters** 变量，但在使用此变量前从未为其分配记录缓冲区。                                                                                     |
| 项目管理和会计 | [543674](https://fix.lcs.dynamics.com/Issue/Details/?bugId=543674) | 执行 **在所有公司中填充项目资源** 批处理作业时，**ResRollup** 表被删除。                                                                          |
| 项目管理和会计 | [544417](https://fix.lcs.dynamics.com/Issue/Details/?bugId=544417) | 使用 **采购订单明细 V2** 实体更新采购订单上的 **项目售价** 字段时出现问题。                                                                           |
| 项目管理和会计 | [547652](https://fix.lcs.dynamics.com/Issue/Details/?bugId=547652) | 根据 ID 编号，不能创建子项目。   出现以下错误：“Function Global::int642int 被错误调用。”                                         |
| 项目管理和会计 | [484274](https://fix.lcs.dynamics.com/Issue/Details/?bugId=484274) | 使用同一发票上的采购类别和物料为采购订单开票时，客户收到错误帐户。                                                                      |
| 项目管理和会计 | [509920](https://fix.lcs.dynamics.com/Issue/Details/?bugId=509920) | 将具有间接成本的项目交易从可记帐调整为不可记帐再调整为可记帐，未正确清除 WIP。                                       |
| 项目管理和会计 | [511274](https://fix.lcs.dynamics.com/Issue/Details/?bugId=511274) | 在销售订单中使用保留期和总折扣时，发票金额不正确。                                                                                          |
| 项目管理和会计 | [511315](https://fix.lcs.dynamics.com/Issue/Details/?bugId=511315) | 即使选择了不同的交易类型，明细详细信息上的地址名称也不更改。                                                                           |
| 项目管理和会计 | [522983](https://fix.lcs.dynamics.com/Issue/Details/?bugId=522983) | 在包含部分产品收货和部分开票的采购订单发票流程中，包含项目要求和采购订单的承诺成本不正确。                       |
| 项目管理和会计 | [524226](https://fix.lcs.dynamics.com/Issue/Details/?bugId=524226) | 当项目的财务维度更改时，采购订单标头不反映这些更改。                                                                                                  |
| 项目管理和会计 | [524979](https://fix.lcs.dynamics.com/Issue/Details/?bugId=524979) | 生成的 **固定价格项目** 报表是空的。                                                                                                         |
| 项目管理和会计 | [529445](https://fix.lcs.dynamics.com/Issue/Details/?bugId=529445) | 查看 **付款时支付** 页上的供应商发票时，发票未选择项目 ID 引用。                                                                          |
| 项目管理和会计 | [529982](https://fix.lcs.dynamics.com/Issue/Details/?bugId=529982) | 时间表条目对于处于 **人力资源经理** 角色、具有一个法人的受限访问权限的用户不正确，因为类别未正确获取默认值。                                         |
| 项目管理和会计 | [530008](https://fix.lcs.dynamics.com/Issue/Details/?bugId=530008) | 调整中未考虑原始项目日期，当 **将调整日期用作新项目日期** 字段设置为 **否** 时，这会导致错误。                                             |
| 项目管理和会计 | [530788](https://fix.lcs.dynamics.com/Issue/Details/?bugId=530788) | 使用批计算项目估算时，结果不正确。                                                                                                         |
| 项目管理和会计 | [530834](https://fix.lcs.dynamics.com/Issue/Details/?bugId=530834) | 项目合同上的支出金额与项目上的帐户内金额不一致。                                                                             |
| 项目管理和会计 | [530883](https://fix.lcs.dynamics.com/Issue/Details/?bugId=530883) | 项目会计和项目经理角色无法使用审批组设置创建工时日记帐。                                                                                 |
| 项目管理和会计 | [531974](https://fix.lcs.dynamics.com/Issue/Details/?bugId=531974) | 无法过帐 Microsoft Excel 导入的支出日记帐。                                                                                                                                       |
| 项目管理和会计 | [532548](https://fix.lcs.dynamics.com/Issue/Details/?bugId=532548) | 允许内部公司场景的供应商交易冲销，包括供应商发票和支出报表。                                                                     |
| 项目管理和会计 | [533426](https://fix.lcs.dynamics.com/Issue/Details/?bugId=533426) | 项目调整不能正确地用间接成本更新销售金额。                                                                                                    |
| 项目管理和会计 | [534869](https://fix.lcs.dynamics.com/Issue/Details/?bugId=534869) | 为固定价格项目发票创建贷方通知单并且发票使用交付记帐规则单位时，已发布单位不可用于重新记帐。 |
| 项目管理和会计 | [535428](https://fix.lcs.dynamics.com/Issue/Details/?bugId=535428) | 使用其他货币的项目合同无法正确计算物料日记帐或发票方案上的会计币种。                                                   |
| 项目管理和会计 | [537158](https://fix.lcs.dynamics.com/Issue/Details/?bugId=537158) | 在采购订单明细上更改项目以转移物料要求。                                                                                                                          |
| 项目管理和会计 | [540603](https://fix.lcs.dynamics.com/Issue/Details/?bugId=540603) | 从预测导入到项目预算会导致金额不正确。                                                                                                                    |
| 项目管理和会计 | [540622](https://fix.lcs.dynamics.com/Issue/Details/?bugId=5406222) | 将交易从可记帐调整为不可记帐时，未创建总帐条目。                                                                                            |
| 项目管理和会计 | [540633](https://fix.lcs.dynamics.com/Issue/Details/?bugId=540633) | 打开功能键 **为项目供应商发票保留期限启用成本金额计算功能** 时，未使用“付款时支付”创建项目交易。                  |
| 项目管理和会计 | [541421](https://fix.lcs.dynamics.com/Issue/Details/?bugId=541421) | **创建发票方案** 页存在多个问题。                                                                                                                             |
| 项目管理和会计 | [543390](https://fix.lcs.dynamics.com/Issue/Details/?bugId=543390) | **所有项目** 页不显示带有新语言代码的列表。                                                                                                            |
| 项目管理和会计 | [543803](https://fix.lcs.dynamics.com/Issue/Details/?bugId=543803) | 预算修订了两次以上时，项目预算余额中未批准的预算金额不正确。                                                                |
| 项目管理和会计 | [543968](https://fix.lcs.dynamics.com/Issue/Details/?bugId=543968) | **采购协议** 页在与 Project Operations 集成的 Finance 法人中不可见。                                                                               |
| 项目管理和会计 | [545456](https://fix.lcs.dynamics.com/Issue/Details/?bugId=545456) | 正确的凭证日期未上载到“项目工时”日记帐行。                                                                                                            |
| 项目管理和会计 | [545878](https://fix.lcs.dynamics.com/Issue/Details/?bugId=545878) | 在面向基于资源的场景的 Project Operations 中，由于集成错误，您不能将报价单转换为赢单状态。                                                                      |
| 项目管理和会计 | [546604](https://fix.lcs.dynamics.com/Issue/Details/?bugId=546604) | 在 Project Operations 中，由于检查重叠的合同子项和交易类型，当您尝试在合同子项与项目 ID 之间创建关联时会收到错误消息。                        |
| 项目管理和会计 | [546949](https://fix.lcs.dynamics.com/Issue/Details/?bugId=546949) | 当 **ProjValEmplProjSetup** 表中的记录超过 14,000 条时，**资源/项目验证组** 页存在性能问题。                                                                     |
| 项目管理和会计 | [547440](https://fix.lcs.dynamics.com/Issue/Details/?bugId=547440) | **ProjCDSProjectContractEntity** 可以设置不同客户的资金来源发票地址。                                                                                   |
| 项目管理和会计 | [547606](https://fix.lcs.dynamics.com/Issue/Details/?bugId=547606) | 资源的标准查找功能在 10.0.15 版本之后将不可用。                                                                                          |
| 项目管理和会计 | [547831](https://fix.lcs.dynamics.com/Issue/Details/?bugId=547831) | 采购订单发票凭证上的分类帐帐户和过帐类型与服务项目不匹配。 项目组被设置为 **余额**，分类帐帐户不正确。                   |
| 项目管理和会计 | [550030](https://fix.lcs.dynamics.com/Issue/Details/?bugId=550030) | 即使 **阻止选择父活动** 设置为 **否**，也不会针对待处理的供应商发票显示活动编号。                                            |
| 项目管理和会计 | [550379](https://fix.lcs.dynamics.com/Issue/Details/?bugId=550379) | 当您使用导航路径 **项目** > **预算** > **修订** > **新建** > **导入** 时，系统会为所有项目创建项目预算修订。                                                            |
| 项目管理和会计 | [550577](https://fix.lcs.dynamics.com/Issue/Details/?bugId=550577) | 调整具有不同交易和会计币种的交易时，出现错误的过帐和总帐条目。                                                                        |
| 项目管理和会计 | [557376](https://fix.lcs.dynamics.com/Issue/Details/?bugId=557376) | 为交易创建过帐发票时未包括维度。                                                                                                   |
| 项目管理和会计 | [559416](https://fix.lcs.dynamics.com/Issue/Details/?bugId=559416) | 创建待定供应商发票时调用 **PurchTotals.purchNewTotalAmount()** 方法，发票未与任何采购订单链接，导致出现性能问题。                    |
| 出差和支出                | [480451](https://fix.lcs.dynamics.com/Issue/Details/?bugId=480451) | 存在与里程设置有关的过帐错误。                                                                                                                                          |
| 出差和支出                | [522084](https://fix.lcs.dynamics.com/Issue/Details/?bugId=522084) | **拆分到个人** 对外币支出交易不起作用。                                                                                                         |
| 出差和支出                | [523938](https://fix.lcs.dynamics.com/Issue/Details/?bugId=523938) | 无论是否将 **代理** 设置为资源，支出类别下拉菜单都显示不正确的类别。                                         |
| 出差和支出                | [539266](https://fix.lcs.dynamics.com/Issue/Details/?bugId=539266) | 由于资源/类别验证错误，您无法保存内部公司支出报表。                                                                                             |
| 出差和支出                | [532610](https://fix.lcs.dynamics.com/Issue/Details/?bugId=532610) | 支出报表过帐中的错误里程费率计算有拆分明细。                                                                                                        |
| 出差和支出                | [537404](https://fix.lcs.dynamics.com/Issue/Details/?bugId=537404) | 当包含销售税且付款方式上的抵销帐户类型为 **工作人员** 时，您不能过帐内部公司支出报表。                                                   |
| 出差和支出                | [542927](https://fix.lcs.dynamics.com/Issue/Details/?bugId=542927) | 回滚对 **TrvRequisitionLine** 数据实体和与该实体关联的唯一索引的更改。                                                                                            |
| 出差和支出                | [543239](https://fix.lcs.dynamics.com/Issue/Details/?bugId=543239) | 在支出报表中的特定点添加了日志记录，以支持创建和更新源文档明细。                                                                                           |
| 出差和支出                | [544323](https://fix.lcs.dynamics.com/Issue/Details/?bugId=544323) | 如果将销售税过帐到目标法人，内部公司场景将提供错误的子分类帐日记帐。                                              |
| 出差和支出                | [546877](https://fix.lcs.dynamics.com/Issue/Details/?bugId=546877) | 在 Project Operations 中，从 Dataverse 中删除支出估算后未从 Finance 中删除支出估算。                                                                                         |
| 出差和支出                | [550575](https://fix.lcs.dynamics.com/Issue/Details/?bugId=550575) | 如果支出类别是非项目类别，则 **支出** 页上选择的财务维度不会复制到支出报表。                                          |

### <a name="regulatory-updates"></a>法规更新
有关财务和运营应用的监管更新的信息，请参阅[监管更新](/dynamics365/finance/localizations/regulatory-updates)。 您还可以登录到 LCS，使用问题搜索工具查看计划的法规更新。 通过问题搜索，您可以按国家/地区、功能类型和发布进行搜索。


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
