---
title: Project Service Automation V3 更新版本 43 中的新增功能或更改
description: 本文列出了 Microsoft Dynamics 365 Project Service Automation 更新版 43 V3 中提供的功能和修补程序。
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
ms.openlocfilehash: b12cfda08f1ea1fc441782003130be445a437f7c
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8915295"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-43-v3"></a>Project Service Automation V3 更新版本 43 中的新增功能或更改

[!include [banner](../includes/psa-now-project-operations.md)]

我们很高兴地宣布 Microsoft Dynamics 365 Project Service Automation 应用的最新更新。 此版本包括对质量、性能和可用性的一些重要改进。 它与 Dynamics 365 9.x 兼容。 若要更新到此版本，请访问 Dynamics 365 Online 解决方案管理中心页面，然后安装该更新。 有关详细信息，请参阅[安装、更新或移除首选解决方案](/power-platform/admin/install-remove-preferred-solution)。

本文列出了 Project Service Automation 更新版 43 V3 的新增和更改的功能和修补程序。 此版本的内部版本号为 V3.10.74.200，通过 2022 年 5 月的自我更新正式发布。

## <a name="update-release-43"></a>更新发布 43

### <a name="bug-fixes"></a>Bug 修复

已修复以下问题。


**时间和支出**

- 从预订或资源分配导入时间条目时，未保留对相关可预订资源的引用。
- 当时间条目网格展开到全屏时，使用 Tab 键导航网格不起作用。
- 提交由其他用户创建的时间条目时，**提交者** 字段错误地填充了创建时间表的用户。
