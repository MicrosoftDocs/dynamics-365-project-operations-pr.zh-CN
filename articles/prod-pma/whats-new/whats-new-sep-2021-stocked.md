---
title: 2021 年 9 月适用于库存/生产订单场景的 Project Operations 新增功能或变更功能
description: 本文提供有关 2021 年 9 月版基于库存/生产场景的 Project Operations 中可用的质量更新的信息。
author: andchoi
ms.date: 11/11/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: andchoi
ms.openlocfilehash: 1e99471b4338209c1f7fe411084d1745d74b2d2c
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8916507"
---
# <a name="whats-new-or-changed-in-project-operations-september-2021-for-stockedproduction-based-scenarios"></a>2021 年 9 月适用于库存/生产订单场景的 Project Operations 新增功能或变更功能

_**适用范围：** 适用于基于库存/生产场景的 Project Operations_

本文适用于以下 Microsoft Dynamics 365 Project Operations 组件和版本：

- Dynamics 365 Finance 环境中的项目管理和会计版本 10.0.21
 
## <a name="quality-updates"></a>质量更新

| 功能区域 | 参考编号 | 质量更新 |
|---|---|---|
| 项目管理和会计 | [412077](https://fix.lcs.dynamics.com/Issue/Details/?bugId=412077) | 如果允许采购经理角色访问一个法人，则此角色也可以访问所有法人中的所有项目。 |
| 项目管理和会计 | [537214](https://fix.lcs.dynamics.com/Issue/Details/?bugId=537214) | 根据原始项目发票结算贷项通知单时，会出现增值税 (VAT) 舍入问题。 |
| 项目管理和会计 | [538002](https://fix.lcs.dynamics.com/Issue/Details/?bugId=538002) | 使用备用项目预算进行预算验证。 |
| 项目管理和会计 | [546265](https://fix.lcs.dynamics.com/Issue/Details/?bugId=546265) | 不在项目报价工作分解结构中计算 **销售价小时** 价格组。 |
| 项目管理和会计 | [555604](https://fix.lcs.dynamics.com/Issue/Details/?bugId=555604) | 启用了 **启用项目合同货币以进行估算计算** 功能后，估算消除失败。 |
| 项目管理和会计 | [563523](https://fix.lcs.dynamics.com/Issue/Details/?bugId=563523) | 在项目支出日记帐的销售税组中使用销项税时，各数量的销售税因式分解会添加到销售价格金额中。 |
| 项目管理和会计 | [564701](https://fix.lcs.dynamics.com/Issue/Details/?bugId=564701) | 将供应商保留款和预付款应用于采购订单发票后，未正确计算最后一次付款的条件税。 |
| 项目管理和会计 | [565642](https://fix.lcs.dynamics.com/Issue/Details/?bugId=565642) | 调整跟踪不适用于期初余额日记帐。 |
| 项目管理和会计 | [568814](https://fix.lcs.dynamics.com/Issue/Details/?bugId=568814) | **各期间的项目预算修订分配** 会跨越所有预算期间。 提交分配后，不会清除记录。 |
| 项目管理和会计 | [569250](https://fix.lcs.dynamics.com/Issue/Details/?bugId=569250) | 在制品 (WIP) 过帐到总帐的金额不正确。 |
| 项目管理和会计 | [570731](https://fix.lcs.dynamics.com/Issue/Details/?bugId=570371) | 项目小时日记帐审批不管用。 |
| 项目管理和会计 | [571391](https://fix.lcs.dynamics.com/Issue/Details/?bugId=571391) | 未标记资金限额时，不会用间接成本来更新项目调整销售价格。 |
| 项目管理和会计 | [575831](https://fix.lcs.dynamics.com/Issue/Details/?bugId=575831) | 当销售表标题为“已开票”且现有行的支持采购订单已完成时，无法创建物料需求。 |
| 项目管理和会计 | [578036](https://fix.lcs.dynamics.com/Issue/Details/?bugId=578036) | 在为里程碑选择的相应项目 ID 中不会过帐具有其他项目的里程碑的计费规则保留金额。 而是会在第一个项目中过帐。 |
| 项目管理和会计 | [578327](https://fix.lcs.dynamics.com/Issue/Details/?bugId=578327) | 当您在发票方案中选择 **财务维度集** 时，会出现以下错误：“无法将 "Dynamics.AX.Application.FormIntControl" 类型的对象转换为 "Dynamics.AX.Application.FormStringControl" 类型。” |
| 项目管理和会计 | [581167](https://fix.lcs.dynamics.com/Issue/Details/?bugId=581167) | **项目发票** 报表将跳过某些行。 |
| 项目管理和会计 | [581489](https://fix.lcs.dynamics.com/Issue/Details/?bugId=581489) | 计算投资项目的成本控制时发生错误。 |
| 项目管理和会计 | [590357](https://fix.lcs.dynamics.com/Issue/Details/?bugId=590357) | **ProjTable::InitFromCustTable - canDeletePostalAddress** 方法会导致性能问题。 |
| 项目管理和会计 | [592493](https://fix.lcs.dynamics.com/Issue/Details/?bugId=592493) | 错误消息应比“意外错误”明确一些。 |
| 项目管理和会计 | [598810](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598810) | 即使未生成发票行，项目发票过帐批处理作业仍会处理和过帐发票方案。 |
| 项目管理和会计 | [574282](https://fix.lcs.dynamics.com/Issue/Details/?bugId=574282) | 关闭公共部门许可证配置密钥时会出现舍入问题。 对于具有多个资金来源的合同，系统根据时间表时数生成了不正确的成本或销售价格。 |
| 项目管理和会计 | [577598](https://fix.lcs.dynamics.com/Issue/Details/?bugId=577598) | 如果销售价格模型是 **贡献率**，则将错误地计算开单项目采购订单上的项目销售价格。 |
| 项目管理和会计 | [580784](https://fix.lcs.dynamics.com/Issue/Details/?bugId=580784) | 系统在计算员工的有效人工费率时不考虑可用的间隔天数。 |
| 项目管理和会计 | [584054](https://fix.lcs.dynamics.com/Issue/Details/?bugId=584054) | 由于出现以下验证错误，内部公司时间表上出现过帐错误：“没有为法人配置贸易伙伴。” |
| 项目管理和会计 | [586303](https://fix.lcs.dynamics.com/Issue/Details/?bugId=586303) | 在已过帐项目交易列表中不会检索具有支出类别的采购订单中的描述。 |
| 项目管理和会计 | [590349](https://fix.lcs.dynamics.com/Issue/Details/?bugId=590349) | 过帐到项目的物料日记帐上的转换不正确。 |
| 项目管理和会计 | [557294](https://fix.lcs.dynamics.com/Issue/Details/?bugId=557294) | 即使已超出资金限额，您仍可以确认采购订单。 |
| 项目管理和会计 | [574162](https://fix.lcs.dynamics.com/Issue/Details/?bugId=574162) | 选择项目 ID 后，普通发票上的 **更正/取消发票** 部分将消失。 |
| 项目管理和会计 | [575425](https://fix.lcs.dynamics.com/Issue/Details/?bugId=575425) | 从包含库存物料的项目销售订单过帐项目发票方案时会出现性能问题。 |
| 项目管理和会计 | [575939](https://fix.lcs.dynamics.com/Issue/Details/?bugId=575939) | 无法过帐项目采购发票，因为出现以下错误：“已错误地调用了 AccDistProcessorProjectExtension.createForProjectRevenueLine 函数。” |
| 项目管理和会计 | [578970](https://fix.lcs.dynamics.com/Issue/Details/?bugId=578970) | 更新项目估算批处理作业的创建以支持执行多个子任务。 |
| 项目管理和会计 | [584519](https://fix.lcs.dynamics.com/Issue/Details/?bugId=584519) | 当工作流停滞在 **已取消** 状态时，时间表状态无法更新为 **草稿**。 |
| 项目管理和会计 | [584757](https://fix.lcs.dynamics.com/Issue/Details/?bugId=584757) | 如果存在多个行，则不会在贷项通知单发票方案中计算保留金额。 |
| 项目管理和会计 | [586034](https://fix.lcs.dynamics.com/Issue/Details/?bugId=586034) | 当您尝试更改采购订单中生成的发票上的金额时，会出现以下错误：“凭证上的交易未按照 XX/XX/XXXX 进行平衡。 （会计币种：0.00 - 申报币种：0.01）”。 |
| 项目管理和会计 | [588714](https://fix.lcs.dynamics.com/Issue/Details/?bugId=588714) | 由于与 **GeneralJournalAccountEntry** 联接，因此以批处理模式过帐项目发票方案时存在性能问题。 |
| 项目管理和会计 | [588851](https://fix.lcs.dynamics.com/Issue/Details/?bugId=588851) | 过帐时间表时存在性能问题。 |
| 项目管理和会计 | [590535](https://fix.lcs.dynamics.com/Issue/Details/?bugId=590535) | 展开所有任务或手动展开单个任务后，工作分解结构的成本估算层次结构未正确对齐。 |
| 项目管理和会计 | [593663](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593663) | 项目报价 Excel 模板无法添加到 **在 Excel 中打开** 菜单中。 |
| 项目管理和会计 | [596669](https://fix.lcs.dynamics.com/Issue/Details/?bugId=596669) | 法人的免税编号未包含在打印的项目发票上。 |
| 项目管理和会计 | [597563](https://fix.lcs.dynamics.com/Issue/Details/?bugId=597563) | 当相对于信用额度调整项目时出现“库存单位中未更新财务数据”错误。 |
| 项目管理和会计 | [598109](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598109) | 应用 KB 461935 后，如果切换到连续数字序列，则无法过帐估算值。 |
| 项目管理和会计 | [598688](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598688) | **TimeEntryDataManager** 导致 Android 版项目时间表移动应用停止响应。 |
| 项目管理和会计 | [602677](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602677) | 发票过帐中的 WIP 冲销值与时间条目中原始过帐 WIP 值不同。 |
| 项目管理和会计 | [602728](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602728) | 在已应用保留款案例中，过帐项目的发票收入时，凭证上的交易不平衡。 |
| 项目管理和会计 | [603320](https://fix.lcs.dynamics.com/Issue/Details/?bugId=603320) | 启用此 **启用项目资源计划性能增强** 功能后，会错误地四舍五入资源可用性和产能的小数值。 |
| 项目管理和会计 | [607324](https://fix.lcs.dynamics.com/Issue/Details/?bugId=607324) | 启用 **使用多个批处理任务创建项目估算** 功能后，在具有多个子任务的批处理中创建估算仅适用于当前期间。 |
| 出差和支出 | [551911](https://fix.lcs.dynamics.com/Issue/Details/?bugId=551911) | 一个旅行申请政策被忽略，但工作流却被正确批准。 |
| 出差和支出 | [563752](https://fix.lcs.dynamics.com/Issue/Details/?bugId=563752) | <p>移动支出应用不在支出行上保存以下信息：</p><ul><li>项目 ID</li><li>支出是否可计费</li><li>活动编号</li></ul> |
| 出差和支出 | [569458](https://fix.lcs.dynamics.com/Issue/Details/?bugId=569458) | 即使未将收据附加至支出行，**已附加收据** 字段仍被设置为 **是**。 |
| 出差和支出 | [571334](https://fix.lcs.dynamics.com/Issue/Details/?bugId=571334) | 将支出类别更改为 **个人** 时出现错误。 |
| 出差和支出 | [572783](https://fix.lcs.dynamics.com/Issue/Details/?bugId=572783) | 将信用卡交易拆分为个人支出后，您无法附加收据并编辑父项支出。 |
| 出差和支出 | [574252](https://fix.lcs.dynamics.com/Issue/Details/?bugId=574252) | 具有项目 ID 的内部公司交易的支出政策无法正常工作。 |
| 出差和支出 | [574489](https://fix.lcs.dynamics.com/Issue/Details/?bugId=574489) | 过帐的支出报表缺少过帐日期信息。 |
| 出差和支出 | [574504](https://fix.lcs.dynamics.com/Issue/Details/?bugId=574504) | 支出移动应用中存在付款方式问题。 |
| 出差和支出 | [584799](https://fix.lcs.dynamics.com/Issue/Details/?bugId=584799) | 为一名员工创建的出差申请可在委托日期之前用于另一名员工的支出报表。 |
| 出差和支出 | [586023](https://fix.lcs.dynamics.com/Issue/Details/?bugId=586023) | 创建支出时，不会在 **支出管理** 工作区中的会计分配级别正确更新对财务维度值所做的更改。 |
| 出差和支出 | [586081](https://fix.lcs.dynamics.com/Issue/Details/?bugId=586081) | 主要支出行审批状态与明细化行工作流审批状态不同步。 |
| 出差和支出 | [590544](https://fix.lcs.dynamics.com/Issue/Details/?bugId=590544) | 如果您过帐支出报表并启用退税，则会发生错误。 |
| 出差和支出 | [564851](https://fix.lcs.dynamics.com/Issue/Details/?bugId=564851) | 代理无法删除离职员工的支出单据。 |
| 出差和支出 | [587306](https://fix.lcs.dynamics.com/Issue/Details/?bugId=587306) | 删除支出行的时间比预期时间长，并且会影响性能。 |
| 出差和支出 | [600455](https://fix.lcs.dynamics.com/Issue/Details/?bugId=600455) | **TrvExpTrans** 因仅删除 **SourceDocumentLine** 而产生了孤立的 **TaxUncommitted** 记录。 |
| 出差和支出 | [609918](https://fix.lcs.dynamics.com/Issue/Details/?bugId=609918) | **ReleaseUpdateDB72_Expense.updateTrvExpTransProjTransId()** 未遵循 **trvExpTrans.ReferenceDataAreaId** 来创建新数字序列。 |

## <a name="regulatory-updates"></a>法规更新

有关财务和运营应用的监管更新的信息，请参阅[监管更新](/dynamics365/finance/localizations/regulatory-updates)。 您还可以登录 Microsoft Dynamics Lifecycle Services (LCS) 并使用问题搜索工具查看计划的监管更新。 利用问题搜索功能，您可以按国家/地区、功能类型和版本进行搜索。

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
