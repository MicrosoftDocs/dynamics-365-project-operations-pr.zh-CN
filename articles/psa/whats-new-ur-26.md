---
title: Project Service Automation V3 更新版本 26 中的新增功能或更改
description: 本主题列出了 Project Service Automation V3 更新版本 26 中可用的功能和修复。
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 01/12/2021
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
ms.openlocfilehash: 135f017533705e165230ac994d217ad7c58bab10
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/15/2021
ms.locfileid: "5280387"
---
# <a name="project-service-automation-update-release-26-v3"></a><span data-ttu-id="826db-103">Project Service Automation V3 更新版本 26</span><span class="sxs-lookup"><span data-stu-id="826db-103">Project Service Automation Update Release 26, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="826db-104">我们很高兴地宣布适用于 Dynamics 365 的 Project Service Automation 应用程序的最新更新已推出。</span><span class="sxs-lookup"><span data-stu-id="826db-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="826db-105">此版本包括对质量、性能和可用性的一些重要改进。</span><span class="sxs-lookup"><span data-stu-id="826db-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="826db-106">此版本与 Dynamics 365 9.x 兼容。</span><span class="sxs-lookup"><span data-stu-id="826db-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="826db-107">若要更新到此版本，请访问 Dynamics 365 Online 的管理中心解决方案页面以安装更新。</span><span class="sxs-lookup"><span data-stu-id="826db-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="826db-108">有关详细信息，请参阅[安装、更新或移除首选解决方案](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution)。</span><span class="sxs-lookup"><span data-stu-id="826db-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="826db-109">本主题列出了 Project Service Automation 更新版本 26 V3 中新增或更改的功能和修复。</span><span class="sxs-lookup"><span data-stu-id="826db-109">This topic lists the features and fixes that are new or changed for Project Service Automation Update Release 26, V3.</span></span> <span data-ttu-id="826db-110">此版本的内部版本号为 V3.10.44.59，通过 2020 年 12 月的自动更新公开发布。</span><span class="sxs-lookup"><span data-stu-id="826db-110">This version has a build number of V3.10.44.59 and is generally available through a self-update in December 2020.</span></span>

## <a name="update-release-26"></a><span data-ttu-id="826db-111">更新发布 26</span><span class="sxs-lookup"><span data-stu-id="826db-111">Update Release 26</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="826db-112">Bug 修复</span><span class="sxs-lookup"><span data-stu-id="826db-112">Bug fixes</span></span>

<span data-ttu-id="826db-113">**时间和支出**</span><span class="sxs-lookup"><span data-stu-id="826db-113">**Time and Expense**</span></span>

<span data-ttu-id="826db-114">已修复以下问题：</span><span class="sxs-lookup"><span data-stu-id="826db-114">The following issues have been fixed:</span></span>

- <span data-ttu-id="826db-115">用户可以对已批准/已提交的时间条目更改任务。</span><span class="sxs-lookup"><span data-stu-id="826db-115">Users are able to change the task on a time entry that has been approved/submitted.</span></span>
- <span data-ttu-id="826db-116">保存时间条目时发生“未设置对象引用”错误。</span><span class="sxs-lookup"><span data-stu-id="826db-116">"Object Reference Not Set" error when saving time entry.</span></span>
- <span data-ttu-id="826db-117">从资源分配中导入时间条目会创建日期/时间值不正确的时间条目。</span><span class="sxs-lookup"><span data-stu-id="826db-117">Time entry import from resource assignments creates time entries with the incorrect DateTime values.</span></span>
- <span data-ttu-id="826db-118">在安装了 Project Service Automation 和 Field Service 应用后，会针对 Field Service 应用中的时间条目在命令栏上显示两次 **新建** 按钮。</span><span class="sxs-lookup"><span data-stu-id="826db-118">When Project Service Automation and the Field Service app are both installed, the **New** button is displaying twice on the command bar for time entries in the Field Service app.</span></span>
- <span data-ttu-id="826db-119">**允许使用计价单位** 和 **计价单位组** 单元格更新现在对 **支出估算** 网格起作用。</span><span class="sxs-lookup"><span data-stu-id="826db-119">**Allow Unit** and **Unit group** cells updates now work on the **Expense Estimates** grid.</span></span>
- <span data-ttu-id="826db-120">**更新时间条目编辑** 窗体包含 **时间线**。</span><span class="sxs-lookup"><span data-stu-id="826db-120">**Update Time Entry Edit** form includes **Timeline**.</span></span>
- <span data-ttu-id="826db-121">在搜索项目审批者角色时，非项目时间条目的时间审批会阻止系统。</span><span class="sxs-lookup"><span data-stu-id="826db-121">Time approval for non-project time entries blocks the system when searching for a project approver role.</span></span>

