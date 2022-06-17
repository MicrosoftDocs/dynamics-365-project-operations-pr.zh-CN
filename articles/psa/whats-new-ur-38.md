---
title: Project Service Automation V3 更新版本 38 中的新增功能或更改
description: 本文列出了 Microsoft Dynamics 365 Project Service Automation 更新版 38 V3 中提供的功能和修补程序。
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 12/06/2021
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
ms.openlocfilehash: ccc08cd0bc365bd4761424a4c0ceac91985e7c89
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8915174"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-38-v3"></a>Project Service Automation V3 更新版本 38 中的新增功能或更改

[!include [banner](../includes/psa-now-project-operations.md)]

我们很高兴地宣布 Microsoft Dynamics 365 Project Service Automation 应用的最新更新。 此版本包括对质量、性能和可用性的一些重要改进。 它与 Dynamics 365 9.x 兼容。 若要更新到此版本，请访问 Dynamics 365 Online 解决方案管理中心页面，然后安装该更新。 有关详细信息，请参阅[安装、更新或移除首选解决方案](/power-platform/admin/install-remove-preferred-solution)。

本文列出了 Project Service Automation 更新版 38 V3 的新增和更改的功能和修补程序。 此版本的内部版本号为 V3.10.59.117，通过 2021 年 12 月的自动更新公开发布。

## <a name="update-release-38"></a>更新发布 38

### <a name="bug-fixes"></a>Bug 修复

已修复以下问题。

**时间和支出**

- 审批集日志长度超过 100,000 条记录时会出现异常。
- 用户无法从 **时间条目** 主页访问 **时间条目** 网格。
- 当没有符合导入条件的项时，**时间条目导入** 对话框不显示任何文本。
- 用户可以创建 **目标状态** 字段设置为 **未知** 的审批集。

**项目管理**

- 夏令时开始时，UTC(+09:30) 和 UTC(+10:00) 的资源分配中未正确显示分布。
- 某些区域设置中隐藏了工作分解结构的 **其他列** 字段。
- **项目任务** 网格中日历控件的日期选择器未正确本地化为中文。

**销售**

- 当具有不同合同单位和货币的可预订资源提交时间条目时，**合同绩效** 和 **项目实际成本** 值不匹配。
- 将发票作为托管解决方案导入时，自动确认发票的自定义工作流失败。 系统了显示以下消息：“Microsoft.Xrm.Sdk.InvalidPluginExecutionException 消息：发票状态无效。”
- 当选择 **根** 作为摘要选项，并且项目的估计值来自混合的交易类（例如，时间、支出和材料估计值）时，系统会将各个交易类汇总为单个费用行。
- 在合同子项与项目关联之前添加支出行的情况下，不会在 **更新价格** 字段中将正确的定价输入为默认值。
- 在 **项目** 和 **任务** 实体中，不允许使用负销售金额。
