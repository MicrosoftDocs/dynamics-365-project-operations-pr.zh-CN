---
title: 适用于基于库存/生产场景的 2021 年 5 月 Project Operations 中的新增功能或更改
description: 本文提供有关 2021 年 5 月版基于库存/生产场景的 Project Operations 中可用的质量更新的信息。
author: andchoi
ms.date: 07/01/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: andchoi
ms.openlocfilehash: eff34a4e9fc1fc6429f1fa7a3e4b0d5b664222f9
ms.sourcegitcommit: a798fed5c59e3fefa62cdfa42c852d529b33fd35
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/18/2022
ms.locfileid: "9029381"
---
# <a name="whats-new-or-changed-in-project-operations-may-2021-for-stockedproduction-based-scenarios"></a>适用于基于库存/生产场景的 2021 年 5 月 Project Operations 中的新增功能或更改

_ **适用范围：** 适用于基于库存/生产场景的 Project Operations

本文适用于以下 Dynamics 365 Project Operations 组件和版本：

- Dynamics 365 Finance 环境中的项目管理和会计版本 10.0.19
 
### <a name="quality-updates"></a>质量更新
                                                                                                                                                                                  
| 功能区域                      | 参考编号| 质量更新                                                                                                                                                                          |
|-----------------------------------|--------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 项目管理和会计 | [529751](https://fix.lcs.dynamics.com/Issue/Details/?bugId=529751) | 当针对项目物料日记帐行关闭实体验证时，导入将失败。                                                                                                                                                   |
| 项目管理和会计 | [550565](https://fix.lcs.dynamics.com/Issue/Details/?bugId=550565) | 与 **GeneralJournalEntry** 查找相关的 WIP 客户报表存在性能问题。                                                                                                                                  |
| 项目管理和会计 | [539044](https://fix.lcs.dynamics.com/Issue/Details/?bugId=539044) | WIP 项目缺少财务维度。                                                                                                                                                                                                    |
| 项目管理和会计 | [540903](https://fix.lcs.dynamics.com/Issue/Details/?bugId=540903) | 过帐发票方案失败，因为向 **ProjBudgetReductionHistory** 分配了错误的 **ProjBudgetAllocationLineIdSales**。                                                                                                                           |
| 项目管理和会计 | [547090](https://fix.lcs.dynamics.com/Issue/Details/?bugId=547090) | 在导入 XML 文件后，常规日记帐显示错误的凭证编号。                                                                                                                                                              |
| 项目管理和会计 | [552160](https://fix.lcs.dynamics.com/Issue/Details/?bugId=552160) | 工作分解结构模板发生一个错误。                                                                                                                                                                                          |
| 项目管理和会计 | [552976](https://fix.lcs.dynamics.com/Issue/Details/?bugId=552976) | **窗体注释** 和 **窗体设置** 在 Finance 法人与 Project Operations 集成时在这些法人中的项目管理设置下不可见。                                                                                                             |
| 项目管理和会计 | [553313](https://fix.lcs.dynamics.com/Issue/Details/?bugId=553313) | 取消内部公司销售订单失败，并显示以下错误“无法在采购订单行 (PurchLine) 中编辑记录。 由于删除记录或更改记录中一个或多个字段的其他用户流程，发生了更新冲突。” |
| 项目管理和会计 | [553775](https://fix.lcs.dynamics.com/Issue/Details/?bugId=553775) | 项目交易调整为项目成本创建错误的财务维度。                                                                                                                                                          |
| 项目管理和会计 | [556751](https://fix.lcs.dynamics.com/Issue/Details/?bugId=556751) | 在处理连接到项目的采购订单时，供应商发票具有其他提示。                                                                                                                                                 |
| 项目管理和会计 | [557925](https://fix.lcs.dynamics.com/Issue/Details/?bugId=557925) | 无法批准时间表行，并显示以下错误“工作流的激活条件无效。 将此问题报告给系统管理员。”                                                                          |
| 项目管理和会计 | [559266](https://fix.lcs.dynamics.com/Issue/Details/?bugId=559266) | 如果您收到错误“因为关联的项目 XXXXXX 存在交易而无法更改项目合同”，则仍然可以在项目级别更改合同。                                                                           |
| 项目管理和会计 | [560432](https://fix.lcs.dynamics.com/Issue/Details/?bugId=560432) | 如果您收到错误“因为状态为已扣除的库存交易不充分而无法开具数量发票”，在运行库存重新计算后，无法过帐采购订单发票。                             |
| 项目管理和会计 | [562013](https://fix.lcs.dynamics.com/Issue/Details/?bugId=562013) | 启用资源请求工作流后，当尝试使用项目资源可用性控件打开页面时，存在性能问题。                                                                                                               |
| 项目管理和会计 | [488320](https://fix.lcs.dynamics.com/Issue/Details/?bugId=488320) | 在向项目合同添加指定另一个项目的记帐规则后，发票状态更改为 **非应计费**。                                                                                                                                |
| 项目管理和会计 | [515219](https://fix.lcs.dynamics.com/Issue/Details/?bugId=515219) | 在从项目采购订单中删除预付发票并启用 **针对项目过帐预付成本** 参数时，将出现一个错误。                                                                                                        |
| 项目管理和会计 | [526439](https://fix.lcs.dynamics.com/Issue/Details/?bugId=526439) | 在过帐项目采购订单发票时，将出现一个错误，因为缺少自动物料标记。                                                                                                                            |
| 项目管理和会计 | [527970](https://fix.lcs.dynamics.com/Issue/Details/?bugId=527970) | 当项目发票凭证的过帐类型等于销售税时，增值税的默认说明为空。                                                                                                                                           |
| 项目管理和会计 | [530352](https://fix.lcs.dynamics.com/Issue/Details/?bugId=530352) | 如果删除相关的已取消物料要求销售订单，项目采购订单将显示错误。                                                                                                                                 |
| 项目管理和会计 | [530651](https://fix.lcs.dynamics.com/Issue/Details/?bugId=530651) | 当标记和取消标记项目物料要求采购订单时，引用将丢失。                                                                                                                                                               |
| 项目管理和会计 | [533023](https://fix.lcs.dynamics.com/Issue/Details/?bugId=533023) | 当为项目物料要求打印领料列表时，减少的数量默认值存在问题。                                                                                                                                                 |
| 项目管理和会计 | [535493](https://fix.lcs.dynamics.com/Issue/Details/?bugId=535493) | 如果存在过度交付，则计算的销售价不正确。                                                                                                                                                                                 |
| 项目管理和会计 | [541329](https://fix.lcs.dynamics.com/Issue/Details/?bugId=541329) | 当在发票方案上没有发票数量的情况下发放保留期时，将过帐错误的留置权。                                                                                                                                                |
| 项目管理和会计 | [541997](https://fix.lcs.dynamics.com/Issue/Details/?bugId=541997) | 当生成时间表期间时，第一个期间显示为第 53 周。                                                                                                                                                                         |
| 项目管理和会计 | [542043](https://fix.lcs.dynamics.com/Issue/Details/?bugId=542043) | Dynamics 365 Project Service Automation 集成参数中的默认项目类型应该为时间和材料和固定价格。                                                                                                         |
| 项目管理和会计 | [543096](https://fix.lcs.dynamics.com/Issue/Details/?bugId=543096) | 删除具有记帐规则的发票方案将生成过帐。                                                                                                                                                                              |
| 项目管理和会计 | [543463](https://fix.lcs.dynamics.com/Issue/Details/?bugId=543463) | 无法消除使用完成百分比方法的消除流程的最终估计，因为系统无法识别收入。                                                                                                                                      |
| 项目管理和会计 | [543938](https://fix.lcs.dynamics.com/Issue/Details/?bugId=543938) | 在过帐项目估计时，不会创建过帐估计记录。                                                                                                                                                                            |
| 项目管理和会计 | [546885](https://fix.lcs.dynamics.com/Issue/Details/?bugId=546885) | 在内部公司开票期间，找不到待定供应商发票上的主客户。                                                                                                                                                               |
| 项目管理和会计 | [547885](https://fix.lcs.dynamics.com/Issue/Details/?bugId=547885) | 如果合同包含物料要求，则不能添加另一个资金源。                                                                                                                                                         |
| 项目管理和会计 | [550379](https://fix.lcs.dynamics.com/Issue/Details/?bugId=550379) | 当您使用 **项目** > **预算** > **修订** > **新建** > **导入** 时，系统将对所有项目的项目预算创建修订。                                                                                                                         |
| 项目管理和会计 | [550577](https://fix.lcs.dynamics.com/Issue/Details/?bugId=550577) |  如果您使用不同的交易和会计货币调整交易，则过帐和总帐条目不正确。                                                                                                                                       |
| 项目管理和会计 | [557049](https://fix.lcs.dynamics.com/Issue/Details/?bugId=557049) | 通过不可扣除的税额，承诺成本过高。                                                                                                                                                                                   |
| 项目管理和会计 | [557376](https://fix.lcs.dynamics.com/Issue/Details/?bugId=557376) | 当为交易创建过帐发票时，不会选择任何维度。                                                                                                                                                                  |
| 项目管理和会计 | [559416](https://fix.lcs.dynamics.com/Issue/Details/?bugId=559416) | 当您创建未与导致性能问题的采购订单链接的待定供应商发票时，将调用 **PurchTotals.purchNewTotalAmount()** 方法。                                                                                   |
| 项目管理和会计 | [563694](https://fix.lcs.dynamics.com/Issue/Details/?bugId=563694) | **已用预算** 和 **剩余预算** 列在项目预算余额上显示不正确的金额。                                                                                                                                                |
| 项目管理和会计 | [565089](https://fix.lcs.dynamics.com/Issue/Details/?bugId=565089) | 当在具有 Project Operations 的 Dataverse 中使用基于任务的记帐时，将过帐交易两次。                                                                                                                                         |
| 项目管理和会计 | [566869](https://fix.lcs.dynamics.com/Issue/Details/?bugId=566869) | 在使用 Project Operations 时，收入识别的完成百分比不正确。                                                                                                                                                  |
| 项目管理和会计 | [568107](https://fix.lcs.dynamics.com/Issue/Details/?bugId=568107) | 当您在 Project Operations 集成方案中使用待定供应商发票时，收入应计是双倍的。                                                                                                                                          |
| 项目管理和会计 | [569736](https://fix.lcs.dynamics.com/Issue/Details/?bugId=569736) | 过帐项目时间表将创建重复的交易。                                                                                                                                                                        |
| 项目管理和会计 | [569819](https://fix.lcs.dynamics.com/Issue/Details/?bugId=569819) | 当针对工作订单过帐物料消耗日记帐时，将出现一个错误。                                                                                                                                  |
| 项目管理和会计 | [571197](https://fix.lcs.dynamics.com/Issue/Details/?bugId=571197) | 由于以下错误“对象引用未设置为对象的实例”，无法生成项目生产订单。                                                                                                                           |
| 项目管理和会计 | [572370](https://fix.lcs.dynamics.com/Issue/Details/?bugId=572370) | 如果收入配置文件规则设置为 **组设置**，无法过帐集成日记帐。                                                                                                                                                           |
| 项目管理和会计 | [573596](https://fix.lcs.dynamics.com/Issue/Details/?bugId=573596) | 对于包含具有多个度量单位的行的项目采购订单，无法过帐采购发票。                                                                                                                                             |
| 项目管理和会计 | [573637](https://fix.lcs.dynamics.com/Issue/Details/?bugId=573637) | 无法使用 **项目 V2** 数据实体更新项目的默认财务维度。                                                                                                                                                          |
| 项目管理和会计 | [573886](https://fix.lcs.dynamics.com/Issue/Details/?bugId=573886) | 当税款采用公司货币以外的其他货币时，无法为项目销售订单创建贷项通知单。                                                                                                                     |
| 项目管理和会计 | [574104](https://fix.lcs.dynamics.com/Issue/Details/?bugId=574104) | 当使用超过 100 个记帐规则创建发票方案时，存在一个问题。                                                                                                                                                                  |
| 项目管理和会计 | [577211](https://fix.lcs.dynamics.com/Issue/Details/?bugId=577211) | 项目估计创建批处理流程的完成时间过长。                                                                                                                                                                      |
| 项目管理和会计 | [577785](https://fix.lcs.dynamics.com/Issue/Details/?bugId=577785) | 当运行功能 **跨所有公司填充项目资源** 时，将发生以下错误“无效的对象名称 ResRollupCalendar。”                                                                                                                                   |
| 项目管理和会计 | [582329](https://fix.lcs.dynamics.com/Issue/Details/?bugId=582329) | 当删除合同时，还会删除与客户关联的地址。                                                                                                                                                                    |
| 出差和支出                  | [514930](https://fix.lcs.dynamics.com/Issue/Details/?bugId=514930) | 未正确评估支出报表审批工作流条件。                                                                                                                                                                           |
| 出差和支出                  | [519304](https://fix.lcs.dynamics.com/Issue/Details/?bugId=519304) | 支出报表策略未正确评估项目 ID。                                                                                                                                                                                   |
| 出差和支出                  | [522463](https://fix.lcs.dynamics.com/Issue/Details/?bugId=522463) | 针对内部公司支出交易 **拆分为个人** 操作无法正确工作。                                                                                                                                                                |
| 出差和支出                  | [534702](https://fix.lcs.dynamics.com/Issue/Details/?bugId=534702) | 当删除出差申请时，有时会删除支出报表行的理由。 当支出报表和出差申请的 recid 相同时，会发生此情况。                                                            |
| 出差和支出                  | [544368](https://fix.lcs.dynamics.com/Issue/Details/?bugId=544368) | 当支出报表策略需要 **项目 ID** 字段时，支出移动应用存在问题。                                                                                                                                                |
| 出差和支出                  | [545331](https://fix.lcs.dynamics.com/Issue/Details/?bugId=545331) | 当您尝试编辑与项目关联的内部公司支出时，将出现以下错误消息“对象引用未设置为对象的实例。”                                                                           |
| 出差和支出                  | [548659](https://fix.lcs.dynamics.com/Issue/Details/?bugId=548659) | 在过帐支出报表后，错误的货币和金额将在银行分类帐中列出。                                                                                                                                                                |
| 出差和支出                  | [555462](https://fix.lcs.dynamics.com/Issue/Details/?bugId=5355462) | 在使用承诺成本关闭出差申请后，不会发放项目的承诺成本。                                                                                                                                              |
| 出差和支出                  | [558336](https://fix.lcs.dynamics.com/Issue/Details/?bugId=558336) | 已对删除信用卡交易功能进行了改进。                                                                                                                                                                                           |
| 出差和支出                  | [525070](https://fix.lcs.dynamics.com/Issue/Details/?bugId=525070) | 当在法人中指定不同的报告货币时，支出报表中包括的销售税的计算不一致。                                                                                                         |
| 出差和支出                  | [527779](https://fix.lcs.dynamics.com/Issue/Details/?bugId=527779) | 当添加新现金出差支出时，性能会受到影响。                                                                                                                                                                                         |
| 出差和支出                  | [537841](https://fix.lcs.dynamics.com/Issue/Details/?bugId=537841) | 未在支出报表上触发支出策略规则。                                                                                                                                                                                            |
| 出差和支出                  | [566386](https://fix.lcs.dynamics.com/Issue/Details/?bugId=566386) | 使用数据管理框架上传新的共享类别会删除所有共享类别的所有子类别。                                                                                                                         |
| 出差和支出                  | [574131](https://fix.lcs.dynamics.com/Issue/Details/?bugId=574131) | 当您创建支出行并选择类别时，将出现以下错误“销售税组 DOM 和物料销售税组 STD 的组合无效。”                                                                  |
| 出差和支出                  | [574900](https://fix.lcs.dynamics.com/Issue/Details/?bugId=574900) | 支出移动应用程序存在同步问题。 

### <a name="regulatory-updates"></a>法规更新
有关财务和运营应用的监管更新的信息，请参阅[监管更新](/dynamics365/finance/localizations/regulatory-updates)。 您也可以使用问题搜索工具登录到 Lifecycle Services (LCS) 并查看计划的法规更新。 通过问题搜索，您可以按国家/地区、功能类型和发布进行搜索。


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
