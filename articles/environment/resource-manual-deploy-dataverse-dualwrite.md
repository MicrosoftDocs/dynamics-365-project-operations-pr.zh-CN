---
title: 通过双重写入支持手动部署 Project Operations Dataverse 应用
description: 本主题说明了如何手动部署 Project Operations Dataverse 应用，以便它支持双重写入。
author: stsporen
ms.date: 06/18/2021
ms.topic: article
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 2ad147da542fc9e7a2705da7a834d1a6512907e5
ms.sourcegitcommit: 205a94ab4168de25b102f31d00a691c8205ba63e
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/18/2021
ms.locfileid: "6273997"
---
# <a name="manually-deploy-the-project-operations-dataverse-app-with-dual-write-support"></a><span data-ttu-id="750e6-103">通过双重写入支持手动部署 Project Operations Dataverse 应用</span><span class="sxs-lookup"><span data-stu-id="750e6-103">Manually deploy the Project Operations Dataverse app with dual-write support</span></span>

<span data-ttu-id="750e6-104">_**适用于：** 面向资源/非库存场景的 Project Operations_</span><span class="sxs-lookup"><span data-stu-id="750e6-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="750e6-105">本主题说明了如何在 Microsoft Dataverse 中手动部署 Microsoft Dynamics 365 Project Operations，以便它支持双重写入。</span><span class="sxs-lookup"><span data-stu-id="750e6-105">This topic explains how to manually deploy Microsoft Dynamics 365 Project Operations in Microsoft Dataverse so that it supports dual-write.</span></span> <span data-ttu-id="750e6-106">Project Operations 可检测环境的配置，并在满足先决条件时添加对双重写入的额外支持。</span><span class="sxs-lookup"><span data-stu-id="750e6-106">Project Operations detects the environment's configuration and adds additional support for dual-write if the prerequisites are met.</span></span>

<span data-ttu-id="750e6-107">在通过 Microsoft Dynamics Lifecycle Services (LCS) 进行部署期间，如果您已按照本主题中的说明操作，可以跳过 Microsoft Power Platform 集成（以前称为 Common Data Service 环境）的部署。</span><span class="sxs-lookup"><span data-stu-id="750e6-107">During deployment through Microsoft Dynamics Lifecycle Services (LCS), if you've followed the instructions in this topic, you can skip the deployment of the Microsoft Power Platform integration (previously known as the Common Data Service environment).</span></span>

<span data-ttu-id="750e6-108">在 Dataverse 中部署 Project Operations 以使其支持双重写入的流程具有四个主要步骤：</span><span class="sxs-lookup"><span data-stu-id="750e6-108">The process of deploying Project Operations in Dataverse so that it supports dual-write has four main steps:</span></span>

