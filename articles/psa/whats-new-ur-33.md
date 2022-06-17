---
title: Project Service Automation V3 更新版本 33 中的新增功能或更改
description: 本文列出了 Project Service Automation 更新版 33 V3 中提供的功能和修补程序。
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 06/30/2021
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.reviewer: johnmichalak
ms.openlocfilehash: d9c282e8b95b111ce71fb441e4dbb2d04f904e0f
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8915405"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-33-v3"></a>Project Service Automation V3 更新版本 33 中的新增功能或更改

[!include [banner](../includes/psa-now-project-operations.md)]

我们很高兴地宣布 Microsoft Dynamics 365 Project Service Automation 应用的最新更新。 此版本包括对质量、性能和可用性的一些重要改进。 它与 Dynamics 365 9.x 兼容。 若要更新到此版本，请访问 Dynamics 365 Online 解决方案管理中心页面，然后安装该更新。 有关详细信息，请参阅[安装、更新或移除首选解决方案](/power-platform/admin/install-remove-preferred-solution)。

本文列出了 Project Service Automation V3 更新版 33 的新增和更改的功能和修补程序。 此版本具有内部版本号 V3.10.54.98，并且于 2021 年 7 月通过自助更新公开发布。

## <a name="update-release-33"></a>更新发布 33

### <a name="bug-fixes"></a>Bug 修复

**时间和支出**

已修复以下问题：

- 两个锁定字段 **msdyn_description** 和 **msdyn_externaldescription** 在提交后可编辑。
- 如果创建了与项目无关的支出，将出现一条错误消息。
- 当创建时间条目时，资源角色将默认为停用角色。
- 不会删除与撤消和删除的支出关联的日记帐行。
- 在 **时间条目快速创建窗体** 上，更新 **项目任务列表** 视图以将默认显示的日期更改为任务的开始日期。
- 从可预订资源的 **相关** 选项卡中创建时间条目时，将错误地为登录用户（而不是父可预订资源）创建了时间条目。
- 新字段将添加到 **批量审批 MDD** 对话框。

**项目规划**

已修复以下问题：
- 将项目工作小时模板与复杂的日历一起应用时，项目创建性能将降低。
- 如果开始日期大于结束日期，则复制项目模板上将显示一个错误，因为每个字段的时间组件不同。

**资源管理**

已修复以下问题：
- 如果在资源利用率查询中使用了不正确的参数，XML 将导致 **资源利用率** 网格上的筛选结果不正确。
- **扩展预订** 确认将显示不正确的预订结束日期。

**销售**

已修复以下问题：
- 如果创建的类别价格缺少值，将出现一条错误消息。
- 如果创建的合同子项里程碑没有订单行，将出现一条错误消息。
