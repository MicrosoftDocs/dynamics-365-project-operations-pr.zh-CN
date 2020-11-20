---
title: 维护团队成员
description: 本主题介绍如何为项目团队预订指定资源和将其分派给任务。
author: ruhercul
manager: AnnBe
ms.date: 10/05/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: abab21ff98481166517be0c74a2c14c36d5e9d1d
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/28/2020
ms.locfileid: "4131512"
---
# <a name="maintain-team-members"></a><span data-ttu-id="e1b83-103">维护团队成员</span><span class="sxs-lookup"><span data-stu-id="e1b83-103">Maintain team members</span></span>

<span data-ttu-id="e1b83-104">_**适用于：** 基于资源/非库存场景的 Project Operations，精简部署 - 估价开票交易_</span><span class="sxs-lookup"><span data-stu-id="e1b83-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="e1b83-105">可向项目添加指定资源，方法是直接为团队预订这些资源。</span><span class="sxs-lookup"><span data-stu-id="e1b83-105">You can add a named resource to your project team by booking them directly to the team.</span></span>

1. <span data-ttu-id="e1b83-106">在 Dynamics 365 Project Operations 中，转到 **项目**，然后选择并打开要为其预订的项目。</span><span class="sxs-lookup"><span data-stu-id="e1b83-106">In Dynamics 365 Project Operations, go to **Projects**, and select the open the project that you're booking for.</span></span>
2. <span data-ttu-id="e1b83-107">在 **项目** 页的 **团队** 选项卡上，选择 **新建**。</span><span class="sxs-lookup"><span data-stu-id="e1b83-107">On the **Project** page, on the **Team** tab, select **New**.</span></span> 
3. <span data-ttu-id="e1b83-108">在 **快速创建项目团队成员** 对话框中，选择可预订资源。</span><span class="sxs-lookup"><span data-stu-id="e1b83-108">In the **Quick Create Project Team Member** dialog box, select the bookable resource.</span></span> <span data-ttu-id="e1b83-109">如果为资源分派了默认角色，将使用该角色填充 **角色** 字段。</span><span class="sxs-lookup"><span data-stu-id="e1b83-109">The **Role** field will populate with the resource's default role if they have one assigned.</span></span> <span data-ttu-id="e1b83-110">您可以更改角色。</span><span class="sxs-lookup"><span data-stu-id="e1b83-110">You can change the role.</span></span> 
4. <span data-ttu-id="e1b83-111">选择将需要资源的开始日期和结束日期，然后选择资源产能的分配方法。</span><span class="sxs-lookup"><span data-stu-id="e1b83-111">Select the from and to dates that the resource will be needed, and select the allocation method of the resource's capacity.</span></span> 
5. <span data-ttu-id="e1b83-112">如果希望该团队成员担任项目审批者，在 **项目审批者** 字段中选择 **是**。</span><span class="sxs-lookup"><span data-stu-id="e1b83-112">In the **Project Approver** field, select **Yes** if you want the team member to be a project approver.</span></span> <span data-ttu-id="e1b83-113">该团队成员可以审批为此项目提交的时间和支出条目。</span><span class="sxs-lookup"><span data-stu-id="e1b83-113">The team member can approve submitted time and expense entries for this project.</span></span> 
6. <span data-ttu-id="e1b83-114">选择 **保存**。</span><span class="sxs-lookup"><span data-stu-id="e1b83-114">Select **Save**.</span></span>

<span data-ttu-id="e1b83-115">可以将预订的资源分派给项目中的任务。</span><span class="sxs-lookup"><span data-stu-id="e1b83-115">You can now assign the booked resource to tasks on the project.</span></span> <span data-ttu-id="e1b83-116">在 **项目** 页中，在 **计划** 选项卡上，将任务分配给新资源。</span><span class="sxs-lookup"><span data-stu-id="e1b83-116">On the **Project** page, on the **Schedule** tab, assign tasks to the new resource.</span></span> <span data-ttu-id="e1b83-117">从任务网格中的 **资源** 字段启动的资源选取器将显示可选团队成员。</span><span class="sxs-lookup"><span data-stu-id="e1b83-117">The resource picker that is launched from the **Resources** field in the task grid will show the team members that you can select.</span></span>


<span data-ttu-id="e1b83-118">在 Project Operations 中，资源预订和任务分配不会紧密耦合。</span><span class="sxs-lookup"><span data-stu-id="e1b83-118">In Project Operations, resource bookings and task assignments aren't tightly coupled.</span></span> <span data-ttu-id="e1b83-119">当您在计划中使用资源选取器时，可以为团队成员分配比其在项目中的工时更多的任务工时。</span><span class="sxs-lookup"><span data-stu-id="e1b83-119">When you use the resource picker in the schedule, you can assign tasks to team members for more hours than their bookings cover on the project.</span></span>

<span data-ttu-id="e1b83-120">团队成员预订和分配之间的差异显示在 **团队** 和 **资源协调** 选项卡上。</span><span class="sxs-lookup"><span data-stu-id="e1b83-120">The differences between team member bookings and assignments are shown on the **Team** and **Resource Reconciliation** tabs.</span></span> <span data-ttu-id="e1b83-121">您还可以在更详细的级别协调资源的预订与分配之间的差异。</span><span class="sxs-lookup"><span data-stu-id="e1b83-121">You can also reconcile the differences between bookings and assignments for resources at a more detailed level.</span></span>

<span data-ttu-id="e1b83-122">使用 **计划** 选项卡上的资源选取器搜索和选择尚不属于项目团队的可预订资源。</span><span class="sxs-lookup"><span data-stu-id="e1b83-122">Use the resource picker on the **Schedule** tab to search for and select bookable resources that are not already part of the project team.</span></span> <span data-ttu-id="e1b83-123">这些资源在资源选取器中显示为 **其他资源**。</span><span class="sxs-lookup"><span data-stu-id="e1b83-123">These resources are shown in the resource picker as **Other Resources**.</span></span>

<span data-ttu-id="e1b83-124">当您进行选择时，将把资源添加到项目团队，并分配给任务，而不会生成任何预订。</span><span class="sxs-lookup"><span data-stu-id="e1b83-124">When you make a selection, the resource is added to the project team and assigned to the task, but no bookings are generated.</span></span>

<span data-ttu-id="e1b83-125">可使用 **协调** 选项卡的扩展预订功能或 **日程安排板** 为项目预订资源产能。</span><span class="sxs-lookup"><span data-stu-id="e1b83-125">You can use the **Reconciliation** tab’s extend booking capability or the **Schedule Board** to book the resource’s capacity to the project.</span></span>

<span data-ttu-id="e1b83-126">为项目预订团队成员之后，您可以使用 **维护预订** 或直接使用 **日程安排板** 来管理其预订。</span><span class="sxs-lookup"><span data-stu-id="e1b83-126">After a team member is booked on your project, you can use **Maintain bookings** or the **Schedule Board** directly to manage their bookings.</span></span>
