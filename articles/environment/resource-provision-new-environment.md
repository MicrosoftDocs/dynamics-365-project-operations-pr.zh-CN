---
title: 设置新环境
description: 此主题提供有关如何设置新的 Project Operations 环境的信息。
author: sigitac
manager: Annbe
ms.date: 10/26/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 9ed502a1312b702e029d8910d62f72b8e0e4df06
ms.sourcegitcommit: 573be7e36604ace82b35e439cfa748aa7c587415
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/25/2020
ms.locfileid: "4642949"
---
# <a name="provision-a-new-environment"></a><span data-ttu-id="93395-103">设置新环境</span><span class="sxs-lookup"><span data-stu-id="93395-103">Provision a new environment</span></span>

<span data-ttu-id="93395-104">_**适用于：** 面向资源/非库存场景的 Project Operations_</span><span class="sxs-lookup"><span data-stu-id="93395-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="93395-105">此主题提供有关如何为资源/非库存场景预配新 Dynamics 365 Project Operations 环境的信息。</span><span class="sxs-lookup"><span data-stu-id="93395-105">This topic provides information about how to provision a new Dynamics 365 Project Operations environment for resource/non-stocked based scenarios.</span></span>

## <a name="enable-project-operations-automated-provisioning-in-an-lcs-project"></a><span data-ttu-id="93395-106">在 LCS 项目中启用 Project Operations 自动设置</span><span class="sxs-lookup"><span data-stu-id="93395-106">Enable Project Operations automated provisioning in an LCS project</span></span>

<span data-ttu-id="93395-107">请使用以下步骤为 LCS 项目启用 Project Operations 自动设置流。</span><span class="sxs-lookup"><span data-stu-id="93395-107">Use following steps to enable the Project Operations automated provisioning flow for your LCS project.</span></span>

