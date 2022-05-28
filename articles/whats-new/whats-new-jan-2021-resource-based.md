---
title: 2021 年 1 月新增功能 - 面向资源/非库存场景的 Project Operations
description: 此主题提供有关 2021 年 1 月版本的面向资源/非库存场景的 Project Operations 中推出的质量更新的信息。
author: sigitac
ms.date: 01/13/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 50874d771afe03b08bd95b670f7095bc2d61509d
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/14/2022
ms.locfileid: "8599535"
---
# <a name="whats-new-january-2021---project-operations-for-resourcenon-stocked-based-scenarios"></a>2021 年 1 月新增功能 - 面向资源/非库存场景的 Project Operations

_**适用于：** 面向资源/非库存场景的 Project Operations_


此主题适用于以下 Dynamics 365 Project Operations 组件和版本：

  - Dataverse 环境中的 Project Operations 版本 4.6.0.154
  - Dynamics 365 Finance 环境中的项目管理和会计版本 10.0.16

## <a name="quality-updates"></a>质量更新

### <a name="project-operations-on-dataverse"></a>Dataverse 上的 Project Operations

| **功能区域** | **参考编号** | **质量更新** |
| --- | --- | --- |
| **部署和配置** | 2106818 | 修复了导致与自定义页面相关的问题的 webresource 重命名。 |
| **记帐和定价** | 2091908 | 修复了在与 Dynamics 365 Field Service 一起安装 Project Operations 时，**发票** 页上的 **锁定定价** 和 **使用当前定价** 选项的可见性问题。 |
| **记帐和定价** | 2103058 | 刷新了 **项目总计** 以处理任务中实际成本的 null 值。 |
| **记帐和定价** | 2116100 | 改进了用于功能 **更正实际值的输入** 的错误消息。 |
| **记帐和定价** | 2116129 | 改进了 **项目** 页上 **估算** 选项卡上的支出估算可见性。 |
| **记帐和定价** | 2119112 | 修复了使用不同汇率时实际销售额和实际成本的聚合问题。 |
| **记帐和定价** | 2134705 | 修复了打开 **发票** 页和安装 Field Service 时出现的错误“无法读取未定义的 **getResourceString** 属性”。 |
| **商机管理** | 2022195 | **项目** 页上基于任务的记帐网格包括一个图标，指示存在链接到该任务的合同子项或报价单明细。 |
| **商机管理** | 2029135 | 修复了用户尝试在为预付款金额开具的已确认发票上打开发票明细时发生的业务流程错误。 |
| **商机管理** | 2040713 | 修复了从合同创建发票和安装 Field Service 时发生的脚本错误。 |
| **项目规划和跟踪** | 2090202 | 将不再使用的业务规则标记为 **弃用**。 |
| **时间和支出** | 2091249 | 加强了控件，让用户无法在已提交或已批准的时间条目上更改任务。 |

### <a name="project-management-and-accounting-in-dynamics-365-finance"></a>Dynamics 365 Finance 中的项目管理和会计

