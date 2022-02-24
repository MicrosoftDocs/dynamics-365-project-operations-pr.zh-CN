---
title: Project Service Automation V3 更新版本 21 中的新增功能或更改
description: 本主题列出了 Project Service Automation V3 更新版本 21 中可用的功能和修复。
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 06/19/2020
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
ms.openlocfilehash: b1194c1cf1997b68030fe88360c6ebb756c715fd
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/10/2021
ms.locfileid: "5147012"
---
# <a name="project-service-automation-update-release-21-v3"></a>Project Service Automation V3 更新版本 21

[!include [banner](../includes/psa-now-project-operations.md)]

我们很高兴地宣布适用于 Dynamics 365 的 Project Service Automation 应用程序的最新更新已推出。 此版本包括对质量、性能和可用性的一些重要改进。 此版本与 Dynamics 365 9.x 兼容。 若要更新到此版本，请访问 Dynamics 365 Online 的管理中心解决方案页面以安装更新。 有关详细信息，请参阅[安装、更新或移除首选解决方案](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution)。

本主题列出了 Project Service Automation V3 更新版本 21 中新增或更改的功能和修复。 该版本的内部版本号为 V 3.10.32.50，并且在 2020 年 6 月通过自行更新公开发布。

## <a name="update-release-21"></a>更新发布 21

### <a name="bug-fixes"></a>Bug 修复

**时间和支出**

已修复以下问题：

- 在仪表板中托管 **时间条目网格控件** 时，网格不会利用仪表板网格容器的整个宽度。
- 对于特定时区，**时间条目** 网格控件不会显示记录。
- 晚上 9:00 之后的时间条目会在错误的日期出现。
- 如果 **需要支出收据** 支出类别没有值，用户将无法提交支出。

**资源管理**

已修复以下问题：

- **对帐** 视图中显示了停用的预订。
- 常规资源履行缺少验证，无法确保存在有效的预订状态。

**项目管理**

已修复以下问题：

- 即使项目不是活动状态，**项目** 窗体网格（**资源分配**、**任务**、**对帐** 视图、**支出估算**）仍可编辑。
- 重复的客户无法与链接到已确认的项目合同的客户进行合并。
- 如果添加的资源无有效日历，则系统不会返回用户友好消息。
- 当项目链接到 **Microsoft Project 加载项** 后，会启用任务网格上的 **添加任务** 按钮。
- 将某种类别的任务分配给资源并且为资源角色定义了成本价时，工作量将失控增长。

**Sales**

我们进行了以下增强：

- 已将 **发票频率** 和 **记帐开始时间** 移至 **发票计划** 选项卡。

已修复以下问题：

- 即使 **角色** 的总销售价不为零，**类别** 的 **总销售价** 也会为零 (0)。
- 当另一个自定义流程正在更新其他字段时，客户无法将 **发票状态** 字段的值更改为 **准备好开发票**。
- 如果重复选择 **刷新发票行** 按钮，则会创建多个重复行。
- **更新价格** 按钮在 **快速视图** 窗体的 **角色价格** 子网格上不起作用。
- **销售价目表解析** 逻辑未正确处理时区，从而导致价目表选择错误。
- 批准单个时间条目后，项目的 **实际总费用** 可能会减少一部分。
- 如果 **检索的角色价格** 在 **基本计价单位** 和 **以基本计价单位表示的价格** 字段中没有值，则 **价格解析** 逻辑不会提供用户友好的错误消息。
