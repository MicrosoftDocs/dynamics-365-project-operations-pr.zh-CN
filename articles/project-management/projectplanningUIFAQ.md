---
title: 在“任务”网格中工作故障排除
description: 本主题提供在“任务”网格中工作时所需的故障排除信息。
author: ruhercul
manager: tfehr
ms.date: 01/19/2021
ms.topic: article
ms.product: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 89bbad62c2a0a5693a57cf5c9a812ab644486469
ms.sourcegitcommit: c9edb4fc3042d97cb1245be627841e0a984dbdea
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/19/2021
ms.locfileid: "5031526"
---
# <a name="troubleshoot-working-in-the-task-grid"></a><span data-ttu-id="cc9fa-103">在“任务”网格中工作故障排除</span><span class="sxs-lookup"><span data-stu-id="cc9fa-103">Troubleshoot working in the Task grid</span></span> 

<span data-ttu-id="cc9fa-104">_**适用于：** 基于资源/非库存场景的 Project Operations，精简部署 - 估价开票交易_</span><span class="sxs-lookup"><span data-stu-id="cc9fa-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="cc9fa-105">本主题介绍如何解决使用成本管理时可能遇到的问题。</span><span class="sxs-lookup"><span data-stu-id="cc9fa-105">This topic describes how to fix issues that you might encounter while working with cost management.</span></span>

## <a name="enable-cookies"></a><span data-ttu-id="cc9fa-106">启用 Cookie</span><span class="sxs-lookup"><span data-stu-id="cc9fa-106">Enable cookies</span></span>

<span data-ttu-id="cc9fa-107">Project Operations 需要启用第三方 Cookie 来呈现工作分解结构。</span><span class="sxs-lookup"><span data-stu-id="cc9fa-107">Project Operations requires that third-party cookies be enabled in order to render the work breakdown structure.</span></span> <span data-ttu-id="cc9fa-108">如果未启用第三方 Cookie，在选择 **项目** 页上的 **任务** 选项卡时，您会看到空白页面，而不是看到任务。</span><span class="sxs-lookup"><span data-stu-id="cc9fa-108">When third-party cookies aren't enabled, instead of seeing tasks, you will see a blank page when you select the **Tasks** tab on the **Project** page.</span></span>

![未启用第三方 Cookie 时的空白选项卡](media/blankschedule.png)


### <a name="workaround"></a><span data-ttu-id="cc9fa-110">解决办法</span><span class="sxs-lookup"><span data-stu-id="cc9fa-110">Workaround</span></span>
<span data-ttu-id="cc9fa-111">对于 Microsoft Edge 或 Google Chrome 浏览器，以下过程概述了如何更新浏览器设置以启用第三方 Cookie。</span><span class="sxs-lookup"><span data-stu-id="cc9fa-111">For Microsoft Edge or Google Chrome browsers, the following procedures outline how to update your browser setting to enable third-party cookies.</span></span>

#### <a name="microsoft-edge"></a><span data-ttu-id="cc9fa-112">Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="cc9fa-112">Microsoft Edge</span></span>

1. <span data-ttu-id="cc9fa-113">打开 Edge 浏览器。</span><span class="sxs-lookup"><span data-stu-id="cc9fa-113">Open your Edge browser.</span></span>
2. <span data-ttu-id="cc9fa-114">在右上角选择 **省略号** (...)，然后选择 **设置**。</span><span class="sxs-lookup"><span data-stu-id="cc9fa-114">In the upper-right corner, select the **ellipsis** (...), and then select **Settings**.</span></span>
3. <span data-ttu-id="cc9fa-115">在 **Cookie 和站点权限** 下，选择 **Cookie 和站点数据**。</span><span class="sxs-lookup"><span data-stu-id="cc9fa-115">Under **Cookies and site permissions**, select **Cookies and site data**.</span></span>
4. <span data-ttu-id="cc9fa-116">关闭 **阻止第三方 Cookie**。</span><span class="sxs-lookup"><span data-stu-id="cc9fa-116">Turn off **Block third-party cookies**.</span></span>

#### <a name="google-chrome"></a><span data-ttu-id="cc9fa-117">Google Chrome</span><span class="sxs-lookup"><span data-stu-id="cc9fa-117">Google Chrome</span></span>

