---
title: 将 Azure 订阅添加到 LCS 项目
description: 此主题提供有关如何将您的 Azure 订阅连接到 LCS 项目的信息。
author: sigitac
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: e741f35f9b229d2897cec06054d91ae620397228
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/30/2020
ms.locfileid: "4175790"
---
# <a name="add-an-azure-subscription-to-an-lcs-project"></a><span data-ttu-id="e8186-103">将 Azure 订阅添加到 LCS 项目</span><span class="sxs-lookup"><span data-stu-id="e8186-103">Add an Azure subscription to an LCS project</span></span>

<span data-ttu-id="e8186-104">_**适用于：** 面向资源/非库存场景的 Project Operations_</span><span class="sxs-lookup"><span data-stu-id="e8186-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="e8186-105">必须使用现有 Azure 订阅部署云托管环境。</span><span class="sxs-lookup"><span data-stu-id="e8186-105">Cloud-hosted environments must be deployed using an existing Azure subscription.</span></span> <span data-ttu-id="e8186-106">此主题说明如何将现有的 Azure 订阅连接到 LCS 项目。</span><span class="sxs-lookup"><span data-stu-id="e8186-106">This topic explains how to connect your existing Azure subscription to an LCS project.</span></span> 

## <a name="grant-admin-consent"></a><span data-ttu-id="e8186-107">授权管理员同意</span><span class="sxs-lookup"><span data-stu-id="e8186-107">Grant admin consent</span></span>

1. <span data-ttu-id="e8186-108">在 LCS 项目的 **环境** 部分，选择 **Microsoft Azure 设置**。</span><span class="sxs-lookup"><span data-stu-id="e8186-108">In your LCS project, in the **Environments** section, select **Microsoft Azure settings**.</span></span>

![Microsoft Azure 设置](./media/1MicrosoftAzureSettings.png)

2. <span data-ttu-id="e8186-110">在 **项目设置** 页上的 **Azure 连接器** 选项卡上，选择 **授权**。</span><span class="sxs-lookup"><span data-stu-id="e8186-110">On the **Project settings** page, on the **Azure connectors** tab, select **Authorize**.</span></span> <span data-ttu-id="e8186-111">这样即可以将环境部署到此项目。</span><span class="sxs-lookup"><span data-stu-id="e8186-111">This allows environments to be deployed to this project.</span></span>

![Azure 连接器](./media/2AzureConnectors.png)

3. <span data-ttu-id="e8186-113">再次选择 **授权** 提供管理员同意。</span><span class="sxs-lookup"><span data-stu-id="e8186-113">Select **Authorize** again to provide admin consent.</span></span>

![授权管理员同意](./media/3GrantAdminConsent.png)

4. <span data-ttu-id="e8186-115">接受权限请求。</span><span class="sxs-lookup"><span data-stu-id="e8186-115">Accept the permissions request.</span></span>

![接受权限请求](./media/4AcceptPermissionRequest.png)

<span data-ttu-id="e8186-117">授权现已完成。</span><span class="sxs-lookup"><span data-stu-id="e8186-117">The authorization is now complete.</span></span> 

![授权成功](./media/5AuthorizationComplete.png)

## <a name="provide-dynamics-deployment-services-access-to-your-azure-subscription"></a><a name="provide"></a><span data-ttu-id="e8186-119">提供对您的 Azure 订阅的 Dynamics 部署服务访问权限</span><span class="sxs-lookup"><span data-stu-id="e8186-119">Provide Dynamics Deployment Services access to your Azure subscription</span></span>

