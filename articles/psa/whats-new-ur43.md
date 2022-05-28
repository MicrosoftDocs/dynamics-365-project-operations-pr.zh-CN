---
title: Project Service Automation V3 更新版本 43 中的新增功能或更改
description: 本主题列出了 Microsoft Dynamics 365 Project Service Automation 更新发行版 43, V3 中的功能和修补程序。
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 05/04/2022
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
ms.openlocfilehash: fcf18a24b3bc354a16a415368063133743e79696
ms.sourcegitcommit: 7e419a5f73f80fa887084e3b212c90586fc397dd
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/05/2022
ms.locfileid: "8709960"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-43-v3"></a>Project Service Automation V3 更新版本 43 中的新增功能或更改

[!include [banner](../includes/psa-now-project-operations.md)]

我们很高兴地宣布 Microsoft Dynamics 365 Project Service Automation 应用的最新更新。 此版本包括对质量、性能和可用性的一些重要改进。 它与 Dynamics 365 9.x 兼容。 若要更新到此版本，请访问 Dynamics 365 Online 解决方案管理中心页面，然后安装该更新。 有关详细信息，请参阅[安装、更新或移除首选解决方案](/power-platform/admin/install-remove-preferred-solution)。

本主题列出了 Project Service Automation 更新版本 43 V3 中新增或更改的功能和修复。 此版本的内部版本号为 V3.10.74.200，通过 2022 年 5 月的自我更新正式发布。

## <a name="update-release-43"></a>更新发布 43

### <a name="bug-fixes"></a>Bug 修复

已修复以下问题。


**时间和支出**

- 从预订或资源分配导入时间条目时，未保留对相关可预订资源的引用。
- 当时间条目网格展开到全屏时，使用 Tab 键导航网格不起作用。
- 提交由其他用户创建的时间条目时，**提交者** 字段错误地填充了创建时间表的用户。
