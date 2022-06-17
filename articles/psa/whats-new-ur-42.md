---
title: Project Service Automation V3 更新版本 42 中的新增功能或更改
description: 本文列出了 Microsoft Dynamics 365 Project Service Automation 更新版 42 V3 中提供的功能和修补程序。
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 04/05/2022
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
ms.openlocfilehash: e9911531e4acbd78db416f554c8d85c4f1fee1cf
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8912704"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-42-v3"></a>Project Service Automation V3 更新版本 42 中的新增功能或更改

[!include [banner](../includes/psa-now-project-operations.md)]

我们很高兴地宣布 Microsoft Dynamics 365 Project Service Automation 应用的最新更新。 此版本包括对质量、性能和可用性的一些重要改进。 它与 Dynamics 365 9.x 兼容。 若要更新到此版本，请访问 Dynamics 365 Online 解决方案管理中心页面，然后安装该更新。 有关详细信息，请参阅[安装、更新或移除首选解决方案](/power-platform/admin/install-remove-preferred-solution)。

本文列出了 Project Service Automation 更新版 42 V3 的新增和更改的功能和修补程序。 此版本的内部版本号为 V3.10.73.61，通常可通过 2022 年 4 月的自我更新获得。

## <a name="update-release-42"></a>更新发布 42

### <a name="bug-fixes"></a>Bug 修复

已修复以下问题。

**时间和支出**

- 当时间表被拒绝时，拒绝它的用户被错误地识别为 **系统**。
- 导入时间条目时，缺少 **资源类别** 值。
- 项目审批者的权限未专门设置为 **可以批准** 时，他们也可以批准提交的项目。

**销售**

- 当实际值记录到非根级别任务时，实际成本会被错误地聚合。
