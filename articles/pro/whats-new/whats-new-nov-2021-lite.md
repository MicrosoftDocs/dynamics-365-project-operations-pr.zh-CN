---
title: 2021 年 11 月新增功能 - Project Operations 精简部署
description: 本主题提供有关 2021 年 11 月版 Project Operations 精简部署中可用的质量更新的信息。
author: sigitac
ms.date: 11/09/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 3f3a19cddd1b91fc76c852153526fb7197a9f92c
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/14/2022
ms.locfileid: "8587759"
---
# <a name="whats-new-november-2021---project-operations-lite-deployment"></a>2021 年 11 月新增功能 - Project Operations 精简部署

_适用范围：精简部署 - 估价交易开票_

本主题适用于以下 Microsoft Dynamics 365 Project Operations 组件和版本：

- Dataverse 环境中的 Project Operations 版本 4.26.0.145、4.26.0.148、4.26.0.150 或 4.26.0.155
  
## <a name="features-included-in-this-release"></a>此版本中包括的功能

此版本包含以下功能：

- 项目计划应用编程接口 (API) 现在支持创建和删除项目 Bucket 的功能

## <a name="quality-updates"></a>质量更新

### <a name="project-operations-in-dataverse"></a>Dataverse 中的 Project Operations

| 功能区域 | 参考编号 | 质量更新 |
| --- | --- | --- |
| 计费和定价 | 2358236 | 发票更正必须允许进行具有零价格行的更正。 |
| 资源管理 | 2410072 | 允许将分配给任务的资源设置为项目经理。 |
| 计费和定价 | 2430234 | 修复成本绩效计算问题。 |
| 时间和支出 | 2436978 | 允许以 hh:mm 格式输入时间。 |
| 计费和定价 | 2448623 | 允许在价目表与组织单位相关联后更新价目表。 |
| 时间和支出 | 2460396 | 允许通过清除单元格来删除时间条目。 |
| 计费和定价 | 2467386 | 允许删除具有任务的项目，即使该任务与已赢单的报价单相关联也不例外。 |
| 时间和支出 | 2461744 | **我未通过的审批** 视图仅包含处于 **已提交** 阶段的项目审批。 |
| 时间和支出 | 2464082 | 当目标状态匹配时，删除从项目审批到审批集的链接。 |
| 时间和支出 | 2468108 | 计划作业不应为审批集设置 **正在处理** 状态。 |
| 时间和支出 | 2471503 | 删除存在了 7 天的审批集。 |
| 计费和定价 | 2480687 | 创建报价单行里程碑时不能删除报价单行引用。 |