1. <span data-ttu-id="cc9fa-118">打开 Chrome 浏览器。</span><span class="sxs-lookup"><span data-stu-id="cc9fa-118">Open your Chrome browser.</span></span>
2. <span data-ttu-id="cc9fa-119">在右上角，选择三个垂直排列的点，然后选择 **设置**。</span><span class="sxs-lookup"><span data-stu-id="cc9fa-119">In the upper-right corner, select the three vertical dots, and then select **Settings**.</span></span>
3. <span data-ttu-id="cc9fa-120">在 **隐私和安全性** 下，选择 **Cookie 和其他站点数据**。</span><span class="sxs-lookup"><span data-stu-id="cc9fa-120">Under **Privacy and security**, select **Cookies and other site data**.</span></span>
4. <span data-ttu-id="cc9fa-121">选择 **允许所有 Cookie**。</span><span class="sxs-lookup"><span data-stu-id="cc9fa-121">Select **Allow all cookies**.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="cc9fa-122">如果您阻止第三方 Cookie，将阻止其他站点的所有 Cookie 和站点数据，即使您的例外列表中允许该站点。</span><span class="sxs-lookup"><span data-stu-id="cc9fa-122">If you block third-party cookies, all cookies and site data from other sites will be blocked, even if the site is allowed on your exceptions list.</span></span>

## <a name="pex-endpoint"></a><span data-ttu-id="cc9fa-123">PEX 终结点</span><span class="sxs-lookup"><span data-stu-id="cc9fa-123">PEX Endpoint</span></span>

<span data-ttu-id="cc9fa-124">Project Operations 需要项目参数引用 PEX 终结点。</span><span class="sxs-lookup"><span data-stu-id="cc9fa-124">Project Operations requires that a project parameter reference the PEX Endpoint.</span></span> <span data-ttu-id="cc9fa-125">需要此终结点与用于呈现工作分解结构的服务进行通信。</span><span class="sxs-lookup"><span data-stu-id="cc9fa-125">This endpoint is required to communicate with the service used to render the work breakdown structure.</span></span> <span data-ttu-id="cc9fa-126">如果未启用此参数，您将收到错误“项目参数无效”。</span><span class="sxs-lookup"><span data-stu-id="cc9fa-126">If the parameter isn't enabled, you will receive the error, "The project parameter is not valid".</span></span> 

### <a name="workaround"></a><span data-ttu-id="cc9fa-127">解决办法</span><span class="sxs-lookup"><span data-stu-id="cc9fa-127">Workaround</span></span>
 ![项目参数上的 PEX 终结点字段](media/projectparameter.png)

1. <span data-ttu-id="cc9fa-129">将 **PEX 终结点** 字段添加到 **项目参数** 页中。</span><span class="sxs-lookup"><span data-stu-id="cc9fa-129">Add the **PEX Endpoint** field to the **Project Parameters** page.</span></span>
2. <span data-ttu-id="cc9fa-130">使用以下值更新此字段：`https://project.microsoft.com/<lang>/?org=<cdsServer>#/taskgrid?projectId=\<id>&type=2`</span><span class="sxs-lookup"><span data-stu-id="cc9fa-130">Update the field with the following value: `https://project.microsoft.com/<lang>/?org=<cdsServer>#/taskgrid?projectId=\<id>&type=2`</span></span>
3. <span data-ttu-id="cc9fa-131">从 **项目参数** 页删除此字段。</span><span class="sxs-lookup"><span data-stu-id="cc9fa-131">Remove the field from the **Project Parameters** page.</span></span>

## <a name="privileges-for-project-for-the-web"></a><span data-ttu-id="cc9fa-132">Web 项目的特权</span><span class="sxs-lookup"><span data-stu-id="cc9fa-132">Privileges for Project for the Web</span></span>

