---
title: Project Service Automation V3 更新版本 15 中的新增功能或更改
description: 本主题介绍 Project Service Automation V3 更新版本 15 中的新增功能。
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 01/27/2020
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
ms.openlocfilehash: 0ec6746c0d3a1a03ee56440c73d044df844046f8
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/10/2021
ms.locfileid: "5143952"
---
# <a name="project-service-automation-update-release-15-v3"></a><span data-ttu-id="243be-103">Project Service Automation V3 更新版本 15</span><span class="sxs-lookup"><span data-stu-id="243be-103">Project Service Automation Update Release 15, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="243be-104">我们很高兴宣布 Dynamics 365 Project Service Automation (PSA) 应用程序的最新更新。</span><span class="sxs-lookup"><span data-stu-id="243be-104">We’re pleased to announce the latest update for the Dynamics 365 Project Service Automation (PSA) application.</span></span> <span data-ttu-id="243be-105">此版本包括对质量、性能和可用性的一些重要改进。</span><span class="sxs-lookup"><span data-stu-id="243be-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="243be-106">此版本与 Dynamics 365 9.x 兼容。</span><span class="sxs-lookup"><span data-stu-id="243be-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="243be-107">若要更新到此版本，请访问 Dynamics 365 Online 的管理中心，然后转到解决方案页面以安装更新。</span><span class="sxs-lookup"><span data-stu-id="243be-107">To update to this release, visit the Admin Center for Dynamics 365 online, and go to the solutions page to install the update.</span></span> <span data-ttu-id="243be-108">有关详细信息，请参阅[安装、更新或移除首选解决方案](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution)。</span><span class="sxs-lookup"><span data-stu-id="243be-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="243be-109">本主题列出了 PSA V3 更新版本 15 中新增或更改的功能和修复。</span><span class="sxs-lookup"><span data-stu-id="243be-109">This topic lists the features and fixes that are new or changed for PSA V3, Update Release 15.</span></span> <span data-ttu-id="243be-110">该版本的内部版本号为 V3.10.5.28，并且在 2020 年 1 月通过自行更新公开发布。</span><span class="sxs-lookup"><span data-stu-id="243be-110">This version has a build number of V3.10.5.28 and is generally available through a self-update in January 2020.</span></span>

## <a name="update-release-15"></a><span data-ttu-id="243be-111">更新发布 15</span><span class="sxs-lookup"><span data-stu-id="243be-111">Update Release 15</span></span> 

### <a name="enhancements"></a><span data-ttu-id="243be-112">增强功能</span><span class="sxs-lookup"><span data-stu-id="243be-112">Enhancements</span></span>

- <span data-ttu-id="243be-113">项目管理</span><span class="sxs-lookup"><span data-stu-id="243be-113">Project Management</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="243be-114">提供错误修补程序</span><span class="sxs-lookup"><span data-stu-id="243be-114">Bug fixes</span></span>

- <span data-ttu-id="243be-115">时间和支出</span><span class="sxs-lookup"><span data-stu-id="243be-115">Time and Expense</span></span>

  - <span data-ttu-id="243be-116">已修复：在协调视图中添加加载时错误处理。</span><span class="sxs-lookup"><span data-stu-id="243be-116">Fixed: Add on-load error handling in the reconciliation view.</span></span>
  - <span data-ttu-id="243be-117">已修复：项目资源中心：重命名 **金额** 以减少多义性。</span><span class="sxs-lookup"><span data-stu-id="243be-117">Fixed: Project Resource Hub: Rename **Amount** to reduce ambiguity.</span></span>
  - <span data-ttu-id="243be-118">已修复：调整 **复制时间条目列** 视图以包括类型。</span><span class="sxs-lookup"><span data-stu-id="243be-118">Fixed: Adjust the view **Copy Time Entry Columns** to include the type.</span></span>
  - <span data-ttu-id="243be-119">已修复：在网格视图中使用小数编辑时间条目持续时间导致某些数字出现未知错误。</span><span class="sxs-lookup"><span data-stu-id="243be-119">Fixed: Editing time entry duration in the grid view using decimal numbers results in unknown error for some numbers.</span></span>

