---
title: Project Service Automation 更新版本 28.6 修补程序 V3 中的新增功能或更改
description: 本主题列出了 Project Service Automation 更新版本 28.6 修补程序 V3 中推出的功能和修复。
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 02/22/2021
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
ms.openlocfilehash: c2389aa2249ae33333a1a8e241de225f43d70899
ms.sourcegitcommit: 24528bb9c0ef8898077cb3bc672daa211c0e73aa
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/04/2021
ms.locfileid: "5481226"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-286-v3"></a><span data-ttu-id="faac4-103">Project Service Automation V3 更新版本 28.6 中的新增功能或更改</span><span class="sxs-lookup"><span data-stu-id="faac4-103">What's new or changed in Project Service Automation Update Release 28.6, V3</span></span>

<span data-ttu-id="faac4-104">我们很高兴地宣布适用于 Dynamics 365 的 Project Service Automation 应用程序的最新更新已推出。</span><span class="sxs-lookup"><span data-stu-id="faac4-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="faac4-105">此版本包括对质量、性能和可用性的一些重要改进。</span><span class="sxs-lookup"><span data-stu-id="faac4-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="faac4-106">此版本与 Dynamics 365 9.x 兼容。</span><span class="sxs-lookup"><span data-stu-id="faac4-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="faac4-107">若要更新到此版本，请访问 Dynamics 365 Online 的管理中心解决方案页面以安装更新。</span><span class="sxs-lookup"><span data-stu-id="faac4-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="faac4-108">有关详细信息，请参阅[安装、更新或移除首选解决方案](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution)。</span><span class="sxs-lookup"><span data-stu-id="faac4-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="faac4-109">本主题列出了 Project Service Automation V3 更新版本 28.6 中新增或更改的功能和修复。</span><span class="sxs-lookup"><span data-stu-id="faac4-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 28.6.</span></span> <span data-ttu-id="faac4-110">该版本的内部版本号为 V3.10.46.147，并且在 2021 年 1 月通过自行更新公开发布。</span><span class="sxs-lookup"><span data-stu-id="faac4-110">This version has a build number of V3.10.46.147 and is generally available through a self-update in January 2021.</span></span>

## <a name="update-release-286"></a><span data-ttu-id="faac4-111">更新发布 28.6</span><span class="sxs-lookup"><span data-stu-id="faac4-111">Update Release 28.6</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="faac4-112">Bug 修复</span><span class="sxs-lookup"><span data-stu-id="faac4-112">Bug fixes</span></span>


<span data-ttu-id="faac4-113">**资源管理**</span><span class="sxs-lookup"><span data-stu-id="faac4-113">**Resource Management**</span></span>

<span data-ttu-id="faac4-114">已修复以下问题：</span><span class="sxs-lookup"><span data-stu-id="faac4-114">The following issues have been fixed:</span></span>

- <span data-ttu-id="faac4-115">在查找资源可用性时，会对未应用日历规则的每个资源都调用 **ExpandCalendar**。</span><span class="sxs-lookup"><span data-stu-id="faac4-115">When finding resource availability, **ExpandCalendar** is called for each resource that has no calendar rules applied.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
