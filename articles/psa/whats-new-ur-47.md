---
title: Project Service Automation V3 更新版本 47 中的新增功能或更改
description: 本文列出了 Microsoft Dynamics 365 Project Service Automation 更新版 47 V3 中提供的功能和修补程序。
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 09/14/2022
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
ms.openlocfilehash: 08e8fa9c41bdd77d93e4d5207266115022fba1b2
ms.sourcegitcommit: 498a5d5a33c47cab788fac4215fc47662042155a
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/14/2022
ms.locfileid: "9477225"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-47-v3"></a>Project Service Automation V3 更新版本 47 中的新增功能或更改

[!include [banner](../includes/psa-now-project-operations.md)]

我们很高兴地宣布 Microsoft Dynamics 365 Project Service Automation 应用的最新更新。 此版本包括对质量、性能和可用性的一些重要改进。 它与 Dynamics 365 9.x 兼容。 若要更新到此版本，请访问 Dynamics 365 Online 解决方案管理中心页面，然后安装该更新。 有关详细信息，请参阅[安装、更新或移除首选解决方案](/power-platform/admin/install-remove-preferred-solution)。

本文列出了 Project Service Automation 更新版 45 V3 的新增和更改的功能和修补程序。 此版本具有内部版本号 V3.10.78.8，并且于 2022 年 7 月通过自助更新公开发布。

## <a name="update-release-47"></a>更新发布 47

### <a name="bug-fixes"></a>Bug 修复

已修复以下问题。

**资源管理**
- 更新了验证，以确保用户在尝试创建没有 **可预订资源** 的项目团队成员时不会触发 null 引用异常。
