---
title: 适用于基于库存/生产场景的 2021 年 7 月 Project Operations 中的新增功能或更改
description: 本文提供有关 2021 年 7 月版基于库存/生产场景的 Project Operations 中可用的质量更新的信息。
author: andchoi
ms.date: 07/01/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: andchoi
ms.openlocfilehash: df9a68c5a12e6aec140867eb1db3d88279c05795
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8933619"
---
# <a name="whats-new-or-changed-in-project-operations-july-2021-for-stockedproduction-based-scenarios"></a>适用于基于库存/生产场景的 2021 年 7 月 Project Operations 中的新增功能或更改

_**适用范围：** 适用于基于库存/生产场景的 Project Operations_

本文适用于以下 Dynamics 365 Project Operations 组件和版本：

- Dynamics 365 Finance 环境中的项目管理和会计版本 10.0.20
 
### <a name="quality-updates"></a>质量更新
                                                                                                                                                                                  
| 功能区域                      | 参考编号| 质量更新                                                                                                                                                                          |
|-----------------------------------|--------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 项目管理和会计 | [485394](https://fix.lcs.dynamics.com/Issue/Details/?bugId=485394) | 一旦从采购申请发布中发放采购订单，就会清除采购申请中的成本承诺记录。                                                                           |
| 项目管理和会计 | [529602](https://fix.lcs.dynamics.com/Issue/Details/?bugId=529602) | 对于采购申请，将发生两次预算验证。 此重复意味着无法关闭申请，并且不会创建相应的采购订单。                                                                                                                        |
| 项目管理和会计 | [539439](https://fix.lcs.dynamics.com/Issue/Details/?bugId=539439) | 由于舍入问题，无法完成记帐规则上的 **记帐百分比**。                                                                              |
| 项目管理和会计 | [540023](https://fix.lcs.dynamics.com/Issue/Details/?bugId=540023) | 当您调整交易并且百分比具有小数时，成本和销售价不会正确调整。                                      |
| 项目管理和会计 | [540927](https://fix.lcs.dynamics.com/Issue/Details/?bugId=540927) | 会计源资源管理器显示具有不同活动的多个时间表行的单个时间表行的小时数。                                      |
| 项目管理和会计 | [541471](https://fix.lcs.dynamics.com/Issue/Details/?bugId=541471) | 保存的视图和时间表行详细信息个性化使系统在尝试打开时间表时始终打开列表中第一个时间表的详细信息。  |
| 项目管理和会计 | [548677](https://fix.lcs.dynamics.com/Issue/Details/?bugId=548677) | 项目根节点将消失，并且工作分解结构记录将在导入后删除。                                                                                             |
| 项目管理和会计 | [548999](https://fix.lcs.dynamics.com/Issue/Details/?bugId=548999) | 根据物料要求部分接收和发放物料时，系统将更新错误的预算消耗余额。 |
| 项目管理和会计 | [550959](https://fix.lcs.dynamics.com/Issue/Details/?bugId=550959) | 项目保留款采购订单不会在 **总计** 窗格或 **待定发票** 网格中正确显示总计。                                                                  |
| 项目管理和会计 | [554593](https://fix.lcs.dynamics.com/Issue/Details/?bugId=554593) | 在关闭库存时，项目物料成本调整将过帐到余额帐户，而不是损益帐户。                                                            |
| 项目管理和会计 | [557394](https://fix.lcs.dynamics.com/Issue/Details/?bugId=557394) | 项目过帐的交易凭证和估计凭证使用 USD 作为会计币种，但金额显示的是 CAD 等效量。              |
| 项目管理和会计 | [560140](https://fix.lcs.dynamics.com/Issue/Details/?bugId=560140) | 在具有部分产品收货和部分开票的采购订单发票流程中，具有物料要求和采购订单的承诺成本是错误的。       |
| 项目管理和会计 | [560567](https://fix.lcs.dynamics.com/Issue/Details/?bugId=560567) | 项目调整不能正确地用间接成本更新销售金额。                                                                                    |
| 项目管理和会计 | [561137](https://fix.lcs.dynamics.com/Issue/Details/?bugId=561137) | **时间表** 表缺少与 **工作人员/资源** 视图的定义关系。                                                                                   |
| 项目管理和会计 | [563330](https://fix.lcs.dynamics.com/Issue/Details/?bugId=563330) | 当您为内部公司时间表从下拉菜单中选择 **活动编号** 字段时，无法填充该字段。                                                                 |
| 项目管理和会计 | [563840](https://fix.lcs.dynamics.com/Issue/Details/?bugId=563840) | 您无法将个性化的 **目的** 或 **活动说明** 字段添加到以下页面：**项目过帐的交易**、**发票方案创建** 或 **发票方案**。  |
| 项目管理和会计 | [566348](https://fix.lcs.dynamics.com/Issue/Details/?bugId=566348) | 当使用数据管理 (**ProjSalesItemRequirementEntity**) 创建物料要求时，将提供错误的交付日期控件。                                              |
| 项目管理和会计 | [566544](https://fix.lcs.dynamics.com/Issue/Details/?bugId=566544) | 当您在 Finance 中选择项目合同 ID 时，Project Operations 集成环境将打开该页面以创建新记录，而不是打开现有项目合同。                                                                                                                 |
| 项目管理和会计 | [567300](https://fix.lcs.dynamics.com/Issue/Details/?bugId=567300) |  标签“@SYS4083080”（“无法找到与输入的值对应的唯一工作人员记录”）不会转换为丹麦语。                                |
| 项目管理和会计 | [569901](https://fix.lcs.dynamics.com/Issue/Details/?bugId=569901) | **物料销售税组** 字段在发票方案上不可编辑。                                                                               |
| 项目管理和会计 | [557049](https://fix.lcs.dynamics.com/Issue/Details/?bugId=557049) | 通过不可扣除的税额，承诺成本过高。                                                                                                    |
| 项目管理和会计 | [565080](https://fix.lcs.dynamics.com/Issue/Details/?bugId=565080) | 过帐具有多个项目和不同财务维度的内部公司时间表将在总帐中生成意外的值。                             |
| 项目管理和会计 | [567962](https://fix.lcs.dynamics.com/Issue/Details/?bugId=567962) | 由于同时运行定期流程 **从暂存中导入** 的多个实例，因此发票方案行会重复。                                      |
| 项目管理和会计 | [571339](https://fix.lcs.dynamics.com/Issue/Details/?bugId=571339) | 贷项通知单发票方案过帐存在错误，因此有关凭证的交易不平衡。    |
| 项目管理和会计 | [573567](https://fix.lcs.dynamics.com/Issue/Details/?bugId=573567) | 在发布暂候的待定发票后，项目承诺成本将变得不正确。                                                                             |
| 项目管理和会计 | [573886](https://fix.lcs.dynamics.com/Issue/Details/?bugId=573886) | 当税款采用公司货币以外的其他货币时，您无法为项目销售订单创建贷项通知单。                                      |
| 项目管理和会计 | [582329](https://fix.lcs.dynamics.com/Issue/Details/?bugId=582329) | 删除合同也会删除与客户关联的地址。                                                                                     |
| 项目管理和会计 | [585811](https://fix.lcs.dynamics.com/Issue/Details/?bugId=585811) | 无法过帐由负时间交易更正导致的发票方案。                                                                    |
| 出差和支出                  | [532075](https://fix.lcs.dynamics.com/Issue/Details/?bugId=532075) | 在支出报表中以不同方式计算税款。                                                                                                                  |
| 出差和支出                  | [546450](https://fix.lcs.dynamics.com/Issue/Details/?bugId=546450) | 发行版本更新 **DB72_Expense.updateTrvExpTransProjTransId()** 不允许 **trvExpTrans.ReferenceDataAreaId** 创建新的数字序列。                    |
| 出差和支出                  | [568805](https://fix.lcs.dynamics.com/Issue/Details/?bugId=568805) | 金额字段不与必填字段一起显示。                                                                                                             |
| 出差和支出                  | [568831](https://fix.lcs.dynamics.com/Issue/Details/?bugId=568831) | 使用支出重新打造用户界面将支出附加到支出报表的性能改进。                                                            |
| 出差和支出                  | [570790](https://fix.lcs.dynamics.com/Issue/Details/?bugId=570790) | 您可以删除过帐的支出报表。                                                                                           |
| 出差和支出                  | [571317](https://fix.lcs.dynamics.com/Issue/Details/?bugId=571317) | 支出策略消息多次显示。                                                                                                       |
| 出差和支出                  | [573969](https://fix.lcs.dynamics.com/Issue/Details/?bugId=573969) | **付款方式** 字段包括在 **新支出** 窗格上。                                                                                                      |
| 出差和支出                  | [523557](https://fix.lcs.dynamics.com/Issue/Details/?bugId=523557) | 如果未找到工作流，**重置支出文档状态** 工具应该将支出报表状态重置为 **草稿**。 

### <a name="regulatory-updates"></a>法规更新
有关财务和运营应用的监管更新的信息，请参阅[监管更新](/dynamics365/finance/localizations/regulatory-updates)。 您也可以使用问题搜索工具登录到 Lifecycle Services (LCS) 并查看计划的法规更新。 通过问题搜索，您可以按国家/地区、功能类型和发布进行搜索。


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
