---
title: Microsoft Project Client 集成
description: 规划和维护项目计划可能非常复杂，因此项目经理需要使用工具来帮助管理此任务。 与 Microsoft Project Client 的集成提供了对打开和管理项目工作分解结构的支持。
author: KimANelson
manager: AnnBe
ms.date: 12/11/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjWbsTemplate
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: c6478e05-50ee-4993-87f4-6ce9cb78f076
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2017-12-04
ms.dyn365.ops.version: 7.2999999999999998
ms.openlocfilehash: e35e1e54bad659d1329c333479830b680a17cbb0
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/24/2020
ms.locfileid: "3749765"
---
# <a name="microsoft-project-client-integration"></a><span data-ttu-id="bf8bd-104">Microsoft Project Client 集成</span><span class="sxs-lookup"><span data-stu-id="bf8bd-104">Microsoft Project client integration</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="bf8bd-105">规划和维护项目计划可能非常复杂，因此项目经理需要使用工具来帮助管理此任务。</span><span class="sxs-lookup"><span data-stu-id="bf8bd-105">Planning and maintaining a project schedule can be complex, so project managers need to use tools that help them manage this task.</span></span> <span data-ttu-id="bf8bd-106">与 Microsoft Project Client 的集成提供了对打开和管理项目工作分解结构的支持。</span><span class="sxs-lookup"><span data-stu-id="bf8bd-106">Integration with Microsoft Project Client provides support to open and manage a project work breakdown structure.</span></span> <span data-ttu-id="bf8bd-107">项目经理可将任何更改发布回 Dynamics 365 Finance 项目工作分解结构。</span><span class="sxs-lookup"><span data-stu-id="bf8bd-107">The project manager can publish any changes back to the Dynamics 365 Finance project work breakdown structure.</span></span>

> [!NOTE]
> <span data-ttu-id="bf8bd-108">如果您在使用 7 月更新（版本 10.0.4），您必须安装 KB 4054797 和 4055884。</span><span class="sxs-lookup"><span data-stu-id="bf8bd-108">If you are using the July update (version 10.0.4), you must install KB 4054797 and 4055884.</span></span>

## <a name="configure-the-microsoft-project-client-add-in"></a><span data-ttu-id="bf8bd-109">配置 Microsoft Project Client 加载项</span><span class="sxs-lookup"><span data-stu-id="bf8bd-109">Configure the Microsoft Project Client add-in</span></span>
<span data-ttu-id="bf8bd-110">若要实现与 Microsoft Project Client 集成，需要在用户的客户端 Microsoft Project 应用程序中安装 Microsoft Dynamics 365 加载项。</span><span class="sxs-lookup"><span data-stu-id="bf8bd-110">To enable the integration with Microsoft Project Client, a Microsoft Dynamics 365 add-in is required to be installed in the user’s client Microsoft Project application.</span></span> <span data-ttu-id="bf8bd-111">方法是打开**项目管理工作区**。</span><span class="sxs-lookup"><span data-stu-id="bf8bd-111">This is done by opening the **Project management workspace**.</span></span>

<span data-ttu-id="bf8bd-112">•   单击该工作区的**链接** > **设置**部分中的**配置项目客户端加载项**。</span><span class="sxs-lookup"><span data-stu-id="bf8bd-112">•   Click **Configure project client add-in** from the **Links** > **Setup** section of the workspace.</span></span>

<span data-ttu-id="bf8bd-113">•   单击**打开**，然后在系统提示时单击**运行**。</span><span class="sxs-lookup"><span data-stu-id="bf8bd-113">•   Click **Open**, then click **Run** when prompted.</span></span>

