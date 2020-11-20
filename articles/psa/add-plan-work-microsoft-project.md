---
title: 在 Microsoft Project 中使用 Project Service 加载项规划工作 | MicrosoftDocs
description: 此主题介绍如何在 Microsoft Project Service 中添加、配置和使用 Microsoft Project 加载项。
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 04/06/2019
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
ms.openlocfilehash: 6bc74442866caccc02e53afc913a55aab81f9629
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/28/2020
ms.locfileid: "4129667"
---
# <a name="use-the-project-service-automation-add-in-to-plan-your-work-in-microsoft-project"></a><span data-ttu-id="6dad7-103">在 Microsoft Project 中使用 Project Service Automation 加载项规划工作</span><span class="sxs-lookup"><span data-stu-id="6dad7-103">Use the Project Service Automation Add-in to plan your work in Microsoft Project</span></span>

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

[!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] <span data-ttu-id="6dad7-104">让您可以更轻松地执行项目规划，包括预计。</span><span class="sxs-lookup"><span data-stu-id="6dad7-104">makes it easier for you to do your project planning, including estimates.</span></span> <span data-ttu-id="6dad7-105">您可以自定义工作，以便成本、工作和销售值可以非常清晰，因为提交的是最终建议。</span><span class="sxs-lookup"><span data-stu-id="6dad7-105">You can define the work so that costs, effort, and sales value are clear as the final proposal is submitted.</span></span>  

 <span data-ttu-id="6dad7-106">现在可以在熟悉的 [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] 环境中安装 [!INCLUDE[pn_ms_dyn_365_psa_for_ms_project](../includes/pn-ms-dyn-365-psa-for-ms-project.md)] 和开展规划工作。</span><span class="sxs-lookup"><span data-stu-id="6dad7-106">Now you can install the [!INCLUDE[pn_ms_dyn_365_psa_for_ms_project](../includes/pn-ms-dyn-365-psa-for-ms-project.md)] and do your planning work in the familiar environment of [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].</span></span> <span data-ttu-id="6dad7-107">可使用 [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] 强大的规划和管理功能，然后在 Project Service Automation 中更新您的计划。</span><span class="sxs-lookup"><span data-stu-id="6dad7-107">Use the robust planning and management capabilities of [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] and then update your project plan in Project Service Automation.</span></span>  

> [!IMPORTANT]
> - <span data-ttu-id="6dad7-108">若要使用 SharePoint 文档管理为 [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] 项目存储 [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] 文件，[!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] 管理员需要开启文档管理。</span><span class="sxs-lookup"><span data-stu-id="6dad7-108">To use SharePoint document management to store your [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] files for [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] projects, your [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] admin will need to turn on document management.</span></span> 
> - <span data-ttu-id="6dad7-109">[!INCLUDE[pn_ms_dyn_365_psa_for_ms_project](../includes/pn-ms-dyn-365-psa-for-ms-project.md)] 仅兼容 [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] 2016 Professional Edition。</span><span class="sxs-lookup"><span data-stu-id="6dad7-109">The [!INCLUDE[pn_ms_dyn_365_psa_for_ms_project](../includes/pn-ms-dyn-365-psa-for-ms-project.md)] is only compatible with [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] 2016 Professional Edition.</span></span>  