- <span data-ttu-id="243be-120">项目管理</span><span class="sxs-lookup"><span data-stu-id="243be-120">Project Management</span></span>

  - <span data-ttu-id="243be-121">已修复：**用于跟踪视图** 的下拉菜单现在将根据选项宽度进行扩展。</span><span class="sxs-lookup"><span data-stu-id="243be-121">Fixed: The drop-down menu for **Use in Tracking View** now expands based on the width of the options.</span></span>
  - <span data-ttu-id="243be-122">已修复：在 +13 时区中管理项目时，任务计算显示的结果不准确。</span><span class="sxs-lookup"><span data-stu-id="243be-122">Fixed: When managing projects in the +13 time zone, tasks calculations can display inaccurate results.</span></span>
  - <span data-ttu-id="243be-123">已修复：使用 24 小时制日历时，已更正 **团队成员结束时间**。</span><span class="sxs-lookup"><span data-stu-id="243be-123">Fixed: **Team Member End Time** has been corrected when using a 24-hour calendar.</span></span>
  - <span data-ttu-id="243be-124">已修复：重新激活了 **msdyn_project** 主窗体中的 **BPF**。</span><span class="sxs-lookup"><span data-stu-id="243be-124">Fixed: Re-activated the **BPF** in **msdyn_project** main form.</span></span>
  - <span data-ttu-id="243be-125">已修复：工作计算不再忽略一天。</span><span class="sxs-lookup"><span data-stu-id="243be-125">Fixed: Assignments calculation no longer ignores one day.</span></span>
  - <span data-ttu-id="243be-126">已修复：当用户和项目的时区不同时，向项目窗体中添加了新通知横幅。</span><span class="sxs-lookup"><span data-stu-id="243be-126">Fixed: A new notification banner has been added to the project form when the time zone differs between user and project.</span></span>

- <span data-ttu-id="243be-127">Sales</span><span class="sxs-lookup"><span data-stu-id="243be-127">Sales</span></span>

  - <span data-ttu-id="243be-128">已修复：支出估计类别查找可用于筛选重复项。</span><span class="sxs-lookup"><span data-stu-id="243be-128">Fixed: Expense estimate category lookup can be used to filter duplicates.</span></span>
  - <span data-ttu-id="243be-129">已修复：**PluginDomain.ExecuteInTryCatchBlock(..)** 中的代码不再隐藏异常的来源。</span><span class="sxs-lookup"><span data-stu-id="243be-129">Fixed: Code in **PluginDomain.ExecuteInTryCatchBlock(..)** no longer hides the origin of the exception.</span></span>
  - <span data-ttu-id="243be-130">已修复：当有 1000 个以上的项目时，不再在 **报价单明细** 窗体内的 **项目查找** 中获取错误消息。</span><span class="sxs-lookup"><span data-stu-id="243be-130">Fixed: No longer get an error message in **Project lookup** in the **Quote Line** form when there are more than 1000 projects.</span></span>
  - <span data-ttu-id="243be-131">已修复：人工估算和支出估算的 **估计** 网格现在显示正确的货币符号。</span><span class="sxs-lookup"><span data-stu-id="243be-131">Fixed: **Estimates** grid for labor estimates and expense estimates now displays the correct currency symbol.</span></span>
  - <span data-ttu-id="243be-132">已修复：组织将 PSA 从更新版本 14 更新为更新版本 15 之后，**计划** 选项卡在 **项目** 窗体上不再显示为空白。</span><span class="sxs-lookup"><span data-stu-id="243be-132">Fixed: After an organization updates PSA from Update Release 14 to Update Release 15, the **Schedule** tab no longer appears as blank on the **Project** form.</span></span>
