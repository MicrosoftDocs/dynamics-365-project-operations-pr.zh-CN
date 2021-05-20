---
title: Project Service Automation V3 更新版本 25 中的新增功能或更改
description: 本主题列出了 Project Service Automation V3 更新版本 25 中可用的功能和修复。
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 10/26/2020
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
ms.openlocfilehash: 3aa10e1d4b23fbe6c2743d71497bdef840776008
ms.sourcegitcommit: 3d78338773929121d17ec3386f6cb67bfb2272cc
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/27/2021
ms.locfileid: "5948860"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-25-v3"></a>Project Service Automation V3 更新版本 25 中的新增功能或更改

[!include [banner](../includes/psa-now-project-operations.md)]

我们很高兴地宣布适用于 Dynamics 365 的 Project Service Automation 应用程序的最新更新已推出。 此版本包括对质量、性能和可用性的一些重要改进。 此版本与 Dynamics 365 9.x 兼容。 若要更新到此版本，请访问 Dynamics 365 Online 的管理中心解决方案页面以安装更新。 有关详细信息，请参阅[安装、更新或移除首选解决方案](/power-platform/admin/install-remove-preferred-solution)。

此主题列出了作为 Project Service Automation V3 更新版 25 的新增或更改功能的功能或修补程序。此版本的版本号为 V 3.10.43.76，通过 2020 年 10 月的自动更新公开发布。

## <a name="update-release-25"></a>更新发布 25

### <a name="bug-fixes"></a>Bug 修复

**时间和支出**

以下问题已修复：

- 显示所检索的基于过大间隔的其他数据的时间条目图表。

**资源管理**

以下问题已修复：

- 添加了包部署程序代码，以在已有更高版本修补程序时跳过 Universal Resource Scheduling 修补程序的导入。

**项目管理**

已修复以下问题：

- 更正了导致项目跟踪网格中的计划成本不正确的舍入和汇率差异。
- 支持在 **项目** 窗体上显示两个或更多个响应网格的功能。
- 提供了验证来解决日历结束日期之后仍然可以分配任务的问题，这会导致资源分配失败。
- 改进了解决由以下各项产生的 Null 引用异常的错误处理：

    - **PreValidateProjectTeamMemberCreate** 插件
    - 创建没有关联项目的项目任务时的 **PreValidateProjectTaskCreate**
    - **PreProjectTeamMemberCreate** 插件
    - **PostProjectTeamMemberDelete** 插件
    - **PreValidateProjectTaskDelete** 插件

**Sales**

已修复以下问题：

- 改进了解决 **复制项目: Estimates HelperResource Management** 产生的 Null 引用异常的错误处理。
- **时间和材料计费积压** 上的 **未准备好开票** 不清除计费状态。
- 更正了 **角色价格** 和 **目录项** 选项卡上标签错误的 **价格** 按钮。


[!INCLUDE[footer-include](../includes/footer-banner.md)]