## <a name="download-and-install-the-add-in"></a><span data-ttu-id="6dad7-110">下载并安装此加载项</span><span class="sxs-lookup"><span data-stu-id="6dad7-110">Download and install the add-in</span></span>  
 <span data-ttu-id="6dad7-111">准备好 [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] 登录信息。</span><span class="sxs-lookup"><span data-stu-id="6dad7-111">Have your [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] sign-in information ready.</span></span> <span data-ttu-id="6dad7-112">从 [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] 连接到 [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] 时需要此信息。</span><span class="sxs-lookup"><span data-stu-id="6dad7-112">You will need this information to connect from [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] to [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span></span>  

1.  <span data-ttu-id="6dad7-113">从下载中心下载适用于您的 Project Service 支持版本（[V2.X](https://go.microsoft.com/fwlink/?linkid=828268) 或 [V3.4+](https://www.microsoft.com/download/details.aspx?id=57956)）的加载项。</span><span class="sxs-lookup"><span data-stu-id="6dad7-113">From the Download Center, download the add-in for your supported version of Project Service, either [V2.X](https://go.microsoft.com/fwlink/?linkid=828268) or [V3.4+](https://www.microsoft.com/download/details.aspx?id=57956).</span></span>  

2.  <span data-ttu-id="6dad7-114">单击下载链接。</span><span class="sxs-lookup"><span data-stu-id="6dad7-114">Click the download link.</span></span>  

3.  <span data-ttu-id="6dad7-115">下载完成后，单击 **是** 安装此加载项。</span><span class="sxs-lookup"><span data-stu-id="6dad7-115">When the download is complete, click **Yes** to install the add-in.</span></span>  

## <a name="configure-the-add-in"></a><span data-ttu-id="6dad7-116">配置加载项</span><span class="sxs-lookup"><span data-stu-id="6dad7-116">Configure the add-in</span></span>  

1. <span data-ttu-id="6dad7-117">打开 [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] 并单击 **Project Service** 选项卡。</span><span class="sxs-lookup"><span data-stu-id="6dad7-117">Open [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] and click the **Project Service** tab.</span></span>  

2. <span data-ttu-id="6dad7-118">单击 **连接**。</span><span class="sxs-lookup"><span data-stu-id="6dad7-118">Click **Connect**.</span></span>  

3. <span data-ttu-id="6dad7-119">输入您的登录信息，然后单击 **登录**。</span><span class="sxs-lookup"><span data-stu-id="6dad7-119">Enter your sign-in information and then click **Sign in**.</span></span>  

   <span data-ttu-id="6dad7-120">现在可以开始使用此加载项。</span><span class="sxs-lookup"><span data-stu-id="6dad7-120">Now you can start using the add-in.</span></span>  

## <a name="read-from-a-template"></a><span data-ttu-id="6dad7-121">从模板读取</span><span class="sxs-lookup"><span data-stu-id="6dad7-121">Read from a template</span></span>  
 <span data-ttu-id="6dad7-122">从在 [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] 中创建并复制到 [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] 的模板读取，以便开始执行项目规划。</span><span class="sxs-lookup"><span data-stu-id="6dad7-122">Read from a template that you created in [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] and copied into [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] to start your project planning.</span></span> [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] <span data-ttu-id="6dad7-123">[创建项目模板 (Project Service Automation)](../psa/create-project-template.md)</span><span class="sxs-lookup"><span data-stu-id="6dad7-123">[Create a project template (Project Service Automation)](../psa/create-project-template.md)</span></span>  

1.  <span data-ttu-id="6dad7-124">在 **Project Service** 选项卡中，单击 **读取** > **Project Service Automation Project 模板**。</span><span class="sxs-lookup"><span data-stu-id="6dad7-124">From the **Project Service** tab, click **Read** > **Project Service Automation Project Template**.</span></span>  

2.  <span data-ttu-id="6dad7-125">从列表中选择一个项目模板，然后单击 **打开**。</span><span class="sxs-lookup"><span data-stu-id="6dad7-125">Choose a project template from the list and then click **Open**.</span></span>  

    > [!NOTE]
    >  <span data-ttu-id="6dad7-126">默认情况下，从模板复制到 Project 的任务设置为手动计划的。</span><span class="sxs-lookup"><span data-stu-id="6dad7-126">By default, the tasks that are copied from the template into Project are set as manually scheduled.</span></span>  

## <a name="assign-pn_project_service_auto-roles-to-project-resources"></a><span data-ttu-id="6dad7-127">将 [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] 角色分派给项目资源</span><span class="sxs-lookup"><span data-stu-id="6dad7-127">Assign [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] roles to project resources</span></span>  

1.  <span data-ttu-id="6dad7-128">打开项目，然后单击 **任务** 功能区。</span><span class="sxs-lookup"><span data-stu-id="6dad7-128">Open a project and click the **Task** ribbon.</span></span>  

2.  <span data-ttu-id="6dad7-129">单击 **甘特图** 菜单，然后选择 **资源工作表**。</span><span class="sxs-lookup"><span data-stu-id="6dad7-129">Click the **Gantt Chart** menu and then choose **Resource Sheet**.</span></span>  

3.  <span data-ttu-id="6dad7-130">在“资源工作表”中，单击 **Project Service资源角色** 下拉菜单，然后选择一个 Project Service Automation 角色。</span><span class="sxs-lookup"><span data-stu-id="6dad7-130">On the Resource Sheet, click the **Project Service Resource Role** drop-down menu and choose a Project Service Automation role.</span></span>  

## <a name="staff-your-project-with-resources"></a><span data-ttu-id="6dad7-131">为项目安排员工资源</span><span class="sxs-lookup"><span data-stu-id="6dad7-131">Staff your project with resources</span></span>  

1.  <span data-ttu-id="6dad7-132">从“Project Service”选项卡中选择一行，然后单击 **查找资源**。</span><span class="sxs-lookup"><span data-stu-id="6dad7-132">From the Project Service tab, select a row and click **Find Resources**.</span></span>  

2.  <span data-ttu-id="6dad7-133">在 **预订资源** 屏幕中，选择要用于该项目的资源。</span><span class="sxs-lookup"><span data-stu-id="6dad7-133">On the **Book Resource** screen, select the resource that you want to use for the project.</span></span>  

3.  <span data-ttu-id="6dad7-134">单击 **预订**，然后单击 **确定**。</span><span class="sxs-lookup"><span data-stu-id="6dad7-134">Click **Book** and then click **OK**.</span></span>  

## <a name="publish-your-project"></a><span data-ttu-id="6dad7-135">发布项目</span><span class="sxs-lookup"><span data-stu-id="6dad7-135">Publish your project</span></span>  
<span data-ttu-id="6dad7-136">项目规划完成后，下一步是导入项目并发布到 [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]。</span><span class="sxs-lookup"><span data-stu-id="6dad7-136">When your project planning is complete, the next step is to import and publish the project in to [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span></span>  

<span data-ttu-id="6dad7-137">项目将导入 [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]。</span><span class="sxs-lookup"><span data-stu-id="6dad7-137">The project will import into [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span></span> <span data-ttu-id="6dad7-138">将应用定价和团队生成流程。</span><span class="sxs-lookup"><span data-stu-id="6dad7-138">The pricing and team generation process are applied.</span></span> <span data-ttu-id="6dad7-139">在 [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] 中打开项目可以看到已生成了团队项目预计和工作分解结构。</span><span class="sxs-lookup"><span data-stu-id="6dad7-139">Open the project in [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] to see that the team, project estimates, and work breakdown structure has been generated.</span></span> <span data-ttu-id="6dad7-140">下表介绍结果的位置：</span><span class="sxs-lookup"><span data-stu-id="6dad7-140">The following table shows where to find the results:</span></span>


|                                                                                          |                                                                                                                                   |
|------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
|  [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] <span data-ttu-id="6dad7-141">**甘特图**</span><span class="sxs-lookup"><span data-stu-id="6dad7-141">**Gantt Chart**</span></span>   | <span data-ttu-id="6dad7-142">导入到 [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] **工作分解结构** 屏幕中。</span><span class="sxs-lookup"><span data-stu-id="6dad7-142">Imports into the [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] **Work Breakdown Structure** screen.</span></span> |
| [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] <span data-ttu-id="6dad7-143">**资源表**</span><span class="sxs-lookup"><span data-stu-id="6dad7-143">**Resource Sheet**</span></span> |   <span data-ttu-id="6dad7-144">导入到 [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] **项目团队成员** 屏幕中。</span><span class="sxs-lookup"><span data-stu-id="6dad7-144">Imports into the [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] **Project Team Members** screen.</span></span>   |
|   [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] <span data-ttu-id="6dad7-145">**使用情况**</span><span class="sxs-lookup"><span data-stu-id="6dad7-145">**Use Usage**</span></span>    |    <span data-ttu-id="6dad7-146">导入到 [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]**项目估算** 屏幕中。</span><span class="sxs-lookup"><span data-stu-id="6dad7-146">Omports into the [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] **Project Estimates** screen.</span></span>     |

<span data-ttu-id="6dad7-147">**导入和发布项目**</span><span class="sxs-lookup"><span data-stu-id="6dad7-147">**To import and publish your project**</span></span>  
1. <span data-ttu-id="6dad7-148">在 **Project Service** 选项卡中，单击 **发布** > **新 Project Service Automation Project 项目**。</span><span class="sxs-lookup"><span data-stu-id="6dad7-148">From the **Project Service** tab, click **Publish** > **New Project Service Automation Project**.</span></span>  

2. <span data-ttu-id="6dad7-149">在 **发布到 Project Service 中的新项目** 对话框中，输入 **项目名称**，然后选择 **客户**。</span><span class="sxs-lookup"><span data-stu-id="6dad7-149">On **Publish to a new project in Project Service** dialog box, enter the **Project Name** and select the **Customer**.</span></span>  

3. <span data-ttu-id="6dad7-150">或者，选中 **将项目计划链接到 Project Service Automation**，将计划的 Project 文件链接到 Project Service Automation。</span><span class="sxs-lookup"><span data-stu-id="6dad7-150">Optionally check the **Link project plan to Project Service Automation** to link the plan Project file to Project Service Automation.</span></span>  

4. <span data-ttu-id="6dad7-151">单击 **发布**。</span><span class="sxs-lookup"><span data-stu-id="6dad7-151">Click **Publish**.</span></span>  

   <span data-ttu-id="6dad7-152">将 Project 文件链接到 [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] 将让 Project 文件成为主文件，并在 [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] 中将工作分解结构设置为只读。</span><span class="sxs-lookup"><span data-stu-id="6dad7-152">Linking the Project file to [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] makes the Project file the master and sets the work breakdown structure in [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] to read-only.</span></span>  <span data-ttu-id="6dad7-153">若要更改项目计划，需要在 [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] 中更改，再作为更新发布到 [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]。</span><span class="sxs-lookup"><span data-stu-id="6dad7-153">In order to make changes to the project plan, you need to make them in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] and publish them as updates to [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span></span>  

## <a name="edit-a-project-thats-been-imported"></a><span data-ttu-id="6dad7-154">编辑已导入的项目</span><span class="sxs-lookup"><span data-stu-id="6dad7-154">Edit a project that’s been imported</span></span>  
 <span data-ttu-id="6dad7-155">可通过两种方法更改已导入 [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] 的项目计划：</span><span class="sxs-lookup"><span data-stu-id="6dad7-155">To make changes to a project plan that's been imported into [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)], you have two options:</span></span>  

- <span data-ttu-id="6dad7-156">在 [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] 中打开主文件并编辑。</span><span class="sxs-lookup"><span data-stu-id="6dad7-156">Open the master file and edit it in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].</span></span>  

- <span data-ttu-id="6dad7-157">取消链接文件并直接在 Project Service 中编辑。</span><span class="sxs-lookup"><span data-stu-id="6dad7-157">Unlink the file and edit it directly in Project Service.</span></span> <span data-ttu-id="6dad7-158">默认情况下，从 [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] 上传的项目已锁定，只能在 Project 中编辑。</span><span class="sxs-lookup"><span data-stu-id="6dad7-158">By default, a project that’s been uploaded from [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] is locked and can only be edited in Project.</span></span> <span data-ttu-id="6dad7-159">若要在 [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] 中编辑文件，必须将其取消链接。</span><span class="sxs-lookup"><span data-stu-id="6dad7-159">To edit the file in [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)], the file has to be unlinked.</span></span>  

### <a name="edit-in-pn_microsoft_project"></a><span data-ttu-id="6dad7-160">在 [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] 中编辑</span><span class="sxs-lookup"><span data-stu-id="6dad7-160">Edit in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]</span></span>  

1. <span data-ttu-id="6dad7-161">单击主菜单中的 **Project Service** > **项目**。</span><span class="sxs-lookup"><span data-stu-id="6dad7-161">From the main menu, click **Project Service** > **Projects**.</span></span>  

2. <span data-ttu-id="6dad7-162">从项目列表打开在 [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] 中创建的项目。</span><span class="sxs-lookup"><span data-stu-id="6dad7-162">From the list of projects, open the one you created in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].</span></span>  

3. <span data-ttu-id="6dad7-163">单击功能区中的 **在 MS Project 中打开**。</span><span class="sxs-lookup"><span data-stu-id="6dad7-163">Click **Open in MS Project** from the ribbon.</span></span> <span data-ttu-id="6dad7-164">这将在 [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] 中打开链接的主文件。</span><span class="sxs-lookup"><span data-stu-id="6dad7-164">This will open the linked master file in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].</span></span>  

