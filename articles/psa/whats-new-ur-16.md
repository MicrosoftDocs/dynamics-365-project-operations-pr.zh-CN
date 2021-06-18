---
title: Project Service Automation V3 更新版本 16 中的新增功能或更改
description: 本主题列出了 Project Service Automation V3 更新版本 16 中可用的功能和修复。
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 02/18/2020
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
ms.openlocfilehash: 5d4851ed27028117d25efb0610c25a5aac9c8b70
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/10/2021
ms.locfileid: "6006770"
---
# <a name="project-service-automation-update-release-16-v3"></a><span data-ttu-id="eb8bf-103">Project Service Automation V3 更新版本 16</span><span class="sxs-lookup"><span data-stu-id="eb8bf-103">Project Service Automation Update Release 16, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="eb8bf-104">我们很高兴地宣布适用于 Dynamics 365 的 Project Service Automation 应用程序的最新更新已推出。</span><span class="sxs-lookup"><span data-stu-id="eb8bf-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="eb8bf-105">此版本包括对质量、性能和可用性的一些重要改进。</span><span class="sxs-lookup"><span data-stu-id="eb8bf-105">This release includes some important improvements to quality, performance, and usability.</span></span>  <span data-ttu-id="eb8bf-106">此版本与 Dynamics 365 9.x 兼容。</span><span class="sxs-lookup"><span data-stu-id="eb8bf-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="eb8bf-107">若要更新到此版本，请访问 Dynamics 365 Online 的管理中心解决方案页面以安装更新。</span><span class="sxs-lookup"><span data-stu-id="eb8bf-107">To update to this release, visit the Admin Center for Dynamics 365 online, solutions page to install the update.</span></span> <span data-ttu-id="eb8bf-108">有关详细信息，请参阅[安装、更新首选解决方案](/dynamics365/project-service/upgrade-psa-home-page)。</span><span class="sxs-lookup"><span data-stu-id="eb8bf-108">For more information, see [Install, Update a Preferred Solution](/dynamics365/project-service/upgrade-psa-home-page).</span></span>
<span data-ttu-id="eb8bf-109">本主题列出了 PSA V3 更新版本 16 中新增或更改的功能和修复。</span><span class="sxs-lookup"><span data-stu-id="eb8bf-109">This topic lists the features and fixes that are new or changed for PSA V3, Update Release 16.</span></span> <span data-ttu-id="eb8bf-110">该版本的内部版本号为 V3.10.6.34，并且在 2020 年 1 月通过自行更新公开发布。</span><span class="sxs-lookup"><span data-stu-id="eb8bf-110">This version has a build number of V3.10.6.34 and is generally available through a self-update in January 2020.</span></span>


## <a name="update-release-16"></a><span data-ttu-id="eb8bf-111">更新发布 16</span><span class="sxs-lookup"><span data-stu-id="eb8bf-111">Update Release 16</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="eb8bf-112">提供错误修补程序</span><span class="sxs-lookup"><span data-stu-id="eb8bf-112">Bug fixes</span></span>

-   <span data-ttu-id="eb8bf-113">时间和支出</span><span class="sxs-lookup"><span data-stu-id="eb8bf-113">Time and Expense</span></span>

    -   <span data-ttu-id="eb8bf-114">已修复：尝试提交已删除时间和支出条目以供审批的用户现在将收到相关错误消息。</span><span class="sxs-lookup"><span data-stu-id="eb8bf-114">Fixed: Users attempting to submit deleted time and expense entries for approvals will now receive relevant error messages.</span></span>