1. <span data-ttu-id="93395-108">转到 [LCS](https://lcs.dynamics.com/v2)，选择 **预览功能管理** 磁贴。</span><span class="sxs-lookup"><span data-stu-id="93395-108">Go to [LCS](https://lcs.dynamics.com/v2) and select the **Preview Feature management** tile.</span></span>
2. <span data-ttu-id="93395-109">在 **预览功能** 列表中，选择 **Project Operations 功能**，然后选择 **已启用预览功能** 启用 Project Operations。</span><span class="sxs-lookup"><span data-stu-id="93395-109">In the **Preview feature** list, select **Project Operations Feature**, and then select **Preview feature enabled** to enable Project Operations.</span></span>

> [!NOTE]
> <span data-ttu-id="93395-110">每个 LCS 项目仅执行一次此步骤。</span><span class="sxs-lookup"><span data-stu-id="93395-110">This step is performed only one time per LCS project.</span></span>

## <a name="provision-a-project-operations-environment"></a><span data-ttu-id="93395-111">设置 Project Operations 环境</span><span class="sxs-lookup"><span data-stu-id="93395-111">Provision a Project Operations environment</span></span>

1. <span data-ttu-id="93395-112">打开新的 Dynamics 365 Finance [演示环境](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment)或[沙盒/生产环境](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deployenvironment-newinfrastructure)部署。</span><span class="sxs-lookup"><span data-stu-id="93395-112">Open a new Dynamics 365 Finance [demo environment](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment) or [sandbox/ production environment](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deployenvironment-newinfrastructure) deployment.</span></span> 
2. <span data-ttu-id="93395-113">**环境设置** 向导演练。</span><span class="sxs-lookup"><span data-stu-id="93395-113">Walk through the **Environment provisioning** wizard.</span></span> 

> [!IMPORTANT]
> <span data-ttu-id="93395-114">确保所选的应用程序版本为 10.0.13 或更高版本。</span><span class="sxs-lookup"><span data-stu-id="93395-114">Make sure selected application version is 10.0.13 or higher.</span></span>

3. <span data-ttu-id="93395-115">若要设置 Project Operations，在 **高级设置** 下选择 **Common Data Service**。</span><span class="sxs-lookup"><span data-stu-id="93395-115">To provision Project Operations, under **Advance settings**, select **Common Data Service**.</span></span> 
4. <span data-ttu-id="93395-116">选择 **是** 启用 **Common Data Service 设置**，然后在必填字段中输入信息：</span><span class="sxs-lookup"><span data-stu-id="93395-116">Enable the **Common Data Service Setting** by selecting **Yes** and then enter information in the required fields:</span></span>

  - <span data-ttu-id="93395-117">客户</span><span class="sxs-lookup"><span data-stu-id="93395-117">Name</span></span>
  - <span data-ttu-id="93395-118">区域</span><span class="sxs-lookup"><span data-stu-id="93395-118">Region</span></span>
  - <span data-ttu-id="93395-119">语言</span><span class="sxs-lookup"><span data-stu-id="93395-119">Language</span></span>
  - <span data-ttu-id="93395-120">货币</span><span class="sxs-lookup"><span data-stu-id="93395-120">Currency</span></span>
 
5. <span data-ttu-id="93395-121">在 **Common Data Service 模板** 字段中，选择 **Project Operations**</span><span class="sxs-lookup"><span data-stu-id="93395-121">In the **Common Data Service Template** field, select **Project Operations**</span></span> 

6. <span data-ttu-id="93395-122">选择部署的环境类型。</span><span class="sxs-lookup"><span data-stu-id="93395-122">Select the environment type for your deployment.</span></span> <span data-ttu-id="93395-123">通过基于订阅的试用，您可以在 30 天内部署 CDS 环境。</span><span class="sxs-lookup"><span data-stu-id="93395-123">A subscription-based trial will let you deploy a CDS environment for 30 days.</span></span> 

![部署设置](./media/1DeploymentSettings.png)

> [!IMPORTANT]
> <span data-ttu-id="93395-125">选择 **同意** 确认服务条款，然后选择 **完成** 返回部署设置。</span><span class="sxs-lookup"><span data-stu-id="93395-125">Select **Agree** to acknowledge the terms of service and then select **Done** to return to the deployment settings.</span></span>

![同意部署](./media/2DeploymentConsent.png)

7. <span data-ttu-id="93395-127">完成向导中的其余必填字段，并确认部署。</span><span class="sxs-lookup"><span data-stu-id="93395-127">Complete the remaining required fields in the wizard and confirm the deployment.</span></span> <span data-ttu-id="93395-128">环境设置时间因环境类型而异。</span><span class="sxs-lookup"><span data-stu-id="93395-128">Environment provisioning time varies based on the environment type.</span></span> <span data-ttu-id="93395-129">设置最多可能需要 6 个小时。</span><span class="sxs-lookup"><span data-stu-id="93395-129">Provisioning might take up to six hours.</span></span>

  <span data-ttu-id="93395-130">在成功完成部署后，环境将显示 **已部署**。</span><span class="sxs-lookup"><span data-stu-id="93395-130">After the deployment completes successfully, the environment will show as **Deployed**.</span></span>

8. <span data-ttu-id="93395-131">若要确认环境已成功部署，选择 **登录**，然后登录到环境进行确认。</span><span class="sxs-lookup"><span data-stu-id="93395-131">To confirm the environment has deployed successfully, select **Login** and log on to the environment to confirm.</span></span>

![ 环境详细信息](./media/3EnvironmentDetails.png)

## <a name="apply-project-operations-finance-demo-data-optional-step"></a><span data-ttu-id="93395-133">应用 Project Operations Finance 演示数据（可选步骤）</span><span class="sxs-lookup"><span data-stu-id="93395-133">Apply Project Operations Finance demo data (optional step)</span></span>

<span data-ttu-id="93395-134">如[本文](resource-apply-finance-demo-data.md)所述，将 Project Operations Finance 演示数据应用于 10.0.13 服务版本的云托管环境。</span><span class="sxs-lookup"><span data-stu-id="93395-134">Apply Project Operations Finance demo data to 10.0.13 service release Cloud Hosted Environment as described in [this article](resource-apply-finance-demo-data.md).</span></span>

## <a name="apply-updates-to-the-finance-environment"></a><span data-ttu-id="93395-135">将更新应用于 Finance 环境</span><span class="sxs-lookup"><span data-stu-id="93395-135">Apply updates to the Finance environment</span></span>

<span data-ttu-id="93395-136">Project Operations 需要应用程序版本为 **10.0.13 (10.0.569.20009)** 或更高的 Finance 环境。</span><span class="sxs-lookup"><span data-stu-id="93395-136">Project Operations requires a Finance environment with application version **10.0.13 (10.0.569.20009)** or higher.</span></span>

<span data-ttu-id="93395-137">您可能需要对您的 Finance 环境应用高质量更新才能获得此版本。</span><span class="sxs-lookup"><span data-stu-id="93395-137">You might need to apply quality updates to your Finance environment to receive this version.</span></span>

1. <span data-ttu-id="93395-138">在 LCS 中，在 **环境详细信息** 页上的 **可用更新** 部分，选择 **查看更新**。</span><span class="sxs-lookup"><span data-stu-id="93395-138">In LCS, on the **Environment details** page, in the **Available Updates** section, select **View Update**.</span></span>

![查看更新](./media/5ViewUpdates.png)

2. <span data-ttu-id="93395-140">在 **二进制更新** 页上，选择 **保存包**。</span><span class="sxs-lookup"><span data-stu-id="93395-140">On the **Binary updates** page, select **Save package.**</span></span>

![保存包](./media/6SavePackage.png)

3. <span data-ttu-id="93395-142">单击 **全选**，然后选择 **保存包**。</span><span class="sxs-lookup"><span data-stu-id="93395-142">Click **Select all** and then select **Save package**.</span></span>

![查看和保存更新](./media/7ReviewAndSaveUpdates.png)

4. <span data-ttu-id="93395-144">输入包的名称和说明，然后选择 **保存**。</span><span class="sxs-lookup"><span data-stu-id="93395-144">Enter a name and a description of the package, and then select **Save**.</span></span> <span data-ttu-id="93395-145">根据 Internet 连接的不同，此过程可能需要一些时间。</span><span class="sxs-lookup"><span data-stu-id="93395-145">Depending on the internet connection, this process might take some time.</span></span>

![将包上载到资产库](./media/8UploadPackageToAssetsLibrary.png)

5. <span data-ttu-id="93395-147">保存包后，请选择 **完成**，然后将此包保存到您的 LCS 项目的资产库中。</span><span class="sxs-lookup"><span data-stu-id="93395-147">After the package is saved, select **Done** and save this package to the Assets library in your LCS project.</span></span>

<span data-ttu-id="93395-148">保存和验证包可能需要约 15 分钟时间。</span><span class="sxs-lookup"><span data-stu-id="93395-148">Saving and validating the package might take ~15 minutes.</span></span>

6. <span data-ttu-id="93395-149">若要应用更新，导航到 LCS 中的 **环境详细信息** 页，选择 **维护** > **应用更新**。</span><span class="sxs-lookup"><span data-stu-id="93395-149">To apply the update, navigate to the **Environment details** page in LCS and select **Maintain** > **Apply updates**.</span></span>

![维护环境](./media/9MaintainEnvironment.png)

7. <span data-ttu-id="93395-151">在更新列表中，选择您创建的包，然后选择 **应用**。</span><span class="sxs-lookup"><span data-stu-id="93395-151">In the updates list select the package you created, and select **Apply**.</span></span>

![应用更新](./media/10ApplyUpdates.png)

<span data-ttu-id="93395-153">维护环境需要一些时间。</span><span class="sxs-lookup"><span data-stu-id="93395-153">Environment servicing will take some time.</span></span> <span data-ttu-id="93395-154">完成后，环境将返回到已部署状态。</span><span class="sxs-lookup"><span data-stu-id="93395-154">After it is complete, the environment will return to a deployed state.</span></span>

![环境已部署](./media/11EnvironmentDeployed.png)

## <a name="establish-a-dual-write-connection"></a><span data-ttu-id="93395-156">建立双写入连接</span><span class="sxs-lookup"><span data-stu-id="93395-156">Establish a Dual Write connection</span></span> 

1. <span data-ttu-id="93395-157">在您的 LCS 项目中，转到 **环境详细信息** 页。</span><span class="sxs-lookup"><span data-stu-id="93395-157">In your LCS project, go to the **Environment details** page.</span></span>
2. <span data-ttu-id="93395-158">在 **Common Data Service 环境信息** 下，选择 **链接到面向应用程序的 CDS**。</span><span class="sxs-lookup"><span data-stu-id="93395-158">Under **Common Data Service Environment Information**, select **Link to CDS for Apps**.</span></span>
3. <span data-ttu-id="93395-159">链接完成后，再次选择 **链接到面向应用程序的 CDS**。</span><span class="sxs-lookup"><span data-stu-id="93395-159">After the link is complete, select **Link to CDS for Apps** again.</span></span> <span data-ttu-id="93395-160">您将被重定向到 Finance 中的“双写入”。</span><span class="sxs-lookup"><span data-stu-id="93395-160">You will be redirected to Dual Write in Finance.</span></span>

![指向 CDS 的链接](./media/12LinktoCDS.png)

4. <span data-ttu-id="93395-162">选择 **应用解决方案** 访问将在集成中映射的实体。</span><span class="sxs-lookup"><span data-stu-id="93395-162">Select **Apply Solution** to access the entities that will be mapped in the integration.</span></span>

![应用解决方案](./media/13ApplySolutions.png)

5. <span data-ttu-id="93395-164">选择 **Dynamics 365 Finance and Operations 双重写入实体映射** 和 **Dynamics 365 Project Operations 双重写入实体映射** 这两个解决方案，然后选择 **应用**。</span><span class="sxs-lookup"><span data-stu-id="93395-164">Select both solutions, **Dynamics 365 Finance and Operations Dual Write Entity Map** and **Dynamics 365 Project Operations Dual Write Entity Maps**, and then select **Apply**.</span></span>

![确认解决方案](./media/14ConfirmSolutions.png)

<span data-ttu-id="93395-166">应用解决方案后，双写入实体将应用于环境。</span><span class="sxs-lookup"><span data-stu-id="93395-166">After the solutions are applied, the Dual Write entities are applied to the environment.</span></span>

![应用解决方案](./media/15ApplyingSolutions.png)

<span data-ttu-id="93395-168">应用实体后，所有可用映射都将在环境中列出。</span><span class="sxs-lookup"><span data-stu-id="93395-168">After the entities are applied, all available mappings are listed in the environment.</span></span>

![双写入映射](./media/15DWMappings.png)

## <a name="refresh-the-data-entities-after-the-update"></a><span data-ttu-id="93395-170">更新后刷新数据实体</span><span class="sxs-lookup"><span data-stu-id="93395-170">Refresh the data entities after the update</span></span>

1. <span data-ttu-id="93395-171">在 Finance 中，转到 **数据管理** 工作区。</span><span class="sxs-lookup"><span data-stu-id="93395-171">In Finance, go to the **Data management** workspace.</span></span>

![数据管理工作区](./media/16DataManagement.png)

2. <span data-ttu-id="93395-173">选择 **框架参数** 磁贴。</span><span class="sxs-lookup"><span data-stu-id="93395-173">Select the **Framework parameters** tile.</span></span>

![框架参数](./media/17FrameworkParameters.png)

3. <span data-ttu-id="93395-175">在 **实体设置** 页上，选择 **刷新实体列表**。</span><span class="sxs-lookup"><span data-stu-id="93395-175">On the **Entity settings** page, select **Refresh Entity list**.</span></span>

![刷新实体列表](./media/18RefreshEntityList.png)

<span data-ttu-id="93395-177">刷新时间大约需要 20 分钟。</span><span class="sxs-lookup"><span data-stu-id="93395-177">The refresh is going to take approximately 20 minutes.</span></span> <span data-ttu-id="93395-178">完成时，您将收到警报。</span><span class="sxs-lookup"><span data-stu-id="93395-178">You will receive an alert when it is complete.</span></span>

![刷新确认](./media/19RefreshConfirmation.png)

## <a name="run-project-operations-dual-write-maps"></a><span data-ttu-id="93395-180">运行 Project Operations 双写入映射</span><span class="sxs-lookup"><span data-stu-id="93395-180">Run Project Operations Dual Write maps</span></span>

1. <span data-ttu-id="93395-181">在您的 LCS 项目中，转到 **环境详细信息** 页。</span><span class="sxs-lookup"><span data-stu-id="93395-181">In your LCS project, go to the **Environment details** page.</span></span>
2. <span data-ttu-id="93395-182">在 **Common Data Service 环境信息** 下，选择 **链接到面向应用程序的 CDS**。</span><span class="sxs-lookup"><span data-stu-id="93395-182">Under **Common Data Service Environment Information**, select **Link to CDS for Apps.**</span></span> <span data-ttu-id="93395-183">选择链接后，您将被重定向到映射中的实体列表。</span><span class="sxs-lookup"><span data-stu-id="93395-183">After you select the link, you will be redirected to the list of entities in the mappings.</span></span>
3. <span data-ttu-id="93395-184">如下表所述启动映射。</span><span class="sxs-lookup"><span data-stu-id="93395-184">Start the maps as described in the following table.</span></span> <span data-ttu-id="93395-185">请确保按照列出的顺序操作。</span><span class="sxs-lookup"><span data-stu-id="93395-185">Make sure to follow the sequence as listed.</span></span>

| <span data-ttu-id="93395-186">**实体映射**</span><span class="sxs-lookup"><span data-stu-id="93395-186">**Entity Map**</span></span> | <span data-ttu-id="93395-187">**刷新实体**</span><span class="sxs-lookup"><span data-stu-id="93395-187">**Refresh entity**</span></span> | <span data-ttu-id="93395-188">**初始同步**</span><span class="sxs-lookup"><span data-stu-id="93395-188">**Initial sync**</span></span> | <span data-ttu-id="93395-189">**用于初始同步的主服务器**</span><span class="sxs-lookup"><span data-stu-id="93395-189">**Master for initial sync**</span></span> | <span data-ttu-id="93395-190">**运行先决条件**</span><span class="sxs-lookup"><span data-stu-id="93395-190">**Run prerequisites**</span></span> | <span data-ttu-id="93395-191">**先决条件初始同步**</span><span class="sxs-lookup"><span data-stu-id="93395-191">**Prerequisites initial sync**</span></span> |
| --- | --- | --- | --- | --- | --- |
| <span data-ttu-id="93395-192">**所有公司的项目资源角色 (bookableresourcecategories)**</span><span class="sxs-lookup"><span data-stu-id="93395-192">**Project Resource Roles for All Companies (bookableresourcecategories)**</span></span> | <span data-ttu-id="93395-193">No</span><span class="sxs-lookup"><span data-stu-id="93395-193">No</span></span> | <span data-ttu-id="93395-194">是</span><span class="sxs-lookup"><span data-stu-id="93395-194">Yes</span></span> | <span data-ttu-id="93395-195">Common Data Service</span><span class="sxs-lookup"><span data-stu-id="93395-195">Common Data Service</span></span> | <span data-ttu-id="93395-196">No</span><span class="sxs-lookup"><span data-stu-id="93395-196">No</span></span> | <span data-ttu-id="93395-197">不适用</span><span class="sxs-lookup"><span data-stu-id="93395-197">N\A</span></span> |
| <span data-ttu-id="93395-198">**法人 (cdm\_companies)**</span><span class="sxs-lookup"><span data-stu-id="93395-198">**Legal entities (cdm\_companies)**</span></span> | <span data-ttu-id="93395-199">No</span><span class="sxs-lookup"><span data-stu-id="93395-199">No</span></span> | <span data-ttu-id="93395-200">是</span><span class="sxs-lookup"><span data-stu-id="93395-200">Yes</span></span> | <span data-ttu-id="93395-201">Finance and Operations 应用</span><span class="sxs-lookup"><span data-stu-id="93395-201">Finance and Operations apps</span></span> | <span data-ttu-id="93395-202">No</span><span class="sxs-lookup"><span data-stu-id="93395-202">No</span></span> | <span data-ttu-id="93395-203">不适用</span><span class="sxs-lookup"><span data-stu-id="93395-203">N\A</span></span> |
| <span data-ttu-id="93395-204">**分类帐 (msdyn_ledgers)**</span><span class="sxs-lookup"><span data-stu-id="93395-204">**Ledger (msdyn_ledgers)**</span></span> | <span data-ttu-id="93395-205">No</span><span class="sxs-lookup"><span data-stu-id="93395-205">No</span></span> | <span data-ttu-id="93395-206">是</span><span class="sxs-lookup"><span data-stu-id="93395-206">Yes</span></span> | <span data-ttu-id="93395-207">Finance and Operations 应用</span><span class="sxs-lookup"><span data-stu-id="93395-207">Finance and Operations apps</span></span> | <span data-ttu-id="93395-208">是</span><span class="sxs-lookup"><span data-stu-id="93395-208">Yes</span></span> | <span data-ttu-id="93395-209">是，Finance and Operations 应用</span><span class="sxs-lookup"><span data-stu-id="93395-209">Yes, Finance and Operations apps</span></span> |
| <span data-ttu-id="93395-210">**Project Operations 集成实际值 (msdyn\_actuals)**</span><span class="sxs-lookup"><span data-stu-id="93395-210">**Project Operations integration actuals (msdyn\_actuals)**</span></span> | <span data-ttu-id="93395-211">No</span><span class="sxs-lookup"><span data-stu-id="93395-211">No</span></span> | <span data-ttu-id="93395-212">No</span><span class="sxs-lookup"><span data-stu-id="93395-212">No</span></span> | <span data-ttu-id="93395-213">不适用</span><span class="sxs-lookup"><span data-stu-id="93395-213">N\A</span></span> | <span data-ttu-id="93395-214">是</span><span class="sxs-lookup"><span data-stu-id="93395-214">Yes</span></span> | <span data-ttu-id="93395-215">No</span><span class="sxs-lookup"><span data-stu-id="93395-215">No</span></span> |
| <span data-ttu-id="93395-216">**项目合同子项 (salesorderdetails)**</span><span class="sxs-lookup"><span data-stu-id="93395-216">**Project contract lines (salesorderdetails)**</span></span> | <span data-ttu-id="93395-217">No</span><span class="sxs-lookup"><span data-stu-id="93395-217">No</span></span> | <span data-ttu-id="93395-218">No</span><span class="sxs-lookup"><span data-stu-id="93395-218">No</span></span> | <span data-ttu-id="93395-219">不适用</span><span class="sxs-lookup"><span data-stu-id="93395-219">N\A</span></span> | <span data-ttu-id="93395-220">No</span><span class="sxs-lookup"><span data-stu-id="93395-220">No</span></span> | <span data-ttu-id="93395-221">No</span><span class="sxs-lookup"><span data-stu-id="93395-221">No</span></span> |
| <span data-ttu-id="93395-222">**项目交易关系的集成实体 (msdyn\_transactionconnections)**</span><span class="sxs-lookup"><span data-stu-id="93395-222">**Integration entity for project transaction relationships (msdyn\_transactionconnections)**</span></span> | <span data-ttu-id="93395-223">No</span><span class="sxs-lookup"><span data-stu-id="93395-223">No</span></span> | <span data-ttu-id="93395-224">No</span><span class="sxs-lookup"><span data-stu-id="93395-224">No</span></span> | <span data-ttu-id="93395-225">不适用</span><span class="sxs-lookup"><span data-stu-id="93395-225">N\A</span></span> | <span data-ttu-id="93395-226">No</span><span class="sxs-lookup"><span data-stu-id="93395-226">No</span></span> | <span data-ttu-id="93395-227">不适用</span><span class="sxs-lookup"><span data-stu-id="93395-227">N\A</span></span> |
| <span data-ttu-id="93395-228">**Project Operations 集成合同子项里程碑 (msdyn\_contractlinesscheduleofvalues)**</span><span class="sxs-lookup"><span data-stu-id="93395-228">**Project Operations integration contract line milestones (msdyn\_contractlinesscheduleofvalues)**</span></span> | <span data-ttu-id="93395-229">No</span><span class="sxs-lookup"><span data-stu-id="93395-229">No</span></span> | <span data-ttu-id="93395-230">No</span><span class="sxs-lookup"><span data-stu-id="93395-230">No</span></span> | <span data-ttu-id="93395-231">不适用</span><span class="sxs-lookup"><span data-stu-id="93395-231">N\A</span></span> | <span data-ttu-id="93395-232">No</span><span class="sxs-lookup"><span data-stu-id="93395-232">No</span></span> | <span data-ttu-id="93395-233">不适用</span><span class="sxs-lookup"><span data-stu-id="93395-233">N\A</span></span> |
| <span data-ttu-id="93395-234">**用于支出预估的 Project Operations 集成实体 (msdyn\_estimateslines)**</span><span class="sxs-lookup"><span data-stu-id="93395-234">**Project Operations integration entity for expense estimates (msdyn\_estimateslines)**</span></span> | <span data-ttu-id="93395-235">No</span><span class="sxs-lookup"><span data-stu-id="93395-235">No</span></span> | <span data-ttu-id="93395-236">No</span><span class="sxs-lookup"><span data-stu-id="93395-236">No</span></span> | <span data-ttu-id="93395-237">不适用</span><span class="sxs-lookup"><span data-stu-id="93395-237">N\A</span></span> | <span data-ttu-id="93395-238">No</span><span class="sxs-lookup"><span data-stu-id="93395-238">No</span></span> | <span data-ttu-id="93395-239">不适用</span><span class="sxs-lookup"><span data-stu-id="93395-239">N\A</span></span> |
| <span data-ttu-id="93395-240">**Project Operations 集成项目支出类别导出实体 (msdyn\_expensecategories)**</span><span class="sxs-lookup"><span data-stu-id="93395-240">**Project Operations integration project expense categories export entity (msdyn\_expensecategories)**</span></span> | <span data-ttu-id="93395-241">No</span><span class="sxs-lookup"><span data-stu-id="93395-241">No</span></span> | <span data-ttu-id="93395-242">No</span><span class="sxs-lookup"><span data-stu-id="93395-242">No</span></span> | <span data-ttu-id="93395-243">不适用</span><span class="sxs-lookup"><span data-stu-id="93395-243">N\A</span></span> | <span data-ttu-id="93395-244">No</span><span class="sxs-lookup"><span data-stu-id="93395-244">No</span></span> | <span data-ttu-id="93395-245">不适用</span><span class="sxs-lookup"><span data-stu-id="93395-245">N\A</span></span> |
| <span data-ttu-id="93395-246">**Project Operations 集成项目支出导出实体 (msdyn\_expenses)**</span><span class="sxs-lookup"><span data-stu-id="93395-246">**Project Operations integration project expenses export entity (msdyn\_expenses)**</span></span> | <span data-ttu-id="93395-247">是</span><span class="sxs-lookup"><span data-stu-id="93395-247">Yes</span></span> | <span data-ttu-id="93395-248">No</span><span class="sxs-lookup"><span data-stu-id="93395-248">No</span></span> | <span data-ttu-id="93395-249">不适用</span><span class="sxs-lookup"><span data-stu-id="93395-249">N\A</span></span> | <span data-ttu-id="93395-250">No</span><span class="sxs-lookup"><span data-stu-id="93395-250">No</span></span> | <span data-ttu-id="93395-251">不适用</span><span class="sxs-lookup"><span data-stu-id="93395-251">N\A</span></span> |
| <span data-ttu-id="93395-252">**用于工时预估的 Project Operations 集成实体 (msdyn\_resourceassignments)**</span><span class="sxs-lookup"><span data-stu-id="93395-252">**Project Operations integration entity for hour estimates (msdyn\_resourceassignments)**</span></span> | <span data-ttu-id="93395-253">是</span><span class="sxs-lookup"><span data-stu-id="93395-253">Yes</span></span> | <span data-ttu-id="93395-254">No</span><span class="sxs-lookup"><span data-stu-id="93395-254">No</span></span> | <span data-ttu-id="93395-255">不适用</span><span class="sxs-lookup"><span data-stu-id="93395-255">N\A</span></span> | <span data-ttu-id="93395-256">No</span><span class="sxs-lookup"><span data-stu-id="93395-256">No</span></span> | <span data-ttu-id="93395-257">不适用</span><span class="sxs-lookup"><span data-stu-id="93395-257">N\A</span></span> |


4. <span data-ttu-id="93395-258">若要刷新实体，选择映射名称，然后选择 **刷新实体**。</span><span class="sxs-lookup"><span data-stu-id="93395-258">To refresh the entity, select the map name, and then select **Refresh entities**.</span></span> 


![刷新映射](./media/20RefreshMapping.png)

5. <span data-ttu-id="93395-260">刷新完成后，运行映射。</span><span class="sxs-lookup"><span data-stu-id="93395-260">After the refresh is complete, run the map.</span></span> <span data-ttu-id="93395-261">在启用下一个映射之前，验证表中的映射是否处于 **正在运行** 状态。</span><span class="sxs-lookup"><span data-stu-id="93395-261">Before you enable the next map, verify that the map in the table is in a state of **Running**.</span></span> <span data-ttu-id="93395-262">运行具有大量先决条件的映射可能需要一些时间。</span><span class="sxs-lookup"><span data-stu-id="93395-262">Running maps with a larger number of prerequisites might take some time.</span></span>

<span data-ttu-id="93395-263">要运行具有先决条件的映射，请启用 **显示相关实体映射** 切换。</span><span class="sxs-lookup"><span data-stu-id="93395-263">To run a map with prerequisites, enable the **Show related entity maps** toggle.</span></span> <span data-ttu-id="93395-264">如果表中指示 **先决条件初始同步** 为 **否**，请在运行前确认 **初始同步** 标志在所有先决条件映射中均为 **关闭**。</span><span class="sxs-lookup"><span data-stu-id="93395-264">If the table indicates **Prerequisite initial sync** is **No**, verify that the **Initial sync** flag is **Off** in all the prerequisite maps before you run it.</span></span>

![运行映射](./media/21RunMap.png)

6. <span data-ttu-id="93395-266">验证所有项目相关映射是否处于运行状态。</span><span class="sxs-lookup"><span data-stu-id="93395-266">Validate all project related maps are in the running state.</span></span>

![所有映射正在运行](./media/22AllMapsRunning.png)


## <a name="apply-configuration-data-in-cds-for-project-operations-optional"></a><span data-ttu-id="93395-268">在 Project Operations 的 CDS 中应用配置数据（可选）</span><span class="sxs-lookup"><span data-stu-id="93395-268">Apply configuration data in CDS for Project Operations (optional)</span></span>

<span data-ttu-id="93395-269">如果已将演示数据应用到 Finance 环境，请参阅[在 Project Operations 的 Common Data Service 中设置和应用配置数据](resource-apply-pro-setup-config-data.md)将演示数据应用到 CDS 环境。</span><span class="sxs-lookup"><span data-stu-id="93395-269">If you have applied demo data to the Finance environment, see [Set up and apply configuration data in the Common Data Service for Project Operations](resource-apply-pro-setup-config-data.md) to apply demo data to CDS environment.</span></span>


<span data-ttu-id="93395-270">您的 Project Operations 环境现在已经完成了设置和配置。</span><span class="sxs-lookup"><span data-stu-id="93395-270">Your Project Operations environment is now provisioned and configured.</span></span> 
