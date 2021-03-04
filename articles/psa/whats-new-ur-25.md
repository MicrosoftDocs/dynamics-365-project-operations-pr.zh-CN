---
title: Project Service Automation V3 更新版本 25 中的新增功能或更改
description: 本主题列出了 Project Service Automation V3 更新版本 25 中可用的功能和修复。
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 10/26/2020
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
ms.openlocfilehash: aabee3fe755e33d2c0f01a96b6f53a68957bc041
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/10/2021
ms.locfileid: "5143718"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-25-v3"></a><span data-ttu-id="be79b-103">Project Service Automation V3 更新版本 25 中的新增功能或更改</span><span class="sxs-lookup"><span data-stu-id="be79b-103">What's new or changed in Project Service Automation Update Release 25, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="be79b-104">我们很高兴地宣布适用于 Dynamics 365 的 Project Service Automation 应用程序的最新更新已推出。</span><span class="sxs-lookup"><span data-stu-id="be79b-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="be79b-105">此版本包括对质量、性能和可用性的一些重要改进。</span><span class="sxs-lookup"><span data-stu-id="be79b-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="be79b-106">此版本与 Dynamics 365 9.x 兼容。</span><span class="sxs-lookup"><span data-stu-id="be79b-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="be79b-107">若要更新到此版本，请访问 Dynamics 365 Online 的管理中心解决方案页面以安装更新。</span><span class="sxs-lookup"><span data-stu-id="be79b-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="be79b-108">有关详细信息，请参阅[安装、更新或移除首选解决方案](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution)。</span><span class="sxs-lookup"><span data-stu-id="be79b-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="be79b-109">此主题列出了作为 Project Service Automation V3 更新版 25 的新增或更改功能的功能或修补程序。此版本的版本号为 V 3.10.43.76，通过 2020 年 10 月的自动更新公开发布。</span><span class="sxs-lookup"><span data-stu-id="be79b-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 25 This version has a build number of V 3.10.43.76 and is generally available through a self-update in October 2020.</span></span>

## <a name="update-release-25"></a><span data-ttu-id="be79b-110">更新发布 25</span><span class="sxs-lookup"><span data-stu-id="be79b-110">Update Release 25</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="be79b-111">Bug 修复</span><span class="sxs-lookup"><span data-stu-id="be79b-111">Bug fixes</span></span>

<span data-ttu-id="be79b-112">**时间和支出**</span><span class="sxs-lookup"><span data-stu-id="be79b-112">**Time and Expense**</span></span>

<span data-ttu-id="be79b-113">以下问题已修复：</span><span class="sxs-lookup"><span data-stu-id="be79b-113">The following issue has been fixed:</span></span>

- <span data-ttu-id="be79b-114">显示所检索的基于过大间隔的其他数据的时间条目图表。</span><span class="sxs-lookup"><span data-stu-id="be79b-114">Time entry chart showing additional data based on too large of an interval being retrieved.</span></span>

<span data-ttu-id="be79b-115">**资源管理**</span><span class="sxs-lookup"><span data-stu-id="be79b-115">**Resource Management**</span></span>

<span data-ttu-id="be79b-116">以下问题已修复：</span><span class="sxs-lookup"><span data-stu-id="be79b-116">The following issue has been fixed:</span></span>

- <span data-ttu-id="be79b-117">添加了包部署程序代码，以在已有更高版本修补程序时跳过 Universal Resource Scheduling 修补程序的导入。</span><span class="sxs-lookup"><span data-stu-id="be79b-117">Added package deployer code to skip the Universal Resource Scheduling patch import if a higher version patch already exists.</span></span>

<span data-ttu-id="be79b-118">**项目管理**</span><span class="sxs-lookup"><span data-stu-id="be79b-118">**Project Management**</span></span>

<span data-ttu-id="be79b-119">已修复以下问题：</span><span class="sxs-lookup"><span data-stu-id="be79b-119">The following issues have been fixed:</span></span>

- <span data-ttu-id="be79b-120">更正了导致项目跟踪网格中的计划成本不正确的舍入和汇率差异。</span><span class="sxs-lookup"><span data-stu-id="be79b-120">Corrected rounding and exchange rate discrepancies resulting in incorrect planned cost in the project tracking grid.</span></span>
- <span data-ttu-id="be79b-121">支持在 **项目** 窗体上显示两个或更多个响应网格的功能。</span><span class="sxs-lookup"><span data-stu-id="be79b-121">Support the ability to display two or more react grids on the **Project** form.</span></span>
- <span data-ttu-id="be79b-122">提供了验证来解决日历结束日期之后仍然可以分配任务的问题，这会导致资源分配失败。</span><span class="sxs-lookup"><span data-stu-id="be79b-122">Provided validation to address the ability to assign a task past the calendar end date, which results in a failed resource assignment.</span></span>
- <span data-ttu-id="be79b-123">改进了解决由以下各项产生的 Null 引用异常的错误处理：</span><span class="sxs-lookup"><span data-stu-id="be79b-123">Improved error handling to address Null Reference Exception generated from the following:</span></span>

    - <span data-ttu-id="be79b-124">**PreValidateProjectTeamMemberCreate** 插件</span><span class="sxs-lookup"><span data-stu-id="be79b-124">**PreValidateProjectTeamMemberCreate** plug-in</span></span>
    - <span data-ttu-id="be79b-125">创建没有关联项目的项目任务时的 **PreValidateProjectTaskCreate**</span><span class="sxs-lookup"><span data-stu-id="be79b-125">**PreValidateProjectTaskCreate** when a project task is created without an associated project</span></span>
    - <span data-ttu-id="be79b-126">**PreProjectTeamMemberCreate** 插件</span><span class="sxs-lookup"><span data-stu-id="be79b-126">**PreProjectTeamMemberCreate** plug-in</span></span>
    - <span data-ttu-id="be79b-127">**PostProjectTeamMemberDelete** 插件</span><span class="sxs-lookup"><span data-stu-id="be79b-127">**PostProjectTeamMemberDelete** plug-in</span></span>
    - <span data-ttu-id="be79b-128">**PreValidateProjectTaskDelete** 插件</span><span class="sxs-lookup"><span data-stu-id="be79b-128">**PreValidateProjectTaskDelete** plug-in</span></span>

<span data-ttu-id="be79b-129">**Sales**</span><span class="sxs-lookup"><span data-stu-id="be79b-129">**Sales**</span></span>

<span data-ttu-id="be79b-130">已修复以下问题：</span><span class="sxs-lookup"><span data-stu-id="be79b-130">The following issues have been fixed:</span></span>

- <span data-ttu-id="be79b-131">改进了解决 **复制项目: Estimates HelperResource Management** 产生的 Null 引用异常的错误处理。</span><span class="sxs-lookup"><span data-stu-id="be79b-131">Improved error handling to address Null Reference Exceptions generated from **Copy Project: Estimates HelperResource Management**.</span></span>
- <span data-ttu-id="be79b-132">**时间和材料计费积压** 上的 **未准备好开票** 不清除计费状态。</span><span class="sxs-lookup"><span data-stu-id="be79b-132">**Not ready to Invoice** on a **Time and Material Billing Backlog** doesn't clear the billing status.</span></span>
- <span data-ttu-id="be79b-133">更正了 **角色价格** 和 **目录项** 选项卡上标签错误的 **价格** 按钮。</span><span class="sxs-lookup"><span data-stu-id="be79b-133">Corrected mislabeled **Prices** buttons on the **Role Price** and **Catalog Items** tab.</span></span>
