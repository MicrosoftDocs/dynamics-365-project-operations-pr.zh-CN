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
# <a name="whats-new-or-changed-in-project-service-automation-version-3-wave-1-2020"></a><span data-ttu-id="2dd47-103">2020 年第 1 波 Project Service Automation 版本 3 中的新增功能或更改</span><span class="sxs-lookup"><span data-stu-id="2dd47-103">What's new or changed in Project Service Automation version 3 wave 1 2020</span></span>
<span data-ttu-id="2dd47-104">本主题重点介绍了迁移到 2020 年第 1 波最新发布的 Project Service Automation (PSA) 版本 3.x 时的关键升级注意事项。</span><span class="sxs-lookup"><span data-stu-id="2dd47-104">The topic highlights key upgrade considerations when moving to the latest release of Project Service Automation (PSA) version 3.x wave 1 2020.</span></span>

## <a name="time-entry"></a><span data-ttu-id="2dd47-105">时间条目</span><span class="sxs-lookup"><span data-stu-id="2dd47-105">Time entry</span></span>
<span data-ttu-id="2dd47-106">时间条目体验已得到扩展，以提供用于将时间条目扩展到更多客户方案中的功能。</span><span class="sxs-lookup"><span data-stu-id="2dd47-106">The time entry experience has been extended to deliver capabilities for extending time entry into more customer scenarios.</span></span> <span data-ttu-id="2dd47-107">这包括添加条目类型的功能（显示为**时间源**），条目类型现在可以根据字段架构名称**时间条目设置**来促使特定行为发生。</span><span class="sxs-lookup"><span data-stu-id="2dd47-107">This includes the capability to add entry types, which now drive specific behavior based on the field schema name **Time Entry Settings**, displayed as **Time Source**.</span></span>

### <a name="upgrade-consideration"></a><span data-ttu-id="2dd47-108">升级注意事项</span><span class="sxs-lookup"><span data-stu-id="2dd47-108">Upgrade consideration</span></span>
<span data-ttu-id="2dd47-109">为了支持此功能，已对 PSA 内的角色进行了更新，以包括新的特权。</span><span class="sxs-lookup"><span data-stu-id="2dd47-109">To support this functionality, the roles within PSA have been updated to include new privileges.</span></span> <span data-ttu-id="2dd47-110">这些特权会授予对**时间条目设置**这个新实体的读取访问权限。</span><span class="sxs-lookup"><span data-stu-id="2dd47-110">These privileges grant read access to the new entity, **Time Entry Settings**.</span></span>

<span data-ttu-id="2dd47-111">应向需要时间记录功能的用户授予**时间条目用户**用户角色和现有角色。</span><span class="sxs-lookup"><span data-stu-id="2dd47-111">Users who require the ability to log time should be granted the user role **Time Entry User** in addition to existing roles.</span></span> <span data-ttu-id="2dd47-112">此角色包括新功能，并确保时间条目将继续有效。</span><span class="sxs-lookup"><span data-stu-id="2dd47-112">This role includes the new functionality and ensures that time entry will continue to work.</span></span>

### <a name="currently-extended-time-entry-changes"></a><span data-ttu-id="2dd47-113">当前扩展的时间条目更改</span><span class="sxs-lookup"><span data-stu-id="2dd47-113">Currently extended time entry changes</span></span>
<span data-ttu-id="2dd47-114">为了最大程度地减小时间条目对当前用户的影响，此角色更改是继续利用时间条目所需的唯一核心要求。</span><span class="sxs-lookup"><span data-stu-id="2dd47-114">To minimize the impact to current users of time entry, this role change is the only core requirement necessary to continue utilizing time entry.</span></span> <span data-ttu-id="2dd47-115">如果创建了自定义视图或单独的时间条目体验，则必须将**时间条目设置**字段设置为正确的 PSA 值。</span><span class="sxs-lookup"><span data-stu-id="2dd47-115">If you have created custom views or separate time entry experiences, you must set the **Time Entry Setting** fields to the correct PSA value.</span></span>
