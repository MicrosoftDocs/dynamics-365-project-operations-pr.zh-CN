---
title: Project Service Automation V3 更新版本 32 中的新增功能或更改
description: 本主题列出了 Project Service Automation V3 更新版本 32 中可用的功能和修复。
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 06/01/2021
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
ms.openlocfilehash: 023e51e834060a35d2d7e3469d34297192e38ba11c12a2c4f57424213aba44ba
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/06/2021
ms.locfileid: "6994850"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-32-v3"></a>Project Service Automation V3 更新版本 32 中的新增功能或更改

[!include [banner](../includes/psa-now-project-operations.md)]

我们很高兴地宣布 Microsoft Dynamics 365 Project Service Automation 应用的最新更新。 此版本包括对质量、性能和可用性的一些重要改进。 它与 Dynamics 365 9.x 兼容。 若要更新到此版本，请访问 Dynamics 365 Online 解决方案管理中心页面，然后安装该更新。 有关详细信息，请参阅[安装、更新或移除首选解决方案](/power-platform/admin/install-remove-preferred-solution)。

本主题列出了 Project Service Automation V3 更新版本 32 中新增或更改的功能和修复。 此版本的内部版本号为 V3.10.53.108，通过 2021 年 6 月的自我更新正式发布。

## <a name="update-release-32"></a>更新发布 32

### <a name="bug-fixes"></a>Bug 修复

#### <a name="general"></a>常规

- 当重大升级失败时，应仅阻止主应用程序入口点，以确保仍可访问共享实体。

#### <a name="time-and-expense"></a>时间和支出

已修复以下问题：

- **TimeEntriesImportFromResourceAssignment** 不维护资源等值线切片的开始和结束时间。
- 当您在 **时间条目** 网格上选择 **打开条目** 时，可能会阻止您选择其他窗体。
- 当您将分配导入时间条目时，客户端代码查询可能会生成一个使查询失败的长 URL。
- 在 **时间条目** 网格中，在从单元格中删除值后，焦点不会保留在网格中。
- 已从现代审批的 **处理审批** 视图中删除了 **拒绝** 按钮。
- 如果出现死锁以及未能正确处理与 **时间条目** 实体相关的自定义项，则会影响时间条目批量审批的稳定性和性能。

#### <a name="project-planning"></a>项目规划

- 当您更新在 **合同签订部门** 字段中具有 NULL 值的项目时，会生成 NULL 引用异常。
- **刷新项目总额** 将错误地计算项目的剩余成本和其余销售。
- 冗余定价计算会影响与资源分配等值线更新相关的性能。

#### <a name="resource-management"></a>资源管理

以下问题已修复：

- 当可预订资源的日历容量大于 1 时，Project Service Automation 会错误地将容量识别为 0（零）。 因此，在计划视图中会出现无限循环。

#### <a name="sales"></a>销售

已修复以下问题：

- 创建具有自定义交易类型的日记帐行时，会发生以下 NULL 引用异常：*Microsoft.Dynamics.ProjectService.Plugins.JournalLinePlugins.ValidateUnitScheduleAndUnitWithTransactionType(TransactionTypetransactionType, TransactionTypeCode transTypeCodeFromPlugin)*。
- 在复制报价单之前停用的角色和类别不应添加到新复制的报价单的收费角色和类别中。
- 单据日期和会计日期与直接在草稿发票上创建的发票行详细信息中提供的开始日期不一致。
- 在复制引用之前与角色和类别的停用相关的场景中会生成 Null 引用异常。
- **项目** 页上的 **更新价格** 操作不会更新支出估算和材料估算。
