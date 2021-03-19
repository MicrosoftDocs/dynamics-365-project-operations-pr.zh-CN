---
title: 在 Finance 环境中更新 Project Operations
description: 本主题提供有关如何在 Dynamics 365 Finance 环境中更新 Project Operations 的信息。
author: ruhercul
manager: tfehr
ms.date: 12/11/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: d68296ec59f0bd58f848154c90e02c58f275ab12
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/15/2021
ms.locfileid: "5291968"
---
# <a name="update-project-operations-in-your-finance-environment"></a><span data-ttu-id="d7d6a-103">在 Finance 环境中更新 Project Operations</span><span class="sxs-lookup"><span data-stu-id="d7d6a-103">Update Project Operations in your Finance environment</span></span>

<span data-ttu-id="d7d6a-104">_**适用于：** 面向资源/非库存场景的 Project Operations_</span><span class="sxs-lookup"><span data-stu-id="d7d6a-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>


<span data-ttu-id="d7d6a-105">本主题提供有关如何在 Dynamics 365 Finance 环境中更新 Dynamics 365 Project Operations 的信息。</span><span class="sxs-lookup"><span data-stu-id="d7d6a-105">This topic provides information about how to update Dynamics 365 Project Operations in your Dynamics 365 Finance environment.</span></span> <span data-ttu-id="d7d6a-106">将 Project Operations 更新为更新 5 (UR5) 需要三个过程：</span><span class="sxs-lookup"><span data-stu-id="d7d6a-106">There are three procedures that are required to update Project Operations to Update 5 (UR5):</span></span>

