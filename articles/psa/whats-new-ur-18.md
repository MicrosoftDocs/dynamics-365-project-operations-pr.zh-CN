---
title: Project Service Automation V3 更新版本 18 中的新增功能或更改
description: 本主题列出了 Project Service Automation V3 更新版本 18 中可用的功能和修复。
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom: dyn365-projectservice
ms.date: 04/27/2020
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
ms.openlocfilehash: 1d7ea200531dd24d56a829f879e3a2532a9b38dc
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/16/2020
ms.locfileid: "4072558"
---
# <a name="project-service-automation-update-release-18-v3"></a>Project Service Automation V3 更新版本 18

我们很高兴地宣布适用于 Dynamics 365 的 Project Service Automation 应用程序的最新更新已推出。 此版本包括对质量、性能和可用性的一些重要改进。 此版本与 Dynamics 365 9.x 兼容。 若要更新到此版本，请访问 Dynamics 365 Online 的管理中心解决方案页面以安装更新。 有关详细信息，请参阅[安装、更新或移除首选解决方案](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution)。

本主题列出了 Project Service Automation V3 更新版本 18 中新增或更改的功能和修复。 此版本的内部版本号为 V3.10.8.12，通常可通过 2020 年 4 月的自我更新获得。

## <a name="update-release-18"></a>更新发布 18

### <a name="bug-fixes"></a>Bug 修复

**时间和支出**

- 已修复： **撤消** 、 **请求** 和 **取消审批** 流时引发异常，同时出现不明错误消息。
- 已修复：当对支出 **取消审批** 失败时，不引发相关异常错误。
- 已修复：在 10 月份切换夏令时 (DST) 后，时间条目网格对澳大利亚非工作日的处理不正确。
- 已修复：由于默认逻辑不正确，无法提交支出。
- 已修复：当时间条目审批失败时，审批会停留在 **待定** 状态。
- 已修复：批量审批时出现 SQL 错误（死锁/超时）。
- 已修复：在审批时间条目时更新团队成员导致用户体验中产生的重大性能问题。

**项目管理**

- 已修复：时区通知从 **协调** 视图移至 **项目** 主窗体。
- 已修复：在打开新项目窗体时，默认日历模板不正确。
- 已修复：对于基于 chromium 的浏览器，用户无法轻松地选择要删除的前置任务。
- 已修复：创建或复制 **采用空模板的项目** 时获得不相关的分配。
- 已修复：在特定边缘情况下，从任务网格中创建新分配导致创建重复记录。
- 已修复：在手动模式下，用户无法更新任务开始日期，使之晚于当前已保存日期。

**资源管理**

- 已修复： **协调** 视图小计行在扩展预订后计算预订差异不正确。
- 已修复： **协调** 视图在可预订资源的日历与项目日历不匹配时显示资源分配情况不正确。

**Sales**

- 已修复：重新审批时间条目（ **批准 > 取消 >** 再次批准）时会创建重复的非计费实际值。
