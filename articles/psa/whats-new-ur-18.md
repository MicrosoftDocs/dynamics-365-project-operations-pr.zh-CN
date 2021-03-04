---
title: Project Service Automation V3 更新版本 18 中的新增功能或更改
description: 本主题列出了 Project Service Automation V3 更新版本 18 中可用的功能和修复。
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 04/27/2020
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
ms.openlocfilehash: d6e0bb669513185ca266858ea9b8a89ed6dd4408
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/10/2021
ms.locfileid: "5147192"
---
# <a name="project-service-automation-update-release-18-v3"></a><span data-ttu-id="35353-103">Project Service Automation V3 更新版本 18</span><span class="sxs-lookup"><span data-stu-id="35353-103">Project Service Automation Update Release 18, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="35353-104">我们很高兴地宣布适用于 Dynamics 365 的 Project Service Automation 应用程序的最新更新已推出。</span><span class="sxs-lookup"><span data-stu-id="35353-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="35353-105">此版本包括对质量、性能和可用性的一些重要改进。</span><span class="sxs-lookup"><span data-stu-id="35353-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="35353-106">此版本与 Dynamics 365 9.x 兼容。</span><span class="sxs-lookup"><span data-stu-id="35353-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="35353-107">若要更新到此版本，请访问 Dynamics 365 Online 的管理中心解决方案页面以安装更新。</span><span class="sxs-lookup"><span data-stu-id="35353-107">To update to this release, visit the Admin Center for Dynamics 365 online, solutions page to install the update.</span></span> <span data-ttu-id="35353-108">有关详细信息，请参阅[安装、更新或移除首选解决方案](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution)。</span><span class="sxs-lookup"><span data-stu-id="35353-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="35353-109">本主题列出了 Project Service Automation V3 更新版本 18 中新增或更改的功能和修复。</span><span class="sxs-lookup"><span data-stu-id="35353-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 18.</span></span> <span data-ttu-id="35353-110">此版本的内部版本号为 V3.10.8.12，通常可通过 2020 年 4 月的自我更新获得。</span><span class="sxs-lookup"><span data-stu-id="35353-110">This version has a build number of V3.10.8.12 and is generally available through a self-update in April 2020.</span></span>

## <a name="update-release-18"></a><span data-ttu-id="35353-111">更新发布 18</span><span class="sxs-lookup"><span data-stu-id="35353-111">Update Release 18</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="35353-112">Bug 修复</span><span class="sxs-lookup"><span data-stu-id="35353-112">Bug fixes</span></span>

<span data-ttu-id="35353-113">**时间和支出**</span><span class="sxs-lookup"><span data-stu-id="35353-113">**Time and Expense**</span></span>

- <span data-ttu-id="35353-114">已修复：**撤消**、**请求** 和 **取消审批** 流时引发异常，同时出现不明错误消息。</span><span class="sxs-lookup"><span data-stu-id="35353-114">Fixed: **Recall**, **Request**, and **Cancel Approval** flows throw exceptions with unclear error messages.</span></span>
- <span data-ttu-id="35353-115">已修复：当对支出 **取消审批** 失败时，不引发相关异常错误。</span><span class="sxs-lookup"><span data-stu-id="35353-115">Fixed: When **Cancel Approval** fails for an expense, a relevant exception error is not thrown.</span></span>
- <span data-ttu-id="35353-116">已修复：在 10 月份切换夏令时 (DST) 后，时间条目网格对澳大利亚非工作日的处理不正确。</span><span class="sxs-lookup"><span data-stu-id="35353-116">Fixed: The Time Entry grid incorrectly handles non-working days in Australia after the daylight savings time (DST) switch in October.</span></span>
- <span data-ttu-id="35353-117">已修复：由于默认逻辑不正确，无法提交支出。</span><span class="sxs-lookup"><span data-stu-id="35353-117">Fixed: Incorrect defaulting logic prevents submission of expenses.</span></span>
- <span data-ttu-id="35353-118">已修复：当时间条目审批失败时，审批会停留在 **待定** 状态。</span><span class="sxs-lookup"><span data-stu-id="35353-118">Fixed: When time entry approval fails, the approval remains in a state of **Pending**.</span></span>
- <span data-ttu-id="35353-119">已修复：批量审批时出现 SQL 错误（死锁/超时）。</span><span class="sxs-lookup"><span data-stu-id="35353-119">Fixed: SQL Errors on bulk approvals (deadlock/timeout).</span></span>
- <span data-ttu-id="35353-120">已修复：在审批时间条目时更新团队成员导致用户体验中产生的重大性能问题。</span><span class="sxs-lookup"><span data-stu-id="35353-120">Fixed: Significant performance issues in the user experience caused by updating team members while approving time entries.</span></span>

