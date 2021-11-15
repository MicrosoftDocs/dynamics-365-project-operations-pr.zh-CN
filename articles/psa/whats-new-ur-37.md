---
title: Project Service Automation V3 更新版本 37 中的新增功能或更改
description: 本主题列出了 Microsoft Dynamics 365 Project Service Automation 更新发行版 37, V3 中的功能和修补程序。
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 11/01/2021
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
ms.openlocfilehash: 7bd00ccbb09fb43f7d7c3e0fef888a4e9dfcc752
ms.sourcegitcommit: f888e9c6e0290608abb915aa599ae9629b0efd3e
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/01/2021
ms.locfileid: "7727594"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-37-v3"></a>Project Service Automation V3 更新版本 37 中的新增功能或更改

[!include [banner](../includes/psa-now-project-operations.md)]

我们很高兴地宣布 Microsoft Dynamics 365 Project Service Automation 应用的最新更新。 此版本包括对质量、性能和可用性的一些重要改进。 它与 Dynamics 365 9.x 兼容。 若要更新到此版本，请访问 Dynamics 365 Online 解决方案管理中心页面，然后安装该更新。 有关详细信息，请参阅[安装、更新或移除首选解决方案](/power-platform/admin/install-remove-preferred-solution)。

本主题列出了 Project Service Automation 更新版本 37 V3 中新增或更改的功能和修复。 该版本的内部版本号为 V3.10.58.120，并且在 2021 年 11 月通过自行更新正式发布。

## <a name="update-release-37"></a>更新发布 37

### <a name="bug-fixes"></a>Bug 修复

已修复以下问题。

**时间和支出**
- 用户无法通过清除单元格来删除时间条目。
- **我未通过的审批** 视图仅包含状态为 **已提交** 的项目审批。

**项目管理**
- 如果项目团队成员的职位名称为空，则用户在 Microsoft 桌面加载项中打开项目时会收到 Null 引用异常错误。
- **项目任务** 页上没有 **保存** 按钮，因此用户无法保存对任务记录所做的更改。
- 用户无法删除具有与 **赢单** 状态报价单相关联的任务的项目。

**销售**
- 将更新 **项目** 页上的 **货币** 字段，以与应用模板的货币匹配。
- 对于具有多种货币的任务，成本计算不正确。
