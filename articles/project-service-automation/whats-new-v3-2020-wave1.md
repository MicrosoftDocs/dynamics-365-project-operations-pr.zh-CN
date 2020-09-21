---
title: 2020 年第 1 波 Project Service Automation 版本 3.x 中的新增功能或更改
description: 本主题介绍 2020 年第 1 波 Project Service Automation 版本 3 中的新增功能和更改。
manager: kfend
ms.service: business-applications
ms.custom:
- dyn365-projectservice
ms.date: 01/24/2020
ms.topic: article
ms.prod: ''
ms.technology: Dynamics 365 Project Service Automation 3.x wave 1 2020
author: stsporen
ms.assetid: 48b408c1-11e7-4005-abac-8fd7c0b064b1
ms.author: stsporen
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 478080c0570b71188c9f1e12b18b5aadc13903e5
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/24/2020
ms.locfileid: "3749700"
---
# <a name="whats-new-or-changed-in-project-service-automation-version-3-wave-1-2020"></a>2020 年第 1 波 Project Service Automation 版本 3 中的新增功能或更改
本主题重点介绍了迁移到 2020 年第 1 波最新发布的 Project Service Automation (PSA) 版本 3.x 时的关键升级注意事项。

## <a name="time-entry"></a>时间条目
时间条目体验已得到扩展，以提供用于将时间条目扩展到更多客户方案中的功能。 这包括添加条目类型的功能（显示为**时间源**），条目类型现在可以根据字段架构名称**时间条目设置**来促使特定行为发生。

### <a name="upgrade-consideration"></a>升级注意事项
为了支持此功能，已对 PSA 内的角色进行了更新，以包括新的特权。 这些特权会授予对**时间条目设置**这个新实体的读取访问权限。

应向需要时间记录功能的用户授予**时间条目用户**用户角色和现有角色。 此角色包括新功能，并确保时间条目将继续有效。

### <a name="currently-extended-time-entry-changes"></a>当前扩展的时间条目更改
为了最大程度地减小时间条目对当前用户的影响，此角色更改是继续利用时间条目所需的唯一核心要求。 如果创建了自定义视图或单独的时间条目体验，则必须将**时间条目设置**字段设置为正确的 PSA 值。
