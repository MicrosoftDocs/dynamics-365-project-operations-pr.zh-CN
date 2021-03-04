---
title: 为项目团队预订指定的可预订资源和分派任务
description: 本主题介绍如何为项目团队预订指定资源和将其分派给任务。
author: JohnPBurrows
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 11/28/2018
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
ms.openlocfilehash: d8a49b6ae8423cb99c710e40704475b4a71d3724
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/10/2021
ms.locfileid: "5145347"
---
# <a name="book-named-bookable-resources-to-a-project-team-and-assign-tasks"></a><span data-ttu-id="c225a-103">为项目团队预订指定的可预订资源和分派任务</span><span class="sxs-lookup"><span data-stu-id="c225a-103">Book named bookable resources to a project team and assign tasks</span></span> 

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="c225a-104">可向项目添加指定资源，方法是直接为团队预订这些资源。</span><span class="sxs-lookup"><span data-stu-id="c225a-104">You can  add a named resource to your project team by booking them directly onto the team.</span></span> <span data-ttu-id="c225a-105">为此，请完成以下步骤：</span><span class="sxs-lookup"><span data-stu-id="c225a-105">To do this, complete the following steps.</span></span>

1. <span data-ttu-id="c225a-106">在 Project Service Automation 中，转到 **项目**，然后选择并打开要为其预订的项目。</span><span class="sxs-lookup"><span data-stu-id="c225a-106">In  Project Service Automation, go to **Projects**, and select the open the project that you are booking for.</span></span>
2. <span data-ttu-id="c225a-107">在 **项目** 页的 **团队** 选项卡上，单击 **新建**。</span><span class="sxs-lookup"><span data-stu-id="c225a-107">On the **Project** page, on the **Team** tab, click **New**.</span></span> 

![从“团队”选项卡添加团队成员](media/RM-how-to-1.png)

3. <span data-ttu-id="c225a-109">在 **快速创建项目团队成员** 对话框中，选择可预订资源。</span><span class="sxs-lookup"><span data-stu-id="c225a-109">In the **Quick Create Project Team Member** dialog box, select the bookable resource.</span></span> <span data-ttu-id="c225a-110">如果为资源分派了默认角色，将使用该角色填充 **角色** 字段。</span><span class="sxs-lookup"><span data-stu-id="c225a-110">The **Role** field will populate with the resource's default role if they have one assigned.</span></span> <span data-ttu-id="c225a-111">可以根据需要更改此角色。</span><span class="sxs-lookup"><span data-stu-id="c225a-111">You can change the role if needed.</span></span> 
4. <span data-ttu-id="c225a-112">选择将需要资源的开始日期和结束日期，然后选择资源产能的分配方法。</span><span class="sxs-lookup"><span data-stu-id="c225a-112">Select the from and to dates that the resource will be needed and select the allocation method of the resource's capacity.</span></span> 
5. <span data-ttu-id="c225a-113">如果希望该团队成员担任项目审批者，请在 **项目审批者** 字段中选择 **是**。</span><span class="sxs-lookup"><span data-stu-id="c225a-113">If you want the team member to be a project approver, select **Yes** in the **Project Approver** field.</span></span> <span data-ttu-id="c225a-114">这意味着该团队成员可以审批为此项目提交的时间和支出条目。</span><span class="sxs-lookup"><span data-stu-id="c225a-114">This will mean that the team member can approve submitted time and expense entries for this project.</span></span> 
6. <span data-ttu-id="c225a-115">单击 **保存**。</span><span class="sxs-lookup"><span data-stu-id="c225a-115">Click **Save**.</span></span>

![在快速创建窗体中添加团队成员](media/RM-how-to-2.png)


<span data-ttu-id="c225a-117">可以将预订的资源分派给项目中的任务。</span><span class="sxs-lookup"><span data-stu-id="c225a-117">You can now assign the booked resource to tasks on the project.</span></span> <span data-ttu-id="c225a-118">在 **项目** 页中，单击 **计划** 选项卡将任务分派给新资源。</span><span class="sxs-lookup"><span data-stu-id="c225a-118">On the **Project** page, click the **Schedule** tab to assign tasks to the new resource.</span></span> <span data-ttu-id="c225a-119">从任务网格中的 **资源** 字段启动的资源选取器将显示可选团队成员。</span><span class="sxs-lookup"><span data-stu-id="c225a-119">The resource picker that is launched from the **Resources** field in the task grid will show the team members that you can select.</span></span>

![在计划选项卡上为任务分派团队成员](media/RM-how-to-3.png)

<span data-ttu-id="c225a-121">在 Project Service Automation (PSA) 版本 3 中，资源预订与任务分派之间的关系不紧密。</span><span class="sxs-lookup"><span data-stu-id="c225a-121">In version 3 for Project Service Automation (PSA), resource bookings and task assignments are not tightly coupled.</span></span> <span data-ttu-id="c225a-122">这意味着当您在计划中使用资源选取器时，可以为团队成员分派比其在项目中的工时更多的任务工时。</span><span class="sxs-lookup"><span data-stu-id="c225a-122">This means that when you use the resource picker in the schedule, you can assign tasks to team members for more hours than their bookings cover on the project.</span></span>
<span data-ttu-id="c225a-123">可以在 **团队** 选项卡或 **资源协调** 选项卡中查看团队成员预订与分派之间的差异。也可以在更详细的级别协调资源的预订与分派之间的差异。</span><span class="sxs-lookup"><span data-stu-id="c225a-123">You can see the differences between team member bookings and assignments on the **Team** tab or on the **Resource Reconciliation** tab. You can also reconcile the differences between bookings and assignments for resources at a more detailed level.</span></span>

![“资源协调”选项卡](media/RM-how-to-4.png)

<span data-ttu-id="c225a-125">也可以使用 **计划** 选项卡上的资源选取器搜索和选择尚不属于项目团队的可预订资源。</span><span class="sxs-lookup"><span data-stu-id="c225a-125">You can also use the resource picker on the **Schedule** tab to search for and select bookable resources that are not already part of the project team.</span></span> <span data-ttu-id="c225a-126">这些在资源选取器中显示为 **其他资源**。</span><span class="sxs-lookup"><span data-stu-id="c225a-126">These are shown in the resource picker as **Other Resources**.</span></span>

![为任务分派非团队成员资源](media/RM-how-to-5.png)

<span data-ttu-id="c225a-128">执行此操作时，将把资源添加到项目团队，并分派给任务，而不会生成任何预订。</span><span class="sxs-lookup"><span data-stu-id="c225a-128">When you do this, the resource is added to the project team and assigned to the task, but no bookings are generated.</span></span>

![有分派，但无预订的团队成员](media/RM-how-to-6.png)

<span data-ttu-id="c225a-130">可使用 **协调** 选项卡的扩展预订功能或 **日程安排板** 为项目预订资源产能。</span><span class="sxs-lookup"><span data-stu-id="c225a-130">You can use the **Reconciliation** tab’s extend booking capability or the **Schedule Board** to book the resource’s capacity to the project.</span></span>

![在资源协调选项卡上扩展团队成员的预订](media/RM-how-to-7.png)

<span data-ttu-id="c225a-132">为项目预订团队成员之后，您可以使用维护预订或直接使用日程安排板来管理其预订。</span><span class="sxs-lookup"><span data-stu-id="c225a-132">After a team member is booked on your project, you can use maintain bookings or use the Schedule Board directly to manage their bookings.</span></span>