### <a name="unlink-a-file-and-edit-in-pn_microsoft_project-service"></a><span data-ttu-id="6dad7-165">取消链接文件并在 [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] Service 中编辑</span><span class="sxs-lookup"><span data-stu-id="6dad7-165">Unlink a file and edit in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] Service</span></span>  

1. <span data-ttu-id="6dad7-166">单击主菜单中的 **Project Service** > **项目**。</span><span class="sxs-lookup"><span data-stu-id="6dad7-166">From the main menu, click **Project Service** > **Projects**.</span></span>  

2. <span data-ttu-id="6dad7-167">从项目列表打开在 [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] 中创建的项目。</span><span class="sxs-lookup"><span data-stu-id="6dad7-167">From the list of projects, open the one you created in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].</span></span>  

3. <span data-ttu-id="6dad7-168">单击功能区中的 **从 MS Project 取消链接**。</span><span class="sxs-lookup"><span data-stu-id="6dad7-168">Click **Unlink from MS Project** from the ribbon.</span></span>  

## <a name="upload-a-project-file-to-sharepoint-or-office-groups"></a><span data-ttu-id="6dad7-169">将 Project 文件上传到 SharePoint 或 Office Groups</span><span class="sxs-lookup"><span data-stu-id="6dad7-169">Upload a Project file to SharePoint or Office Groups</span></span>  
 <span data-ttu-id="6dad7-170">可以将 Project 文件上传到 SharePoint 并在 [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] 项目的“关联的文档”下找到。</span><span class="sxs-lookup"><span data-stu-id="6dad7-170">You can upload your Project file to SharePoint and find it under the Associated Documents for your [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] project.</span></span>  <span data-ttu-id="6dad7-171">需要请管理员为“项目”实体配置并开启 SharePoint 文档管理。</span><span class="sxs-lookup"><span data-stu-id="6dad7-171">You need to have your administrator configure SharePoint document management and turn it on for the Project entity.</span></span> 

 <span data-ttu-id="6dad7-172">如果您安装了 Office Groups，还可以将 Project 文件上传到 [!INCLUDE[pn_onedrive_for_business](../includes/pn-onedrive-for-business.md)]。</span><span class="sxs-lookup"><span data-stu-id="6dad7-172">You can also upload your Project file to [!INCLUDE[pn_onedrive_for_business](../includes/pn-onedrive-for-business.md)] if you have Office Groups set up.</span></span>

