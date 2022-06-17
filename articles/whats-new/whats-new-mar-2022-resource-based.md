---
title: 2022 年 3 月新增功能 - 基于资源/非库存场景的 Project Operations
description: 本文提供有关 2022 年 3 月版基于资源/非库存场景的 Project Operations 中可用的质量更新的信息。
author: sigitac
ms.date: 03/31/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 986d0652ed502873085259fef5ad40aba99c278d
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8910895"
---
# <a name="whats-new-march-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>2022 年 3 月新增功能 - 基于资源/非库存场景的 Project Operations

*适用范围：适用于基于资源/非库存场景的 Project Operations*

本文适用于以下 Microsoft Dynamics 365 Project Operations 组件和版本：

- Dataverse 环境中的 Project Operations 版本 4.30.0.99
- Dynamics 365 Finance 环境中的项目管理和会计版本 10.0.25

## <a name="features-included-in-this-release"></a>此版本中包括的功能

新的重构的现代支出工作区现在支持每日津贴。 使用每日津贴的公司可以启用此功能，为用户提供一种简单的方式来提交和报销每日津贴支出。 有关详细信息，请参阅[每日津贴支出](../expense/per-diem-expenses.md)。

## <a name="project-operations-dual-write-maps-updates"></a>Project Operations 双重写入映射更新

下表列出了在 Project Operations 2022 年 3 月版中修改或添加的双写入映射。

| **实体映射** | **更新版本** | **注释** |
| --- | --- | --- |
| Project Operations 集成项目供应商发票明细导出实体 msdyn\_projectvendorinvoicelines | 1.0.0.3 | 映射已更新为与 Dataverse 中的供应商发票明细实体保持一致。 <br>请勿激活映射版本 1.0.0.4。 它将在下一次每月更新中与 Finance 环境版本 10.0.26 结合使用。 |

当更新 Project Operations Dataverse 解决方案和 Finance 解决方案版本时，始终运行您环境中的最新映射版本并启用所有相关表映射。 如果未激活映射的最新版本，某些特性和功能可能无法正常运行。 您可以在 **双重写入** 页的 **版本** 列中查看映射的活动版本。 要激活映射的新版本，请选择 **表映射版本**，选择最新版本，然后保存所选版本。 如果您已经自定义了现成的表映射，请重新应用更改。 有关详细信息，请参阅[应用程序生命周期管理](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management)。

如果您在启动映射时遇到问题，请按照双重写入故障排除指南的[映射中缺少表列问题](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps)部分中的说明进行操作。

## <a name="quality-updates"></a>质量更新

### <a name="project-operations-on-dataverse"></a>Dataverse 上的 Project Operations

| 功能区域 | 参考编号 | 质量更新 |
| --- | --- | --- |
| 时间和支出 | 2388011 | 在批量审批期间向时间条目提交者显示拒绝注释。 |
| 项目规划和跟踪 | 2495294 | **任务详细信息** 页面上的项目详细信息不能进行编辑。 |
| 计费和定价 | 2499605 | 从报价单里程碑创建的合同里程碑被错误地标记为只读。 |
| 项目规划和跟踪 | 2506050 | 如果没有要保存的更改，操作集会保持待定状态一小时。 然后集被错误地标记为 **失败**，而它应该立即完成。 |
| 计费和定价 | 2507401 | 由于缓存不正确，错误地在项目中输入了默认合同签订部门。 |
| 计费和定价 | 2541660 | 双写入中的 **销售订单创建验证** 应仅适用于基于项目的订单。 |
| 计费和定价 | 2552745 | 税款在设置了拆分记帐规则的客户之间不拆分。 |
| 计费和定价 | 2558859 | 改进了设置定价维度时的错误消息。 |
| 计费和定价 | 2558933 | 当 **msdyn\_project** 添加为定价维度时，**从项目估算导入** 失败。 |
| 计费和定价 | 2559101 | 项目参数删除不会被阻止并导致问题。 |
|   商机管理 | 2570390 | 双写入插件强制报价单、订单和商机上的客户类型为 **客户**，即使该客户类型不正确。 |
| 计费和定价 | 2586097 | 从项目合同子项中删除项目时，不会冲销拆分的已记帐实际成本。 |
| 计费和定价 | 2589619 | 目录外材料的税款会传播到未记帐实际销售额和发票。 |
|   商机管理 | 2594015 | 对于具有 **Net60** 付款条款的客户，报价单不能作为赢单结束。 |
| 项目规划和跟踪 | 2595841 | 在 Project for the Web 中，用户在创建新资源请求时会收到关于缺少的 **msdyn\_actualstart** 的错误消息。 |
| 时间和支出 | 2602511 | 时间条目的 **拒绝者** 字段显示 **系统** 而不是指定用户为拒绝者。 |
| 时间和支出 | 2602528 | 项目审批者可以批准其未被列为审批者的项目的时间。 |
| 计费和定价 | 2608550 | 即使原始发票没有更改，也可以确认更正发票。 |

### <a name="project-management-and-accounting-on-dynamics-365-finance"></a>Dynamics 365 Finance 中的项目管理和会计

