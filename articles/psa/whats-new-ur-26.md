---
title: Project Service Automation V3 更新版本 26 中的新增功能或更改
ms.openlocfilehash: 849e7288ee91d3e9360c0b03f6b8b37ff29338e7
ms.sourcegitcommit: 573be7e36604ace82b35e439cfa748aa7c587415
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/25/2020
ms.locfileid: "4643252"
---
<a name="project-service-automation-update-release-26-v3"></a><span data-ttu-id="cebdb-102">Project Service Automation V3 更新版本 26</span><span class="sxs-lookup"><span data-stu-id="cebdb-102">Project Service Automation Update Release 26, V3</span></span>
================================================

<span data-ttu-id="cebdb-103">我们很高兴地宣布适用于 Dynamics 365 的 Project Service Automation 应用程序的最新更新已推出。</span><span class="sxs-lookup"><span data-stu-id="cebdb-103">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="cebdb-104">此版本包括对质量、性能和可用性的一些重要改进。</span><span class="sxs-lookup"><span data-stu-id="cebdb-104">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="cebdb-105">此版本与 Dynamics 365 9.x 兼容。</span><span class="sxs-lookup"><span data-stu-id="cebdb-105">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="cebdb-106">若要更新到此版本，请访问 Dynamics 365 Online 的管理中心解决方案页面以安装更新。</span><span class="sxs-lookup"><span data-stu-id="cebdb-106">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="cebdb-107">有关详细信息，请参阅[安装、更新或移除首选解决方案](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution)。</span><span class="sxs-lookup"><span data-stu-id="cebdb-107">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="cebdb-108">本主题列出了 Project Service Automation 更新版本 26 V3 中新增或更改的功能和修复。</span><span class="sxs-lookup"><span data-stu-id="cebdb-108">This topic lists the features and fixes that are new or changed for Project Service Automation Update Release 26, V3.</span></span> <span data-ttu-id="cebdb-109">此版本的内部版本号为 V3.10.44.59，通过 2020 年 12 月的自动更新公开发布。</span><span class="sxs-lookup"><span data-stu-id="cebdb-109">This version has a build number of V3.10.44.59 and is generally available through a self-update in December 2020.</span></span>

<a name="update-release-26"></a><span data-ttu-id="cebdb-110">更新发布 26</span><span class="sxs-lookup"><span data-stu-id="cebdb-110">Update Release 26</span></span>
-----------------

### <a name="bug-fixes"></a><span data-ttu-id="cebdb-111">Bug 修复</span><span class="sxs-lookup"><span data-stu-id="cebdb-111">Bug fixes</span></span>

<span data-ttu-id="cebdb-112">**时间和支出**</span><span class="sxs-lookup"><span data-stu-id="cebdb-112">**Time and Expense**</span></span>

<span data-ttu-id="cebdb-113">已修复以下问题：</span><span class="sxs-lookup"><span data-stu-id="cebdb-113">The following issues have been fixed:</span></span>

-   <span data-ttu-id="cebdb-114">用户可以对已批准/已提交的时间条目更改任务。</span><span class="sxs-lookup"><span data-stu-id="cebdb-114">Users are able to change the task on a time entry that has been approved/submitted.</span></span>

-   <span data-ttu-id="cebdb-115">保存时间条目时发生“未设置对象引用”错误。</span><span class="sxs-lookup"><span data-stu-id="cebdb-115">"Object Reference Not Set" error when saving time entry.</span></span>

-   <span data-ttu-id="cebdb-116">从资源分配中导入时间条目会创建日期/时间值不正确的时间条目。</span><span class="sxs-lookup"><span data-stu-id="cebdb-116">Time entry import from resource assignments creates time entries with the incorrect DateTime values.</span></span>

-   <span data-ttu-id="cebdb-117">在安装了 Project Service Automation 和 Field Service 应用后，会针对 Field Service 应用中的时间条目在命令栏上显示两次 **新建** 按钮。</span><span class="sxs-lookup"><span data-stu-id="cebdb-117">When Project Service Automation and the Field Service app are both installed, the **New** button is displaying twice on the command bar for time entries in the Field Service app.</span></span>

-   <span data-ttu-id="cebdb-118">**允许使用计价单位** 和 **计价单位组** 单元格更新现在对 **支出估算** 网格起作用。</span><span class="sxs-lookup"><span data-stu-id="cebdb-118">**Allow Unit** and **Unit group** cells updates now work on the **Expense Estimates** grid.</span></span>

-   <span data-ttu-id="cebdb-119">**更新时间条目编辑** 窗体包含 **时间线**。</span><span class="sxs-lookup"><span data-stu-id="cebdb-119">**Update Time Entry Edit** form includes **Timeline**.</span></span>

-   <span data-ttu-id="cebdb-120">在搜索项目审批者角色时，非项目时间条目的时间审批会阻止系统。</span><span class="sxs-lookup"><span data-stu-id="cebdb-120">Time approval for non-project time entries blocks the system when searching for a project approver role.</span></span>

