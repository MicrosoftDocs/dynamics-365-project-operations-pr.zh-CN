---
title: 创建资源分配
description: 此主题提供有关创建通用资源和指定资源分配的信息。
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: a6f4f12a962cb570e8b83d8ee7a01fc0cc2c6155
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/15/2021
ms.locfileid: "5287092"
---
# <a name="create-resource-assignments"></a><span data-ttu-id="560d2-103">创建资源分配</span><span class="sxs-lookup"><span data-stu-id="560d2-103">Create resource assignments</span></span>

<span data-ttu-id="560d2-104">_**适用于：** 基于资源/非库存场景的 Project Operations，精简部署 - 估价开票交易_</span><span class="sxs-lookup"><span data-stu-id="560d2-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="560d2-105">资源分配是项目团队成员与叶节点任务的直接关联。</span><span class="sxs-lookup"><span data-stu-id="560d2-105">A resource assignment is the direct association of a project team member to a leaf node task.</span></span> <span data-ttu-id="560d2-106">此主题提供有关分配资源的不同方法的信息。</span><span class="sxs-lookup"><span data-stu-id="560d2-106">This topic provides information about the different ways to assign resources.</span></span>

## <a name="create-a-generic-team-member-through-task-assignment"></a><span data-ttu-id="560d2-107">通过任务分派创建通用团队成员</span><span class="sxs-lookup"><span data-stu-id="560d2-107">Create a generic team member through task assignment</span></span>


<span data-ttu-id="560d2-108">通过任务分配创建通用团队成员时，将创建占位符或通用资源。</span><span class="sxs-lookup"><span data-stu-id="560d2-108">When you create a generic team member through task assignment, you create a placeholder or generic resource.</span></span> <span data-ttu-id="560d2-109">此通用资源描述您最终希望处理任务的指定资源的特征。</span><span class="sxs-lookup"><span data-stu-id="560d2-109">This generic resource describes the characteristics of the named resource you ultimately want to work on the tasks.</span></span> <span data-ttu-id="560d2-110">然后，您生成一个用于搜索和预订指定资源的要求，或使用要求提交请求。</span><span class="sxs-lookup"><span data-stu-id="560d2-110">You then generate a requirement, or submit a request using the requirement, that is used to search for and book the named resource.</span></span>

1. <span data-ttu-id="560d2-111">在任务的计划网格上，选择 **资源** 单元格中的资源图标。</span><span class="sxs-lookup"><span data-stu-id="560d2-111">On the Schedule grid for a task, select the Resource icon in the **Resource** cell.</span></span>
2. <span data-ttu-id="560d2-112">键入名称用作占位符资源的名称。</span><span class="sxs-lookup"><span data-stu-id="560d2-112">Type a name to serve as the placeholder resource’s name.</span></span> <span data-ttu-id="560d2-113">例如，“项目经理”。</span><span class="sxs-lookup"><span data-stu-id="560d2-113">For example, Program Manager.</span></span>
3. <span data-ttu-id="560d2-114">选择 **创建**，然后 **快速创建项目团队成员** 字段中，为通用资源设置角色。</span><span class="sxs-lookup"><span data-stu-id="560d2-114">Select **Create**, and in the **Quick Create Project Team Member** field, set the role for the generic resource.</span></span>
4. <span data-ttu-id="560d2-115">通过在任务的 **资源选择器** 上选择资源，将所需的任务分配给此占位符资源。</span><span class="sxs-lookup"><span data-stu-id="560d2-115">Assign tasks as needed to this placeholder resource by selecting the resource on the **Resource Selector** for the task.</span></span> <span data-ttu-id="560d2-116">资源在 **团队成员** 下列出。</span><span class="sxs-lookup"><span data-stu-id="560d2-116">The resources listed under **Team Members**.</span></span>
5. <span data-ttu-id="560d2-117">在完成分配通用资源后，在 **团队** 选项卡上，选择通用资源，然后选择 **生成要求** 为该通用资源创建资源要求。</span><span class="sxs-lookup"><span data-stu-id="560d2-117">When you’re finished assigning the generic resource, on the **Team** tab, select the generic resource, and then select **Generate Requirement** to create a resource requirement for the generic resource.</span></span>
6. <span data-ttu-id="560d2-118">为通用资源选择 **预订**，然后使用日程安排板查找和预订实际资源。</span><span class="sxs-lookup"><span data-stu-id="560d2-118">Select **Book** for the generic resource and then use the Schedule board to find and book a real resource.</span></span> <span data-ttu-id="560d2-119">您还可以提交由资源经理满足的要求。</span><span class="sxs-lookup"><span data-stu-id="560d2-119">You can also submit the requirement for fulfillment by a resource manager.</span></span>
7. <span data-ttu-id="560d2-120">当通用资源完全满足指定资源要求（满足部分资源要求不会进行资源分配）时，通用资源将被从团队中删除。</span><span class="sxs-lookup"><span data-stu-id="560d2-120">When the generic resource is fully fulfilled (partial resource requirement fulfillment will not result in a resource assignment) with a named resource, the generic resource is removed from the team.</span></span> <span data-ttu-id="560d2-121">通用资源的任务分配被分配给满足通用资源的资源要求的指定资源。</span><span class="sxs-lookup"><span data-stu-id="560d2-121">The task assignments for the generic resource are assigned to the named resource that fulfilled the generic resource’s resource requirement.</span></span>

