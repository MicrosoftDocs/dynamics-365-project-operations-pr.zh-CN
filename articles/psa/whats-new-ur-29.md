---
title: Project Service Automation V3 更新版本 29 中的新增功能或更改
description: 本主题列出了 Project Service Automation V3 更新版本 29 中可用的功能和修复。
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
ms.openlocfilehash: 0e1ff0db42adb8b991b26dca1585bd603b2e2276
ms.sourcegitcommit: f57408d6637f670b920d7ce95f8ace8eb1963093
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/17/2021
ms.locfileid: "5664632"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-29-v3"></a><span data-ttu-id="99fce-103">Project Service Automation V3 更新版本 29 中的新增功能或更改</span><span class="sxs-lookup"><span data-stu-id="99fce-103">What's new or changed in Project Service Automation Update Release 29, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="99fce-104">我们很高兴地宣布适用于 Dynamics 365 的 Project Service Automation 应用程序的最新更新已推出。</span><span class="sxs-lookup"><span data-stu-id="99fce-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="99fce-105">此版本包括对质量、性能和可用性的一些重要改进。</span><span class="sxs-lookup"><span data-stu-id="99fce-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="99fce-106">此版本与 Dynamics 365 9.x 兼容。</span><span class="sxs-lookup"><span data-stu-id="99fce-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="99fce-107">若要更新到此版本，请访问 Dynamics 365 Online 的管理中心解决方案页面以安装更新。</span><span class="sxs-lookup"><span data-stu-id="99fce-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="99fce-108">有关详细信息，请参阅[安装、更新或移除首选解决方案](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution)。</span><span class="sxs-lookup"><span data-stu-id="99fce-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="99fce-109">本主题列出了 Project Service Automation V3 更新版本 29 中新增或更改的功能和修复。</span><span class="sxs-lookup"><span data-stu-id="99fce-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 29.</span></span> <span data-ttu-id="99fce-110">此版本的内部版本号为 V3.10.47.7，通过 2021 年 2 月的自动更新公开发布。</span><span class="sxs-lookup"><span data-stu-id="99fce-110">This version has a build number of V3.10.47.7 and is generally available through a self-update in February 2021.</span></span>

## <a name="update-release-29"></a><span data-ttu-id="99fce-111">更新发布 29</span><span class="sxs-lookup"><span data-stu-id="99fce-111">Update Release 29</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="99fce-112">Bug 修复</span><span class="sxs-lookup"><span data-stu-id="99fce-112">Bug fixes</span></span>

<span data-ttu-id="99fce-113">**时间和支出**</span><span class="sxs-lookup"><span data-stu-id="99fce-113">**Time and Expense**</span></span>

<span data-ttu-id="99fce-114">已修复以下问题：</span><span class="sxs-lookup"><span data-stu-id="99fce-114">The following issues have been fixed:</span></span>

- <span data-ttu-id="99fce-115">用户无法在时间条目网格中看到记录在非工作日上的工作时间。</span><span class="sxs-lookup"><span data-stu-id="99fce-115">Users can't see working hours logged on non-working days in the time entry grid.</span></span>
- <span data-ttu-id="99fce-116">可以在此网格上编辑已批准的支出条目。</span><span class="sxs-lookup"><span data-stu-id="99fce-116">Approved expense entries can be edited on the grid.</span></span>

<span data-ttu-id="99fce-117">**项目管理**</span><span class="sxs-lookup"><span data-stu-id="99fce-117">**Project Management**</span></span>

<span data-ttu-id="99fce-118">已修复以下问题：</span><span class="sxs-lookup"><span data-stu-id="99fce-118">The following issues have been fixed:</span></span>

- <span data-ttu-id="99fce-119">缺少验证逻辑，因此无法确保资源分派工作小时数不能为负数。</span><span class="sxs-lookup"><span data-stu-id="99fce-119">Missing validation logic to ensure resource assignment effort hours can't be negative.</span></span>
- <span data-ttu-id="99fce-120">自定义操作 **AssignResourcesForTask** 会更新所有字段，而不是只更新已更改的字段。</span><span class="sxs-lookup"><span data-stu-id="99fce-120">The custom action, **AssignResourcesForTask** updates all fields instead of only changed fields.</span></span>
- <span data-ttu-id="99fce-121">在具有在 **CreateProject** 事件中注册的插件或工作流的环境中复制项目时，如果 **CopyWBSToProject** 失败，则不会更新 **msdyn_bulkgenerationstatus** 属性。</span><span class="sxs-lookup"><span data-stu-id="99fce-121">When copying a project in an environment with plug-ins or workflows that are registered on the **CreateProject** event, the **msdyn_bulkgenerationstatus** attribute isn't updated if the **CopyWBSToProject** fails.</span></span>
- <span data-ttu-id="99fce-122">展开项目日历时，工作日未按升序排序，从而导致某些项目任务更新失败。</span><span class="sxs-lookup"><span data-stu-id="99fce-122">When you expand the project calendar, the working days aren't sorted in ascending order causing some project task updates to fail.</span></span>
- <span data-ttu-id="99fce-123">对现有项目更改项目经理会触发组织单位默认逻辑。</span><span class="sxs-lookup"><span data-stu-id="99fce-123">Changing the Project Manager on an existing project triggers the organizational unit defaulting logic.</span></span>

<span data-ttu-id="99fce-124">**销售**</span><span class="sxs-lookup"><span data-stu-id="99fce-124">**Sales**</span></span>

<span data-ttu-id="99fce-125">已修复以下问题：</span><span class="sxs-lookup"><span data-stu-id="99fce-125">The following issues have been fixed:</span></span>

- <span data-ttu-id="99fce-126">如果没有合同子项，则初始化过程中，**合同** 页面上的 **合同绩效** 选项卡会失败而不给出提示。</span><span class="sxs-lookup"><span data-stu-id="99fce-126">The **Contract Performance** tab on the **Contract** page fails silently during initialization when no contract lines are present.</span></span>