<span data-ttu-id="cc9fa-133">Project Operations 依赖于外部计划服务。</span><span class="sxs-lookup"><span data-stu-id="cc9fa-133">Project Operations relies on an external scheduling service.</span></span> <span data-ttu-id="cc9fa-134">此服务需要用户分配有多个角色以可以读取和写入与工作分解结构相关的实体。</span><span class="sxs-lookup"><span data-stu-id="cc9fa-134">The service requires that a user have several roles assigned to read and write to entities related to the work breakdown structure.</span></span> <span data-ttu-id="cc9fa-135">这些实体包括项目任务、资源分配和任务依赖关系。</span><span class="sxs-lookup"><span data-stu-id="cc9fa-135">These entities include project tasks, resource assignments, and task dependencies.</span></span> <span data-ttu-id="cc9fa-136">如果用户在转到 **任务** 选项卡时无法呈现工作分解结构，可能是因为尚未启用 Project Operations 项目。</span><span class="sxs-lookup"><span data-stu-id="cc9fa-136">If a user can't render the work breakdown structure when they go to the **Tasks** tab, it's probably because Project for Project Operations hasn't been enabled.</span></span> <span data-ttu-id="cc9fa-137">用户可能会收到安全角色错误或与拒绝访问相关的错误。</span><span class="sxs-lookup"><span data-stu-id="cc9fa-137">A user might receive either a security role error, or an error related to a denial of access.</span></span>


## <a name="workaround"></a><span data-ttu-id="cc9fa-138">解决办法</span><span class="sxs-lookup"><span data-stu-id="cc9fa-138">Workaround</span></span>

1. <span data-ttu-id="cc9fa-139">转到 **设置 > 安全 > 用户 > 应用程序用户**。</span><span class="sxs-lookup"><span data-stu-id="cc9fa-139">Go to **Setting > Security > Users > Application Users**.</span></span>  

   ![应用程序读取器](media/applicationuser.jpg)
   
2. <span data-ttu-id="cc9fa-141">双击应用程序用户记录验证以下各项：</span><span class="sxs-lookup"><span data-stu-id="cc9fa-141">Double-click the application user record to verify the following:</span></span>

 - <span data-ttu-id="cc9fa-142">用户有权访问项目。</span><span class="sxs-lookup"><span data-stu-id="cc9fa-142">The user has access to the project.</span></span> <span data-ttu-id="cc9fa-143">此验证通常通过确保用户具有 **项目经理** 安全角色来完成。</span><span class="sxs-lookup"><span data-stu-id="cc9fa-143">This verification is typically done by ensuring that the user has **Project Manager** security role.</span></span>
 - <span data-ttu-id="cc9fa-144">Microsoft Project 应用程序用户已存在并且配置正确。</span><span class="sxs-lookup"><span data-stu-id="cc9fa-144">The Microsoft Project application user exists and is configured correctly.</span></span>
 
3. <span data-ttu-id="cc9fa-145">如果此用户不存在，您可以创建一个新用户记录。</span><span class="sxs-lookup"><span data-stu-id="cc9fa-145">If this user doesn't exist, you can create a new user record.</span></span> <span data-ttu-id="cc9fa-146">选择 **新建用户**。</span><span class="sxs-lookup"><span data-stu-id="cc9fa-146">Select **New Users**.</span></span> <span data-ttu-id="cc9fa-147">将输入窗体更改为 **应用程序用户**，然后添加 **应用程序 ID**。</span><span class="sxs-lookup"><span data-stu-id="cc9fa-147">Change the entry form to **Application User**, and then add the **Application ID**.</span></span>

   ![应用程序用户详细信息](media/applicationuserdetails.jpg)

