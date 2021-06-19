---
title: Project Service Automation V3 更新版本 32 中的新增功能或更改
description: 本主题列出了 Project Service Automation V3 更新版本 32 中可用的功能和修复。
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 06/01/2021
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
ms.openlocfilehash: 11bf451ef4f24e2301ffde4f86a556a8a4fe30b0
ms.sourcegitcommit: 886102894244887d72e5a6213071e8d8a52c9d48
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/01/2021
ms.locfileid: "6129655"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-32-v3"></a><span data-ttu-id="a489b-103">Project Service Automation V3 更新版本 32 中的新增功能或更改</span><span class="sxs-lookup"><span data-stu-id="a489b-103">What's new or changed in Project Service Automation Update Release 32, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="a489b-104">我们很高兴地宣布 Microsoft Dynamics 365 Project Service Automation 应用的最新更新。</span><span class="sxs-lookup"><span data-stu-id="a489b-104">We're pleased to announce the latest update for the Microsoft Dynamics 365 Project Service Automation app.</span></span> <span data-ttu-id="a489b-105">此版本包括对质量、性能和可用性的一些重要改进。</span><span class="sxs-lookup"><span data-stu-id="a489b-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="a489b-106">它与 Dynamics 365 9.x 兼容。</span><span class="sxs-lookup"><span data-stu-id="a489b-106">It's compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="a489b-107">若要更新到此版本，请访问 Dynamics 365 Online 解决方案管理中心页面，然后安装该更新。</span><span class="sxs-lookup"><span data-stu-id="a489b-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page, and install the update.</span></span> <span data-ttu-id="a489b-108">有关详细信息，请参阅[安装、更新或移除首选解决方案](/power-platform/admin/install-remove-preferred-solution)。</span><span class="sxs-lookup"><span data-stu-id="a489b-108">For more information, see [Install, update, or remove a preferred solution](/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="a489b-109">本主题列出了 Project Service Automation V3 更新版本 32 中新增或更改的功能和修复。</span><span class="sxs-lookup"><span data-stu-id="a489b-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 32.</span></span> <span data-ttu-id="a489b-110">此版本的内部版本号为 V3.10.53.108，通过 2021 年 6 月的自我更新正式发布。</span><span class="sxs-lookup"><span data-stu-id="a489b-110">This version has a build number of V3.10.53.108 and is generally available through a self-update in June 2021.</span></span>

## <a name="update-release-32"></a><span data-ttu-id="a489b-111">更新发布 32</span><span class="sxs-lookup"><span data-stu-id="a489b-111">Update Release 32</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="a489b-112">Bug 修复</span><span class="sxs-lookup"><span data-stu-id="a489b-112">Bug fixes</span></span>

#### <a name="general"></a><span data-ttu-id="a489b-113">常规</span><span class="sxs-lookup"><span data-stu-id="a489b-113">General</span></span>

- <span data-ttu-id="a489b-114">当重大升级失败时，应仅阻止主应用程序入口点，以确保仍可访问共享实体。</span><span class="sxs-lookup"><span data-stu-id="a489b-114">When a major upgrade fails, only the main application entry points should be blocked, to ensure that shared entities are still accessible.</span></span>

#### <a name="time-and-expense"></a><span data-ttu-id="a489b-115">时间和支出</span><span class="sxs-lookup"><span data-stu-id="a489b-115">Time and Expense</span></span>

<span data-ttu-id="a489b-116">已修复以下问题：</span><span class="sxs-lookup"><span data-stu-id="a489b-116">The following issues have been fixed:</span></span>

- <span data-ttu-id="a489b-117">**TimeEntriesImportFromResourceAssignment** 不维护资源等值线切片的开始和结束时间。</span><span class="sxs-lookup"><span data-stu-id="a489b-117">**TimeEntriesImportFromResourceAssignment** doesn't maintain the start and end times of the resource assignment contour slice.</span></span>
- <span data-ttu-id="a489b-118">当您在 **时间条目** 网格上选择 **打开条目** 时，可能会阻止您选择其他窗体。</span><span class="sxs-lookup"><span data-stu-id="a489b-118">When you select **Open Entry** on the **Time Entry** grid, you might be prevented from selecting other forms.</span></span>
- <span data-ttu-id="a489b-119">当您将分配导入时间条目时，客户端代码查询可能会生成一个使查询失败的长 URL。</span><span class="sxs-lookup"><span data-stu-id="a489b-119">While you import assignments to time entries, the client code query could generate a long URL that fails the query.</span></span>
- <span data-ttu-id="a489b-120">在 **时间条目** 网格中，在从单元格中删除值后，焦点不会保留在网格中。</span><span class="sxs-lookup"><span data-stu-id="a489b-120">In the **Time Entry** grid, after a value is deleted from a cell, the focus doesn't remain in the grid.</span></span>
- <span data-ttu-id="a489b-121">已从现代审批的 **处理审批** 视图中删除了 **拒绝** 按钮。</span><span class="sxs-lookup"><span data-stu-id="a489b-121">The **Reject** button has been removed from the **Processing approvals** view for modern approvals.</span></span>
- <span data-ttu-id="a489b-122">如果出现死锁以及未能正确处理与 **时间条目** 实体相关的自定义项，则会影响时间条目批量审批的稳定性和性能。</span><span class="sxs-lookup"><span data-stu-id="a489b-122">The stability and performance of time entry bulk approval are affected by deadlocks and a failure to appropriately handle customizations that are related to the **Time Entry** entity.</span></span>