## <a name="open-and-edit-an-existing-draft-work-breakdown-structure-in-microsoft-project-client"></a><span data-ttu-id="bf8bd-114">在 Microsoft Project Client 中打开和编辑现有草稿工作分解结构</span><span class="sxs-lookup"><span data-stu-id="bf8bd-114">Open and edit an existing draft work breakdown structure in Microsoft Project Client</span></span>
<span data-ttu-id="bf8bd-115">如果已为 Dynamics 365 Finance 中的某个项目创建了工作分解结构，并且该工作分解结构处于草稿状态，则可在 Microsoft Project Client 应用程序中打开该工作分解结构。</span><span class="sxs-lookup"><span data-stu-id="bf8bd-115">If a project in Dynamics 365 Finance already has a work breakdown structure created, the work breakdown structure can be opened in the Microsoft Project Client application if the work breakdown structure is in a draft status.</span></span> <span data-ttu-id="bf8bd-116">若要从**项目**页面打开，请单击**计划**选项卡中的**在 Microsoft Project 中打开**链接。也可以从 Microsoft Project Client 应用程序内部打开该页面，方法是单击 **Microsoft Dynamics 365** 选项卡中的**打开**。从列表中选择**法人**和**项目**。</span><span class="sxs-lookup"><span data-stu-id="bf8bd-116">To open from the **Project** page, click **Open in Microsoft Project** link from the **Plan** tab. This page can also be opened from within the Microsoft Project Client application by clicking **Open** in the **Microsoft Dynamics 365** tab. Select the **Legal entity** and **Project** from the list.</span></span>

> [!NOTE]
> <span data-ttu-id="bf8bd-117">如果浏览器使用的是 Internet Explorer，则需要单击**保存**手动从文件下载到的位置打开。</span><span class="sxs-lookup"><span data-stu-id="bf8bd-117">If you're using Internet Explorer as your browser, you will need to click **Save** to manually open from the location that the file is downloaded to.</span></span> <span data-ttu-id="bf8bd-118">或者，单击 **保存并打开**以在 Microsoft Project Client 中打开文件。</span><span class="sxs-lookup"><span data-stu-id="bf8bd-118">Or, click **Save and open** to open the file in Microsoft Project Client.</span></span> <span data-ttu-id="bf8bd-119">保存时，请勿重命名文件。</span><span class="sxs-lookup"><span data-stu-id="bf8bd-119">Do not rename the file name when saving.</span></span>

<span data-ttu-id="bf8bd-120">使用 Microsoft Project Client 对文件进行任何编辑之前，需要将其签出。单击 **Microsoft Dynamics 365** 选项卡中的**签出**。这将阻止其他用户在同一时间从 Finance 内部编辑此工作分解结构。</span><span class="sxs-lookup"><span data-stu-id="bf8bd-120">Before making any edits to the file using Microsoft Project Client, you need to check it out. Click **Check out** in the **Microsoft Dynamics 365** tab. This will prevent other users from editing the work breakdown structure from within Finance at the same time.</span></span> <span data-ttu-id="bf8bd-121">若要在完成任何编辑之后发布工作分解结构，请单击 **Microsoft Dynamics 365** 选项卡上的**签入**。</span><span class="sxs-lookup"><span data-stu-id="bf8bd-121">To publish the work breakdown structure after completing any edits, click **Check in** on the **Microsoft Dynamics 365** tab.</span></span>

<span data-ttu-id="bf8bd-122">如果已在 Finance 中向项目添加了项目团队，将使用团队成员填充资源列表。</span><span class="sxs-lookup"><span data-stu-id="bf8bd-122">If a project team has already been added to the project in Finance, the resource list will be populated with the team members.</span></span> <span data-ttu-id="bf8bd-123">如果尚未向项目添加项目团队，可通过单击 **Microsoft Dynamics 365** 选项卡上的**资源**按钮，在 Microsoft Project Client 内部选择资源和建立团队。</span><span class="sxs-lookup"><span data-stu-id="bf8bd-123">If a project team has not yet been added to the project, you can select resources and build the team within Microsoft Project Client by clicking the **Resources** button on the **Microsoft Dynamics 365** tab.</span></span> 

<span data-ttu-id="bf8bd-124">签入期间，将把以下数据同步回 Finance ：</span><span class="sxs-lookup"><span data-stu-id="bf8bd-124">The following data will be synced back to Finance as part of the check-in process:</span></span>

<span data-ttu-id="bf8bd-125">•   任务名称</span><span class="sxs-lookup"><span data-stu-id="bf8bd-125">•   Task name</span></span>

<span data-ttu-id="bf8bd-126">•   开始日期</span><span class="sxs-lookup"><span data-stu-id="bf8bd-126">•   Start date</span></span>

<span data-ttu-id="bf8bd-127">•   完成日期</span><span class="sxs-lookup"><span data-stu-id="bf8bd-127">•   Finish date</span></span>

