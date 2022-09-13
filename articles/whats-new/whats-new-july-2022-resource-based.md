---
title: 2022 年 7 月新增功能 - 基于资源/非库存场景的 Project Operations
description: 本文提供有关 2022 年 7 月版基于资源/非库存场景的 Microsoft Dynamics 365 Project Operations 中可用的质量更新的信息。
author: ramagadu
ms.date: 07/19/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: ramagadu
ms.openlocfilehash: e63b29741dbaa400a2176ff8b4c35c6d64dfeab4
ms.sourcegitcommit: 7ed8e77a92917f2d242988ca02bd7de9571cce5e
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/02/2022
ms.locfileid: "9403940"
---
# <a name="whats-new-july-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>2022 年 7 月新增功能 - 基于资源/非库存场景的 Project Operations

_**适用于：** 面向资源/非库存场景的 Project Operations_

本文适用于以下 Microsoft Dynamics 365 Project Operations 组件和版本：

- Dataverse 环境中的 Project Operations 版本 4.44.0.22
- Dynamics 365 Finance 环境中的项目管理和会计版本 10.0.28

## <a name="project-operations-dual-write-maps-updates"></a>Project Operations 双重写入映射更新

此版本中没有对 Project Operations 双重写入映射的更新。 有关 Project Operations 双重写入映射的当前列表和版本，请参阅 [Project Operations 双重写入映射版本](../environment/resource-dual-write-maps.md)。

当更新 Project Operations Dataverse 解决方案和 Finance 解决方案版本时，始终运行您环境中的最新映射版本并启用所有相关表映射。 如果未激活映射的最新版本，某些特性和功能可能无法正常运行。 您可以在 **双重写入** 页的 **版本** 列中查看映射的活动版本。 要激活映射的新版本，请选择 **表映射版本**，选择最新版本，然后保存所选版本。 如果您已经自定义了现成的表映射，请重新应用更改。 有关详细信息，请参阅[应用程序生命周期管理](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management)。

如果您在启动映射时遇到问题，请按照双重写入故障排除指南的[映射中缺少表列问题](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps)部分中的说明进行操作。

## <a name="quality-updates"></a>质量更新

### <a name="project-operations-on-dataverse"></a>Dataverse 上的 Project Operations

| 功能区域 | 参考编号 | 质量更新 |
| --- | --- | --- |
| 部署和配置 | 2761472 | 已处理 Project Operations 安装错误。 |
| 计费和定价 | 2746940 | 分包合同子项名称的最大长度应为 100 个字符。 |
| 计费和定价 | 2739162 | 客户必须能够在实际网格视图中看到功能区按钮。 |
| 项目规划和跟踪 | 2730318 | 更新了项目主题中不受支持的字符的验证。 |
| 计费和定价 | 2705361 | 里程碑开票销售实际值必须包含在项目跟踪字段中。 |
| 计费和定价 | 2675880 | 防止项目链接到不基于工作的合同子项。 |
| 计费和定价 | 2664396 | 如果保存的报价单价目表没有报价，则一定会有一个错误指出报价不能为空。 |
| 计费和定价 | 2184019 | 对于没有支持合同或报价的项目，不应显示 **基于任务的计费** 选项卡。 |
| 时间和支出 | 2754459 | 当定期的计划云端流处于停用状态时，显示横幅并绕过异步处理。 |
| 计费和定价 | 2724391 | 当项目合同拆分计费规则缺少客户值时，会引发错误异常。 |
| 计费和定价 | 2708638 | 在“材料使用”和“材料使用审批”中使用网格搜索进行搜索时未找到记录。|
| 计费和定价 | 2686977 | 在创建发票期间阻止验证发票行。 |
| 计费和定价 | 2683032 | 应计费角色和类别的复制不能扩大到 5000 条记录以上。|
| 计费和定价 | 2673363 | 当项目的工作量和支出估算值和实际值都存在时，项目的成本消耗百分比将出错。 |

### <a name="project-management-and-accounting-in-finance"></a>Finance 中的项目管理和会计

有关此更新中包含的缺陷修复的信息，请登录 Microsoft Dynamics Lifecycle Services (LCS)，然后查看[知识库文章](https://fix.lcs.dynamics.com/Issue/Details?bugId=694438)。

## <a name="features-turned-on-by-default-in-upcoming-release"></a>即将发布的版本中默认启用的功能

下表列出了版本 10.0.29 中默认启用的功能。 大多数自动启用的功能都可以在[功能管理](/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview)中关闭。 将来，某些已自动开启的功能可能会从功能管理中移除并成为强制性功能。 此更改可确保客户使用当前功能，以便在添加时可以在当前功能的基础上生成增强功能。 永远不会在不到一年的时间内自动启用功能，除非确定它们是必不可少的功能。

| 功能名称 | 启用日期 | 功能添加时间 | 功能状态 | 模块 |
| --- | --- | --- |--- |--- |
| 允许根据资金规则分配的变化调整小时交易 | 2022 年 9 月 16 日 | 2020 年 10 月 7 日 | 默认打开 | 项目管理和会计 |
| 项目采购订单预付款发票冲销功能 | 2022 年 9 月 16 日 | 2021 年 10 月 6 日 | 默认打开 | 项目管理和会计 |
| 将 Project Operations 用于基于资源的方案/非库存方案时删除发票方案行 | 2022 年 9 月 16 日 | 2021 年 10 月 6 日 | 默认打开 | 项目管理和会计 |
| 调整已过帐项目交易的会计 | 2022 年 9 月 16 日 | 2020 年 5 月 10 日 | 默认打开 | 项目管理和会计 |
| 为项目启用默认会计设置 | 2022 年 9 月 16 日 | 2020 年 2 月 19 日 | 默认打开 | 项目管理和会计 |
| 为项目启用多个合同子项 | 2022 年 9 月 16 日 | 2020 年 6 月 29 日 | 默认打开 | 项目管理和会计 |
| 如果当前审批状态不允许编辑，将项目小时日记帐设置为只读 | 2022 年 9 月 16 日 | 2021 年 10 月 6 日 | 默认打开 | 项目管理和会计 |
| 更新采购行并打开采购订单更改管理参数时，从采购行同步销售行 | 2022 年 9 月 16 日 | 2020 年 10 月 7 日 | 默认打开 | 项目管理和会计 |
| 启用 Dynamics 365 Customer Engagement 上的 Project Operations | 2022 年 9 月 16 日 | 2020 年 6 月 29 日 | 默认打开 | 项目管理和会计 |
| 项目交易冲销更正功能 | 2022 年 9 月 16 日 | 2020 年 7 月 13 日 | 默认打开 | 项目管理和会计 |

## <a name="features-that-become-mandatory-in-the-upcoming-release"></a>即将发布的版本中必备的功能

下表列出了从版本 10.0.29 以后必须具备的功能。

| 功能名称 | 启用日期 | 功能添加时间 | 功能状态 | 模块 |
| --- | --- | --- | --- | --- |
| 在不四舍五入汇率的情况下计算资金来源的承诺值 | 2022 年 9 月 16 日 | 2020 年 6 月 14 日 | 必需 | 项目管理和会计 |
| 启用与原始交易具有相同分类帐科目的项目调整过帐 | 2022 年 9 月 16 日 | 2020 年 6 月 14 日 | 必需 | 项目管理和会计 |
| 项目合同承诺金额详细信息 | 2022 年 9 月 16 日 | 2019 年 8 月 31 日 | 必需 | 项目管理和会计 |
| 在项目发票方案创建期间启用按资源排序 | 2022 年 9 月 16 日 | 2019 年 8 月 31 日 | 必需 | 项目管理和会计 |