<span data-ttu-id="826db-122">**资源管理**</span><span class="sxs-lookup"><span data-stu-id="826db-122">**Resource Management**</span></span>

<span data-ttu-id="826db-123">已修复以下问题：</span><span class="sxs-lookup"><span data-stu-id="826db-123">The following issues have been fixed:</span></span>

- <span data-ttu-id="826db-124">在 **PostProjectCreate** 插件中添加了验证，以在创建之前检查主要要求。</span><span class="sxs-lookup"><span data-stu-id="826db-124">Added validation in the **PostProjectCreate** plug-in to check for a primary requirement before creating one.</span></span>
- <span data-ttu-id="826db-125">如果从窗体中删除字段，则 **项目团队成员** 快速创建窗体会引发 null 引用异常。</span><span class="sxs-lookup"><span data-stu-id="826db-125">**Project Team Member** quick create form throws a null reference exception if fields are removed from the form.</span></span>
- <span data-ttu-id="826db-126">针对一年生成 12 小时的要求将失败。</span><span class="sxs-lookup"><span data-stu-id="826db-126">Generate requirements for 12 hours over 1 year will fail.</span></span>
- <span data-ttu-id="826db-127">改进了创建资源要求期间出现的错误消息 null 引用异常。</span><span class="sxs-lookup"><span data-stu-id="826db-127">Improved error message null reference exception during resource requirement creation.</span></span>

<span data-ttu-id="826db-128">**项目管理**</span><span class="sxs-lookup"><span data-stu-id="826db-128">**Project Management**</span></span>

<span data-ttu-id="826db-129">已修复以下问题：</span><span class="sxs-lookup"><span data-stu-id="826db-129">The following issues have been fixed:</span></span>

- <span data-ttu-id="826db-130">改进了验证以解决 **PreProjectUpdate** 插件中出现的 null 引用异常。</span><span class="sxs-lookup"><span data-stu-id="826db-130">Improved validation to address null reference exception generated in the **PreProjectUpdate** plug-in.</span></span>
- <span data-ttu-id="826db-131">Microsoft Project 桌面加载项发布的项目将删除未分配的工作。</span><span class="sxs-lookup"><span data-stu-id="826db-131">Projects published by the Microsoft Project desktop add-in delete unassigned assignments.</span></span>
- <span data-ttu-id="826db-132">由于 **PreValidateProjectTaskUpdate** 插件中出现 null 引用异常而在任务项目引用无效时添加了新验证。</span><span class="sxs-lookup"><span data-stu-id="826db-132">Added new validation when a task’s project reference is invalid due to null reference exception in **PreValidateProjectTaskUpdate** plug-in.</span></span>
- <span data-ttu-id="826db-133">团队成员网格不显示团队成员记录中的不同工作。</span><span class="sxs-lookup"><span data-stu-id="826db-133">Team Member grid does not show distinct assignments on the team member record.</span></span>
- <span data-ttu-id="826db-134">由于 **PreProjectTaskDelete** 插件中出现 null 引用异常而添加了新的验证和错误消息。</span><span class="sxs-lookup"><span data-stu-id="826db-134">Added new validation and error messages due to null reference exception in **PreProjectTaskDelete** plug-in.</span></span>

<span data-ttu-id="826db-135">**Sales**</span><span class="sxs-lookup"><span data-stu-id="826db-135">**Sales**</span></span>

<span data-ttu-id="826db-136">已修复以下问题：</span><span class="sxs-lookup"><span data-stu-id="826db-136">The following issues have been fixed:</span></span>

- <span data-ttu-id="826db-137">在报价单或合同中选择基于项目的行时，**建议** 按钮应仅在选择与现有产品关联的基于产品的行时才可见。</span><span class="sxs-lookup"><span data-stu-id="826db-137">When selecting a project-based line in quote or contract, the **Suggestion** button should only be visible when selecting a product-based line associated with an existing product.</span></span>
- <span data-ttu-id="826db-138">从 **Create_ProjectContract** 特权中分开了 **Create_Product** 特权。</span><span class="sxs-lookup"><span data-stu-id="826db-138">Split **Create_Product** privilege from **Create_ProjectContract** privilege.</span></span>
- <span data-ttu-id="826db-139">删除账单明细将导致 **MarkReadyToInvoiceForProductContractLineAfterDeletingInvoice** 上出现 null 引用错误。</span><span class="sxs-lookup"><span data-stu-id="826db-139">Deleting an invoice line causes null reference failure on **MarkReadyToInvoiceForProductContractLineAfterDeletingInvoice**.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]