### <a name="upload-a-file-for-sharepoint"></a><span data-ttu-id="6dad7-173">为 SharePoint 上载文件</span><span class="sxs-lookup"><span data-stu-id="6dad7-173">Upload a file for SharePoint</span></span>  

1. <span data-ttu-id="6dad7-174">单击主菜单中的 **Project Service** > **上传**。</span><span class="sxs-lookup"><span data-stu-id="6dad7-174">From the main menu, click **Project Service** > **Upload**.</span></span>  

2. <span data-ttu-id="6dad7-175">选择 **到 Project Service Automation Project 文档**。</span><span class="sxs-lookup"><span data-stu-id="6dad7-175">Select **To Project Service Automation Project Documents**.</span></span>  

3. <span data-ttu-id="6dad7-176">在 **启用在 [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] 中打开** 对话框中，选择 **是** 或 **否**。</span><span class="sxs-lookup"><span data-stu-id="6dad7-176">On the **Enable Open in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** dialog, select **Yes** or **No**.</span></span>  

   - <span data-ttu-id="6dad7-177">如果单击 **是**，则可以在 Project Service Automation 中选择 **在 [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] 中打开** 按钮，启动 [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] 并从 SharePoint 文档库加载 Project 文件。</span><span class="sxs-lookup"><span data-stu-id="6dad7-177">If you click **Yes**, you'll be able select the **Open in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** button in Project Service Automation, launch [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)], and load the Project file from the SharePoint document library.</span></span>  

   - <span data-ttu-id="6dad7-178">如果单击 **否**，则 **在 [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] 中打开** 按钮的链接无效。</span><span class="sxs-lookup"><span data-stu-id="6dad7-178">If you click **No**, the link for the **Open in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** button won't work.</span></span>  

