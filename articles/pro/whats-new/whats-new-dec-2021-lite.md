---
title: 2021 年 12 月新增功能 - Project Operations Lite 部署
description: 本主题提供有关 2021 年 12 月版 Project Operations 精简部署中可用的质量更新的信息。
author: sigitac
ms.date: 12/09/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: b1ff0a14bf6cb445913bcba11f83234826014857
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/14/2022
ms.locfileid: "8585367"
---
# <a name="whats-new-december-2021---project-operations-lite-deployment"></a>2021 年 12 月新增功能 - Project Operations Lite 部署

_适用范围：精简部署 - 估价交易开票_

本主题适用于以下 Microsoft Dynamics 365 Project Operations 组件和版本：

- Dataverse 环境中的 Project Operations 版本 4.27.0.195、4.27.0.242、4.27.0.244


## <a name="features-included-in-this-release"></a>此版本中包括的功能

### <a name="subcontract-management"></a>分包合同管理 

- [分包项目团队成员](../subcontracting/subcontracting-project-team-members.md)：项目经理可以创建指定的或一般团队成员，并通过分包合同和分包合同子项来影响人员配备和评估。
- [针对项目团队成员的分包选项](../subcontracting/subcon-options.md)：为指定的或一般项目团队成员进行人员配备选择时，项目经理可以查看现有的分包合同，或者为一个或多个项目团队成员创建新分包合同。 
- [对已分包资源分配的成本评估](../subcontracting/costing-subcon-ra.md)：项目成本评估将考虑分包的资源分配，并且将使用与分包合同关联的采购价目表对这些分配估算成本。 
- [将日程安排板配置为显示合同工和分包产能](../subcontracting/configure-sb-subcon.md)：Project Operations 中的日程安排板现在可以配置为搜索并建议合同工类型的可预订资源和分包产能以及员工。 在针对特定项目要求的人员配备上下文范围内搜索资源或在项目要求上下文之外进行搜索时，可以应用此配置。
- [为项目配备合同工和分包产能](../subcontracting/staffing-cw.md)：现在可以利用日程安排板经验为项目预订合同工。
- [记录分包组件项目中的时间、支出和材料使用情况](../subcontracting/recording-subcon-actuals.md)：合同工可以记录时间和支出，项目团队成员还可以记录使用项目分包合同采购的材料的使用情况。 这将导致记录使用已采购产能或材料的项目的准确成本。
- [分包合同的状态转换](../subcontracting/subcon-states.md)：分包合同可能处于已确认（以完成与供应商的谈判）、已关闭（表示交付完成）或已取消（表示在交付完成前终止与供应商的合同）状态。

### <a name="task-planning"></a>任务计划
- 改进了系统管理员故障排除。 当用户无法打开项目时，管理员可以在[项目日程安排日志](../../project-management/schedule-api-logs.md)中查看 Project for the Web 中生成的与许可证无关的错误。
- [在 Microsoft Project for the web 中使用任务清单](https://support.microsoft.com/en-us/office/use-task-checklists-in-microsoft-project-for-the-web-c69bcf73-5c75-4ad3-9893-6d6f92360e9c)。 在 Microsoft Project for the web 中，您可以向任务添加清单以跟踪特定项。

## <a name="quality-updates"></a>质量更新

| **功能区域** | **参考编号** | **质量更新** |
| --- | --- | --- |
| 规划和跟踪 | 2392596 | 计划 API 现在允许更新 **剩余工作量**、**已完成工作量** 和 **已完成 %** 字段。 |
| 规划和跟踪 | 2478497 | 因为系统将使用自动编号来填充计划 API 的 **活动编号** 和 **任务 ID** 字段，所以输入时这些字段可以为空。|
| 时间和支出 | 2468135 | 审批重试次数从五次减少到三次。 |
| 时间和支出 | 2468188 | 修复了 **注释** 实体的 **notetext** 属性中日志文本超过最大长度的问题。 |
