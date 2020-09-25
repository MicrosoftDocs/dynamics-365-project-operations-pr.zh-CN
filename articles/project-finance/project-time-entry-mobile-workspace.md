---
title: 项目时间条目移动工作区
description: 此主题提供有关项目时间条目移动工作区的信息。 此工作区让用户可以使用其移动设备根据项目输入和保存时间。
author: KimANelson
manager: AnnBe
ms.date: 12/01/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 272101
ms.assetid: 4505f021-b9bb-4b87-be24-6bf0bd88ee60
ms.search.region: Global
ms.search.industry: Service industries
ms.author: knelson
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.openlocfilehash: ee11f7f392676adb59bd25f6549737482faf5fdb
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/24/2020
ms.locfileid: "3749717"
---
# <a name="project-time-entry-mobile-workspace"></a><span data-ttu-id="d5dd3-104">项目时间条目移动工作区</span><span class="sxs-lookup"><span data-stu-id="d5dd3-104">Project time entry mobile workspace</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d5dd3-105">此主题提供有关**项目时间条目**移动工作区的信息。</span><span class="sxs-lookup"><span data-stu-id="d5dd3-105">This topic provides information about the **Project time entry** mobile workspace.</span></span> <span data-ttu-id="d5dd3-106">此工作区让用户可以使用其移动设备根据项目输入和保存时间。</span><span class="sxs-lookup"><span data-stu-id="d5dd3-106">This workspace lets users enter and save time against a project by using their mobile device.</span></span>

<span data-ttu-id="d5dd3-107">此移动工作区用于与 Dynamics 365 for Unified Ops 移动应用一起使用。</span><span class="sxs-lookup"><span data-stu-id="d5dd3-107">This mobile workspace is intended to be used with the Dynamics 365 Unified Ops mobile app.</span></span> 

## <a name="overview"></a><span data-ttu-id="d5dd3-108">概述</span><span class="sxs-lookup"><span data-stu-id="d5dd3-108">Overview</span></span>
<span data-ttu-id="d5dd3-109">作为其日常工作的一部分，项目资源通常是在现场或出差。</span><span class="sxs-lookup"><span data-stu-id="d5dd3-109">As part of their daily work, project resources are often on-site or traveling.</span></span> <span data-ttu-id="d5dd3-110">**项目时间条目**移动工作区让用户可以在所选择的移动设备上根据项目输入计费或非计费时间。</span><span class="sxs-lookup"><span data-stu-id="d5dd3-110">The **Project time entry** mobile workspace lets users enter their billable or non-billable time against a project on the mobile device of their choice.</span></span> <span data-ttu-id="d5dd3-111">因此，项目资源可以随时随地记录时间条目。</span><span class="sxs-lookup"><span data-stu-id="d5dd3-111">Therefore, project resources can record time entries anytime and anywhere.</span></span> <span data-ttu-id="d5dd3-112">他们还可以查看已记录的时间条目。</span><span class="sxs-lookup"><span data-stu-id="d5dd3-112">They can also view time entries that have already been recorded.</span></span> 

<span data-ttu-id="d5dd3-113">具体而言，在**项目时间条目**移动工作区中，用户可以执行以下任务：</span><span class="sxs-lookup"><span data-stu-id="d5dd3-113">Specifically, in the **Project time entry** mobile workspace, users can perform these tasks:</span></span>