1. <span data-ttu-id="750e6-109">[在 Dataverse 中创建支持双重写入的新环境](#create)。</span><span class="sxs-lookup"><span data-stu-id="750e6-109">[Create a new environment in Dataverse that supports dual-write](#create).</span></span>
2. <span data-ttu-id="750e6-110">[将双重写入先决条件添加到环境](#prerequisites)。</span><span class="sxs-lookup"><span data-stu-id="750e6-110">[Add dual-write prerequisites to the environment](#prerequisites).</span></span>
3. <span data-ttu-id="750e6-111">[添加 Project Operations Dataverse 应用](#dataverse)。</span><span class="sxs-lookup"><span data-stu-id="750e6-111">[Add the Project Operations Dataverse app](#dataverse).</span></span>
4. <span data-ttu-id="750e6-112">[链接您的环境](#link)。</span><span class="sxs-lookup"><span data-stu-id="750e6-112">[Link your environments](#link).</span></span>

## <a name="create-a-new-environment-in-dataverse-that-supports-dual-write"></a><a name="create"></a><span data-ttu-id="750e6-113">在 Dataverse 中创建支持双重写入的新环境</span><span class="sxs-lookup"><span data-stu-id="750e6-113">Create a new environment in Dataverse that supports dual-write</span></span>

<span data-ttu-id="750e6-114">若要完成此过程，您必须以管理员身份登录。</span><span class="sxs-lookup"><span data-stu-id="750e6-114">To complete this procedure, you must sign in as an administrator.</span></span>

1. <span data-ttu-id="750e6-115">打开 [Power Platform 管理中心](https://admin.powerplatform.com)，然后以管理员身份登录。</span><span class="sxs-lookup"><span data-stu-id="750e6-115">Open the [Power Platform admin center](https://admin.powerplatform.com), and sign in as an administrator.</span></span>
2. <span data-ttu-id="750e6-116">创建新环境并对其进行命名。</span><span class="sxs-lookup"><span data-stu-id="750e6-116">Create a new environment, and name it.</span></span>
3. <span data-ttu-id="750e6-117">选择环境类型。</span><span class="sxs-lookup"><span data-stu-id="750e6-117">Select the environment type.</span></span> <span data-ttu-id="750e6-118">如果您已注册试用产品/服务，请选择 **试用（基于订阅）**。</span><span class="sxs-lookup"><span data-stu-id="750e6-118">If you signed up for the trial offer, select **Trial (subscription-based)**.</span></span>
4. <span data-ttu-id="750e6-119">确认部署区域。</span><span class="sxs-lookup"><span data-stu-id="750e6-119">Confirm the deployment region.</span></span>
5. <span data-ttu-id="750e6-120">启用 **为此环境创建数据库** 选项。</span><span class="sxs-lookup"><span data-stu-id="750e6-120">Enable the **Create a database for this environment** option.</span></span> 
6. <span data-ttu-id="750e6-121">确认语言，然后确认货币与您的 Finance and Operations 应用的货币匹配。</span><span class="sxs-lookup"><span data-stu-id="750e6-121">Confirm the language, and then confirm that the currency matches the currency for your Finance and Operations apps.</span></span>
7. <span data-ttu-id="750e6-122">启用 **Dynamics 365 应用** 选项，并确认 **自动部署这些应用** 字段设置为 **无**。</span><span class="sxs-lookup"><span data-stu-id="750e6-122">Enable the **Dynamics 365 apps** option, and confirm that the **Automatically deploy these apps** field is set to **None**.</span></span>
8. <span data-ttu-id="750e6-123">如果需要安全组，请添加安全组。</span><span class="sxs-lookup"><span data-stu-id="750e6-123">Add a security group, if a security group is required.</span></span>
9. <span data-ttu-id="750e6-124">选择 **保存** 创建环境。</span><span class="sxs-lookup"><span data-stu-id="750e6-124">Select **Save** to create the environment.</span></span>
10. <span data-ttu-id="750e6-125">等待，直到部署完成，并且环境到达 **准备就绪** 状态。</span><span class="sxs-lookup"><span data-stu-id="750e6-125">Wait until the deployment is completed and the environment reaches the **Ready** state.</span></span>

## <a name="add-dual-write-prerequisites-to-the-environment"></a><a name="prerequisites"></a><span data-ttu-id="750e6-126">将双重写入先决条件添加到环境</span><span class="sxs-lookup"><span data-stu-id="750e6-126">Add dual-write prerequisites to the environment</span></span>

<span data-ttu-id="750e6-127">双重写入支持包括添加到关键实体（例如 **公司** 实体）的其他字段。</span><span class="sxs-lookup"><span data-stu-id="750e6-127">Dual-write support includes additional fields that are added to key entities, such as the **Company** entity.</span></span> <span data-ttu-id="750e6-128">如果您要向现有环境添加双重写入支持，可能必须更新数据才能启用该支持。</span><span class="sxs-lookup"><span data-stu-id="750e6-128">If you're adding dual-write support to an existing environment, you might have to update the data to enable the support.</span></span> <span data-ttu-id="750e6-129">有关如何启动数据的信息，请参阅[启动公司数据](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/bootstrap-company-data)。</span><span class="sxs-lookup"><span data-stu-id="750e6-129">For information about how to bootstrap the data, see [Bootstrap company data](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/bootstrap-company-data).</span></span> <span data-ttu-id="750e6-130">有关双重写入的详细信息，请参阅[双重写入系统要求](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-system-req)。</span><span class="sxs-lookup"><span data-stu-id="750e6-130">For more information about dual-write, see [Dual-write system requirements](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-system-req).</span></span>

<span data-ttu-id="750e6-131">完成此过程以将双重写入先决条件添加到您的环境。</span><span class="sxs-lookup"><span data-stu-id="750e6-131">Complete this procedure to add the dual-write prerequisites to your environment.</span></span>

1. <span data-ttu-id="750e6-132">打开您刚才创建的环境，然后转到 **资源** \> **Dynamics 365 应用**。</span><span class="sxs-lookup"><span data-stu-id="750e6-132">Open the environment that you just created, and then go to **Resource** \> **Dynamics 365 apps**.</span></span>
2. <span data-ttu-id="750e6-133">在应用列表中选择 **双重写入核心解决方案**，然后安装它。</span><span class="sxs-lookup"><span data-stu-id="750e6-133">Select **Dual-write core solution** in the app list, and install it.</span></span>
3. <span data-ttu-id="750e6-134">等待，直到安装完成。</span><span class="sxs-lookup"><span data-stu-id="750e6-134">Wait until the installation is completed.</span></span> <span data-ttu-id="750e6-135">然后，在应用列表中选择 **双重写入应用程序业务流程解决方案**，然后安装它。</span><span class="sxs-lookup"><span data-stu-id="750e6-135">Then select **Dual-write application orchestration solution** in the app list, and install it.</span></span>

## <a name="add-the-project-operations-dataverse-app"></a><a name="dataverse"></a><span data-ttu-id="750e6-136">添加 Project Operations Dataverse 应用</span><span class="sxs-lookup"><span data-stu-id="750e6-136">Add the Project Operations Dataverse app</span></span>

<span data-ttu-id="750e6-137">仅在安装 Project Operations 之前完成了前面的过程，才能完成此过程。</span><span class="sxs-lookup"><span data-stu-id="750e6-137">You can complete this procedure only if you completed the previous procedures before you installed Project Operations.</span></span> <span data-ttu-id="750e6-138">在安装期间，系统会分析环境配置，并添加对双重写入的支持（如果需要）。</span><span class="sxs-lookup"><span data-stu-id="750e6-138">During installation, the system analyzes the environment configuration and adds support for dual-write if it's required.</span></span>

1. <span data-ttu-id="750e6-139">打开您之前创建的环境，然后转到 **资源** \> **Dynamics 365 应用**。</span><span class="sxs-lookup"><span data-stu-id="750e6-139">Open the environment that you created earlier, and then go to **Resource** \> **Dynamics 365 apps**.</span></span>
2. <span data-ttu-id="750e6-140">在应用列表中选择 **Microsoft Dynamics 365 Project Operations**，然后安装它。</span><span class="sxs-lookup"><span data-stu-id="750e6-140">Select **Microsoft Dynamics 365 Project Operations** in the app list, and install it.</span></span>

## <a name="link-your-environments"></a><a name="link"></a><span data-ttu-id="750e6-141">链接您的环境</span><span class="sxs-lookup"><span data-stu-id="750e6-141">Link your environments</span></span>

<span data-ttu-id="750e6-142">在部署 Dataverse 环境后，您可以在 Finance and Operations 应用中设置链接。</span><span class="sxs-lookup"><span data-stu-id="750e6-142">After the Dataverse environment is deployed, you can set up the link in your Finance and Operations apps.</span></span> <span data-ttu-id="750e6-143">按照[使用双重写入向导链接您的环境](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/link-your-environment)中的步骤操作。</span><span class="sxs-lookup"><span data-stu-id="750e6-143">Follow the steps in [Use the dual-write wizard to link your environments](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/link-your-environment).</span></span>
