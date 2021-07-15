---
title: Project Service Automation V3 更新版本 33 中的新增功能或更改
description: 本主题列出了 Project Service Automation V3 更新版本 33 中可用的功能和修复。
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 06/30/2021
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
ms.openlocfilehash: 2c96e4abd484bb66285421baaad82ead9589bbe9
ms.sourcegitcommit: be5beba71ee9770c0083b4fe5cc89e7ec6b741b8
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 07/02/2021
ms.locfileid: "6334509"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-33-v3"></a><span data-ttu-id="28418-103">Project Service Automation V3 更新版本 33 中的新增功能或更改</span><span class="sxs-lookup"><span data-stu-id="28418-103">What's new or changed in Project Service Automation Update Release 33, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="28418-104">我们很高兴地宣布 Microsoft Dynamics 365 Project Service Automation 应用的最新更新。</span><span class="sxs-lookup"><span data-stu-id="28418-104">We're pleased to announce the latest update for the Microsoft Dynamics 365 Project Service Automation app.</span></span> <span data-ttu-id="28418-105">此版本包括对质量、性能和可用性的一些重要改进。</span><span class="sxs-lookup"><span data-stu-id="28418-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="28418-106">它与 Dynamics 365 9.x 兼容。</span><span class="sxs-lookup"><span data-stu-id="28418-106">It's compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="28418-107">若要更新到此版本，请访问 Dynamics 365 Online 解决方案管理中心页面，然后安装该更新。</span><span class="sxs-lookup"><span data-stu-id="28418-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page, and install the update.</span></span> <span data-ttu-id="28418-108">有关详细信息，请参阅[安装、更新或移除首选解决方案](/power-platform/admin/install-remove-preferred-solution)。</span><span class="sxs-lookup"><span data-stu-id="28418-108">For more information, see [Install, update, or remove a preferred solution](/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="28418-109">本主题列出了 Project Service Automation V3 更新版本 33 中新增或更改的功能和修复。</span><span class="sxs-lookup"><span data-stu-id="28418-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 33.</span></span> <span data-ttu-id="28418-110">此版本具有内部版本号 V3.10.54.98，并且于 2021 年 7 月通过自助更新公开发布。</span><span class="sxs-lookup"><span data-stu-id="28418-110">This version has a build number of V3.10.54.98 and is generally available through a self-update in July 2021.</span></span>

## <a name="update-release-33"></a><span data-ttu-id="28418-111">更新发布 33</span><span class="sxs-lookup"><span data-stu-id="28418-111">Update Release 33</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="28418-112">Bug 修复</span><span class="sxs-lookup"><span data-stu-id="28418-112">Bug fixes</span></span>

<span data-ttu-id="28418-113">**时间和支出**</span><span class="sxs-lookup"><span data-stu-id="28418-113">**Time and Expense**</span></span>

<span data-ttu-id="28418-114">已修复以下问题：</span><span class="sxs-lookup"><span data-stu-id="28418-114">The following issues have been fixed:</span></span>

- <span data-ttu-id="28418-115">两个锁定字段 **msdyn_description** 和 **msdyn_externaldescription** 在提交后可编辑。</span><span class="sxs-lookup"><span data-stu-id="28418-115">Two locked fields, **msdyn_description** and **msdyn_externaldescription** are editable after submission.</span></span>
- <span data-ttu-id="28418-116">如果创建了与项目无关的支出，将出现一条错误消息。</span><span class="sxs-lookup"><span data-stu-id="28418-116">An error message occurs if an expense is created that isn't related to a project.</span></span>
- <span data-ttu-id="28418-117">当创建时间条目时，资源角色将默认为停用角色。</span><span class="sxs-lookup"><span data-stu-id="28418-117">When a time entry is created, the resource role defaults to an inactive role.</span></span>
- <span data-ttu-id="28418-118">不会删除与撤消和删除的支出关联的日记帐行。</span><span class="sxs-lookup"><span data-stu-id="28418-118">Journal lines associated with a recalled and deleted expense aren't deleted.</span></span>
- <span data-ttu-id="28418-119">在 **时间条目快速创建窗体** 上，更新 **项目任务列表** 视图以将默认显示的日期更改为任务的开始日期。</span><span class="sxs-lookup"><span data-stu-id="28418-119">On the **Time entry Quick Create Form**, update the **Project Task List** view to change the date displayed by default to the start date of the task.</span></span>
- <span data-ttu-id="28418-120">从可预订资源的 **相关** 选项卡中创建时间条目时，将错误地为登录用户（而不是父可预订资源）创建了时间条目。</span><span class="sxs-lookup"><span data-stu-id="28418-120">When you create a time entry from the **Related** tab of the bookable resource, the time entry is incorrectly created for the signed-in user instead of the parent bookable resource.</span></span>
- <span data-ttu-id="28418-121">新字段将添加到 **批量审批 MDD** 对话框。</span><span class="sxs-lookup"><span data-stu-id="28418-121">New fields are added to the **Bulk approval MDD** dialog box.</span></span>

<span data-ttu-id="28418-122">**项目规划**</span><span class="sxs-lookup"><span data-stu-id="28418-122">**Project planning**</span></span>

<span data-ttu-id="28418-123">已修复以下问题：</span><span class="sxs-lookup"><span data-stu-id="28418-123">The following issues have been fixed:</span></span>
- <span data-ttu-id="28418-124">将项目工作小时模板与复杂的日历一起应用时，项目创建性能将降低。</span><span class="sxs-lookup"><span data-stu-id="28418-124">Slow project creation performance when project work hour templates are applied with complex calendars.</span></span>
- <span data-ttu-id="28418-125">如果开始日期大于结束日期，则复制项目模板上将显示一个错误，因为每个字段的时间组件不同。</span><span class="sxs-lookup"><span data-stu-id="28418-125">When the start date is greater than the end date, an error displays on the copy project template because of differences in the time component of each field.</span></span>

<span data-ttu-id="28418-126">**资源管理**</span><span class="sxs-lookup"><span data-stu-id="28418-126">**Resource management**</span></span>

<span data-ttu-id="28418-127">已修复以下问题：</span><span class="sxs-lookup"><span data-stu-id="28418-127">The following issues have been fixed:</span></span>
- <span data-ttu-id="28418-128">如果在资源利用率查询中使用了不正确的参数，XML 将导致 **资源利用率** 网格上的筛选结果不正确。</span><span class="sxs-lookup"><span data-stu-id="28418-128">An incorrect parameter is used in the resource utilization query and the XML leads to incorrect filter results on the **Resource Utilization** grid.</span></span>
- <span data-ttu-id="28418-129">**扩展预订** 确认将显示不正确的预订结束日期。</span><span class="sxs-lookup"><span data-stu-id="28418-129">The **Extend Bookings** confirmation displays incorrect end date for bookings.</span></span>

<span data-ttu-id="28418-130">**销售**</span><span class="sxs-lookup"><span data-stu-id="28418-130">**Sales**</span></span>

<span data-ttu-id="28418-131">已修复以下问题：</span><span class="sxs-lookup"><span data-stu-id="28418-131">The following issues have been fixed:</span></span>
- <span data-ttu-id="28418-132">如果创建的类别价格缺少值，将出现一条错误消息。</span><span class="sxs-lookup"><span data-stu-id="28418-132">An error message occurs if a category price is created with missing values.</span></span>
- <span data-ttu-id="28418-133">如果创建的合同子项里程碑没有订单行，将出现一条错误消息。</span><span class="sxs-lookup"><span data-stu-id="28418-133">An error message occurs if a contract line milestone is created without an order line.</span></span>