#### <a name="project-planning"></a><span data-ttu-id="a489b-123">项目规划</span><span class="sxs-lookup"><span data-stu-id="a489b-123">Project Planning</span></span>

- <span data-ttu-id="a489b-124">当您更新在 **合同签订部门** 字段中具有 NULL 值的项目时，会生成 NULL 引用异常。</span><span class="sxs-lookup"><span data-stu-id="a489b-124">A null reference exception is generated when you update a project that has a null value in the **Contracting Unit** field.</span></span>
- <span data-ttu-id="a489b-125">**刷新项目总额** 将错误地计算项目的剩余成本和其余销售。</span><span class="sxs-lookup"><span data-stu-id="a489b-125">**Refresh Project Totals** incorrectly calculates the remaining cost and remaining sales on a project.</span></span>
- <span data-ttu-id="a489b-126">冗余定价计算会影响与资源分配等值线更新相关的性能。</span><span class="sxs-lookup"><span data-stu-id="a489b-126">Redundant pricing calculations affect performance that is related to updates on resource assignment contours.</span></span>

#### <a name="resource-management"></a><span data-ttu-id="a489b-127">资源管理</span><span class="sxs-lookup"><span data-stu-id="a489b-127">Resource Management</span></span>

<span data-ttu-id="a489b-128">以下问题已修复：</span><span class="sxs-lookup"><span data-stu-id="a489b-128">The following issue has been fixed:</span></span>

- <span data-ttu-id="a489b-129">当可预订资源的日历容量大于 1 时，Project Service Automation 会错误地将容量识别为 0（零）。</span><span class="sxs-lookup"><span data-stu-id="a489b-129">When a bookable resource's calendar capacity is more than 1, Project Service Automation incorrectly recognizes the capacity as 0 (zero).</span></span> <span data-ttu-id="a489b-130">因此，在计划视图中会出现无限循环。</span><span class="sxs-lookup"><span data-stu-id="a489b-130">Therefore, an infinite loop occurs in the schedule view.</span></span>

#### <a name="sales"></a><span data-ttu-id="a489b-131">销售</span><span class="sxs-lookup"><span data-stu-id="a489b-131">Sales</span></span>

<span data-ttu-id="a489b-132">已修复以下问题：</span><span class="sxs-lookup"><span data-stu-id="a489b-132">The following issues have been fixed:</span></span>

- <span data-ttu-id="a489b-133">创建具有自定义交易类型的日记帐行时，会发生以下 NULL 引用异常：*Microsoft.Dynamics.ProjectService.Plugins.JournalLinePlugins.ValidateUnitScheduleAndUnitWithTransactionType(TransactionTypetransactionType, TransactionTypeCode transTypeCodeFromPlugin)*。</span><span class="sxs-lookup"><span data-stu-id="a489b-133">When a journal line is created that has a custom transaction type, the following null reference exception occurs: *Microsoft.Dynamics.ProjectService.Plugins.JournalLinePlugins.ValidateUnitScheduleAndUnitWithTransactionType(TransactionTypetransactionType, TransactionTypeCode transTypeCodeFromPlugin)*.</span></span>
- <span data-ttu-id="a489b-134">在复制报价单之前停用的角色和类别不应添加到新复制的报价单的收费角色和类别中。</span><span class="sxs-lookup"><span data-stu-id="a489b-134">Roles and categories that are inactivated before a quotation is copied should not be added to chargeable roles and categories of the newly copied quotation.</span></span>
- <span data-ttu-id="a489b-135">单据日期和会计日期与直接在草稿发票上创建的发票行详细信息中提供的开始日期不一致。</span><span class="sxs-lookup"><span data-stu-id="a489b-135">The document date and accounting date aren't aligned with the start date that is provided on an invoice line detail that is created directly on a draft invoice.</span></span>
- <span data-ttu-id="a489b-136">在复制引用之前与角色和类别的停用相关的场景中会生成 Null 引用异常。</span><span class="sxs-lookup"><span data-stu-id="a489b-136">Null reference exceptions are generated in scenarios that are related to inactivation of roles and categories before a quotation is copied.</span></span>
- <span data-ttu-id="a489b-137">**项目** 页上的 **更新价格** 操作不会更新支出估算和材料估算。</span><span class="sxs-lookup"><span data-stu-id="a489b-137">The **Update Prices** action on the **Projects** page doesn't update expense estimates and material estimates.</span></span>
