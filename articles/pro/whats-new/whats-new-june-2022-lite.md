---
title: 2022 年 6 月新增功能 - Project Operations 精简部署
description: 本文提供有关 2022 年 6 月版 Microsoft Dynamics 365 Project Operations 精简部署中可用的质量更新的信息。
author: sigitac
ms.date: 06/03/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 2d773603abef7ab45d4d1c298e5553e57893294d
ms.sourcegitcommit: 51745acac29dfacba43a4003d86baff4d6ca2fb8
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/14/2022
ms.locfileid: "8959389"
---
# <a name="whats-new-june-2022---project-operations-lite-deployment"></a>2022 年 6 月新增功能 - Project Operations 精简部署

_**适用于：** 精简部署 - 估价交易开票_

本文适用于以下 Microsoft Dynamics 365 Project Operations 组件和版本：

- Dataverse 环境中的 Project Operations 版本 4.43.0.77

## <a name="quality-updates"></a>质量更新

| 功能区域 | 参考编号 | 质量更新 |
| --- | --- | --- |
| 转包 | 2708885 | 修复了用户创建可预订资源预订标题记录时，未填写可预订资源时出现的错误信息。 |
| 项目规划和跟踪 | 2629441 | 更正了工作流触发逻辑，以帮助防止更新项目任务时出现无限循环。 |
| 时间和支出 | 2641209 | 从分配/预订导入时间条目必须保留可预订资源引用。 |
| 项目规划和跟踪 | 2651148 | 必须保护项目文档标题。|
| 项目规划和跟踪 | 2653145 | 添加了验证以确保不能创建名称中包含无效字符的项目记录。 |
| 时间和支出 | 2654710 | 更正了 **审批** 页面上的筛选。 |
| 计费和定价 | 2667805 | 添加了验证，以帮助阻止在支持的未记帐实际销售额不存在时创建已记帐实际销售额。 |
| 计费和定价 | 2668378 | 添加了验证，以帮助阻止添加自定义定价维度，除非填写了逻辑名称和字段名称。 |
| 时间和支出 | 2700428 | 改进了审批逻辑，以确保即使其中一个审批集在系统作业中卡住，也可以处理项目的其他审批集。 |