-   <span data-ttu-id="d5dd3-114">对于任何选择的日期，输入在特定任务上所用的工时数。</span><span class="sxs-lookup"><span data-stu-id="d5dd3-114">For any selected date, enter the number of hours that you spent on a specific task.</span></span>
-   <span data-ttu-id="d5dd3-115">按项目名称或客户搜索查找为其输入时间的项目。</span><span class="sxs-lookup"><span data-stu-id="d5dd3-115">Search by project name or customer to find the project to enter time for.</span></span>
-   <span data-ttu-id="d5dd3-116">指定您所用时间的类别和活动。</span><span class="sxs-lookup"><span data-stu-id="d5dd3-116">Specify the category and activity for the time that you spent.</span></span>
-   <span data-ttu-id="d5dd3-117">将项目时间记录为计费或非计费。</span><span class="sxs-lookup"><span data-stu-id="d5dd3-117">Record the time as billable or non-billable for the project.</span></span>
-   <span data-ttu-id="d5dd3-118">可以选择输入任何外部或内部注释。</span><span class="sxs-lookup"><span data-stu-id="d5dd3-118">Optionally enter any external or internal comments.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="d5dd3-119">先决条件</span><span class="sxs-lookup"><span data-stu-id="d5dd3-119">Prerequisites</span></span>
<span data-ttu-id="d5dd3-120">先决条件根据为您的组织部署的 Microsoft Dynamics 365 版本不同。</span><span class="sxs-lookup"><span data-stu-id="d5dd3-120">The prerequisites differ, based on the version of Microsoft Dynamics 365 that has been deployed for your organization.</span></span>

### <a name="prerequisites-if-you-use-dynamics-365-finance"></a><span data-ttu-id="d5dd3-121">使用 Dynamics 365 Finance 的先决条件</span><span class="sxs-lookup"><span data-stu-id="d5dd3-121">Prerequisites if you use Dynamics 365 Finance</span></span>
<span data-ttu-id="d5dd3-122">如果已经为您的组织部署 Finance，系统管理员必须发布**项目时间条目**移动工作区。</span><span class="sxs-lookup"><span data-stu-id="d5dd3-122">If Finance has been deployed for your organization, the system administrator must publish the **Project time entry** mobile workspace.</span></span> <span data-ttu-id="d5dd3-123">有关说明，请查阅 [发布移动工作区](../../dev-itpro/mobile-apps/publish-mobile-workspace.md)。</span><span class="sxs-lookup"><span data-stu-id="d5dd3-123">For instructions, see [Publish a mobile workspace](../../dev-itpro/mobile-apps/publish-mobile-workspace.md).</span></span>

### <a name="prerequisites-if-you-use-version-1611-with-platform-update-3-or-later"></a><span data-ttu-id="d5dd3-124">使用带平台更新 3 或更高版本的版本 1611 时的先决条件</span><span class="sxs-lookup"><span data-stu-id="d5dd3-124">Prerequisites if you use version 1611 with Platform update 3 or later</span></span>
<span data-ttu-id="d5dd3-125">如果已经为您的组织部署带平台更新 3 或更高版本的版本 1611，系统管理员必须完成以下先决条件。</span><span class="sxs-lookup"><span data-stu-id="d5dd3-125">If version 1611 with Platform update 3 or later has been deployed for your organization, the system administrator must complete the following prerequisites.</span></span> 

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="d5dd3-126">先决条件</span><span class="sxs-lookup"><span data-stu-id="d5dd3-126">Prerequisite</span></span></th>
<th><span data-ttu-id="d5dd3-127">角色</span><span class="sxs-lookup"><span data-stu-id="d5dd3-127">Role</span></span></th>
<th><span data-ttu-id="d5dd3-128">描述</span><span class="sxs-lookup"><span data-stu-id="d5dd3-128">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">