1. <span data-ttu-id="e8186-120">转到 [Microsoft Azure 记帐](https://portal.azure.com/#blade/Microsoft\_Azure\_Billing/SubscriptionsBlade)，选择您的订阅。</span><span class="sxs-lookup"><span data-stu-id="e8186-120">Go to [Microsoft Azure billing](https://portal.azure.com/#blade/Microsoft\_Azure\_Billing/SubscriptionsBlade) and select your subscription.</span></span> <span data-ttu-id="e8186-121">Dynamics 部署服务需要访问此订阅才能够部署环境。</span><span class="sxs-lookup"><span data-stu-id="e8186-121">Dynamics Deployment Services needs to access this subscription to be able to deploy environments.</span></span>

![Azure 订阅详细信息](./media/6AzureSubscription.png)

2. <span data-ttu-id="e8186-123">在导航窗格中选择 **访问控制 (IAM)**，然后选择 **添加角色分配**。</span><span class="sxs-lookup"><span data-stu-id="e8186-123">Select **Access control (IAM)** in the navigation pane, and then select **Add role assignment**.</span></span>
3. <span data-ttu-id="e8186-124">在右侧的滑块中，选择 **参与者角色**，在提供的列表中找到并选择 **Dynamics 部署服务**。</span><span class="sxs-lookup"><span data-stu-id="e8186-124">In the slider on the right side, select **Contributor role**, and in the list provided, find and select **Dynamics Deployment Services**.</span></span> 
4. <span data-ttu-id="e8186-125">选择 **保存**。</span><span class="sxs-lookup"><span data-stu-id="e8186-125">Select **Save**.</span></span>

![订阅访问](./media/7SubscriptionAccess.png)

### <a name="add-a-subscription-connector-to-an-lcs-project"></a><span data-ttu-id="e8186-127">将订阅连接器添加到 LCS 项目</span><span class="sxs-lookup"><span data-stu-id="e8186-127">Add a subscription connector to an LCS project</span></span>

1. <span data-ttu-id="e8186-128">在 LCS 项目的 **Microsoft Azure 设置** 页上，选择 **添加** 添加新连接器。</span><span class="sxs-lookup"><span data-stu-id="e8186-128">In your LCS project, on the **Microsoft Azure settings** page, select **Add** to add a new connector.</span></span>
2. <span data-ttu-id="e8186-129">输入 Azure 订阅 ID。</span><span class="sxs-lookup"><span data-stu-id="e8186-129">Enter your Azure subscription ID.</span></span> <span data-ttu-id="e8186-130">您可以在 [Azure 门户](https://ms.portal.azure.com/)中，在屏幕左下方的 **设置** 下找到您的 Azure 订阅 ID。</span><span class="sxs-lookup"><span data-stu-id="e8186-130">You can find your Azure subscription ID in the [Azure portal](https://ms.portal.azure.com/), under  **Settings**  in the lower left of the screen.</span></span>
3. <span data-ttu-id="e8186-131">在 **配置以使用 Azure 资源管理器** 字段中，选择 **是**。</span><span class="sxs-lookup"><span data-stu-id="e8186-131">In the **Configure to use Azure Resource Manager** field, select **Yes**.</span></span>
4. <span data-ttu-id="e8186-132">确保 Azure 的订阅 AAD 租户域与您所使用的域属 Azure 订阅匹配，然后选择 **下一步**。</span><span class="sxs-lookup"><span data-stu-id="e8186-132">Make sure Azure's Subscription AAD Tenant Domain matches the domain-owning Azure subscription that you are using, and select **Next**.</span></span>
5. <span data-ttu-id="e8186-133">在 **Microsoft Azure 设置** 屏幕上，选择 **下一步** 进行确认。</span><span class="sxs-lookup"><span data-stu-id="e8186-133">On the **Microsoft Azure Setup** screen, select **Next** to confirm.</span></span> <span data-ttu-id="e8186-134">如果在此屏幕上收到错误，请返回本主题中的[提供对 Azure 订阅的 Dynamics 部署服务访问权限](#provide)一节，确保您已完成所有步骤。</span><span class="sxs-lookup"><span data-stu-id="e8186-134">If you receive an error on this screen, return to the section [Provide Dynamics Deployment Services access to Azure subscription](#provide) in this topic and make sure you have completed all of the steps.</span></span>
6. <span data-ttu-id="e8186-135">将 Azure 管理证书下载到计算机上的本地文件夹，然后转到 **设置** > **管理证书**，将其上载到 Azure 管理门户。</span><span class="sxs-lookup"><span data-stu-id="e8186-135">Download the Azure Management Certificate to a local folder on your computer, and then upload it to Azure Management Portal by going to **Settings** > **Management Certificates**.</span></span> <span data-ttu-id="e8186-136">此证书可以让 LCS 代表您与 Azure 通信。</span><span class="sxs-lookup"><span data-stu-id="e8186-136">This certificate will enable LCS to communicate with Azure on your behalf.</span></span> <span data-ttu-id="e8186-137">如果您的用户具有对订阅的访问权限，可以跳过此步骤。</span><span class="sxs-lookup"><span data-stu-id="e8186-137">You can skip this step if your user has access to the subscription.</span></span>
7. <span data-ttu-id="e8186-138">选择 **下一步**。</span><span class="sxs-lookup"><span data-stu-id="e8186-138">Select  **Next**.</span></span>
8. <span data-ttu-id="e8186-139">选择要进行部署的 Azure 区域，然后选择一个靠近计划要使用此系统的位置的数据中心。</span><span class="sxs-lookup"><span data-stu-id="e8186-139">Select the Azure region to deploy in and select a data center that is close to where you plan to use this system.</span></span>
9.  <span data-ttu-id="e8186-140">选择 **连接**。</span><span class="sxs-lookup"><span data-stu-id="e8186-140">Select  **Connect**.</span></span>

<span data-ttu-id="e8186-141">您已成功连接 Azure 订阅。</span><span class="sxs-lookup"><span data-stu-id="e8186-141">You have successfully connected your Azure subscription.</span></span> <span data-ttu-id="e8186-142">现在，您可以部署 Dynamics 365 Finance 云托管环境了。</span><span class="sxs-lookup"><span data-stu-id="e8186-142">You can now deploy Dynamics 365 Finance cloud-hosted environments.</span></span>


