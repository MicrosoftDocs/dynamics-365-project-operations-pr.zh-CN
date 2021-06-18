---
title: Project Service Automation V3 更新版本 30 中的新增功能或更改
description: 本主题列出了 Project Service Automation V3 更新版本 30 中可用的功能和修复。
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 04/01/2021
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
ms.openlocfilehash: 3b6b7dba9c2a22587d27006b9972c950fbb454f2
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/10/2021
ms.locfileid: "6010415"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-30-v3"></a>Project Service Automation V3 更新版本 30 中的新增功能或更改

[!include [banner](../includes/psa-now-project-operations.md)]

我们很高兴地宣布适用于 Dynamics 365 的 Project Service Automation 应用程序的最新更新已推出。 此版本包括对质量、性能和可用性的一些重要改进。 此版本与 Dynamics 365 9.x 兼容。 若要更新到此版本，请访问 Dynamics 365 Online 的管理中心解决方案页面以安装更新。 有关详细信息，请参阅[安装、更新或移除首选解决方案](/power-platform/admin/install-remove-preferred-solution.md)。

本主题列出了 Project Service Automation V3 更新版本 30 中新增或更改的功能和修复。 此版本的内部版本号为 V3.10.51.61，通常可通过 2021 年 4 月的自我更新获得。

## <a name="update-release-30"></a>更新发布 30

### <a name="bug-fixes"></a>Bug 修复

**时间和支出**

已修复以下问题：

- 如果删除了 **角色** 字段，则在 **快速创建** 页上创建和保存时间条目时将出错。
- “时间条目”筛选器应用了错误的筛选器运算符。
- 在时间条目控件中选择 **复制周** 时，不会自动显示复制的时间表。

**资源管理**

已修复以下问题：

- 在扩展预订时，分派给硬预订的预订状态不正确。 扩展预订操作会考虑预订设置元数据中定义为 **已提交** 的预订状态。
- 如果未指定有效的预订状态，则不会正确本地化错误消息。

**项目管理**

已修复以下问题：

- 项目不能用一种货币来创建，但却包含另一种货币的相关任务。

**销售**

已修复以下问题：

- 复制价目表时，不会更新价格。
- 当成本明细具有来源值时，以赢单形式结束报价单将失败。
- 在 **项目任务** 实体中，**估计成本** 已重命名为 **计划成本(基础货币)**。
- 创建或删除发票时会生成 null 引用异常。
