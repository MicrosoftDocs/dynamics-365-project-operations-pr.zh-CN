---
title: 2020 年第 1 波 Project Service Automation 版本 3.x 中的新增功能或更改
description: 本主题介绍 2020 年第 1 波 Project Service Automation 版本 3 中的新增功能和更改。
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 05/15/2020
ms.topic: article
author: stsporen
ms.author: stsporen
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: fef9cb62e989c693c8b3d00cb15441c284f66554
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/15/2021
ms.locfileid: "5280162"
---
# <a name="whats-new-or-changed-in-project-service-automation-version-3-wave-1-2020"></a>2020 年第 1 波 Project Service Automation 版本 3 中的新增功能或更改

[!include [banner](../includes/psa-now-project-operations.md)]

本主题重点介绍了迁移到 2020 年第 1 波最新发布的 Project Service Automation (PSA) 版本 3.x 时的关键升级注意事项。

## <a name="time-entry"></a>时间条目
时间条目体验已得到扩展，以提供用于将时间条目扩展到更多客户方案中的功能。 这包括添加条目类型的功能（显示为 **时间源**），条目类型现在可以根据字段架构名称 **时间条目设置** 来促使特定行为发生。 为了支持此功能，已增加了一个新解决方案，称为“时间、费用、进展状况和审批”(TESA)。

### <a name="upgrade-consideration"></a>升级注意事项
为了支持此功能，已对 PSA 内的角色进行了更新，以包括新的特权。 这些特权会授予对 **时间条目设置** 这个新实体的读取访问权限。

应向需要时间记录功能的用户授予 **时间条目用户** 用户角色和现有角色。 此角色包括新功能，并确保时间条目将继续有效。

此外，如果您有任何自定义应用模块中包含时间条目实体的所有窗体，您需要从该模块中删除 **TESA 时间条目快速创建窗体**。

### <a name="currently-extended-time-entry-changes"></a>当前扩展的时间条目更改
为了最大程度地减小时间条目对当前用户的影响，此角色更改是继续利用时间条目所需的唯一核心要求。 如果创建了自定义视图或单独的时间条目体验，则必须将 **时间条目设置** 字段设置为正确的 PSA 值。


[!INCLUDE[footer-include](../includes/footer-banner.md)]