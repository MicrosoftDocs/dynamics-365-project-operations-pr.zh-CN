---
title: 2022 年 2 月新增功能 - 基于资源/非库存场景的 Project Operations
description: 本主题提供有关 2022 年 2 月版基于资源/非库存场景的 Project Operations 中可用的质量更新的信息。
author: sigitac
ms.date: 01/27/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 76ae00517c857415c89d7a03f421686dad28da93
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/14/2022
ms.locfileid: "8600823"
---
# <a name="whats-new-february-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>2022 年 2 月新增功能 - 基于资源/非库存场景的 Project Operations

*适用范围：适用于基于资源/非库存场景的 Project Operations*

本主题适用于以下 Microsoft Dynamics 365 Project Operations 组件和版本：

- Dataverse 环境中的 Project Operations 版本 4.28.0.120
- Dynamics 365 Finance 环境中的项目管理和会计版本 10.0.24

## <a name="features-included-in-this-release"></a>此版本中包括的功能

- 在此版本开始，您最多可以将 300 个团队成员添加到单个项目中。 之前，对团队成员数量的限制是 150。 有关详细信息，请参阅[项目限制](../project-management/create-wbs.md#project-limitations)。

## <a name="project-operations-dual-write-map-updates"></a>Project Operations 双写入映射更新

下表列出了在 Project Operations 2022 年 2 月版中修改或添加的双写入映射。

| 实体映射 | 更新版本 | 注释  |
| --- | --- | --- |
| Project Operations 集成项目支出导出实体 (msdyn\_expenses) | 1.0.0.3 | 将项目活动同步扩展到 Dataverse。 |

有关 Project Operations 双写入映射的当前列表和版本，请参阅 [Project Operations 双写入映射版本](../environment/resource-dual-write-maps.md)。

当更新 Project Operations Dataverse 解决方案和 Finance 解决方案版本时，始终运行您环境中的最新映射版本并启用所有相关表映射。 如果未激活映射的最新版本，某些特性和功能可能无法正常运行。 您可以在 **双重写入** 页的 **版本** 列中查看映射的活动版本。 要激活映射的新版本，请选择 **表映射版本**，选择最新版本，然后保存所选版本。 如果您已经自定义了现成的表映射，请重新应用更改。 有关详细信息，请参阅[应用程序生命周期管理](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management)。

如果您在启动映射时遇到问题，请按照双写入故障排除指南的[映射中缺少表列问题](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps)部分中的说明进行操作。

## <a name="quality-updates"></a>质量更新

### <a name="project-operations-on-dataverse"></a>Dataverse 上的 Project Operations

| 功能区域 | 参考编号 | 质量更新 |
| --- | --- | --- |
| 计费和定价 | 2415109 | **运营付款条款** 字段中的默认值必须是项目合同客户记录和估价发票记录。 |
| 计费和定价 | 2497369 | 材料更正必须遵从 **更正** 参数中的日期值。 |
| 计费和定价 | 2498697 | 改进了 **时间条目撤消** 的安全配置。 |
| 计费和定价 | 2513824 | 对于基于资源的场景，Project Operations 中的交易类别 ID 不能超过 28 个字符。 |
| 计费和定价 | 2517455 | 不允许 **刷新发票明细交易** 操作针对同一个发票同时触发多次。 |
| 计费和定价 | 2517465 | **停用发票明细详细信息** 操作由于不受支持被阻止。 |
| 计费和定价 | 2556660 | 修复了对附加到项目参数记录的价目表进行的时效检查。 |
|   商机管理 | 2369202 | 更正了验证具有重叠生效日期的价目表能否附加到同一项目合同的业务逻辑。 |
|   商机管理 | 2385965 | 更正了选择 **保存并关闭** 时 **项目合同** 页面的 **客户** 选项卡上的行为。 |
| 时间和支出 | 2538503 | 过帐支出报表后，项目任务必须在 **项目实际值** 实体中可用。 |

### <a name="project-management-and-accounting-on-dynamics-365-finance"></a>Dynamics 365 Finance 中的项目管理和会计

| 功能区域 | 参考编号 | 质量更新 |
| --- | --- | --- |
| 项目管理和会计 | [615496](https://fix.lcs.dynamics.com/Issue/Details/?bugId=615496) | 在导入供应商贷方通知单期间，发生错误。 错误消息指出“保留金额不能超过剩余净金额。” |
| 项目管理和会计 | [619391](https://fix.lcs.dynamics.com/Issue/Details/?bugId=619391) | 如果发票方案包含任何属于未记帐实际销售额的零金额费用交易，则不能开票。 |
| 项目管理和会计 | [624423](https://fix.lcs.dynamics.com/Issue/Details/?bugId=624423) | 更新采购价格并启用 **激活更改管理** 后，过帐的成本不正确。|
| 项目管理和会计 | [628386](https://fix.lcs.dynamics.com/Issue/Details/?bugId=628386) | 固定价格项目的过帐估算在估算凭证中使用了不正确的货币和金额，即使在启用了 **启用项目合同货币以进行估算计算** 功能时。 |
| 项目管理和会计 | [629239](https://fix.lcs.dynamics.com/Issue/Details/?bugId=629239) | **ProjDMFDataPopulation\_Extension** 不应调用来启用更改跟踪而不捕捉具有未启用的配置键的实体的异常。 |
| 项目管理和会计 | [623818](https://fix.lcs.dynamics.com/Issue/Details/?bugId=623818) | 过帐多个高级日记帐并发生错误时的批处理作业已修复。 |
| 出差和支出 | [616805](https://fix.lcs.dynamics.com/Issue/Details/?bugId=616805) | 由于存在与支出报表中的预付现金有关的结算问题，税额不包括在预付现金中。 |
| 出差和支出 | [616959](https://fix.lcs.dynamics.com/Issue/Details/?bugId=616959) | **支出 - 已过帐交易** 报表中不包含销售税信息。 |
| 出差和支出 | [618943](https://fix.lcs.dynamics.com/Issue/Details/?bugId=618943) | 违反 **需要收据** 支出政策时在支出报表中错误地显示警告。 |
| 出差和支出 | [633470](https://fix.lcs.dynamics.com/Issue/Details/?bugId=633470) | 当交易是里程支出的结果时，项目交易在总销售额中不包括非抵扣销售税。 |
| 出差和支出 | [642979](https://fix.lcs.dynamics.com/Issue/Details/?bugId=642979) | 当明细化行包含税时，您无法更改明细化行日期，并会出现源文档状态错误。 |

## <a name="removed-and-deprecated-features"></a>已删除和弃用的功能

[Project Operations 中已删除或弃用的功能](removed-depreciated-features-project.md)主题描述了 Dynamics 365 Project Operations 已删除或弃用的功能。

- 已删除的功能在产品中已不再可用。
- 已弃用的功能在活跃的开发中不存在，而且在将来的更新中可能被移除。

在从产品中删除任何功能之前的 12 个月，[Project Operations 中已删除或弃用的功能](removed-depreciated-features-project.md)主题中会显示弃用公告。

对于仅影响编译时，但是与沙盒和生产环境二进制兼容的突发更改，弃用时间将低于 12 个月。 通常，这些更改是必须对编译器进行的功能更新。