<td><span data-ttu-id="d5dd3-129">实现 KB 4018050。</span><span class="sxs-lookup"><span data-stu-id="d5dd3-129">Implement KB 4018050.</span></span></td>
<td><span data-ttu-id="d5dd3-130">系统管理员</span><span class="sxs-lookup"><span data-stu-id="d5dd3-130">System administrator</span></span></td>
<td><span data-ttu-id="d5dd3-131">KB 4018050 是包含<strong>项目时间条目</strong>移动工作区的 X++ 更新或元数据修补程序。</span><span class="sxs-lookup"><span data-stu-id="d5dd3-131">KB 4018050 is an X++ update or metadata hotfix that contains the <strong>Project time entry</strong> mobile workspace.</span></span> <span data-ttu-id="d5dd3-132">若要实施 KB 4018050，系统管理员必须遵循这些步骤。</span><span class="sxs-lookup"><span data-stu-id="d5dd3-132">To implement KB 4018050, your system administrator must follow these steps.</span></span>
<ol>
<li><span data-ttu-id="d5dd3-133"><a href="../../dev-itpro/migration-upgrade/download-hotfix-lcs.md">从 Microsoft Dynamics Lifecycle Services (LCS) 下载元数据修补程序</a>。</span><span class="sxs-lookup"><span data-stu-id="d5dd3-133"><a href="../../dev-itpro/migration-upgrade/download-hotfix-lcs.md">Download the metadata hotfix from Microsoft Dynamics Lifecycle Services (LCS)</a>.</span></span></li>
<li><span data-ttu-id="d5dd3-134"><a href="../../dev-itpro/migration-upgrade/install-metadata-hotfix-package.md">安装元数据修补程序</a>。</span><span class="sxs-lookup"><span data-stu-id="d5dd3-134"><a href="../../dev-itpro/migration-upgrade/install-metadata-hotfix-package.md">Install the metadata hotfix</a>.</span></span></li>
<li><span data-ttu-id="d5dd3-135"><a href="../../dev-itpro/deployment/create-apply-deployable-package.md">创建</a>包含 <strong>ApplicationSuite</strong> 和 <strong>ProjectMobile</strong> 模型的可部署包，然后将可部署包上载到 LCS。</span><span class="sxs-lookup"><span data-stu-id="d5dd3-135"><a href="../../dev-itpro/deployment/create-apply-deployable-package.md">Create a deployable package</a> that contains the <strong>ApplicationSuite</strong> and <strong>ProjectMobile</strong> models, and then upload the deployable package to LCS.</span></span></li>
<li><span data-ttu-id="d5dd3-136"><a href="../../dev-itpro/deployment/apply-deployable-package-system.md">应用可部署包</a>。</span><span class="sxs-lookup"><span data-stu-id="d5dd3-136"><a href="../../dev-itpro/deployment/apply-deployable-package-system.md">Apply the deployable package</a>.</span></span></li>

</ol></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d5dd3-137">发布<strong>项目时间条目</strong>移动工作区。</span><span class="sxs-lookup"><span data-stu-id="d5dd3-137">Publish the <strong>Project time entry</strong> mobile workspace.</span></span></td>
<td><span data-ttu-id="d5dd3-138">系统管理员</span><span class="sxs-lookup"><span data-stu-id="d5dd3-138">System administrator</span></span></td>
<td><span data-ttu-id="d5dd3-139">请查阅<a href="../../dev-itpro/mobile-apps/publish-mobile-workspace.md">发布移动工作区</a>。</span><span class="sxs-lookup"><span data-stu-id="d5dd3-139">See <a href="../../dev-itpro/mobile-apps/publish-mobile-workspace.md">Publish a mobile workspace</a>.</span></span></td>
</tr>
</tbody>
</table>

## <a name="download-and-install-the-mobile-app"></a><span data-ttu-id="d5dd3-140">下载并安装移动应用</span><span class="sxs-lookup"><span data-stu-id="d5dd3-140">Download and install the mobile app</span></span>

<span data-ttu-id="d5dd3-141">下载并安装 Finance and Operations 移动应用：</span><span class="sxs-lookup"><span data-stu-id="d5dd3-141">Download and install the Finance and Operations mobile app:</span></span>

