---
title: Project Service Automation V3 更新版本 41 中的新增功能或更改
description: 本主题列出了 Microsoft Dynamics 365 Project Service Automation 更新发行版 41, V3 中的功能和修补程序。
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 03/07/2022
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
ms.openlocfilehash: 649d8bca36fda0a09dc7230ee4d742cadb32f3b3
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/14/2022
ms.locfileid: "8580905"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-41-v3"></a>Project Service Automation V3 更新版本 41 中的新增功能或更改

[!include [banner](../includes/psa-now-project-operations.md)]

我们很高兴地宣布 Microsoft Dynamics 365 Project Service Automation 应用的最新更新。 此版本包括对质量、性能和可用性的一些重要改进。 它与 Dynamics 365 9.x 兼容。 若要更新到此版本，请访问 Dynamics 365 Online 解决方案管理中心页面，然后安装该更新。 有关详细信息，请参阅[安装、更新或移除首选解决方案](/power-platform/admin/install-remove-preferred-solution)。

本主题列出了 Project Service Automation 更新版本 41 V3 中新增或更改的功能和修复。 此版本的内部版本号为 V3.10.62.162，并且在 2022 年 3 月通过自行更新公开发布。

## <a name="update-release-41"></a>更新发布 41

### <a name="bug-fixes"></a>Bug 修复

已修复以下问题。

**项目管理**
- 当您尝试从基于从桌面加载项创建的项目的模板创建项目时，显示以下错误：“资源分配的‘计划的工作’字段验证: 每个资源分配时间片段的‘结束日期’不得早于其‘开始日期’”。

**时间和支出**
- 当您尝试删除时间条目时，显示以下错误消息：“ISV 代码中出现意外错误”。

**销售**
- 当您为固定价格里程碑创建发票时，不会填充 **说明** 和 **外部说明** 字段。 