-   <span data-ttu-id="eb8bf-115">项目管理</span><span class="sxs-lookup"><span data-stu-id="eb8bf-115">Project Management</span></span>

    -   <span data-ttu-id="eb8bf-116">已修复：采用了在模板中为团队成员定义的资源单位，并且对新项目应用了模板。</span><span class="sxs-lookup"><span data-stu-id="eb8bf-116">Fixed: The resourcing units defined for team members in templates are respected with the templates are applied to a new project.</span></span>

    -   <span data-ttu-id="eb8bf-117">已修复：改进了记录所有权重新分派的处理。</span><span class="sxs-lookup"><span data-stu-id="eb8bf-117">Fixed: Improved handling of the re-assignment of record ownership.</span></span>

    -   <span data-ttu-id="eb8bf-118">已修复：将不允许复制正在进行复制的项目，直到完成所有复制操作为止。</span><span class="sxs-lookup"><span data-stu-id="eb8bf-118">Fixed: Projects that are in the process of being copied will not be permitted to copied until all copy operations are complete.</span></span>

-   <span data-ttu-id="eb8bf-119">资源管理</span><span class="sxs-lookup"><span data-stu-id="eb8bf-119">Resource Management</span></span>

    -   <span data-ttu-id="eb8bf-120">已修复：扩展预订现在可正确处理较短持续时间，不会再为扩展预订创建零小时的持续时间。</span><span class="sxs-lookup"><span data-stu-id="eb8bf-120">Fixed: Extend bookings now handles short durations correctly and no longer creates zero hours for extended bookings.</span></span>

    -   <span data-ttu-id="eb8bf-121">已修复：现在，当项目时区为 +5:30 GMT 且用户的时区不同时，会呈现协调视图。</span><span class="sxs-lookup"><span data-stu-id="eb8bf-121">Fixed: The reconciliation view now renders when the project time zone is +5:30 GMT and the user’s time aone is different.</span></span>

-   <span data-ttu-id="eb8bf-122">Sales</span><span class="sxs-lookup"><span data-stu-id="eb8bf-122">Sales</span></span>

    -   <span data-ttu-id="eb8bf-123">已修复：在删除映射到合同子项的项目并映射新项目时，不会根据合同子项中定义的记帐和定价规则重新评估该新项目中的实际记录。</span><span class="sxs-lookup"><span data-stu-id="eb8bf-123">Fixed: When a project mapped to a contract line is removed and a new project is mapped, the actual records on the new project were not getting re-evaluated based on the billing and pricing rules defined on the contract line.</span></span> <span data-ttu-id="eb8bf-124">此版本中已修复该问题。</span><span class="sxs-lookup"><span data-stu-id="eb8bf-124">This has been fixed in this release.</span></span> <span data-ttu-id="eb8bf-125">根据合同子项的定价和记帐规则，新映射项目中的定价和实际记录将被正确冲销并重新创建。</span><span class="sxs-lookup"><span data-stu-id="eb8bf-125">Pricing and actual records on the newly mapped project will get reversed and re-created correctly based on the pricing and billing rules of the contract line.</span></span> <span data-ttu-id="eb8bf-126">未映射项目的实际记录也将被重新评估并重新创建为一项结果。</span><span class="sxs-lookup"><span data-stu-id="eb8bf-126">The actual records of the un-mapped project will also get re-evaluated and re-created as a consequence.</span></span>

    -   <span data-ttu-id="eb8bf-127">已修复：已将其他验证添加到评估行的 **金额** 字段中，以确保不会保留 null 值。</span><span class="sxs-lookup"><span data-stu-id="eb8bf-127">Fixed: Additional validation has been added to an estimate line’s **Amount** field to ensure that null values are not persisted.</span></span>

    -   <span data-ttu-id="eb8bf-128">已修复：对项目更新了实际值后，向项目主表单中添加了刷新按钮，以允许用户重新同步实际值。</span><span class="sxs-lookup"><span data-stu-id="eb8bf-128">Fixed: When actuals have been updated on a project, a refresh button has been added to the project main form to allow users to re-sync the actuals.</span></span>

    -   <span data-ttu-id="eb8bf-129">已修复：当用户从 2.X 升级到 3.X 时，将允许项目名称为 NULL 值的项目。</span><span class="sxs-lookup"><span data-stu-id="eb8bf-129">Fixed: When users upgrade from 2.X to 3.X, projects with a NULL value for project name will be permitted.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]