## <a name="assign-a-named-resource-from-the-list-of-all-bookable-resources"></a><span data-ttu-id="560d2-122">从所有可预订资源列表分派指定资源</span><span class="sxs-lookup"><span data-stu-id="560d2-122">Assign a named resource from the list of all bookable resources</span></span>

<span data-ttu-id="560d2-123">您可以在 **资源选取器** 中使用搜索框来搜索所有可用的可预订资源，然后将其分配给叶节点任务。</span><span class="sxs-lookup"><span data-stu-id="560d2-123">You can use the search box in the **Resource Picker** to search all active bookable resources and assign them to any leaf node task.</span></span> <span data-ttu-id="560d2-124">将把按照这种方法分派的资源添加到无任何预订的团队。</span><span class="sxs-lookup"><span data-stu-id="560d2-124">Resources assigned this way are added to the team without any bookings.</span></span> <span data-ttu-id="560d2-125">这类似添加团队成员并选择 **无** 作为分配方法。</span><span class="sxs-lookup"><span data-stu-id="560d2-125">This is similar to adding a team member and selecting **None** as the allocation method.</span></span> <span data-ttu-id="560d2-126">资源在 **团队**、**资源分配** 和 **协调** 选项卡上将显示为仅具有分配和预订不足的资源。</span><span class="sxs-lookup"><span data-stu-id="560d2-126">The resource is displayed on the **Team**, **Resource Assignment**, and **Reconciliation** tabs as resources with only assignments and a booking deficit.</span></span> <span data-ttu-id="560d2-127">如果您要使用其可用性，请预订这些资源。</span><span class="sxs-lookup"><span data-stu-id="560d2-127">Book them if you want to use their availability.</span></span>

1. <span data-ttu-id="560d2-128">从任务网格、板或时间线，导航到 **分配到** 单元格。</span><span class="sxs-lookup"><span data-stu-id="560d2-128">From the task grid, board, or timeline, navigate to the **Assigned To** cell.</span></span>
2. <span data-ttu-id="560d2-129">在搜索框中，开始键入名称。</span><span class="sxs-lookup"><span data-stu-id="560d2-129">In the search box, start typing a name.</span></span> <span data-ttu-id="560d2-130">名称的搜索结果显示在 **资源选择器** 中 **其他资源** 下。</span><span class="sxs-lookup"><span data-stu-id="560d2-130">The search results for the name are displayed in the **Resource Selector** under **Other Resources**.</span></span>
3. <span data-ttu-id="560d2-131">选择要分配给任务的资源，或在 **其他团队资源** 下选择资源的名称。</span><span class="sxs-lookup"><span data-stu-id="560d2-131">Select the resource that you want to assign to the task or select the name of the resource under **Other Team Resources**.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]