| 功能区域 | 参考编号 | 质量更新 |
| --- | --- | --- |
| 项目管理和会计 | [606759](https://fix.lcs.dynamics.com/Issue/Details/?bugId=606759) | **类别 ID** 字段的允许长度在 Finance 和 Project Operations 之间不匹配。 |
| 项目管理和会计 | [617806](https://fix.lcs.dynamics.com/Issue/Details/?bugId=617806) | 当 **记帐开票** 字段设置为 **损益** 并使用 **完成百分比** 原则时，固定价格项目无法取消。 |
| 项目管理和会计 | [620979](https://fix.lcs.dynamics.com/Issue/Details/?bugId=620979) | 在 Project Operations 集成日记帐的支出行的项目设置中输入了不正确的默认销售税组。 |
| 项目管理和会计 | [623014](https://fix.lcs.dynamics.com/Issue/Details/?bugId=623014) | 您无法在与 Project Operations 的集成部署中编辑项目发票方案标题维度。 |
| 项目管理和会计 | [624283](https://fix.lcs.dynamics.com/Issue/Details/?bugId=624283) | 内部公司供应商发票不能与 Dataverse 集成。 |
| 项目管理和会计 | [634156](https://fix.lcs.dynamics.com/Issue/Details/?bugId=634156) | 客户余额货币与报告货币存在不匹配的情况。 |
| 项目管理和会计 | [641612](https://fix.lcs.dynamics.com/Issue/Details/?bugId=641612) | 即使客户的所有发票都暂停，您也可以过帐项目发票。 |
| 项目管理和会计 | [642945](https://fix.lcs.dynamics.com/Issue/Details/?bugId=642945) | 具有 **标题** 和 **行** 视图的项目发票方案中缺少 **删除所有行** 按钮。 |
| 项目管理和会计 | [637760](https://fix.lcs.dynamics.com/Issue/Details/?bugId=637760) | 过帐供应商发票时，出现以下错误：“发票的会计日期必须与相关采购订单在同一会计年度。 请运行采购订单年终处理或将日期更改为当前会计年度。” |
| 出差和支出 | [604128](https://fix.lcs.dynamics.com/Issue/Details/?bugId=604128) | 发布出差申请的承诺成本后，未发布项目的承诺成本。 |
| 出差和支出 | [620803](https://fix.lcs.dynamics.com/Issue/Details/?bugId=620803) | 提交支出报表时出现以下错误：“堆栈跟踪：公司不存在。” |
| 出差和支出 | [622465](https://fix.lcs.dynamics.com/Issue/Details/?bugId=622465) | 当在项目上选择 **Require activity for journal** 参数时，不会在支出报表中输入默认的 **项目 ID**。 |
| 出差和支出 | [626781](https://fix.lcs.dynamics.com/Issue/Details/?bugId=626781) | **过帐支出** 按钮在资源/非库存场景的 Project Operations 中无法正常工作。 |
| 出差和支出 | [635348](https://fix.lcs.dynamics.com/Issue/Details/?bugId=635348) | 包含乘客的里程支出报表的 **每英里费率** 有问题。 |
| 出差和支出 | [638019](https://fix.lcs.dynamics.com/Issue/Details/?bugId=638019) | 在 **里程费率层** 支出类别中使用两种不同的车辆类型时，员工的支出里程费率未正确加总。 |
| 出差和支出 | [641272](https://fix.lcs.dynamics.com/Issue/Details/?bugId=641272) | 对出差申请行上的 **项目** 字段的查找未返回正确的项目列表。 |
| 出差和支出 | [645905](https://fix.lcs.dynamics.com/Issue/Details/?bugId=645905) | **正在审核的里程** 在支出报表中显示警告。 |
| 出差和支出 | [647819](https://fix.lcs.dynamics.com/Issue/Details/?bugId=647819) | 支出 OCR 服务的 URL 存在问题，收据光学字符识别 (OCR) 服务无法正常工作。 |
| 出差和支出 | [648684](https://fix.lcs.dynamics.com/Issue/Details/?bugId=648684) | 启用 **能够快速列出经常性支出明细** 功能后，每次打开 **列出明细** 页面时，支出报表上明细化行上的金额都会改变金额。 |
| 出差和支出 | [651899](https://fix.lcs.dynamics.com/Issue/Details/?bugId=651899) | 当临时列表有多个审批者时，您不能删除支出报表。 |

## <a name="removed-and-deprecated-features"></a>已删除和弃用的功能

[Project Operations 中已删除或弃用的功能](removed-depreciated-features-project.md)一文描述了 Dynamics 365 Project Operations 已删除或弃用的功能。

- 已删除的功能在产品中已不再可用。
- 已弃用的功能在活跃的开发中不存在，而且在将来的更新中可能被移除。

在从产品中删除任何功能之前的 12 个月，[Project Operations 中已删除或弃用的功能](removed-depreciated-features-project.md)一文中会显示弃用公告。

对于仅影响编译时，但是与沙盒和生产环境二进制兼容的突发更改，弃用时间将低于 12 个月。 通常，这些更改是必须对编译器进行的功能更新。