4. <span data-ttu-id="6dad7-179">可以在 [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] 中具体 [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] 项目的 **文档** 下找到 [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] 文件。</span><span class="sxs-lookup"><span data-stu-id="6dad7-179">The [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] file can be found in [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] under **Documents** for the specific [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] project.</span></span>  

### <a name="upload-a-file-for-office-groups"></a><span data-ttu-id="6dad7-180">为 Office Groups 上传文件</span><span class="sxs-lookup"><span data-stu-id="6dad7-180">Upload a file for Office Groups</span></span>  

1. <span data-ttu-id="6dad7-181">单击主菜单中的 **Project Service** > **上传**。</span><span class="sxs-lookup"><span data-stu-id="6dad7-181">From the main menu, click **Project Service** > **Upload**.</span></span>  

2. <span data-ttu-id="6dad7-182">选择 **到 Project Service Automation Project 文档**。</span><span class="sxs-lookup"><span data-stu-id="6dad7-182">Select **To Project Service Automation Project Documents**.</span></span>  

3. <span data-ttu-id="6dad7-183">在 **启用在 [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] 中打开** 对话框中，选择 **是** 或 **否**。</span><span class="sxs-lookup"><span data-stu-id="6dad7-183">On the **Enable Open in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** dialog, select **Yes** or **No**.</span></span>  

   - <span data-ttu-id="6dad7-184">如果单击 **是**，则可以在 Project Service Automation 中选择 **在 [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] 中打开** 按钮，启动 [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] 并从 SharePoint 文档库加载 Project 文件。</span><span class="sxs-lookup"><span data-stu-id="6dad7-184">If you click **Yes**, you'll be able to select the **Open in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** button in Project Service Automation, launch [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)], and load the Project file from the SharePoint document library.</span></span>  

   - <span data-ttu-id="6dad7-185">如果单击 **否**，则 **在 [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] 中打开** 按钮的链接无效。</span><span class="sxs-lookup"><span data-stu-id="6dad7-185">If you click **No**, the link for the **Open in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** button won't work.</span></span>  