<span data-ttu-id="35353-121">**项目管理**</span><span class="sxs-lookup"><span data-stu-id="35353-121">**Project Management**</span></span>

- <span data-ttu-id="35353-122">已修复：时区通知从 **协调** 视图移至 **项目** 主窗体。</span><span class="sxs-lookup"><span data-stu-id="35353-122">Fixed: Time zone notification moved from the **Reconciliation** view to the **Project** main form.</span></span>
- <span data-ttu-id="35353-123">已修复：在打开新项目窗体时，默认日历模板不正确。</span><span class="sxs-lookup"><span data-stu-id="35353-123">Fixed: Calendar template is not correctly defaulting when a new project form opens.</span></span>
- <span data-ttu-id="35353-124">已修复：对于基于 chromium 的浏览器，用户无法轻松地选择要删除的前置任务。</span><span class="sxs-lookup"><span data-stu-id="35353-124">Fixed: For chromium-based browsers, users are unable to easily select predecessor tasks to delete.</span></span>
- <span data-ttu-id="35353-125">已修复：创建或复制 **采用空模板的项目** 时获得不相关的分配。</span><span class="sxs-lookup"><span data-stu-id="35353-125">Fixed: Creating or copying **Project from Empty template** fetches unrelated assignments.</span></span>
- <span data-ttu-id="35353-126">已修复：在特定边缘情况下，从任务网格中创建新分配导致创建重复记录。</span><span class="sxs-lookup"><span data-stu-id="35353-126">Fixed: In specific edge cases, creating a new assignment from the task grid results in duplicate records being created.</span></span>
- <span data-ttu-id="35353-127">已修复：在手动模式下，用户无法更新任务开始日期，使之晚于当前已保存日期。</span><span class="sxs-lookup"><span data-stu-id="35353-127">Fixed: In manual mode, users are unable to update task start dates to be later than the current date saved.</span></span>

<span data-ttu-id="35353-128">**资源管理**</span><span class="sxs-lookup"><span data-stu-id="35353-128">**Resource Management**</span></span>

- <span data-ttu-id="35353-129">已修复：**协调** 视图小计行在扩展预订后计算预订差异不正确。</span><span class="sxs-lookup"><span data-stu-id="35353-129">Fixed: **Reconciliation** view subtotal row incorrectly calculates bookings variance after extending bookings.</span></span>
- <span data-ttu-id="35353-130">已修复：**协调** 视图在可预订资源的日历与项目日历不匹配时显示资源分配情况不正确。</span><span class="sxs-lookup"><span data-stu-id="35353-130">Fixed: **Reconciliation** view incorrectly displays resource assignments when the bookable resource has a calendar that does not match the project calendar.</span></span>

<span data-ttu-id="35353-131">**Sales**</span><span class="sxs-lookup"><span data-stu-id="35353-131">**Sales**</span></span>

- <span data-ttu-id="35353-132">已修复：重新审批时间条目（**批准 > 取消 >** 再次批准）时会创建重复的非计费实际值。</span><span class="sxs-lookup"><span data-stu-id="35353-132">Fixed: When time entries are re-approved (**Approve > Cancel >** approve again), a duplicate non-chargeable actual is created.</span></span>
