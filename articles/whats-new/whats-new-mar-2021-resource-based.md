---
title: 2021 年 3 月新增功能 - 面向资源/非库存场景的 Project Operations
description: 本文提供有关 2021 年 3 月版基于资源/非库存场景的 Project Operations 中可用的质量更新的信息。
author: sigitac
ms.date: 03/03/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: fbdcb01117c39f879f80319b01d278c91a56e8f6
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8932929"
---
# <a name="whats-new-march-2021---project-operations-for-resourcenon-stocked-based-scenarios"></a>2021 年 3 月新增功能 - 面向资源/非库存场景的 Project Operations

_**适用于：** 面向资源/非库存场景的 Project Operations_

本文适用于以下 Dynamics 365 Project Operations 组件和版本：

- Dataverse 环境中的 Project Operations 版本 4.8.0.91 
- Dynamics 365 Finance 环境中的项目管理和会计版本 10.0.16 

## <a name="quality-updates"></a>质量更新

### <a name="project-operations-on-dataverse"></a>Dataverse 上的 Project Operations


| **功能区域** | **参考编号** | **质量更新** |
| --- | --- | --- |
| 计费和定价 | 2133873 | 修复了 **费用估计值** 网格中 **销售单价** 货币符号的显示问题。 |
| 计费和定价 | 2174616 | 赢得报价单时，会在从该报价单复制的合同子项详细信息中引用合同自定义价目表。 |
| 商机管理 | 2167475 | 产生未记帐实际条目的更正发票中的固定税额。 |
| 商机管理 | 2176285 | 不能将税额从销售合同/报价单明细详细信息复制到成本合同/报价单明细详细信息。 |
| 商机管理 | 2188079 | 不得为不基于工作的合同创建拆分记帐规则。 |
| 规划和跟踪 | 2125274 | **项目开始日期映射** 的 **项目双重写入映射** 属性已从 **msdyn\_taskearlieststart** 更新为 **msdyn\_actualstart**。 |
| 规划和跟踪 | 2138853 | 更新了项目复制功能，以确保将引用任务的支出估计行复制到目标项目。 |
| 规划和跟踪 | 2154306 | 针对基于资源的方案修正了在 Project Operations 中删除费用估计值的问题。 |
| 规划和跟踪 | 2173259 | 项目复制功能已更新，以确保其在特定情况下不显示 **正在复制 WBS** 错误消息。 |
| 时间和支出 | 2148910 | 修复了 **时间条目** 网格中的 **编辑条目** 页的显示问题。 |
| 时间和支出 | 2159798 | 加强了控件，以确保无法编辑已批准的费用条目。 |

### <a name="project-management-and-accounting-on-dynamics-365-finance"></a>Dynamics 365 Finance 中的项目管理和会计

有关详细信息，请参阅 [2021 年 1 月新增功能 - 面向资源/非库存场景的 Project Operations](whats-new-jan-2021-resource-based.md)。

## <a name="regulatory-updates"></a>法规更新

有关财务和运营应用的监管更新的信息，请参阅[监管更新](/dynamics365/finance/localizations/regulatory-updates)。 了解法规更新的另一种方法是登录 LCS，然后使用问题搜索工具查看计划的法规更新。 通过问题搜索，您可以按国家/地区、功能类型和发布进行搜索。


[!INCLUDE[footer-include](../includes/footer-banner.md)]