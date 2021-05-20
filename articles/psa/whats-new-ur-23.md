---
title: Project Service Automation V3 更新版本 23 中的新增功能或更改
description: 本主题列出了 Project Service Automation V3 更新版本 23 中可用的功能和修复。
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 08/25/2020
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
ms.openlocfilehash: f90c0d2168b261cf1b6ef10374f282274ea61af5
ms.sourcegitcommit: 3d78338773929121d17ec3386f6cb67bfb2272cc
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/27/2021
ms.locfileid: "5948948"
---
# <a name="project-service-automation-update-release-23-v3"></a><span data-ttu-id="b0951-103">Project Service Automation V3 更新版本 23</span><span class="sxs-lookup"><span data-stu-id="b0951-103">Project Service Automation Update Release 23, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="b0951-104">我们很高兴地宣布适用于 Dynamics 365 的 Project Service Automation 应用程序的最新更新已推出。</span><span class="sxs-lookup"><span data-stu-id="b0951-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="b0951-105">此版本包括对质量、性能和可用性的一些重要改进。</span><span class="sxs-lookup"><span data-stu-id="b0951-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="b0951-106">此版本与 Dynamics 365 9.x 兼容。</span><span class="sxs-lookup"><span data-stu-id="b0951-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="b0951-107">若要更新到此版本，请访问 Dynamics 365 Online 的管理中心解决方案页面以安装更新。</span><span class="sxs-lookup"><span data-stu-id="b0951-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="b0951-108">有关详细信息，请参阅[安装、更新或移除首选解决方案](/power-platform/admin/install-remove-preferred-solution)。</span><span class="sxs-lookup"><span data-stu-id="b0951-108">For more information, see [Install, update, or remove a preferred solution](/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="b0951-109">本主题列出了 Project Service Automation V3 更新版本 23 中新增或更改的功能和修复。</span><span class="sxs-lookup"><span data-stu-id="b0951-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 23.</span></span> <span data-ttu-id="b0951-110">该版本的内部版本号为 V 3.10.34.30，并且在 2020 年 8 月通过自行更新公开发布。</span><span class="sxs-lookup"><span data-stu-id="b0951-110">This version has a build number of V 3.10.34.30 and is generally available through a self-update in August 2020.</span></span>

## <a name="update-release-23"></a><span data-ttu-id="b0951-111">更新发布 23</span><span class="sxs-lookup"><span data-stu-id="b0951-111">Update Release 23</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="b0951-112">Bug 修复</span><span class="sxs-lookup"><span data-stu-id="b0951-112">Bug fixes</span></span>

<span data-ttu-id="b0951-113">**时间和支出**</span><span class="sxs-lookup"><span data-stu-id="b0951-113">**Time and Expense**</span></span>

<span data-ttu-id="b0951-114">已修复以下问题：</span><span class="sxs-lookup"><span data-stu-id="b0951-114">The following issues have been fixed:</span></span>
- <span data-ttu-id="b0951-115">在 **项目团队成员删除** 中处理边缘案例以提供有意义的异常。</span><span class="sxs-lookup"><span data-stu-id="b0951-115">Handle edge case in **Project Team Member Delete** to provide a meaningful exception.</span></span>
- <span data-ttu-id="b0951-116">导入工作会导致空白删除屏幕。</span><span class="sxs-lookup"><span data-stu-id="b0951-116">Assignment import results in a blank remove screen.</span></span>

<span data-ttu-id="b0951-117">**资源管理**</span><span class="sxs-lookup"><span data-stu-id="b0951-117">**Resource Management**</span></span>

<span data-ttu-id="b0951-118">已修复以下问题：</span><span class="sxs-lookup"><span data-stu-id="b0951-118">The following issues have been fixed:</span></span>

- <span data-ttu-id="b0951-119">**资源利用率网格资源卡** 在时间刻度超过五天时显示错误的数据。</span><span class="sxs-lookup"><span data-stu-id="b0951-119">The **Resource utilization grid resource card** shows incorrect data when the time scale is more than five days.</span></span>
- <span data-ttu-id="b0951-120">当客户创建可预订资源时，插件会间歇性地无法自动将资源添加到 Microsoft Office 365 组。</span><span class="sxs-lookup"><span data-stu-id="b0951-120">When customers create a bookable resource, the plug-in intermittently fails to automatically add the resource to a Microsoft Office 365 group.</span></span>
- <span data-ttu-id="b0951-121">**协调** 视图在 **周** 或 **月** 视图中错误地显示手动信息。</span><span class="sxs-lookup"><span data-stu-id="b0951-121">**Reconciliation** view displays manual contours incorrectly in the **Week** or **Month** view.</span></span>

<span data-ttu-id="b0951-122">**项目管理**</span><span class="sxs-lookup"><span data-stu-id="b0951-122">**Project Management**</span></span>

<span data-ttu-id="b0951-123">已修复以下问题：</span><span class="sxs-lookup"><span data-stu-id="b0951-123">The following issues have been fixed:</span></span>

- <span data-ttu-id="b0951-124">过多的 **usersettings 的 RetrieveMultiple** 实体导致项目审批和其他操作的性能下降。</span><span class="sxs-lookup"><span data-stu-id="b0951-124">An excessive number of **RetrieveMultiple for usersettings** entities are causing degraded performance for project approvals and other operations.</span></span>
- <span data-ttu-id="b0951-125">**任务计划** 网格资源查找限制最多只显示项目团队的五个团队成员。</span><span class="sxs-lookup"><span data-stu-id="b0951-125">The **Task Planning** grid resource lookup is limited to only show up to five team members from the project team.</span></span> 
- <span data-ttu-id="b0951-126">**任务计划** 网格资源查找不会筛选停用资源。</span><span class="sxs-lookup"><span data-stu-id="b0951-126">The **Task Planning** grid resource lookup does not filter inactive resources.</span></span>
- <span data-ttu-id="b0951-127">手动模式未在项目计划工作分解结构中按预期工作。</span><span class="sxs-lookup"><span data-stu-id="b0951-127">Manual mode is not working as expected in the project planning work breakdown structure.</span></span>
- <span data-ttu-id="b0951-128">**任务计划** 网格显示 **停用交易记录类别**。</span><span class="sxs-lookup"><span data-stu-id="b0951-128">The **Task Planning** grid shows **Inactive Transaction Categories**.</span></span>
- <span data-ttu-id="b0951-129">当任务有多个工作时，**资源分配** 网格舍入不正确。</span><span class="sxs-lookup"><span data-stu-id="b0951-129">The **Resource Assignment** grid rounds incorrectly when a task has multiple assignments.</span></span>
- <span data-ttu-id="b0951-130">单个任务的计划成本和实际成本的舍入值不同。</span><span class="sxs-lookup"><span data-stu-id="b0951-130">Rounding values are different between planned cost and actual cost for a single task.</span></span>

<span data-ttu-id="b0951-131">**Sales**</span><span class="sxs-lookup"><span data-stu-id="b0951-131">**Sales**</span></span>

<span data-ttu-id="b0951-132">已修复以下问题：</span><span class="sxs-lookup"><span data-stu-id="b0951-132">The following issues have been fixed:</span></span>

- <span data-ttu-id="b0951-133">**提取所有交易记录类别** 双击创建多个行。</span><span class="sxs-lookup"><span data-stu-id="b0951-133">**Fetch All Transaction Categories** double-click creates multiple lines.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]