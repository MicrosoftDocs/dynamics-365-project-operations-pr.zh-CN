---
title: 2021 年 10 月适用于库存/生产订单场景的 Project Operations 新增功能或变更功能
description: 本主题提供有关 2021 年 10 月版适用于库存/生产订单场景的 Project Operations 中可用的质量更新的信息。
author: andchoi
ms.date: 11/17/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: andchoi
ms.openlocfilehash: 449cab5880c29cf110c9c5a266cbb4b102b5fc83
ms.sourcegitcommit: 2e4483d5b88213a9f33109f7adb989108521327d
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/17/2021
ms.locfileid: "7818463"
---
# <a name="whats-new-or-changed-in-project-operations-october-2021-for-stockedproduction-based-scenarios"></a>2021 年 10 月适用于库存/生产订单场景的 Project Operations 新增功能或变更功能

_**适用范围：** 适用于基于库存/生产场景的 Project Operations_

本主题适用于以下 Microsoft Dynamics 365 Project Operations 组件和版本：

- Dynamics 365 Finance 环境中的项目管理和会计版本 10.0.22
 
## <a name="quality-updates"></a>质量更新

| 功能区域 | 参考编号 | 质量更新 |
|--------------|------------------|----------------|
| 项目管理和会计 | [557017](https://fix.lcs.dynamics.com/Issue/Details/?bugId=557017) | 过帐内部公司客户发票时，未正确冲销项目在制品 (WIP) 和应计收入金额。 |
| 项目管理和会计 | [558232](https://fix.lcs.dynamics.com/Issue/Details/?bugId=558232) | **存在未结交易时防止项目关闭** 功能无法使用。 |
| 项目管理和会计 | [559271](https://fix.lcs.dynamics.com/Issue/Details/?bugId=559271) | 启用该功能时，普通发票上的计费分类不会自动填充项目维度。 |
| 项目管理和会计 | [574013](https://fix.lcs.dynamics.com/Issue/Details/?bugId=574013) | 在非内部公司方案中，过帐项目发票时，未正确冲销 WIP 和应计收入金额。 |
| 项目管理和会计 | [577857](https://fix.lcs.dynamics.com/Issue/Details/?bugId=577857) | 当 Microsoft Excel 加载项与项目支出日记帐一起使用，并且 **对方科目类型** 字段设置为 **项目** 时，会切换借方和贷方值。 |
| 项目管理和会计 | [577972](https://fix.lcs.dynamics.com/Issue/Details/?bugId=577972) | 项目交易中过帐的金额在项目采购订单上被高估，该采购订单包括库存物料并且在标记 **UseTax** 时具有不可扣除的税额。 |
| 项目管理和会计 | [581216](https://fix.lcs.dynamics.com/Issue/Details/?bugId=581216) | 系统会在项目损益报表和项目 WIP 报表之间拆分金额。 |
| 项目管理和会计 | [582065](https://fix.lcs.dynamics.com/Issue/Details/?bugId=582065) | 调整部分退回的物料要求后，现有库存不正确。 |
| 项目管理和会计 | [582682](https://fix.lcs.dynamics.com/Issue/Details/?bugId=582682) | 在 Microsoft Project 中编辑资源名称时，它们会在 Project Operations 中重复。 |
| 项目管理和会计 | [583873](https://fix.lcs.dynamics.com/Issue/Details/?bugId=583873) | 具有应付帐款内部公司待定供应商发票成本的内部公司支出报表会先过帐到 **项目 WIP 成本** 过帐类型。 不过，在处理过程中，估算相关成本会过帐到 **项目成本** 过帐类型，而不是预期的 **内部公司成本** 过帐类型。 |
| 项目管理和会计 | [584732](https://fix.lcs.dynamics.com/Issue/Details/?bugId=584732) | 项目支出交易中的供应商保留款结果未显示。 |
| 项目管理和会计 | [587453](https://fix.lcs.dynamics.com/Issue/Details/?bugId=587453) | 时间表必须将以交易货币为单位的交易金额四舍五入到所有会计分配和常规日记帐分配条目中指定的小数位数。 |
| 项目管理和会计 | [589409](https://fix.lcs.dynamics.com/Issue/Details/?bugId=589409) | 当确定计划订单时，会自动更新项目物料需求的数量。 |
| 项目管理和会计 | [590206](https://fix.lcs.dynamics.com/Issue/Details/?bugId=590206) | 无法对采购订单的预付款发票冲销凭证编号、交易类型供应商余额和帐号。 |
| 项目管理和会计 | [593068](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593068) | 当启用供应商发票集成时，内部公司供应商发票将损坏。 |
| 项目管理和会计 | [593335](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593335) | 创建项目支出日记帐时，成本金额会显示在 **贷方** 字段中。 |
| 项目管理和会计 | [593382](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593382) | 项目发票的付款条款无法按预期方式发挥作用。 |
| 项目管理和会计 | [593565](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593565) | 当数字序列设置为连续时，可能会重复使用时间表凭证。 |
| 项目管理和会计 | [593652](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593652) | 法国：**手动保留金额** 逻辑与项目合同发票方案中的 **自动保留金额** 逻辑不匹配。 |
| 项目管理和会计 | [596263](https://fix.lcs.dynamics.com/Issue/Details/?bugId=596263) | 在发布供应商保留后，凭证过帐有不正确的附加行。 |
| 项目管理和会计 | [596650](https://fix.lcs.dynamics.com/Issue/Details/?bugId=596650) | 更改 **创建发票方案** 页面上的 **发票日期** 字段时，可能会出现以下错误：“未将对象引用设置为对象的实例。” |
| 项目管理和会计 | [597679](https://fix.lcs.dynamics.com/Issue/Details/?bugId=597679) | 当您尝试审批 **TSLine** 工作流中的时间表时发生错误，并且有星期六和星期日的时间表策略。 |
| 项目管理和会计 | [597801](https://fix.lcs.dynamics.com/Issue/Details/?bugId=597801) | 计算发票方案的发票总额时，**发票方案交易汇总** 中不包括期初余额项目物料类型。 |
| 项目管理和会计 | [597886](https://fix.lcs.dynamics.com/Issue/Details/?bugId=597886) | 如果项目生产订单上的消耗成本为 0（零），则在您尝试估算时会出现以下错误：“已尝试除以零。” |
| 项目管理和会计 | [598706](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598706) | Android 版项目工时单移动应用停止响应。 此问题与 **TimeEntryDataManager ArgumentNullException** 相关。 |
| 项目管理和会计 | [598758](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598758) | Project Operations 集成日记帐在您过帐时失败，因为帐户缺少维度。 但是，缺少维度的帐户不是您要过帐到的帐户。 |
| 项目管理和会计 | [598929](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598929) | 从 **过帐成本** 页面上的 **选择** 对话框中删除搜索中的 **ToDate** 筛选器后，系统未清除此筛选器。 |
| 项目管理和会计 | [599757](https://fix.lcs.dynamics.com/Issue/Details/?bugId=599757) | 针对为 **仅时间** 类型的项目创建的时间表，**重置所有分配** 失败并显示一个错误。 |
| 项目管理和会计 | [602650](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602650) | 将采购类别分配给项目时，待定供应商发票上的 **项目** 选项卡不可编辑。 |
| 项目管理和会计 | [605121](https://fix.lcs.dynamics.com/Issue/Details/?bugId=605121) | 如果您未登录到 Project Operations Dataverse，则缺少导航窗格。 |
| 项目管理和会计 | [546467](https://fix.lcs.dynamics.com/Issue/Details/?bugId=546467) | 对于公司内部项目调整交易，目标公司中存在问题。 |
| 项目管理和会计 | [563579](https://fix.lcs.dynamics.com/Issue/Details/?bugId=563579) | 如果总帐中的 **采购订单年终流程** 处理了采购订单，则项目的承诺成本会计算错误的数量和成本价格。 |
| 项目管理和会计 | [581454](https://fix.lcs.dynamics.com/Issue/Details/?bugId=581454) | 当具有质检订单的项目生产订单报告为完成时出现以下错误：“没有与库存交易一起标记虚拟交易。” |
| 项目管理和会计 | [596408](https://fix.lcs.dynamics.com/Issue/Details/?bugId=596408) | 过帐与项目相关的应付帐款发票时出现以下错误：“枚举的文本项目 - 成本 - 物料不存在。” |
| 项目管理和会计 | [597237](https://fix.lcs.dynamics.com/Issue/Details/?bugId=597237) | 当您手动累积收入时，间接成本会翻倍。 |
| 项目管理和会计 | [601198](https://fix.lcs.dynamics.com/Issue/Details/?bugId=601198) | 应计收入和 WIP 过帐不产生交易。 |
| 项目管理和会计 | [602095](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602095) | 当收到的项目采购订单存在时，标准成本物料的待定价格激活失败。 |
| 项目管理和会计 | [602677](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602677) | 发票过帐中的 WIP 冲销值与时间条目中原始过帐 WIP 值不同。 |
| 项目管理和会计 | [602728](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602728) | 在凭证上的交易不平衡的应用保留款情况下，项目发票收入存在过帐问题。 |
| 项目管理和会计 | [603624](https://fix.lcs.dynamics.com/Issue/Details/?bugId=603624) | 在过帐发票方案后创建估算会在 Project Operations 中阻止导入更正行。 |
| 项目管理和会计 | [606083](https://fix.lcs.dynamics.com/Issue/Details/?bugId=606083) | 应该不能修改已完全开票的里程碑记录。 |
| 项目管理和会计 | [611389](https://fix.lcs.dynamics.com/Issue/Details/?bugId=611389) | 使用自动费用时，无法过帐时间表的公司内部客户发票，并且会显示错误消息。 |
| 项目管理和会计 | [612991](https://fix.lcs.dynamics.com/Issue/Details/?bugId=612991) | 未正确更新子项目的地址。 |
| 项目管理和会计 | [613418](https://fix.lcs.dynamics.com/Issue/Details/?bugId=613418) | 物料需求的成本价格随合并采购订单的采购价格一起更新。 |
| 项目管理和会计 | [614145](https://fix.lcs.dynamics.com/Issue/Details/?bugId=614145) | 更新采购价格并启用参数 **激活更改管理** 后，过帐的成本不正确。 |
| 出差和支出 | [575305](https://fix.lcs.dynamics.com/Issue/Details/?bugId=575305) | 当您在支出移动应用中搜索类别时，可以看到所有用户支出。 |
| 出差和支出 | [583101](https://fix.lcs.dynamics.com/Issue/Details/?bugId=583101) | 从信用卡交易创建的支出中过帐的供应商交易和销售税交易金额不正确。 |
| 出差和支出 | [583760](https://fix.lcs.dynamics.com/Issue/Details/?bugId=583760) | 刷新支出报表页面时会显示一条不相关的警告消息。 |
| 出差和支出 | [598656](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598656) | 在删除临时审批者，然后通过工作流重新提交时，使用了错误的临时审批者。 |
| 出差和支出 | [612742](https://fix.lcs.dynamics.com/Issue/Details/?bugId=612742) | 发生与里程设置相关的过帐错误。 |
| 出差和支出 | [620773](https://fix.lcs.dynamics.com/Issue/Details/?bugId=620773) | 将未附加的交易重新添加到公司内部支出的支出报表时，分配不更新法人。 |

### <a name="regulatory-updates"></a>法规更新

有关 Finance and Operations 应用的法规更新的信息，请参阅[法规更新](/dynamics365/finance/localizations/regulatory-updates)。 您还可以登录 Microsoft Dynamics Lifecycle Services (LCS) 并使用问题搜索工具查看计划的监管更新。 利用问题搜索功能，您可以按国家/地区、功能类型和版本进行搜索。

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