<span data-ttu-id="bf8bd-128">•   前置任务</span><span class="sxs-lookup"><span data-stu-id="bf8bd-128">•   Predecessors</span></span>

<span data-ttu-id="bf8bd-129">•   资源名称</span><span class="sxs-lookup"><span data-stu-id="bf8bd-129">•   Resource names</span></span>

<span data-ttu-id="bf8bd-130">•   类别</span><span class="sxs-lookup"><span data-stu-id="bf8bd-130">•   Category</span></span>

<span data-ttu-id="bf8bd-131">•   资源类别</span><span class="sxs-lookup"><span data-stu-id="bf8bd-131">•   Resource category</span></span>

<span data-ttu-id="bf8bd-132">•   工时</span><span class="sxs-lookup"><span data-stu-id="bf8bd-132">•   Work hours</span></span>

<span data-ttu-id="bf8bd-133">•   注释</span><span class="sxs-lookup"><span data-stu-id="bf8bd-133">•   Notes</span></span>

<span data-ttu-id="bf8bd-134">•   优先级</span><span class="sxs-lookup"><span data-stu-id="bf8bd-134">•   Priority</span></span>

> [!NOTE]
> <span data-ttu-id="bf8bd-135">如果向 Microsoft Project Client 文件添加其他任何列，这些列将不会保存到该文件，也不会在再次打开该文件时显示。</span><span class="sxs-lookup"><span data-stu-id="bf8bd-135">If you add any other columns to your Microsoft Project Client file, they will not be saved to the file and will not be displayed when the file is opened again.</span></span>

## <a name="create-the-work-breakdown-structure-for-an-existing-project-using-microsoft-project-client"></a><span data-ttu-id="bf8bd-136">使用 Microsoft Project Client 为现有项目创建工作分解结构</span><span class="sxs-lookup"><span data-stu-id="bf8bd-136">Create the work breakdown structure for an existing project using Microsoft Project Client</span></span>
<span data-ttu-id="bf8bd-137">若要使用 Microsoft Project Client 为现有项目创建新的工作分解结构，请执行以下步骤：</span><span class="sxs-lookup"><span data-stu-id="bf8bd-137">To create a new work breakdown structure using Microsoft Project Client, follow these steps:</span></span>


1.  <span data-ttu-id="bf8bd-138">打开 Microsoft Project Client。</span><span class="sxs-lookup"><span data-stu-id="bf8bd-138">Open Microsoft Project Client.</span></span>

2.  <span data-ttu-id="bf8bd-139">在 **Microsoft Dynamics 365** 选项卡上，单击**打开**。</span><span class="sxs-lookup"><span data-stu-id="bf8bd-139">On the **Microsoft Dynamics 365** tab, click **Open**.</span></span>

3.  <span data-ttu-id="bf8bd-140">选择项目的**法人**。</span><span class="sxs-lookup"><span data-stu-id="bf8bd-140">Select the **Legal entity** for the project.</span></span>

4.  <span data-ttu-id="bf8bd-141">选择**项目**。</span><span class="sxs-lookup"><span data-stu-id="bf8bd-141">Select the **Project**.</span></span>

5.  <span data-ttu-id="bf8bd-142">单击 **Microsoft Dynamics 365** 选项卡上的**签出**。</span><span class="sxs-lookup"><span data-stu-id="bf8bd-142">Click **Check out** on the **Microsoft Dynamics 365** tab.</span></span>

6.  <span data-ttu-id="bf8bd-143">准备好发布到 Finance 时，在 **Microsoft Dynamics 365** 选项卡上单击**签入**。</span><span class="sxs-lookup"><span data-stu-id="bf8bd-143">When ready to publish to Finance, click **Check in** on the **Microsoft Dynamics 365** tab.</span></span>

## <a name="replace-the-existing-work-breakdown-structure-for-an-existing-project-using-microsoft-project-client"></a><span data-ttu-id="bf8bd-144">使用 Microsoft Project Client 替换现有项目的现有工作分解结构</span><span class="sxs-lookup"><span data-stu-id="bf8bd-144">Replace the existing work breakdown structure for an existing project using Microsoft Project Client</span></span>
<span data-ttu-id="bf8bd-145">若要使用 Microsoft Project Client 创建新工作分解结构和替换现有项目的现有工作分解结构，请执行以下步骤：</span><span class="sxs-lookup"><span data-stu-id="bf8bd-145">To create a new work breakdown structure using Microsoft Project Client and replace an existing work breakdown structure for an existing project, follow these steps:</span></span>