4. <span data-ttu-id="6dad7-186">可以在 [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] 中具体 [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] 项目的 **文档** 下找到 [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] 文件。</span><span class="sxs-lookup"><span data-stu-id="6dad7-186">The [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] file can be found in [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] under **Documents** for the specific [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] project.</span></span>  

## <a name="publish--your-project-as-a-template"></a><span data-ttu-id="6dad7-187">将项目发布为模板</span><span class="sxs-lookup"><span data-stu-id="6dad7-187">Publish  your project as a template</span></span>  
 <span data-ttu-id="6dad7-188">可以通过在 [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] 中将项目保存为项目模板来保存项目并重复使用。</span><span class="sxs-lookup"><span data-stu-id="6dad7-188">You can save your project and reuse it by saving it as a project template in [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span></span>  <span data-ttu-id="6dad7-189">在 [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] 中，项目模板是可重复使用的项目计划。</span><span class="sxs-lookup"><span data-stu-id="6dad7-189">Project templates are reusable project plans in [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span></span> [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] <span data-ttu-id="6dad7-190">[创建项目模板 (Project Service Automation)](../psa/create-project-template.md)</span><span class="sxs-lookup"><span data-stu-id="6dad7-190">[Create a project template (Project Service Automation)](../psa/create-project-template.md)</span></span>  

1. <span data-ttu-id="6dad7-191">在 **Project Service** 选项卡中，单击 **发布** > **新 Project Service Automation Project 模板**。</span><span class="sxs-lookup"><span data-stu-id="6dad7-191">From the **Project Service** tab, click **Publish** > **New Project Service Automation Project Template**.</span></span>  

2. <span data-ttu-id="6dad7-192">在 **发布到 Project Service 模板中的新项目** 对话框中，输入 **项目模板名称**。</span><span class="sxs-lookup"><span data-stu-id="6dad7-192">On the **Publish to a new project in Project Service template** dialog box, enter the **Project template name**.</span></span>  

3. <span data-ttu-id="6dad7-193">也可以选中 **将项目计划链接到 Project Service Automation**，将 Project 文件链接到 [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]。</span><span class="sxs-lookup"><span data-stu-id="6dad7-193">Optionally, check the **Link project plan to Project Service Automation** to link the Project file to [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span></span>  

4. <span data-ttu-id="6dad7-194">单击 **发布**。</span><span class="sxs-lookup"><span data-stu-id="6dad7-194">Click **Publish**.</span></span>  

<span data-ttu-id="6dad7-195">将 Project 文件链接到 [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] 将让 Project 文件成为主文件，并在 [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] 模板中将工作分解结构设置为只读。</span><span class="sxs-lookup"><span data-stu-id="6dad7-195">Linking the Project file to [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] makes the Project file the master and sets the work breakdown structure in the [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] template to read-only.</span></span>  <span data-ttu-id="6dad7-196">若要更改项目计划，需要在 [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] 中更改，再作为更新发布到 [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]。</span><span class="sxs-lookup"><span data-stu-id="6dad7-196">In order to make changes to the project plan, you need to make them in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] and publish them as updates to [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span></span>

### <a name="see-also"></a><span data-ttu-id="6dad7-197">另请参阅</span><span class="sxs-lookup"><span data-stu-id="6dad7-197">See Also</span></span>  
 [<span data-ttu-id="6dad7-198">项目经理指南</span><span class="sxs-lookup"><span data-stu-id="6dad7-198">Project Manager Guide</span></span>](../psa/project-manager-guide.md)
