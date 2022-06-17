---
title: 2021 年 6 月新增功能 - Project Operations 精简部署
description: 本文提供有关 2021 年 6 月版 Project Operations 精简部署中可用的质量更新的信息。
author: sigitac
ms.date: 06/10/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 16fffb06ebb72ac25982374bff27a015eccfae1b
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8913931"
---
# <a name="whats-new-june-2021---project-operations-lite-deployment"></a>2021 年 6 月新增功能 - Project Operations 精简部署

_适用范围：精简部署 - 估价交易开票_

本文适用于以下 Dynamics 365 Project Operations 组件和版本：

  - Dataverse 环境上的 Project Operations 版本 4.11.0.156 或 4.11.0.164。

## <a name="quality-updates"></a>质量更新

| **功能区域** | **参考编号** | **质量更新** |
| --- | --- | --- |
| 计费和定价 | 2281417 | 修复了与通过发票计划自动发票创建操作失败有关的问题。 |
| 计费和定价 | 2287835 |   改进了发票确认性能。 |
| 商机管理 | 2222555 | 在使用 **从项目估计导入** 时，材料估计应计费必须正确复制到报价单明细详细信息。 |
| 商机管理 | 2223427 | 现在，自定义允许用于操作 **GenerateRetainersFromRetainerScheduleOptions**。 |
| 商机管理 | 2277528 | 修复了具有多个客户的项目合同子项的记帐里程碑值计算。 |
| 项目规划和跟踪 | 2226110 | 修复了 **项目团队** 网格中 **生成要求** 函数的间歇性问题。 |
| 项目规划和跟踪 | 2208109 | 用户无法使用一种货币创建项目，而使用另一种货币创建相关任务。 |
| 项目规划和跟踪 | 2258228 | 允许使用计划 API 修改 **计划** 实体的字段列表已更新。 |
| 项目规划和跟踪 | 2293989 | 必须将正确的语言和区域设置传递到 **项目任务** 网格。|
| 资源管理 | 2220493 | 修复了在将资源请求快速标记为完成时 **任务** 网格中的用户体验。 |
| 资源管理 | 2330496 | 修复了 **日程安排板** 加载问题。 （质量更新在版本 4.11.0.164 中提供） |
| 时间和支出 | 2194431 | **时间条目** 网格必须遵守在 **系统设置** 中设置的一周的开始。 |
| 时间和支出 | 2277311 | 在删除 **时间条目** 网格的单元格中的值后，光标将保留在网格中。 |