-   [<span data-ttu-id="d5dd3-142">适用于 Android 手机</span><span class="sxs-lookup"><span data-stu-id="d5dd3-142">For Android phones</span></span>](https://go.microsoft.com/fwlink/?linkid=850662)
-   [<span data-ttu-id="d5dd3-143">适用于 iPhones</span><span class="sxs-lookup"><span data-stu-id="d5dd3-143">For iPhones</span></span>](https://go.microsoft.com/fwlink/?linkid=850663)

## <a name="sign-in-to-the-mobile-app"></a><span data-ttu-id="d5dd3-144">登录到移动应用</span><span class="sxs-lookup"><span data-stu-id="d5dd3-144">Sign in to the mobile app</span></span>
1.  <span data-ttu-id="d5dd3-145">在移动设备上启动应用程序。</span><span class="sxs-lookup"><span data-stu-id="d5dd3-145">Start the app on your mobile device.</span></span>
2.  <span data-ttu-id="d5dd3-146">输入您的 Dynamics 365 URL。</span><span class="sxs-lookup"><span data-stu-id="d5dd3-146">Enter your Dynamics 365 URL.</span></span>
3.  <span data-ttu-id="d5dd3-147">首次登录时，将提示您输入您的用户名和密码。</span><span class="sxs-lookup"><span data-stu-id="d5dd3-147">The first time that you sign in, you're prompted for your user name and password.</span></span> <span data-ttu-id="d5dd3-148">输入凭据。</span><span class="sxs-lookup"><span data-stu-id="d5dd3-148">Enter your credentials.</span></span>
4.  <span data-ttu-id="d5dd3-149">登录后，将显示您的公司的可用工作区。</span><span class="sxs-lookup"><span data-stu-id="d5dd3-149">After you sign in, the available workspaces for your company are shown.</span></span> <span data-ttu-id="d5dd3-150">请注意，如果您的系统管理员以后发布新工作区，您必须刷新移动工作区列表。</span><span class="sxs-lookup"><span data-stu-id="d5dd3-150">Note that if your system administrator publishes a new workspace later, you will have to refresh the list of mobile workspaces.</span></span>

<span data-ttu-id="d5dd3-151">[![下拉以刷新](./media/pull-to-refresh-list-of-workspaces-183x300.png)](./media/pull-to-refresh-list-of-workspaces.png)</span><span class="sxs-lookup"><span data-stu-id="d5dd3-151">[![Pull to refresh](./media/pull-to-refresh-list-of-workspaces-183x300.png)](./media/pull-to-refresh-list-of-workspaces.png)</span></span>

## <a name="enter-time-by-using-the-project-time-entry-mobile-workspace"></a><span data-ttu-id="d5dd3-152">通过使用项目时间条目移动工作区输入时间</span><span class="sxs-lookup"><span data-stu-id="d5dd3-152">Enter time by using the Project time entry mobile workspace</span></span>
1.  <span data-ttu-id="d5dd3-153">在移动设备上，选择**项目时间条目**工作区。</span><span class="sxs-lookup"><span data-stu-id="d5dd3-153">On your mobile device, select the **Project time entry** workspace.</span></span>
2.  <span data-ttu-id="d5dd3-154">选择**时间条目**。</span><span class="sxs-lookup"><span data-stu-id="d5dd3-154">Select **Time entry**.</span></span> <span data-ttu-id="d5dd3-155">此时将显示当前周的日历日期。</span><span class="sxs-lookup"><span data-stu-id="d5dd3-155">The calendar dates for the current week are shown.</span></span>
3.  <span data-ttu-id="d5dd3-156">对于所选日期，选择**操作**&gt;**新条目**。</span><span class="sxs-lookup"><span data-stu-id="d5dd3-156">For a selected date, select **Actions** &gt; **New entry**.</span></span>
4.  <span data-ttu-id="d5dd3-157">输入要记录的小时数。</span><span class="sxs-lookup"><span data-stu-id="d5dd3-157">Enter the number of hours to record.</span></span>
5.  <span data-ttu-id="d5dd3-158">为时间条目选择项目。</span><span class="sxs-lookup"><span data-stu-id="d5dd3-158">Select the project for the time entry.</span></span> <span data-ttu-id="d5dd3-159">列表显示加载到您的应用程序中供脱机使用的项目。</span><span class="sxs-lookup"><span data-stu-id="d5dd3-159">A list shows the projects that are loaded into your app for offline use.</span></span> <span data-ttu-id="d5dd3-160">默认情况下，加载 50 项，但是开发人员可以更改此数字。</span><span class="sxs-lookup"><span data-stu-id="d5dd3-160">By default, 50 items are loaded, but a developer can change this number.</span></span> <span data-ttu-id="d5dd3-161">有关详细信息，请参阅 [移动平台](../../dev-itpro/mobile-apps/platform/mobile-platform-home-page.md)。</span><span class="sxs-lookup"><span data-stu-id="d5dd3-161">For more information, see [Mobile platform](../../dev-itpro/mobile-apps/platform/mobile-platform-home-page.md).</span></span>
6.  <span data-ttu-id="d5dd3-162">如果您的项目不在该列表中，请选择**搜索**。</span><span class="sxs-lookup"><span data-stu-id="d5dd3-162">If your project isn't in the list, select **Search**.</span></span> <span data-ttu-id="d5dd3-163">按名称搜索，或切换到按项目名称或客户搜索。</span><span class="sxs-lookup"><span data-stu-id="d5dd3-163">Search by name, or switch to search by project name or customer.</span></span>
7.  <span data-ttu-id="d5dd3-164">选择类别。</span><span class="sxs-lookup"><span data-stu-id="d5dd3-164">Select a category.</span></span> <span data-ttu-id="d5dd3-165">列表显示加载到您的应用程序中供脱机使用的类别。</span><span class="sxs-lookup"><span data-stu-id="d5dd3-165">A list shows the categories that are loaded into your app for offline use.</span></span> <span data-ttu-id="d5dd3-166">默认情况下，加载 50 项，但是开发人员可以更改此数字。</span><span class="sxs-lookup"><span data-stu-id="d5dd3-166">By default, 50 items are loaded, but a developer can change this number.</span></span> <span data-ttu-id="d5dd3-167">有关详细信息，请参阅 [移动平台](../../dev-itpro/mobile-apps/platform/mobile-platform-home-page.md)。</span><span class="sxs-lookup"><span data-stu-id="d5dd3-167">For more information, see [Mobile platform](../../dev-itpro/mobile-apps/platform/mobile-platform-home-page.md).</span></span>
8.  <span data-ttu-id="d5dd3-168">如果您的类别不在该列表中，请选择**搜索**。</span><span class="sxs-lookup"><span data-stu-id="d5dd3-168">If your category isn't in the list, select **Search**.</span></span> <span data-ttu-id="d5dd3-169">按类别搜索，或切换到按类别名称搜索。</span><span class="sxs-lookup"><span data-stu-id="d5dd3-169">Search by category, or switch to search by category name.</span></span>
9.  <span data-ttu-id="d5dd3-170">选择活动。</span><span class="sxs-lookup"><span data-stu-id="d5dd3-170">Select an activity.</span></span> <span data-ttu-id="d5dd3-171">列表显示加载到您的应用程序中供脱机使用的活动。</span><span class="sxs-lookup"><span data-stu-id="d5dd3-171">A list shows the activities that are loaded into your app for offline use.</span></span> <span data-ttu-id="d5dd3-172">默认情况下，加载 50 项，但是开发人员可以更改此数字。</span><span class="sxs-lookup"><span data-stu-id="d5dd3-172">By default, 50 items are loaded, but a developer can change this number.</span></span> <span data-ttu-id="d5dd3-173">有关详细信息，请参阅 [移动平台](../../dev-itpro/mobile-apps/platform/mobile-platform-home-page.md)。</span><span class="sxs-lookup"><span data-stu-id="d5dd3-173">For more information, see [Mobile platform](../../dev-itpro/mobile-apps/platform/mobile-platform-home-page.md).</span></span>
10. <span data-ttu-id="d5dd3-174">如果您的活动不在该列表中，请选择**搜索**。</span><span class="sxs-lookup"><span data-stu-id="d5dd3-174">If your activity isn't in the list, select **Search**.</span></span> <span data-ttu-id="d5dd3-175">按活动编号搜索，或切换到按用途搜索。</span><span class="sxs-lookup"><span data-stu-id="d5dd3-175">Search by activity number, or switch to search by purpose.</span></span>

11. <span data-ttu-id="d5dd3-176">选择行属性。</span><span class="sxs-lookup"><span data-stu-id="d5dd3-176">Select the line property.</span></span>
12. <span data-ttu-id="d5dd3-177">可选：输入任何外部和内部注释。</span><span class="sxs-lookup"><span data-stu-id="d5dd3-177">Optional: Enter any external and internal comments.</span></span>
13. <span data-ttu-id="d5dd3-178">选择**完成**。</span><span class="sxs-lookup"><span data-stu-id="d5dd3-178">Select **Done**.</span></span>