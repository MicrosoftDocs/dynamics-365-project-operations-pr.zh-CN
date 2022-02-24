---
title: Project Service Automation V3 更新版本 23 中的新增功能或更改
description: 本主题列出了 Project Service Automation V3 更新版本 23 中可用的功能和修复。
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 08/25/2020
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
ms.openlocfilehash: 87f89828aeff22d9b473539e294d5cf04d46a203
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/10/2021
ms.locfileid: "5150027"
---
# <a name="project-service-automation-update-release-23-v3"></a>Project Service Automation V3 更新版本 23

[!include [banner](../includes/psa-now-project-operations.md)]

我们很高兴地宣布适用于 Dynamics 365 的 Project Service Automation 应用程序的最新更新已推出。 此版本包括对质量、性能和可用性的一些重要改进。 此版本与 Dynamics 365 9.x 兼容。 若要更新到此版本，请访问 Dynamics 365 Online 的管理中心解决方案页面以安装更新。 有关详细信息，请参阅[安装、更新或移除首选解决方案](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution)。

本主题列出了 Project Service Automation V3 更新版本 23 中新增或更改的功能和修复。 该版本的内部版本号为 V 3.10.34.30，并且在 2020 年 8 月通过自行更新公开发布。

## <a name="update-release-23"></a>更新发布 23

### <a name="bug-fixes"></a>Bug 修复

**时间和支出**

已修复以下问题：
- 在 **项目团队成员删除** 中处理边缘案例以提供有意义的异常。
- 导入工作会导致空白删除屏幕。

**资源管理**

已修复以下问题：

- **资源利用率网格资源卡** 在时间刻度超过五天时显示错误的数据。
- 当客户创建可预订资源时，插件会间歇性地无法自动将资源添加到 Microsoft Office 365 组。
- **协调** 视图在 **周** 或 **月** 视图中错误地显示手动信息。

**项目管理**

已修复以下问题：

- 过多的 **usersettings 的 RetrieveMultiple** 实体导致项目审批和其他操作的性能下降。
- **任务计划** 网格资源查找限制最多只显示项目团队的五个团队成员。 
- **任务计划** 网格资源查找不会筛选停用资源。
- 手动模式未在项目计划工作分解结构中按预期工作。
- **任务计划** 网格显示 **停用交易记录类别**。
- 当任务有多个工作时，**资源分配** 网格舍入不正确。
- 单个任务的计划成本和实际成本的舍入值不同。

**Sales**

已修复以下问题：

- **提取所有交易记录类别** 双击创建多个行。