<span data-ttu-id="cebdb-121">**资源管理**</span><span class="sxs-lookup"><span data-stu-id="cebdb-121">**Resource Management**</span></span>

<span data-ttu-id="cebdb-122">已修复以下问题：</span><span class="sxs-lookup"><span data-stu-id="cebdb-122">The following issues have been fixed:</span></span>

-   <span data-ttu-id="cebdb-123">在 **PostProjectCreate** 插件中添加了验证，以在创建之前检查主要要求。</span><span class="sxs-lookup"><span data-stu-id="cebdb-123">Added validation in the **PostProjectCreate** plug-in to check for a primary requirement before creating one.</span></span>

-   <span data-ttu-id="cebdb-124">如果从窗体中删除字段，则 **项目团队成员** 快速创建窗体会引发 null 引用异常。</span><span class="sxs-lookup"><span data-stu-id="cebdb-124">**Project Team Member** quick create form throws a null reference exception if fields are removed from the form.</span></span>

-   <span data-ttu-id="cebdb-125">针对一年生成 12 小时的要求将失败。</span><span class="sxs-lookup"><span data-stu-id="cebdb-125">Generate requirements for 12 hours over 1 year will fail.</span></span>

-   <span data-ttu-id="cebdb-126">改进了创建资源要求期间出现的错误消息 null 引用异常。</span><span class="sxs-lookup"><span data-stu-id="cebdb-126">Improved error message null reference exception during resource requirement creation.</span></span>

<span data-ttu-id="cebdb-127">**项目管理**</span><span class="sxs-lookup"><span data-stu-id="cebdb-127">**Project Management**</span></span>

<span data-ttu-id="cebdb-128">已修复以下问题：</span><span class="sxs-lookup"><span data-stu-id="cebdb-128">The following issues have been fixed:</span></span>

-   <span data-ttu-id="cebdb-129">改进了验证以解决 **PreProjectUpdate** 插件中出现的 null 引用异常。</span><span class="sxs-lookup"><span data-stu-id="cebdb-129">Improved validation to address null reference exception generated in the **PreProjectUpdate** plug-in.</span></span>

-   <span data-ttu-id="cebdb-130">Microsoft Project 桌面加载项发布的项目将删除未分配的工作。</span><span class="sxs-lookup"><span data-stu-id="cebdb-130">Projects published by the Microsoft Project desktop add-in delete unassigned assignments.</span></span>

-   <span data-ttu-id="cebdb-131">由于 **PreValidateProjectTaskUpdate** 插件中出现 null 引用异常而在任务项目引用无效时添加了新验证。</span><span class="sxs-lookup"><span data-stu-id="cebdb-131">Added new validation when a task’s project reference is invalid due to null reference exception in **PreValidateProjectTaskUpdate** plug-in.</span></span>

-   <span data-ttu-id="cebdb-132">团队成员网格不显示团队成员记录中的不同工作。</span><span class="sxs-lookup"><span data-stu-id="cebdb-132">Team Member grid does not show distinct assignments on the team member record.</span></span>

-   <span data-ttu-id="cebdb-133">由于 **PreProjectTaskDelete** 插件中出现 null 引用异常而添加了新的验证和错误消息。</span><span class="sxs-lookup"><span data-stu-id="cebdb-133">Added new validation and error messages due to null reference exception in **PreProjectTaskDelete** plug-in.</span></span>

<span data-ttu-id="cebdb-134">**Sales**</span><span class="sxs-lookup"><span data-stu-id="cebdb-134">**Sales**</span></span>

<span data-ttu-id="cebdb-135">已修复以下问题：</span><span class="sxs-lookup"><span data-stu-id="cebdb-135">The following issues have been fixed:</span></span>

-   <span data-ttu-id="cebdb-136">在报价单或合同中选择基于项目的行时，**建议** 按钮应仅在选择与现有产品关联的基于产品的行时才可见。</span><span class="sxs-lookup"><span data-stu-id="cebdb-136">When selecting a project-based line in quote or contract, the **Suggestion** button should only be visible when selecting a product-based line associated with an existing product.</span></span>

-   <span data-ttu-id="cebdb-137">从 **Create_ProjectContract** 特权中分开了 **Create_Product** 特权。</span><span class="sxs-lookup"><span data-stu-id="cebdb-137">Split **Create_Product** privilege from **Create_ProjectContract** privilege.</span></span>

-   <span data-ttu-id="cebdb-138">删除账单明细将导致 **MarkReadyToInvoiceForProductContractLineAfterDeletingInvoice** 上出现 null 引用错误。</span><span class="sxs-lookup"><span data-stu-id="cebdb-138">Deleting an invoice line causes null reference failure on **MarkReadyToInvoiceForProductContractLineAfterDeletingInvoice**.</span></span>