- [<span data-ttu-id="d7d6a-107">将包导入预览项目</span><span class="sxs-lookup"><span data-stu-id="d7d6a-107">Import the package into your preview project</span></span>](#import)
- [<span data-ttu-id="d7d6a-108">应用更新</span><span class="sxs-lookup"><span data-stu-id="d7d6a-108">Apply the update</span></span>](#apply)
- [<span data-ttu-id="d7d6a-109">更新 Dataverse 环境</span><span class="sxs-lookup"><span data-stu-id="d7d6a-109">Update your Dataverse environment</span></span>](#update)

## <a name="import-the-package-into-your-lcs-project"></a><a name="import"></a><span data-ttu-id="d7d6a-110">将包导入 LCS 项目</span><span class="sxs-lookup"><span data-stu-id="d7d6a-110">Import the package into your LCS project</span></span>

1. <span data-ttu-id="d7d6a-111">作为项目负责人或环境经理登录到 [Lifecycle Services (LCS)](https://lcs.dynamics.com/)。</span><span class="sxs-lookup"><span data-stu-id="d7d6a-111">Sign in to [Lifecycle Services (LCS)](https://lcs.dynamics.com/) as a Project Owner or Environment manager.</span></span>
2. <span data-ttu-id="d7d6a-112">从项目列表中，选择您的 LCS 项目。</span><span class="sxs-lookup"><span data-stu-id="d7d6a-112">From the list of projects, select your LCS project.</span></span>
3. <span data-ttu-id="d7d6a-113">在 **项目** 页上的 **环境** 组中，打开要更新的环境。</span><span class="sxs-lookup"><span data-stu-id="d7d6a-113">On the **Project** page, in the **Environments** group, open the environment that you want to update.</span></span>
4. <span data-ttu-id="d7d6a-114">验证环境是否正在运行。</span><span class="sxs-lookup"><span data-stu-id="d7d6a-114">Verify that the environment is running.</span></span> <span data-ttu-id="d7d6a-115">如果未启动，请启动该环境。</span><span class="sxs-lookup"><span data-stu-id="d7d6a-115">If it isn't started, start the environment.</span></span>
5. <span data-ttu-id="d7d6a-116">在 **可用更新** 下的 **新版本** 部分，选择 10.0.15 对应的 **查看更新**。</span><span class="sxs-lookup"><span data-stu-id="d7d6a-116">In the **New release** section under **Available updates**, select **View update** for 10.0.15.</span></span>

![查看更新按钮](media/view-update.png)

6. <span data-ttu-id="d7d6a-118">在 **二进制更新** 页上，选择 **保存包**。</span><span class="sxs-lookup"><span data-stu-id="d7d6a-118">On the **Binary updates** page, select **Save package**.</span></span>
7. <span data-ttu-id="d7d6a-119">在 **查看和保存更新** 页上，选择 **保存包**。</span><span class="sxs-lookup"><span data-stu-id="d7d6a-119">On the **Review and save updates** page, select **Save package**.</span></span>
8. <span data-ttu-id="d7d6a-120">在打开的 **将包保存到资产库** 窗格中，输入包名称，然后选择 **保存包**。</span><span class="sxs-lookup"><span data-stu-id="d7d6a-120">On the **Save package to asset library** pane that opens, enter the package name and then select **Save package**.</span></span>
9. <span data-ttu-id="d7d6a-121">LCS 保存完包后，**完成** 按钮将启用。</span><span class="sxs-lookup"><span data-stu-id="d7d6a-121">When LCS has finished saving the package, the **Done** button is enabled.</span></span> <span data-ttu-id="d7d6a-122">选择 **完成**。</span><span class="sxs-lookup"><span data-stu-id="d7d6a-122">Select **Done**.</span></span> <span data-ttu-id="d7d6a-123">LCS 将验证包。</span><span class="sxs-lookup"><span data-stu-id="d7d6a-123">LCS will verify the package.</span></span> <span data-ttu-id="d7d6a-124">验证可能花几分钟，最多一小时。</span><span class="sxs-lookup"><span data-stu-id="d7d6a-124">Verification can take a few minutes or up to one hour.</span></span>


## <a name="apply-the-package-update"></a><a name="apply"></a><span data-ttu-id="d7d6a-125">应用包更新</span><span class="sxs-lookup"><span data-stu-id="d7d6a-125">Apply the package update</span></span>

1. <span data-ttu-id="d7d6a-126">在 LCS 中的 **环境详细信息** 页上，选择 **维护** > **应用更新**。</span><span class="sxs-lookup"><span data-stu-id="d7d6a-126">In LCS, on the **Environment details** page, select **Maintain** > **Apply Updates**.</span></span>
2. <span data-ttu-id="d7d6a-127">在列表中，选择之前保存的包，然后选择 **应用**。</span><span class="sxs-lookup"><span data-stu-id="d7d6a-127">From the list, select the package that you saved earlier, and then select **Apply**.</span></span>
3. <span data-ttu-id="d7d6a-128">选择 **是** 确认您要部署该包。</span><span class="sxs-lookup"><span data-stu-id="d7d6a-128">Select **Yes** to confirm that you want to deploy the package.</span></span>

![确认包部署对话框](media/confirm-package-deployment.png)

4. <span data-ttu-id="d7d6a-130">选择 **是** 确认您要更新应用程序。</span><span class="sxs-lookup"><span data-stu-id="d7d6a-130">Select **Yes** to confirm that you want to update the application.</span></span>

![确认应用程序更新对话框](media/confirm-application-update.png)

<span data-ttu-id="d7d6a-132">部署和应用程序更新将开始。</span><span class="sxs-lookup"><span data-stu-id="d7d6a-132">The deployment and application update will start.</span></span> 

<span data-ttu-id="d7d6a-133">在 **环境详细信息** 页的右上角，环境状态将更新为 **服务**。</span><span class="sxs-lookup"><span data-stu-id="d7d6a-133">On the **Environment details** page, in the top-right corner, the environment status will update to **Servicing**.</span></span> <span data-ttu-id="d7d6a-134">大约两个小时后，更新将完成。</span><span class="sxs-lookup"><span data-stu-id="d7d6a-134">In approximately two hours, the update will be complete.</span></span> <span data-ttu-id="d7d6a-135">应用程序版本信息将更新为 **Microsoft Dynamics 365 for Finance and Operations 10.0.15)**，环境状态将更新为 **已部署**。</span><span class="sxs-lookup"><span data-stu-id="d7d6a-135">The application release information will update to **Microsoft Dynamics 365 for Finance and Operations 10.0.15)** and the environment status will update to **Deployed**.</span></span>


## <a name="update-your-dataverse-environment"></a><a name="update"></a><span data-ttu-id="d7d6a-136">更新 Dataverse 环境</span><span class="sxs-lookup"><span data-stu-id="d7d6a-136">Update your Dataverse environment</span></span>

1. <span data-ttu-id="d7d6a-137">登录 [Power Platform 管理中心](https://admin.powerplatform.com/)。</span><span class="sxs-lookup"><span data-stu-id="d7d6a-137">Sign in to the [Power Platform admin center](https://admin.powerplatform.com/).</span></span>
2. <span data-ttu-id="d7d6a-138">在列表中，查找并打开用于安装 Project Operations 的环境。</span><span class="sxs-lookup"><span data-stu-id="d7d6a-138">In the list, find and open the environment that you used to install Project Operations.</span></span>
3. <span data-ttu-id="d7d6a-139">在 **环境** 页上，选择 **资源** > **Dynamics 365 应用**。</span><span class="sxs-lookup"><span data-stu-id="d7d6a-139">On the **Environments** page, select **Resource** > **Dynamics 365 apps**.</span></span>
4. <span data-ttu-id="d7d6a-140">在列表中，找到 **Microsoft Dynamics 365 Project Operations**，在 **状态** 列中，选择 **有可用更新**。</span><span class="sxs-lookup"><span data-stu-id="d7d6a-140">In the list, locate **Microsoft Dynamics 365 Project Operations**, and in the **Status** column, select **Update Available**.</span></span>
5. <span data-ttu-id="d7d6a-141">选中 **我同意服务条款** 复选框，然后选择 **更新**。</span><span class="sxs-lookup"><span data-stu-id="d7d6a-141">Select the **I agree to the terms of service** check box, and then select **Update**.</span></span> <span data-ttu-id="d7d6a-142">将安装解决方案的最新版本。</span><span class="sxs-lookup"><span data-stu-id="d7d6a-142">The latest version of the solution will be installed.</span></span>

<span data-ttu-id="d7d6a-143">安装完成后，您已安装了版本 4.5.0.134。</span><span class="sxs-lookup"><span data-stu-id="d7d6a-143">After the installation is complete, you'll have version 4.5.0.134 installed.</span></span>

## <a name="configure-new-features"></a><span data-ttu-id="d7d6a-144">配置新功能</span><span class="sxs-lookup"><span data-stu-id="d7d6a-144">Configure new features</span></span>

### <a name="enable-dual-write-mapping"></a><span data-ttu-id="d7d6a-145">启用双重写入映射</span><span class="sxs-lookup"><span data-stu-id="d7d6a-145">Enable dual-write mapping</span></span>

<span data-ttu-id="d7d6a-146">在 Finance 和 Dataverse 环境上完成更新后，可以启用所需的双重写入映射。</span><span class="sxs-lookup"><span data-stu-id="d7d6a-146">After you complete the update on the Finance and Dataverse environments, you can enable the required dual-write mappings.</span></span> <span data-ttu-id="d7d6a-147">完成以下过程启用双重写入映射。</span><span class="sxs-lookup"><span data-stu-id="d7d6a-147">Complete the following procedures to enable dual-write mappings.</span></span>

- [<span data-ttu-id="d7d6a-148">更新 Customer Engagement 环境的安全设置</span><span class="sxs-lookup"><span data-stu-id="d7d6a-148">Update security settings on Customer Engagement environment</span></span>](#security)
- [<span data-ttu-id="d7d6a-149">刷新数据实体</span><span class="sxs-lookup"><span data-stu-id="d7d6a-149">Refresh data entities</span></span>](#refresh)
- [<span data-ttu-id="d7d6a-150">更新和运行双重写入映射</span><span class="sxs-lookup"><span data-stu-id="d7d6a-150">Update and run the dual-write mappings</span></span>](#run)

### <a name="update-security-settings-on-the-dataverse-environment"></a><a name="security"></a><span data-ttu-id="d7d6a-151">更新 Dataverse 环境的安全设置</span><span class="sxs-lookup"><span data-stu-id="d7d6a-151">Update security settings on the Dataverse environment</span></span>

<span data-ttu-id="d7d6a-152">对实体的安全特权的以下更新是更新 UR5 所必需的。</span><span class="sxs-lookup"><span data-stu-id="d7d6a-152">The following updates to the security privileges for entities are required as part of the update to UR5.</span></span>

1. <span data-ttu-id="d7d6a-153">在 Dataverse 环境中，转到 **设置**，在 **系统** 组中，选择 **安全**。</span><span class="sxs-lookup"><span data-stu-id="d7d6a-153">In your Dataverse environment, go to **Settings**, and in the **System** group, select **Security**.</span></span>

![Dataverse 环境设置](media/Picture21.png)

2. <span data-ttu-id="d7d6a-155">选择 **安全角色**。</span><span class="sxs-lookup"><span data-stu-id="d7d6a-155">Select **Security Roles**.</span></span>
3. <span data-ttu-id="d7d6a-156">在角色列表中，选择 **双重写入应用用户**，然后选择 **自定义实体** 选项卡。</span><span class="sxs-lookup"><span data-stu-id="d7d6a-156">From the list of roles, select **dual-write app user** and select the **Custom Entities** tab.</span></span> 
4. <span data-ttu-id="d7d6a-157">验证角色对以下各项具有 **读取** 和 **追加到** 权限：</span><span class="sxs-lookup"><span data-stu-id="d7d6a-157">Verify that the role has **Read** and **Append To** permissions for:</span></span>

      - <span data-ttu-id="d7d6a-158">**货币汇率类型**</span><span class="sxs-lookup"><span data-stu-id="d7d6a-158">**Currency Exchange Rate Type**</span></span>
      - <span data-ttu-id="d7d6a-159">**会计科目表**</span><span class="sxs-lookup"><span data-stu-id="d7d6a-159">**Chart Of Accounts**</span></span> 
      - <span data-ttu-id="d7d6a-160">**会计日历**</span><span class="sxs-lookup"><span data-stu-id="d7d6a-160">**Fiscal Calendar**</span></span> 
      - <span data-ttu-id="d7d6a-161">**分类帐**</span><span class="sxs-lookup"><span data-stu-id="d7d6a-161">**Ledger**</span></span>

5. <span data-ttu-id="d7d6a-162">更新安全角色后，转到 **设置** > **安全** > **团队**。</span><span class="sxs-lookup"><span data-stu-id="d7d6a-162">After the security role is updated, go to **Settings** > **Security** > **Teams**.</span></span> <span data-ttu-id="d7d6a-163">确认 **双重写入应用用户** 角色已应用于团队。</span><span class="sxs-lookup"><span data-stu-id="d7d6a-163">Verify that the **dual-write app user** role has been applied to the team.</span></span> 

### <a name="refresh-data-entities-from-the-update"></a><a name="refresh"></a><span data-ttu-id="d7d6a-164">从更新刷新数据实体</span><span class="sxs-lookup"><span data-stu-id="d7d6a-164">Refresh data entities from the update</span></span>

1. <span data-ttu-id="d7d6a-165">在 Finance 环境中，打开 **数据管理** 工作区，然后打开 **Framework 参数** 页。</span><span class="sxs-lookup"><span data-stu-id="d7d6a-165">In your Finance environment, open the **Data management** workspace, and then open the **Framework parameters** page.</span></span>
2. <span data-ttu-id="d7d6a-166">在 **实体设置** 选项卡上，选择 **刷新实体列表**。</span><span class="sxs-lookup"><span data-stu-id="d7d6a-166">On the **Entity settings** tab, select **Refresh entity list**.</span></span>
3. <span data-ttu-id="d7d6a-167">选择 **关闭** 确认实体刷新。</span><span class="sxs-lookup"><span data-stu-id="d7d6a-167">Select **Close** to confirm the entity refresh.</span></span>

 > [!NOTE]
 > <span data-ttu-id="d7d6a-168">此过程大约需要 20 分钟完成。</span><span class="sxs-lookup"><span data-stu-id="d7d6a-168">This process will take approximately 20 minutes to complete.</span></span> <span data-ttu-id="d7d6a-169">刷新完成后，您会收到通知。</span><span class="sxs-lookup"><span data-stu-id="d7d6a-169">You will be notified when the refresh is complete.</span></span>

### <a name="update-dual-write-mappings"></a><a name="run"></a><span data-ttu-id="d7d6a-170">更新双重写入映射</span><span class="sxs-lookup"><span data-stu-id="d7d6a-170">Update dual-write mappings</span></span>

1. <span data-ttu-id="d7d6a-171">在 **数据管理** 工作区，选择 **双重写入**。</span><span class="sxs-lookup"><span data-stu-id="d7d6a-171">In the **Data management** workspace, select **Dual-write**.</span></span>
2. <span data-ttu-id="d7d6a-172">选择 **应用解决方案**，在列表中选择两个解决方案，然后选择 **应用**。</span><span class="sxs-lookup"><span data-stu-id="d7d6a-172">Select **Apply solutions**, select both solutions in the list, and then select **Apply**.</span></span>
3. <span data-ttu-id="d7d6a-173">在 **双重写入** 页上，选择以下表映射，然后选择 **停止**。</span><span class="sxs-lookup"><span data-stu-id="d7d6a-173">On the **Dual-write** page, select the following table maps, and then select **Stop**.</span></span>

    - <span data-ttu-id="d7d6a-174">**Project Operations 集成实际值 (msdyn_actuals)**</span><span class="sxs-lookup"><span data-stu-id="d7d6a-174">**Project Operations integration actuals (msdyn_actuals)**</span></span>
    - <span data-ttu-id="d7d6a-175">**Project Operations 集成项目支出类别 (msdyn_expensecategories)**</span><span class="sxs-lookup"><span data-stu-id="d7d6a-175">**Project Operations integration project expense categories (msdyn_expensecategories)**</span></span>
    - <span data-ttu-id="d7d6a-176">**Project Operations 集成实际值项目支出导出实体 (msdyn_expenses)**</span><span class="sxs-lookup"><span data-stu-id="d7d6a-176">**Project Operations integration actuals project expenses export entity (msdyn_expenses)**</span></span>

4. <span data-ttu-id="d7d6a-177">在 **表映射版本** 页上，对这三个实体的每个实体应用新版本的映射。</span><span class="sxs-lookup"><span data-stu-id="d7d6a-177">On the **Table map version** page, apply a new version of the map to each of the three entities.</span></span>
5. <span data-ttu-id="d7d6a-178">在 **双重写入** 页上，选择运行重新启动映射。</span><span class="sxs-lookup"><span data-stu-id="d7d6a-178">On the **Dual-write** page, select run to restart the maps.</span></span>
6. <span data-ttu-id="d7d6a-179">从映射列表中，选择具有所有先决条件的 **分类帐(msdyn_ledgers)** 映射，然后选中 **初始同步** 复选框。</span><span class="sxs-lookup"><span data-stu-id="d7d6a-179">From the list of maps, select the **Ledger (msdyn_ledgers)** map with all prerequisites and select the **Initial sync** check box.</span></span> 
7. <span data-ttu-id="d7d6a-180">在 **用于初始同步的主应用** 中，选择 **Finance and Operations 应用**，然后选择 **运行**。</span><span class="sxs-lookup"><span data-stu-id="d7d6a-180">In the **Master for initial sync** field, select **Finance and Operations apps** and then select **Run**.</span></span>
 
 ![分类帐映射同步](media/DW6.png)
 


[!INCLUDE[footer-include](../includes/footer-banner.md)]