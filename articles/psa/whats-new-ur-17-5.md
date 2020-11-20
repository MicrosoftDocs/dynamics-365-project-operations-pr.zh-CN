---
title: Project Service Automation V3 更新版本 17.5 修补程序中的新增功能或更改
description: 本主题列出了 Project Service Automation V3 更新版本 17.5 中可用的功能和修复。
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 03/13/2020
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
ms.openlocfilehash: 235a27d45b3c82303d4ef5434c779b3c11421586
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/28/2020
ms.locfileid: "4118777"
---
# <a name="project-service-automation-update-release-175-v3"></a><span data-ttu-id="1f12f-103">Project Service Automation V3 更新版本 17.5</span><span class="sxs-lookup"><span data-stu-id="1f12f-103">Project Service Automation Update Release 17.5, V3</span></span>

<span data-ttu-id="1f12f-104">我们很高兴地宣布适用于 Dynamics 365 的 Project Service Automation 应用程序的最新更新已推出。</span><span class="sxs-lookup"><span data-stu-id="1f12f-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="1f12f-105">此版本包括对质量、性能和可用性的一些重要改进。</span><span class="sxs-lookup"><span data-stu-id="1f12f-105">This release includes some important improvements to quality, performance, and usability.</span></span>  <span data-ttu-id="1f12f-106">此版本与 Dynamics 365 9.x 兼容。</span><span class="sxs-lookup"><span data-stu-id="1f12f-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="1f12f-107">若要更新到此版本，请访问 Dynamics 365 Online 的管理中心解决方案页面以安装更新。</span><span class="sxs-lookup"><span data-stu-id="1f12f-107">To update to this release, visit the Admin Center for Dynamics 365 online, solutions page to install the update.</span></span> <span data-ttu-id="1f12f-108">有关详细信息，请参阅[安装、更新或移除首选解决方案](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution)。</span><span class="sxs-lookup"><span data-stu-id="1f12f-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="1f12f-109">本主题列出了 V3 更新版本 17.5 中新增或更改的功能和修复。</span><span class="sxs-lookup"><span data-stu-id="1f12f-109">This topic lists the features and fixes that are new or changed for V3, Update Release 17.5.</span></span> <span data-ttu-id="1f12f-110">该版本的内部版本号为 V3.10.7.32，并且在 2020 年 3 月通过自行更新公开发布。</span><span class="sxs-lookup"><span data-stu-id="1f12f-110">This version has a build number of V3.10.7.32 and is generally available through a self-update in March 2020.</span></span>


## <a name="update-release-175"></a><span data-ttu-id="1f12f-111">更新发布 17.5</span><span class="sxs-lookup"><span data-stu-id="1f12f-111">Update Release 17.5</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="1f12f-112">提供错误修补程序</span><span class="sxs-lookup"><span data-stu-id="1f12f-112">Bug fixes</span></span>


<span data-ttu-id="1f12f-113">**项目管理**</span><span class="sxs-lookup"><span data-stu-id="1f12f-113">**Project Management**</span></span>

- <span data-ttu-id="1f12f-114">已修复：解决了长期任务所发生的服务器端同步问题。</span><span class="sxs-lookup"><span data-stu-id="1f12f-114">Fixed: Addressed server-side synchronization issues that occur with long duration tasks.</span></span>
- <span data-ttu-id="1f12f-115">已修复：解决了 24 小时工作时间模板不准确地使任务额外增加一天的问题。</span><span class="sxs-lookup"><span data-stu-id="1f12f-115">Fixed: Addressed 24-hour work hour templates inaccurately adding an additional day to tasks.</span></span>
- <span data-ttu-id="1f12f-116">已修复：解决了 +13 GMT 工作时间模板不准确地将任务提前一天的问题。</span><span class="sxs-lookup"><span data-stu-id="1f12f-116">Fixed: Addressed +13 GMT work hour templates inaccurately shifting tasks one day ahead.</span></span>