4. <span data-ttu-id="cc9fa-149">在许可证的服务计划详细信息中验证是否已为用户分配了正确的许可证，并且已启用了服务。</span><span class="sxs-lookup"><span data-stu-id="cc9fa-149">Verify that the user has been assigned the correct license and that the service is enabled in the service plans details of the license.</span></span>
5. <span data-ttu-id="cc9fa-150">验证用户是否可以打开 project.microsoft.com。</span><span class="sxs-lookup"><span data-stu-id="cc9fa-150">Verify that the user can open project.microsoft.com.</span></span>
6. <span data-ttu-id="cc9fa-151">通过项目参数验证系统是否指向正确的项目终结点。</span><span class="sxs-lookup"><span data-stu-id="cc9fa-151">Verify through the project parameters that the system is pointing to the correct project endpoint.</span></span>
7. <span data-ttu-id="cc9fa-152">验证是否已创建项目应用程序用户。</span><span class="sxs-lookup"><span data-stu-id="cc9fa-152">Verify that the project application user is created.</span></span>
8. <span data-ttu-id="cc9fa-153">向用户应用以下安全角色：</span><span class="sxs-lookup"><span data-stu-id="cc9fa-153">Apply the following security roles to the user:</span></span>

  - <span data-ttu-id="cc9fa-154">Dataverse 用户</span><span class="sxs-lookup"><span data-stu-id="cc9fa-154">Dataverse User</span></span>
  - <span data-ttu-id="cc9fa-155">Project Operations 系统</span><span class="sxs-lookup"><span data-stu-id="cc9fa-155">Project Operations System</span></span>
  - <span data-ttu-id="cc9fa-156">项目系统</span><span class="sxs-lookup"><span data-stu-id="cc9fa-156">Project System</span></span>

## <a name="error-when-updating-the-work-breakdown-structure"></a><span data-ttu-id="cc9fa-157">更新工作分解结构时出错</span><span class="sxs-lookup"><span data-stu-id="cc9fa-157">Error when updating the work breakdown structure</span></span>

<span data-ttu-id="cc9fa-158">当对工作分解结构进行一个或多个更新时，更改最终失败并且未保存。</span><span class="sxs-lookup"><span data-stu-id="cc9fa-158">When one or more updates are made to the work breakdown structure, the changes eventually fail and aren't saved.</span></span> <span data-ttu-id="cc9fa-159">计划网格中出现错误，指出“无法保存您最近所作的更改。”</span><span class="sxs-lookup"><span data-stu-id="cc9fa-159">An error occurs in the schedule grid noting that “Recent change you’ve made couldn’t be saved.”</span></span>

### <a name="workaround"></a><span data-ttu-id="cc9fa-160">解决办法</span><span class="sxs-lookup"><span data-stu-id="cc9fa-160">Workaround</span></span>

1. <span data-ttu-id="cc9fa-161">在许可证的服务计划详细信息中验证是否已为用户分配了正确的许可证，并且已启用了服务。</span><span class="sxs-lookup"><span data-stu-id="cc9fa-161">Verify that the user has been assigned the correct license and that the service is enabled in the service plans details of the license.</span></span>
2. <span data-ttu-id="cc9fa-162">验证用户是否可以打开 project.microsoft.com。</span><span class="sxs-lookup"><span data-stu-id="cc9fa-162">Verify that the user can open project.microsoft.com.</span></span>
3. <span data-ttu-id="cc9fa-163">验证系统是否指向正确的项目终结点。</span><span class="sxs-lookup"><span data-stu-id="cc9fa-163">Verify that the system is pointing to the correct project endpoint,.</span></span>
4. <span data-ttu-id="cc9fa-164">验证是否已创建项目应用程序用户。</span><span class="sxs-lookup"><span data-stu-id="cc9fa-164">Verify that the Project Application user has been created.</span></span>
5. <span data-ttu-id="cc9fa-165">向用户应用以下安全角色：</span><span class="sxs-lookup"><span data-stu-id="cc9fa-165">Apply the following security roles to the user:</span></span>
  
  - <span data-ttu-id="cc9fa-166">Dataverse 用户或基本用户</span><span class="sxs-lookup"><span data-stu-id="cc9fa-166">Dataverse user or Base user</span></span>
  - <span data-ttu-id="cc9fa-167">Project Operations 系统</span><span class="sxs-lookup"><span data-stu-id="cc9fa-167">Project Operations System</span></span>
  - <span data-ttu-id="cc9fa-168">项目系统</span><span class="sxs-lookup"><span data-stu-id="cc9fa-168">Project System</span></span>
  - <span data-ttu-id="cc9fa-169">Project Operations 双重写入系统（如果要部署面向资源/非库存场景的 Project Operations，则需要此角色。）</span><span class="sxs-lookup"><span data-stu-id="cc9fa-169">Project Operations Dual Write System (This role is required if you are deploying the resource/non-stocked based scenario of Project Operations.)</span></span>
