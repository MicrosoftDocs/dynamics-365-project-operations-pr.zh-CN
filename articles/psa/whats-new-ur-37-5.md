---
title: Project Service Automation V3 更新版本 37.5 中的新增功能或更改
description: 本文列出了 Microsoft Dynamics 365 Project Service Automation 更新版 37.5 V3 中提供的功能和修补程序。
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 11/15/2021
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
ms.openlocfilehash: 46782c4c430ad5d78f2ed1936ae71b42327af9a9
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8915265"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-375-v3"></a>Project Service Automation V3 更新版本 37.5 中的新增功能或更改

[!include [banner](../includes/psa-now-project-operations.md)]

我们很高兴地宣布 Microsoft Dynamics 365 Project Service Automation 应用的最新更新。 此版本包括对质量、性能和可用性的一些重要改进。 它与 Dynamics 365 9.x 兼容。 若要更新到此版本，请访问 Dynamics 365 Online 解决方案管理中心页面，然后安装该更新。 有关详细信息，请参阅[安装、更新或移除首选解决方案](/power-platform/admin/install-remove-preferred-solution)。

本文列出了 Project Service Automation 更新版 37.5 V3 的新增和更改的功能和修补程序。 该版本的内部版本号为 V3.10.58.130，并且在 2021 年 11 月通过自行更新正式发布。

## <a name="update-release-375"></a>更新发布 37.5

### <a name="bug-fixes"></a>Bug 修复

已修复以下问题。

**资源管理**
- 当您更新现有预订并且为 **增加小时数方法** 或 **减少小时数方法** 选择 **比例** 时，会创建重复预订。