1.  <span data-ttu-id="bf8bd-146">打开 Microsoft Project Client。</span><span class="sxs-lookup"><span data-stu-id="bf8bd-146">Open the Microsoft Project Client.</span></span>

2.  <span data-ttu-id="bf8bd-147">在 Microsoft Project Client 中创建计划。</span><span class="sxs-lookup"><span data-stu-id="bf8bd-147">Create the schedule in Microsoft Project Client.</span></span>

3.  <span data-ttu-id="bf8bd-148">在 **Microsoft Dynamics 365** 选项卡上，单击**保存更改** > **替换现有项目**。</span><span class="sxs-lookup"><span data-stu-id="bf8bd-148">On the **Microsoft Dynamics 365** tab, click **Save changes** > **Replace existing project**.</span></span>

4.  <span data-ttu-id="bf8bd-149">选择项目的**法人**。</span><span class="sxs-lookup"><span data-stu-id="bf8bd-149">Select the **Legal entity** for the project.</span></span>

5.  <span data-ttu-id="bf8bd-150">选择**项目**。</span><span class="sxs-lookup"><span data-stu-id="bf8bd-150">Select the **Project**.</span></span>

6.  <span data-ttu-id="bf8bd-151">单击**确定**。</span><span class="sxs-lookup"><span data-stu-id="bf8bd-151">Click **OK**.</span></span>

## <a name="create-a-new-project-from-within-microsoft-project-client"></a><span data-ttu-id="bf8bd-152">从 Microsoft Project Client 内部创建新项目</span><span class="sxs-lookup"><span data-stu-id="bf8bd-152">Create a new project from within Microsoft Project Client</span></span>


1.  <span data-ttu-id="bf8bd-153">打开 Microsoft Project Client。</span><span class="sxs-lookup"><span data-stu-id="bf8bd-153">Open the Microsoft Project Client.</span></span>

2.  <span data-ttu-id="bf8bd-154">在 Microsoft Project Client 中创建计划。</span><span class="sxs-lookup"><span data-stu-id="bf8bd-154">Create the schedule in Microsoft Project Client.</span></span>

3.  <span data-ttu-id="bf8bd-155">在 **Microsoft Dynamics 365** 选项卡上，单击**保存更改** > **保存到新项目**。</span><span class="sxs-lookup"><span data-stu-id="bf8bd-155">On the **Microsoft Dynamics 365** tab, click **Save changes** > **Save to new Project**.</span></span>

4.  <span data-ttu-id="bf8bd-156">选择项目的**法人**。</span><span class="sxs-lookup"><span data-stu-id="bf8bd-156">Select the **Legal entity** for the project.</span></span>

5.  <span data-ttu-id="bf8bd-157">必要时输入**项目 ID**。</span><span class="sxs-lookup"><span data-stu-id="bf8bd-157">Enter the **Project ID**, if necessary.</span></span>

6.  <span data-ttu-id="bf8bd-158">输入**项目名称**。</span><span class="sxs-lookup"><span data-stu-id="bf8bd-158">Enter the **Project name**.</span></span>

7.  <span data-ttu-id="bf8bd-159">选择**项目类型**、**项目组**和**项目合同 ID**。</span><span class="sxs-lookup"><span data-stu-id="bf8bd-159">Select the **Project type**, **Project group** and the **Project contract ID**.</span></span> <span data-ttu-id="bf8bd-160">也可以通过单击 **新建**创建新的项目合同。</span><span class="sxs-lookup"><span data-stu-id="bf8bd-160">Alternatively, you can create a new project contract by clicking **New**.</span></span>

8.  <span data-ttu-id="bf8bd-161">选择要用于安排资源的**日历**。</span><span class="sxs-lookup"><span data-stu-id="bf8bd-161">Select the **Calendar** to be used for resourcing.</span></span>

11. <span data-ttu-id="bf8bd-162">单击**确定**。</span><span class="sxs-lookup"><span data-stu-id="bf8bd-162">Click **OK**.</span></span>