| **功能区域** | **参考编号** | **质量更新** |
| --- | --- | --- |
| **项目管理和会计** | [478667](https://fix.lcs.dynamics.com/Issue/Details/?bugId=478667) | 具有多个资金来源的固定价格项目在 **记帐** 页上的合同金额不正确。 |
| **项目管理和会计** | [480260](https://fix.lcs.dynamics.com/Issue/Details/?bugId=480260) | **Invoiceproposal.PSAnfRefProjId** 占位符未显示工作流 **查看项目发票方案** 的项目 ID。 |
| **项目管理和会计** | [481227](https://fix.lcs.dynamics.com/Issue/Details/?bugId=481227) | 发布项目发票方案时使用了错误的现金折扣日期。 |
| **项目管理和会计** | [482558](https://fix.lcs.dynamics.com/Issue/Details/?bugId=482558) | 在 Project Operations 中删除和读取资源分配会将 Finance 中的项目预测条目加倍。 |
| **项目管理和会计** | [484468](https://fix.lcs.dynamics.com/Issue/Details/?bugId=484468) | 在 Project Operations 中，如果项目上没有合同子项，您无法在 Dataverse 中创建项目估算。 |
| **项目管理和会计** | [485871](https://fix.lcs.dynamics.com/Issue/Details/?bugId=485871) | 当成本过帐到余额时，项目支出交易的财务维度与相关凭证和支出报表的会计分配不同步。 |
| **项目管理和会计** | [488382](https://fix.lcs.dynamics.com/Issue/Details/?bugId=488382) | 固定价格项目的已过帐项目交易中的 **发票状态** 筛选器不起作用。 |
| **项目管理和会计** | [491941](https://fix.lcs.dynamics.com/Issue/Details/?bugId=491941) | 冲销估算消除在 **定期** 部分不起作用。 |
| **项目管理和会计** | [509989](https://fix.lcs.dynamics.com/Issue/Details/?bugId=509989) | 与 Dataverse 集成后，可以在 Project Operations 中删除发票方案行。 |
| **项目管理和会计** | [510041](https://fix.lcs.dynamics.com/Issue/Details/?bugId=510041) | 在没有 Dataverse 集成的情况下阻止启用多个合同子项功能。 |
| **项目管理和会计** | [510527](https://fix.lcs.dynamics.com/Issue/Details/?bugId=510527) | 当记帐开票等于损益时，已开票收入在“估算”页上列出时为零。 |
| **项目管理和会计** | [514167](https://fix.lcs.dynamics.com/Issue/Details/?bugId=514167) | 发票更正在集成环境中不工作。 |
| **项目管理和会计** | [514364](https://fix.lcs.dynamics.com/Issue/Details/?bugId=514364) | 在内部公司项目开票中发布 WIP - 销售值时，选择了错误帐户。 |
| **项目管理和会计** | [514385](https://fix.lcs.dynamics.com/Issue/Details/?bugId=514385) | 在 Project Operations 中，无法更新 Dataverse 中估算任务的依赖关系。 |
| **项目管理和会计** | [515258](https://fix.lcs.dynamics.com/Issue/Details/?bugId=515258) | 在 Finance 中反复删除 Project Operations 集成日记帐导致数据丢失。 |
| **项目管理和会计** | [519716](https://fix.lcs.dynamics.com/Issue/Details/?bugId=519716) | 发布项目发票方案时发生以下错误：“加回已扣除的预付款发票时，交易未对报告货币进行平衡”。 |
| **项目管理和会计** | [521807](https://fix.lcs.dynamics.com/Issue/Details/?bugId=521807) | 在 Project Operations 中更新默认项目合同后，扣减中包含错误的项目 ID。 |
| **项目管理和会计** | [522799](https://fix.lcs.dynamics.com/Issue/Details/?bugId=522799) | 启用 Project Operations 后，无法完成估算和收入确认。 |
| **项目管理和会计** | [527319](https://fix.lcs.dynamics.com/Issue/Details/?bugId=527319) | 在 Project Operations 中，从合同中删除项目不重置合同上的默认项目。 |
| **项目管理和会计** | [528212](https://fix.lcs.dynamics.com/Issue/Details/?bugId=528212) | 在 Project Operations 中，在内部公司发票上，错误的支出行显示在 **添加行** 列表中。 |
| **出差和支出** | [515334](https://fix.lcs.dynamics.com/Issue/Details/?bugId=515334) | 由于合同子项缺少时间设置，无法发布支出行。 |
| **出差和支出** | [437673](https://fix.lcs.dynamics.com/Issue/Details/?bugId=437673) | 当必须进行项目/类别验证时，与项目相关联的支出类别在支出报表中看不到。 |
| **出差和支出** | [441256](https://fix.lcs.dynamics.com/Issue/Details/?bugId=441256) | 按行发布支出报表时，预付现金余额未更新。 |
| **出差和支出** | [465396](https://fix.lcs.dynamics.com/Issue/Details/?bugId=465396) | 冲销使用两个或多个付款交易结算发票的结算后，**更新付款信息** 作业失败。 |
| **出差和支出** | [472892](https://fix.lcs.dynamics.com/Issue/Details/?bugId=472892) | 每日支出类别的最后一日餐饮减少量的计算存在问题。 |
| **出差和支出** | [477714](https://fix.lcs.dynamics.com/Issue/Details/?bugId=477714) | 如果用户的第一个连接使用 es-MX 语言，**每个员工的支出类型** 报表不会显示分项支出。 |
| **出差和支出** | [487516](https://fix.lcs.dynamics.com/Issue/Details/?bugId=487516) | 支出报表发票的供应商付款使用了错误的摘要帐户进行结算过账。 |
| **出差和支出** | [487531](https://fix.lcs.dynamics.com/Issue/Details/?bugId=487531) | 当支出报表过帐时启用了 **允许根据抵销付款帐户对交易进行分组** 和 **过帐时更正会计日期**，会计日期不会在 **会计分配** 表中分组，这会影响销售税记录。 |
| **出差和支出** | [488292](https://fix.lcs.dynamics.com/Issue/Details/?bugId=488292) | 当清除“在支出中使用”复选框，然后再次选中时，支出子类别映射被删除。 |
| **出差和支出** | [506175](https://fix.lcs.dynamics.com/Issue/Details/?bugId=506175) | 如果在标头级别添加了项目 ID，则无法创建内部公司支出报表。 |
| **出差和支出** | [509491](https://fix.lcs.dynamics.com/Issue/Details/?bugId=509491) | 支出金额超过预付现金金额时的支出付款存在问题。 |
| **出差和支出** | [509556](https://fix.lcs.dynamics.com/Issue/Details/?bugId=509556) | 如果将用户角色分派给特定组织，内部公司支出报表中的 **项目 ID** 字段为空。 |
| **出差和支出** | [518186](https://fix.lcs.dynamics.com/Issue/Details/?bugId=518186) | 添加新支出行时，支出类别被锁定。 |
| **出差和支出** | [520914](https://fix.lcs.dynamics.com/Issue/Details/?bugId=520914) | 已拆分的分项支出报表行导致发布的应付帐款\总帐凭证不完整。 由于 **TRVEXPTRANS.SOURCEDOCUMENTLINE** 重复，会计源资源管理器也被损坏。 |
| **出差和支出** | [521768](https://fix.lcs.dynamics.com/Issue/Details/?bugId=521768) | 在客户有重复项的 **TRVREQUISITIONLINE** 表上添加的索引导致升级过程中出错。 |
| **出差和支出** | [525106](https://fix.lcs.dynamics.com/Issue/Details/?bugId=525106) | 在 Project Operations 中，无法创建或审批 Dataverse 中内部公司任务的时间。 |

## <a name="regulatory-updates"></a>法规更新

有关财务和运营应用的监管更新的信息，请参阅[监管更新](/dynamics365/finance/localizations/regulatory-updates)。 您还可以登录到 LCS，使用问题搜索工具查看计划的法规更新。 通过问题搜索，您可以按国家/地区、功能类型和发布进行搜索。


[!INCLUDE[footer-include](../includes/footer-banner.md)]